---
description: 若要從本機電腦或從遠端電腦取得 WMI 的資料，您必須連接到特定的命名空間，以連線至 WMI 服務。
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: WMI 工作：連接至 WMI 服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987472"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="eb5f3-103">WMI 工作：連接至 WMI 服務</span><span class="sxs-lookup"><span data-stu-id="eb5f3-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="eb5f3-104">若要從本機電腦或從遠端電腦取得 WMI 的資料，您必須連接到特定的 [*命名空間*](gloss-n.md)，以連線至 wmi 服務。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="eb5f3-105">在大部分情況下，請使用速記的 [標記](creating-a-wmi-script.md) 連接或 [**定位器**](swbemlocator-connectserver.md) 連接。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="eb5f3-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="eb5f3-107">遠端連線需要適用于 Windows 防火牆和 DCOM 的適當設定。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="eb5f3-108">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md) 並 [透過 Windows 防火牆連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="eb5f3-109">從 Windows Vista 開始， (UAC) 的「使用者帳戶控制」可能會影響 WMI 存取。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="eb5f3-110">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="eb5f3-111">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="eb5f3-112">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="eb5f3-113">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="eb5f3-114">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="eb5f3-114">**To run a script**</span></span>

1.  <span data-ttu-id="eb5f3-115">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="eb5f3-116">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="eb5f3-117">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="eb5f3-118">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="eb5f3-119">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="eb5f3-120">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="eb5f3-121">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="eb5f3-122">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="eb5f3-123">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="eb5f3-124">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb5f3-125">如何…</span><span class="sxs-lookup"><span data-stu-id="eb5f3-125">How do I...</span></span></th>
<th><span data-ttu-id="eb5f3-126">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="eb5f3-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb5f3-127">...使用 WMI 連接到遠端電腦？</span><span class="sxs-lookup"><span data-stu-id="eb5f3-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="eb5f3-128">請在您的「 <a href="constructing-a-moniker-string.md">標記</a> 」連接字串中指定下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="eb5f3-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="eb5f3-129">NetBIOS 電腦名稱稱，例如 &quot; atl-dc-01&quot;</span><span class="sxs-lookup"><span data-stu-id="eb5f3-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="eb5f3-130">完整的功能變數名稱，例如 &quot; atl-dc-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="eb5f3-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="eb5f3-131">IPv4 位址，例如 &quot; 192.168.1。1&quot;</span><span class="sxs-lookup"><span data-stu-id="eb5f3-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="eb5f3-132">從 Windows Vista 開始，如果目的電腦和您要進行連線的電腦都執行 IPv6，您就可以指定 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="eb5f3-133">如需詳細資訊，請參閱連線 <a href="connecting-to-wmi-on-a-remote-computer.md">到遠端電腦上的 wmi</a> ，以及 <a href="ipv6-and-ipv4-support-in-wmi.md">WMI 中的 IPv6 和 IPv4 支援</a>。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb5f3-134">VB</span><span class="sxs-lookup"><span data-stu-id="eb5f3-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb5f3-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="eb5f3-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb5f3-136">...執行替代認證下的 WMI 腳本？</span><span class="sxs-lookup"><span data-stu-id="eb5f3-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="eb5f3-137">使用 <a href="swbemlocator-connectserver.md"><strong>wbemscripting.swbemlocator. ConnectServer</strong></a> 方法或 c + + 中的 <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator：： ConnectServer</strong></a> ，並包含適當的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="eb5f3-138">連接到本機電腦時，您無法變更認證。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="eb5f3-139">如需詳細資訊，請參閱 <a href="creating-a-wmi-script.md">建立 Wmi 腳本</a> 和 <a href="connecting-to-wmi-on-a-remote-computer.md">連接至遠端電腦上的 wmi</a>。</span><span class="sxs-lookup"><span data-stu-id="eb5f3-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb5f3-140">VB</span><span class="sxs-lookup"><span data-stu-id="eb5f3-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb5f3-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="eb5f3-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="eb5f3-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb5f3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb5f3-143">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="eb5f3-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="eb5f3-144">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="eb5f3-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="eb5f3-145">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="eb5f3-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
