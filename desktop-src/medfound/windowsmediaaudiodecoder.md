---
description: Windows Media 音訊解碼器會將 Windows Media 音訊編碼器編碼的音訊串流解碼。
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: 'Windows Media 音訊 (Wmcodecdsp 的解碼器) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984296"
---
# <a name="windows-media-audio-decoder"></a>Windows Media 音訊的解碼器

Windows Media 音訊解碼器會將 [**Windows Media 音訊編碼器**](windowsmediaaudioencoder.md)編碼的音訊串流解碼。 編碼器和解碼器支援三種編碼音訊類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。

## <a name="class-identifier"></a>類別識別碼

Windows Media 音訊解碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMADecMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立音訊解碼器的實例。

## <a name="input-formats"></a>輸入格式

下表顯示的音訊格式標記代表 Windows Media 音訊的解碼器所支援的輸入分類。 如需有關如何設定此解碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊解碼](configuringaudiodecoding.md)。



| 格式化標記常數             | 格式化標記值 | 音訊格式                     |
|---------------------------------|------------------|----------------------------------|
| WAVE \_ 格式 \_ WMAUDIO2          | 0x0161           | Windows Media 音訊標準     |
| WAVE \_ 格式 \_ WMAUDIO3          | 0x0162           | Windows Media 音訊專業人員 |
| WAVE \_ 格式 \_ WMAUDIO \_ 無損 | 0x0163           | Windows Media 音訊無損     |



 

## <a name="output-formats"></a>輸出格式

下表顯示的音訊格式標記代表 **Windows Media 音訊的解碼器** 所支援的輸出類型。 如需有關如何設定編碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊編碼](configuringaudioencoding.md)。



| 格式化標記常數       | 格式化標記值 | 音訊格式                                          |
|---------------------------|------------------|-------------------------------------------------------|
| WAVE \_ 格式 \_ PCM         | 0x0001           | PCM 格式                                            |
| WAVE \_ 格式 \_ IEEE \_ FLOAT | 0x0003           | IEEE 浮點數                                   |
| WAVE \_ 格式 \_ 可擴充  | 0xFFFE           | **WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式 |



 

## <a name="interfaces"></a>介面

音訊解碼物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。

Windows Media 音訊的解碼器會根據您所取得的介面和執行的 Windows 版本，以一或 MFT 的形式運作。 下表顯示音訊解碼器以 SQL-DMO 或 MFT 的行為條件。



| 作業系統 | 解碼器行為                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Windows Media 音訊的解碼器一律會以 SQL-DMO 的方式運作。                                                                                                                                |
| Windows Vista    | Windows Media 音訊的解碼器預設會以一種方式運作。 如果您在音訊解碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。 |
| Windows 7        | Windows Media 音訊的解碼器預設會以一種方式運作。 如果您在音訊解碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。                                    |



 

## <a name="properties"></a>屬性

Windows Media 音訊的解碼器支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>指定在解碼檔案結尾可能會傳回的額外 PCM 樣本數上限。<br/> <dl> Windows Vista （含）以後版本。<br />
Standard、Professional、無損。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>指定音訊解碼器將使用的動態範圍控制模式。<br/> <dl> Windows XP （含）以後版本。<br />
Standard、Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。 <br/> <dl> Windows XP （含）以後版本。<br />
Professional<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>指定音訊解碼器是否應提供高解析度的輸出。<br/> <dl> Windows XP （含）以後版本。<br />
Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>指定音訊解碼器是否應該執行 Lt-Rt 折迭。<br/> <dl> Windows Vista （含）以後版本。<br />
Professional。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>指定用戶端電腦上的說話者設定。<br/> <dl> Windows XP （含）以後版本。<br />
Professional。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>指定音訊內容的平均音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>指定輸出音訊內容所需的平均音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>指定音訊內容中發生的最高音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Professional、無損。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>指定輸出音訊內容所需的最大音量層級。<br/> <dl> Windows XP （含）以後版本。<br />
Professional、無損。<br />
唯寫。<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> </dl>

 

 




