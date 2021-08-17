---
title: 'CreateSession 方法 (WSManDisp .h) '
description: 建立可用於後續網路作業的會話物件。
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- CreateSession 方法 Windows 遠端管理
- CreateSession 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateSession 方法
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330f8ea6456001c7e3b81dfbfeb07a125d30a5069596ef7d4f3e6ad561994ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742601"
---
# <a name="wsmancreatesession-method"></a>WSMan. CreateSession 方法

建立可用於後續網路作業的 [**會話**](session.md) 物件。

## <a name="syntax"></a>語法


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*連接* \[在中，選擇性\]
</dt> <dd>

要連接的通訊協定和服務，包括 IPv4 或 IPv6。 連接資訊的格式如下： <*傳輸* >< *位址* >< *尾碼*>。 如需範例，請參閱備註。 如果未提供任何連接資訊，則會使用本機電腦。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

指定驗證方法的會話旗標，例如用於連接到遠端電腦的驗證方法，例如「 [*協商驗證*](windows-remote-management-glossary.md) 」或「 [*摘要式驗證*](windows-remote-management-glossary.md)」。 這些旗標也會指定其他會話連接資訊，例如編碼或加密。 此參數必須包含 **\_ \_ WSManSessionFlags** 中的一或多個旗標以進行遠端連線。 如需詳細資訊，請參閱 [會話常數](session-constants.md)。 本機電腦上的 WinRM 連接不需要任何旗標設定。 預設值為 **WSManFlagUseNegotiate**。

如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md) 和 *connectionOptions* 參數。

</dd> <dt>

*connectionOptions* \[在中，選擇性\]
</dt> <dd>

[**ConnectionOptions**](connectionoptions.md)物件的指標，其中包含使用者名稱和密碼。 預設值為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

可以用來執行本機或遠端 WinRM 作業的 [**會話**](session.md) 物件。

## <a name="remarks"></a>備註

**CreateSession** 方法會藉由收集參數，例如旗標、認證和 *連接* 參數的連接字串，初始化 [**會話**](session.md)物件。 **CreateSession** 並不會實際連接到本機或遠端電腦。 如果無法建立連接，則在呼叫 **CreateSession** 之後，第一個 **會話作業**（例如 [**Get**](session-get.md)或 [**列舉**](session-enumerate.md)）會發生失敗。 此行為不同于與遠端電腦上的 [*命名空間*](windows-remote-management-glossary.md)的 [*WMI*](windows-remote-management-glossary.md)連接。 如需詳細資訊，請參閱[Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。

下列 VBScript 程式碼範例會用來呼叫這個方法。


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



下列範例顯示在建立 HTTPS 會話時，用來指定 *連線參數 (* 中的連接資訊的不同格式、<*位址*> 欄位必須符合伺服器電腦憑證名稱，否則) 發生失敗：

-   "https://service"

    使用 HTTPS 連接到預設的 web 服務位置。

-   "https://service.corp.com/websvcs/wsman"

    使用 HTTPS 連接到特定的 web 服務位置。

-   "HTTPs:// \[ E3D7：0000：0000：0000：51F4：9BC8： C0A8： 6420 \] "

    使用 HTTPS 和 IPv6 搭配預設通訊埠。

-   "HTTPs:// \[ E3D7：0000：0000：0000：51F4：9BC8： C0A8： 6420 \] ： 9999/wsman"

    使用 HTTPS 和 IPv6 搭配指定的埠。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會在本機電腦上建立會話。


```VB
 Set NewSession = Wsman.CreateSession   
   
```



下列 VBScript 程式碼範例會在以 IP 位址識別的遠端電腦上建立會話。 腳本會提供帳戶的使用者名稱和密碼。 **WSManFlagCredUserNamePassword** 和 **WSManFlagUseBasic** 旗標會合並，以指出帳戶是遠端電腦上的本機帳戶。 如果建立會話失敗，腳本會終止。 腳本會使用傳回常數的方法，例如 [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)。

若要執行此腳本，請注意，您必須設定用戶端和伺服器的預設設定，以允許未加密的流量和基本驗證 (**AllowUnencrypted** 設為 **true** ，基本身份設定為 **true**) 。 如需詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



在下列 VBScript 程式碼範例中，此帳戶是網域帳戶，而且會使用「協商驗證」。 使用「協商驗證」時，您必須將使用者名稱指定為 `computername\username` 或 `ipaddress\username` 。


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
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

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**會話**](session.md)
</dt> <dt>

[遠端連線的驗證](authentication-for-remote-connections.md)
</dt> <dt>

[Windows 遠端管理的安裝和設定](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





