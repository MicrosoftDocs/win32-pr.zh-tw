---
description: SelectionResizing 事件-發生于目前的選取範圍即將變更時（例如，透過對使用者介面的改變、剪下和貼上程式或選取屬性）。
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: 'SelectionResizing 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260ac01f303b7f6ced5f38c77bc2d490d1e99aa53382ebe7d2daf52f986ccf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712678"
---
# <a name="inkoverlayselectionresizing-event"></a>SelectionResizing 事件

發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。

## <a name="syntax"></a>語法


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CurSelectionRect* \[在\]
</dt> <dd>

**SelectionResizing** 事件之後選取範圍的周框。

> [!Note]  
> 這個矩形是在用戶端視窗座標中指定，可讓您在調整大小時維持外觀比例。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionResizing 識別碼的) \_ 。

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
</dt> <dt>

[**Selection 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle 類別**](inkrectangle-class.md)
</dt> </dl>

 

 




