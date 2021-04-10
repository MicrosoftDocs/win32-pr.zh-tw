---
description: 若要將已經在執行中的處理常式，偵錯工具應該使用 DebugActiveProcess 搭配處理序識別碼。 若要取出進程識別碼的清單，請使用 EnumProcesses 或 Process32First 函式。
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: 正在執行進程的偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109992"
---
# <a name="debugging-a-running-process"></a><span data-ttu-id="03ffb-104">正在執行進程的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="03ffb-104">Debugging a Running Process</span></span>

<span data-ttu-id="03ffb-105">若要將已經在執行中的處理常式，偵錯工具應該使用 [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 搭配處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="03ffb-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="03ffb-106">若要取出進程識別碼的清單，請使用 [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) 或 [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) 函式。</span><span class="sxs-lookup"><span data-stu-id="03ffb-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="03ffb-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 會將偵錯工具附加至使用中的進程。</span><span class="sxs-lookup"><span data-stu-id="03ffb-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="03ffb-108">在此情況下，只有使用中的進程可以進行調試;其子進程無法進行。</span><span class="sxs-lookup"><span data-stu-id="03ffb-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="03ffb-109">偵錯工具必須具有執行中進程的適當存取權，才能使用 **DebugActiveProcess**。</span><span class="sxs-lookup"><span data-stu-id="03ffb-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="03ffb-110">如需存取權限的詳細資訊，請參閱 [存取控制](../secauthz/access-control.md)。</span><span class="sxs-lookup"><span data-stu-id="03ffb-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="03ffb-111">當偵錯工具已建立或附加至它想要進行偵錯工具的程式之後，系統會將進程中發生之所有偵測事件的偵錯工具，以及在任何子進程中（如果有指定）通知偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="03ffb-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="03ffb-112">如需有關偵錯工具事件的詳細資訊，請參閱 [偵錯工具事件](debugging-events.md)。</span><span class="sxs-lookup"><span data-stu-id="03ffb-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="03ffb-113">若要從正在進行調試的進程卸離，偵錯工具應該使用 [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) 函數。</span><span class="sxs-lookup"><span data-stu-id="03ffb-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
