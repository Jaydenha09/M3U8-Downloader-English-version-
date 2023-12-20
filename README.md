
![M3U8-Downloader-Build](https://img.shields.io/github/workflow/status/heisir2014/M3U8-Downloader/M3U8-Downloader-Build?style=flat-square)
[![Release](https://img.shields.io/github/v/release/heisir2014/m3u8-downloader?style=flat-square)](https://github.com/HeiSir2014/M3U8-Downloader/releases/latest)
[![Download](https://img.shields.io/github/downloads/heisir2014/m3u8-downloader/total?style=flat-square)](https://github.com/HeiSir2014/M3U8-Downloader/releases/latest)
# M3U8-Downloader Direct Download
M3U8-Downloader is an application developed based on the Electron framework that allows downloading and playing HLS video streams. Its key features include the following:

| Feature                   | Supported |
| :------------------------ | --------: |
| HLS protocol VOD sources   |        ✓ |
| Custom HTTP header download|        ✓ |
| Custom KEY and IV decryption|        ✓ |
| Local M3U8 file download   |        ✓ |
| M3U8 live sources          |        ✓ |
| Standard AES-128-CBC encryption |   ✓ |
| Standard AES-196-CBC encryption |   ✓ |
| Standard AES-256-CBC encryption |   ✓ |
| Non-standard AES-*-CBC encryption |  ㄨ(customizable) |
| Webpage video source sniffing |  ✓ |


<div align="center">
    <br>
    <img width="739" src="https://github.com/HeiSir2014/M3U8-Downloader/blob/master/resource/HLSDownloadShow-3-1.gif?raw=true" alt="M3U8-Downloader">
    <br>
</div>

# Feature Planning

```mermaid
flowchart LR
    A1("M3U8-Downloader") ---> B1("MP4, M3U8, MPD Download")
    B1 ---> C1(Customize File Name)
    B1 ---> C2(Customize HTTP Header)
    C2 ---> D1(Referer, Cookies, User-Agent)
    B1 ---> C3(Customize AES Key)
    B1 ---> C4(Multiple Bitrate Selection)
    B1 ---> C5(HTTP Proxy)
    
    A1 ---> B2("MP4, M3U8, MPD Batch Download")
    A1 ---> B3(Merge TS Files)
    A1 ---> B4(Browser Resource Sniffing)
    B4 ---> C6(FLV, MP4, MP3, WAV)
    B4 ---> C7(HLS - M3U8, TS)
    B4 ---> C8(DASH - MPD)
    B4 ---> C12(Simulate Multiple Terminals)
    A1 ---> B5(Settings)
    B5 ---> C9(Storage Path)
    B5 ---> C10(Set Proxy)
    B5 ---> C11(View Logs)
```
![mermaid-diagram-20210328004859](https://i.loli.net/2021/03/28/Ca5yhFQeTmG69DK.png)

---

# Obtaining M3U8 video URLs

To obtain the M3U8 video URL, open the video webpage in the Chrome browser, press F12, navigate to the Network tab, enter 'm3u8' in the Filter box, and then press F5 to refresh the page. If the video on the webpage uses HLS as its source, you can capture the video stream address here. Then, right-click on it, select 'Copy' -> 'Copy Link Address'.

By providing the M3U8 source address, you can download and losslessly transcode it into an MP4 file.

[Adding Custom Headers - Video Tutorial](https://player.bilibili.com/player.html?aid=498666070&bvid=BV1QK411n7VJ&cid=206827525&page=1)

# Download the executable package.

## Go to Baidu Netdisk for download.

```
Link：https://pan.baidu.com/s/14zaMkxgfTC0HSge-Ze6EpQ 
extraction code：m3u8 
```

## Download from GitHub.
## [Download from Releases](https://github.com/HeiSir2014/M3U8-Downloader/releases)

# Run the source code.
### Set up Node.js development environment

Install the latest version of Node.js.[NodeJs Download](http://nodejs.org/)

### Clone the code

Create a new folder in any directory to store the code and execute the following commands
```
cd newdir

git clone https://github.com/HeiSir2014/M3U8-Downloader.git .
```
### Yarn Environment Installation

```
npm install yarn -g
```

### Package Dependency Installation

```
yarn
```

ffmpeg-static installation timed out, you can try using a mirror:

```
FFMPEG_BINARIES_URL=https://cdn.npmmirror.com/binaries/ffmpeg-static yarn
```

### Run M3U8-Downloader

```
yarn start
```
### Packaging and Deployment

```
//Packaging for Windows Platform
yarn pack-win

//Packaging for Mac Platform
yarn pack-mac

```

### Enjoy it

### Donate

[Donation Link](https://tools.heisir.cn/HLSDownload/2019/07/08/02/)
