---
description: 流覽 COM + 集合階層
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: 流覽 COM + 集合階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973162"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="da0c0-103">流覽 COM + 集合階層</span><span class="sxs-lookup"><span data-stu-id="da0c0-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="da0c0-104">您可以使用 [**COMAdminCatalog**](comadmincatalog.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，輕鬆地取得某些集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="da0c0-105">這個方法會抓取「最上層」集合;也就是 [**應用程式**](applications.md)之類的集合，它本身就是唯一的，而且不會以邏輯方式建立小計另一個集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="da0c0-106">但是，許多集合都是以邏輯方式建立小計在另一個集合之下，因為它們包含屬於某些較大結構的元素。</span><span class="sxs-lookup"><span data-stu-id="da0c0-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="da0c0-107">例如， [**元件**](components.md) 集合是建立小計或相關的 [**應用程式**](applications.md) 集合，因為它包含特定 com + 應用程式中所安裝的元件，而該元件本身會對應到 **應用程式** 集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="da0c0-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="da0c0-108">相關的集合（例如這不是唯一的）;每個不同的應用程式都有一個 **元件** 集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="da0c0-109">因此，集合會以階層式結構排列，並自然地對應到它們所包含的專案之間的邏輯關聯性。</span><span class="sxs-lookup"><span data-stu-id="da0c0-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="da0c0-110">集合階層的圖表可在 [Com + 系統管理集合](com--administration-collections.md)中找到。</span><span class="sxs-lookup"><span data-stu-id="da0c0-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="da0c0-111">針對您想要使用 COMAdmin 物件設定的許多元素，您需要流覽集合階層的某些部分，以取得適當的專案。</span><span class="sxs-lookup"><span data-stu-id="da0c0-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="da0c0-112">這表示實務上，如果您想要取得相關集合中的專案，您必須先完成所有必要的較高層級歸類集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="da0c0-113">若要抓取相關的集合，您需要在父集合中取出與子集合相關的特定專案。</span><span class="sxs-lookup"><span data-stu-id="da0c0-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="da0c0-114">例如，如果您想要設定對應至特定 COM + 應用程式中某個元件的專案，您必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="da0c0-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="da0c0-115">取得 [**應用程式**](applications.md) 集合，並填入。</span><span class="sxs-lookup"><span data-stu-id="da0c0-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="da0c0-116">列舉 [**應用程式**](applications.md) 集合的內容，直到到達對應至正確 com + 應用程式的專案為止。</span><span class="sxs-lookup"><span data-stu-id="da0c0-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="da0c0-117">取得並填入該特定 COM + 應用程式的 [**元件**](components.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="da0c0-118">列舉 [**元件**](components.md) 集合的內容，直到到達對應至正確元件的專案為止。</span><span class="sxs-lookup"><span data-stu-id="da0c0-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="da0c0-119">下列 Microsoft Visual Basic 範例顯示如何執行上述步驟：</span><span class="sxs-lookup"><span data-stu-id="da0c0-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="da0c0-120">上述範例中使用兩個不同的 **>getcollection** 方法。</span><span class="sxs-lookup"><span data-stu-id="da0c0-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="da0c0-121">第一個是由 [**COMAdminCatalog**](comadmincatalog.md) 所公開，用來取得最上層的集合，在此案例中為「應用程式」。</span><span class="sxs-lookup"><span data-stu-id="da0c0-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="da0c0-122">第二個是由 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 所公開，用來取得與目前集合相關的集合;您可以藉由傳遞名稱 "Components" 和父物件的索引鍵屬性值，精確地指出您想要的集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="da0c0-123">索引鍵屬性值通常是可唯一識別物件的名稱或 GUID。此值會在每個集合的檔中識別。</span><span class="sxs-lookup"><span data-stu-id="da0c0-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="da0c0-124">在最常見的情況下，您必須在收集您想要的集合之前，以反復方式取得集合階層的相關集合。</span><span class="sxs-lookup"><span data-stu-id="da0c0-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="da0c0-125">您所採取的步驟會重複執行相同的一般模型。</span><span class="sxs-lookup"><span data-stu-id="da0c0-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="da0c0-126">如需完整的集合清單，請參閱 [Com + 系統管理集合](com--administration-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="da0c0-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="da0c0-127">在某些情況下，您可能會想要在第二次於收集階層的路徑後面使用快捷方式方法。</span><span class="sxs-lookup"><span data-stu-id="da0c0-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="da0c0-128">只有在您已經快取所有中間的索引鍵值之後，才可以使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="da0c0-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="da0c0-129">如需詳細資訊，請參閱 [**ICOMAdminCatalog：： GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery)。</span><span class="sxs-lookup"><span data-stu-id="da0c0-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da0c0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="da0c0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0c0-131">填入 COM + 集合</span><span class="sxs-lookup"><span data-stu-id="da0c0-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="da0c0-132">查詢可用的相關集合</span><span class="sxs-lookup"><span data-stu-id="da0c0-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="da0c0-133">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="da0c0-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



