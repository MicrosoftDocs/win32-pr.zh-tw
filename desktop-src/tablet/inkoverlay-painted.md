---
description: 當 InkOverlay 物件或 InkPicture 控制項已完成重繪本身時發生。
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: 'InkOverlay：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f433f18d5e94be1163be519f4ee33fbe0b8d08a2e33feadd363a8eb3a43a6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218932"
---
# <a name="inkoverlaypainted-event"></a>InkOverlay. 繪製事件

當 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 控制項已完成重繪本身時發生。

## <a name="syntax"></a>語法


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDC* \[在\]
</dt> <dd>

發生事件的裝置內容。

</dd> <dt>

*Rect* \[在\]
</dt> <dd>

重新繪製的 [**InkRectangle**](inkrectangle-class.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEPainted 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> </dl>

 

 




