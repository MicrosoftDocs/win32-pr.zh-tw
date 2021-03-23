---
title: 命令佇列和命令清單的設計原理
description: 啟用轉譯工作和多執行緒調整的目標，需要對 Direct3D 應用程式如何將轉譯工作提交至 GPU 的基本變更。
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- 命令清單
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104297"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a><span data-ttu-id="86443-105">命令佇列和命令清單的設計原理</span><span class="sxs-lookup"><span data-stu-id="86443-105">Design Philosophy of Command Queues and Command Lists</span></span>

<span data-ttu-id="86443-106">啟用轉譯工作和多執行緒調整的目標，需要對 Direct3D 應用程式如何將轉譯工作提交至 GPU 的基本變更。</span><span class="sxs-lookup"><span data-stu-id="86443-106">The goals of enabling reuse of rendering work and of multi-threaded scaling, required fundamental changes to how Direct3D apps submit rendering work to the GPU.</span></span> <span data-ttu-id="86443-107">在 Direct3D 12 中，提交轉譯工作的程式與舊版不同，有三種重要的方式：</span><span class="sxs-lookup"><span data-stu-id="86443-107">In Direct3D 12, the process of submitting rendering work differs from earlier versions in three important ways:</span></span>

<dl> 1. <span data-ttu-id="86443-108">排除立即內容。</span><span class="sxs-lookup"><span data-stu-id="86443-108">Elimination of the immediate context.</span></span> <span data-ttu-id="86443-109">這會啟用多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="86443-109">This enables multi-threading.</span></span>  
2. <span data-ttu-id="86443-110">應用程式現在擁有轉譯呼叫如何分組為圖形處理單元， (GPU) 工作專案。</span><span class="sxs-lookup"><span data-stu-id="86443-110">Apps now own how rendering calls are grouped into graphics processing unit (GPU) work items.</span></span> <span data-ttu-id="86443-111">這可重複使用。</span><span class="sxs-lookup"><span data-stu-id="86443-111">This enables re-use.</span></span>  
3. <span data-ttu-id="86443-112">應用程式現在會明確地控制將工作提交至 GPU 的時間。</span><span class="sxs-lookup"><span data-stu-id="86443-112">Apps now explicitly control when work is submitted to the GPU .</span></span> <span data-ttu-id="86443-113">這會啟用專案1和2。</span><span class="sxs-lookup"><span data-stu-id="86443-113">This enables items 1 and 2.</span></span>  
</dl>

-   [<span data-ttu-id="86443-114">移除立即內容</span><span class="sxs-lookup"><span data-stu-id="86443-114">Removal of the immediate context</span></span>](#removal-of-the-immediate-context)
-   [<span data-ttu-id="86443-115">GPU 工作專案的群組</span><span class="sxs-lookup"><span data-stu-id="86443-115">Grouping of GPU work items</span></span>](#grouping-of-gpu-work-items)
-   [<span data-ttu-id="86443-116">GPU 工作提交</span><span class="sxs-lookup"><span data-stu-id="86443-116">GPU work submission</span></span>](#gpu-work-submission)
-   [<span data-ttu-id="86443-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="86443-117">Related topics</span></span>](#related-topics)

## <a name="removal-of-the-immediate-context"></a><span data-ttu-id="86443-118">移除立即內容</span><span class="sxs-lookup"><span data-stu-id="86443-118">Removal of the immediate context</span></span>

<span data-ttu-id="86443-119">Microsoft Direct3D 11 到 Microsoft Direct3D 12 的最大變更，就是不再有與裝置相關聯的單一立即內容。</span><span class="sxs-lookup"><span data-stu-id="86443-119">The largest change from Microsoft Direct3D 11 to Microsoft Direct3D 12 is that there is no longer a single, immediate context associated with a device.</span></span> <span data-ttu-id="86443-120">相反地，若要轉譯，應用程式會建立可在其中呼叫傳統轉譯 Api 的命令清單。</span><span class="sxs-lookup"><span data-stu-id="86443-120">Instead, to render, apps create command lists in which traditional rendering APIs can be called.</span></span> <span data-ttu-id="86443-121">命令清單看起來類似于使用立即內容的 Direct3D 11 應用程式轉譯方法，因為它包含繪製基本專案或變更呈現狀態的呼叫。</span><span class="sxs-lookup"><span data-stu-id="86443-121">A command list looks similar to the render method of a Direct3D 11 app that used the immediate context in that it contains calls that draw primitives or change the rendering state.</span></span> <span data-ttu-id="86443-122">如同立即內容，每個命令清單都不是無限制執行緒;不過，您可以同時記錄多個命令清單，以利用新式、多重核心的處理器。</span><span class="sxs-lookup"><span data-stu-id="86443-122">Like immediate contexts, each command list is not free-threaded; however, multiple command lists can be recorded concurrently, which takes advantage of modern, multi-core processors.</span></span>

<span data-ttu-id="86443-123">命令清單通常會執行一次。</span><span class="sxs-lookup"><span data-stu-id="86443-123">Command lists are typically executed once.</span></span> <span data-ttu-id="86443-124">但是，如果應用程式在提交新的執行之前，確保先前的執行已完成，就可以多次執行命令清單。</span><span class="sxs-lookup"><span data-stu-id="86443-124">However, a command list can be executed multiple times if the application ensures that the previous executions are complete before submitting new executions.</span></span> <span data-ttu-id="86443-125">如需有關命令清單同步處理的詳細資訊，請參閱 [執行和同步處理命令](executing-and-synchronizing-command-lists.md)清單。</span><span class="sxs-lookup"><span data-stu-id="86443-125">For more information about command list synchronization, see [Executing and synchronizing command lists](executing-and-synchronizing-command-lists.md).</span></span>

## <a name="grouping-of-gpu-work-items"></a><span data-ttu-id="86443-126">GPU 工作專案的群組</span><span class="sxs-lookup"><span data-stu-id="86443-126">Grouping of GPU work items</span></span>

<span data-ttu-id="86443-127">除了命令清單之外，Direct3D 12 還會藉由新增第二個層級的命令清單（稱為組合），來利用目前所有硬體中的 *功能。*</span><span class="sxs-lookup"><span data-stu-id="86443-127">In addition to command lists, Direct3D 12 takes advantage of functionality present in all hardware today by adding a second level of command lists, which are called *bundles*.</span></span> <span data-ttu-id="86443-128">為了協助區分這兩種類型，第一層命令清單可以稱為 *直接命令清單*。</span><span class="sxs-lookup"><span data-stu-id="86443-128">To help to distinguish these two types, the first-level command lists can be referred to as *direct command lists*.</span></span> <span data-ttu-id="86443-129">套件組合的目的是要讓應用程式將少量的 API 命令群組在一起，以便於稍後從直接命令清單中重複執行。</span><span class="sxs-lookup"><span data-stu-id="86443-129">The purpose of bundles is to allow apps to group a small number of API commands together for later, repeated execution from within direct command lists.</span></span> <span data-ttu-id="86443-130">建立配套時，驅動程式會盡可能地執行最多預先處理，以使稍後的執行更有效率。</span><span class="sxs-lookup"><span data-stu-id="86443-130">At the time of creating a bundle, the driver will perform as much pre-processing as possible to make later execution efficient.</span></span> <span data-ttu-id="86443-131">然後，您可以從多個命令清單內執行套件組合，並在相同的命令清單中多次執行。</span><span class="sxs-lookup"><span data-stu-id="86443-131">Bundles can then be executed from within multiple command lists and multiple times within the same command list.</span></span>

<span data-ttu-id="86443-132">重複使用套件組合是使用單一 CPU 執行緒改善效率的大型驅動程式。</span><span class="sxs-lookup"><span data-stu-id="86443-132">The re-use of bundles is a large driver of improved efficiency with single CPU threads.</span></span> <span data-ttu-id="86443-133">因為套組是預先處理的，且可以提交多次，所以在組合內可以執行哪些作業有某些限制。</span><span class="sxs-lookup"><span data-stu-id="86443-133">Because bundles are pre-processed and can be submitted multiple times, there are certain restrictions on what operations can be performed within a bundle.</span></span> <span data-ttu-id="86443-134">如需詳細資訊，請參閱 [建立和錄製命令清單和](recording-command-lists-and-bundles.md)組合。</span><span class="sxs-lookup"><span data-stu-id="86443-134">For more information, see [Creating and recording command lists and bundles](recording-command-lists-and-bundles.md).</span></span>

## <a name="gpu-work-submission"></a><span data-ttu-id="86443-135">GPU 工作提交</span><span class="sxs-lookup"><span data-stu-id="86443-135">GPU work submission</span></span>

<span data-ttu-id="86443-136">若要在 GPU 上執行工作，應用程式必須明確地將命令清單提交至與 Direct3D 裝置相關聯的命令佇列。</span><span class="sxs-lookup"><span data-stu-id="86443-136">To execute work on the GPU, an app must explicitly submit a command list to a command queue associated with the Direct3D device.</span></span> <span data-ttu-id="86443-137">您可以多次提交 direct 命令清單來執行多次，但應用程式會負責確保在 GPU 上執行的直接命令清單已完成執行，然後再次提交。</span><span class="sxs-lookup"><span data-stu-id="86443-137">A direct command list can be submitted for execution multiple times, but the app is responsible for ensuring that the direct command list has finished executing on the GPU before submitting it again.</span></span> <span data-ttu-id="86443-138">套件組合沒有並行使用限制，而且可以在多個命令清單中執行多次，但無法直接將配套提交到命令佇列以供執行。</span><span class="sxs-lookup"><span data-stu-id="86443-138">Bundles have no concurrent-use restrictions and can be executed multiple times in multiple command lists, but bundles cannot be directly submitted to a command queue for execution.</span></span>

<span data-ttu-id="86443-139">任何執行緒都可以隨時將命令清單提交至任何命令佇列，而執行時間會自動序列化命令佇列中的命令清單提交，同時保留提交順序。</span><span class="sxs-lookup"><span data-stu-id="86443-139">Any thread may submit a command list to any command queue at any time, and the runtime will automatically serialize submission of the command list in the command queue while preserving the submission order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86443-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="86443-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86443-141">在 Direct3D 12 中提交工作</span><span class="sxs-lookup"><span data-stu-id="86443-141">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 




