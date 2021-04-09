---
title: 'D2D1_POINT_2U (D2DBaseTypes) '
description: '表示在二維空間中的 x 座標和 y 座標組。 |D2D1_POINT_2U (D2DBaseTypes) '
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195984"
---
# <a name="d2d1_point_2u"></a>D2D1 \_ 點 \_ 2u

表示在二維空間中的 x 座標和 y 座標組。


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a>備註

Direct2D 中的點會以 [**D2D1 \_ 點 \_ 2f**](d2d1-point-2f.md) 或 **D2D1 \_ 點 \_ 2u** 結構表示。 兩者都在二維空間中包含 x 座標和 y 座標組。 **D2D1 \_ 點 \_ 2f** 結構會將座標儲存為 **FLOAT** 值，而 **D2D1 \_ 點 \_ 2u** 結構會將這些座標儲存為 **UINT32** 值。

**D2D1 \_點 \_ 2u** 是已定義之型別 [**D2D \_ 點 \_ 2u**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)的新名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2DBaseTypes (包含 D2d1) </dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D2D \_ 點 \_ 2u**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[**D2D \_ 點 \_ 2f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





