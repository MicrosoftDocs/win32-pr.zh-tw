---
description: WMI 腳本可以壓縮 c + + 程式所需的許多步驟。
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: 使用 VBScript 連接至 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850780"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="855fc-103">使用 VBScript 連接至 WMI</span><span class="sxs-lookup"><span data-stu-id="855fc-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="855fc-104">WMI 腳本可以壓縮 c + + 程式所需的許多步驟。</span><span class="sxs-lookup"><span data-stu-id="855fc-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="855fc-105">它們可以連接至 WMI，而不只是透過 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件，也可以透過「winmgmts：」標記。</span><span class="sxs-lookup"><span data-stu-id="855fc-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="855fc-106">「名字標記」（namespace）是在 WMI 中尋找命名空間、類別或實例的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="855fc-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="855fc-107">名稱 "winmgmts：" 是告知 Windows Script Host 使用 WMI 物件、連接至預設命名空間，並取得 [**SWbemServices**](swbemservices.md) 物件的 wmi 標記。</span><span class="sxs-lookup"><span data-stu-id="855fc-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="855fc-108">其他連接資訊（例如模擬層級或特定類別或實例）會出現在字串後面的 [標記名稱] 中。</span><span class="sxs-lookup"><span data-stu-id="855fc-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="855fc-109">您可以在建立或取得 WMI 物件的呼叫中使用名字。</span><span class="sxs-lookup"><span data-stu-id="855fc-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="855fc-110">如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="855fc-111">下列程式說明如何使用 **wbemscripting.swbemlocator** 連接到 WMI。</span><span class="sxs-lookup"><span data-stu-id="855fc-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="855fc-112">**使用 Wbemscripting.swbemlocator 連接到 WMI**</span><span class="sxs-lookup"><span data-stu-id="855fc-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="855fc-113">使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))的呼叫來取出定位器物件。</span><span class="sxs-lookup"><span data-stu-id="855fc-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="855fc-114">使用 [**ConnectServer**](swbemlocator-connectserver.md) 方法的呼叫來登入命名空間。</span><span class="sxs-lookup"><span data-stu-id="855fc-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="855fc-115">如果您未在 [**ConnectServer**](swbemlocator-connectserver.md)的呼叫中指定電腦，則 WMI 會連接到本機電腦。</span><span class="sxs-lookup"><span data-stu-id="855fc-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="855fc-116">如果您沒有指定命名空間，則 WMI 會連接到登錄機碼中指定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="855fc-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="855fc-117">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設命名空間**</span><span class="sxs-lookup"><span data-stu-id="855fc-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="855fc-118">預設命名空間是 \\ 根 \\ cimv2。</span><span class="sxs-lookup"><span data-stu-id="855fc-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="855fc-119">如需命名空間的詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。</span><span class="sxs-lookup"><span data-stu-id="855fc-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="855fc-120">使用 [**SWbemServices \_**](swbemservices-security-.md)方法的呼叫來設定模擬等級。</span><span class="sxs-lookup"><span data-stu-id="855fc-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="855fc-121">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="855fc-122">實行腳本的用途。</span><span class="sxs-lookup"><span data-stu-id="855fc-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="855fc-123">WMI 公開各種腳本物件，這些物件是用來存取和操作網路上的資料。</span><span class="sxs-lookup"><span data-stu-id="855fc-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="855fc-124">如需詳細資訊，請參閱操作 WMI 的 [類別和實例資訊](manipulating-class-and-instance-information.md) 和 [腳本 API](scripting-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="855fc-125">下列程式描述如何連接至 WMI，並使用標記來取得物件。</span><span class="sxs-lookup"><span data-stu-id="855fc-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="855fc-126">**若要連接至 WMI 並使用標記抓取物件**</span><span class="sxs-lookup"><span data-stu-id="855fc-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="855fc-127">使用輸入參數中的標記來呼叫 [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) 。</span><span class="sxs-lookup"><span data-stu-id="855fc-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="855fc-128">Moiniker 包含數個您可以用來連線到 WMI 的元素：</span><span class="sxs-lookup"><span data-stu-id="855fc-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="855fc-129">"Winmgmts：" 會告知 WSH 使用 [腳本 API 物件](scripting-api-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="855fc-130">在此特定範例中，WSH 會知道它應該會傳回描述系統上第一個 Win32 Register-scheduledjob 的 SWbemObject \_ 。</span><span class="sxs-lookup"><span data-stu-id="855fc-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="855fc-131">其他可能傳回的物件將會是 SWbemCollection 或 [**SWbemServices**](swbemservices.md) 物件，取決於所述的名字。</span><span class="sxs-lookup"><span data-stu-id="855fc-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="855fc-132">您可以選擇性地設定連接的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="855fc-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="855fc-133">不過請注意，您不能在標記中設定名稱和密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="855fc-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="855fc-134">如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="855fc-135">您可以選擇性地定義 WMI 物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="855fc-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="855fc-136">這包括本機或遠端電腦、命名空間，以及類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="855fc-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="855fc-137">如需在 WMI 腳本中使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) 的詳細資訊，請參閱 [建立實例](creating-an-instance.md) 和抓取 [wmi 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="855fc-138">除了抓取單一專案或集合，您也可以選擇取出 [**SWbemServices**](swbemservices.md) 物件 (如先前範例) 所述。</span><span class="sxs-lookup"><span data-stu-id="855fc-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="855fc-139">之後，您就可以在傳回的物件上呼叫其他查詢。</span><span class="sxs-lookup"><span data-stu-id="855fc-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="855fc-140">在上述範例中，模擬或 impersonationLevel = 3 是預設的進程安全性層級。</span><span class="sxs-lookup"><span data-stu-id="855fc-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="855fc-141">在下列範例中，除非您需要將進程安全性變更為 **委派**，否則不需要指定此進程的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="855fc-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="855fc-142">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="855fc-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="855fc-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="855fc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855fc-144">WMI 中的腳本</span><span class="sxs-lookup"><span data-stu-id="855fc-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
