---
title: WinSNMP 函數
description: 用於 WinSNMP 的函式可分為下列功能群組。 字母清單如下。
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c5ebb49e8ec56c0d0b1174fd667d847c09d3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092900"
---
# <a name="winsnmp-functions"></a><span data-ttu-id="cb986-104">WinSNMP 函數</span><span class="sxs-lookup"><span data-stu-id="cb986-104">WinSNMP Functions</span></span>

<span data-ttu-id="cb986-105">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="cb986-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb986-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="cb986-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cb986-107">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="cb986-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="cb986-108">用於 WinSNMP 的函式可分為下列功能群組。</span><span class="sxs-lookup"><span data-stu-id="cb986-108">The functions used with WinSNMP fall into the following functional groupings.</span></span> <span data-ttu-id="cb986-109">字母清單如下。</span><span class="sxs-lookup"><span data-stu-id="cb986-109">An alphabetic list follows.</span></span>

-   [<span data-ttu-id="cb986-110">通訊功能</span><span class="sxs-lookup"><span data-stu-id="cb986-110">Communications Functions</span></span>](#winsnmp-communications-functions)
-   [<span data-ttu-id="cb986-111">Entity 和 CoNtext 函數</span><span class="sxs-lookup"><span data-stu-id="cb986-111">Entity and Context Functions</span></span>](#winsnmp-entity-and-context-functions)
-   [<span data-ttu-id="cb986-112">資料庫函數</span><span class="sxs-lookup"><span data-stu-id="cb986-112">Database Functions</span></span>](#winsnmp-database-functions)
-   [<span data-ttu-id="cb986-113">PDU 函式</span><span class="sxs-lookup"><span data-stu-id="cb986-113">PDU Functions</span></span>](#winsnmp-pdu-functions)
-   [<span data-ttu-id="cb986-114">公用程式函數</span><span class="sxs-lookup"><span data-stu-id="cb986-114">Utility Functions</span></span>](#winsnmp-utility-functions)
-   [<span data-ttu-id="cb986-115">變數系結函式</span><span class="sxs-lookup"><span data-stu-id="cb986-115">Variable Binding Functions</span></span>](#winsnmp-variable-binding-functions)
-   [<span data-ttu-id="cb986-116">WinSNMP 函數位母清單</span><span class="sxs-lookup"><span data-stu-id="cb986-116">WinSNMP Functions   Alphabetic List</span></span>](/windows)

## <a name="winsnmp-communications-functions"></a><span data-ttu-id="cb986-117">WinSNMP 通訊功能</span><span class="sxs-lookup"><span data-stu-id="cb986-117">WinSNMP Communications Functions</span></span>

<span data-ttu-id="cb986-118">WinSNMP 通訊函式提供呼叫的 WinSNMP 應用程式與 Microsoft WinSNMP 執行之間的介面。</span><span class="sxs-lookup"><span data-stu-id="cb986-118">The WinSNMP communications functions provide an interface between the calling WinSNMP application and the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="cb986-119">此執行會處理應用程式與其他管理實體之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="cb986-119">The implementation handles communication between the application and other management entities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb986-120">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-120">Function</span></span></th>
<th><span data-ttu-id="cb986-121">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb986-122"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-122"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></span></span></td>
<td><span data-ttu-id="cb986-123">要求 Microsoft WinSNMP 執行會取消重新傳輸嘗試，以及輸入 SNMP 要求訊息的超時通知。</span><span class="sxs-lookup"><span data-stu-id="cb986-123">Requests that the Microsoft WinSNMP implementation cancel retransmission attempts and time-out notifications for an SNMP request message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-124"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-124"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></span></span></td>
<td><span data-ttu-id="cb986-125">通知執行應用程式已中斷連線，不再需要配置的資源。</span><span class="sxs-lookup"><span data-stu-id="cb986-125">Informs the implementation that an application is disconnecting and no longer requires allocated resources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-126"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-126"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></span></span></td>
<td><span data-ttu-id="cb986-127">當在 WinSNMP 應用程式內沒有任何未處理的 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> 或 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> 呼叫成功時，執行清除。</span><span class="sxs-lookup"><span data-stu-id="cb986-127">Performs cleanup when there are no outstanding successful calls to <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> or <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> within a WinSNMP application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-128"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-128"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></span></span></td>
<td><span data-ttu-id="cb986-129">啟用執行以解除配置與會話相關聯的資源，以及關閉通訊機制。</span><span class="sxs-lookup"><span data-stu-id="cb986-129">Enables the implementation to deallocate resources associated with a session, and to close communications mechanisms.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-130"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-130"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></span></span></td>
<td><span data-ttu-id="cb986-131">要求執行以開啟 WinSNMP 會話，並配置資源和通訊機制。</span><span class="sxs-lookup"><span data-stu-id="cb986-131">Requests the implementation to open a WinSNMP session and allocate resources and communications mechanisms.</span></span> <span data-ttu-id="cb986-132">開發新的 WinSNMP 應用程式時，建議您呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式來開啟 WinSNMP 會話，而不是呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="cb986-132">When developing new WinSNMP applications, it is recommended that you call the <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> function to open a WinSNMP session instead of calling the <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-133"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-133"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></span></span></td>
<td><span data-ttu-id="cb986-134">將 WinSNMP 應用程式註冊或取消註冊為 SNMP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="cb986-134">Registers or unregisters a WinSNMP application as an SNMP agent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-135"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-135"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></span></span></td>
<td><span data-ttu-id="cb986-136">要求執行以開啟 WinSNMP 會話，並配置資源和通訊機制。</span><span class="sxs-lookup"><span data-stu-id="cb986-136">Requests the implementation to open a WinSNMP session and allocate resources and communications mechanisms.</span></span> <span data-ttu-id="cb986-137">開發新的 WinSNMP 應用程式時，建議您呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式來開啟 WinSNMP 會話，而不是呼叫 <strong>SnmpOpen</strong> 函數。</span><span class="sxs-lookup"><span data-stu-id="cb986-137">When developing new WinSNMP applications, it is recommended that you call the <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> function to open a WinSNMP session instead of calling the <strong>SnmpOpen</strong> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-138"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-138"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></span></span></td>
<td><span data-ttu-id="cb986-139">傳回 SNMP 訊息和未完成的陷阱資料和通知。</span><span class="sxs-lookup"><span data-stu-id="cb986-139">Returns SNMP messages and outstanding trap data and notifications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-140"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-140"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></span></span></td>
<td><span data-ttu-id="cb986-141">通知執行應用程式必須註冊或取消註冊陷阱和通知。</span><span class="sxs-lookup"><span data-stu-id="cb986-141">Informs the implementation that the application needs to register or unregister for traps and notifications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-142"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-142"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></span></span></td>
<td><span data-ttu-id="cb986-143">要求執行會傳輸通訊協定資料單位。</span><span class="sxs-lookup"><span data-stu-id="cb986-143">Requests that the implementation transmit a protocol data unit.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-144"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-144"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></span></span></td>
<td><span data-ttu-id="cb986-145">通知執行執行應用程式的初始化程式。</span><span class="sxs-lookup"><span data-stu-id="cb986-145">Notifies the implementation to perform initialization procedures for the application.</span></span> <span data-ttu-id="cb986-146">應用程式必須先成功呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> 函式，才能呼叫任何其他的 WinSNMP 函數。</span><span class="sxs-lookup"><span data-stu-id="cb986-146">An application must call the <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> function successfully before it calls any other WinSNMP function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb986-147"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-147"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></span></span></td>
<td><span data-ttu-id="cb986-148">通知 Microsoft WinSNMP 可執行檔 WinSNMP 應用程式需要執行的服務。</span><span class="sxs-lookup"><span data-stu-id="cb986-148">Notifies the Microsoft WinSNMP implementation that the WinSNMP application requires the implementation's services.</span></span> <span data-ttu-id="cb986-149"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> 可支援在相同應用程式中使用 WinSNMP 的多個獨立軟體模組。</span><span class="sxs-lookup"><span data-stu-id="cb986-149"><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> enables support for multiple independent software modules that use WinSNMP within the same application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb986-150"><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb986-150"><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></span></span></td>
<td><span data-ttu-id="cb986-151">通知可使用 SNMP 訊息或非同步事件的 WinSNMP 會話。</span><span class="sxs-lookup"><span data-stu-id="cb986-151">Notifies a WinSNMP session that an SNMP message or asynchronous event is available.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb986-152">這個回呼函式只適用于因為呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式而開啟的會話。</span><span class="sxs-lookup"><span data-stu-id="cb986-152">This callback function applies only to sessions opened as a result of a call to the <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> function.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a><span data-ttu-id="cb986-153">WinSNMP 實體和內容函式</span><span class="sxs-lookup"><span data-stu-id="cb986-153">WinSNMP Entity and Context Functions</span></span>

<span data-ttu-id="cb986-154">WinSNMP 實體和內容函數可讓 WinSNMP 應用程式為 SNMP 實體和內容指定易記的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb986-154">The WinSNMP entity and context functions enable a WinSNMP application to specify user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="cb986-155">Microsoft WinSNMP 實行會使用實作為資料庫，將名稱轉譯為其 SNMPv1 或 SNMPv2C 元件。</span><span class="sxs-lookup"><span data-stu-id="cb986-155">The Microsoft WinSNMP implementation translates the name to its SNMPv1 or SNMPv2C components using the implementation's database.</span></span>



| <span data-ttu-id="cb986-156">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-156">Function</span></span>                                     | <span data-ttu-id="cb986-157">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-157">Description</span></span>                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb986-158">**SnmpCoNtextToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-158">**SnmpContextToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | <span data-ttu-id="cb986-159">傳回字串，這個字串會識別一組受管理物件資源)  (的 SNMP 內容。</span><span class="sxs-lookup"><span data-stu-id="cb986-159">Returns a string that identifies an SNMP context (a set of managed object resources).</span></span>                                  |
| [<span data-ttu-id="cb986-160">**SnmpEntityToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-160">**SnmpEntityToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | <span data-ttu-id="cb986-161">傳回識別 SNMP 管理實體的字串。</span><span class="sxs-lookup"><span data-stu-id="cb986-161">Returns a string that identifies an SNMP management entity.</span></span>                                                            |
| [<span data-ttu-id="cb986-162">**SnmpFreeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cb986-162">**SnmpFreeContext**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | <span data-ttu-id="cb986-163">釋放 [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) 函數針對 SNMP 內容所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="cb986-163">Releases resources allocated by the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) function for an SNMP context.</span></span>         |
| [<span data-ttu-id="cb986-164">**SnmpFreeEntity**</span><span class="sxs-lookup"><span data-stu-id="cb986-164">**SnmpFreeEntity**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | <span data-ttu-id="cb986-165">釋放 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) 函式針對 SNMP 管理實體所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="cb986-165">Releases resources allocated by the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function for an SNMP management entity.</span></span> |
| [<span data-ttu-id="cb986-166">**SnmpSetPort**</span><span class="sxs-lookup"><span data-stu-id="cb986-166">**SnmpSetPort**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | <span data-ttu-id="cb986-167">變更指派給 SNMP 目的地實體的埠。</span><span class="sxs-lookup"><span data-stu-id="cb986-167">Changes the port assigned to an SNMP destination entity.</span></span>                                                               |
| [<span data-ttu-id="cb986-168">**SnmpStrToCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cb986-168">**SnmpStrToContext**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | <span data-ttu-id="cb986-169">傳回特定于執行之 SNMP 內容資訊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb986-169">Returns a handle to SNMP context information that is specific to the implementation.</span></span>                                   |
| [<span data-ttu-id="cb986-170">**SnmpStrToEntity**</span><span class="sxs-lookup"><span data-stu-id="cb986-170">**SnmpStrToEntity**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | <span data-ttu-id="cb986-171">傳回特定于執行之 SNMP 管理實體資訊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb986-171">Returns a handle to SNMP management entity information that is specific to the implementation.</span></span>                         |



 

## <a name="winsnmp-database-functions"></a><span data-ttu-id="cb986-172">WinSNMP 資料庫函式</span><span class="sxs-lookup"><span data-stu-id="cb986-172">WinSNMP Database Functions</span></span>

<span data-ttu-id="cb986-173">WinSNMP 資料庫函式會提供一個可存取 Microsoft WinSNMP 實行系統管理資訊存放區中目前設定的 WinSNMP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cb986-173">The WinSNMP database functions provide a WinSNMP application with access to the current settings in the Microsoft WinSNMP implementation's store of administrative information.</span></span> <span data-ttu-id="cb986-174">這些函數允許變更重新傳輸模式以及實體和內容轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="cb986-174">These functions permit changing the retransmission mode and the entity and context translation mode.</span></span> <span data-ttu-id="cb986-175">資料庫函式也會提供應用程式操作超時和重試計數值的能力。</span><span class="sxs-lookup"><span data-stu-id="cb986-175">The database functions also provide the application with the ability to manipulate the time-out and retry count values.</span></span>



| <span data-ttu-id="cb986-176">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-176">Function</span></span>                                               | <span data-ttu-id="cb986-177">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-177">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb986-178">**SnmpGetRetransmitMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-178">**SnmpGetRetransmitMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | <span data-ttu-id="cb986-179">傳回重新傳輸模式的目前設定。</span><span class="sxs-lookup"><span data-stu-id="cb986-179">Returns the current setting of the retransmission mode.</span></span>                                               |
| [<span data-ttu-id="cb986-180">**SnmpGetRetry**</span><span class="sxs-lookup"><span data-stu-id="cb986-180">**SnmpGetRetry**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | <span data-ttu-id="cb986-181">傳回重新傳輸 SNMP 訊息要求的重試計數值（單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb986-181">Returns the retry count value, in units, for the retransmission of SNMP message requests.</span></span>             |
| [<span data-ttu-id="cb986-182">**SnmpGetTimeout**</span><span class="sxs-lookup"><span data-stu-id="cb986-182">**SnmpGetTimeout**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | <span data-ttu-id="cb986-183">傳回 SNMP 訊息要求的傳輸超時值（以百分之一秒為限）。</span><span class="sxs-lookup"><span data-stu-id="cb986-183">Returns the time-out value, in hundredths of a second, for the transmission of SNMP message requests.</span></span> |
| [<span data-ttu-id="cb986-184">**SnmpGetTranslateMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-184">**SnmpGetTranslateMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | <span data-ttu-id="cb986-185">傳回實體和內容轉譯模式的目前設定。</span><span class="sxs-lookup"><span data-stu-id="cb986-185">Returns the current setting of the entity and context translation mode.</span></span>                               |
| [<span data-ttu-id="cb986-186">**SnmpGetVendorInfo**</span><span class="sxs-lookup"><span data-stu-id="cb986-186">**SnmpGetVendorInfo**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | <span data-ttu-id="cb986-187">抓取可識別 WinSNMP 供應商的資訊。</span><span class="sxs-lookup"><span data-stu-id="cb986-187">Retrieves information that identifies the WinSNMP vendor.</span></span>                                             |
| [<span data-ttu-id="cb986-188">**SnmpSetRetransmitMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-188">**SnmpSetRetransmitMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | <span data-ttu-id="cb986-189">變更重新傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="cb986-189">Changes the retransmission mode.</span></span>                                                                      |
| [<span data-ttu-id="cb986-190">**SnmpSetRetry**</span><span class="sxs-lookup"><span data-stu-id="cb986-190">**SnmpSetRetry**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | <span data-ttu-id="cb986-191">變更 SNMP 訊息要求重新傳輸的重試計數值。</span><span class="sxs-lookup"><span data-stu-id="cb986-191">Changes the retry count value for the retransmission of SNMP message requests.</span></span>                        |
| [<span data-ttu-id="cb986-192">**SnmpSetTimeout**</span><span class="sxs-lookup"><span data-stu-id="cb986-192">**SnmpSetTimeout**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | <span data-ttu-id="cb986-193">變更 SNMP 訊息要求的傳輸超時值。</span><span class="sxs-lookup"><span data-stu-id="cb986-193">Changes the time-out value for the transmission of SNMP message requests.</span></span>                             |
| [<span data-ttu-id="cb986-194">**SnmpSetTranslateMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-194">**SnmpSetTranslateMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | <span data-ttu-id="cb986-195">變更實體和內容轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="cb986-195">Changes the entity and context translation mode.</span></span>                                                      |



 

## <a name="winsnmp-pdu-functions"></a><span data-ttu-id="cb986-196">WinSNMP PDU 函式</span><span class="sxs-lookup"><span data-stu-id="cb986-196">WinSNMP PDU Functions</span></span>

<span data-ttu-id="cb986-197">WinSNMP PDU 函式可讓 WinSNMP 應用程式解壓縮和更新 PDU (或欄位) 的資料元素。</span><span class="sxs-lookup"><span data-stu-id="cb986-197">The WinSNMP PDU functions enable WinSNMP applications to extract and update the data elements (or fields) of a PDU.</span></span> <span data-ttu-id="cb986-198">這包括呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式或 [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) 函數所傳回的 pdu。</span><span class="sxs-lookup"><span data-stu-id="cb986-198">This includes PDUs returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function or the [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) function.</span></span> <span data-ttu-id="cb986-199">PDU 函式也會建立要在 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 和 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式中使用的 pdu。</span><span class="sxs-lookup"><span data-stu-id="cb986-199">The PDU functions also construct PDUs for use in the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) and [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) functions.</span></span>



| <span data-ttu-id="cb986-200">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-200">Function</span></span>                                     | <span data-ttu-id="cb986-201">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-201">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb986-202">**SnmpCreatePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-202">**SnmpCreatePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | <span data-ttu-id="cb986-203">建立並初始化 SNMP 通訊協定資料單位。</span><span class="sxs-lookup"><span data-stu-id="cb986-203">Creates and initializes an SNMP protocol data unit.</span></span>                                                                                                                               |
| [<span data-ttu-id="cb986-204">**SnmpDuplicatePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-204">**SnmpDuplicatePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | <span data-ttu-id="cb986-205">複製 SNMP 通訊協定資料單位。</span><span class="sxs-lookup"><span data-stu-id="cb986-205">Duplicates an SNMP protocol data unit.</span></span>                                                                                                                                            |
| [<span data-ttu-id="cb986-206">**SnmpFreePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-206">**SnmpFreePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | <span data-ttu-id="cb986-207">釋放與 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 或 [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) 函數所建立的 SNMP 通訊協定資料單位相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="cb986-207">Releases resources associated with an SNMP protocol data unit created by the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) or the [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) function.</span></span> |
| [<span data-ttu-id="cb986-208">**SnmpGetPduData**</span><span class="sxs-lookup"><span data-stu-id="cb986-208">**SnmpGetPduData**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | <span data-ttu-id="cb986-209">從指定的 SNMP 通訊協定資料單位傳回選取的資料元素。</span><span class="sxs-lookup"><span data-stu-id="cb986-209">Returns selected data elements from a specified SNMP protocol data unit.</span></span>                                                                                                          |
| [<span data-ttu-id="cb986-210">**SnmpSetPduData**</span><span class="sxs-lookup"><span data-stu-id="cb986-210">**SnmpSetPduData**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | <span data-ttu-id="cb986-211">更新指定 SNMP 通訊協定資料單位中選取的資料元素。</span><span class="sxs-lookup"><span data-stu-id="cb986-211">Updates selected data elements in a specified SNMP protocol data unit.</span></span>                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a><span data-ttu-id="cb986-212">WinSNMP 公用程式函式</span><span class="sxs-lookup"><span data-stu-id="cb986-212">WinSNMP Utility Functions</span></span>

<span data-ttu-id="cb986-213">WinSNMP 公用程式函式可讓 WinSNMP 應用程式跨 WinSNMP 介面管理物件和 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="cb986-213">The WinSNMP utility functions enable a WinSNMP application to manage objects and SNMP messages across the WinSNMP interface.</span></span>



| <span data-ttu-id="cb986-214">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-214">Function</span></span>                                         | <span data-ttu-id="cb986-215">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-215">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb986-216">**SnmpDecodeMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-216">**SnmpDecodeMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | <span data-ttu-id="cb986-217">將已編碼或已序列化的 SNMP 訊息解碼成其構成元件。</span><span class="sxs-lookup"><span data-stu-id="cb986-217">Decodes an encoded or serialized SNMP message into its constituent components.</span></span>                                      |
| [<span data-ttu-id="cb986-218">**SnmpEncodeMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-218">**SnmpEncodeMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | <span data-ttu-id="cb986-219">建立編碼的 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="cb986-219">Creates an encoded SNMP message.</span></span>                                                                                    |
| [<span data-ttu-id="cb986-220">**SnmpFreeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cb986-220">**SnmpFreeDescriptor**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | <span data-ttu-id="cb986-221">發出 Microsoft WinSNMP 的信號，指出它應該釋放配置給特定描述項的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cb986-221">Signals the Microsoft WinSNMP implementation that it should free the memory it allocated for a specific descriptor.</span></span> |
| [<span data-ttu-id="cb986-222">**SnmpGetLastError**</span><span class="sxs-lookup"><span data-stu-id="cb986-222">**SnmpGetLastError**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | <span data-ttu-id="cb986-223">傳回最後一次 SNMP 操作的最後錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="cb986-223">Returns the last-error code value for the last SNMP operation.</span></span>                                                      |
| [<span data-ttu-id="cb986-224">**SnmpOidCompare**</span><span class="sxs-lookup"><span data-stu-id="cb986-224">**SnmpOidCompare**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | <span data-ttu-id="cb986-225">比較兩個 SNMP 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb986-225">Compares two SNMP object identifiers.</span></span>                                                                               |
| [<span data-ttu-id="cb986-226">**SnmpOidCopy**</span><span class="sxs-lookup"><span data-stu-id="cb986-226">**SnmpOidCopy**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | <span data-ttu-id="cb986-227">複製 SNMP 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb986-227">Copies an SNMP object identifier.</span></span>                                                                                   |
| [<span data-ttu-id="cb986-228">**SnmpOidToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-228">**SnmpOidToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | <span data-ttu-id="cb986-229">將 SNMP 物件識別碼的內部二進位標記法轉換為其點數位字串格式。</span><span class="sxs-lookup"><span data-stu-id="cb986-229">Converts the internal binary representation of an SNMP object identifier to its dotted numeric string format.</span></span>       |
| [<span data-ttu-id="cb986-230">**SnmpStrToOid**</span><span class="sxs-lookup"><span data-stu-id="cb986-230">**SnmpStrToOid**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | <span data-ttu-id="cb986-231">將 SNMP 物件識別碼的點數位字串格式轉換為其內部二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="cb986-231">Converts the dotted numeric string format of an SNMP object identifier to its internal binary representation.</span></span>       |



 

## <a name="winsnmp-variable-binding-functions"></a><span data-ttu-id="cb986-232">WinSNMP 變數系結函式</span><span class="sxs-lookup"><span data-stu-id="cb986-232">WinSNMP Variable Binding Functions</span></span>

<span data-ttu-id="cb986-233">WinSNMP 變數系結函式可讓 WinSNMP 應用程式建立和操作變數系結清單，並將它們包含在 Pdu 中。</span><span class="sxs-lookup"><span data-stu-id="cb986-233">The WinSNMP variable binding functions enable WinSNMP applications to construct and manipulate variable binding lists, and include them in PDUs.</span></span>



| <span data-ttu-id="cb986-234">函式</span><span class="sxs-lookup"><span data-stu-id="cb986-234">Function</span></span>                                     | <span data-ttu-id="cb986-235">描述</span><span class="sxs-lookup"><span data-stu-id="cb986-235">Description</span></span>                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb986-236">**SnmpCountVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-236">**SnmpCountVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | <span data-ttu-id="cb986-237">列舉指定變數系結清單中的變數系結專案。</span><span class="sxs-lookup"><span data-stu-id="cb986-237">Enumerates the variable binding entries in a specified variable binding list.</span></span>                                                                                                   |
| [<span data-ttu-id="cb986-238">**SnmpCreateVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-238">**SnmpCreateVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | <span data-ttu-id="cb986-239">建立新的變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="cb986-239">Creates a new variable binding list.</span></span>                                                                                                                                            |
| [<span data-ttu-id="cb986-240">**SnmpDeleteVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-240">**SnmpDeleteVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | <span data-ttu-id="cb986-241">從變數系結清單中移除變數系結專案。</span><span class="sxs-lookup"><span data-stu-id="cb986-241">Removes a variable binding entry from a variable binding list.</span></span>                                                                                                                  |
| [<span data-ttu-id="cb986-242">**SnmpDuplicateVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-242">**SnmpDuplicateVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | <span data-ttu-id="cb986-243">複製變數繫結欄位表。</span><span class="sxs-lookup"><span data-stu-id="cb986-243">Copies a variable binding list.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="cb986-244">**SnmpFreeVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-244">**SnmpFreeVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | <span data-ttu-id="cb986-245">釋放 [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) 或 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 函數先前配置的變數系結清單資源。</span><span class="sxs-lookup"><span data-stu-id="cb986-245">Releases resources for a variable binding list allocated previously by the [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) or the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> |
| [<span data-ttu-id="cb986-246">**SnmpGetVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-246">**SnmpGetVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | <span data-ttu-id="cb986-247">從指定的變數繫結項目抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="cb986-247">Retrieves information from a specified variable binding entry.</span></span>                                                                                                                  |
| [<span data-ttu-id="cb986-248">**SnmpSetVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-248">**SnmpSetVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | <span data-ttu-id="cb986-249">變更變數系結清單中的變數繫結項目;將新的變數繫結項目附加至現有的變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="cb986-249">Changes variable binding entries in a variable binding list; appends new variable binding entries to an existing variable binding list.</span></span>                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a><span data-ttu-id="cb986-250">WinSNMP 函數位母清單</span><span class="sxs-lookup"><span data-stu-id="cb986-250">WinSNMP Functions   Alphabetic List</span></span>

-   [<span data-ttu-id="cb986-251">**SNMPAPI \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cb986-251">**SNMPAPI\_CALLBACK**</span></span>](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [<span data-ttu-id="cb986-252">**SnmpCancelMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-252">**SnmpCancelMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [<span data-ttu-id="cb986-253">**SnmpCleanup**</span><span class="sxs-lookup"><span data-stu-id="cb986-253">**SnmpCleanup**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [<span data-ttu-id="cb986-254">**SnmpClose**</span><span class="sxs-lookup"><span data-stu-id="cb986-254">**SnmpClose**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [<span data-ttu-id="cb986-255">**SnmpCoNtextToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-255">**SnmpContextToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [<span data-ttu-id="cb986-256">**SnmpCountVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-256">**SnmpCountVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [<span data-ttu-id="cb986-257">**SnmpCreatePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-257">**SnmpCreatePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [<span data-ttu-id="cb986-258">**SnmpCreateSession**</span><span class="sxs-lookup"><span data-stu-id="cb986-258">**SnmpCreateSession**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [<span data-ttu-id="cb986-259">**SnmpCreateVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-259">**SnmpCreateVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [<span data-ttu-id="cb986-260">**SnmpDecodeMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-260">**SnmpDecodeMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [<span data-ttu-id="cb986-261">**SnmpDeleteVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-261">**SnmpDeleteVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [<span data-ttu-id="cb986-262">**SnmpDuplicatePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-262">**SnmpDuplicatePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [<span data-ttu-id="cb986-263">**SnmpDuplicateVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-263">**SnmpDuplicateVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [<span data-ttu-id="cb986-264">**SnmpEncodeMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-264">**SnmpEncodeMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [<span data-ttu-id="cb986-265">**SnmpEntityToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-265">**SnmpEntityToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [<span data-ttu-id="cb986-266">**SnmpFreeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cb986-266">**SnmpFreeContext**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [<span data-ttu-id="cb986-267">**SnmpFreeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cb986-267">**SnmpFreeDescriptor**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [<span data-ttu-id="cb986-268">**SnmpFreeEntity**</span><span class="sxs-lookup"><span data-stu-id="cb986-268">**SnmpFreeEntity**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [<span data-ttu-id="cb986-269">**SnmpFreePdu**</span><span class="sxs-lookup"><span data-stu-id="cb986-269">**SnmpFreePdu**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [<span data-ttu-id="cb986-270">**SnmpFreeVbl**</span><span class="sxs-lookup"><span data-stu-id="cb986-270">**SnmpFreeVbl**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [<span data-ttu-id="cb986-271">**SnmpGetLastError**</span><span class="sxs-lookup"><span data-stu-id="cb986-271">**SnmpGetLastError**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [<span data-ttu-id="cb986-272">**SnmpGetPduData**</span><span class="sxs-lookup"><span data-stu-id="cb986-272">**SnmpGetPduData**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [<span data-ttu-id="cb986-273">**SnmpGetRetransmitMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-273">**SnmpGetRetransmitMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [<span data-ttu-id="cb986-274">**SnmpGetRetry**</span><span class="sxs-lookup"><span data-stu-id="cb986-274">**SnmpGetRetry**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [<span data-ttu-id="cb986-275">**SnmpGetTimeout**</span><span class="sxs-lookup"><span data-stu-id="cb986-275">**SnmpGetTimeout**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [<span data-ttu-id="cb986-276">**SnmpGetTranslateMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-276">**SnmpGetTranslateMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [<span data-ttu-id="cb986-277">**SnmpGetVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-277">**SnmpGetVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [<span data-ttu-id="cb986-278">**SnmpGetVendorInfo**</span><span class="sxs-lookup"><span data-stu-id="cb986-278">**SnmpGetVendorInfo**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [<span data-ttu-id="cb986-279">**SnmpListen**</span><span class="sxs-lookup"><span data-stu-id="cb986-279">**SnmpListen**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [<span data-ttu-id="cb986-280">**SnmpOidCompare**</span><span class="sxs-lookup"><span data-stu-id="cb986-280">**SnmpOidCompare**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [<span data-ttu-id="cb986-281">**SnmpOidCopy**</span><span class="sxs-lookup"><span data-stu-id="cb986-281">**SnmpOidCopy**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [<span data-ttu-id="cb986-282">**SnmpOidToStr**</span><span class="sxs-lookup"><span data-stu-id="cb986-282">**SnmpOidToStr**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [<span data-ttu-id="cb986-283">**SnmpOpen**</span><span class="sxs-lookup"><span data-stu-id="cb986-283">**SnmpOpen**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [<span data-ttu-id="cb986-284">**SnmpRecvMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-284">**SnmpRecvMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [<span data-ttu-id="cb986-285">**SnmpRegister**</span><span class="sxs-lookup"><span data-stu-id="cb986-285">**SnmpRegister**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [<span data-ttu-id="cb986-286">**SnmpSendMsg**</span><span class="sxs-lookup"><span data-stu-id="cb986-286">**SnmpSendMsg**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [<span data-ttu-id="cb986-287">**SnmpSetPduData**</span><span class="sxs-lookup"><span data-stu-id="cb986-287">**SnmpSetPduData**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [<span data-ttu-id="cb986-288">**SnmpSetPort**</span><span class="sxs-lookup"><span data-stu-id="cb986-288">**SnmpSetPort**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [<span data-ttu-id="cb986-289">**SnmpSetRetransmitMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-289">**SnmpSetRetransmitMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [<span data-ttu-id="cb986-290">**SnmpSetRetry**</span><span class="sxs-lookup"><span data-stu-id="cb986-290">**SnmpSetRetry**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [<span data-ttu-id="cb986-291">**SnmpSetTimeout**</span><span class="sxs-lookup"><span data-stu-id="cb986-291">**SnmpSetTimeout**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [<span data-ttu-id="cb986-292">**SnmpSetTranslateMode**</span><span class="sxs-lookup"><span data-stu-id="cb986-292">**SnmpSetTranslateMode**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [<span data-ttu-id="cb986-293">**SnmpSetVb**</span><span class="sxs-lookup"><span data-stu-id="cb986-293">**SnmpSetVb**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [<span data-ttu-id="cb986-294">**SnmpStartup**</span><span class="sxs-lookup"><span data-stu-id="cb986-294">**SnmpStartup**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [<span data-ttu-id="cb986-295">**SnmpStrToCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cb986-295">**SnmpStrToContext**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [<span data-ttu-id="cb986-296">**SnmpStrToEntity**</span><span class="sxs-lookup"><span data-stu-id="cb986-296">**SnmpStrToEntity**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [<span data-ttu-id="cb986-297">**SnmpStrToOid**</span><span class="sxs-lookup"><span data-stu-id="cb986-297">**SnmpStrToOid**</span></span>](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

