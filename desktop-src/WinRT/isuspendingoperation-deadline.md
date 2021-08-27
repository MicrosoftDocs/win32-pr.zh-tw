---
description: 取得延遲的應用程式暫停作業繼續之前剩餘的時間。
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: 'ISuspendingOperation：:D eadline 屬性 (Windows。ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 448f4d89ec2f1b7e3f68255897b32b3f4cba2ec753ae8f6cc7751c9041b01266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121498"
---
# <a name="isuspendingoperationdeadline-property"></a>ISuspendingOperation：:D eadline 屬性

取得延遲的應用程式暫停作業繼續之前剩餘的時間。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>屬性值

延遲的應用程式暫停操作之前的剩餘時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 標頭<br/>                   | <dl> <dt>Windows。ApplicationModel。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows。ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




