---
description: 發生于 InkOverlay 物件或 InkPicture 完成重繪本身之前。
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: 'InkOverlay：繪製事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513929"
---
# <a name="inkoverlaypainting-event"></a>InkOverlay. 繪製事件

發生于 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 完成重繪本身之前。

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

要重新繪製的矩形。

</dd> <dt>

*允許* \[in、out\]
</dt> <dd>

是否會發生重新繪製。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEPainting 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> </dl>

 

 




