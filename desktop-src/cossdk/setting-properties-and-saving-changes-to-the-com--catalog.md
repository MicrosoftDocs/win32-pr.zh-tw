---
description: 集合中的每個專案都會公開屬性。
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: 編輯 COM + 目錄中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688815"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="de03c-103">編輯 COM + 目錄中的屬性</span><span class="sxs-lookup"><span data-stu-id="de03c-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="de03c-104">集合中的每個專案都會公開屬性。</span><span class="sxs-lookup"><span data-stu-id="de03c-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="de03c-105">這些屬性可保存專案所代表之任何元素的設定資料。</span><span class="sxs-lookup"><span data-stu-id="de03c-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="de03c-106">在 [元件服務] 系統管理工具中，這些屬性會出現在您透過以滑鼠右鍵按一下資料夾中的專案來存取的屬性頁面上。</span><span class="sxs-lookup"><span data-stu-id="de03c-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="de03c-107">因為指定集合中的專案全都代表相同類型，所以這些專案會公開一組在集合中一致的屬性。</span><span class="sxs-lookup"><span data-stu-id="de03c-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="de03c-108">例如， [**應用程式**](applications.md) 集合會公開 Name 屬性、AppID 屬性等等。</span><span class="sxs-lookup"><span data-stu-id="de03c-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="de03c-109">這類似于「元件服務」系統管理工具中的每個應用程式如何使用一致的結構化屬性頁面。</span><span class="sxs-lookup"><span data-stu-id="de03c-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="de03c-110">如需 **應用程式** 集合可用的屬性清單，請參閱 **應用程式**。</span><span class="sxs-lookup"><span data-stu-id="de03c-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="de03c-111">如需 [**元件**](components.md) 集合可用的屬性清單，請參閱 **元件**。</span><span class="sxs-lookup"><span data-stu-id="de03c-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="de03c-112">如需每個集合中的專案所公開之屬性的完整清單，請參閱 [Com + 系統管理集合](com--administration-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="de03c-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="de03c-113">您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件，表示集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="de03c-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="de03c-114">這個物件可讓您設定和取得專案所公開的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="de03c-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="de03c-115">設定屬性時，您也可能會將其他寫入器與 COM + 類別目錄進行爭用。</span><span class="sxs-lookup"><span data-stu-id="de03c-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="de03c-116">如需詳細資訊，請參閱 [取得和設定屬性](getting-and-setting-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="de03c-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="de03c-117">設定屬性之後，在您明確儲存變更之前，不會實際認可任何變更。</span><span class="sxs-lookup"><span data-stu-id="de03c-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="de03c-118">如需詳細資訊，請參閱 [儲存或捨棄變更](saving-or-discarding-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="de03c-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="de03c-119">當您儲存變更時，COM + 類別目錄會強制執行一些設定邏輯，以確保您不會將某些專案設定為不相容的設定。</span><span class="sxs-lookup"><span data-stu-id="de03c-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="de03c-120">當您明確變更某些其他屬性時，它也會變更某些屬性。</span><span class="sxs-lookup"><span data-stu-id="de03c-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="de03c-121">如需詳細資訊，請參閱 [屬性之間的相互相關性](interdependencies-between-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="de03c-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="de03c-122">此外，COM + 也有一項功能，可讓您以動態方式查詢以查看指定集合中的專案可使用哪些屬性。</span><span class="sxs-lookup"><span data-stu-id="de03c-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="de03c-123">如需詳細資訊，請參閱 [查詢可用的屬性](querying-for-available-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="de03c-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de03c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="de03c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de03c-125">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="de03c-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="de03c-126">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="de03c-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="de03c-127">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="de03c-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="de03c-128">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="de03c-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="de03c-129">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="de03c-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



