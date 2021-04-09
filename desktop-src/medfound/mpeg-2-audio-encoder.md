---
description: Microsoft 媒體基礎的 MPEG-2 音訊編碼器是媒體基礎轉換，可將 mono 或身歷聲音訊編碼為 MPEG-2 音訊 (ISO/IEC 11172-3) 或 MPEG-2 音訊 (ISO/IEC 13818-3) 。
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: MPEG-2 音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848443"
---
# <a name="mpeg-2-audio-encoder"></a>MPEG-2 音訊編碼器

Microsoft 媒體基礎的 MPEG-2 音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，可將 mono 或身歷聲音訊編碼為 mpeg-2 音訊 (ISO/iec 11172-3) 或 mpeg-2 音訊 (ISO/iec 13818-3) 。

編碼器支援第1層和第2層音訊。 它不支援 MPEG-Layer 3 (MP3) 音訊。 針對 MPEG-2，編碼器支援 (LSF) 部分的 MPEG-2 音訊的低取樣頻率。 它不支援多重通道擴充。 MFT 會輸出 MPEG 基本資料流程。 它無法產生 packetized 的基本資料流程、程式資料流程或傳輸串流。

## <a name="class-identifier"></a>類別識別碼

MEPG-2 音訊編碼器 (CLSID) 的類別識別碼為 **clsid \_ CMPEG2AudioEncoderMFT**，定義于標頭檔 wmcodecdsp 中。

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
<td>必要。 必須是 <strong>MFAudioFormat_MPEG</strong>。 這個子類型可用於 MPEG-2 和 MPEG-2 音訊。</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>每秒樣本數。</td>
<td>必要。 MPEG-2 和 MPEG-2 都支援下列值：
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
此外，MPEG-2 LSF 支援下列值： <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24000</li>
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
<td>編碼 MPEG 資料流程的位元速率（以每秒位元組數為單位）。</td>
<td>選擇性。<br/> ISO/IEC 11172-3 和 ISO/IEC 13818-3 (LSF) 規格會根據取樣率、通道數目和音訊層 (1 或 2) ，定義數位費率。 <br/> 編碼器預設為第2層音訊。 如果未設定 <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> 屬性，則編碼器會使用下列預設的位元速率：<br/>
<ul>
<li>MPEG-1 身歷聲：每秒224000位 (bps) = 每秒28000位元組。</li>
<li>MPEG-2 mono： 192000 bps = 每秒24000位元組。</li>
<li>MPEG-2 LSF、mono 或身歷聲： 160000 bps = 每秒20000位元組。</li>
</ul>
這個屬性可以設定為其他值。 如果根據 MPEG 規格，此值無效，則 MFT 會拒絕媒體類型。<br/> 您也可以使用 <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> 介面來設定位元速率。 如需詳細資訊，請參閱「備註」。<br/></td>
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



 

編碼器不支援取樣率轉換或身歷聲/mono 轉換。 如果未設定選用的屬性，編碼器會在設定類型之後，將它們新增至媒體類型。

## <a name="codec-properties"></a>編解碼器屬性

編碼器透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面支援下列屬性。



| 屬性                                                                                | 描述                                                                                      | 預設值                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | 指定平均編碼的位元速率（以位/秒為單位）。                                      | 如輸出媒體類型中適用于 [MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性所述。                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | 指定 MPEG 音訊編碼模式。                                                          | 雙聲道音訊的身歷聲，或1聲道音訊的單一通道。<br/> 針對雙聲道音訊，編碼器也支援雙重通道和聯合身歷聲。<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | 指定是否要在 MPEG 音訊串流中設定著作權位。                             | 沒有著作權。                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | 指定當編碼的資料流程解碼時，應使用的反強調篩選類型。 | 未指定任何強調。                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | 指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。                    | CRC 總和檢查碼會寫入位資料流程。                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | 指定 MPEG 音訊層。                                                                  | 第2層音訊。                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | 指定是否要針對 MPEG 音訊資料流程中的原始位進行設定。                          | 「原始」位為 off。                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | 指定是否要針對 MPEG 音訊資料流程中的私用使用者位進行設定。                      | 私用使用者位為 off。                                                                                                                                               |



 

若要取得 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面的指標，請呼叫 MFT 上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

MFT 會執行下列 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法：

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

所有其他 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法都會傳回 **E \_ >notimpl**。

## <a name="remarks"></a>備註

每個 MPEG 音訊框架都包含 384 (第1層) 或 1152 (第2層) 每個頻道的音訊範例。 不過，編碼器的每個輸入緩衝區可能包含任意數目的 PCM 樣本。 每個輸入緩衝區的大小必須是區塊對齊的倍數。 編碼器會快取輸入範例，直到它對 MPEG 音訊框架足夠。

每個輸出緩衝區都包含一個原始 MPEG 框架。 每個輸出緩衝區的大小取決於位元速率和取樣率。

### <a name="configuring-the-encoder"></a>設定編碼器

若要變更編碼器上的任何預設設定，請執行下列步驟：

1.  建立編碼器 MFT 的實例。
2.  呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以取得慣用的輸出類型清單。 編碼器會列舉 mono 和身歷聲的所有採樣速率。 根據取樣率和通道數目，選取其中一種媒體類型。 [ [MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性工作表示預設的位元速率（以位元組為單位）。
3.  選擇性：您可以針對輸出媒體類型上的 [MF \_ MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_ ](mf-mt-audio-avg-bytes-per-second-attribute.md) 設定新的值，以覆寫預設的位元速率。 有效的位元速率取決於取樣率、通道數目和音訊層。
    > [!Note]  
    > 在設定程式的這個階段中，編碼器會預設為第2層音訊，而且只會接受第2層的位元速率。 您將能夠在稍後的步驟中，將編碼器切換至第1層 (請參閱步驟 7) 。 在這種情況下，請立即保留預設的位元速率;您可以在步驟8中再次加以變更。

     

4.  呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定輸出媒體類型。 如果您為 [ \_ \_ \_ \_ \_ 每 \_ 秒的 MF MT 音訊平均位元組](mf-mt-audio-avg-bytes-per-second-attribute.md) 設定您自己的值，而 MFT 拒絕輸出媒體類型，可能是因為您指定了不正確位元速率。
5.  呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 來列舉輸入媒體類型。 由於取樣率和通道數目必須與輸出類型相同，因此只會列舉兩個選項：32位浮點 PCM 輸入和16位整數 PCM 輸入。 選取其中一個。
6.  呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定輸入媒體類型。
7.  選擇性：若要編碼第1層音訊，請將 [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) 屬性設定為 **eAVEncMPALayer \_ 1**。
8.  選擇性：若要變更位元速率，請設定 [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) 屬性。 位元速率必須是 MPEG-2 或 MPEG-2 LSF 規格中所列的其中一個有效位速度。 或者，您也可以呼叫 [**ICodecAPI：： GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) ，以根據目前的設定取得有效位速率的清單。
9.  選擇性：使用2聲道音訊，您可以設定 [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) 屬性，將編碼模式變更為雙聲道或結合身歷聲。 您可以呼叫 [**ICodecAPI：： GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) 來取得有效的選項。  (1 聲道音訊，唯一的選項是 mono。 ) 
10. 選擇性：設定先前所列的其他任何 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 屬性。

請務必遵循這些步驟的順序。 尤其是在變更任何 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 屬性之前，請先設定輸出媒體類型。 此外，您必須先設定 **ICodecAPI** 屬性，然後再接收第一個輸入範例。 在 MFT 收到輸入之後，編解碼器屬性會是唯讀的，而 [**ICodecAPI：： SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 會傳回值 **\_ FALSE**。

### <a name="supported-bit-rates"></a>支援的位元速率

編碼器支援下列位元速率。



MPEG-1

MPEG-2

第1層

第2層

第1層

第2層

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* 僅限 Mono  
\*\* 僅限身歷聲  
</dl>

### <a name="example-media-types"></a>範例媒體類型

以下是將16位整數 PCM 編碼的媒體類型範例，以預設位元速率編碼的 48-kHz 身歷聲音訊。

輸出媒體類型：

| 屬性                                                                           | 值                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ 音訊**  |
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [MF \_ MT \_ 音訊 \_ 數目 \_ 通道](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

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
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
