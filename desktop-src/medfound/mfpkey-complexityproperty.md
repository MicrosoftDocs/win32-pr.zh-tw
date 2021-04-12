---
description: 指定編碼器演算法的複雜度。
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: 'MFPKEY_COMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192271"
---
# <a name="mfpkey_complexity-property"></a>MFPKEY \_ 複雜性屬性

\[[**MFPKEY \_**](mfpkey-complexityexproperty.md)您可以在 [需求] 區段中指定的作業系統使用複雜性。 它在後續版本中可能會變更或無法使用。 相反地，請使用 **MFPKEY \_ COMPLEXITYEX**。\]

指定編碼器演算法的複雜度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

預設值取決於影片編碼器的版本，如下表所示。



| 編碼器版本                 | 預設值 |
|---------------------------------|---------------|
| Windows Media 視訊9編碼器   | 3             |
| Windows Media 視訊7/8 編碼器 | 1             |



 

## <a name="remarks"></a>備註

這個整數值的範圍是從0到3。 較低的值會使編解碼器使用較不復雜的編碼演算法。 雖然更簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。

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

 

 




