---
title: 工作集資訊
description: 進程的工作集是實際對應至其處理內容的記憶體數量。 PSAPI.DLL 可讓您取得工作集的快照集，或監視工作集。
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3942796ec1150dee411d6074b13f9ee2be4a22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093119"
---
# <a name="working-set-information"></a><span data-ttu-id="fe14d-104">工作集資訊</span><span class="sxs-lookup"><span data-stu-id="fe14d-104">Working Set Information</span></span>

<span data-ttu-id="fe14d-105">進程的工作集是實際對應至其處理內容的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="fe14d-105">The working set of a process is the amount of memory physically mapped to its process context.</span></span> <span data-ttu-id="fe14d-106">PSAPI.DLL 可讓您取得工作集的快照集，或監視工作集。</span><span class="sxs-lookup"><span data-stu-id="fe14d-106">PSAPI enables you to take snapshots of the working set or to monitor the working set.</span></span>

<span data-ttu-id="fe14d-107">[**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset)或 [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex)函式會使用指定進程目前工作集中每個頁面的資訊快照來填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fe14d-107">The [**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) or [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) function fills a buffer with a snapshot of the information for every page in the current working set of the specified process.</span></span> <span data-ttu-id="fe14d-108">此函式只會報告實際存在於呼叫它的實際頁面。</span><span class="sxs-lookup"><span data-stu-id="fe14d-108">The function reports only those pages that are physically present at the exact moment it is called.</span></span>

<span data-ttu-id="fe14d-109">您可以使用工作集監視來找出特定作業需要多少額外的 RAM (例如，將檔案儲存) 。</span><span class="sxs-lookup"><span data-stu-id="fe14d-109">You can use working set monitoring to find out how much additional RAM a particular operation takes (for example, saving a file).</span></span> <span data-ttu-id="fe14d-110">若要開始監視工作集，請呼叫 [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) 函數。</span><span class="sxs-lookup"><span data-stu-id="fe14d-110">To begin monitoring the working set, call the [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) function.</span></span> <span data-ttu-id="fe14d-111">並非所有的程式都可讓您讀取其工作集資訊，因此請確定函式會傳回非零的值，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="fe14d-111">Not all processes let you read their working set information, so be sure that the function returns a nonzero value before you continue.</span></span> <span data-ttu-id="fe14d-112">接下來，呼叫 [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) 函數。</span><span class="sxs-lookup"><span data-stu-id="fe14d-112">Next, call the [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) function.</span></span> <span data-ttu-id="fe14d-113">此函數只會報告自您開始監視工作集之後，已載入記憶體的頁面。</span><span class="sxs-lookup"><span data-stu-id="fe14d-113">This function reports only the pages that have been loaded in memory since you began monitoring the working set.</span></span> <span data-ttu-id="fe14d-114">此函式會傳回 [**Psapi.dll \_ WS \_ WATCH \_ 資訊**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) 結構的陣列中的資料，每個新增的頁面都會有一個結構，並新增至處理常式的工作集。</span><span class="sxs-lookup"><span data-stu-id="fe14d-114">The function returns data in an array of [**PSAPI\_WS\_WATCH\_INFORMATION**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) structures, one structure for each new page added to the working set of the process.</span></span> <span data-ttu-id="fe14d-115">此結構會告訴您哪些頁面位於記憶體中，以及導致系統將它們分頁的原因。</span><span class="sxs-lookup"><span data-stu-id="fe14d-115">The structure tells you which pages are in memory, and what caused the system to page them in.</span></span>

<span data-ttu-id="fe14d-116">[**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset)函式會採用進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe14d-116">The [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) function takes a process handle.</span></span> <span data-ttu-id="fe14d-117">它會盡可能從進程工作集移除最多頁面。</span><span class="sxs-lookup"><span data-stu-id="fe14d-117">It removes as many pages as possible from the process working set.</span></span> <span data-ttu-id="fe14d-118">這項作業主要適用于測試和微調。</span><span class="sxs-lookup"><span data-stu-id="fe14d-118">This operation is useful primarily for testing and tuning.</span></span> <span data-ttu-id="fe14d-119">請注意，如果您傳遞-1 的最小和最大大小， [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) 函式會執行相同的工作。</span><span class="sxs-lookup"><span data-stu-id="fe14d-119">Note that the [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) function does the same thing if you pass it -1 for the minimum and maximum sizes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe14d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe14d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe14d-121">工作集</span><span class="sxs-lookup"><span data-stu-id="fe14d-121">Working Set</span></span>](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 