---
description: 標記字串格式類似于標準 WMI 物件路徑。 如需詳細資訊，請參閱 WMI 物件路徑需求。
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: 建立標記字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318951"
---
# <a name="constructing-a-moniker-string"></a>建立標記字串

標記字串格式類似于標準 WMI 物件路徑。 如需詳細資訊，請參閱 [WMI 物件路徑需求](wmi-object-path-requirements.md)。

標記具有下列部分：

-   前置詞 WinMgmts： (強制) 。 前置詞會指示 Windows Script Host (WSH) 下列程式碼將使用 [腳本 API 物件](scripting-api-objects.md)。
-   安全性設定元件 (選用) 
-   WMI 物件路徑元件 (選用) 

您無法在 WMI 的標記字串中指定密碼。 如果您必須變更密碼 (*strPassword* 參數) 或連接至 WMI 時) 的驗證類型 (*strAuthority* 參數，則呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)。 請注意，您只能指定連線到遠端電腦的密碼和授權單位。 嘗試在本機電腦上執行的腳本中進行設定，會導致錯誤。 如需使用安全性設定和物件路徑元件的詳細資訊，請參閱 [WMI 安全性設定](/previous-versions/tn-archive/ee156574(v=technet.10))。

下列的標記會指定 [**SWbemServices**](swbemservices.md) 物件，該物件表示命名空間根 \\ 預設值、啟用模擬和 wbemPrivilegeDebug (SeDebugPrivilege) 許可權，以及停用 wbemPrivilegeSecurity (SeSecurityPrivilege) 許可權。


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> 所有字串常值都不區分大小寫。
>
> 許可權上的 "！" 前置詞表示要停用許可權;省略這個前置詞表示要啟用許可權。
>
> 在電腦名稱稱或命名空間之前的括弧中指定安全性設定時，電腦名稱稱或命名空間會使用 "！" 前置詞。

 

指定物件路徑時，允許下列預設指派：

-   您可以從物件路徑省略電腦電腦名稱稱，在此情況下會假設為本機電腦名稱稱。
-   命名空間可以從物件路徑中省略，在此情況下會假設為預設命名空間。

    這取決於登錄機碼 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設命名空間** 的值，預設值為「根 CIMv2」 \\ 。

-   也可以指定類別或實例，在此情況下，傳回的物件是 WMI 物件，而不是服務物件。

> [!Note]  
> 如果指定了類別或實例，則在指定電腦電腦名稱稱時無法省略命名空間。

 

如需 WMI 標記字串上所使用之許可權常數的參考，請參閱 [許可權常數](privilege-constants.md)和「腳本簡短名稱」描述項。

## <a name="valid-moniker-strings"></a>有效的標記字串

下列範例會顯示有效的標記字串。

下列的標記會識別本機電腦上的預設命名空間。 傳回 [**SWbemServices**](swbemservices.md) 物件。


```VB
WinMgmts:
```



下列的標記會識別電腦 myServer 上的預設命名空間。 傳回 [**SWbemServices**](swbemservices.md) 物件。


```VB
"WinMgmts://myServer"
```



下列的標記會識別 \\ myServer 電腦上的根 cimv2 命名空間。 傳回 [**SWbemServices**](swbemservices.md) 物件。


```VB
"WinMgmts://myServer/root/cimv2"
```



下列的標記會識別 \\ 本機伺服器上的根 cimv2 命名空間。 傳回 [**SWbemServices**](swbemservices.md) 物件。


```VB
"WinMgmts:root/cimv2"
```



下列的標記會識別 myServer 伺服器上根 cimv2 命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別 \\ 。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



下列的標記會識別本機伺服器上根 cimv2 命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別 \\ 。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



下列的標記會識別本機伺服器上預設命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



下列的標記會在本機伺服器上的預設腳本命名空間中，識別對應至磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例。 傳回 [**SWbemObject**](swbemobject.md) 物件。 腳本的預設命名空間是由 WMI 控制項中指定的預設命名空間設定設定所決定。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



下列的「標記」（namespace）可識別 myServer 伺服器上根 cimv2 命名空間中與磁片磁碟機 C：對應的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 \\ 。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



下列的標記會在本機伺服器上的根 cimv2 命名空間中，識別對應至磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 \\ 。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



下列的標記會識別對應到本機伺服器上預設命名空間中磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例。 傳回 [**SWbemObject**](swbemobject.md) 物件。


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



下列的標記會將模擬層級設定為模擬，並設定 SE \_ DEBUG 許可權。


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



下列的標記會將模擬層級設定為模擬，並設定 SE \_ DEBUG 許可權。 它也會撤銷 SE \_ SHUTDOWN 許可權。


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



下列的標記會從根 wmi 命名空間取出 **myclass** 類別的美式英文當地語系化描述 \\ 。


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



下列的標記會要求使用主體 mydomain 伺服器的 Kerberos 驗證 \\ 。


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



下列的標記會要求使用 mydomain 網域的 NTLM 驗證。


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



下列 VBScript 程式碼範例示範如何在標記中結合安全性和地區設定參數。


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> 雖然標記可提供物件的更直接存取權，但在某些情況下，重複使用的標記可能會比明確連接至 WMI 的對等程式碼更有效率。 如果要考慮應用程式效能，請考慮使用替代機制。
>
> 當執行內嵌于 HTML 網頁的腳本時，不可能使用 VBScript 所提供的 **GetObject** 函式來更新或設定資料，因為 Microsoft Internet Explorer 基於安全考慮而拒絕使用此呼叫。

 

 

 
