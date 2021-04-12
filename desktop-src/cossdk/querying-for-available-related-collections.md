---
description: 查詢可用的相關集合
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: 查詢可用的相關集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317904"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="7fd64-103">查詢可用的相關集合</span><span class="sxs-lookup"><span data-stu-id="7fd64-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="7fd64-104">如果您撰寫的是一般用途的管理工具，您可能需要撰寫用來導覽整個集合階層的常式。</span><span class="sxs-lookup"><span data-stu-id="7fd64-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="7fd64-105">為了支援此功能，COM + 的功能可讓您以動態方式查詢任何指定集合中可用的相關集合。</span><span class="sxs-lookup"><span data-stu-id="7fd64-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="7fd64-106">[**RelatedCollectionInfo**](relatedcollectioninfo.md)集合可從任何您持有的集合中取得，而且每個可用的相關集合都包含一個專案。</span><span class="sxs-lookup"><span data-stu-id="7fd64-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="7fd64-107">您可以列舉這些專案，以判斷指定的集合是否可用。</span><span class="sxs-lookup"><span data-stu-id="7fd64-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="7fd64-108">您可以使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，從您持有的任何集合取得 [**RelatedCollectionInfo**](relatedcollectioninfo.md)集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7fd64-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fd64-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fd64-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd64-110">流覽 COM + 集合階層</span><span class="sxs-lookup"><span data-stu-id="7fd64-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="7fd64-111">填入 COM + 集合</span><span class="sxs-lookup"><span data-stu-id="7fd64-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="7fd64-112">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="7fd64-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



