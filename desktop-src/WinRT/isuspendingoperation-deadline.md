---
description: 取得延遲的應用程式暫停作業繼續之前剩餘的時間。
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: 'ISuspendingOperation：:D eadline 屬性 (ApplicationModel .h) '
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
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943431"
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
| 標頭<br/>                   | <dl> <dt>ApplicationModel。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




