---
description: 杜比音訊編碼器是媒體基礎轉換 (MFT) 將 mono 或身歷聲音訊編碼為杜比數位，也稱為杜比 AC-3。
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: 杜比數位音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153561"
---
# <a name="dolby-digital-audio-encoder"></a>杜比數位音訊編碼器

杜比音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 將 mono 或身歷聲音訊編碼為杜比數位，也稱為杜比 AC-3。 編碼器不支援多重通道輸入，例如5.1 通道設定。

> [!IMPORTANT]
> 在 Windows 8 之前的 Windows 版本中，Microsoft 應用程式所使用的杜比數位授權方案會限制 Microsoft 的杜比數位技術。

 

如需有關杜比數位音訊的詳細資訊，請參閱 Advanced 電視 Systems 委員會 (ATSC) 檔 *數位音訊壓縮標準 (AC-3、E-AC-3) 修訂 B*。

## <a name="class-identifier"></a>類別識別碼

[杜比音訊編碼器] (CLSID) 的類別識別碼是 **clsid \_ CMSDolbyDigitalEncMFT**，定義于標頭檔 wmcodecdsp 中。

## <a name="output-types"></a>輸出型別

在輸入類型之前，必須先設定輸出類型。 下表列出輸出媒體類型的必要和選擇性屬性。



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>主要類型。</td>
<td>必要。 必須是 <strong>MFMediaType_Audio</strong>。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>音訊子類型。</td>
<td>必要。 必須是 <strong>MFAudioFormat_Dolby_AC3</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>每秒樣本數。</td>
<td>必要。 支援下列值：
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>通道數目。</td>
<td>必要。 必須是 1 (mono) 或 2 (身歷聲) 。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>指定喇叭位置的音訊通道指派。</td>
<td>選擇性。 如果設定，則值必須是 0x3 (front 左方和右聲道) 或 0x4 (front center 頻道) 。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>編碼的 AC-3 串流的位元速率（以每秒位元組數為單位）。</td>
<td>選擇性。 請參閱備註中的有效值。 如果未設定此屬性，則編碼器會使用預設的位元速率，如備註中所述。</td>
</tr>
</tbody>
</table>



 

如果未設定選用的屬性，編碼器會在設定類型之後，將它們新增至媒體類型。

## <a name="input-types"></a>輸入類型

下表列出輸入媒體類型的必要和選擇性屬性。



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>主要類型。</td>
<td>必要。 必須是 <strong>MFMediaType_Audio</strong>。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>音訊子類型。</td>
<td>必要。 必須是 <strong>MFAudioFormat_PCM</strong> 或 <strong>MFAudioFormat_Float</strong>。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>每個音訊樣本的位數數目。</td>
<td>必要。 如果子類型為 <strong>MFAudioFormat_PCM</strong>，則值必須是16，如果是 <strong>MFAudioFormat_Float</strong>子類型，則為32。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>每秒樣本數。</td>
<td>必要。 必須符合輸出類型。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>通道數目。</td>
<td>必要。 必須符合輸出類型。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>區塊對齊（以位元組為單位）。</td>
<td>必要。 計算值，如下所示：
<ul>
<li><strong>MFAudioFormat_PCM</strong>：通道數目×2。</li>
<li><strong>MFAudioFormat_Float</strong>：通道數目×4。</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>編碼 AC3 資料流程的位元速率（以每秒位元組數為單位）。</td>
<td>必要。 每秒必須等於區塊對齊×樣本。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>指定喇叭位置的音訊通道指派。</td>
<td>選擇性。 如果設定，則值必須符合輸出類型。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>每個音訊樣本中音訊資料的有效位數。</td>
<td>選擇性。 如果設定，此值必須等同于 <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>。</td>
</tr>
</tbody>
</table>



 

編碼器不支援取樣率轉換或身歷聲/mono 轉換。

## <a name="remarks"></a>備註

每一頻道的每一台 AC 3 音訊框架包含1536個音訊範例。 不過，編碼器的每個輸入緩衝區可能包含任意數目的 PCM 樣本。 每個輸入緩衝區的大小必須是區塊對齊的倍數。 編碼器會快取輸入範例，直到每個頻道有足夠的1536音訊樣本為止;此時編碼器會輸出一個 AC 3 框架。

每個輸出緩衝區都包含一個原始的 AC 3 框架。 持續時間相當於 1536 PCM 樣本的持續時間，以目前的取樣率為 (32 毫秒) 以 48 kHz 取樣速率、34.83 毫秒（44.1 kHz）和 48 msec （32 kHz) ）。 每個輸出緩衝區的大小取決於位元速率和取樣率。

若要指定編碼位元速率，請在輸出類型中設定 [MF \_ MT \_ 音訊的 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性。 下表顯示編碼位元速率和 MF \_ MT \_ 音訊 \_ \_ \_ 每秒位元組數 \_ 之間的關聯性。



| 位元速率 (kbps)  | [\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_](mf-mt-audio-avg-bytes-per-second-attribute.md) | 備註                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | 僅限 Mono。                                              |
| 80              | 10000                                                                                    | 僅限 Mono。                                              |
| 96              | 12000                                                                                    | 僅限 Mono。                                              |
| 112             | 14000                                                                                    | 僅限 Mono。                                              |
| 128             | 16000                                                                                    | Mono 或身歷聲。                                         |
| 160             | 20000                                                                                    | Mono 或身歷聲。                                         |
| 192             | 24000                                                                                    | Mono 或身歷聲。 這是 mono 的預設設定。   |
| 224             | 28000                                                                                    | Mono 或身歷聲。                                         |
| 256             | 32000                                                                                    | Mono 或身歷聲。 這是身歷聲的預設設定。 |
| 320             | 40000                                                                                    | 僅限身歷聲。                                            |
| 384             | 48000                                                                                    | 僅限身歷聲。                                            |
| 448             | 56000                                                                                    | 僅限身歷聲。                                            |



 

預設的編碼位元速率會設定為 256 kbps （適用于身歷聲）和 192 kbps （mono）。 預設設定會反映在編碼器的 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法所傳回的媒體類型中。

### <a name="example-media-types"></a>範例媒體類型

以下是將16位整數 PCM 編碼的媒體類型範例，以 256 kbps 的預設位元速率為 48-kHz 身歷聲音訊。

輸出媒體類型：

| 屬性                                                                           | 值                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ 音訊**        |
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ 杜 \_ AC3** |
| [\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [MF \_ MT \_ 音訊 \_ 數目 \_ 通道](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

輸入媒體類型：

| 屬性                                                                                | 值                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ 音訊** |
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ MT \_ 音訊 \_ 數目 \_ 通道](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 




