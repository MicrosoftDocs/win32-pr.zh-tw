---
description: 杜比音訊解碼器是一種會將杜比數位 (AC-3) 和杜比數位加號解碼的 MFT。
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: 杜比音訊解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689308"
---
# <a name="dolby-audio-decoder"></a>杜比音訊解碼器

杜比音訊解碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可將下列串流類型解碼：

-   杜比數位，也稱為杜比 AC-3
-   杜比數位 Plus，也稱為增強的 AC-3 (E-AC-3) 

> [!IMPORTANT]
> 在 Windows 8 之前的 Windows 版本中，Microsoft 應用程式所使用的杜比數位授權方案會限制 Microsoft 的杜比數位技術。

 

如需這些格式的詳細資訊，請參閱 Advanced 電視 Systems 委員會 (ATSC) 檔 *數位音訊壓縮標準 (AC-3、E-AC-3) 修訂 B*。

此解碼器也可以將杜比數位加號串流轉換為 AC-3 S/PIDF 輸出的杜數位格式，或為 HDMI 數位輸出格式化杜比數位的資料流程。

## <a name="class-identifier"></a>類別識別碼

[杜比音訊解碼器] (CLSID) 的類別識別碼是 **clsid \_ CMSDDPlusDecMFT**，定義于標頭檔 wmcodecdsp 中。

## <a name="input-types"></a>輸入類型

杜比音訊解碼器支援下列輸入子類型。



| Subtype                                 | 描述                                                                                                                                                 | 標頭       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ 杜 \_ AC3**            | 杜比數位音訊。                                                                                                                                        | mfapi。h      |
| **MEDIASUBTYPE \_ DVM**                   | 杜比數位音訊;請參閱 [**音訊子類型**](../directshow/audio-subtypes.md)。 此子類型可與 **MEDIASUBTYPE \_ 杜比 \_ AC3** 互換使用。<br/> | wmcodecdsp。h |
| **MFAudioFormat \_ 杜比 \_ 數位 \_ 加號** | 杜比數位加號音訊。                                                                                                                                   | mfapi。h      |



 

下表列出輸入媒體類型的需要和選擇性屬性。



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
<td>必要。 請參閱上表以取得詳細資料。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>取樣率（以每秒樣本數為單位）。</td>
<td>選擇性。 有效的值為：48000、44100、32000、24000、22050和16000。 如果未設定此屬性，則預設值為48000。 <br/>
<blockquote>
[!Note]<br />
這份清單中的三個最高比率僅限最高的 AC-3 個串流。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</td>
<td>選擇性。 有效值的範圍為 1 (mono) 為 8 (7.1 channel configuration) 。 如果未設定此屬性，預設值為 2 (身歷聲) 。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>指定喇叭位置的音訊通道指派。</td>
<td>選擇性。 如果有指定，此值必須與音訊通道的數目一致。 如果未設定屬性，則會使用預設通道遮罩（以通道數目為基礎）。</td>
</tr>
</tbody>
</table>



 

下表列出支援的杜比通道設定。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>通道設定</th>
<th>通道數目</th>
<th>通道遮罩</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1/0 (mono) </td>
<td>1</td>
<td>0x4 (<strong>SPEAKER_FRONT_CENTER</strong>) </td>
</tr>
<tr class="even">
<td>2/0 (身歷聲) 或 1 + 1 (雙 mono) </td>
<td>2</td>
<td>0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>) </td>
</tr>
<tr class="odd">
<td>3/0</td>
<td>3</td>
<td>0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> |SPEAKER_FRONT_CENTER) </td>
</tr>
<tr class="even">
<td>2/1</td>
<td>3</td>
<td>0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>) </td>
</tr>
<tr class="odd">
<td>3/1</td>
<td>4</td>
<td>0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>) </td>
</tr>
<tr class="even">
<td>2/2</td>
<td>4</td>
<td>0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>) <br/> 或<br/> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)  <br/></td>
</tr>
<tr class="odd">
<td>3/2</td>
<td>5</td>
<td>0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong></strong> SPEAKER_BACK_RIGHT) <br/> 或<br/> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong></strong> SPEAKER_SIDE_RIGHT)  <br/></td>
</tr>
<tr class="even">
<td>3/2 + LFE</td>
<td>6</td>
<td>0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong></strong>  |  <strong></strong> SPEAKER_BACK_LEFT SPEAKER_BACK_RIGHT) <br/> 或<br/> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong></strong>  |  <strong></strong> SPEAKER_SIDE_LEFT SPEAKER_SIDE_RIGHT) <br/></td>
</tr>
<tr class="odd">
<td>3/2/2 + LFE
<blockquote>
[!Note]<br />
僅限杜比數位加號。
</blockquote>
<br/> <br/></td>
<td>8</td>
<td>0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> |SPEAKER_SIDE_LEFT |SPEAKER_SIDE_RIGHT) </td>
</tr>
</tbody>
</table>



 

此外，通道設定1/0、2/0、3/0、2/1、3/1 和2/2 也可能出現 LFE 通道。

## <a name="output-types"></a>輸出型別

杜比音訊解碼器支援下列輸出子類型。



| Subtype                                                   | 描述                                                                                                                               | 標頭    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ 杜 \_ AC3 \_ SPDIF**                      | 針對 S/PDIF 數位輸出格式化的 AC-3 音訊。                                                                                     | mfapi。h   |
| **KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號** | 針對 HDMI 數位輸出格式化的杜數位加音訊。                                                                               | ksmedia。h |
| **MFAudioFormat \_ 浮點數**                                  | IEEE 32 位浮點 PCM 音訊<br/> **Windows 10**：身歷聲、5.1、7。1<br/> **先前的版本**：身歷聲、5。1<br/> | mfapi。h   |
| **MFAudioFormat \_ PCM**                                    | 16位 PCM 音訊<br/> **Windows 10**：身歷聲、5.1、7。1<br/> **先前的版本**：身歷聲、5。1<br/>                     | mfapi。h   |



 

下表列出輸出媒體類型的必要和選擇性屬性。



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
<td>必要。 請參閱上表以取得詳細資料。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>取樣率（以每秒樣本數為單位）。</td>
<td>必要。 有效的值為：48000、44100、32000、24000、22050和16000。 輸出取樣率必須與輸入取樣率相同。 此解碼器無法變更資料流程的取樣率。</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</td>
<td>PCM 輸出的必要參數。 <br/> 數位輸出不需要。 <br/> 如果輸入類型是 mono、身歷聲或雙 mono (全都不會有 LFE 通道) ，唯一有效的值為2，表示身歷聲輸出。 否則，此值可以是： <br/>
<ul>
<li>適用于身歷聲 downmix 的2</li>
<li>6適用于5.1 通道設定</li>
<li>7.1 通道設定為8</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>指定喇叭位置的音訊通道指派。</td>
<td>如果通道數目大於2，則需要進行 PCM 輸出。 值必須是：<br/>
<ul>
<li>0x3 的身歷聲輸出</li>
<li>5.1 通道輸出的0x3F</li>
<li>7.1 通道輸出的0x63F</li>
</ul>
數位輸出不需要。 <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>每個音訊樣本的位數數目。</td>
<td>PCM 輸出的必要參數。 <strong>MFAudioFormat_Float</strong>的值必須是32，而<strong>MFAudioFormat_PCM</strong>的值必須是16。<br/> 數位輸出不需要。<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>每個音訊樣本中音訊資料的有效位數。</td>
<td>PCM 輸出的選擇性。 如果設定，此值必須等同于 <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>。<br/> 數位輸出子類型不需要。<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>區塊對齊（以位元組為單位）。</td>
<td>PCM 輸出的選擇性。 數位輸出不需要。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>每秒的平均位元組數。</td>
<td>PCM 輸出的選擇性。 數位輸出不需要。</td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a>轉換屬性

杜比音訊解碼器會實 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 應用程式可以使用這個方法來取得或設定下列屬性。



| 屬性                                                                                | 描述                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | 指定2通道杜比音訊資料流程是否編碼為身歷聲或雙 mono。 在解碼第一個杜比框架之前，此值為 **eAVDecAudioDualMono \_ 未指定**。 解碼開始之後，此值會反映最近的杜比框架。<br/> 唯讀。 <br/> |
| [CODECAPI \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | 指定解碼器如何重現雙重 mono 音訊。 預設值為 **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**。 應用程式可以隨時設定這個屬性。<br/> 讀取/寫入<br/>                                                                            |
| [CODECAPI \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | 針對杜比數位 (AC-3) 串流，指定輸入資料流程的位元速率（以位/秒為單位）。 針對杜比數位 Plus (E-AC3) ，此值一律為零。<br/> 唯讀。<br/>                                                                                              |
| [CODECAPI \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | 當解碼器執行動態範圍控制時的高階剪下。<br/> 讀取/寫入<br/>                                                                                                                                                                                    |
| [CODECAPI \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | 當解碼器執行動態範圍控制時，低層級的提升。<br/> 讀取/寫入<br/>                                                                                                                                                                                   |
| [CODECAPI \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | 壓縮控制模式。<br/> 讀取/寫入<br/>                                                                                                                                                                                                                          |
| [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | 身歷聲 downmix 的類型。 當輸入是多聲道資料流程且輸出為身歷聲資料流程時，就會套用此屬性。<br/> 讀取/寫入<br/>                                                                                                                           |
| [MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更](mft-support-dynamic-format-change-attribute.md) | 這個屬性會傳回 **FALSE**，表示在設定新的輸入類型之前，必須先清空解碼器。<br/> 讀取/寫入<br/>                                                                                                                                          |



 

## <a name="remarks"></a>備註

此解碼器只接受原始的杜比串流，如/52B 所定義。 不支援承載（例如 Packetized 基本資料流程） (PE) 。 針對杜比數位 Plus，解碼器會解碼為5.1 個通道。 在 Windows 10 上，會在不 downmix 的情況下解碼7.1 通道資料流程。 在舊版作業系統上，如果資料流程是7.1 通道，則只會解碼5.1 通道 downmix。 如果資料流程是具有多個獨立子資料流程的杜比數位加號，則只會解碼獨立的子資料流程0。 此解碼器會略過其他獨立子串流。 此外，此解碼器會略過所有相依的子串流。 此解碼器支援以數位 Rights Management (DRM) 技術保護的資料流程解密和解碼。

如果輸入媒體類型具有 mono、身歷聲或雙 (mono 以外的通道設定，則在沒有 LFE 通道) 的情況下，此解碼器會提供兩個選項供輸出通道設定使用：

-   8聲道輸出 (7.1 通道設定) 
-   6聲道輸出 (5.1 通道設定) 
-   身歷聲 downmix

如果選取了身歷聲 downmix，您可以使用 [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) 屬性，在 MFT 上設定 downmix 的類型。

如果輸出類型為 **MFAudioFormat \_ 杜比 \_ AC3 \_ SPDIF**，則每個輸出緩衝區都包含6144個位元組。 緩衝區以8位元組 S/PDIF 標頭開頭，後面接著壓縮的 AC 3 框架，後面接著零填補至6144個位元組。

如果輸出類型為 **KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號**，則每個輸出緩衝區都包含24576個位元組。 緩衝區是以8位元組 S/PDIF 標頭為開頭，後面接著1–6個壓縮的杜比數位加框架，對應至 1536 PCM 範例，後面接著零填補至24576個位元組。 針對 HDMI 輸出，只會封裝獨立的子串流0。

已向旗標 **mft \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 註冊解碼器 mft，這表示必須由應用程式解除鎖定才能使用的 mft。 如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
