---
description: 本主題說明如何在媒體基礎中指定 Advanced Audio 編碼 (AAC) 資料流程的格式。
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: AAC 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945593"
---
# <a name="aac-media-types"></a>AAC 媒體類型

本主題說明如何在媒體基礎中指定 Advanced Audio 編碼 (AAC) 資料流程的格式。

針對 AAC 音訊定義了兩個子類型：



| Subtype                     | 描述          | 標頭       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | Raw AAC 或 ADTS AAC。 | mfapi。h      |
| **MEDIASUBTYPE \_ 原始 \_ AAC1** | 原始 AAC。             | wmcodecdsp。h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

針對此子類型，媒體類型會在應用光譜頻內複寫 (.SBR) 和參數身歷聲 (PS) 工具（如果有的話）之前，提供取樣率和通道數目。 .SBR 工具的效果是將已解碼的取樣率加倍，相對於 core AAC-LC 取樣率。 PS 工具的效果是從 mono 通道核心 AAC-LC 串流解碼身歷聲。

此子類型相當於 **MEDIASUBTYPE \_ MPEG \_ HEAAC**，定義于 wmcodecdsp 中。 請參閱 [音訊子類型 guid](audio-subtype-guids.md)。

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ 原始 \_ AAC1
</dt> <dd>

這個子類型是用於包含在 AVI 檔案中的 AAC，且其音訊格式標記等於 WAVE \_ 格式的 \_ RAW \_ AAC1 (0x00FF) 。

針對此子類型，媒體類型會提供套用 .SBR 和 PS 工具之後的取樣速率和通道數目（如果有的話）。

</dd> </dl>

下列媒體類型屬性適用于 AAC 音訊。



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>主要類型。 必須是 <strong>MFMediaType_Audio</strong>。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>音訊子類型。 如需詳細資料，請參閱先前的描述。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>音訊設定檔和層級。 <br/> 這個屬性的值是 <strong>audioProfileLevelIndication</strong> 欄位，如 ISO/IEC 14496-3 所定義。<br/> 如果不明，請將設定為零或 0xFE (&quot; 未指定任何音訊設定檔 &quot;) 。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>編碼 AAC 資料流程的位元速率（以每秒位元組數為單位）。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>裝載類型。<br/> 只適用于 <strong>MFAudioFormat_AAC</strong>。<br/> <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> 是選擇性的。 如果未指定此屬性，則會使用預設值0，此值會指定資料流程只包含 raw_data_block 元素。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>已解碼 PCM 音訊的位深度。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>將音訊頻道指派給喇叭位置。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>通道的數目，包括低頻率 (LFE) 通道（如果有的話）。<br/> 此值的解讀取決於媒體子類型，如先前所述。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>取樣率（以每秒樣本數為單位）。<br/> 此值的解讀取決於媒體子類型，如先前所述。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>這個屬性的值取決於子類型：<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>：包含在<strong>WAVEFORMATEX</strong>結構後面出現的部分<a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a>結構， (也就是<strong>wfx</strong>成員) 之後。 後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>：包含 AudioSpecificConfig () 資料。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

