---
description: 電腦軟體的 WMI 工作會取得資訊，例如 Microsoft Windows Installer (MSI) 和軟體版本所安裝的軟體。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: WMI 工作：電腦軟體
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514044"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="02be4-104">WMI 工作：電腦軟體</span><span class="sxs-lookup"><span data-stu-id="02be4-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="02be4-105">電腦軟體的 WMI 工作會取得資訊，例如 Microsoft Windows Installer (MSI) 和軟體版本所安裝的軟體。</span><span class="sxs-lookup"><span data-stu-id="02be4-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="02be4-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="02be4-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="02be4-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="02be4-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="02be4-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="02be4-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="02be4-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="02be4-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="02be4-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="02be4-110">**To run a script**</span></span>

1.  <span data-ttu-id="02be4-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="02be4-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="02be4-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="02be4-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="02be4-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="02be4-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="02be4-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="02be4-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="02be4-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="02be4-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="02be4-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="02be4-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="02be4-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="02be4-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="02be4-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="02be4-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="02be4-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="02be4-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="02be4-120">執行「Select \* From Win32 \_ Product」查詢可能會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="02be4-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="02be4-121">這是因為支援 Win32 產品的提供者 \_ 未進行查詢優化。</span><span class="sxs-lookup"><span data-stu-id="02be4-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="02be4-122">如需詳細資訊，請參閱 [知識庫文章 974524](https://support.microsoft.com/kb/974524)。</span><span class="sxs-lookup"><span data-stu-id="02be4-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="02be4-123">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="02be4-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02be4-124">如何…</span><span class="sxs-lookup"><span data-stu-id="02be4-124">How do I...</span></span></th>
<th><span data-ttu-id="02be4-125">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="02be4-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02be4-126">...使用腳本卸載軟體？</span><span class="sxs-lookup"><span data-stu-id="02be4-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="02be4-127">如果軟體是使用 Microsoft Windows Installer (MSI) 安裝的，請使用 WMI 類別 <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> 和 <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="02be4-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02be4-128">VB</span><span class="sxs-lookup"><span data-stu-id="02be4-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="02be4-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02be4-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="02be4-130">...使用腳本清查電腦上安裝的所有軟體嗎？</span><span class="sxs-lookup"><span data-stu-id="02be4-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="02be4-131">如果軟體是使用 Microsoft Windows Installer (MSI 安裝) 請使用 WMI 類別 <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="02be4-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02be4-132">VB</span><span class="sxs-lookup"><span data-stu-id="02be4-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="02be4-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02be4-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02be4-134">...判斷安裝的 Microsoft Office 版本為何？</span><span class="sxs-lookup"><span data-stu-id="02be4-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="02be4-135">使用 <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> 類別，並檢查 <strong>Version</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="02be4-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02be4-136">VB</span><span class="sxs-lookup"><span data-stu-id="02be4-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="02be4-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02be4-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="02be4-138">範例</span><span class="sxs-lookup"><span data-stu-id="02be4-138">Examples</span></span>

<span data-ttu-id="02be4-139">[Powershell 遠端電腦資訊腳本](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436)powershell 程式碼範例會使用許多硬體和軟體類別（包括 Win32Product），以使用 WMI 和遠端登入尋找有關遠端電腦的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="02be4-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02be4-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="02be4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02be4-141">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="02be4-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="02be4-142">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="02be4-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="02be4-143">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="02be4-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

