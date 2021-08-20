---
description: InkPicture 控制項調整大小時， (寬度和/或高度屬性值變更) 時發生。
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: 'InkPicture： Resize 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1cf2e84efc3f1d4123c31abee0218e6fc23b515a4c3bd82c570152f2a85d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042070"
---
# <a name="inkpictureresize-event"></a>InkPicture。調整大小事件

[InkPicture](inkpicture-control-reference.md)控制項調整大小時， (寬度和/或高度屬性值變更) 時發生。

## <a name="syntax"></a>語法


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*離開* 
</dt> <dd>

從視窗左邊的圖元數，其中包含控制項左邊的控制項。

</dd> <dt>

*前幾個* 
</dt> <dd>

從視窗頂端的圖元數，包含控制項頂端的控制項。

</dd> <dt>

*對* 
</dt> <dd>

從視窗左邊的圖元數，其中包含控制項右邊的控制項。

</dd> <dt>

*下層* 
</dt> <dd>

從視窗頂端的圖元數，包含控制項底部的控制項。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

控制項的新寬度（以圖元為單位）會等於 *右邊* 和 *左方* 參數之間的差異。 同樣地，新的高度將等於 *底端* 和 *頂端* 之間的差異。

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 **DISPID \_ IPEResize** 的識別碼來實作為 IDispatch 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




