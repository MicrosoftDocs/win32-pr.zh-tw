---
description: InkEdit 控制項的內容變更時發生。
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: InkEdit (筆跡) 變更事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994468"
---
# <a name="inkeditchange-event"></a>InkEdit。變更事件

[InkEdit](inkedit-control-reference.md)控制項的內容變更時發生。

## <a name="syntax"></a>語法


```C++
void Change();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

每當影響 [InkEdit](inkedit-control-reference.md) 控制項內容的任何屬性變更時，就會發生此事件。

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 **DISPID \_ IeeChange** 的識別碼來實作為 IDispatch 介面。

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

 

 




