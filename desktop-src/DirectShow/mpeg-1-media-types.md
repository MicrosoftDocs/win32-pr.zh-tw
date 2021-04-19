---
description: 此區段會列出用於 MPEG-2 資料的媒體類型。
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: MPEG-2 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981928"
---
# <a name="mpeg-1-media-types"></a>MPEG-2 媒體類型

此區段會列出用於 MPEG-2 資料的媒體類型。

## <a name="mpeg-1-system-stream"></a>MPEG-1 系統串流



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| 主要類型            | 媒體媒體的 \_ 串流                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| 格式類型           | 格式 \_ MPEGStreams                             |
| 格式結構      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| 媒體範例內容 | 位元組資料流程;無對齊                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>視訊 CD 的 MPEG-2 系統資料流程



|                       |                            |
|-----------------------|----------------------------|
| 主要類型            | 媒體媒體的 \_ 串流          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| 格式類型           | GUID \_ Null                 |
| 格式結構      | 無                       |
| 媒體範例內容 | 位元組資料流程;沒有對齊。 |



 

## <a name="mpeg-1-audio-packet"></a>MPEG-2 音訊封包



|                       |                                                |
|-----------------------|------------------------------------------------|
| 主要類型            | 媒體 \_ 媒體                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| 格式類型           | 格式 \_ WaveFormatEx                           |
| 格式結構      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| 媒體範例內容 | 單一 MPEG 封包，包括封包標頭。 |



 

## <a name="mpeg-1-audio-payload"></a>MPEG-2 音訊承載



|                       |                                            |
|-----------------------|--------------------------------------------|
| 主要類型            | 媒體 \_ 媒體                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| 格式類型           | 格式 \_ WaveFormatEx                       |
| 格式結構      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| 媒體範例內容 | 位元組對齊的 MPEG-2 音訊資料。            |



 

## <a name="mpeg-1-video-packet"></a>MPEG-2 視頻包



|                       |                                                |
|-----------------------|------------------------------------------------|
| 主要類型            | 媒體 \_ 媒體                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| 格式類型           | 格式 \_ MPEGVideo                              |
| 格式結構      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| 媒體範例內容 | 單一 MPEG 封包，包括封包標頭。 |



 

## <a name="mpeg-1-video-payload"></a>MPEG-2 影片承載



|                       |                                          |
|-----------------------|------------------------------------------|
| 主要類型            | 媒體 \_ 媒體                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| 格式類型           | 格式 \_ MPEGVideo                        |
| 格式結構      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| 媒體範例內容 | 位元組對齊的 MPEG-2 影片資料。          |



 

## <a name="mpeg-1-native-video-stream"></a>MPEG-2 原生影片串流



|                       |                                                |
|-----------------------|------------------------------------------------|
| 主要類型            | 媒體媒體的 \_ 串流                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| 格式類型           | GUID \_ Null                                     |
| 格式結構      | 無                                           |
| 媒體範例內容 | 影片串流位元組陣列 (不) 系統層。 |



 

## <a name="mpeg-1-native-audio-stream"></a>MPEG-2 原生音訊串流



|                       |                                                |
|-----------------------|------------------------------------------------|
| 主要類型            | 媒體媒體的 \_ 串流                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| 格式類型           | GUID \_ Null                                     |
| 格式結構      | 無                                           |
| 媒體範例內容 | 音訊串流位元組陣列 (不) 系統層。 |



 

## <a name="remarks"></a>備註

DirectShow MPEG-2 篩選準則支援這些類型，如下所示。



| 篩選               | 方向 | 支援的媒體類型                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| MPEG-2 分隔器      | 輸入     | MPEG-2 系統 streamMPEG-1 視訊 CD 的系統資料流程<br/>                                                 |
| MPEG-2 分隔器      | 輸出    | MPEG-2 音訊 packetMPEG-1 音訊承載<br/> MPEG-2 視頻包<br/> MPEG-2 影片承載<br/> |
| 軟體音訊編解碼器 | 輸入     | MPEG-2 音訊 packetMPEG-1 音訊承載<br/>                                                                |
| 軟體視頻編碼器 | 輸入     | MPEG-2 Video packetMPEG-1 Video 承載<br/>                                                                |
| 軟體音訊編解碼器 | 輸出    | PCM 音訊                                                                                                         |
| 軟體視頻編碼器 | 輸出    | 未壓縮的影片 (Y41P、YUY2、UYVY、RGB-24、RGB-32、RGB-565、RGB-555、RGB-8)                                     |



 

MPEG-2 視頻包和裝載媒體類型包含完整的序列標頭，如此一來，就可以從檔案中間播放資料，而不需要使用序列標頭來初始化播放影片。

影片序列標頭會附加至 MPEG 影片的影片資料類型，讓播放可以從資料流程的中間開始。 此欄位的長度最多為140個位元組;它包含序列標頭起始程式碼 (0x000001B3) 開始，以及遇到第一個序列標頭中找到的任何量化矩陣。

 

 




