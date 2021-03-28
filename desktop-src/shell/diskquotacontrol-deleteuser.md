---
description: 從磁片區刪除使用者。
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: 'DiskQuotaControl. DeleteUser 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191170"
---
# <a name="diskquotacontroldeleteuser-method"></a>DiskQuotaControl. DeleteUser 方法

從磁片區刪除使用者。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*oUser* 
</dt> <dd>

Type： **Object**

評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果使用者擁有磁片區上的任何儲存空間，這個方法將會失敗。 從磁片區刪除使用者之前，必須先刪除該使用者的所有存放裝置、移至另一個磁片區，或將其擁有權轉移給另一位使用者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Dskquota。h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




