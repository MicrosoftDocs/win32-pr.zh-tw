---
description: 用於管理網路的 WMI 工作，並取得連接和 IP 或 MAC 位址的相關資訊。 如需其他範例，請參閱 TechNet ScriptCenter，網址為 https://www.microsoft.com/technet 。
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: WMI 工作：網路功能
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31e8346a064fe2f6c7ab624897be8e789474f7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980780"
---
# <a name="wmi-tasks-networking"></a><span data-ttu-id="467d2-104">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="467d2-104">WMI Tasks: Networking</span></span>

<span data-ttu-id="467d2-105">用於管理網路的 WMI 工作，並取得連接和 IP 或 MAC 位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="467d2-105">WMI tasks for networking manage and obtain information about connections and IP or MAC addresses.</span></span> <span data-ttu-id="467d2-106">如需其他範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="467d2-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="467d2-107">本主題所顯示的腳本範例只會從本機電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="467d2-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="467d2-108">如需如何使用腳本從遠端電腦取得資料的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="467d2-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="467d2-109">下列程式描述如何執行腳本。</span><span class="sxs-lookup"><span data-stu-id="467d2-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="467d2-110">**執行指令碼**</span><span class="sxs-lookup"><span data-stu-id="467d2-110">**To run a script**</span></span>

1.  <span data-ttu-id="467d2-111">複製程式碼，並將它儲存在副檔名為 .vbs 的檔案中，例如 *filename.vbs*。</span><span class="sxs-lookup"><span data-stu-id="467d2-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="467d2-112">確定您的文字編輯器不會將 .txt 副檔名新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="467d2-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="467d2-113">開啟 [命令提示字元] 視窗，並流覽至您儲存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="467d2-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="467d2-114">在命令提示字元中，輸入 **cscript filename.vbs** 。</span><span class="sxs-lookup"><span data-stu-id="467d2-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="467d2-115">如果您無法存取事件記錄檔，請檢查是否從提高許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="467d2-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="467d2-116">某些事件記錄檔，例如安全性事件記錄檔，可能會受到使用者存取控制 (UAC) 的保護。</span><span class="sxs-lookup"><span data-stu-id="467d2-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="467d2-117">依預設，cscript 會在命令提示字元視窗中顯示腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="467d2-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="467d2-118">由於 WMI 腳本可能會產生大量的輸出，因此您可能會想要將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="467d2-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="467d2-119">在命令提示字元中輸入 **cscript filename.vbs > outfile.txt** ，將 *filename.vbs* 腳本的輸出重新導向至 *outfile.txt*。</span><span class="sxs-lookup"><span data-stu-id="467d2-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="467d2-120">下表列出可用於從本機電腦取得各種資料類型的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="467d2-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-121">如何…</span><span class="sxs-lookup"><span data-stu-id="467d2-121">How do I...</span></span></th>
<th><span data-ttu-id="467d2-122">WMI 類別或方法</span><span class="sxs-lookup"><span data-stu-id="467d2-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="467d2-123">...要使用 WMI 停用網路連接嗎？</span><span class="sxs-lookup"><span data-stu-id="467d2-123">...disable a network connection using WMI?</span></span></td>
<td><span data-ttu-id="467d2-124">如果您使用 DHCP，請使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 和 <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> 方法來釋放 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="467d2-124">If you are using DHCP, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> and the <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> method to release the IP address.</span></span> <span data-ttu-id="467d2-125">如果您不是使用 DHCP，則不能使用 WMI 來停用網路連接。</span><span class="sxs-lookup"><span data-stu-id="467d2-125">If you are not using DHCP, you cannot use WMI to disable a network connection.</span></span> <span data-ttu-id="467d2-126">若要重新啟用網路連接，請使用 <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ObjNetCard RenewDHCPLease</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="467d2-126">To re-enable the network connection, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard.RenewDHCPLease</strong></a>.</span></span> <span data-ttu-id="467d2-127">您也可以使用 <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>>releasedhcpleaseall</strong></a> 和 <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> 方法來釋放或更新所有 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="467d2-127">You can also release or renew all of the DHCP leases using the <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> and <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> methods.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-128">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
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
<th><span data-ttu-id="467d2-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="467d2-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="467d2-130">...要停用或啟用 NIC 嗎？</span><span class="sxs-lookup"><span data-stu-id="467d2-130">...disable or enable a NIC?</span></span></td>
<td><p><span data-ttu-id="467d2-131">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> 類別以及 <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>停</strong></a> 用或 <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>啟用</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="467d2-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> or <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="467d2-132">...判斷哪些 IP 位址已指派給指定的網路連線？</span><span class="sxs-lookup"><span data-stu-id="467d2-132">...determine which IP address has been assigned to a given network connection?</span></span></td>
<td><p><span data-ttu-id="467d2-133">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> 類別和 <strong>NetConnectionID</strong> 屬性，來判斷網路連接的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="467d2-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <strong>NetConnectionID</strong> property to determine the MAC address of the network connection.</span></span> <span data-ttu-id="467d2-134">然後，使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別尋找與 MAC 位址相關聯的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="467d2-134">Then, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class to find the IP address associated with the MAC address.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-135">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-136">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="467d2-137">...要判斷網路介面卡的 MAC 位址嗎？</span><span class="sxs-lookup"><span data-stu-id="467d2-137">...determine the MAC address of a network adapter?</span></span></td>
<td><p><span data-ttu-id="467d2-138">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別，並檢查 <strong>MACAddress</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="467d2-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>MACAddress</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="467d2-139">...判斷電腦的 IP 位址嗎？</span><span class="sxs-lookup"><span data-stu-id="467d2-139">...determine the IP address of a computer?</span></span></td>
<td><p><span data-ttu-id="467d2-140">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別，並檢查 <strong>IPAddress</strong> 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="467d2-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>IPAddress</strong> property.</span></span> <span data-ttu-id="467d2-141">這會以陣列的形式傳回，因此請使用 For-Each 迴圈來取得值。</span><span class="sxs-lookup"><span data-stu-id="467d2-141">This is returned as an array, so use a For-Each loop to get the value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-142">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
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
<th><span data-ttu-id="467d2-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="467d2-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="467d2-144">...configu) 電腦以開始透過 DHCP 取得其 IP 位址？</span><span class="sxs-lookup"><span data-stu-id="467d2-144">...configure a computer to start getting its IP address through DHCP?</span></span></td>
<td><p><span data-ttu-id="467d2-145">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="467d2-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-146">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="467d2-147">...為電腦指派靜態 IP 位址？</span><span class="sxs-lookup"><span data-stu-id="467d2-147">...assign a computer a static IP address?</span></span></td>
<td><p><span data-ttu-id="467d2-148">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別和 <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="467d2-148">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-149">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-149">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="467d2-150">...取得網路介面卡的相關資訊，而不需同時抓取 RAS 和 VPN 連線等專案的相關資訊？</span><span class="sxs-lookup"><span data-stu-id="467d2-150">...get information about network adapters without also retrieving information about things like RAS and VPN connections?</span></span></td>
<td><p><span data-ttu-id="467d2-151">使用 <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="467d2-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class.</span></span> <span data-ttu-id="467d2-152">在您的<a href="querying-with-wql.md">WQL</a>查詢中，使用這個子句： Where <strong>IPEnabled</strong>  =  <strong>True</strong>。</span><span class="sxs-lookup"><span data-stu-id="467d2-152">In your <a href="querying-with-wql.md">WQL</a> query, use this clause: Where <strong>IPEnabled</strong> = <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-153">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-153">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="467d2-154">...不使用 Ping.exe ping 電腦嗎？</span><span class="sxs-lookup"><span data-stu-id="467d2-154">...ping a computer without using Ping.exe?</span></span></td>
<td><p><span data-ttu-id="467d2-155">使用 <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> 類別。</span><span class="sxs-lookup"><span data-stu-id="467d2-155">Use the <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> class.</span></span></p>
<p><span data-ttu-id="467d2-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> 可以傳回同時具有 IPv4 位址和 IPv6 位址之電腦的資料。</span><span class="sxs-lookup"><span data-stu-id="467d2-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> can return data for computers that have both IPv4 addresses and IPv6 addresses.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-157">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="467d2-158">VB</span><span class="sxs-lookup"><span data-stu-id="467d2-158">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="467d2-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="467d2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467d2-160">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="467d2-160">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="467d2-161">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="467d2-161">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="467d2-162">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="467d2-162">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

