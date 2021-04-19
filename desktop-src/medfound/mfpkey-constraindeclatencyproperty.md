---
description: 指定編碼器是否受限於最大的解碼器延遲需求。
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: 'MFPKEY_CONSTRAINDECLATENCY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969319"
---
# <a name="mfpkey_constraindeclatency-property"></a>MFPKEY \_ CONSTRAINDECLATENCY 屬性

指定編碼器是否受限於最大的解碼器延遲需求。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

如果您將此屬性保留為預設值 [ **VARIANT \_ FALSE**]，則編碼器會列舉一組預設的模式，其中大約有1500毫秒的解碼器延遲。 如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) 屬性來指定最大的解碼器延遲。 在此情況下，編碼器會建立符合延遲需求的模式，並只列舉這些模式。 編碼器可確保預先 (的) 解碼器緩衝區大小的需求小於或等於 **MFPKEY \_ MAXDECLATENCYMS**。

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

 

 
