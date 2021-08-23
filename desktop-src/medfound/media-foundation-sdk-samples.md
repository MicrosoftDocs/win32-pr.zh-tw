---
description: 本節說明範例應用程式，示範如何使用媒體基礎的編碼 SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated 或淘汰的 SamplesRelated 主題
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: 媒體基礎 SDK 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7d07d4136e613b4c6b553aa089834f58ccf65b6b87043ec5148d8db4ee6547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465139"
---
# <a name="media-foundation-sdk-samples"></a>媒體基礎 SDK 範例

本節說明示範如何使用媒體基礎的範例應用程式。

-   [編碼範例](#encoding-samples)
-   [播放範例](#playback-samples)
-   [外掛程式](#plug-ins)
-   [來源讀取器範例](#source-reader-samples)
-   [影片捕獲](#video-capture)
-   [其他範例](#miscellaneous-samples)
-   [已淘汰或已淘汰的範例](#deprecated-or-obsolete-samples)
-   [相關主題](#related-topics)

## <a name="encoding-samples"></a>編碼範例



| 範例                            | 描述                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [轉碼](transcode-sample.md) | 說明如何 reencode 媒體檔案以 Windows 媒體格式。 |



 

## <a name="playback-samples"></a>播放範例



| 範例                                            | 描述                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | 使用 [媒體會話](media-session.md)播放音訊和影片檔案。 這個範例示範如何建立播放拓撲、控制媒體會話，以及在播放期間接收會話事件。 |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | 示範 [BasicPlayback](/previous-versions//bb970475(v=vs.85)) 範例中未包含的一些播放函式。                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | 播放受保護的音訊和影片檔案。 此範例說明如何使用受保護的媒體路徑 (PMP) 會話，以及如何使用內容啟用程式物件。                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| 範例                                       | Sub-Area                         | Description                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [解碼 器](decoder-sample.md)                | 媒體基礎轉換 (MFT)  | 影片解碼器。                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | 其他                    | [增強型影片](enhanced-video-renderer.md)轉譯器的自訂展示者 (EVR) 。                 |
| [MFT \_ AudioDelay](mft-audiodelay-sample.md) | MFT                              | 音訊效果轉換。 說明如何撰寫音訊處理的基本 MFT。                           |
| [MFT \_ 灰階](mft-grayscale-sample.md)   | MFT                              | 灰階影片效果。 說明如何撰寫影片處理的基本 MFT。                           |
| [MPEG1Source](mpeg1source-sample.md)        | 媒體來源                     | 剖析 MPEG-2 系統層串流。 說明如何撰寫自訂媒體來源和位元組資料流程處理常式。 |
| [WavSink](wavsink-sample.md)                | 媒體接收器                       | 寫入 .wav 檔案的封存接收。 說明如何撰寫自訂媒體接收。                        |
| [WavSource](wavsource-sample.md)            | 媒體來源                     | 剖析 .wav 檔。 說明如何撰寫自訂媒體來源和位元組資料流程處理常式。                   |



 

## <a name="source-reader-samples"></a>來源讀取器範例



| 範例                                      | 描述                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [音訊剪輯](audio-clip-sample.md)         | 使用 [來源讀取器](source-reader.md) 將音訊從媒體檔案解碼。      |
| [VideoThumbnail](videothumbnail-sample.md) | 使用 [來源讀取器](source-reader.md) 從影片檔案取得單一畫面格。 |



 

## <a name="video-capture"></a>影片捕獲



| 範例                                        | 描述                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | 示範如何使用 Direct3D 轉譯影片，從影片捕獲裝置預覽影片。 |
| [MFCaptureToFile](mfcapturetofile-sample.md) | 說明如何從攝影機將影片捕獲到檔案。                                   |



 

## <a name="miscellaneous-samples"></a>其他範例



| 範例                                         | 描述                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | 示範如何從 Advanced 系統格式剖析資料， (ASF) 檔。                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | 說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | 使用 DirectX Video 加速 (DXVA) 2.0 來建立 4:2:2 YUV 影片的串流。 此範例說明如何使用 DXVA 的影片處理功能。 |



 

## <a name="deprecated-or-obsolete-samples"></a>已淘汰或已淘汰的範例



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>範例</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>示範 <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API 的一些先進播放功能。</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></td>
<td>將灰階效果套用到影片。 說明如何將 MFTs 插入播放拓撲中。<br/>
<blockquote>
[!Note]<br />
SDK 中已不再包含此範例。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">播放 清單</a></td>
<td>使用 sequencer 來源播放一系列的音訊檔案。<br/>
<blockquote>
[!Note]<br />
SDK 中已不再包含此範例。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">SimpleCapture</a></td>
<td>說明如何使用 MFPlay API，從影片捕獲裝置預覽影片。</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">SimplePlay</a></td>
<td>說明如何使用 MFPlay API 播放媒體檔案。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 媒體基礎](microsoft-media-foundation-sdk.md)
</dt> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
