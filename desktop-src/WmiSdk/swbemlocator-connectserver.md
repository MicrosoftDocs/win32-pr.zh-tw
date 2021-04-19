---
description: 連接到在 strServer 參數中指定之電腦上的命名空間。
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: 'Wbemscripting.swbemlocator. ConnectServer 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987790"
---
# <a name="swbemlocatorconnectserver-method"></a>Wbemscripting.swbemlocator. ConnectServer 方法

[**Wbemscripting.swbemlocator**](swbemlocator.md)物件的 **ConnectServer** 方法會連接到 *strServer* 參數中指定之電腦上的命名空間。 目的電腦可以是本機或遠端，但必須安裝 WMI。 如需範例以及與連接的 [標記類型] 的比較，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。

從 Windows Vista 開始， **wbemscripting.swbemlocator** 可以使用 *strServer* 參數中的 ipv6 位址，連線到執行 ipv6 的電腦。 如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strServer* \[在中，選擇性\]
</dt> <dd>

您要連接的電腦名稱稱。 如果遠端電腦與您用來登入的使用者帳戶位於不同的網域，請使用完整的電腦名稱稱。 如果您未提供此參數，則呼叫會預設為本機電腦。

範例： `server1.network.fabrikam`

您也可以在此參數中使用 IP 位址。 如果 IP 位址是 IPv6 格式，目的電腦必須執行 IPv6。 IPv4 中的位址看起來像 `123.123.123.123`

IPv6 格式的 IP 位址看起來像 `2010:836B:4179::836B:4179`

如需有關 DNS 和 IPv4 的詳細資訊，請參閱「備註」一節。

</dd> <dt>

*strNamespace* \[在中，選擇性\]
</dt> <dd>

字串，指定您登入的命名空間。 例如，若要登入根 \\ 預設命名空間，請使用根 \\ 預設值。 如果您未指定此參數，它會預設為設定為腳本之預設命名空間的命名空間。 如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。

範例：「根 \\ CIMV2」

</dd> <dt>

*strUser* \[在中，選擇性\]
</dt> <dd>

要用來連接的使用者名稱。 字串的格式可以是使用者名稱或網域使用者名稱 \\ 。 將此參數保留空白，以使用目前的安全性內容。 *StrUser* 參數只能搭配遠端 WMI 伺服器的連接使用。 如果您嘗試指定本機 WMI 連接的 *strUser* ，連接嘗試就會失敗。 如果使用 Kerberos 驗證，則無法在網路上攔截 *strUser* 和 *strPassword* 中指定的使用者名稱和密碼。 您可以使用 UPN 格式來指定 *strUser*。

範例： "DomainName \\ UserName"

> [!Note]  
> 如果在 *strAuthority* 中指定網域，則不得在此指定網域。 在這兩個參數中指定定義域會導致不正確參數錯誤。

 

</dd> <dt>

*strPassword* \[在中，選擇性\]
</dt> <dd>

字串，指定嘗試連接時要使用的密碼。 將參數保留空白，以使用目前的安全性內容。 *StrPassword* 參數只能搭配遠端 WMI 伺服器的連接使用。 如果您嘗試指定本機 WMI 連接的 *strPassword* ，連接嘗試就會失敗。 如果使用 Kerberos 驗證，則無法在網路上攔截 *strUser* 和 *strPassword* 中指定的使用者名稱和密碼。

</dd> <dt>

*strLocale* \[在中，選擇性\]
</dt> <dd>

指定當地語系化程式碼的字串。 如果您想要使用目前的地區設定，請將其保留空白。 如果不是空白，則此參數必須是字串，指出必須在其中取出資訊的所需地區設定。 若為 Microsoft 地區設定識別碼，則字串的格式為 "MS \_ xxxx"，其中 xxxx 是十六進位格式的字串，表示 LCID。 例如，美式英文會顯示為「MS \_ 409」。

</dd> <dt>

*strAuthority* \[在中，選擇性\]
</dt> <dd>

<dt>

""
</dt> <dd>

這是選擇性參數。 但是，如果指定了，則只能使用 Kerberos 或 NTLMDomain。

</dd> <dt>

Kerberos：
</dt> <dd>

如果 *strAuthority* 參數的開頭是 "Kerberos：" 字串，則會使用 kerberos 驗證，且此參數應包含 kerberos 主體名稱。 Kerberos 主體名稱會指定為 Kerberos：*domain*，例如 `Kerberos:fabrikam` `fabrikam` 您嘗試連接的伺服器。

範例： "Kerberos： DOMAIN"

</dd> <dt>

NTLMDomain
</dt> <dd>

若要使用 NT Lan Manager (NTLM) 驗證，您必須將它指定為 NTLMDomain：*domain*，例如 `NTLMDomain:fabrikam` where `fabrikam` 是網域的名稱。

範例： "NTLMDomain： DOMAIN"

</dd> </dl>

如果您將此參數保留空白，作業系統會與 COM 協商，以決定是否要使用 NTLM 或 Kerberos 驗證。 這個參數只能與遠端 WMI 伺服器的連接搭配使用。 如果您嘗試設定本機 WMI 連接的授權單位，連接嘗試就會失敗。

> [!Note]  
> 如果網域是在 *strUser* 中指定，這是慣用的位置，則不得在此指定。 在這兩個參數中指定定義域會導致不正確參數錯誤。

 

</dd> <dt>

*iSecurityFlags* \[在中，選擇性\]
</dt> <dd>

用來將旗標值傳遞至 **ConnectServer**。

<dt>

0 (0x0) 
</dt> <dd>

這個參數的值為0，只會在建立伺服器的連接之後，才傳回 **ConnectServer** 的呼叫。 如果無法建立連線，這可能會導致您的程式無限期停止回應。

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait * * * * (128 (0x80) ) 


</dt> <dd>

**ConnectServer** 呼叫保證會在2分鐘以內傳回。 如果無法建立連線，請使用此旗標來防止您的程式停止無限期地回應。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，WMI 會傳回 [**SWbemServices**](swbemservices.md)物件，該物件系結至 *strServer* 中指定之電腦上的 *strNamespace* 中指定的命名空間。

## <a name="error-codes"></a>錯誤碼

**ConnectServer** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前或指定的使用者名稱和密碼無效或已獲授權，無法進行連接。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100E) 
</dt> <dd>

指定的命名空間不存在於伺服器上。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效，或無法剖析命名空間。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

發生網路錯誤，導致無法正常運作。

</dd> </dl>

## <a name="remarks"></a>備註

當您在遠端電腦上使用不同的使用者名稱和密碼認證連接到帳戶時，通常會使用 **ConnectServer** 方法，因為您無法在 [標記](constructing-a-moniker-string.md) 字串中指定不同的密碼。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

使用 IPv4 位址連線到遠端伺服器可能會導致非預期的行為。 可能的原因是您的環境中有過時的 DNS 專案。 在這些情況下，將會使用機器的過時 PTR 專案，並產生無法預測的結果。 若要避免此行為，您可以將句點附加 ( "."在呼叫 ConnectServer 之前 ) 至 IP 位址。 這會導致反向 DNS 查閱失敗，但可能會允許在正確的電腦上成功 **ConnectServer** 呼叫。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何連接到遠端電腦，以取得 [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) 資料。 在 *strAuthority* 中使用 *strDomain* 中指定的功能變數名稱。


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



下列 PowerShell 程式碼片段會存取遠端伺服器，並列出可用的 WMI 類別。


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ wbemscripting.swbemlocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Wbemscripting.swbemlocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[建立 WMI 腳本](creating-a-wmi-script.md)
</dt> </dl>

 

