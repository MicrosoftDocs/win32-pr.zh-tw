---
description: 用來設定和取得物件安全描述項的函式。
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 低層級安全性描述元函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989082"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="183c0-103">低層級安全性描述元函式</span><span class="sxs-lookup"><span data-stu-id="183c0-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="183c0-104">有幾組低層級的函式可用於設定及抓取物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="183c0-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="183c0-105">每一組都只適用于一組有限的 Windows 物件。</span><span class="sxs-lookup"><span data-stu-id="183c0-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="183c0-106">例如，一組適用于檔案物件，另一組則適用于登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="183c0-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="183c0-107">下表顯示與不同類型的安全物件搭配使用的低層級函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="183c0-108">物件型別</span><span class="sxs-lookup"><span data-stu-id="183c0-108">Object type</span></span></th>
<th><span data-ttu-id="183c0-109">低層級函數</span><span class="sxs-lookup"><span data-stu-id="183c0-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="183c0-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">檔案</a></span><span class="sxs-lookup"><span data-stu-id="183c0-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="183c0-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">目錄</a></span><span class="sxs-lookup"><span data-stu-id="183c0-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="183c0-112">Mailslots</span><span class="sxs-lookup"><span data-stu-id="183c0-112">Mailslots</span></span></li>
<li><span data-ttu-id="183c0-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">具名管道</a></span><span class="sxs-lookup"><span data-stu-id="183c0-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-114">使用 <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> 和 <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="183c0-115">這些函數會使用字元字串來識別安全物件，而不是使用控制碼。</span><span class="sxs-lookup"><span data-stu-id="183c0-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="183c0-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">處理序</a></span><span class="sxs-lookup"><span data-stu-id="183c0-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="183c0-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">執行緒</a></span><span class="sxs-lookup"><span data-stu-id="183c0-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="183c0-118"><a href="access-rights-for-access-token-objects.md">存取權杖</a></span><span class="sxs-lookup"><span data-stu-id="183c0-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="183c0-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">檔案對應物件</a></span><span class="sxs-lookup"><span data-stu-id="183c0-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="183c0-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">信號燈</a></span><span class="sxs-lookup"><span data-stu-id="183c0-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="183c0-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">事件</a></span><span class="sxs-lookup"><span data-stu-id="183c0-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="183c0-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></span><span class="sxs-lookup"><span data-stu-id="183c0-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="183c0-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">可等候計時器</a></span><span class="sxs-lookup"><span data-stu-id="183c0-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-124">使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="183c0-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">視窗工作站</a></span><span class="sxs-lookup"><span data-stu-id="183c0-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="183c0-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">桌上型電腦</a></span><span class="sxs-lookup"><span data-stu-id="183c0-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-127">使用 <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="183c0-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">登錄機碼</a></span><span class="sxs-lookup"><span data-stu-id="183c0-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-129">使用 <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> 和 <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="183c0-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows 服務物件</a></span><span class="sxs-lookup"><span data-stu-id="183c0-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-131">使用 <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="183c0-132">印表機物件</span><span class="sxs-lookup"><span data-stu-id="183c0-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-133">使用 <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> 結構搭配 <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> 和 <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="183c0-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">網路共用</a></span><span class="sxs-lookup"><span data-stu-id="183c0-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-135">使用層級502搭配 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> 和 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="183c0-136"><a href="acl-based-access-control.md">私用物件 (建立應用程式私用的物件) </a></span><span class="sxs-lookup"><span data-stu-id="183c0-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="183c0-137">使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>、 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>、 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="183c0-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
