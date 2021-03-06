---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Jane Doe
---

## 1.2 

#### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     |
| 1024x768 PNG image                         | 1.5  MB       |
| 1024x768 RAW image                         | 2.25 MB       | 
| HD (1080p) HEVC Video (15 minutes)         | 36 MB         |
| HD (1080p) Uncompressed Video (15 minutes) | 36000 MB      |
| 4K UHD HEVC Video (15 minutes)             | 228 MB        |
| 4k UHD Uncompressed Video (15 minutes)     | 228000 MB     |
| Human Genome (Uncompressed)                | 200 GB        |

1 byte per character so 128 bytes
Pixel size(considering 16 bit color) = 1024 * 768 * 16 = 12,582,912 pixels. 12,582,912/(8 * 1024)/1024 = 1.5 
Pixel size = 786,432 * 3 = 2,359,296/(1024 * 1024) = 2.25 
15 * 60 = 900. So, 900 * 30 * 1290 * 1080 * 8/8/1000/1024/1024 = approx 36
15 * 60 = 900. So,900 * 30 * 1290 * 1080 * 8/8/1024/1024 = approx 36,000
15 * 60 = 900. So, 900 * 30 * 4096 * 2160 * 8/8/1000/1024/1024 = approx 228 MB
15 * 60 = 900. So, 900 * 30 * 4096 * 2160 * 8/8/1024/1024 = approx 228,000 MB
From genome sequencer 200GB

#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64GB     |   1  |
| Daily Twitter Tweets (Snappy Compressed)  | 38GB     |   1  |
| Daily Instagram Photos                    | 168TB    |   51 |
| Daily YouTube Videos                      | 104TB    |   32 |
| Yearly Twitter Tweets (Uncompressed)      | 25TB     |   8  |
| Yearly Twitter Tweets (Snappy Compressed) | 14TB     |   5  |
| Yearly Instagram Photos                   | 61,320TB | 18396|
| Yearly YouTube Videos                     | 37,960TB | 11388|
Daily twitter tweets is approx 500 million - considering 128 bytes 500M * 128 = 64GB
Daily twitter tweets compressed - considering 1.7 compression ration = 64GB/1.7 = 38GB
75 million photos are uploaded daily - 2.25 * 75,000,000 = 168GB
500 hours of youtube videos uploade daily - 500 * 60 * 24 = 720000 hours. So, 72,000 * 4 * 15(15 min length) = 104TB
Yearly twitter tweets(uncompressed) - 64GB * 365 = 25TB
Yearly twitter tweets(compressed) - 38GB * 365 = 14TB
Yearly instagram photos - 168TB * 365 = 61,320TB
Yearly youtube videos - 104TB * 365 = 37,960TB


#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | 51   | Less than 1|
| Twitter Tweets (Snappy Compressed) | 32   | Less than 1|
| Instagram Photos                   | 18396|   171      |
| YouTube Videos                     | 11388|   105      |
Failure rate is 0.93% as per https://www.backblaze.com/b2/hard-drive-test-data.html

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 140.56 ms            |
| Low Earth Orbit Satellite | 600 ms               |
| Geostationary Satellite   | 240-279 ms           |
| Earth to the Moon         | 1300 ms              |
| Earth to Mars             | 3 minutes            | 
https://wondernetwork.com/pings/Los%20Angeles/Amsterdam
https://www.omniaccess.com/leo/#:~:text=The%20GEO%20latency%20is%20of,and%20an%20essential%20part%20if
https://www.satsig.net/latency.htm
https://www.spaceacademy.net.au/spacelink/commdly.htm
https://www.forbes.com/sites/quora/2016/08/31/when-we-eventually-get-to-mars-this-is-how-the-internet-will-work-there/?sh=1966d9b37dae