---
description: 以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: 'MFPKEY_DYN_VBR_BAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996686"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>MFPKEY \_ DYN \_ VBR \_ BAVG 屬性

以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ I4**

## <a name="remarks"></a>備註

如果 [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) 和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。 在此情況下，編碼器會根據此屬性的值和 [**MFPKEY \_ DYN \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) 屬性來設定本身。

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

 

 
