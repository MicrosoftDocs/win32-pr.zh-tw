---
description: 發生于使用者按一下 InkPicture 控制項時。
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: 'InkPicture： Click event (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218537"
---
# <a name="inkpictureclick-event"></a>InkPicture。按一下事件

發生于使用者按一下 [InkPicture](inkpicture-control-reference.md) 控制項時。

## <a name="syntax"></a>語法


```C++
void Click();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

按一下控制項除了按一下事件之外，還會產生 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件。

> [!Note]  
> 若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件。

 

如果 **click** 事件中有程式碼，則 [**DblClick**](inkpicture-dblclick.md) 事件永遠不會觸發，因為 **click** 事件是在兩者之間觸發的第一個事件。 如此一來，滑鼠點擊就會被 **click** 事件攔截，因此不會發生 **DblClick** 事件。

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 **DISPID \_ IPEClick** 的識別碼來實作為 IDispatch 介面。

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
</dt> </dl>

 

 




