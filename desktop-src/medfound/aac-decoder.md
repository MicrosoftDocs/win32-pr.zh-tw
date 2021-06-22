---
description: Microsoft 媒體基礎的 AAC 解碼器是媒體基礎轉換，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC 解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436582"
---
# <a name="aac-decoder"></a>AAC 解碼器

Microsoft 媒體基礎的 AAC 解碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：

-   MPEG-2 AAC 低複雜度 (LC) 設定檔 (多重通道) 。
-   MPEG-2 AAC v1 (多重通道) 搭配 AAC-LC 核心。
-   使用 AAC-LC 核心的 MPEG-2 AAC v2 (身歷聲) 。

AAC 解碼器支援音訊資料傳輸串流中沒有標頭和 AAC 的原始 AAC 串流 (ADTS) 。

從 Windows 8 開始，AAC 解碼器也支援使用多工層來解碼 MPEG-2 音訊廣播串流， (LATM) 和同步處理層 (LOA) 。 它也可以將 LATM/LOA 資料流程轉換為 ADTS。

## <a name="class-identifier"></a>類別識別碼

AAC 編碼器 (CLSID) 的類別識別碼是 **clsid \_ CMSAACDecMFT**，定義于標頭檔 wmcodecdsp 中。

## <a name="media-types"></a>媒體類型

AAC 解碼器支援下列媒體類型。

### <a name="input-types"></a>輸入類型

AAC 解碼器支援下列音訊子類型：



| Subtype                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 標頭       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | Raw AAC 或 ADTS AAC。<br/> 針對此子類型，媒體類型會在應用光譜頻內複寫 (.SBR) 和參數身歷聲 (PS) 工具（如果有的話）之前，提供取樣率和通道數目。 .SBR 工具的效果是將已解碼的取樣率加倍，相對於 core AAC-LC 取樣率。 PS 工具的效果是從 mono 通道核心 AAC-LC 串流解碼身歷聲。<br/> 這個子類型相當於 wmcodecdsp 中定義的 **MEDIASUBTYPE_MPEG_HEAAC**。 請參閱 [音訊子類型 guid](audio-subtype-guids.md)。 <br/> [Mpeg-2 檔案來源](mpeg-4-file-source.md)和 ADTS 剖析器會輸出此子類型。 <br/> | mfapi。h      |
| **MEDIASUBTYPE_RAW_AAC1** | 原始 AAC。 <br/> 此子類型是用於包含在 AAC 中，且音訊格式標記等於 WAVE_FORMAT_RAW_AAC1 (0x00FF) 的 AVI 檔案中的。 <br/> 針對此子類型，媒體類型會提供套用 .SBR 和 PS 工具之後的取樣速率和通道數目（如果有的話）。<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp。h |



 

若要設定 AAC 解碼器，請在輸入媒體類型上設定下列屬性。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>主要類型。</td>
<td>必須是 <strong>MFMediaType_Audio</strong>。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>音訊子類型。</td>
<td>如需詳細資料，請參閱先前的描述。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>音訊設定檔和層級。 <br/></td>
<td>選擇性。 只適用于 <strong>MFAudioFormat_AAC</strong>。 <br/> 這個屬性的值是 <strong>audioProfileLevelIndication</strong> 欄位，如 ISO/IEC 14496-3 所定義。 <br/> 如果不明，請將設定為零或 0xFE (&quot; 未指定任何音訊設定檔 &quot;) 。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>裝載類型。<br/></td>
<td>只適用于 <strong>MFAudioFormat_AAC</strong>。 此解碼器支援下列承載類型： <br/>
<ul>
<li>0：原始 AAC。 資料流程只包含 raw_data_block 的 () 元素，如 MPEG-2 所定義。</li>
<li>1： ADTS。 資料流程包含 adts_sequence 的 () ，如 MPEG-2 所定義。 每個 adts_frame () 只允許一個 raw_data_block () 。</li>
<li>3：具有同步處理層的音訊廣播串流 (LOA) 和多工層 (LATM) 。 在這三種類型的 LOA 中，只支援 <strong>AudioSyncStream</strong> 。 多工層是 <strong>AudioMuxElement</strong>，限制為一個音訊程式和一層。</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> 是選擇性的。 如果未指定此屬性，則會使用預設值0，此值會指定資料流程只包含 raw_data_block 元素。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>已解碼 PCM 音訊所需的位深度。</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>指定喇叭位置的音訊通道指派。</td>
<td>選擇性。 如需詳細資訊，請參閱 <a href="#format-constraints">格式條件約束</a>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>通道的數目，包括低頻率 (LFE) 通道（如果有的話）。<br/></td>
<td>此值的解讀取決於媒體子類型，如先前所述。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>取樣率（以每秒樣本數為單位）。<br/></td>
<td>此值的解讀取決於媒體子類型，如先前所述。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>其他格式資訊。</td>
<td>這個屬性的值取決於子類型。<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>：包含在<strong>WAVEFORMATEX</strong>結構後面出現的部分<a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a>結構， (也就是<strong>wfx</strong>成員) 之後。 後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>：包含 AudioSpecificConfig () 資料。 此資料必須出現;否則，此解碼器將會拒絕媒體類型。</li>
</ul>
AudioSpecificConfig () 資料的長度為2個位元組，適用于 AAC-LC 或 AAC，且具有 .SBR/PS 的隱含信號。 使用 .SBR/PS 的明確信號，AAC 超過2個位元組。<br/> 在 AudioSpecificConfig () 中定義的 <strong>audioObjectType</strong> 值必須是2，表示 AAC-LC。 <strong>ExtensionAudioObjectType</strong>的值必須是5，適用于 .sbr 或29（適用于 PS）。 <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>輸出型別

此解碼器支援下列輸出類型：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>IEEE 浮點音訊。</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>16位 PCM 音訊。</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>需要 Windows 8。 <br/> 此輸出類型可以用來將 LOA/LATM 格式的 AAC 資料流程轉換成 ADTS 格式。 <br/> 若要將 LOA/LATM 資料流程轉換成 ADTS 資料流程，請將輸入類型設定為具有裝載類型 3 (LOA) 的 <strong>MFAudioFormat_AAC</strong> 。 然後，將輸出類型設定為承載類型 1 (ADTS) 的 <strong>MFAudioFormat_AAC</strong> 。 此解碼器將會重新格式化 conainter，而不會解碼位流。 <br/>
<blockquote>
[!Note]<br />
此解碼器不會將 <strong>MFAudioFormat_AAC</strong> 註冊為輸出類型。 但是，如果應用程式設定所述的輸入類型， <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform：： GetOutputAvailableType</strong></a> 方法會傳回可用輸出類型清單中 <strong>MFAudioFormat_AAC</strong> 。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

如果輸入資料流程包含兩個以上的通道，AAC 解碼器會提供輸出格式的兩個選項：

-   與輸入類型相同的通道設定。
-   身歷聲折迭。

## <a name="format-constraints"></a>格式條件約束

已解碼的音訊取樣率必須是下列其中一項，套用 .SBR 之後 (如果存在) ：

-   8 kHz
-   11.025 kHz
-   12 kHz
-   16 kHz
-   22.05 kHz
-   24 kHz
-   32 kHz
-   44.1 kHz
-   48 kHz

不支援超過 48 kHz 的取樣率。

此解碼器支援最多6個音訊通道。 針對每個說話者設定，解碼器預期 AAC 的語法元素會以特定的順序出現。 下表列出支援的說話者設定。 資料表的第三個數據行使用下列標記法來列出預期的語法元素及其順序：

-   <SCE1>：與 front center 喇叭相關聯的 single_channel_element (SCE) 。
-   <SCE2>：與後置的喇叭相關的 SCE。
-   <CPE1>：與 front 喇叭相關聯的 channel_pair_element (CPE) 。
-   <CPE2>：與後 (或側邊) 喇叭相關聯的 CPE
-   <LFE>： Lfe_channel_element (LFE) 。

如需這些語法元素的詳細資訊，請參閱 ISO/IEC 13818-7。



| 組態       | 通道遮罩                                                                                                                                                              | AAC 語法元素                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| 身歷聲或雙 mono | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_LOW_FREQUENCY** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

針對原始 AAC，每個輸入範例必須只包含一個完整的 AAC 壓縮框架。

針對 ADTS，每個輸入範例可以包含多個音訊畫面格，也可以包含部分框架，也就是框架可以橫跨範例界限。 每個 ADTS 標頭後面都必須有一個 AAC 框架。

AAC 解碼器不支援下列任何一項：

-   主要設定檔、Sample-Rate 可調整 (SRS) 設定檔或長期預測 (LTP) 設定檔。
-   音訊資料交換格式 (ADIF) 。
-   LATM/老撾傳輸串流。
-   結合通道元素 (CCEs) 。 此解碼器會使用 CCEs 略過音訊框架。
-   AAC-具有960範例框架大小的 LC。 僅支援 1024-範例框架。

## <a name="transform-attributes"></a>轉換屬性

AAC 解碼器會 [**執行 IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 應用程式可以使用這個方法來取得或設定下列屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>指定雙聲道音訊是否編碼為身歷聲或雙 mono。 視為唯讀。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>指定解碼器如何重現雙重 mono 音訊。 預設值為 [ <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>：輸出 Ch1 至左方和右邊的喇叭。 <br/> 應用程式可以設定此屬性來變更預設行為。<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>AAC 解碼器不會處理動態格式變更，而且必須在設定新的輸入媒體類型之前排清或清空。 將此屬性視為唯讀。 <br/>
<blockquote>
[!Note]<br />
AAC 解碼器錯誤地將此屬性的值報告為 <strong>TRUE</strong> 。
</blockquote>
<br/> <br/> 在 Windows 7 中，解碼器錯誤地將這個屬性的值報告為 <strong>TRUE</strong> 。 在 Windows 8 中，此解碼器會報告 <strong>FALSE</strong>，也就是正確的值<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>範例媒體類型

以下是使用原始 AAC 承載之6通道 48-kHz AAC-LC 串流所需的輸入媒體類型範例：



| 屬性                                                                                      | 值                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00，0x00，0x2a，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x11，0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (選用)                                                                       |



 

[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的前12個位元組會對應到下列 [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)結構成員：

-   **wPayloadType** = 0 (原始 AAC) 
-   **wAudioProfileLevelIndication** = 0X2A (AAC 設定檔，層級 4) 
-   **wStructType** = 0

[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的最後兩個位元組包含 AudioSpecificConfig () 的值，如 mpeg-2 所定義。

-   AudioSpecificConfig. audioObjectType = 2 (AAC LC)  (5 個位) 
-   AudioSpecificConfig. samplingFrequencyIndex = 3 (4 位) 
-   AudioSpecificConfig. channelConfiguration = 6 (4 位) 
-   GASpecificConfig. frameLengthFlag = 0 (1 位) 
-   GASpecificConfig. dependsOnCoreCoder = 0 (1 位) 
-   GASpecificConfig. extensionFlag = 0 (1 位) 

指定此輸入類型時，請使用下列輸出媒體類型，從解碼器取得6通道的32位浮點 PCM 音訊：



| 屬性                                                                                    | 值                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (選用)        |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (選用)             |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3f (選用)           |



 

如果已安裝 Windows Vista 的平臺更新補充，AAC 音訊解碼器可在 Windows Vista 上取得，但只能在 Windows Vista 上使用 [來源讀取器](source-reader.md)來存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Windows 7 上的Msmpeg2adec.dll;</dt><dt>Windows 8 上的MSAudDecMFT.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[AAC 媒體類型](aac-media-types.md)
</dt> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[**Microsoft MPEG-1/DD/AAC 音訊解碼器**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>
