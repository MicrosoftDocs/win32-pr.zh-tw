---
description: 在 COM + 類別目錄上取出集合
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: 在 COM + 類別目錄上取出集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688692"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="ec807-103">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="ec807-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="ec807-104">COM + 目錄中的資料會儲存在集合的階層中。</span><span class="sxs-lookup"><span data-stu-id="ec807-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="ec807-105">在 [元件服務] 系統管理工具中，其中許多集合會顯示為主控台樹中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ec807-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="ec807-106">未顯示為資料夾的集合只能以程式設計的方式存取。</span><span class="sxs-lookup"><span data-stu-id="ec807-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="ec807-107">集合可做為專案的容器。</span><span class="sxs-lookup"><span data-stu-id="ec807-107">Collections serve as containers for items.</span></span> <span data-ttu-id="ec807-108">指定集合中的專案都是一致的類型;也就是說，它們全都代表相同種類的元素，而且集合中可以有任意數目的專案。</span><span class="sxs-lookup"><span data-stu-id="ec807-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="ec807-109">例如， [**應用程式**](applications.md) 集合包含電腦上所安裝之每個 com + 應用程式的專案。</span><span class="sxs-lookup"><span data-stu-id="ec807-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="ec807-110">此集合會在系統管理工具中顯示為 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ec807-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="ec807-111">集合會以階層式結構的形式出現，因為它們所包含的專案會遵循固有的包含順序。</span><span class="sxs-lookup"><span data-stu-id="ec807-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="ec807-112">例如，因為元件是安裝在 COM + 應用程式中，所以 [**元件**](components.md) 集合會以邏輯方式在 [**應用程式**](applications.md) 集合下建立小計。</span><span class="sxs-lookup"><span data-stu-id="ec807-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="ec807-113">更特別的是，若要將安裝的元件存放至該特定應用程式，**應用程式** 集合中的每個專案都有一個不同的 **元件** 集合。</span><span class="sxs-lookup"><span data-stu-id="ec807-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="ec807-114">只要您想要取得專案並設定其屬性，您就必須在目錄上取得集合。</span><span class="sxs-lookup"><span data-stu-id="ec807-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="ec807-115">在一般情況下，您需要逐步執行數個集合，以取得您想要的專案。</span><span class="sxs-lookup"><span data-stu-id="ec807-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="ec807-116">如需執行此操作的程式，請參閱 [流覽 COM + 集合](navigating-the-com--collection-hierarchy.md)階層。</span><span class="sxs-lookup"><span data-stu-id="ec807-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="ec807-117">在您抓取集合，而且可以直接使用其包含的專案之前，您必須填入集合，以從 COM + 類別目錄提取集合內容的資料。</span><span class="sxs-lookup"><span data-stu-id="ec807-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="ec807-118">如需詳細資訊，請參閱填入 [COM + 集合](populating-com--collections.md)。</span><span class="sxs-lookup"><span data-stu-id="ec807-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="ec807-119">此外，您還可以使用此工具，以動態方式查詢以查看您所持有的指定集合中有哪些相關的集合可供使用。</span><span class="sxs-lookup"><span data-stu-id="ec807-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="ec807-120">如需詳細資訊，請參閱 [查詢可用的相關集合](querying-for-available-related-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="ec807-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec807-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec807-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec807-122">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="ec807-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="ec807-123">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="ec807-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="ec807-124">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="ec807-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="ec807-125">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="ec807-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="ec807-126">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="ec807-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



