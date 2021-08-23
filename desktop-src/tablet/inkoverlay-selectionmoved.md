---
description: SelectionMoved 事件-發生于目前選取範圍的位置已變更時，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: 'SelectionMoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e1c9501a9670ebfa89cdcf30fac7a1044450cef932e7c7abb522a5199fd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032066"
---
# <a name="inkoverlayselectionmoved-event"></a>SelectionMoved 事件

發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。

## <a name="syntax"></a>語法


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldSelectionRect* \[在\]
</dt> <dd>

所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionMoved** 事件之前就已存在。

> [!Note]  
> 這個矩形是以筆墨空間座標指定，可允許復原案例。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 僅分派介面中定義， (具有 DISPID IOESelectionMoved 識別碼的) \_ 。

若要取得已移動之筆劃集合的新周框，請呼叫 [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) 方法。

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

 

