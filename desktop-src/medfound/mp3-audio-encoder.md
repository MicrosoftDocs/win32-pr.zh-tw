---
description: Microsoft 媒體基礎。
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: MP3 音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026395"
---
# <a name="mp3-audio-encoder"></a>MP3 音訊編碼器

Microsoft 媒體基礎 MP3 音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可將 mpeg-2 的第3層 (MP3) 音訊編碼。

## <a name="class-identifier"></a>類別識別碼

MP3 編碼器 (CLSID) 的類別識別碼是 **clsid \_ MP3ACMCodecWrapper**，定義于標頭檔 wmcodecdsp 中。

## <a name="media-types"></a>媒體類型

MP3 編碼器支援下列媒體類型。 輸出類型必須在輸入類型之前設定。

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
<td>必須是 <strong>MFAudioFormat_MP3</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>編碼的 MP3 資料流程的位元速率（以每秒位元組數為單位）。</td>
<td>編碼器支援標準 (32、40、48、56、64、80、96、112、128、160、192、224、256或 320 Kbps) 所定義的所有位元速率。<br/> 適用于 mono 的預設位元速率為 128 Kbps，身歷聲為 320 Kbps。<br/> 您可以使用這個屬性來指定編碼的位元速率。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>通道數目。</td>
<td>支援下列值：
<ul>
<li>1 (mono)</li>
<li>2 (身歷聲) </li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>每秒樣本數。</td>
<td>支援下列值：
<ul>
<li>48000 (48 KHz) </li>
<li>44100 (44.1 KHz) </li>
<li>32000 (32 KHz) </li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>其他編解碼器資料。</td>
<td>這個屬性包含 <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> 結構的12個位元組，該結構會遵循該結構的 <strong>wfx</strong> 成員。</td>
</tr>
</tbody>
</table>



 

或者，您可以填入 [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) 結構，然後呼叫 [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) 將結構轉換成媒體基礎的媒體類型。

### <a name="input-types"></a>輸入類型

在輸入媒體類型上設定下列屬性。



| 屬性                                                                               | 描述         | 備註                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                               | 主要類型。         | 必須是 **MFMediaType \_ 音訊**。 |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                      | 亞。            | 必須是 **MFAudioFormat \_ PCM**。 |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)       | 每個樣本的位數。    | 必須是16。                     |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md) | 每秒樣本數。 | 必須符合輸出類型。     |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)              | 通道數目。 | 必須符合輸出類型。     |



 

編碼器僅支援16位的整數 PCM 輸入。 它不支援32位浮點數輸入。

### <a name="media-formats"></a>媒體格式

MPEG 1 和 MPEG-2 標準定義252第3層音訊格式。 MP3 編碼器支援具有一些例外狀況的標準，以及一些其他格式，如下所述。 第3層定義如下：



| 需求 | 值 |
|----------------------------------|---------------------------------------------------------------|
| 通道                         | mono 或身歷聲                                                |
| 以 kHz 為例的 MPEG-2 取樣率       | 44.1、48、32                                                  |
| MPEG-2 編碼的位元速率（kbps） | 32、40、48、56、64、80、96、112、128、160、192、224、256、320 |
| MPEG-2 範例速率（kHz）       | 8、11.025、12、16、22.05、24                                  |
| MPEG-2 編碼的位元速率（kbps） | 8、16、24、32、40、48、56、64、80、96、112、144、160          |



 

MP3 編碼器也支援下列格式。



| 採樣速率 | 位元速度     | 頻道號碼 |
|-------------|--------------|----------------|
| 8000        | 18000、20000 | 2              |
| 11025       | 18000、20000 | 1 或 2         |
| 12000       | 18000、20000 | 1 或 2         |
| 16000       | 18000、20000 | 1              |
| 32000       | 144000       | 1 或 2         |
| 44100       | 144000       | 1 或 2         |
| 48000       | 144000       | 1 或 2         |



 

MP3 編碼器不支援標準所定義的下列格式。



| 採樣速率 | 位元速率                                    | 頻道號碼 |
|-------------|----------------------------------------------|----------------|
| 12000       | 80000、96000、112000、128000、144000、160000 | 1 或 2         |
| 11025       | 80000、96000、112000、128000、144000、160000 | 1 或 2         |
| 8000        | 80000、96000、112000、128000、144000、160000 | 1 或 2         |
| 8000        | 8000、11025、12000、16000、22050、24000      | 2              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
