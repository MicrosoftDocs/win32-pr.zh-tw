---
description: 一般而言，如果您有單一執行緒的單元 (STA) ，就不需要同步處理，因為該單元會為您提供同步處理。
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: COM + 同步處理概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689116"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="ac9bb-103">COM + 同步處理概念</span><span class="sxs-lookup"><span data-stu-id="ac9bb-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="ac9bb-104">一般而言，如果您有單一執行緒的單元 (STA) ，就不需要同步處理，因為該單元會為您提供同步處理。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="ac9bb-105">當您有多執行緒單元 (MTA) 和無限制執行緒物件時，同步處理就會變得很重要。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="ac9bb-106">在過去，無限制執行緒物件必須處理鎖定。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="ac9bb-107">您可以藉由設定元件的同步處理屬性，來消除使用鎖定的需求。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="ac9bb-108">同步處理具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ac9bb-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="ac9bb-109">允許一個呼叫者一次輸入元件。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="ac9bb-110">禁止跨進程或跨電腦的流程。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="ac9bb-111">流程中的元件至元件。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="ac9bb-112">允許來自相同呼叫端的重新進入。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="ac9bb-113">不同于單元，活動會跨越多個進程和主機的內容。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="ac9bb-114">同步處理會決定哪個活動會包含物件。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="ac9bb-115">物件可以位於下列任何活動中：</span><span class="sxs-lookup"><span data-stu-id="ac9bb-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="ac9bb-116">Creator 的活動</span><span class="sxs-lookup"><span data-stu-id="ac9bb-116">Creator's activity</span></span>
-   <span data-ttu-id="ac9bb-117">新增活動</span><span class="sxs-lookup"><span data-stu-id="ac9bb-117">New activity</span></span>
-   <span data-ttu-id="ac9bb-118">沒有活動</span><span class="sxs-lookup"><span data-stu-id="ac9bb-118">No activity</span></span>

<span data-ttu-id="ac9bb-119">COM + 可針對每個活動的一連串鎖定來確保並行。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="ac9bb-120">如果呼叫端嘗試輸入已由另一個呼叫者使用的 COM + 同步處理元件，呼叫會被封鎖直到釋放鎖定為止。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="ac9bb-121">此封鎖行為不會有時間，而且無法設定為超時。如果鎖定未在使用中，則會取得鎖定並處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="ac9bb-122">完成之後，就會釋放鎖定給下一個呼叫者。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="ac9bb-123">為了防止鎖死，COM + 會透過整個網路中連結的一連串呼叫來管理跨活動的所有物件存取。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="ac9bb-124">COM + 提供下列同步處理設定：</span><span class="sxs-lookup"><span data-stu-id="ac9bb-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="ac9bb-125">Disabled</span><span class="sxs-lookup"><span data-stu-id="ac9bb-125">Disabled</span></span>
-   <span data-ttu-id="ac9bb-126">不支援</span><span class="sxs-lookup"><span data-stu-id="ac9bb-126">Not Supported</span></span>
-   <span data-ttu-id="ac9bb-127">支援</span><span class="sxs-lookup"><span data-stu-id="ac9bb-127">Supported</span></span>
-   <span data-ttu-id="ac9bb-128">必要</span><span class="sxs-lookup"><span data-stu-id="ac9bb-128">Required</span></span>
-   <span data-ttu-id="ac9bb-129">必須是新交易</span><span class="sxs-lookup"><span data-stu-id="ac9bb-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="ac9bb-130">某些同步處理設定會與其他 COM + 元件設定一起使用。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="ac9bb-131">例如，如果已啟用 [Com + 及時 (JIT) ](com--just-in-time-activation.md) 啟用服務，則需要同步處理。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="ac9bb-132">如果您啟用交易，則需要 JIT;因此，COM + [交易處理](com--transactions.md) 也需要進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="ac9bb-133">因此，具有 JIT = True 設定的類別，也必須設定為 [同步] = [必要] 或 [同步處理 = RequiresNew]。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="ac9bb-134">如需使用 [元件服務] 系統管理工具設定同步處理選項的指示，請參閱 [設定同步處理屬性](setting-the-synchronization-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="ac9bb-135">若要取得有關使用 COM + 管理程式庫來設定同步處理選項的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md)。</span><span class="sxs-lookup"><span data-stu-id="ac9bb-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac9bb-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac9bb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac9bb-137">COM + 同步處理工作</span><span class="sxs-lookup"><span data-stu-id="ac9bb-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



