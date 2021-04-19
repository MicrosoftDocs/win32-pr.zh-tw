---
description: 所有使用者都具有系統中處理常式清單的讀取權限，而且有許多不同的函式會列舉使用中的進程。 您應使用的函式將取決於所需平臺支援等因素。
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: 進程列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979783"
---
# <a name="process-enumeration"></a><span data-ttu-id="12ea0-104">進程列舉</span><span class="sxs-lookup"><span data-stu-id="12ea0-104">Process Enumeration</span></span>

<span data-ttu-id="12ea0-105">所有使用者都具有系統中處理常式清單的讀取權限，而且有許多不同的函式會列舉使用中的進程。</span><span class="sxs-lookup"><span data-stu-id="12ea0-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="12ea0-106">您應使用的函式將取決於所需平臺支援等因素。</span><span class="sxs-lookup"><span data-stu-id="12ea0-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="12ea0-107">下列函數用來列舉進程。</span><span class="sxs-lookup"><span data-stu-id="12ea0-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="12ea0-108">函式</span><span class="sxs-lookup"><span data-stu-id="12ea0-108">Function</span></span>                                                    | <span data-ttu-id="12ea0-109">描述</span><span class="sxs-lookup"><span data-stu-id="12ea0-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="12ea0-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="12ea0-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="12ea0-111">抓取系統中每個處理常式物件的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="12ea0-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="12ea0-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="12ea0-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="12ea0-113">抓取系統快照中所發生第一個進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ea0-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="12ea0-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="12ea0-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="12ea0-115">抓取系統快照中所記錄之下一個進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ea0-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="12ea0-116">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="12ea0-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="12ea0-117">抓取指定終端機伺服器上使用中進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ea0-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="12ea0-118">Toolhelp 函數和 [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) 列舉所有進程。</span><span class="sxs-lookup"><span data-stu-id="12ea0-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="12ea0-119">若要列出在特定使用者帳戶中執行的處理常式，請使用 [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) 並篩選使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="12ea0-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="12ea0-120">您可以篩選會話識別碼，以隱藏在其他終端機伺服器會話中執行的進程。</span><span class="sxs-lookup"><span data-stu-id="12ea0-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="12ea0-121">您也可以藉由呼叫 [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)、 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)和 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 與 **TokenUser**，依使用者帳戶篩選進程（不論列舉函數為何）。</span><span class="sxs-lookup"><span data-stu-id="12ea0-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="12ea0-122">不過，除非您已授與存取權，否則無法開啟受安全描述項保護的進程。</span><span class="sxs-lookup"><span data-stu-id="12ea0-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
