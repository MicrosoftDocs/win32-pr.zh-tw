---
description: 發生于使用者按一下 InkEdit 控制項時。
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: 'InkEdit： Click event (筆跡) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997568"
---
# <a name="inkeditclick-event"></a>InkEdit。按一下事件

發生于使用者按一下 [InkEdit](inkedit-control-reference.md) 控制項時。

## <a name="syntax"></a>語法


```C++
void Click();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

按一下控制項除了按一下事件之外，還會產生 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。

> [!Note]  
> 若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。

 

如果 **click** 事件中有程式碼，則 [**DblClick**](inkedit-dblclick.md) 事件永遠不會觸發，因為 **click** 事件是在兩者之間觸發的第一個事件。 如此一來，滑鼠點擊就會被 **click** 事件攔截，因此不會發生 **DblClick** 事件。

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 **DISPID \_ IeeClick** 的識別碼來實作為 IDispatch 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>筆跡 (也需要筆跡 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




