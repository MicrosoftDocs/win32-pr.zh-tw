---
description: 指定是否將編碼器所列舉的模式 limeted 至符合 MFPKEY \_ 所需 VBRQUALITY 所指定之品質需求的模式 \_ 。
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: 'MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991035"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>MFPKEY \_ 限制 \_ 列舉的 \_ VBRQUALITY 屬性

指定是否將編碼器所列舉的模式 limeted 至符合 [**MFPKEY \_ 所需 \_ VBRQUALITY 所**](mfpkey-desired-vbrqualityproperty.md)指定之品質需求的模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

若要列舉符合特定品質需求的 VBR 模式，請設定下列編碼器屬性。

-   將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 設定為 **VARIANT \_ TRUE**。
-   Set **MFPKEY \_ 將 \_ 列舉的 \_ VBRQUALITY 限制** 為 **VARIANT \_ TRUE**。
-   將 [**MFPKEY \_ 所需的 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 設定為所需的品質。 若為不失真模式，請將所需的品質設定為100。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
