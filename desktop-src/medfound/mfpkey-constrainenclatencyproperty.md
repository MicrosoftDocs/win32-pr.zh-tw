---
description: 指定編碼器是否受限於最大延遲需求。
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: 'MFPKEY_CONSTRAINENCLATENCY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113418"
---
# <a name="mfpkey_constrainenclatency-property"></a>MFPKEY \_ CONSTRAINENCLATENCY 屬性

指定編碼器是否受限於最大延遲需求。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

如果您將此屬性保留為 **變數 \_ FALSE** 的預設值，則編碼器會列舉一組預設的模式，其具有大約2000毫秒的編碼器延遲。 如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) 屬性來指定最大編碼器延遲。 在此情況下，編碼器會建立符合延遲需求的模式，並只列舉這些模式。 編碼器在一段時間內收到等於 **MFPKEY \_ MAXENCLATENCYMS** 的輸入時，就會保證輸出範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
