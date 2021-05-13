---
description: 將非預設磁片配額指派給新的使用者。
title: DiskQuotaControl. AddUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841529"
---
# <a name="diskquotacontroladduser-method"></a>DiskQuotaControl. AddUser 方法

將非預設磁片配額指派給新的使用者。

## <a name="syntax"></a>語法


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLogonName* 
</dt> <dd>

類型： **CHAR**

包含使用者登入名稱的字串值。 您可以使用 [**UserNameResolution**](diskquotacontrol-usernameresolution.md) 屬性來指定名稱的解析方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

Type： **Object**

傳回評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。

## <a name="remarks"></a>備註

當使用者第一次寫入磁片區時，NTFS 檔案系統會自動建立使用者配額專案。 以這種方式建立的專案，會獲指派預設的警告臨界值和磁片區的固定配額限制值。 此方法可讓您在使用者將資訊寫入磁片區之前，建立使用者配額專案。 它會傳回 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件，這個物件可用來指派與磁片區的預設設定不同的警告臨界值或配額限制值。

如果使用者已經存在，則不會建立新專案。 方法會傳回與現有專案相關聯的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




