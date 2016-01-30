---
layout: webview
title: Test Webview
analytics: true
---

<script type="text/javascript">
  var accountKey, sustainTime
  SomApi.account = accountKey
  SomApi.domainName = "{{ site.domain }}"
  SomApi.config.sustainTime = sustainTime
  SomApi.config.testServerEnabled = true
  SomApi.config.userInfoEnabled = false
  SomApi.config.latencyTestEnabled = true

  SomApi.config.progress = {
    enabled: true,
    verbose: true
  }

  SomApi.onTestCompleted = onTestCompleted;
  SomApi.onError = onError;
  SomApi.onProgress = onProgress

  progressInterval = 300
  timeLatestDownloadProgressSent = 0
  unsentDownloadProgressValues = []
  timeLatestUploadProgressSent = 0
  unsentUploadProgressValues = []

  webkit.messageHandlers.pageLoadedHandler.postMessage("Test page loaded.")

  function start() {
    _gs("event", "Start Test")
    SomApi.startTest()
    webkit.messageHandlers.testStartHandler.postMessage("Speed test in progress. Please wait...")
  }

  function onProgress(progress) {
    now = new Date().getTime()

    if (progress.type == "latency") {
      webkit.messageHandlers.onProgressHandler.postMessage(progress)
    } else if (progress.type == "download") {
      delta = now - timeLatestDownloadProgressSent
      unsentDownloadProgressValues.push(progress.currentSpeed)

      if (delta > progressInterval) {
        progress.currentSpeed = Array.max(unsentDownloadProgressValues)
        timeLatestDownloadProgressSent = now
        unsentDownloadProgressValues = []
        webkit.messageHandlers.onProgressHandler.postMessage(progress)
      }
    } else {
      delta = now - timeLatestUploadProgressSent
      unsentUploadProgressValues.push(progress.currentSpeed)

      if (delta > progressInterval) {
        progress.currentSpeed = Array.max(unsentUploadProgressValues)
        timeLatestUploadProgressSent = now
        unsentUploadProgressValues = []
        webkit.messageHandlers.onProgressHandler.postMessage(progress)
      }
    }
  }

  function onTestCompleted(testResult) {
    webkit.messageHandlers.onCompletionHandler.postMessage(testResult)
  }

  function onError(error) {
    webkit.messageHandlers.onErrorHandler.postMessage(error)
  }

  Array.max = function(array) {
    return Math.max.apply(Math, array)
  }
</script>
