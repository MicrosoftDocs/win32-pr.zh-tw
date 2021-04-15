---
description: 下表列出音訊的媒體子類型 Guid。 在適用的情況下，每個資料表都會列出在 Mmreg 中宣告的相等格式標記。
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: 音訊子類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467655"
---
# <a name="audio-subtypes"></a>音訊子類型

下表列出音訊的媒體子類型 Guid。 在適用的情況下，每個資料表都會列出在 Mmreg 中宣告的相等格式標記。

## <a name="uncompressed-audio-types"></a>未壓縮的音訊類型



| GUID                          | 描述                | 標頭  | 相等的格式標記                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ FLOAT** | IEEE 浮點音訊。 | uuid。h | **WAVE \_格式化 \_ IEEE \_ FLOAT** (0x0003)  |
| **MEDIASUBTYPE \_ PCM**         | PCM 音訊。                 | uuid。h | **WAVE \_格式化 \_ PCM** (0x0001)          |



 

## <a name="mpeg-4-and-aac-audio-types"></a>MPEG 4 和 AAC 音訊類型



| GUID                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | 標頭       | 相等的格式標記                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Advanced Audio 編碼 (AAC 音訊資料傳輸串流中的) 音訊 (ADTS) 格式。<br/> 格式區塊是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構， **wFormatTag** 等於 **WAVE \_ 格式 \_ MPEG \_ ADTS \_ AAC**。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構會指定核心 AAC-LC 取樣率和通道數目（在套用光譜頻內複寫 (.sbr) 或參數身歷聲 (PS) 工具（如果有的話）之前。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構之後不需要額外的資料。<br/>                                                                                                                                                                 | wmcodecdsp。h | **WAVE \_格式化 \_ MPEG \_ ADTS \_ AAC** (0x1600)  |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | High-Efficiency (AAC) 串流的 Advanced 音訊編碼。<br/> 格式區塊是 [**HEAACWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) 結構。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp。h | **WAVE \_格式化 \_ MPEG \_ HEAAC** (0x1610)      |
| **MEDIASUBTYPE \_ MPEG \_ LOA**      | 具有同步處理層的 MPEG-2 音訊廣播串流 (LOA) 和多工層 (LATM) 。<br/> 格式區塊是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構， **wFormatTag** 等於 **WAVE \_ 格式 \_ MPEG \_ loa**。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構會在套用光譜 .SBR 或 PS 工具（如果有的話）之前，指定核心 AAC-LC 取樣率和通道數目。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構之後不需要額外的資料。<br/>                                                                                                                                                                                             | wmcodecdsp。h | **WAVE \_格式化 \_ MPEG \_ loa** (0x1602)       |
| **MEDIASUBTYPE \_ 原始 \_ AAC1**       | 原始 AAC。<br/> 格式區塊是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，其 **wFormatTag** 等於 **WAVE \_ 格式 \_ 原始 \_ AAC1**。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構會在套用 .SBR 和 PS 工具（如果有的話）之後，指定已解碼音訊中的取樣率和通道數目。<br/> [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構後面會接著包含 AudioSpecificConfig () 資料的額外位元組，如 ISO/IEC 14496-3 (mpeg-2 音訊) 所定義。 <br/> AudioSpecificConfig () 資料的長度為2個位元組，適用于 AAC-LC 或 AAC，且具有 .SBR/PS 的隱含信號。 使用 .SBR/PS 的明確信號，AAC 超過2個位元組。<br/> | wmcodecdps。h | **WAVE \_將 \_ 原始 \_ AAC1 格式化** (0x00FF)        |



 

## <a name="dolby-audio-types"></a>杜比音訊類型



| GUID                                | 描述                                                                                                                                                                                                             | 標頭       | 相等的格式標記                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ 杜 \_ DDPLUS**     | 杜比數位加號音訊。                                                                                                                                                                                               | wmcodecdsp。h | n/a                                          |
| **MEDIASUBTYPE \_ 杜 \_ AC3**        | 杜比數位 (AC-3) 音訊。                                                                                                                                                                                             | ksuuids。h    | n/a                                          |
| **MEDIASUBTYPE \_ 杜 \_ AC3 \_ SPDIF** | 透過 S/PDIF 的杜比 AC-3。                                                                                                                                                                                                 | uuid。h      | **WAVE \_格式化 \_ 杜 \_ AC3 \_ SPDIF** (0x0092)  |
| **MEDIASUBTYPE \_ DVM**               | DVM AC-3 編解碼器。 在播放具有杜比數位音訊的 AVI 檔案時使用。<br/> 格式區塊是格式標記等於 **WAVE \_ 格式 \_ DVM** 的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構。<br/> | wmcodecdsp。h | **WAVE \_FORMAT \_ DVM** (0x2000)                |
| **MEDIASUBTYPE \_ 原始 \_ 運動**        | 透過 S/PDIF 的 AC-3;請參閱備註。                                                                                                                                                                                          | uuid。h      | **WAVE \_將 \_ RAW \_ 運動格式化** (0x0240)         |
| **MEDIASUBTYPE \_ SPDIF \_ 標記 \_ 241h**  | 透過 S/PDIF 的 AC-3;請參閱備註。                                                                                                                                                                                          | uuid。h      | **WAVE \_FORMAT \_ ESST \_ AC3** (0x0241)          |



 

若要指定填補的 AC 3，請使用子類型 **MEDIASUBTYPE [ \_ 杜比 \_ AC3 \_ SPDIF**]，其對應至 0x0092 (WAVE \_ 格式 \_ 杜 \_ AC3 \_ spdif) 的格式標記。 0x240 和0x241 的值也用來表示填補的 AC 3，但 Microsoft 鼓勵使用0x0092。

## <a name="miscellaneous-audio-types"></a>其他音訊類型



| GUID                                | 描述                                                                                                                                                                                                                                                                          | 標頭       | 相等的格式標記           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **MEDIASUBTYPE \_ DRM \_ 音訊**        | 具有數位版權管理 (DRM) 保護的音訊。                                                                                                                                                                                                                               | uuid。h      | **WAVE \_將 \_ DRM 格式化** (0x0009)   |
| **MEDIASUBTYPE \_ DTS**               | 數位劇院系統 (DTS) 音訊。<br/> 格式區塊是格式標記等於 **WAVE \_ 格式 \_ UNKNOWN** 的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構。<br/>                                                                                              | ksuuids。h    | n/a                             |
| **MEDIASUBTYPE \_ DTS2**              | 數位劇院系統 (DTS) 音訊。<br/> 格式區塊是格式標記等於 **WAVE \_ 格式 \_ DTS2** 的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構。<br/> 這個子類型相當於 **MEDIASUBTYPE \_ DTS** ，但會使用不同的格式標記。<br/> | wmcodecdsp。h | **WAVE \_FORMAT \_ DTS2** (0x2001)  |
| **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**  | DVD-音訊資料。                                                                                                                                                                                                                                                                      | ksuuids。h    | n/a                             |
| **MEDIASUBTYPE \_ MPEG1AudioPayload** | MPEG-2 音訊承載。                                                                                                                                                                                                                                                                | uuid。h      | **WAVE \_格式化 \_ MPEG** (0x0050)  |
| **MEDIASUBTYPE \_ MPEG1Packet**       | MPEG1 音訊封包。                                                                                                                                                                                                                                                                  | uuid。h      | n/a                             |
| **MEDIASUBTYPE \_ MPEG1Payload**      | MPEG1 音訊承載。                                                                                                                                                                                                                                                                 | uuid。h      | n/a                             |
| **MEDIASUBTYPE \_ MPEG2 \_ 音訊**      | MPEG-2 音訊資料。                                                                                                                                                                                                                                                                   | ksuuids。h    | n/a                             |



 

## <a name="audio-format-tags"></a>音訊格式標記

[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構中的 **wFormatTag** 欄位會指定音訊格式類型。 媒體範例通常是 **WAVEFORMATEX** 結構的 **wBitsPerSample** 欄位中所指定的樣本數。 這不一定適用于可以來自 packetized 資料流程的 MPEG 音訊範例，因此不一定會封裝在範例/框架界限上。 針對 MPEG 音訊，媒體範例中的時間戳記是第一個畫面格的時間戳記，而第一個位元組是包含在媒體範例中。

系統會為每個 **wFormatTag** 定義媒體子類型，如下所示：

-   子類型 GUID 的 Data1 子欄位與 **wFormatTag** 值相同。
-   Data 2 欄位為0。
-   Data 3 欄位為0x0010。
-   Data 4 欄位是0x80、0x00、0x00、0xAA、0x00、0x38、0x9B、0x71。

因此，針對 PCM 音訊，子類型 GUID (在 **MEDIASUBTYPE \_ PCM** 中定義于 uuid. h 中，) 為：

`{00000001-0000-0010-8000-00AA00389B71}`

[**CreateAudioMediaType**](createaudiomediatype.md)函式可以用來從 **WAVEFORMATEX** 結構建立 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構。

## <a name="obsolete-audio-types"></a>過時的音訊類型

下列音訊子類型已淘汰，不應使用：

-   **MEDIASUBTYPE \_ MPEG \_ RAW \_ AAC**
-   **MEDIASUBTYPE \_ PCMAudioObsolete**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

