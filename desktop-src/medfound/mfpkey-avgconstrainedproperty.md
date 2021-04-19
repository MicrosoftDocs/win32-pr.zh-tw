---
description: 指定編碼器是否使用平均可控的 VBR 編碼。
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: 'MFPKEY_AVGCONSTRAINED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970802"
---
# <a name="mfpkey_avgconstrained-property"></a>MFPKEY \_ AVGCONSTRAINED 屬性

指定編碼器是否使用平均可控的 VBR 編碼。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

如果此屬性和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。 在此情況下，編碼器會根據 [**MFPKEY \_ DYN \_ Vbr \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) 和 [**MFPKEY \_ DYN \_ vbr \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md)的值來設定本身。

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

 

 
