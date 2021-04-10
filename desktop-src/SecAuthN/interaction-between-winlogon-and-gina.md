---
description: Winlogon 和 GINA 必須傳達初始化資訊、處理安全的注意順序 (SAS) 監視和通知，以及允許登出和關機活動。
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Winlogon 和 GINA 之間的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027355"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="a34b5-103">Winlogon 和 GINA 之間的互動</span><span class="sxs-lookup"><span data-stu-id="a34b5-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="a34b5-104">[*Winlogon*](../secgloss/w-gly.md) 和 [*GINA*](../secgloss/g-gly.md) 必須傳達初始化資訊、處理 [*安全的注意順序*](../secgloss/s-gly.md) (SAS) 監視和通知，以及允許登出和關機活動。</span><span class="sxs-lookup"><span data-stu-id="a34b5-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="a34b5-105">Winlogon 的狀態會決定呼叫哪個 GINA 函式來處理任何指定的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="a34b5-106">通訊的發生順序如下所示。</span><span class="sxs-lookup"><span data-stu-id="a34b5-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="a34b5-107">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="a34b5-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a34b5-108">事件</span><span class="sxs-lookup"><span data-stu-id="a34b5-108">Event</span></span></th>
<th><span data-ttu-id="a34b5-109">描述</span><span class="sxs-lookup"><span data-stu-id="a34b5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a34b5-110">工作站開機</span><span class="sxs-lookup"><span data-stu-id="a34b5-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="a34b5-111">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> 函式，以通知有關所使用之 Winlogon 版本的 GINA。</span><span class="sxs-lookup"><span data-stu-id="a34b5-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="a34b5-112">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> 函式，為 GINA 提供支援函式的位址、Winlogon 的控制碼，以及取得 GINA (的 <a href="/windows/desktop/SecGloss/c-gly"><em>內容</em></a> 資訊，以便在所有未來的 GINA) 呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="a34b5-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="a34b5-113">Winlogon 處於已登出狀態。</span><span class="sxs-lookup"><span data-stu-id="a34b5-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34b5-114">沒有人登入</span><span class="sxs-lookup"><span data-stu-id="a34b5-114">No one is logged on</span></span></td>
<td><span data-ttu-id="a34b5-115"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-116">收到 SAS 事件時，GINA 會呼叫 Winlogon 的 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="a34b5-117">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> 函式，允許 GINA 處理使用者的識別和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="a34b5-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="a34b5-118">登入成功時，Winlogon 會處於登入狀態。</span><span class="sxs-lookup"><span data-stu-id="a34b5-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34b5-119">使用者已登入</span><span class="sxs-lookup"><span data-stu-id="a34b5-119">The user is logged on</span></span></td>
<td><span data-ttu-id="a34b5-120"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-121">收到 SAS 事件時，GINA 會呼叫 Winlogon 的 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="a34b5-122">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式，允許 GINA 將選項呈現給目前登入的使用者。</span><span class="sxs-lookup"><span data-stu-id="a34b5-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34b5-123">使用者已登入並想要鎖定電腦</span><span class="sxs-lookup"><span data-stu-id="a34b5-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="a34b5-124"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-125">GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="a34b5-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-126">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-127">GINA 會傳回 WLX_SAS_ACTION_LOCK_WKSTA。</span><span class="sxs-lookup"><span data-stu-id="a34b5-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="a34b5-128">Winlogon 處於工作站鎖定狀態。</span><span class="sxs-lookup"><span data-stu-id="a34b5-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34b5-129">使用者已登入、工作站已鎖定，且使用者想要解除鎖定電腦</span><span class="sxs-lookup"><span data-stu-id="a34b5-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="a34b5-130"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-131">GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="a34b5-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-132">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-133">GINA 會傳回 WLX_SAS_ACTION_UNLOCK_WKSTA。</span><span class="sxs-lookup"><span data-stu-id="a34b5-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34b5-134">使用者已登入，而程式呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> 函式</span><span class="sxs-lookup"><span data-stu-id="a34b5-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="a34b5-135">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34b5-136">使用者已登入，而想要使用 SAS 登出</span><span class="sxs-lookup"><span data-stu-id="a34b5-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="a34b5-137"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-138">GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="a34b5-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-139">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-140">GINA 會傳回 WLX_SAS_ACTION_LOGOFF。</span><span class="sxs-lookup"><span data-stu-id="a34b5-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="a34b5-141">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34b5-142">使用者已登入，並想要使用 ExitWindowsEx 來登出和關閉<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="a34b5-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="a34b5-143">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-144">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34b5-145">使用者已登入，並想要使用 SAS 登出和關閉</span><span class="sxs-lookup"><span data-stu-id="a34b5-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="a34b5-146"> (GINA 會監視裝置) 的 SAS 事件。</span><span class="sxs-lookup"><span data-stu-id="a34b5-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="a34b5-147">GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="a34b5-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-148">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-149">GINA 會傳回 WLX_SAS_ACTION_SHUTDOWN。</span><span class="sxs-lookup"><span data-stu-id="a34b5-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="a34b5-150">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="a34b5-151">Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="a34b5-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
