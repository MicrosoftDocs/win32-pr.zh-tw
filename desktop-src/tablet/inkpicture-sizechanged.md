---
description: 發生于調整 InkPicture 控制項的大小時，特別是在寬度或高度屬性值變更之後。
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: 'InkPicture. SizeChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945164"
---
# <a name="inkpicturesizechanged-event"></a>InkPicture. SizeChanged 事件

發生于調整 [InkPicture](inkpicture-control-reference.md) 控制項的大小時，特別是在 [**寬度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) 或 [**高度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) 屬性值變更之後。

## <a name="syntax"></a>語法


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*左方* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項左邊的 x 座標。

</dd> <dt>

*頂端* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項頂端的 y 座標。

</dd> <dt>

*Right* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項右邊的 x 座標。

</dd> <dt>

*底部* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項底部的 y 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPESizeChanged 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

