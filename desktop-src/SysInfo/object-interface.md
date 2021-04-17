---
description: Windows 所提供的函式會執行下列工作：
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: 物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469209"
---
# <a name="object-interface"></a><span data-ttu-id="dd3b8-103">物件介面</span><span class="sxs-lookup"><span data-stu-id="dd3b8-103">Object Interface</span></span>

<span data-ttu-id="dd3b8-104">Windows 所提供的函式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="dd3b8-104">Windows provides functions that perform the following tasks:</span></span>

-   <span data-ttu-id="dd3b8-105">建立物件</span><span class="sxs-lookup"><span data-stu-id="dd3b8-105">Create an object</span></span>
-   <span data-ttu-id="dd3b8-106">取得物件控制碼</span><span class="sxs-lookup"><span data-stu-id="dd3b8-106">Get an object handle</span></span>
-   <span data-ttu-id="dd3b8-107">取得物件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="dd3b8-107">Get information about the object</span></span>
-   <span data-ttu-id="dd3b8-108">設定物件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="dd3b8-108">Set information about the object</span></span>
-   <span data-ttu-id="dd3b8-109">關閉物件控制碼</span><span class="sxs-lookup"><span data-stu-id="dd3b8-109">Close the object handle</span></span>
-   <span data-ttu-id="dd3b8-110">終結物件</span><span class="sxs-lookup"><span data-stu-id="dd3b8-110">Destroy the object</span></span>

<span data-ttu-id="dd3b8-111">每個物件都不需要這些工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-111">Some of these tasks are not necessary for each object.</span></span> <span data-ttu-id="dd3b8-112">某些工作會針對某些物件合併。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-112">Some of these tasks are combined for certain objects.</span></span> <span data-ttu-id="dd3b8-113">例如，應用程式可以建立事件物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-113">For example, an application can create an event object.</span></span> <span data-ttu-id="dd3b8-114">其他應用程式可以開啟事件，以取得此事件物件的唯一控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-114">Other applications can open the event to obtain a unique handle to this event object.</span></span> <span data-ttu-id="dd3b8-115">當每個應用程式使用事件完成時，它會關閉其對物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-115">As each application finishes using the event, it closes its handle to the object.</span></span> <span data-ttu-id="dd3b8-116">當事件物件沒有剩餘的開啟控制碼時，系統會終結事件物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-116">When there are no remaining open handles to the event object, the system destroys the event object.</span></span> <span data-ttu-id="dd3b8-117">相反地，應用程式可以取得現有視窗物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-117">In contrast, an application can obtain a handle to an existing window object.</span></span> <span data-ttu-id="dd3b8-118">當不再需要視窗物件時，應用程式必須終結物件，使視窗控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-118">When the window object is no longer needed, the application must destroy the object, which invalidates the window handle.</span></span>

<span data-ttu-id="dd3b8-119">有時候，在所有物件控制碼都關閉之後，物件仍會保留在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-119">Occasionally, an object remains in memory after all object handles have been closed.</span></span> <span data-ttu-id="dd3b8-120">例如，執行緒可以建立事件物件，並等候事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-120">For example, a thread could create an event object and wait on the event handle.</span></span> <span data-ttu-id="dd3b8-121">當執行緒正在等候時，另一個執行緒可以關閉相同的事件物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-121">While the thread is waiting, another thread could close the same event object handle.</span></span> <span data-ttu-id="dd3b8-122">事件物件會保留在記憶體中（沒有任何事件物件控制碼），直到事件物件設定為信號狀態且等候作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-122">The event object remains in memory, without any event object handles, until the event object is set to the signaled state and the wait operation is completed.</span></span> <span data-ttu-id="dd3b8-123">此時，系統會從記憶體中移除物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-123">At this time, the system removes the object from memory.</span></span>

<span data-ttu-id="dd3b8-124">控制碼和物件會耗用記憶體。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-124">Handles and objects consume memory.</span></span> <span data-ttu-id="dd3b8-125">因此，若要保留系統效能，您應該在不再需要時立即關閉控制碼和刪除物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-125">Therefore, to preserve system performance, you should close handles and delete objects as soon as they are no longer needed.</span></span> <span data-ttu-id="dd3b8-126">如果您沒有這樣做，您的應用程式可能會因為分頁檔過度使用而造成系統效能傷害。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-126">If you do not do this, your application can hurt system performance, due to excessive use of the paging file.</span></span>

<span data-ttu-id="dd3b8-127">當進程結束時，系統會自動關閉處理常式，並刪除進程所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-127">When a process terminates, the system automatically closes handles and deletes objects created by the process.</span></span> <span data-ttu-id="dd3b8-128">但是，當執行緒終止時，系統通常不會關閉控制碼或刪除物件。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-128">However, when a thread terminates, the system usually does not close handles or delete objects.</span></span> <span data-ttu-id="dd3b8-129">唯一的例外是視窗、攔截、視窗位置和動態資料交換 (DDE) 交談物件;當建立執行緒終止時，這些物件會遭到終結。</span><span class="sxs-lookup"><span data-stu-id="dd3b8-129">The only exceptions are window, hook, window position, and dynamic data exchange (DDE) conversation objects; these objects are destroyed when the creating thread terminates.</span></span>

 

 



