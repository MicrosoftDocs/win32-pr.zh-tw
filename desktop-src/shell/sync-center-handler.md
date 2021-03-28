---
description: 本主題提供建立 DLL 檔案的逐步檢查需求，該檔案會執行處理常式以搭配同步中心使用。 這項資訊在 Windows Vista 中是有效的。
title: 開發 Windows 同步中心處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973272"
---
# <a name="developing-a-windows-sync-center-handler"></a><span data-ttu-id="8511d-104">開發 Windows 同步中心處理常式</span><span class="sxs-lookup"><span data-stu-id="8511d-104">Developing a Windows Sync Center Handler</span></span>

<span data-ttu-id="8511d-105">本主題提供建立 DLL 檔案的逐步檢查需求，該檔案會執行處理常式以搭配同步中心使用。</span><span class="sxs-lookup"><span data-stu-id="8511d-105">This topic provides a step-by-step examination of the requirements to build a DLL file that implements a handler to be used with Sync Center.</span></span> <span data-ttu-id="8511d-106">這項資訊在 Windows Vista 中是有效的。</span><span class="sxs-lookup"><span data-stu-id="8511d-106">This information is valid as of Windows Vista.</span></span>

-   [<span data-ttu-id="8511d-107">Vista 之前的 Windows 同步處理體驗</span><span class="sxs-lookup"><span data-stu-id="8511d-107">The Windows Synchronization Experience Before Vista</span></span>](#the-windows-synchronization-experience-before-vista)
-   [<span data-ttu-id="8511d-108">同步中心 Api</span><span class="sxs-lookup"><span data-stu-id="8511d-108">Sync Center APIs</span></span>](#sync-center-apis)
    -   [<span data-ttu-id="8511d-109">基本介面</span><span class="sxs-lookup"><span data-stu-id="8511d-109">Essential Interfaces</span></span>](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a><span data-ttu-id="8511d-110">Vista 之前的 Windows 同步處理體驗</span><span class="sxs-lookup"><span data-stu-id="8511d-110">The Windows Synchronization Experience Before Vista</span></span>

<span data-ttu-id="8511d-111">Windows XP 提供 [同步處理管理員](syncmgr-start-page.md) (mobsync.exe) 。</span><span class="sxs-lookup"><span data-stu-id="8511d-111">Windows XP provided a [Synchronization Manager](syncmgr-start-page.md) (mobsync.exe).</span></span> <span data-ttu-id="8511d-112">許多裝置（例如 mp3 播放機、行動電話和攝影機）也都提供自己的同步處理介面，而不是使用同步處理管理員。</span><span class="sxs-lookup"><span data-stu-id="8511d-112">Many devices such as mp3 players, cell phones, and cameras also provided their own synchronization interfaces rather than using the Synchronization Manager.</span></span> <span data-ttu-id="8511d-113">這會導致不一致且 noncentralized 的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="8511d-113">This resulted in an inconsistent and noncentralized user experience.</span></span>

<span data-ttu-id="8511d-114">Windows Vista 提供的新同步中心功能比舊版的同步處理管理員多了許多優點。</span><span class="sxs-lookup"><span data-stu-id="8511d-114">The new Sync Center feature provided in Windows Vista has several advantages over the older Synchronization Manager.</span></span>

-   <span data-ttu-id="8511d-115">更好的發現能力</span><span class="sxs-lookup"><span data-stu-id="8511d-115">Better discoverability</span></span>
-   <span data-ttu-id="8511d-116">不需要直接使用者動作</span><span class="sxs-lookup"><span data-stu-id="8511d-116">Less need for direct user action</span></span>
-   <span data-ttu-id="8511d-117">不會封鎖其他作業</span><span class="sxs-lookup"><span data-stu-id="8511d-117">Does not block other operations</span></span>
-   <span data-ttu-id="8511d-118">更好的同步處理進度視覺效果</span><span class="sxs-lookup"><span data-stu-id="8511d-118">Better visualization of the synchronization progress</span></span>
-   <span data-ttu-id="8511d-119">更容易瞭解開發模型</span><span class="sxs-lookup"><span data-stu-id="8511d-119">Easier to understand development model</span></span>

## <a name="sync-center-apis"></a><span data-ttu-id="8511d-120">同步中心 Api</span><span class="sxs-lookup"><span data-stu-id="8511d-120">Sync Center APIs</span></span>

<span data-ttu-id="8511d-121">同步中心會透過多個元件物件模型 (COM) 介面，與處理常式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8511d-121">Sync Center communicates with handlers through a number of Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="8511d-122">並非所有這些介面都需要執行同步中心處理常式。</span><span class="sxs-lookup"><span data-stu-id="8511d-122">Not all of these interfaces are needed to implement a Sync Center handler.</span></span> <span data-ttu-id="8511d-123">本主題分為兩個部分。</span><span class="sxs-lookup"><span data-stu-id="8511d-123">This topic has been broken into two sections.</span></span> <span data-ttu-id="8511d-124">第一節說明每個處理常式都必須支援的基本 COM 介面，而第二個區段會檢查選用的 COM 介面，並查看處理常式支援這些介面的原因。</span><span class="sxs-lookup"><span data-stu-id="8511d-124">The first section explains the essential COM interfaces that every handler must support, and the second section examines the optional COM interfaces and looks at the reasons that a handler would support them.</span></span>

-   [<span data-ttu-id="8511d-125">基本介面</span><span class="sxs-lookup"><span data-stu-id="8511d-125">Essential Interfaces</span></span>](#essential-interfaces)

### <a name="essential-interfaces"></a><span data-ttu-id="8511d-126">基本介面</span><span class="sxs-lookup"><span data-stu-id="8511d-126">Essential Interfaces</span></span>

<span data-ttu-id="8511d-127">所有同步中心處理常式都必須支援下列介面：</span><span class="sxs-lookup"><span data-stu-id="8511d-127">All Sync Center handlers must support the following interfaces:</span></span>

-   [<span data-ttu-id="8511d-128">**ISyncMgrHandler**</span><span class="sxs-lookup"><span data-stu-id="8511d-128">**ISyncMgrHandler**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [<span data-ttu-id="8511d-129">**ISyncMgrHandlerInfo**</span><span class="sxs-lookup"><span data-stu-id="8511d-129">**ISyncMgrHandlerInfo**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [<span data-ttu-id="8511d-130">**ISyncMgrSyncItemContainer**</span><span class="sxs-lookup"><span data-stu-id="8511d-130">**ISyncMgrSyncItemContainer**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [<span data-ttu-id="8511d-131">**IEnumSyncMgrSyncItems**</span><span class="sxs-lookup"><span data-stu-id="8511d-131">**IEnumSyncMgrSyncItems**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [<span data-ttu-id="8511d-132">**ISyncMgrSyncItem**</span><span class="sxs-lookup"><span data-stu-id="8511d-132">**ISyncMgrSyncItem**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [<span data-ttu-id="8511d-133">**ISyncMgrSyncItemInfo**</span><span class="sxs-lookup"><span data-stu-id="8511d-133">**ISyncMgrSyncItemInfo**</span></span>](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

<span data-ttu-id="8511d-134">[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) 和 [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) 是用來描述與同步中心同步處理相關的單一同步處理專案。</span><span class="sxs-lookup"><span data-stu-id="8511d-134">[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) and [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) are used to describe a single sync item involved in the synchronization to the Sync Center.</span></span> <span data-ttu-id="8511d-135">同步處理專案通常代表特定的資料類型 (例如) 的影像或特定位置的資料。</span><span class="sxs-lookup"><span data-stu-id="8511d-135">A sync item generally represents either a particular data type (such as images) or a particular location of data.</span></span>

<span data-ttu-id="8511d-136">代表不同資料位置的同步處理專案允許進行非常特定的同步處理。</span><span class="sxs-lookup"><span data-stu-id="8511d-136">Sync items that represent different data locations allow for very specific synchronizations.</span></span> <span data-ttu-id="8511d-137">位置的資料細微性是由處理常式作者所撰寫，但請小心設計。</span><span class="sxs-lookup"><span data-stu-id="8511d-137">The granularity of the location is up to the handler author, but care should be taken in the design.</span></span> <span data-ttu-id="8511d-138">如果)  (位置的同步處理專案太少，則會限制使用者只同步特定資料的能力。</span><span class="sxs-lookup"><span data-stu-id="8511d-138">If there are too few sync items (locations), then the user is restricted in their ability to sync only certain data.</span></span> <span data-ttu-id="8511d-139">另一方面，太多的資料細微性可能會變得難以管理。</span><span class="sxs-lookup"><span data-stu-id="8511d-139">At the other extreme, too much granularity can become unmanageable.</span></span>

<span data-ttu-id="8511d-140">如果處理常式支援一個以上的資料型別或多個資料位置，則需要支援一個以上的同步處理專案物件。</span><span class="sxs-lookup"><span data-stu-id="8511d-140">If a handler supports more than one data type or multiple data locations, then it needs to support more than one sync item object.</span></span> <span data-ttu-id="8511d-141">其中一個範例可能是 (PDA) 的個人資料助理，可讓使用者同步處理連絡人、行事曆專案和檔。</span><span class="sxs-lookup"><span data-stu-id="8511d-141">An example might be a personal data assistant (PDA) that allows the user to sync contacts, calendar items and documents.</span></span> <span data-ttu-id="8511d-142">這三種資料類型需要以三個唯一的物件來表示，而每個物件會公開 [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) 和 [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="8511d-142">These three data types would need to be represented by three unique objects that each expose the [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) and [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) interfaces.</span></span>

<span data-ttu-id="8511d-143">[**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)介面會提供一種機制，以列舉處理常式的同步處理專案。</span><span class="sxs-lookup"><span data-stu-id="8511d-143">The [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) interface provides a mechanism to enumerate through a handler's sync items.</span></span> <span data-ttu-id="8511d-144">為了取得此列舉值，同步中心會呼叫處理常式所公開的 [**ISyncMgrSyncItemContainer：： GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) 方法。</span><span class="sxs-lookup"><span data-stu-id="8511d-144">To retrieve this enumerator, Sync Center calls the [**ISyncMgrSyncItemContainer::GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) method exposed by the handler.</span></span> <span data-ttu-id="8511d-145">[**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) 也包含兩個其他方法，同步中心可以使用這些方法來取得處理常式同步處理專案的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="8511d-145">[**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) also contains two other methods that the Sync Center can use to retrieve information about the handler's sync items:</span></span>

-   <span data-ttu-id="8511d-146">[**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) 會傳回特定的同步處理專案。</span><span class="sxs-lookup"><span data-stu-id="8511d-146">[**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) returns a specific sync item.</span></span>
-   <span data-ttu-id="8511d-147">[**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) 會傳回處理常式所支援的同步處理專案數目。</span><span class="sxs-lookup"><span data-stu-id="8511d-147">[**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) returns the number of sync items supported by the handler.</span></span>

<span data-ttu-id="8511d-148">[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) 和 [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) 可用來描述處理常式的屬性，並啟動實際的同步處理。</span><span class="sxs-lookup"><span data-stu-id="8511d-148">[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) and [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) are used to describe the properties of the hander and launch the actual synchronization.</span></span> <span data-ttu-id="8511d-149">[**ISyncMgrHandler：： Synchronize：**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) 處理常式程式碼會執行同步處理，並提供進度的意見反應，以及任何發生的問題。</span><span class="sxs-lookup"><span data-stu-id="8511d-149">[**ISyncMgrHandler::Synchronize**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) is where the handler code carries out the synchronization and provides feedback on progress and any issues that occur.</span></span>

<span data-ttu-id="8511d-150">許多介面方法都不需要完全實作為。</span><span class="sxs-lookup"><span data-stu-id="8511d-150">Many of the interface methods do not need to be fully implemented.</span></span> <span data-ttu-id="8511d-151">同步中心提供特定數量的預設資訊。</span><span class="sxs-lookup"><span data-stu-id="8511d-151">Sync Center provides a certain amount of default information.</span></span> <span data-ttu-id="8511d-152">介面可讓處理常式覆寫此資訊，並視需要提供要顯示的自訂資訊。</span><span class="sxs-lookup"><span data-stu-id="8511d-152">The interfaces allow a handler to override this information and provide custom information to display, if needed.</span></span>

 

 



