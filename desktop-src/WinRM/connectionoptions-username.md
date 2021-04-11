---
title: 'ConnectionOptions： UserName 屬性 (WSManDisp. h) '
description: 設定並取得遠端電腦上本機或網域帳戶的使用者名稱。 這個屬性會決定驗證的使用者名稱。
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- UserName 屬性 Windows 遠端管理
- UserName 屬性 Windows 遠端管理，ConnectionOptions 物件
- ConnectionOptions 物件 Windows 遠端管理，使用者名稱屬性
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104585"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions。 UserName 屬性

設定並取得遠端電腦上本機或網域帳戶的使用者名稱。 這個屬性會決定驗證的使用者名稱。 如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>屬性值

包含遠端電腦上本機或網域帳戶之使用者名稱的字串。

如果未提供任何值，且未設定 **WSManFlagCredUsernamePassword** 旗標，則會使用執行腳本之帳戶的使用者名稱。

如果未提供任何值，且已設定 **WSManFlagCredUsernamePassword** 旗標，則腳本會提示使用者輸入使用者名稱和密碼。 如果未輸入有效的使用者名稱和密碼，則會傳回拒絕存取錯誤。

## <a name="remarks"></a>備註

下列語法用來指定此屬性。


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



使用 [*negotiate*](windows-remote-management-glossary.md)或 *Kerberos* 驗證時，您可以提供網域帳戶的使用者 **名稱** 和 [**密碼**](connectionoptions-password.md)，或使用 [*基本*](windows-remote-management-glossary.md)身份驗證的本機帳戶。 若要連接到本機帳戶， [**CreateSession**](wsman-createsession.md) 旗標必須包含 **WSManFlagUseBasic** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合。 若要連接到網域帳戶， **CreateSession** 旗標必須包含 **WSManFlagUseNegotiate** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合，或是 **WSManFlagUseKerberos** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合。 網域帳戶的使用者名稱 **必須以** 「電腦使用者名稱」格式指定 \\ ，其中「電腦」部分的字串可以是名稱或 IP 位址。 如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



若要連接到網域帳戶， [**CreateSession**](wsman-createsession.md) 旗標必須包含 **WSManFlagUseNegotiate** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合，以連接到需要協商驗證的網域帳戶。


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





