---
description: 分配器管理員會提供資源機的資源集區，並確保資源配置器所提供的資源已正確地登記在應用程式物件交易中。
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: COM + 分配管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510556"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="41c90-103">COM + 分配管理員</span><span class="sxs-lookup"><span data-stu-id="41c90-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="41c90-104">分配器管理員會提供資源機的資源集區，並確保資源配置器所提供的資源已正確地登記在應用程式物件的交易中。</span><span class="sxs-lookup"><span data-stu-id="41c90-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="41c90-105">分配器管理員會自動回收在物件存留期結束時仍保留的資源，以避免資源「流失」的可能性。</span><span class="sxs-lookup"><span data-stu-id="41c90-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="41c90-106">分配者管理員可以要求資源配置者建立新的資源，或在需要調整清查層級時終結閒置資源，而不是使用靜態設定。</span><span class="sxs-lookup"><span data-stu-id="41c90-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="41c90-107">由於公開給應用程式的資源配置器介面不需要是 COM 介面，因此可以在進程中使用分配者管理員，而不需要初始化 COM，例如，以支援 ODBC 資源配置器。</span><span class="sxs-lookup"><span data-stu-id="41c90-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="41c90-108">建立資源時，資源配置器可能會指定閒置資源在損毀之前，要保留在集區中的時間長度。</span><span class="sxs-lookup"><span data-stu-id="41c90-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="41c90-109">在分配器管理員中執行的執行緒一律會尋找這些閒置資源。</span><span class="sxs-lookup"><span data-stu-id="41c90-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="41c90-110">清查統計資料管理員</span><span class="sxs-lookup"><span data-stu-id="41c90-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="41c90-111">分配器管理員會使用 *清查統計資料管理員* 來管理集區資源清查層級。</span><span class="sxs-lookup"><span data-stu-id="41c90-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="41c90-112">清查統計資料管理員會維護每個資源使用時間的記錄，並在未使用 *x* 秒時移除清查中的資源，其中會在建立資源時為每個資源設定 *x* 的值。</span><span class="sxs-lookup"><span data-stu-id="41c90-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="41c90-113">持有者元件</span><span class="sxs-lookup"><span data-stu-id="41c90-113">The Holder Component</span></span>

<span data-ttu-id="41c90-114">分配器管理員會輪詢每個 *持有者*，這是一個由分配管理程式所建立的元件，每隔10秒就會列出每個資源配置器的資源清查，讓它能夠重新調整其資源清查。</span><span class="sxs-lookup"><span data-stu-id="41c90-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="41c90-115">每個持有者都會呼叫清查統計資料管理員，以建議每種資源類型的清查層級。</span><span class="sxs-lookup"><span data-stu-id="41c90-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="41c90-116">如此一來，持有者可能會要求資源配置器建立或損毀某些清查。</span><span class="sxs-lookup"><span data-stu-id="41c90-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="41c90-117">持有者和資源配置器會與特定類型的要求資源進行通訊。</span><span class="sxs-lookup"><span data-stu-id="41c90-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="41c90-118">持有者與資源配置器之間存在下列關聯性：</span><span class="sxs-lookup"><span data-stu-id="41c90-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="41c90-119">持有者可以從資源配置器要求資源。</span><span class="sxs-lookup"><span data-stu-id="41c90-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="41c90-120">資源配置器會傳回可用的資源，或建立一個新資源。</span><span class="sxs-lookup"><span data-stu-id="41c90-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="41c90-121">持有者可以通知資源配置器，應用程式不再需要資源，然後將它傳回資源集區。</span><span class="sxs-lookup"><span data-stu-id="41c90-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="41c90-122">持有者和資源配置器會一起運作，以維護資源集區的大小。</span><span class="sxs-lookup"><span data-stu-id="41c90-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41c90-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="41c90-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c90-124">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="41c90-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



