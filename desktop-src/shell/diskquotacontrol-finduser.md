---
description: 在磁片區的配額檔案中，依名稱尋找使用者的專案。
title: DiskQuotaControl. FindUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971965"
---
# <a name="diskquotacontrolfinduser-method"></a>DiskQuotaControl. FindUser 方法

在磁片區的配額檔案中，依名稱尋找使用者的專案。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLogonName* 
</dt> <dd>

類型： **字串**

包含使用者登入名稱的字串值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。

## <a name="remarks"></a>備註

即使配額檔案中沒有使用者的專案，這個方法也會傳回 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。 傳回的使用者物件具有警告臨界值，且會將固定配額限制設定為磁片區的預設值。

從 [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) 傳回的字串可以用來取代 *sLogonName* 參數。 當 **FindUser** 收到 sid 字串時，會使用對應的 sid 直接查閱磁片區上的使用者配額記錄。 這會略過 SID 名稱快取。 如果 **FindUser** 因格式不相符而失敗 (例如，提供的登入名稱與 SAM 相容的 UPN) ，以及快取的登入名稱，則可以使用 **TranslateLogonNameToSID** 將登入名稱轉譯成 SID 字串，然後再傳遞到 **FindUser**。 下列 VBScript 程式碼說明這項技巧。


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

 

 




