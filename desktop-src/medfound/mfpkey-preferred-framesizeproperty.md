---
description: 指定每個框架慣用的樣本數目。
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: 'MFPKEY_PREFERRED_FRAMESIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000990"
---
# <a name="mfpkey_preferred_framesize-property"></a>MFPKEY \_ 慣用 \_ FRAMESIZE 屬性

指定每個框架慣用的樣本數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="remarks"></a>備註

若要指定慣用的框架大小，請設定下列屬性。

-   將 [**\_ 要求 \_ \_ FRAMESIZE 的 MFPKEY**](mfpkey-requesting-a-framesizeproperty.md) 設定為 **VARIANT \_ TRUE**。
-   將 **MFPKEY \_ 偏好 \_ FRAMESIZE** 設定為每個畫面格所需的樣本數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
