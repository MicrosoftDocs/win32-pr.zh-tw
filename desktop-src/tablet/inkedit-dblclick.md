---
description: 發生于按兩下 InkEdit 控制項時。
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: InkEdit (筆跡) 的 DblClick 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975482"
---
# <a name="inkeditdblclick-event"></a>InkEdit： DblClick 事件

發生于按兩下 [InkEdit](inkedit-control-reference.md) 控制項時。

## <a name="syntax"></a>語法


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*取消* \[in、out\]
</dt> <dd>

**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。 如果 [**Click**](inkedit-click.md) 事件中有程式碼，則不會觸發 **DblClick** 事件。

 

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 **DISPID \_ IeeDblClick** 的識別碼來實作為 IDispatch 介面。

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

 

 




