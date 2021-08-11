---
description: 針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: 'MFPKEY_DYN_VBR_RAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242610"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>MFPKEY \_ DYN \_ VBR \_ RAVG 屬性

針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ I4**

## <a name="remarks"></a>備註

如果 [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) 和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。 在此情況下，編碼器會根據此屬性的值和 [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) 屬性來設定本身。

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

 

 
