---
description: 隨著需要壓縮音訊格式的媒體存放裝置增加，應用程式必須識別、描述和使用各種新編碼的音訊內容，以將內容從電腦傳輸至裝置，例如 HDMI 或 DisplayPort 接收者。
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: 表示 IEC 61937 傳輸的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0de8fb8910ee3534d8878cdab2c35a01f17115de477ba30ea821e89ae11b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018286"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>表示 IEC 61937 傳輸的格式

隨著需要壓縮音訊格式的媒體存放裝置增加，應用程式必須識別、描述和使用各種新編碼的音訊內容，以將內容從電腦傳輸至裝置，例如 HDMI 或 DisplayPort 接收者。

若要代表要透過 IEC 61937 相容介面傳輸的編碼音訊串流，應用程式必須提供：

-   要傳輸的編碼音訊資料流程特性。

-   目標裝置上已解碼音訊串流的特性。

在 Windows Vista 和 Windows 舊版的作業系統中，應用程式可以從通道數目、取樣大小，以及使用此格式之音訊串流的資料速率，推斷音訊格式的品質等級。 針對 PCM 格式，可從指定格式的 **WAVEFORMATEX** 結構的 **nChannels**、 **nSamplesPerSec** 和 **nAvgBytesPerSec** 成員取得這項資訊。 針對非 PCM 格式，已 commandeered 這三個成員，以將壓縮資料的相關資訊儲存在音訊資料流程中。 因此， **WAVEFORMATEX** 結構在解壓縮並播放串流之後，缺乏非 PCM 音訊串流的有效通道、取樣大小和資料速率的相關資訊。 根據此結構中的資訊，使用者或應用程式可能難以推斷非 PCM 串流的品質等級。

**WAVEFORMATEX** 已延伸至 **WAVEFORMATEXTENSIBLE** 結構，以提供額外的資料流程特性。 不過，此結構也不適合用來描述 IEC 61937 傳輸的資料流程，因為它的目的是要代表一組特性，並且用於未壓縮的多重通道 PCM 資料。

在 Windows 7 中，作業系統會提供新結構 **WAVEFORMATEXTENSIBLE \_ IEC61937** 的支援，以擴充 **WAVEFORMATEXTENSIBLE** 結構來儲存兩組音訊資料流程特性，藉此解決這個問題：編碼的音訊格式在音訊串流解碼後的傳輸和特性。 新的結構會明確指定非 PCM 格式的通道、樣本大小和資料速率的有效數目。 利用這項資訊，應用程式可以在解壓縮並播放非 PCM 串流之後，推斷其品質層級。

**WAVEFORMATEXTENSIBLE \_ IEC61937** 結構是在 Windows 7 SDK 隨附的 KsMedia. h 標頭中宣告的。 **FormatExt** 成員是 **WAVEFORMATEXTENSIBLE** 結構，可儲存要傳送之資料流程的特性。 **WAVEFORMATEXTENSIBLE** 結構的 **格式** 成員是 **WAVEFORMATEX** 結構。 這個 **WAVEFORMATEX** 和 **WAVEFORMATEXTENSIBLE** 的內容會向應用程式指出結構是否可解釋為 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構。 針對 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構：

-   **WAVEFORMATEX** 的 **wFormatTag** 成員必須包含可延伸 \_ () 的 WAVE 格式 \_ `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` 。

-   **WAVEFORMATEXTENSIBLE** 結構的 **SubFormat** 成員會指定要傳送之編碼格式的 GUID。 例如， `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` 表示杜比數位加上的格式。 如需支援的 Guid，請參閱 SubFormat Guid。

-   WAVEFORMATEX 的 **cbSize** 成員所指定的大小為34個位元組。 (`FormatExt.Format.cbSize = 34`). **WAVEFORMATEXTENSIBLE \_ IEC61937** 的總大小為52個位元組。

**WAVEFORMATEXTENSIBLE \_ IEC61937** 的 **DwEncodedSamplesPerSec**、 **dwEncodedChannelCount** 和 **dwAverageBytesPerSec** 成員會描述取樣率、通道數目，以及音訊串流在解碼後的位元組位元速率（以位元組為單位）。

## <a name="subformat-guids"></a>SubFormat Guid

在 Windows 7 中，KsMedia 標頭包含 CEA-861-D 所定義之壓縮音訊格式的 SubFormat guid 定義。 Guid 是在 **WAVEFORMATEXTENSIBLE** 的 SubFormat 成員中指定，在 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構的 **FormatExt** 成員中指定 (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`) 。

下表列出以標準 IEC 61937 編碼音訊格式提供之壓縮音訊格式的 Guid。 這些格式類似于現有的使用中程式碼 3 (AC-3) 和數位劇院音效 (DTS) 格式標記法 Windows。



| CEA 861 類型 | SubFormat GUID                                                                                                          | 描述                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | 請參閱資料流程。                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ WAVEFORMATEX<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG1<br/>                       | MPEG-2 (第1層 & 2)                          |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG3<br/>                       | MPEG-2 (第3層)                              |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (多重通道)                          |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ AAC<br/>                         | Advanced Audio 編碼 (ADTS) 中的 MPEG-2/4 AAC |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0a         | 0000000a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號<br/>        | 杜比數位加號                           |
| 0x0a         | 0000010a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ PLUS \_ ATMOS<br/> | 以杜比數位加號編碼的杜比 Atmos  |
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS \_ HD<br/> | DTS HD  |
| 0x0b         | 0000010b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ .dtsx \_ E1<br/> | DTS： X E1  |
| 0x0b         | 0000030b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ .dtsx \_ E2<br/> | DTS： X E2  |
| 0x0f         |                                                                                                                         | 未使用的保留                              |



 

下表列出以高位速率音訊範例封包傳輸的壓縮音訊格式 Guid。



| CEA 861 類型 | SubFormat GUID                                                                                           | 描述                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 位、96Khz)                                                                                                           |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MLP<br/>   | 杜比1.0：<br/> 杜比 TrueHD (MLP –經線無失真封裝) –24位 192KHz/高達 18 Mbps、8個通道)  <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MAT20<br/> | 杜比2.0： <br/> 杜比 TrueHD –24位 192KHz/最高可達 18 Mbps、8個通道或 LPCM，最高可達 24 Mbps。 <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MAT21<br/> | 杜比2.1： <br/> 杜比 TrueHD –24位 192KHz/最高可達 18 Mbps、8個通道或 LPCM，最高可達 24 Mbps。 <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ WMA \_ PRO<br/>     | WindowsMedia Audio (WMA) Pro                                                                                                   |



 

Microsoft 提供的 HD 音訊類別驅動程式支援 PCM、AC3、DTS、AAC、杜數位 Plus、WMA Pro、 (MLP) 格式。 HD 音訊類別驅動程式不支援且可由協力廠商解決方案執行的壓縮音訊格式 Guid，如下表所示。



| CEA 861 類型 | SubFormat GUID                                                                                              | 描述                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ ATRAC<br/>           | 適應性轉換聲場編碼 (ATRAC)                                      |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 一個 \_ 位 \_ 音訊<br/> | One-Bit 音訊                                                                  |
| 0x0d         | 0000000d-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DST<br/>             | 直接串流傳輸 (DST) —無失真壓縮的 DSD (直接串流數位) 。 |



 

## <a name="dolby-digital-plus-format"></a>杜比數位加號格式

當杜比數位 Plus 內容透過 IEC 60958 傳輸時，連結取樣率必須是內容取樣率的四倍。 杜比數位加號支援 32 KHz、44.1 KHz 和 48 KHz 的內容取樣率。 HDMI 等介面不支援 128 KHz (32 KHz x 4) ，因此只能支援44.1 和 48 KHz 內容範例速率。

下列範例顯示以 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以代表內容取樣率 48 KHz 的杜比數位格式。


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>TrueHD () 的杜比

杜比 TrueHD 內容會透過 IEC 60958 在 176.4 kHz/8 通道上傳輸， (要求 60958 44.1、88.2 和 176.4 kHz 之 705.6 kHz 的) 畫面播放速率，以及 192 kHz/8 通道 (需要適用于60958、768和 48 kHz 之內容取樣速率的 IEC 96 幀) 速率。

下列範例顯示 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以代表內容取樣率為 96 KHz 的杜比 TrueHD。

杜比1。0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



杜比2。0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



杜比2。1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> 支援某個版本的杜比，不表示支援較低版本號碼的杜比。 由於杜比2.1 可回溯相容于舊版的杜比，因此指出支援杜比的類別驅動程式通常也會指出針對每個版本使用不同的 WAVEFORMATEXTENSIBLE IEC61937 結構，以2.0 支援杜比、2.1 和1.0。 \_

 

## <a name="wma-pro"></a>WMA Pro

WMA Pro 音訊內容可在下表所列的四個設定檔中的其中一個進行編碼。



| 設定檔 | 屬性-值                                                                                                                                                                                                                                                      | 描述                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | 最大位元速率– 192000 bps <br/> 最大取樣率– 48 KHz <br/> 最大頻道計數-2 <br/> 緩衝區大小上限– 600 \* 1024 位 <br/> 每一框架的樣本數上限-2048 <br/> 每一框架的最大位數-655536<br/>   | 建議使用無線音樂和串流。<br/> 音訊框架中的最大位元速率為 1536000 bps。<br/>          |
| M1      | 最大位元速率– 385000 bps <br/> 最大取樣率– 48 KHz <br/> 最大頻道計數–6 <br/> 緩衝區大小上限– 600 \* 1024 位 <br/> 每一框架的樣本數上限-4096 <br/> 每一框架的最大位數-131072<br/>   | 建議用於環繞音效標準定義影片。<br/> 音訊框架中的最大位元速率為 1536000 bps。<br/> |
| M2      | 最大位元速率– 769000 bps <br/> 最大取樣率– 96 KHz <br/> 最大頻道計數–6 <br/> 緩衝區大小上限– 1200 \* 1024 位 <br/> 每一框架的樣本數上限-4096 <br/> 每一框架的最大位數-131072<br/>  | 適用于環繞音效高定義電影的建議。<br/> 音訊框架中的最大速率是 3072000 bps。<br/>         |
| M3      | 最大位元速率– 3000000 bps <br/> 最大取樣率– 96 KHz <br/> 最大頻道計數–8 <br/> 緩衝區大小上限– 2400 \* 1024 位 <br/> 每一框架的樣本數上限-4096 <br/> 每一框架的最大位數-131072<br/> | 適用于數位劇院的建議。<br/> 音訊框架中的最大速率是 3072000 bps。<br/>                               |



 

M0 和 M1 設定檔適用于 48 KHz/16 位/身歷聲 (1536000 bps) IEC 60958 串流。 M2 和 M3 設定檔適用于 96 KHz/16 位/身歷聲 (3072000 bps) IEC 60958 串流。

下列範例顯示 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以將 WMA Pro 表示為 M2 設定檔。


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置格式](device-formats.md)
</dt> </dl>

 

 




