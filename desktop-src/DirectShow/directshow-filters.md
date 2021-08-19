---
description: DirectShow過濾 器
ms.assetid: a7cb806e-5705-483e-b7b2-39f427681ae5
title: DirectShow過濾 器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420d604c903f1e3749545252740159deea04e31fb5710ac0b49d31d7b4bd493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016185"
---
# <a name="directshow-filters"></a>DirectShow過濾 器

DirectShow 在 Windows 中提供一組預設篩選器。 這些篩選器支援許多資料格式，同時提供高程度的硬體獨立性。 應用程式也可以在目標系統上註冊並安裝自訂篩選器。

使用中的包裝函式、avi 解壓縮程式和 avi 壓縮程式篩選器可搭配音訊和視訊壓縮管理員使用，以啟用 DirectShow 篩選圖形中使用的各種編解碼器。

此處列出 DirectShow 軟體發展工具組 (SDK) 支援的所有篩選器。 如果篩選準則出現在 GraphEdit 中，但未記載在此參考區段中，則表示篩選器已由協力廠商安裝，或由其他 Microsoft 技術在內部使用。 DirectShow SDK 不支援這種篩選。



| 篩選                                                                          | Description                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [進行中的包裝函式](acm-wrapper-filter.md)                                           | 啟用音訊壓縮管理員 (的) 編解碼器，以聯結篩選圖形。                                                                                                                                                              |
| [類比視頻縱橫](analog-video-crossbar-filter.md)                       | 代表影片啟用裝置上支援 Windows Driver Model (WDM) 的視頻縱橫區。                                                                                                                                 |
| [音訊捕獲](audio-capture-filter.md)                                       | 代表音訊捕獲裝置。                                                                                                                                                                                                 |
| [音訊轉譯器 (WaveOut) ](audio-renderer--waveout--filter.md)                 | 使用 **waveOut \*** api 來呈現波形音訊。                                                                                                                                                                               |
| [AVI 壓縮](avi-compressor-filter.md)                                     | 啟用影片壓縮管理員 (BC-VCM-LVM-HYPERV) 壓縮機來聯結篩選圖形。                                                                                                                                                         |
| [AVI 解壓縮](avi-decompressor-filter.md)                                 | 啟用影片壓縮管理員 (BC-VCM-LVM-HYPERV) decompressors 來聯結篩選圖形。                                                                                                                                                       |
| [AVI 繪圖](avi-draw-filter.md)                                                 | 當影片輸出到外部 NTSC 電視監視器時，自動提取到播放圖形，而不是 AVI 解壓縮程式。                                                                                       |
| [AVI Mux](avi-mux-filter.md)                                                   | 接受多個輸入資料流程，並將它們交錯成 AVI 格式。                                                                                                                                                                |
| [AVI 分隔器](avi-splitter-filter.md)                                         | 在播放 AVI 檔案的播放中分割音訊和影片串流。                                                                                                                                                                            |
| [AVI/WAV 檔案來源](avi-wav-file-source.md)                                  | 讀取 AVI 和 WAV 來源檔案，並針對檔案類型產生適當的輸出圖釘。 (已取代。)                                                                                                                           |
| [CC 解碼器](cc-decoder-filter.md)                                             | 接受 capture 篩選器所提供的範例波形，並傳遞已解碼的封閉字幕資料。                                                                                                                                 |
| [色彩空間轉換器](color-space-converter-filter.md)                       | 從一個 RGB 色彩類型轉換成另一個 RGB 類型。                                                                                                                                                                               |
| [DirectSound 轉譯器](directsound-renderer-filter.md)                         | 使用 DirectSound API 呈現音訊。                                                                                                                                                                                            |
| [DMO包裝](dmo-wrapper-filter.md)                                           | 可讓 DirectShow 應用程式在篩選圖形中使用[DirectX 媒體物件](directx-media-objects.md) (DMO) 。                                                                                                            |
| [DV Muxer](dv-muxer-filter.md)                                                 | 結合數位視訊 (DV) 編碼的影片串流與一或兩個音訊串流，以產生交錯式 DV 串流。                                                                                                               |
| [DV 分隔器](dv-splitter-filter.md)                                           | 將交錯的 DV 資料流程分割成其元件的影片和音訊串流。                                                                                                                                                         |
| [DV 影片解碼](dv-video-decoder-filter.md)                                 | 將 DV 串流解碼成未壓縮的影片。                                                                                                                                                                                        |
| [DV 影片編碼器](dv-video-encoder-filter.md)                                 | 將未壓縮的影片串流編碼為 DV 影片。                                                                                                                                                                                 |
| [DVD 導覽器](dvd-navigator-filter.md)                                       | 開啟 DVD-Video 磁片區中所有必要的檔案、流覽線性 DVD-Video，然後剖析產生的 MPEG-2 程式串流。                                                                                 |
| [**增強的影片轉譯器**](enhanced-video-renderer-filter.md)               | 具有與媒體基礎 EVR 媒體接收相同之核心功能和外掛程式模型的影片轉譯器。                                                                                                                           |
| [檔案來源 (Async) ](file-source--async--filter.md)                           | 開啟和讀取許多不同資料格式的本機檔案，並將資料傳遞至剖析器篩選器。                                                                                                                                  |
| [檔案來源 (URL) ](file-source--url--filter.md)                               | 適用于可透過統一資源定位器識別的任何原始程式檔 (URL) ，以及其媒體主要類型為 stream。                                                                                                         |
| [檔案資料流程轉譯器](file-stream-renderer-filter.md)                         | 轉譯由多檔案剖析器篩選器剖析的檔案名。                                                                                                                                                                 |
| [檔案寫入器](file-writer-filter.md)                                           | 用來將檔案寫入光碟（不論格式為何）。                                                                                                                                                                                   |
| [全螢幕轉譯器](full-screen-renderer-filter.md)                         | 使用 DirectDraw 來呈現舊版圖形卡片上的全螢幕影片。 (已過時。)                                                                                                                                                    |
| [無限 Pin 指標](infinite-pin-tee-filter.md)                                 | 將傳遞給其輸入釘選的樣本傳遞給變數數目的輸出圖釘。                                                                                                                                                    |
| [內部指令碼命令轉譯器](internal-script-command-renderer-filter.md) | 接收指令碼命令，並將它們分派至應用程式。                                                                                                                                                                    |
| [第21行的解碼器](line-21-decoder-filter.md)                                   | 將第21行的隱藏式輔助字幕資訊轉換成具有標題文字的點陣圖。                                                                                                                                                           |
| [**Microsoft AC3 編碼器**](microsoft-ac3-encoder.md)                          | 將身歷聲 PCM 音訊編碼為杜比數位位流。 協力廠商應用程式不支援 (。 )                                                                                                                                 |
| [**Microsoft MPEG-1/DD 音訊解碼器**](microsoft-mpeg-1-dd-audio-decoder.md)  | 解碼 MPEG-2、AAC 和杜比數位音訊。                                                                                                                                                                                       |
| [**Microsoft MPEG-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md)        | 編碼 MPEG-2 音訊。                                                                                                                                                                                                               |
| [**Microsoft MPEG-2 編碼器**](microsoft-mpeg-2-encoder.md)                    | 編碼 MPEG-2 音訊和影片。                                                                                                                                                                                                     |
| [**Microsoft MPEG-2 影片解碼**](microsoft-mpeg-2-video-decoder.md)        | 將 MPEG-2 影片解碼。                                                                                                                                                                                                               |
| [**Microsoft MPEG 2 影片編碼器**](microsoft-mpeg-2-video-encoder.md)        | 編碼 MPEG 2 影片。                                                                                                                                                                                                               |
| [MIDI 剖析器](midi-parser-filter.md)                                           | 讀取中找到的 MIDI 資料。中間和。RMI 檔。                                                                                                                                                                               |
| [**MIDI 轉譯器**](midi-renderer-filter.md)                                   | 從 MIDI 剖析器篩選器轉譯 MIDI 資料。                                                                                                                                                                                      |
| [MJPEG 壓縮](mjpeg-compressor-filter.md)                                 | 使用動畫 JPEG 壓縮來壓縮未壓縮的影片串流。                                                                                                                                                             |
| [MJPEG 解壓縮](mjpeg-decompressor-filter.md)                             | 將影片串流從動畫 JPEG 解碼成未壓縮的影片。                                                                                                                                                                      |
| [MPEG-2 音訊解碼器](mpeg-1-audio-decoder-filter.md)                         | 將 MPEG-2 的第一層和第 II 層音訊解碼為 PCM。                                                                                                                                                                                   |
| [MPEG-2 資料流程分隔器](mpeg-1-stream-splitter-filter.md)                     | 將 MPEG-2 系統資料流程分割成其元件音訊和影片串流。                                                                                                                                                          |
| [MPEG-2 視頻解碼器](mpeg-1-video-decoder-filter.md)                         | 解碼 MPEG 1 影片。                                                                                                                                                                                                               |
| [MPEG-2 信號信號](mpeg-2-demultiplexer.md)                                | Demultiplexes 以 push 模式傳遞的 MPEG-2 傳輸資料流程，以及以 push 或 pull 模式傳遞的程式資料流程。                                                                                                |
| [MPEG-2 分隔器](mpeg-2-splitter.md)                                          | 剖析 MPEG-2 程式串流、建立每個資料流程的輸出針腳，然後將壓縮的音訊和/或影片 MPEG 封包輸出到 MPEG-2 解碼篩選器。                                                                       |
| [MSDV 驅動程式](msdv-driver.md)                                                  | DV 攝影機的 Windows Driver Model (WDM) 驅動程式。                                                                                                                                                                            |
| [MSTape 驅動程式](mstape-driver.md)                                              | 支援 D VHS 和 MPEG 攝像機裝置。                                                                                                                                                                                          |
| [MSYUV 色彩空間轉換器編解碼器](msyuv-color-space-converter-codec.md)      | 在用戶端上啟用視頻來來源資料的播放方式，其視頻顯示器介面卡無法用於硬體中的 YUV 至 RGB 轉換。                                                                                  |
| [多重檔案剖析器](multi-file-parser-filter.md)                               | 剖析可讓您指定多個檔案名的簡單檔案格式，就好像是一個檔案一樣。                                                                                                                          |
| [重迭 Mixer 2](overlay-mixer-2-filter.md)                                   | 和覆迭 Mixer 一樣，但是可以自動新增至篩選圖形。 (已過時。)                                                                                                                                               |
| [重迭 Mixer](overlay-mixer-filter.md)                                       | 專為使用行21隱藏式字幕的 DVD 播放和廣播影片串流所設計。  (淘汰。 由影片混合轉譯器取代。 )                                                                                  |
| [QT 解壓縮](qt-decompressor-filter.md)                                   | Apple QuickTime 2.0 的影片解壓縮。 (已過時。)                                                                                                                                                                                 |
| [QuickTime 影片剖析器](quicktime-movie-parser-filter.md)                     | 將 Apple QuickTime 資料分割成音訊和影片串流。 (已過時。)                                                                                                                                                               |
| [薩米文 (CC) 剖析器](sami--cc--parser-filter.md)                                 | 剖析從已同步處理的可存取媒體交換的資料字幕資料 (薩米) 的檔案。                                                                                                                                                 |
| [智慧型 t](smart-tee-filter.md)                                               | 用於影片捕獲圖形，以將影片串流分割成預覽資料流程和捕獲資料流程。                                                                                                                                  |
| [T/接收到接收轉換器](tee-sink-to-sink-converter.md)                    | 提供有效率的方法，讓您不需要在核心和使用者模式之間進行昂貴的轉換，就能在核心模式中複製資料串流。                                                                                         |
| [電視音訊](tv-audio-filter.md)                                                 | 提供控制電視音訊解碼、身歷聲或 monoaural 選取專案，以及 (SAP) 選擇的次要音訊程式。                                                                                                          |
| [電視調諧器](tv-tuner-filter.md)                                                 | 選取要查看的類比廣播或纜線頻道。                                                                                                                                                                          |
| [VBI 介面配置器](vbi-surface-allocator.md)                              | 使用硬體視訊連接埠捕獲案例，控制類比電視圖中 VBI 緩衝區的配置。                                                                                                                      |
| [VFW Capture 篩選](vfw-capture-filter.md)                                    | 適用于使用影片進行 Windows 的較舊影片捕獲硬體。                                                                                                                                                                |
| [VGA 16 色 Ditherer](vga-16-color-ditherer-filter.md)                       | 從 RGB 色彩類型轉換為4位色彩顯示，讓 AVI 和 MPEG 視頻資料流程可以顯示在較舊的16色監視器上。 (已過時。)                                                                                |
| [影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Windows XP 中的預設影片轉譯器。 提供先進的呈現和視頻混合功能。                                                                                                                                  |
| [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9)     | 類似于 VMR-7 但可在 DirectX 支援的所有平臺上使用。                                                                                                                                                               |
| [影片埠管理員](video-port-manager.md)                                    | 可讓影片混合轉譯器順暢地在將影片資料從影片捕獲裝置或硬體解碼器傳送到圖形晶片的系統上順暢運作。                                                      |
| [影片轉譯器](video-renderer-filter.md)                                     | Windows 98SE、Windows 2000 和 Windows Millennium Edition 上的預設影片轉譯器。 連接到任何會產生解壓縮影片資料的影片轉換篩選。                                                                 |
| [WAVE 剖析器](wave-parser-filter.md)                                           | 剖析 wav、澳大利亞或. aif 檔案中的 WAV 格式音訊資料。                                                                                                                                                                         |
| [WDM 影片捕獲](wdm-video-capture-filter.md)                               | 控制使用 Windows Driver Model (WDM) 驅動程式的類比捕獲裝置。                                                                                                                                                        |
| [Windows媒體來源篩選](windows-media-source-filter.md)                  | 用來播放 Windows 媒體的預設來源篩選，以及使用 Microsoft mpeg-2 編碼器建立的 MPEG 4 內容。 這是 Windows Media Player 6.4 所使用的來源篩選。 (已過時。)                                          |
| [WM ASF 讀取器](wm-asf-reader-filter.md)                                       | Windows 媒體內容的檔案播放來源篩選，以及使用任何 Microsoft mpeg-2 編碼器 DMOs 建立的內容。 必須明確加入至篩選圖形。 此篩選是以 Windows 媒體格式 SDK 為基礎。 |
| [WM ASF 寫入器](wm-asf-writer-filter.md)                                       | 接受未壓縮的輸入資料流程，並使用 Microsoft mpeg-2 編碼器 DMO 來建立包含 Windows 媒體資料流程或 MPEG 4 串流的 ASF 檔。 此篩選是以 Windows 媒體格式 SDK 為基礎。                    |
| [WST 編解碼器](wst-codec-filter.md)                                               | 解碼及/或複製 WST 解碼篩選器的已解碼和向前更正錯誤的 Teletext 資料。 (已過時。)                                                                                                             |
| [WST 解碼](wst-decoder-filter.md)                                           | 接受 WST 編解碼器中已解碼的全球標準 Teletext 資料，並使用 Microsoft 提供的字型，在重迭 Mixer 上將點陣圖傳遞給釘選2。 (已過時。)                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow參考](directshow-reference.md)
</dt> </dl>

 

 



