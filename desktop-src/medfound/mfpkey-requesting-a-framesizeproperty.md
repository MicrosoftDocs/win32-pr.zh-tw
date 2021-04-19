---
description: 指定編碼器是否應使用每個畫面格的樣本數所提供的慣用框架大小。
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: 'MFPKEY_REQUESTING_A_FRAMESIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979617"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ 要求 \_ \_ FRAMESIZE 屬性

指定編碼器是否應使用每個畫面格的樣本數所提供的慣用框架大小。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="remarks"></a>備註

若要指定慣用的框架大小，請設定下列屬性。

-   將 **\_ 要求 \_ \_ FRAMESIZE 的 MFPKEY** 設定為 VARIANT \_ TRUE。
-   將 [**MFPKEY \_ 偏好 \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) 設定為每個畫面格所需的樣本數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
