---
description: 以字串格式將登入名稱轉譯為對應的使用者安全識別碼。
title: DiskQuotaControl. TranslateLogonNameToSID 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027059"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>DiskQuotaControl. TranslateLogonNameToSID 方法

以字串格式將登入名稱轉譯為對應的使用者安全識別碼。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*logonname* 
</dt> <dd>

類型： **字串**

指定使用者登入名稱的字串值。

</dd> </dl>

## <a name="return-value"></a>傳回值

以對應至所提供登入名稱的字串格式，傳回 (SID) 的使用者安全識別碼。 傳回的字串包含標準的封閉括弧。 例如：

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>備註

傳回的 SID 字串可以傳遞至 [**FindUser**](diskquotacontrol-finduser.md) 方法，以取代登入名稱。

[**FindUser**](diskquotacontrol-finduser.md) ( *logonname*) 方法的呼叫失敗時，可能是因為表單 (（例如，安全性帳戶管理員 \[ SAM 相容） \] 和使用者主體名稱 \[ UPN \]) 所提供的登入名稱和儲存在 SID 名稱快取中的表單不符。 在這種情況下，登入名稱可以轉換為 SID，並重複呼叫 **FindUser** 。 **FindUser** 會辨識 sid 字串，且會略過 sid 名稱快取查閱。 下列 Microsoft Visual Basic Scripting Edition (VBScript) 程式碼說明這項技巧。


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



相較于 SID 名稱快取中的查閱，名稱對 SID 轉譯可能會是較慢的進程。 因此，建議您先使用登入名稱來呼叫 [**FindUser**](diskquotacontrol-finduser.md) 。 上述範例使用這項技術。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




