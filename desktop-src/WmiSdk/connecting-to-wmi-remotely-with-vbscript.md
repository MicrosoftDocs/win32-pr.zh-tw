---
description: 您可以建立連線物件來建立與 WMI 的遠端連線。 此物件包含電腦的名稱、您想要連接的 WMI 命名空間，以及任何相關的認證和驗證層級。
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: 使用 VBScript 從遠端連線至 WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982354"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="cad71-104">使用 VBScript 從遠端連線至 WMI</span><span class="sxs-lookup"><span data-stu-id="cad71-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="cad71-105">您可以建立連線物件來建立與 WMI 的遠端連線。</span><span class="sxs-lookup"><span data-stu-id="cad71-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="cad71-106">此物件包含電腦的名稱、您想要連接的 WMI 命名空間，以及任何相關的認證和驗證層級。</span><span class="sxs-lookup"><span data-stu-id="cad71-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="cad71-107">**使用 VBScript 連接到遠端系統**</span><span class="sxs-lookup"><span data-stu-id="cad71-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="cad71-108">指定連接資訊，例如遠端電腦名稱稱、認證，以及連線的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="cad71-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="cad71-109">如果您要使用相同的認證連接到遠端電腦 (網域和使用者名稱) 您登入時，您可以在 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[名字](constructing-a-moniker-string.md)中指定連接資訊，如下列程式碼範例所述。</span><span class="sxs-lookup"><span data-stu-id="cad71-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="cad71-110">一般來說，您應該指定要在遠端電腦上連接的 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="cad71-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="cad71-111">這是因為在不同的電腦上，預設命名空間可能不相同。</span><span class="sxs-lookup"><span data-stu-id="cad71-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="cad71-112">指定命名空間可確保您連接至所有電腦上的相同命名空間。</span><span class="sxs-lookup"><span data-stu-id="cad71-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="cad71-113">如需 VBScript 常數的詳細資訊，以及使用 [標記] 連接的腳本字串，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="cad71-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="cad71-114">如果您連接到不同網域中的遠端電腦，或是使用不同的使用者名稱和密碼，則必須使用 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cad71-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="cad71-115">如同使用標記，您可以使用 **ConnectServer** 來指定認證、驗證層級，以及遠端連線的命名空間。</span><span class="sxs-lookup"><span data-stu-id="cad71-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="cad71-116">下列程式碼範例說明如何使用 ConnectServer 來存取使用系統管理員帳戶和密碼的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cad71-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="cad71-117">針對遠端連線使用 [**ConnectServer**](swbemlocator-connectserver.md) 函式時，請在對 [**SWbemServices**](swbemservices-security-.md)的呼叫所取得的安全性物件上設定模擬和驗證。</span><span class="sxs-lookup"><span data-stu-id="cad71-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="cad71-118">您可以使用列舉 [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) 來指定模擬層級。</span><span class="sxs-lookup"><span data-stu-id="cad71-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="cad71-119">下列程式碼範例會設定舊版 VBScript 程式碼範例的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="cad71-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="cad71-120">請注意，某些連接需要特定的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="cad71-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="cad71-121">如需詳細資訊，請參閱 [設定用戶端應用程式流程安全性](setting-client-application-process-security.md) 和 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="cad71-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="cad71-122">尤其是，如果您要在遠端電腦上連接的命名空間需要加密連線才能傳回資料，則您應該將驗證層級設定為 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 或6。</span><span class="sxs-lookup"><span data-stu-id="cad71-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="cad71-123">您也可以使用此驗證等級，即使命名空間不需要它也一樣。</span><span class="sxs-lookup"><span data-stu-id="cad71-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="cad71-124">這可確保資料會在網路上進行加密。</span><span class="sxs-lookup"><span data-stu-id="cad71-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="cad71-125">如果您嘗試設定較低的驗證等級，則會傳回拒絕存取訊息。</span><span class="sxs-lookup"><span data-stu-id="cad71-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="cad71-126">如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="cad71-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="cad71-127">建立連線之後，您可以繼續存取 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="cad71-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="cad71-128">如需詳細資訊，請參閱 [腳本和應用程式的 WMI](wmi-tasks-for-scripts-and-applications.md)工作。</span><span class="sxs-lookup"><span data-stu-id="cad71-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cad71-129">範例</span><span class="sxs-lookup"><span data-stu-id="cad71-129">Examples</span></span>

<span data-ttu-id="cad71-130">如需更大的 VBScript 範例，請參閱 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 參考頁面中的範例一節。</span><span class="sxs-lookup"><span data-stu-id="cad71-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="cad71-131">下列 VBScript 程式碼範例會藉由建立遠端電腦名稱稱陣列，然後在每部電腦上顯示隨插即用裝置（ [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)的實例）的名稱，連接到同一網域中的一組遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cad71-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="cad71-132">若要執行下列腳本，您必須是遠端電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cad71-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="cad71-133">請注意，在 [模擬 \\ \\ 等級] 設定之後，腳本會新增遠端電腦名稱稱之前所需的 ""。</span><span class="sxs-lookup"><span data-stu-id="cad71-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="cad71-134">如需 WMI 路徑的詳細資訊，請參閱 [描述 Wmi 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cad71-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="cad71-135">下列 VBScript 程式碼範例可讓您使用不同的認證連接到遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cad71-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="cad71-136">例如，位於不同網域的遠端電腦，或是連接到需要不同使用者名稱和密碼的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="cad71-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="cad71-137">在此情況下，請使用 [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) 連接。</span><span class="sxs-lookup"><span data-stu-id="cad71-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="cad71-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="cad71-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cad71-139">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="cad71-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
