---
description: SNMP 提供者支援寫入至記錄檔和偵錯工具。
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: SNMP 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985628"
---
# <a name="snmp-events"></a><span data-ttu-id="e3c62-103">SNMP 事件</span><span class="sxs-lookup"><span data-stu-id="e3c62-103">SNMP Events</span></span>

<span data-ttu-id="e3c62-104">SNMP 提供者支援寫入至記錄檔和偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e3c62-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="e3c62-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="e3c62-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="e3c62-106">有幾個登錄機碼和值會定義目前產生的記錄層級和類型：</span><span class="sxs-lookup"><span data-stu-id="e3c62-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="e3c62-107">偵錯</span><span class="sxs-lookup"><span data-stu-id="e3c62-107">Debugging</span></span>

    <span data-ttu-id="e3c62-108">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ MICROSOFT \\ WBEM \\ 提供者 \\ 記錄登錄** 機碼包含記錄值，指出是否可以將資訊寫入至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e3c62-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="e3c62-109">記錄值會設定為0以停用偵錯工具輸出，或設定為1來啟用它。</span><span class="sxs-lookup"><span data-stu-id="e3c62-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="e3c62-110">記錄是 REG \_ DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="e3c62-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="e3c62-111">記錄</span><span class="sxs-lookup"><span data-stu-id="e3c62-111">Logging</span></span>

    <span data-ttu-id="e3c62-112">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ MICROSOFT \\ WBEM 提供者 \\ \\ 記錄 \\ WBEMSNMP 登錄** 機碼會保存 SNMP 提供者特定的所有記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="e3c62-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="e3c62-113">下表列出與此索引鍵相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e3c62-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3c62-114">值</span><span class="sxs-lookup"><span data-stu-id="e3c62-114">Value</span></span></th>
<th><span data-ttu-id="e3c62-115">描述</span><span class="sxs-lookup"><span data-stu-id="e3c62-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3c62-116">類型</span><span class="sxs-lookup"><span data-stu-id="e3c62-116">Type</span></span></td>
<td><span data-ttu-id="e3c62-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="e3c62-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="e3c62-118">採用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e3c62-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="e3c62-119">&quot;File &quot; = (預設) 將偵測輸出傳送至檔案。</span><span class="sxs-lookup"><span data-stu-id="e3c62-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="e3c62-120">&quot;偵錯工具 &quot; = 將偵測輸出傳送至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e3c62-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3c62-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="e3c62-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="e3c62-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="e3c62-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="e3c62-123">接受從1024到 2 ^ 32-1 的整數值。</span><span class="sxs-lookup"><span data-stu-id="e3c62-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="e3c62-124">此值是記錄檔允許的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e3c62-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="e3c62-125">如果小於1024，記錄機制會使用值1024。</span><span class="sxs-lookup"><span data-stu-id="e3c62-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="e3c62-126">針對此值，建議使用大小下限為 8 KB。</span><span class="sxs-lookup"><span data-stu-id="e3c62-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="e3c62-127">當檔案到達 MaxFileSize 所指定的大小時，檔案名前面會加上 ' ~ ' 字元，並會建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="e3c62-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="e3c62-128">因此，記錄所需的最大磁碟空間是此值的兩倍。</span><span class="sxs-lookup"><span data-stu-id="e3c62-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3c62-129">檔案</span><span class="sxs-lookup"><span data-stu-id="e3c62-129">File</span></span></td>
<td><span data-ttu-id="e3c62-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="e3c62-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="e3c62-131">定義當記錄類型設定為 ' File ' 時，要將偵錯工具輸出傳送至其中的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e3c62-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="e3c62-132">預設值為 ' <WBEMLOGS> \wbemsnmp.log. '</span><span class="sxs-lookup"><span data-stu-id="e3c62-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="e3c62-133">如果 <WBEMLOGS> 無法從 WMI 登錄區段判斷目錄，此值會預設為 ' c:\wbemsnmp.log '。</span><span class="sxs-lookup"><span data-stu-id="e3c62-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="e3c62-134">如果使用共用（例如 \\ machine\share\wbemsnmp.log 或 M:\wbemsnmp.log，其中 M： \\ machine\share），則執行 WMI 的本機系統帳戶必須具有 machine\share. 的讀取/寫入存取權限。 \\</span><span class="sxs-lookup"><span data-stu-id="e3c62-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3c62-135">層級</span><span class="sxs-lookup"><span data-stu-id="e3c62-135">Level</span></span></td>
<td><span data-ttu-id="e3c62-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="e3c62-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="e3c62-137">接受從0到 2 ^ 32-1 的整數值。</span><span class="sxs-lookup"><span data-stu-id="e3c62-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="e3c62-138">值是包含32位的邏輯遮罩。</span><span class="sxs-lookup"><span data-stu-id="e3c62-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="e3c62-139">下列位元遮罩會合並，以定義產生的偵錯工具輸出類型：</span><span class="sxs-lookup"><span data-stu-id="e3c62-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="e3c62-140">0： SNMP 類別提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法調用</span><span class="sxs-lookup"><span data-stu-id="e3c62-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="e3c62-141">1： SNMP 類別提供者的執行</span><span class="sxs-lookup"><span data-stu-id="e3c62-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="e3c62-142">2： SNMP 執行個體提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法調用</span><span class="sxs-lookup"><span data-stu-id="e3c62-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="e3c62-143">3： SNMP 執行個體提供者的執行</span><span class="sxs-lookup"><span data-stu-id="e3c62-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="e3c62-144">4： SNMP 類別庫</span><span class="sxs-lookup"><span data-stu-id="e3c62-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="e3c62-145">5： SNMP SMIR</span><span class="sxs-lookup"><span data-stu-id="e3c62-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="e3c62-146">6： SNMP 交互碼</span><span class="sxs-lookup"><span data-stu-id="e3c62-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="e3c62-147">7： SNMP 類型對應程式碼</span><span class="sxs-lookup"><span data-stu-id="e3c62-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="e3c62-148">8： SNMP 執行緒程式碼</span><span class="sxs-lookup"><span data-stu-id="e3c62-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="e3c62-149">9： SNMP 事件提供者介面和實作為</span><span class="sxs-lookup"><span data-stu-id="e3c62-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="e3c62-150">將層級設定為 (2 ^ 0 + 2 ^ 8 =) 257 適用于涉及 SNMP 類別提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法呼叫的作業，以及使用 snmp 執行緒程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="e3c62-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




