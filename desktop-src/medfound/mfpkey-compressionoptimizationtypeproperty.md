---
description: 指定要用於 Windows Media 視訊 9 Advanced Profile 編碼器的最佳視覺品質設定。
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: 'MFPKEY_COMPRESSIONOPTIMIZATIONTYPE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974228"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE 屬性

指定要用於 Windows Media 視訊 9 Advanced Profile 編碼器的最佳視覺品質設定。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可讓您快速地設定數種影片編碼選項。 它可能會設定為下列其中一個值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>編解碼器不會強制優化，而且會使用其他屬性指定的任何功能。 在許多情況下，編解碼器將會使用內部邏輯來判斷未指定的設定。 這是預設值。</td>
</tr>
<tr class="even">
<td>1</td>
<td>啟用將產生最佳視覺品質的功能。使用此值會設定編解碼器，就如同您已設定下列屬性：<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
如果您在上一個清單中設定任何屬性，您設定的值會覆寫與此設定相關聯的值，但 <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>除外。<br/></td>
</tr>
</tbody>
</table>



 

將 MFPKEY COMPRESSIONOPTIMIZATIONTYPE 屬性的值設定 \_ 為1，也有將 Dquant 選項登錄設定設定為2，以及將「動作向量成本」方法登錄設定為1的效果。 如需詳細資訊，請參閱 [使用 Windows Media 視訊 9 Advanced Profile 編解碼器的 Advanced 設定](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)的 web 文章。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




