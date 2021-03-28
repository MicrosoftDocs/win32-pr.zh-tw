---
description: 取得使用者帳戶的狀態。
title: DIDiskQuotaUser. AccountStatus 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972001"
---
# <a name="didiskquotauseraccountstatus-property"></a>DIDiskQuotaUser. AccountStatus 屬性

取得使用者帳戶的狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>屬性值

這個屬性可以採用下列其中一個值。



| 狀態            | 值 | 描述                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | 帳戶資訊已解決。    |
| dqAcctUnavailable | 1     | 帳戶資訊無法使用。 |
| dqAcctDeleted     | 2     | 帳戶已刪除。           |
| dqAcctInvalid     | 3     | 帳戶無效。                 |
| dqAcctUnknown     | 4     | 找不到帳戶。            |
| dqAcctUnresolved  | 5     | 帳戶資訊無法解析。  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DIDiskQuotaUser 物件**](didiskquotauser-object.md)
</dt> </dl>

 

 




