---
description: 指定編解碼器在編碼時是否應該使用保守感知優化。
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: 'MFPKEY_PERCEPTUALOPTLEVEL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192248"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>MFPKEY \_ PERCEPTUALOPTLEVEL 屬性

指定編解碼器在編碼時是否應該使用保守感知優化。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

保守感知優化是編解碼器嘗試在影片框架中識別「重要」和「不重要」區域的程式。 在識別出這些框架區域之後，編解碼器會在重要區域品質的同時提供較高的優先順序，而不重要的區域品質。

感知優化強調讓影像看起來是正確的，而不是工作嚴格的數學精確度。

根據所編碼的影片類型而定，優化的結果會有很大的差別。 這項功能非常適合低位速率和低解析度的編碼 (例如，web 串流) ，但在適用于封存影片品質的情況下，最好避免這樣做。

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

 

 




