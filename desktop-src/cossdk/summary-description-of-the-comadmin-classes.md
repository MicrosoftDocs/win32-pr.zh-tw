---
description: COMAdmin 程式庫提供三個類別 (comadmin.dll) ，其中每個類別都會執行 COM 雙重介面。
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: COMAdmin 類別的摘要描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971954"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="cc50f-103">COMAdmin 類別的摘要描述</span><span class="sxs-lookup"><span data-stu-id="cc50f-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="cc50f-104">COMAdmin 程式庫提供三個類別 (comadmin.dll) ，其中每個類別都會執行 COM 雙重介面。</span><span class="sxs-lookup"><span data-stu-id="cc50f-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="cc50f-105">您可以使用從這些類別建立的物件來取得目錄的存取權，以表示目錄中的集合，以及代表集合中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="cc50f-106">COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="cc50f-106">COMAdminCatalog</span></span>

<span data-ttu-id="cc50f-107">[**COMAdminCatalog**](comadmincatalog.md)類別代表目錄本身。</span><span class="sxs-lookup"><span data-stu-id="cc50f-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="cc50f-108">從 **COMAdminCatalog** 建立的物件是您在程式設計管理中使用的基本物件。</span><span class="sxs-lookup"><span data-stu-id="cc50f-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="cc50f-109">除了在具現化時建立與目錄伺服器的基本連線， **COMAdminCatalog** 提供的方法可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="cc50f-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="cc50f-110">取得目錄的集合。</span><span class="sxs-lookup"><span data-stu-id="cc50f-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="cc50f-111">連接至遠端電腦上的目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="cc50f-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="cc50f-112">安裝、匯出、啟動、關閉，以及取得 COM + 應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc50f-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="cc50f-113">將元件安裝至 COM + 應用程式，並取得有關元件的資訊。</span><span class="sxs-lookup"><span data-stu-id="cc50f-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="cc50f-114">啟動、停止或重新整理電腦上正在執行的服務。</span><span class="sxs-lookup"><span data-stu-id="cc50f-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="cc50f-115">重新整理、還原或備份目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="cc50f-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="cc50f-116">在 COM + 1.0 中， [**COMAdminCatalog**](comadmincatalog.md) 類別會執行 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) 介面。</span><span class="sxs-lookup"><span data-stu-id="cc50f-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="cc50f-117">在 COM + 1.5 中， **COMAdminCatalog** 類別會將 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) 實作為其預設介面。</span><span class="sxs-lookup"><span data-stu-id="cc50f-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="cc50f-118">COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="cc50f-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="cc50f-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md)類別代表目錄中的任何集合，方法是在物件具現化時提供命名特定集合的字串。</span><span class="sxs-lookup"><span data-stu-id="cc50f-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="cc50f-120"> (可用的目錄集合會在 [Com + 系統管理集合](com--administration-collections.md)的資料表中命名。當您藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)物件的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法來抓取最上層集合時，會從這個類別建立 ) 物件。</span><span class="sxs-lookup"><span data-stu-id="cc50f-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="cc50f-121">藉由呼叫其父集合物件的 **>getcollection** 方法，以抓取子集合時，也會建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="cc50f-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="cc50f-122">**COMAdminCatalogCollection** 物件可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="cc50f-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="cc50f-123">列舉集合中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="cc50f-124">從集合中取出專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="cc50f-125">在集合中加入或移除專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="cc50f-126">儲存或捨棄對集合所做的任何暫止變更或其包含的專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="cc50f-127">取得目錄中不同的集合。</span><span class="sxs-lookup"><span data-stu-id="cc50f-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="cc50f-128">[**COMAdminCatalogObject**](comadmincatalogobject.md)類別會實 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)介面。</span><span class="sxs-lookup"><span data-stu-id="cc50f-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="cc50f-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="cc50f-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="cc50f-130">[**COMAdminCatalogObject**](comadmincatalogobject.md)類別代表集合中包含的任何專案。</span><span class="sxs-lookup"><span data-stu-id="cc50f-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="cc50f-131">當透過目錄集合物件的 [**item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) 屬性取得專案時，會從這個類別建立物件。</span><span class="sxs-lookup"><span data-stu-id="cc50f-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="cc50f-132">從 **COMAdminCatalogObject** 類別建立的物件可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="cc50f-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="cc50f-133">取得或設定物件用來表示之專案所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="cc50f-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="cc50f-134">取得專案及其屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc50f-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="cc50f-135">[**COMAdminCatalogObject**](comadmincatalogobject.md)類別會實 [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)介面。</span><span class="sxs-lookup"><span data-stu-id="cc50f-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc50f-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc50f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc50f-137">存取 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="cc50f-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="cc50f-138">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="cc50f-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



