---
description: InkPicture 控制項已完成重繪本身時發生。
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: 'InkPicture 繪製事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987001"
---
# <a name="inkpicturepainted-event"></a>InkPicture 繪製事件

[InkPicture](inkpicture-control-reference.md)控制項已完成重繪本身時發生。

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

此事件方法是在識別碼為 DISPID IOEPainted 的 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分配介面中定義 \_ 。

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

 

 




