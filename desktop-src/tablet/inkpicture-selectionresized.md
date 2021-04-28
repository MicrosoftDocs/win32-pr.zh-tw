---
description: InkPicture. SelectionResized 事件-發生于目前選取範圍的大小變更時，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: 'InkPicture. SelectionResized 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086466"
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
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
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

 

