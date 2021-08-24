---
title: 'ConnectionOptions 物件 (WSManDisp) '
description: ConnectionOptions 物件會傳遞至 CreateSession 方法，以提供與遠端電腦上的本機帳戶相關聯的使用者名稱和密碼。
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- ConnectionOptions 物件 Windows 遠端管理
- ConnectionOptions 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734088"
---
# <a name="connectionoptions-object"></a>ConnectionOptions 物件

**ConnectionOptions** 物件會傳遞至 [**CreateSession**](wsman-createsession.md)方法，以提供與遠端電腦上的本機帳戶相關聯的使用者名稱和密碼。 如果未提供任何參數，則執行腳本之帳戶的認證會設定為預設值。

## <a name="members"></a>成員

**ConnectionOptions** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ConnectionOptions** 物件具有這些屬性。



| 屬性                                                  | 存取類型           | 描述                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**密碼**](connectionoptions-password.md)<br/> | 唯寫<br/> | 設定遠端電腦上的本機或網域帳戶的密碼。<br/>           |
| [**使用者**](connectionoptions-username.md)<br/> | 讀取/寫入<br/> | 設定並取得遠端電腦上本機或網域帳戶的使用者名稱。<br/> |



 

## <a name="remarks"></a>備註

**ConnectionOptions** 物件會對應至 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)介面。

如果 Windows 遠端管理用戶端應用程式是在模擬下執行，則如果您設定 [**Password**](connectionoptions-password.md)屬性，就會發生失敗。 用戶端應用程式是在本機或遠端電腦上將要求傳送至 WinRM 的腳本或其他程式。 用戶端應用程式可能會在模擬下執行，因為它呼叫的函式如 [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85))。 如果 ASP 進程是在模擬用戶端的帳戶下執行，則 (ASP) 或服務的作用中伺服器頁面就無法要求使用者名稱和密碼。

使用使用者 [**名稱**](connectionoptions-username.md)和 [**密碼**](connectionoptions-password.md)進行驗證時，應在 [**WSman. CreateSession**](wsman-createsession.md)呼叫上設定 **WSManFlagCredUserNamePassword** 旗標。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例示範如何建立 **ConnectionOptions** 物件、在遠端電腦上設定帳戶的屬性，以及用來建立 [**會話**](session.md) 物件。


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端連線的驗證](authentication-for-remote-connections.md)
</dt> <dt>

[WinRM 腳本 API](winrm-scripting-api.md)
</dt> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> <dt>

[從本機電腦取得資料](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

