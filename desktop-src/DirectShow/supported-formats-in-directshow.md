---
description: DirectShow 中支援的格式
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: DirectShow 中支援的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984223"
---
# <a name="supported-formats-in-directshow"></a>DirectShow 中支援的格式

DirectShow 是一個開放的架構，這表示它可以支援任何格式，只要有篩選器可以剖析和解碼它即可。 由 Microsoft 提供的篩選器（可透過 DirectShow 或作為 Windows 作業系統元件的可轉散發套件）提供下列檔案和壓縮格式的預設支援。

檔案類型：



| 檔案類型                                                                                        | 相關資訊                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF) ，包括 Windows Media 音訊 (WMA) 和 Windows Media 視訊 WMV ( | [WM ASF 讀取器篩選器](about-the-wm-asf-reader-filter.md)<br/> [WM ASF 寫入器篩選器](wm-asf-writer-filter.md)<br/> |
| .AIFF                                                                                             | [WAVE 剖析器篩選](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [WAVE 剖析器篩選](wave-parser-filter.md)                                                                                      |
| 影音交錯技術 (AVI)                                                                    | [AVI Mux 篩選](avi-mux-filter.md)<br/> [AVI 分隔器篩選](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [MIDI 剖析器篩選](midi-parser-filter.md)<br/> [**MIDI 轉譯器篩選**](midi-renderer-filter.md)<br/>           |
| Snd                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [WAVE 剖析器篩選](wave-parser-filter.md)                                                                                      |



 

壓縮格式：



| 格式                                        | 相關資訊                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Microsoft MPEG-1/DD/AAC 音訊解碼器**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| 數位視訊 (DV)                             | [DV 影片解碼篩選](dv-video-decoder-filter.md)<br/> [DV 影片編碼器篩選器](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Microsoft MPEG-2 影片解碼**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-2 影片版本1。0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-2 第3版                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [MJPEG 壓縮程式篩選器](mjpeg-compressor-filter.md)<br/> [MJPEG 解壓縮程式篩選器](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG 音訊第3層 (MP3) 僅 (解壓縮)  |                                                                                                                                                                                                                                                 |
| MPEG-2 第1層和第二層音訊             | [**Microsoft MPEG-1/DD/AAC 音訊解碼器**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [MPEG-2 音訊解碼篩選器](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| MPEG-2 影片                                  | [MPEG-2 影片解碼篩選器](mpeg-1-video-decoder-filter.md)<br/> [**Microsoft MPEG-2 影片解碼**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| MPEG-2 音訊                                  | [**Microsoft MPEG-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Microsoft MPEG-2 編碼器**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| MPEG-2 影片                                  | [**Microsoft MPEG-2 編碼器**](microsoft-mpeg-2-encoder.md)<br/> [**Microsoft MPEG-2 影片解碼**](microsoft-mpeg-2-video-decoder.md)<br/> [**Microsoft MPEG 2 影片編碼器**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

如需特定協力廠商編解碼器的可用性資訊，以便與 DirectShow 應用程式轉散發，請洽詢編解碼器製造商。

 

 




