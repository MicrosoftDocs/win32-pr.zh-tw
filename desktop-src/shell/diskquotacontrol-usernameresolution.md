---
description: 設定或取得值，這個值會控制如何將使用者安全識別碼 (SID) 解析為使用者名稱。
title: DiskQuotaControl. UserNameResolution 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972125"
---
# <a name="diskquotacontrolusernameresolution-property"></a>DiskQuotaControl. UserNameResolution 屬性

設定或取得值，這個值會控制如何將使用者安全識別碼 (SID) 解析為使用者名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>屬性值

這個屬性可以設定為下列其中一個值。



| 解決類型 | 值 | 描述                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | 請勿解析使用者名稱資訊。                                                                                                                    |
| dqResolveSync   | 1     | 請稍候，正在解析名稱資訊。                                                                                                                   |
| dqResolveAsync  | 2     | 請勿在解析名稱資訊時等候。 解析名稱時，會引發 [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) 事件。 |



 

## <a name="remarks"></a>備註

這個屬性會影響 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的列舉，以及 [**AddUser**](diskquotacontrol-adduser.md) 和 [**FindUser**](diskquotacontrol-finduser.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




