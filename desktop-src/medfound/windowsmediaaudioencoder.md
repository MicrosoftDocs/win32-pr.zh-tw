---
description: Windows Media 音訊編碼器會編碼音訊串流。 編碼器支援三種編碼輸出類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: 'Windows Media 音訊編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976207"
---
# <a name="windows-media-audio-encoder"></a>Windows Media 音訊編碼器

Windows Media 音訊編碼器會編碼音訊串流。 編碼器支援三種編碼輸出類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。

## <a name="class-identifier"></a>類別識別碼

Windows Media 音訊編碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMAEncMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立音訊編碼器的實例。

## <a name="input-formats"></a>輸入格式

下表顯示的音訊格式標記代表 Windows Media 音訊編碼器所支援的輸入分類。 如需有關如何設定編碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊編碼](configuringaudioencoding.md)。



| 格式化標記常數       | 格式化標記值 | 音訊格式                                          |
|---------------------------|------------------|-------------------------------------------------------|
| WAVE \_ 格式 \_ PCM         | 0x0001           | PCM 格式                                            |
| WAVE \_ 格式 \_ IEEE \_ FLOAT | 0x0003           | IEEE 浮點數                                   |
| WAVE \_ 格式 \_ 可擴充  | 0xFFFE           | **WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式 |



 

## <a name="output-formats"></a>輸出格式

下表顯示的音訊格式標記，代表 Windows Media 音訊編碼器支援的輸出分類。



| 格式化標記常數             | 格式化標記值 | 音訊格式                     |
|---------------------------------|------------------|----------------------------------|
| WAVE \_ 格式 \_ WMAUDIO2          | 0x0161           | Windows Media 音訊標準     |
| WAVE \_ 格式 \_ WMAUDIO3          | 0x0162           | Windows Media 音訊專業人員 |
| WAVE \_ 格式 \_ WMAUDIO \_ 無損 | 0x0163           | Windows Media 音訊無損     |



 

## <a name="interfaces"></a>介面

音訊 endoder 物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以做為 (MFT) 媒體基礎轉換。

Windows Media 音訊編碼器的運作方式，視您取得的介面和執行的 Windows 版本而定。 下表顯示音訊編碼器以 SQL-DMO 或 MFT 行為的條件。



| 作業系統 | 編碼器行為                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Windows Media 音訊編碼器一律會以一種方式運作。                                                                                                                                |
| Windows Vista    | Windows Media 音訊編碼器預設會以一種方式運作。 如果您在音訊編碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。 |
| Windows 7        | Windows Media 音訊編碼器預設會以一種方式運作。 如果您在音訊編碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。                                    |



 

## <a name="encoder-properties"></a>編碼器屬性

Windows Media 音訊編碼器支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>指定編碼器是否使用平均可控的 VBR 編碼。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>以毫秒為單位，指定限制可變位速率的緩衝區視窗（以毫秒為單位）， (VBR) 資料流程的尖峰位元速率。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。 <br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>指定編碼器是否受限於最大的解碼器延遲需求。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>指定是否限制編碼演算法的複雜度。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>指定編碼器是否受限於最大延遲需求。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>指定由編碼器列舉的模式是否限制為符合品質需求的模式。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>指定編碼內容的複雜性設定檔。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>指定 VBR 編碼所需的品質等級。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>指定編碼器是否使用雜訊替代。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>指定編碼器是否使用 PCM 範圍限制。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>指定編碼器中的帶狀截斷所允許的最大編碼頻寬。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>指定編碼器中的頻外截斷所允許的最低編碼頻寬。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>指定允許最小編碼頻寬的品質。 <br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>指定允許最大編碼頻寬的品質。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>指定編碼器是否執行帶狀截斷。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>指定編碼器是否使用 Windows Media 音訊編碼器第7版所執行之遮罩計算的樣式。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>指定編碼器是否執行身歷聲影像處理。 <br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>指定編碼演算法的複雜度。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>指定編碼傳遞的結尾。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>指定核心編碼器是否使用 &quot; Plus &quot; 功能。<br/> <dl> Windows Vista （含）以後版本。<br />
Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>指定最大的解碼器延遲（以毫秒為單位）。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>指定編碼器的最大延遲（以毫秒為單位）。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>指定最新列舉輸出類型的 VBR 品質層級。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>指定編碼器所支援的最大傳遞數目。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>指定編碼器將用來編碼內容的傳遞數。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>指定編碼器是否受尖峰位速率的限制。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>指定每個框架慣用的樣本數目。<br/> <dl> Windows Vista （含）以後版本。<br />
Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>指定編碼器是否應使用慣用的框架大小。<br/> <dl> Windows Vista （含）以後版本。<br />
Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 編碼。 <br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>指定編碼資料流程的平均緩衝區視窗（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>指定編碼資料流程的最大緩衝區視窗（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>指定編碼資料流程的平均位元速率（以每秒位數為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>指定編碼資料流程的最大位元速率（以每秒位數為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>指定編碼器是否使用 VBR 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Windows Media 音訊編解碼器目前未使用此屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>指定音訊內容的平均音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>指定音訊內容中發生的最高音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>指定 VBR 編碼音訊的每秒平均位元組數。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>指定編碼器是否應該為每個畫面產生1個 WMA 封包。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>指定編碼器是否應產生動態範圍控制參數。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>指定描述輸入音訊內容的 <strong>WAVEFORMATEX</strong> 結構。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>指定編碼器是否應啟用即時 S/PDIF 編碼。<br/> <dl> Windows Vista （含）以後版本。<br />
Professional。<br />
讀取/寫入<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> </dl>

 

 




