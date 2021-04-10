---
description: Microsoft 媒體基礎的 AAC 編碼器是媒體基礎的轉換，它會編碼 Advanced 音訊編碼 (AAC) 低複雜性 (LC) 設定檔，如 ISO/IEC 13818-7 (MPEG-2 音訊第7部分) 所定義。
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: AAC 編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848110"
---
# <a name="aac-encoder"></a>AAC 編碼器

Microsoft 媒體基礎的 AAC 編碼器是 [媒體基礎的轉換](media-foundation-transforms.md) ，它會編碼 Advanced 音訊編碼 (AAC) 低複雜性 (LC) 設定檔，如 ISO/IEC 13818-7 (Mpeg-2 音訊第7部分) 所定義。

AAC 編碼器不支援對任何其他 AAC 設定檔（例如 Main、SSR 或 LTP）進行編碼。

## <a name="class-identifier"></a>類別識別碼

AAC 編碼器 (CLSID) 的類別識別碼是 **clsid \_ AACMFTEncoder**，定義于標頭檔 wmcodecdsp 中。

## <a name="media-types"></a>媒體類型

AAC 編碼器支援下列媒體類型。 您可以將類型設定為 [第一個]、[第一個] 或 [輸出類型]。

### <a name="input-types"></a>輸入類型

在輸入媒體類型上設定下列屬性。



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
<td>亞。</td>
<td>必須是 <strong>MFAudioFormat_PCM</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>每個樣本的位數。</td>
<td>必須是16。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>每秒樣本數。</td>
<td>支援下列值：
<ul>
<li>44100 (44.1 KHz) </li>
<li>48000 (48 KHz) </li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>通道數目。</td>
<td>必須是 1 (mono) 或 2 (身歷聲) 或 6 (5.1) 。
<blockquote>
[!Note]<br />
Windows 10 引進了6個音訊通道的支援，且不適用於舊版的 Windows。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

設定輸入類型之後，編碼器會衍生下列值，並將其新增至媒體類型：

-   [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>輸出型別

在輸出媒體類型上設定下列屬性。



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
<td>必須是 <strong>MFAudioFormat_AAC</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>每個樣本的位數。</td>
<td>必須是16。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>每秒樣本數。</td>
<td>必須符合輸入類型。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>通道數目。</td>
<td>必須符合輸入類型。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>編碼 AAC 資料流程的位元速率（以每秒位元組數為單位）。</td>
<td>支援下列值：
<ul>
<li>12000</li>
<li>16000</li>
<li>20000</li>
<li>24000</li>
</ul>
Mono 和身歷聲的預設值為 12000 (96 Kbps) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>AAC 裝載類型。</td>
<td>選擇性。 如果設定，此值必須為零，表示資料流程只包含 raw_data_block 元素。<br/> 選擇性。 如果未設定屬性，則預設值為零，表示資料流程只包含 (原始 AAC) 的 raw_data_block 元素。 <br/> 在 Windows 7 中，如果已設定此屬性，則值必須為零。<br/> 從 Windows 8 開始，值可以是 0 (原始 AAC) 或 1 (ADTS AAC) 。 <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>AAC 音訊設定檔和層級。</td>
<td>選擇性。 支援下列值：
<ul>
<li>0x29 (預設) </li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2C</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

下表列出可用於 MF_MT_AAC_PROFILE_LEVEL_INDICATION 屬性的值。

| MF_MT_AAC_PROFILE_LEVEL_INDICATION 值 | 設定檔                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | AAC Profile L2                    | 
| 0x2A                                     | AAC 設定檔 L4                    | 
| 0x2B                                     | AAC 設定檔 L5                    | 
| 0x2C                                     | 高效率 v1 AAC 設定檔 L2 | 
| 0x2E                                     | 高效率 v1 AAC 設定檔 L4 | 
| 0x2F                                     | 高效率 v1 AAC 設定檔 L5 | 
| 0x30                                     | 高效率 v2 AAC 設定檔 L2 | 
| 0x31                                     | 高效率 v2 AAC 設定檔 L3 | 
| 0x32                                     | 高效率 v2 AAC 設定檔 L4 | 
| 0x33                                     | 高效率 v2 AAC 設定檔 L5 | 

 

設定輸出類型之後，AAC 編碼器會藉由新增 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性來更新類型。 這個屬性（attribute）包含在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構後面出現的 [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)結構部分 (也就是 **wfx** 成員) 之後。 後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。

每個輸出範例都包含一個不含標頭的壓縮 AAC 框架。 此格式相當於 MPEG-2 所定義的原始 \_ 資料 \_ 區塊 () 元素。 如果輸出類型中有 [ [MF \_ MT \_ AAC 裝載 \_ \_ 類型](mf-mt-aac-payload-type.md) ] 屬性，則必須設定為 [零]，以指出此裝載類型。

每個輸出範例都包含一個對應到 1024 PCM 範例的壓縮 AAC 框架。 例如，在 48 Khz 取樣率，一個壓縮框架的持續時間是21.33 毫秒。

如果 [MF \_ MT \_ AAC \_ 裝載 \_ 類型](mf-mt-aac-payload-type.md) 為零 (預設值) ，則每個輸出範例都會包含一個原始 \_ 資料 \_ 區塊 () 元素，如 ISO/IEC 13818-7 所定義。

## <a name="example-media-types"></a>範例媒體類型

以下是從 44.1-kHz、160 Kbps 身歷聲音訊編碼至原始 AAC 時所需的媒體類型範例

輸入媒體類型：



| 屬性                                                                                    | 值                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ 音訊** |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (選用)       |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)             | 4 (選用)            |
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md)         | 1 (選用)            |
| [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (選用)      |
| [**MF \_ MT \_ 固定 \_ 大小 \_ 範例**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (選用)            |



 

輸出媒體類型：



| 屬性                                                                                      | 值                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                                      | **MFMediaType \_ 音訊**                                                                          |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [MF \_ MT \_ AAC \_ 裝載 \_ 類型](mf-mt-aac-payload-type.md)                                       | 0 (選用)                                                                                     |
| [MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (選用)                                                                                  |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)               | 1 (選用)                                                                                     |
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md)           | 0 (選用)                                                                                     |
| [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (選用)                                                                                |
| [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md)                                        | {0x00，0x00，0x29，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x12，0x10} (選用)  |



 

## <a name="remarks"></a>備註

在目前的執行中，每個輸入範例都必須有有效的時間和持續時間。 若要設定取樣時間，請呼叫 [**IMFSample：： SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)。 若要設定範例持續時間，請呼叫 [**IMFSample：： SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)。

如果未設定範例時間，編碼器的 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法會傳回 **MF \_ E \_ NO \_ 範例 \_ 時間戳記**。 如果未設定範例持續時間， **ProcessInput** 方法會傳回 **MF \_ E \_ 無 \_ 範例 \_ 持續時間**。

範例持續時間可以計算如下：


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



其中 *nAudioSamplesPerChannel* 是輸入緩衝區中每個通道的 PCM 音訊樣本數目，而 *nSamplesPerSec* 則是取樣率（以樣本/秒為單位）。

> [!Note]  
> 由於目前的執行中有錯誤，如果範例持續時間設定為零，則 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 呼叫會成功，但後續呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 將會擲回零除的例外狀況。 若要避免這個錯誤，請在每個輸入範例上設定有效的非零持續時間。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[**AAC 解碼器**](aac-decoder.md)
</dt> <dt>

[AAC 媒體類型](aac-media-types.md)
</dt> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

