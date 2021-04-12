---
description: 應用程式回收可以針對已知問題提供快速修正，以大幅提高 COM + 應用程式的整體穩定性，並協助防止非預期的問題。
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: COM + 應用程式回收概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab37376ff3bc6d03f454f63822641ed69fad0b47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385904"
---
# <a name="com-application-recycling-concepts"></a><span data-ttu-id="9972e-103">COM + 應用程式回收概念</span><span class="sxs-lookup"><span data-stu-id="9972e-103">COM+ Application Recycling Concepts</span></span>

<span data-ttu-id="9972e-104">應用程式回收可以針對已知問題提供快速修正，以大幅提高 COM + 應用程式的整體穩定性，並協助防止非預期的問題。</span><span class="sxs-lookup"><span data-stu-id="9972e-104">Application recycling can significantly increase the overall stability of your COM+ applications by offering a quick fix for known problems and helping to protect against unexpected ones.</span></span> <span data-ttu-id="9972e-105">例如，應用程式效能可能會因為問題（例如記憶體流失、nonscalable 資源使用量和進程失敗）而降級。</span><span class="sxs-lookup"><span data-stu-id="9972e-105">For example, application performance can degrade over time because of problems such as memory leaks, nonscalable resource usage, and process failure.</span></span> <span data-ttu-id="9972e-106">COM + 會提供應用程式回收，作為這些問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="9972e-106">COM+ provides application recycling as a solution to these problems.</span></span> <span data-ttu-id="9972e-107">您可以使用應用程式回收來自動關閉進程並重新啟動，進而重新初始化失敗的程式並重新配置其使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9972e-107">You can use application recycling to automatically shut down a process and restart it, thus reinitializing a failing process and reallocating memory it uses.</span></span>

<span data-ttu-id="9972e-108">應用程式回收的運作方式是建立與應用程式相關聯的 Dllhost.exe 進程複本。</span><span class="sxs-lookup"><span data-stu-id="9972e-108">Application recycling works by creating a duplicate of the Dllhost process associated with an application.</span></span> <span data-ttu-id="9972e-109">這種重複的 Dllhost.exe 程式會提供未來所有物件要求的服務，讓舊的 Dllhost.exe 完成服務剩餘的物件要求。</span><span class="sxs-lookup"><span data-stu-id="9972e-109">This duplicate Dllhost process services all future object requests, which leaves the old Dllhost to finish servicing the remaining object requests.</span></span> <span data-ttu-id="9972e-110">當舊的 Dllhost.exe 進程偵測到進程中物件的所有外部參考，或達到到期超時值時，就會關閉。</span><span class="sxs-lookup"><span data-stu-id="9972e-110">The old Dllhost process is shut down when it detects the release of all external references to objects in the process or when the expiration time-out value is reached.</span></span> <span data-ttu-id="9972e-111">透過此行為，應用程式回收可確保用戶端應用程式不會遇到服務中斷。</span><span class="sxs-lookup"><span data-stu-id="9972e-111">Through this behavior, application recycling ensures that a client application does not experience a service interruption.</span></span>

> [!Note]  
> <span data-ttu-id="9972e-112">您無法回收已設定為以 Windows 服務形式執行的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9972e-112">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="9972e-113">此外，程式庫應用程式具有其主機進程的回收和共用屬性。</span><span class="sxs-lookup"><span data-stu-id="9972e-113">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="9972e-114">您可以使用 [元件服務] 系統管理工具，或透過 COM + 系統管理 SDK，以程式設計方式設定應用程式回收。</span><span class="sxs-lookup"><span data-stu-id="9972e-114">You can configure application recycling administratively, by using the Component Services administrative tool, or programmatically, through the COM+ Administrative SDK.</span></span> <span data-ttu-id="9972e-115">您可以根據 [**應用程式**](applications.md)集合中 [**COMAdminCatalogObject**](comadmincatalogobject.md)物件的下列屬性，以數個準則來回收進程：</span><span class="sxs-lookup"><span data-stu-id="9972e-115">You can recycle processes based on several criteria, determined by the following properties of a [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection:</span></span>

-   <span data-ttu-id="9972e-116">**RecycleLifetimeLimit.**</span><span class="sxs-lookup"><span data-stu-id="9972e-116">**RecycleLifetimeLimit.**</span></span> <span data-ttu-id="9972e-117">進程回收之前可執行檔最大分鐘數。</span><span class="sxs-lookup"><span data-stu-id="9972e-117">The maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="9972e-118">有效範圍是從0到30240分鐘 (21 天) 。</span><span class="sxs-lookup"><span data-stu-id="9972e-118">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="9972e-119">預設分鐘數為0，表示進程不會回收達到存留期限制。</span><span class="sxs-lookup"><span data-stu-id="9972e-119">The default number of minutes is 0, which indicates that the process will not recycle from reaching a lifetime limit.</span></span>
-   <span data-ttu-id="9972e-120">**RecycleMemoryLimit.**</span><span class="sxs-lookup"><span data-stu-id="9972e-120">**RecycleMemoryLimit.**</span></span> <span data-ttu-id="9972e-121">在回收進程之前，進程記憶體使用量的最大數量 (以 kb) 。</span><span class="sxs-lookup"><span data-stu-id="9972e-121">The maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="9972e-122">如果進程記憶體使用量超過指定的數目超過一分鐘，則會回收進程。</span><span class="sxs-lookup"><span data-stu-id="9972e-122">If the process memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="9972e-123">有效範圍是0到 1048576 KB。</span><span class="sxs-lookup"><span data-stu-id="9972e-123">The valid range is 0 through 1,048,576 KB.</span></span> <span data-ttu-id="9972e-124">預設的記憶體使用量數量為 0 KB，表示進程將不會從達到記憶體限制時回收。</span><span class="sxs-lookup"><span data-stu-id="9972e-124">The default amount of memory usage is 0 KB, which indicates that the process will not recycle from reaching a memory limit.</span></span>
-   <span data-ttu-id="9972e-125">**RecycleCallLimit.**</span><span class="sxs-lookup"><span data-stu-id="9972e-125">**RecycleCallLimit.**</span></span> <span data-ttu-id="9972e-126">應用程式物件在回收進程之前可以接受的呼叫數上限。</span><span class="sxs-lookup"><span data-stu-id="9972e-126">The maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="9972e-127">有效範圍是從0到1048576的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9972e-127">The valid range is 0 through 1,048,576 calls.</span></span> <span data-ttu-id="9972e-128">預設的呼叫次數是0，表示進程不會從達到通話限制的情況下回收。</span><span class="sxs-lookup"><span data-stu-id="9972e-128">The default number of calls is 0, which indicates that the process will not recycle from reaching a call limit.</span></span>
-   <span data-ttu-id="9972e-129">**RecycleActivationLimit.**</span><span class="sxs-lookup"><span data-stu-id="9972e-129">**RecycleActivationLimit.**</span></span> <span data-ttu-id="9972e-130">回收進程之前，要接受的應用程式物件啟用數目上限。</span><span class="sxs-lookup"><span data-stu-id="9972e-130">The maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="9972e-131">有效範圍是0到1048576的啟用。</span><span class="sxs-lookup"><span data-stu-id="9972e-131">The valid range is 0 through 1,048,576 activations.</span></span> <span data-ttu-id="9972e-132">預設啟用數目為0，表示處理常式將不會從達到啟用限制時回收。</span><span class="sxs-lookup"><span data-stu-id="9972e-132">The default number of activations is 0, which indicates that the process will not recycle from reaching an activation limit.</span></span>

<span data-ttu-id="9972e-133">此外，也會使用 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件的 RecycleExpirationTimeout 屬性來強制關閉回收進程。</span><span class="sxs-lookup"><span data-stu-id="9972e-133">Additionally, the RecycleExpirationTimeout property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object is used to force the shutdown of a recycled process.</span></span> <span data-ttu-id="9972e-134">它會指出在強制關閉進程之前，要等候回收進程中物件之所有外部參考的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="9972e-134">It indicates the number of minutes to wait for the release of all external references to objects in the recycled process before forcibly shutting down the process.</span></span> <span data-ttu-id="9972e-135">有效範圍是從1到1440分鐘 (24 小時) ，而預設到期時間為15分鐘。</span><span class="sxs-lookup"><span data-stu-id="9972e-135">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="9972e-136">只有當已根據其他條件決定將回收處理程序時，才會使用此值。</span><span class="sxs-lookup"><span data-stu-id="9972e-136">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>

<span data-ttu-id="9972e-137">您可以選取一個以上的準則來回收應用程式。</span><span class="sxs-lookup"><span data-stu-id="9972e-137">You can select more than one criterion for recycling an application.</span></span> <span data-ttu-id="9972e-138">在滿足第一組準則之後，COM + 會回收應用程式。</span><span class="sxs-lookup"><span data-stu-id="9972e-138">COM+ recycles the application after the first of the set of criteria is satisfied.</span></span> <span data-ttu-id="9972e-139">您可以設定到期的到期時間值，以決定在強制關機之前，舊的 Dllhost.exe 進程可以花在完成剩餘服務要求的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9972e-139">You can set the expiration time-out value to determine how long an old Dllhost process can spend completing remaining service requests before being forcibly shut down.</span></span>

<span data-ttu-id="9972e-140">[**ApplicationInstances**](applicationinstances.md)集合提供 HasRecycled 屬性，此屬性可讓您判斷應用程式是否曾經被回收。</span><span class="sxs-lookup"><span data-stu-id="9972e-140">The [**ApplicationInstances**](applicationinstances.md) collection provides the HasRecycled property, which provides a way to determine whether the application has ever been recycled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9972e-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="9972e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9972e-142">COM + 應用程式回收工作</span><span class="sxs-lookup"><span data-stu-id="9972e-142">COM+ Application Recycling Tasks</span></span>](com--application-recycling-tasks.md)
</dt> <dt>

[<span data-ttu-id="9972e-143">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="9972e-143">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



