---
description: 填入 COM + 集合
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: 填入 COM + 集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317876"
---
# <a name="populating-com-collections"></a><span data-ttu-id="de320-103">填入 COM + 集合</span><span class="sxs-lookup"><span data-stu-id="de320-103">Populating COM+ Collections</span></span>

<span data-ttu-id="de320-104">在您抓取集合之後，且您可以直接使用其包含的專案之前，您必須使用 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) 方法填入集合。</span><span class="sxs-lookup"><span data-stu-id="de320-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="de320-105">這會從 COM + 目錄中提取集合內容的資料。</span><span class="sxs-lookup"><span data-stu-id="de320-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="de320-106">請務必瞭解，每當您使用 COMAdmin 物件來操作集合中的專案或資料時，您實際上是在暫時快取的資料。您無法直接使用保存的目錄。</span><span class="sxs-lookup"><span data-stu-id="de320-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="de320-107">您對集合或其任何專案所做的任何動作都會反映在目錄上，直到您在集合上呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 為止。</span><span class="sxs-lookup"><span data-stu-id="de320-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="de320-108">如需詳細資訊，請參閱 [儲存或捨棄變更](saving-or-discarding-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="de320-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="de320-109">在呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，任何後續要 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)的呼叫，都有會將暫止的變更捨棄到集合中所有專案的效果。</span><span class="sxs-lookup"><span data-stu-id="de320-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="de320-110">**填入** 時，一律會填入您正在使用的快取，並在基礎目錄資料存放區上保存任何資料。</span><span class="sxs-lookup"><span data-stu-id="de320-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de320-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="de320-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de320-112">流覽 COM + 集合階層</span><span class="sxs-lookup"><span data-stu-id="de320-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="de320-113">查詢可用的相關集合</span><span class="sxs-lookup"><span data-stu-id="de320-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="de320-114">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="de320-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



