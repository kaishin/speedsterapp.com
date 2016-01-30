---
layout: default
---

# FAQ

If your question is not answered below, feel free to [get in touch](/support).

## Why are the results often slower than other speed testing services?

Currently, Speedster uses the SpeedOf.Me API which, unlike other services, downloads large contiguous sample files, similar to what usually happens when downloading a webpage or media. This is while other speed test services download small chunks in parallel and do heavy adjustments to calculate your approximate speed.

In short, the results you get with Speedster/SpeedOf.Me are more accurate and representative of your actual Internet quality.

## What servers are used to perform the tests?

Speedster uses—through SpeedOf.Me—several test servers (PoPs) in various locations to obtain the most accurate results. Defaulting to the closest test server is not the answer since the results will be always higher than the real speed for connecting to the rest of the Internet.Here are the currently avaiable locations:

- North America: Ashburn(2), Atlanta(2), Chicago(2), Dallas(2), Los Angeles(5), Miami(2), New York(2), San Jose(2), Seattle(2), Newark, Boston and Philadelphia
- Europe: Amsterdam(2), Frankfurt(3), London(2), Madrid(2), Paris(2), Vienna, Copenhagen, Stockholm(2), Helsinki, Milan and Warsaw
- Asia: Hong Kong, Singapore, Bangalore, Chennai, Mumbai, Noida, Batam, Osaka, Tokyo(2), Jakarta, Kaohsiung and Seoul
- Australia: Sydney, Melbourne
- South America: Sao Paulo

## How do the tests work?

Speedster tests your bandwidth in several passes. Sample file sizes increase gradually until it takes longer than eight seconds to download or upload the sample file. As a result, it is able to measure connection speeds in a wider range than other tools.
