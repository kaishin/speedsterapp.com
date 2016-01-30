---
layout: webview
title: Fake Test Webview
---

<script type="text/javascript">
  var data = [
  {
    currentSpeed: 0.27,
    maxSpeed: 0.27,
    pass: 1,
    percentDone: 25,
    type: "download"
  },
  {
    currentSpeed: 2.31,
    maxSpeed: 2.31,
    pass: 2,
    percentDone: 100,
    type: "download"
  },
  {
    currentSpeed: 9.23,
    maxSpeed: 9.23,
    pass: 4,
    percentDone: 100,
    type: "download"
  },
  {
    currentSpeed: 18.45,
    maxSpeed: 18.45,
    pass: 5,
    percentDone: 100,
    type: "download"
  },
  {
    currentSpeed: "",
    maxSpeed: "",
    pass: "",
    percentDone: 90,
    type: "latency"
  },
  {
    currentSpeed: 36.48,
    maxSpeed: 36.48,
    pass: 6,
    percentDone: 99,
    type: "download"
  },
  {
    currentSpeed: 26.62,
    maxSpeed: 73.82,
    pass: 8,
    percentDone: 19,
    type: "download"
  },
  {
    currentSpeed: 39.15,
    maxSpeed: 73.82,
    pass: 8,
    percentDone: 36,
    type: "download"
  },
  {
    currentSpeed: 48.49,
    maxSpeed: 73.82,
    pass: 8,
    percentDone: 54,
    type: "download"
  },
  {
    currentSpeed: 56.07,
    maxSpeed: 73.82,
    pass: 8,
    percentDone: 75,
    type: "download"
  },
  {
    currentSpeed: 62.95,
    maxSpeed: 73.82,
    pass: 8,
    percentDone: 97,
    type: "download"
  },
  {
    currentSpeed: 63.67,
    maxSpeed: 73.82,
    pass: 9,
    percentDone: 8,
    type: "download"
  },
  {
    currentSpeed: 55.36,
    maxSpeed: 73.82,
    pass: 9,
    percentDone: 19,
    type: "download"
  },

  {
    currentSpeed: 108.88,
    maxSpeed: 108.88,
    pass: 11,
    percentDone: 43,
    type: "download"
  },
  {
    currentSpeed: 109.09,
    maxSpeed: 109.09,
    pass: 11,
    percentDone: 46,
    type: "download"
  },
  {
    currentSpeed: 109.21,
    maxSpeed: 109.21,
    pass: 11,
    percentDone: 100,
    type: "download"
  },

  {
    currentSpeed: 6.46,
    maxSpeed: 6.46,
    pass: 1,
    percentDone: 26,
    type: "upload"
  },
  {
    currentSpeed: 6.83,
    maxSpeed: 6.83,
    pass: 1,
    percentDone: 29,
    type: "upload"
  },
  {
    currentSpeed: 7.31,
    maxSpeed: 7.31,
    pass: 1,
    percentDone: 35,
    type: "upload"
  },
  {
    currentSpeed: 7.76,
    maxSpeed: 7.76,
    pass: 1,
    percentDone: 41,
    type: "upload"
  },
  {
    currentSpeed: 8.119,
    maxSpeed: 8.119,
    pass: 1,
    percentDone: 46,
    type: "upload"
  },
  {
    currentSpeed: 8.45,
    maxSpeed: 8.45,
    pass: 1,
    percentDone: 52,
    type: "upload"
  },
  {
    currentSpeed: 8.73,
    maxSpeed: 8.73,
    pass: 1,
    percentDone: 57,
    type: "upload"
  },
  {
    currentSpeed: 8.78,
    maxSpeed: 8.78,
    pass: 1,
    percentDone: 61,
    type: "upload"
  },
  {
    currentSpeed: 9,
    maxSpeed: 9,
    pass: 1,
    percentDone: 66,
    type: "upload"
  },
  {
    currentSpeed: 11.2,
    maxSpeed: 11.2,
    pass: 2,
    percentDone: 99,
    type: "upload"
  },
  {
    download: 100.62,
    jitter: 35777,
    latency: 206,
    maxDownload: 112.68,
    maxUpload: 11.21,
    testServer: "Unknown",
    upload: 11.21
  }];

  webkit.messageHandlers.pageLoadedHandler.postMessage("Test page loaded.");

  function start() {
    webkit.messageHandlers.testStartHandler.postMessage("Speed test in progress. Please wait...");
    setInterval(sendNext, 300);
  }

  function sendNext() {
    if (data.length > 1) {
      webkit.messageHandlers.onProgressHandler.postMessage(data.shift());
    } else if (data.length == 1) {
      webkit.messageHandlers.onCompletionHandler.postMessage(data.shift());
    }
  }
</script>
