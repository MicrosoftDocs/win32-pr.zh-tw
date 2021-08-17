---
description: InkPicture. SelectionResizing 事件-發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或選取屬性）。
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: 'InkPicture. SelectionResizing 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caeae852802599a401c1cdff97436672e0cbfe252f8f1e96d6f4c98367c828ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966957"
---
# <a name="inkpictureselectionresizing-event"></a>InkPicture. SelectionResizing 事件

發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。

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

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionResizing 識別碼的) \_ 。

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
</dt> <dt>

[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**InkRectangle 類別**](inkrectangle-class.md)
</dt> </dl>

 

 




