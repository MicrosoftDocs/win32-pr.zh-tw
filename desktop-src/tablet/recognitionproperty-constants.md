---
description: 定義值，這些值會指定辨識替代項的屬性。  (API) 的 Tablet PC 應用程式開發介面，會使用全域唯一識別碼 (Guid) 來識別封包屬性（在自動化中是常數位符串）。
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: 'RecognitionProperty 常數 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd18aeae50e0ae08337dd89a494292a7accbb389e6d02f0b990035fbf9644879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856419"
---
# <a name="recognitionproperty-constants"></a>RecognitionProperty 常數

定義值，這些值會指定辨識替代項的屬性。  (API) 的 Tablet PC 應用程式開發介面，會使用全域唯一識別碼 (Guid) 來識別封包屬性（在自動化中是常數位符串）。

下表列出可用的辨識替代屬性全域唯一識別碼 (GUID) 欄位。 藉由呼叫 [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue)方法，使用這些 guid 來存取 [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)物件的屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數名稱</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件行號屬性的 GUID。 <br/> LineNumber 指定具有特定行號的替代項。<br/>
<blockquote>
[!Note]<br />
東亞字元的辨識器不支援此欄位。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之分割屬性的 GUID。 <br/> 分割會指定辨識器用來產生辨識結果的基本筆墨片段或單位。<br/>
<blockquote>
[!Note]<br />
未實作。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之辨識作用點屬性的 GUID。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">GUID，識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之辨識結果的最大筆觸計數的屬性。 <br/>
<blockquote>
[!Note]<br />
未實作。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">GUID，可識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之每英寸點的屬性。 <br/>
<blockquote>
[!Note]<br />
未實作。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">GUID，可識別辨識器在辨識結果中的信賴層級的屬性。<br/>
<blockquote>
[!Note]<br />
信賴評估僅適用于美國英文以及 Microsoft Windows XP Tablet PC Edition 和 Windows Vista 中的所有手勢辨識器。 為任何其他辨識器提供信賴屬性的方法會傳回 E_NOTIMPL。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之線條度量屬性的 GUID，這是用來取得度量的行。 <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

在 c + + 中，您可以在 Msinkaut .h 標頭檔中存取這些常數， <systemdrive> \\ \\ \\ \\ \\ 如果您將 SDK 安裝在預設位置，則該檔案位於： Program Files Microsoft sdk Windows 6.0 版包含目錄。

> [!Note]  
> 在 c + + 中，這些常數是 WCHARs，而不是 Bstr。 使用之前，請先將它們轉換成 Bstr。 如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AlternatesWithConstantPropertyValues 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**ConfidenceAlternates 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**LineAlternates 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**IInkRecognitionAlternates 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




