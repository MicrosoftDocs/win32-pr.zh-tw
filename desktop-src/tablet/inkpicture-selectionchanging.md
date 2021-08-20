---
description: 發生于 InkPicture 控制項內的筆墨選取即將變更時（例如，透過變更使用者介面、剪下和貼上程式或選取屬性）。
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: 'InkPicture. SelectionChanging 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5960fd212b4362f697c1c83b1bc03729cb9d619081ee6c4895a01a7d7124dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042060"
---
# <a name="inkpictureselectionchanging-event"></a>InkPicture. SelectionChanging 事件

發生于 [InkPicture](inkpicture-control-reference.md) 控制項內的筆墨選取即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。

## <a name="syntax"></a>語法


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewSelection* \[在\]
</dt> <dd>

要選取的新 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionChanging 識別碼的) \_ 。

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
</dt> </dl>

 

