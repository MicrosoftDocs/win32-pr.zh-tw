---
description: InkPicture. SelectionResized 事件-發生于目前選取範圍的大小變更時，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: 'InkPicture. SelectionResized 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e67bc19d4d35c356e0774f0843ba62432606c1ee4f1f84095e64c4808d09bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451049"
---
# <a name="inkpictureselectionresized-event"></a>InkPicture. SelectionResized 事件

發生于目前選取範圍的大小變更時，例如透過對使用者介面的變異、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。

## <a name="syntax"></a>語法


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldSelectionRect* \[在\]
</dt> <dd>

所選 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的周框，在引發 **SelectionResized** 事件之前就已存在。

> [!Note]  
> 這個矩形是以筆墨空間座標指定，可允許復原案例。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionResized 識別碼的) \_ 。

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

 

