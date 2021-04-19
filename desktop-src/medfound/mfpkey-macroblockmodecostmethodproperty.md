---
description: 指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: 'MFPKEY_MACROBLOCKMODECOSTMETHOD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974633"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>MFPKEY \_ MACROBLOCKMODECOSTMETHOD 屬性

指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可以設定為下列其中一個值。



| 值 | 使用的方法                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | 悲傷/Hadamard。 此選項會將編解碼器設定為僅在計算成本時使用失真。             |
| 1     | RD 成本。 此選項會設定編解碼器，以在計算成本時同時考慮速率和失真。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




