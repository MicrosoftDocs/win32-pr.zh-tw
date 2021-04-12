---
description: 發生于 InkPicture 控制項自行重繪之前。
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: 'InkPicture：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193332"
---
# <a name="inkpicturepainting-event"></a>InkPicture。繪製事件

發生于 [InkPicture](inkpicture-control-reference.md) 控制項自行重繪之前。

## <a name="syntax"></a>語法


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDC* \[在\]
</dt> <dd>

將在其上進行繪製的裝置內容。

</dd> <dt>

*Rect* \[在\]
</dt> <dd>

要重新繪製的筆墨矩形。

</dd> <dt>

*允許* \[in、out\]
</dt> <dd>

是否會發生重新繪製。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEPainting 識別碼的) \_ 。

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

 

 




