---
description: 登錄的 WMI 工作會建立和修改登錄機碼和值。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: WMI 工作：登錄
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983828"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="503a1-104">WMI 工作：登錄</span><span class="sxs-lookup"><span data-stu-id="503a1-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="503a1-105">登錄的 WMI 工作會建立和修改登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="503a1-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="503a1-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="503a1-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="503a1-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="503a1-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="503a1-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="503a1-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="503a1-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="503a1-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="503a1-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="503a1-110">**To run a script**</span></span>

1.  <span data-ttu-id="503a1-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="503a1-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="503a1-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="503a1-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="503a1-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="503a1-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="503a1-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="503a1-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="503a1-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="503a1-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="503a1-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="503a1-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="503a1-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="503a1-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="503a1-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="503a1-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="503a1-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="503a1-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="503a1-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="503a1-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-121">如何…</span><span class="sxs-lookup"><span data-stu-id="503a1-121">How do I...</span></span></th>
<th><span data-ttu-id="503a1-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="503a1-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="503a1-123">...使用 WMI 讀取登錄機碼值？</span><span class="sxs-lookup"><span data-stu-id="503a1-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="503a1-124">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="503a1-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="503a1-125">您無法取得此類別的任何實例，因為 <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">系統登錄提供者</a> 只是方法和事件提供者。</span><span class="sxs-lookup"><span data-stu-id="503a1-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="503a1-126">不過，您可以透過 <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> 或 <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>enumvalue 類型</strong></a>等方法取得登錄資料。</span><span class="sxs-lookup"><span data-stu-id="503a1-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="503a1-127">位於 root\cimv2 命名空間中的 <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>會取得整個登錄的相關資料，例如它的大小。</span><span class="sxs-lookup"><span data-stu-id="503a1-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-128">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
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
<th><span data-ttu-id="503a1-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="503a1-130">...要建立新的登錄機碼嗎？</span><span class="sxs-lookup"><span data-stu-id="503a1-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="503a1-131">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別，以及 <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-132">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="503a1-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="503a1-134">...在機碼下建立新的登錄值？</span><span class="sxs-lookup"><span data-stu-id="503a1-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="503a1-135">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別，以及 <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="503a1-136">然後使用其中一個 Set 方法，取決於值是什麼登錄資料類型，例如 <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="503a1-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="503a1-137">Set 方法會建立值（如果尚未存在）。</span><span class="sxs-lookup"><span data-stu-id="503a1-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="503a1-138">如需詳細資訊，請參閱將登錄 <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">資料類型對應至 WMI 資料類型</a>。</span><span class="sxs-lookup"><span data-stu-id="503a1-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-139">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="503a1-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="503a1-141">...嘗試撰寫腳本來讀取登錄時，請避免收到不正確類別錯誤？</span><span class="sxs-lookup"><span data-stu-id="503a1-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="503a1-142">存取 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別時，請使用 root\default 命名空間。</span><span class="sxs-lookup"><span data-stu-id="503a1-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="503a1-143"><strong>StdRegProv</strong> 不是 cimv2 命名空間的一部分，因此， &quot; &quot; 如果您嘗試連接到 &quot; root\cimv2： StdRegProv，就會產生無效類別錯誤 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="503a1-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-144">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="503a1-145">...要檢查特定登錄機碼的安全性嗎？</span><span class="sxs-lookup"><span data-stu-id="503a1-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="503a1-146">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別和 <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="503a1-147">您只能檢查正在執行腳本或應用程式之目前使用者的存取權限。</span><span class="sxs-lookup"><span data-stu-id="503a1-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="503a1-148">您無法檢查另一個指定使用者的存取權限。</span><span class="sxs-lookup"><span data-stu-id="503a1-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="503a1-149">...要讀取和寫入二進位登錄值嗎？</span><span class="sxs-lookup"><span data-stu-id="503a1-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="503a1-150">使用位於 Root\Default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別， &quot; &quot; 以及 <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> 和 <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="503a1-151">以一連串位元組十六進位值形式出現在 RegEdt32 公用程式中的登錄值，會採用 <strong>REG_BINARY</strong> 資料格式。</span><span class="sxs-lookup"><span data-stu-id="503a1-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="503a1-152">如需詳細資訊，請參閱將登錄 <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">資料類型對應至 WMI 資料類型</a>。</span><span class="sxs-lookup"><span data-stu-id="503a1-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="503a1-153">下列 VBScript 程式碼範例會建立具有二進位值的新索引鍵。</span><span class="sxs-lookup"><span data-stu-id="503a1-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="503a1-154">二進位值會在以十六進位指定的 <em>iValues</em> 位元組陣列中提供。</span><span class="sxs-lookup"><span data-stu-id="503a1-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-155">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="503a1-156">下列腳本會讀取二進位值。</span><span class="sxs-lookup"><span data-stu-id="503a1-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-157">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
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
<th><span data-ttu-id="503a1-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="503a1-159">...讀取和寫入含有多個字串的登錄值？</span><span class="sxs-lookup"><span data-stu-id="503a1-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="503a1-160">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別，以及 <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> 和 <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="503a1-161">以空格分隔的一連串字串形式出現在 RegEdt32 公用程式中的登錄機碼會採用 <strong>REG_MULTI_SZ</strong> 資料格式。</span><span class="sxs-lookup"><span data-stu-id="503a1-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="503a1-162">如需詳細資訊，請參閱將登錄 <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">資料類型對應至 WMI 資料類型</a>。</span><span class="sxs-lookup"><span data-stu-id="503a1-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="503a1-163">下列 VBScript 程式碼範例會建立新的索引鍵和新的 multistring 值。</span><span class="sxs-lookup"><span data-stu-id="503a1-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-164">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
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
<th><span data-ttu-id="503a1-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="503a1-166">下列腳本會讀取 multistring 值。</span><span class="sxs-lookup"><span data-stu-id="503a1-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-167">VB</span><span class="sxs-lookup"><span data-stu-id="503a1-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
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
<th><span data-ttu-id="503a1-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="503a1-169">...要移除登錄機碼嗎？</span><span class="sxs-lookup"><span data-stu-id="503a1-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="503a1-170">使用位於 root\default 命名空間中的 <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> 類別和 <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="503a1-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="503a1-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="503a1-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="503a1-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="503a1-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="503a1-173">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="503a1-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="503a1-174">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="503a1-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="503a1-175">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="503a1-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="503a1-176">修改系統登錄</span><span class="sxs-lookup"><span data-stu-id="503a1-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="503a1-177">**StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="503a1-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
