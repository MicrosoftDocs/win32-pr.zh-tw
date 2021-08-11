---
description: 本主題列出 Microsoft 媒體基礎原始支援的媒體格式
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: 媒體基礎中支援的媒體格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238187"
---
# <a name="supported-media-formats-in-media-foundation"></a>媒體基礎中支援的媒體格式

本主題列出 Microsoft 媒體基礎原始支援的媒體格式 協力廠商可以撰寫自訂外掛程式，以支援其他格式。

## <a name="file-containers"></a>檔案容器



| 格式                                           | 副檔名          | 媒體來源                                 | 媒體接收器                                   | 需要                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2、. 3gp、. .3gp2、. 3gpp | [MPEG-2 檔案來源](mpeg-4-file-source.md) | 3GP File Sink                                | Windows 7                                                             |
|  (ASF) 的 Advanced 串流格式                  | .asf、.wma、.wmv         | [ASF 媒體來源](asf-media-source.md)     | [ASF 媒體接收器](asf-media-sinks.md)        | Windows Vista                                                         |
| 音訊資料傳輸串流 (ADTS) 。              | aac、. adts              | ADTS 檔案來源                             | 無                                         | Windows 7                                                             |
| AVI                                              | .avi                     | AVI 檔案來源                              | 無                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**MP3 檔案來源**](mp3-file-source.md)   | MP3 檔案接收                                | 檔案來源： Windows Vista<br/> File sink： Windows 7<br/> |
| MPEG-4                                           | m4a、. m4v、mov、.mp4   | [MPEG-2 檔案來源](mpeg-4-file-source.md) | [**MPEG-2 File 接收**](mpeg-4-file-sink.md) | Windows 7                                                             |
| 已同步的可存取媒體交換 (薩米)  | . 薩米文，smi-s              | [薩米媒體來源](sami-media-source.md)   | 無                                         | Windows Vista                                                         |
| 波                                             | .wav                     | AVI 檔案來源                              | 無                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>音訊轉碼器



| 格式                                              | 解碼器                                                                                                                                                          | 編碼器                                                                                                                                                          | 需要      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ定律編碼                                        | 音訊壓縮管理員 (的) μ定律編解碼器                                                                                                                      | 無                                                                                                                                                             | Windows Vista |
| 適應性差異脈衝程式碼 (ADPCM)  | ADPCM 編解碼器                                                                                                                                                  | 無                                                                                                                                                             | Windows Vista |
| Advanced Audio 編碼 (AAC)                          | [**AAC 解碼器**](aac-decoder.md)                                                                                                                               | [**AAC 編碼器**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows媒體 MP3 解碼**](windows-media-mp3-decoder.md)                                                                                                   | 無                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | 進行中的 GSM 6.10 編解碼器                                                                                                                                               | 無                                                                                                                                                             | Windows Vista |
| Windows Media 音訊 (WMA)                           | [**Windows媒體音訊解碼器**](windowsmediaaudiodecoder.md)<br/> [**WindowsMedia Audio Voice 解碼**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows媒體音訊編碼器**](windowsmediaaudioencoder.md)<br/> [**WindowsMedia Audio Voice 編碼器**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> 媒體基礎為上表所列的數個已進行的編解碼器提供包裝函式。 不過，媒體基礎不支援任意的未執行編解碼器。

 

## <a name="video-codecs"></a>視訊轉碼器



| 格式                                                                                                         | 解碼器                                                                                                                                                                  | 編碼器                                                                                                                             | 需要      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| DV 影片                                                                                                       | [**DV 影片解碼**](dv-video-decoder.md)                                                                                                                             | 無                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**H.264 Video 解碼**](h-264-video-decoder.md)                                                                                                                       | [**H.264 影片編碼器**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/>  (h.264 基準設定檔相容于 MPEG-2 Pt2 簡短的影片標頭模式) <br/> | [**MPEG 4 第2部分影片解碼**](mpeg4part2videodecoder.md)                                                                                                            | 無                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | MJPEG 解碼器                                                                                                                                                            | 無                                                                                                                                | Windows 7     |
| Mpeg-4 第 2 部分                                                                                                  | [**MPEG 4 第2部分影片解碼**](mpeg4part2videodecoder.md)                                                                                                            | 無                                                                                                                                | Windows 7     |
| MPEG 4 v1/v2/v3                                                                                                | [**Windows媒體 MPEG-2 V3 解碼器**](./windowsmediampeg4v3decoder.md)<br/> [**WindowsMedia MPEG4 V1/V2 解碼器**](windowsmediampeg4decoder.md)<br/>         | 無                                                                                                                                | Windows Vista |
| Windows Media 視訊 (WMV)                                                                                      | [**Windows媒體 Video 9 解碼器**](windowsmediavideo9decoder.md)<br/> [**WindowsMedia Video 9 螢幕解碼**](windowsmediavideo9screendecoder.md)<br/> | WindowsMedia Video 9 編碼器<br/> WindowsMedia Video 9 螢幕編碼器<br/> Windows媒體影片7/8 編碼器<br/> | Windows Vista |



 

> [!Note]  
> [需要] 資料行列出在媒體基礎應用程式中使用這些編解碼器所需的最低作業系統。 在 Windows Vista 作為[DirectX 媒體物件](../directshow/directx-media-objects.md) (DMOs) 之前引進了某些編解碼器。 如果編解碼器支援 DMO 功能，可以搭配[DirectShow](../directshow/directshow.md)或[Windows 媒體格式 SDK](../wmformat/windows-media-format-11-sdk.md)來使用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> <dt>

[媒體來源和接收](media-sources-and-sinks.md)
</dt> </dl>

 

 
