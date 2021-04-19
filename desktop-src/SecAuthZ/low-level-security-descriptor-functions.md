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
# <a name="low-level-security-descriptor-functions"></a>低層級安全性描述元函式

有幾組低層級的函式可用於設定及抓取物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。 每一組都只適用于一組有限的 Windows 物件。 例如，一組適用于檔案物件，另一組則適用于登錄機碼。 下表顯示與不同類型的安全物件搭配使用的低層級函數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>物件型別</th>
<th>低層級函數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">檔案</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">目錄</a></li>
<li>Mailslots</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">具名管道</a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> 和 <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> 函數。 這些函數會使用字元字串來識別安全物件，而不是使用控制碼。</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">處理序</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">執行緒</a></li>
<li><a href="access-rights-for-access-token-objects.md">存取權杖</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">檔案對應物件</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">信號燈</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">事件</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">可等候計時器</a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> 函數。</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">視窗工作站</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">桌上型電腦</a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> 函數。</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">登錄機碼</a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> 和 <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> 函數。</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Windows 服務物件</a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> 函數。</td>
</tr>
<tr class="even">
<td><ul>
<li>印表機物件</li>
</ul></td>
<td>使用 <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> 結構搭配 <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> 和 <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> 函數。</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">網路共用</a></li>
</ul></td>
<td>使用層級502搭配 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> 和 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> 函數。</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">私用物件 (建立應用程式私用的物件) </a></li>
</ul></td>
<td>使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>、 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>、 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> 和 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> 函數。</td>
</tr>
</tbody>
</table>



 

 

 
