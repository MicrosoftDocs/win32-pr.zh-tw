---
description: 取得應用程式暫停作業。
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'ISuspendingEventArgs：： SuspendingOperation 屬性 (Windows. ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848038"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a>ISuspendingEventArgs：： SuspendingOperation 屬性

取得應用程式暫停作業。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a>屬性值

暫止作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 標頭<br/>                   | <dl> <dt>ApplicationModel。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 




