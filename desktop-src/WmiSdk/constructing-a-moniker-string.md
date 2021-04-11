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
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="43c22-104">建立標記字串</span><span class="sxs-lookup"><span data-stu-id="43c22-104">Constructing a Moniker String</span></span>

<span data-ttu-id="43c22-105">標記字串格式類似于標準 WMI 物件路徑。</span><span class="sxs-lookup"><span data-stu-id="43c22-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="43c22-106">如需詳細資訊，請參閱 [WMI 物件路徑需求](wmi-object-path-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43c22-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="43c22-107">標記具有下列部分：</span><span class="sxs-lookup"><span data-stu-id="43c22-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="43c22-108">前置詞 WinMgmts： (強制) 。</span><span class="sxs-lookup"><span data-stu-id="43c22-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="43c22-109">前置詞會指示 Windows Script Host (WSH) 下列程式碼將使用 [腳本 API 物件](scripting-api-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="43c22-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="43c22-110">安全性設定元件 (選用) </span><span class="sxs-lookup"><span data-stu-id="43c22-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="43c22-111">WMI 物件路徑元件 (選用) </span><span class="sxs-lookup"><span data-stu-id="43c22-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="43c22-112">您無法在 WMI 的標記字串中指定密碼。</span><span class="sxs-lookup"><span data-stu-id="43c22-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="43c22-113">如果您必須變更密碼 (*strPassword* 參數) 或連接至 WMI 時) 的驗證類型 (*strAuthority* 參數，則呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)。</span><span class="sxs-lookup"><span data-stu-id="43c22-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="43c22-114">請注意，您只能指定連線到遠端電腦的密碼和授權單位。</span><span class="sxs-lookup"><span data-stu-id="43c22-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="43c22-115">嘗試在本機電腦上執行的腳本中進行設定，會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="43c22-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="43c22-116">如需使用安全性設定和物件路徑元件的詳細資訊，請參閱 [WMI 安全性設定](/previous-versions/tn-archive/ee156574(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="43c22-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="43c22-117">下列的標記會指定 [**SWbemServices**](swbemservices.md) 物件，該物件表示命名空間根 \\ 預設值、啟用模擬和 wbemPrivilegeDebug (SeDebugPrivilege) 許可權，以及停用 wbemPrivilegeSecurity (SeSecurityPrivilege) 許可權。</span><span class="sxs-lookup"><span data-stu-id="43c22-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="43c22-118">所有字串常值都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="43c22-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="43c22-119">許可權上的 "！" 前置詞表示要停用許可權;省略這個前置詞表示要啟用許可權。</span><span class="sxs-lookup"><span data-stu-id="43c22-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="43c22-120">在電腦名稱稱或命名空間之前的括弧中指定安全性設定時，電腦名稱稱或命名空間會使用 "！" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="43c22-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="43c22-121">指定物件路徑時，允許下列預設指派：</span><span class="sxs-lookup"><span data-stu-id="43c22-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="43c22-122">您可以從物件路徑省略電腦電腦名稱稱，在此情況下會假設為本機電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="43c22-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="43c22-123">命名空間可以從物件路徑中省略，在此情況下會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="43c22-124">這取決於登錄機碼 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設命名空間** 的值，預設值為「根 CIMv2」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="43c22-125">也可以指定類別或實例，在此情況下，傳回的物件是 WMI 物件，而不是服務物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="43c22-126">如果指定了類別或實例，則在指定電腦電腦名稱稱時無法省略命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="43c22-127">如需 WMI 標記字串上所使用之許可權常數的參考，請參閱 [許可權常數](privilege-constants.md)和「腳本簡短名稱」描述項。</span><span class="sxs-lookup"><span data-stu-id="43c22-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="43c22-128">有效的標記字串</span><span class="sxs-lookup"><span data-stu-id="43c22-128">Valid Moniker Strings</span></span>

<span data-ttu-id="43c22-129">下列範例會顯示有效的標記字串。</span><span class="sxs-lookup"><span data-stu-id="43c22-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="43c22-130">下列的標記會識別本機電腦上的預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="43c22-131">傳回 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="43c22-132">下列的標記會識別電腦 myServer 上的預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="43c22-133">傳回 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="43c22-134">下列的標記會識別 \\ myServer 電腦上的根 cimv2 命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="43c22-135">傳回 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="43c22-136">下列的標記會識別 \\ 本機伺服器上的根 cimv2 命名空間。</span><span class="sxs-lookup"><span data-stu-id="43c22-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="43c22-137">傳回 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="43c22-138">下列的標記會識別 myServer 伺服器上根 cimv2 命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="43c22-139">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="43c22-140">下列的標記會識別本機伺服器上根 cimv2 命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="43c22-141">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="43c22-142">下列的標記會識別本機伺服器上預設命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別。</span><span class="sxs-lookup"><span data-stu-id="43c22-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="43c22-143">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="43c22-144">下列的標記會在本機伺服器上的預設腳本命名空間中，識別對應至磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例。</span><span class="sxs-lookup"><span data-stu-id="43c22-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="43c22-145">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="43c22-146">腳本的預設命名空間是由 WMI 控制項中指定的預設命名空間設定設定所決定。</span><span class="sxs-lookup"><span data-stu-id="43c22-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="43c22-147">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="43c22-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="43c22-148">下列的「標記」（namespace）可識別 myServer 伺服器上根 cimv2 命名空間中與磁片磁碟機 C：對應的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="43c22-149">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="43c22-150">下列的標記會在本機伺服器上的根 cimv2 命名空間中，識別對應至磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="43c22-151">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="43c22-152">下列的標記會識別對應到本機伺服器上預設命名空間中磁片磁碟機 C：的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例。</span><span class="sxs-lookup"><span data-stu-id="43c22-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="43c22-153">傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43c22-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="43c22-154">下列的標記會將模擬層級設定為模擬，並設定 SE \_ DEBUG 許可權。</span><span class="sxs-lookup"><span data-stu-id="43c22-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="43c22-155">下列的標記會將模擬層級設定為模擬，並設定 SE \_ DEBUG 許可權。</span><span class="sxs-lookup"><span data-stu-id="43c22-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="43c22-156">它也會撤銷 SE \_ SHUTDOWN 許可權。</span><span class="sxs-lookup"><span data-stu-id="43c22-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="43c22-157">下列的標記會從根 wmi 命名空間取出 **myclass** 類別的美式英文當地語系化描述 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="43c22-158">下列的標記會要求使用主體 mydomain 伺服器的 Kerberos 驗證 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43c22-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="43c22-159">下列的標記會要求使用 mydomain 網域的 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="43c22-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="43c22-160">下列 VBScript 程式碼範例示範如何在標記中結合安全性和地區設定參數。</span><span class="sxs-lookup"><span data-stu-id="43c22-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


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
> 雖然標記可提供物件的更直接存取權，但在某些情況下，重複使用的標記可能會比明確連接至 WMI 的對等程式碼更有效率。 <span data-ttu-id="43c22-162">如果要考慮應用程式效能，請考慮使用替代機制。</span><span class="sxs-lookup"><span data-stu-id="43c22-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="43c22-163">當執行內嵌于 HTML 網頁的腳本時，不可能使用 VBScript 所提供的 **GetObject** 函式來更新或設定資料，因為 Microsoft Internet Explorer 基於安全考慮而拒絕使用此呼叫。</span><span class="sxs-lookup"><span data-stu-id="43c22-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
