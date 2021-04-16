---
description: 取得和設定屬性
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: '取得和設定 (元件服務的屬性) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468309"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="f764e-103">取得和設定 (元件服務的屬性) </span><span class="sxs-lookup"><span data-stu-id="f764e-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="f764e-104">您必須執行下列步驟，才能讀取或寫入集合中的專案所公開的特定屬性：</span><span class="sxs-lookup"><span data-stu-id="f764e-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="f764e-105">取得集合。</span><span class="sxs-lookup"><span data-stu-id="f764e-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="f764e-106">從 COM + 類別目錄填入集合，以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="f764e-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="f764e-107">取出集合中的特定專案，並以 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別中的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="f764e-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="f764e-108">如需說明這些步驟的範例，請參閱 [流覽 COM + 集合](navigating-the-com--collection-hierarchy.md)階層。</span><span class="sxs-lookup"><span data-stu-id="f764e-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="f764e-109">因為公開的特定屬性會根據專案代表的專案而有所不同;也就是說，代表元件的專案具有不同于一個代表 COM + 應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="f764e-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="f764e-110">在 [**COMAdminCatalogObject**](comadmincatalogobject.md)上使用單一泛型屬性（Value 屬性）設定這些屬性的任何一個。</span><span class="sxs-lookup"><span data-stu-id="f764e-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="f764e-111">Value 屬性可讓您取得或設定專案所公開的任何特定命名屬性，取得時傳回的命名屬性值，並在設定時使用名稱和值。</span><span class="sxs-lookup"><span data-stu-id="f764e-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="f764e-112">在使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)方法明確儲存變更之前，不會實際將任何變更記錄至 com + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="f764e-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="f764e-113">指定集合中所有專案上所有屬性的暫止變更都會一次儲存。</span><span class="sxs-lookup"><span data-stu-id="f764e-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="f764e-114">如需詳細資訊，請參閱 [儲存或捨棄變更](saving-or-discarding-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="f764e-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="f764e-115">並非您所做的所有變更都將被接受。</span><span class="sxs-lookup"><span data-stu-id="f764e-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="f764e-116">COM + 類別目錄會強制執行一些一致性邏輯，以確保您以合理的方式設定專案。</span><span class="sxs-lookup"><span data-stu-id="f764e-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="f764e-117">此外，當您變更某些屬性時，其他屬性可能會由相同的一致性邏輯自動變更。</span><span class="sxs-lookup"><span data-stu-id="f764e-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="f764e-118">當您嘗試儲存變更時，就會顯示這些效果。</span><span class="sxs-lookup"><span data-stu-id="f764e-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="f764e-119">您可能會與另一個寫入器對 COM + 類別目錄進行競爭。</span><span class="sxs-lookup"><span data-stu-id="f764e-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="f764e-120">在對指定集合進行 [**擴展和**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 的呼叫之間，不會鎖定目錄中的任何資料。</span><span class="sxs-lookup"><span data-stu-id="f764e-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="f764e-121">多個合作物件可以同時設定指定集合中的專案，而且可能會在儲存變更時進行爭用。</span><span class="sxs-lookup"><span data-stu-id="f764e-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="f764e-122">這表示，其他人可能會在您執行程式之前或之後變更物件的設定，不論是在本機或遠端使用 COMAdmin 物件或使用「元件服務」系統管理工具來執行。</span><span class="sxs-lookup"><span data-stu-id="f764e-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="f764e-123">在目錄上撰寫物件的一般規則是，物件上的所有屬性都會一次寫入。</span><span class="sxs-lookup"><span data-stu-id="f764e-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="f764e-124">也就是最後一個寫入器獲勝—物件會精確地儲存在目錄中，如同最後一個寫入器設定的一樣。</span><span class="sxs-lookup"><span data-stu-id="f764e-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f764e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f764e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f764e-126">屬性之間的相互相關性</span><span class="sxs-lookup"><span data-stu-id="f764e-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="f764e-127">查詢可用的屬性</span><span class="sxs-lookup"><span data-stu-id="f764e-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="f764e-128">儲存或捨棄變更</span><span class="sxs-lookup"><span data-stu-id="f764e-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



