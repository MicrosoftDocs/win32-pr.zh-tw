---
description: 指定編碼器是否受限於最大延遲需求。
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: 'MFPKEY_CONSTRAINENCLATENCY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981527"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
