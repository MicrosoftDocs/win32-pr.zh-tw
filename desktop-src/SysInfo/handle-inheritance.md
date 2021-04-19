---
description: 子進程可以繼承其父進程的控制碼。 繼承的控制碼只在子進程的內容中有效。 若要讓子進程繼承其父進程的開啟控制碼，請使用下列步驟。
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: 處理繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000322"
---
# <a name="handle-inheritance"></a><span data-ttu-id="edc38-105">處理繼承</span><span class="sxs-lookup"><span data-stu-id="edc38-105">Handle Inheritance</span></span>

<span data-ttu-id="edc38-106">子進程可以繼承其父進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="edc38-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="edc38-107">繼承的控制碼只在子進程的內容中有效。</span><span class="sxs-lookup"><span data-stu-id="edc38-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="edc38-108">若要讓子進程繼承其父進程的開啟控制碼，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="edc38-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="edc38-109">使用設定為 **TRUE** 的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構的 **bInheritHandle** 成員建立控制碼。</span><span class="sxs-lookup"><span data-stu-id="edc38-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="edc38-110">使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立子進程，並將 *bInheritHandles* 參數設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="edc38-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="edc38-111">[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式會複製要在目前進程或另一個進程中使用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="edc38-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="edc38-112">如果應用程式為另一個進程複製其中一個控制碼，則重複的控制碼只在其他進程的內容中有效。</span><span class="sxs-lookup"><span data-stu-id="edc38-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="edc38-113">重複或繼承的控制碼是唯一值，但它是指與原始控制碼相同的物件。</span><span class="sxs-lookup"><span data-stu-id="edc38-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="edc38-114">進程可以繼承或複製下列物件類型的控制碼：</span><span class="sxs-lookup"><span data-stu-id="edc38-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="edc38-115">存取權杖</span><span class="sxs-lookup"><span data-stu-id="edc38-115">Access Token</span></span>
-   <span data-ttu-id="edc38-116">通訊裝置</span><span class="sxs-lookup"><span data-stu-id="edc38-116">Communications device</span></span>
-   <span data-ttu-id="edc38-117">主控台輸入</span><span class="sxs-lookup"><span data-stu-id="edc38-117">Console input</span></span>
-   <span data-ttu-id="edc38-118">主控台畫面緩衝區</span><span class="sxs-lookup"><span data-stu-id="edc38-118">Console screen buffer</span></span>
-   <span data-ttu-id="edc38-119">桌面</span><span class="sxs-lookup"><span data-stu-id="edc38-119">Desktop</span></span>
-   <span data-ttu-id="edc38-120">目錄</span><span class="sxs-lookup"><span data-stu-id="edc38-120">Directory</span></span>
-   <span data-ttu-id="edc38-121">事件</span><span class="sxs-lookup"><span data-stu-id="edc38-121">Event</span></span>
-   <span data-ttu-id="edc38-122">檔案</span><span class="sxs-lookup"><span data-stu-id="edc38-122">File</span></span>
-   <span data-ttu-id="edc38-123">檔案對應</span><span class="sxs-lookup"><span data-stu-id="edc38-123">File mapping</span></span>
-   <span data-ttu-id="edc38-124">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="edc38-124">Job</span></span>
-   <span data-ttu-id="edc38-125">郵箱</span><span class="sxs-lookup"><span data-stu-id="edc38-125">Mailslot</span></span>
-   <span data-ttu-id="edc38-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="edc38-126">Mutex</span></span>
-   <span data-ttu-id="edc38-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="edc38-127">Pipe</span></span>
-   <span data-ttu-id="edc38-128">處理序</span><span class="sxs-lookup"><span data-stu-id="edc38-128">Process</span></span>
-   <span data-ttu-id="edc38-129">登錄機碼</span><span class="sxs-lookup"><span data-stu-id="edc38-129">Registry key</span></span>
-   <span data-ttu-id="edc38-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="edc38-130">Semaphore</span></span>
-   <span data-ttu-id="edc38-131">插座</span><span class="sxs-lookup"><span data-stu-id="edc38-131">Socket</span></span>
-   <span data-ttu-id="edc38-132">Thread</span><span class="sxs-lookup"><span data-stu-id="edc38-132">Thread</span></span>
-   <span data-ttu-id="edc38-133">計時器</span><span class="sxs-lookup"><span data-stu-id="edc38-133">Timer</span></span>
-   <span data-ttu-id="edc38-134">視窗站</span><span class="sxs-lookup"><span data-stu-id="edc38-134">Window station</span></span>

<span data-ttu-id="edc38-135">所有其他物件都是建立它們的進程的私用;無法複製或繼承其物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="edc38-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="edc38-136">如需詳細資訊，請參閱[繼承](/windows/desktop/ProcThread/inheritance)。</span><span class="sxs-lookup"><span data-stu-id="edc38-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
