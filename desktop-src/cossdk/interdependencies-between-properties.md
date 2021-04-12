---
description: 屬性之間的相互相關性
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: 屬性之間的相互相關性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936328"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="7986f-103">屬性之間的相互相關性</span><span class="sxs-lookup"><span data-stu-id="7986f-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="7986f-104">當您設定屬性時，COM + 類別目錄會強制執行一些一致性邏輯，以確保您以合理的方式設定元素。</span><span class="sxs-lookup"><span data-stu-id="7986f-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="7986f-105">此邏輯可以用兩種方式來執行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7986f-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="7986f-106">**依賴。**</span><span class="sxs-lookup"><span data-stu-id="7986f-106">**Dependencies.**</span></span> <span data-ttu-id="7986f-107">您可能會遭到封鎖而無法進行一些變更，因為另一個屬性相依于您嘗試設定之屬性的特定設定。</span><span class="sxs-lookup"><span data-stu-id="7986f-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="7986f-108">例如，如果元件是以所需的屬性交易來設定，而且您接著嘗試將同步處理設定變更為 [無]，當您嘗試呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 時就會產生錯誤，因為交易相依于同步處理。</span><span class="sxs-lookup"><span data-stu-id="7986f-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="7986f-109">**副作用。**</span><span class="sxs-lookup"><span data-stu-id="7986f-109">**Side effects.**</span></span> <span data-ttu-id="7986f-110">如果您沒有明確設定，某些屬性可能會變更。</span><span class="sxs-lookup"><span data-stu-id="7986f-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="7986f-111">例如，如果您設定的元件需要屬性交易，則也會將同步處理設定為 [必要]。</span><span class="sxs-lookup"><span data-stu-id="7986f-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="7986f-112">這實際上是相依性的翻轉端—一個屬性優先于另一個屬性，而其相依性則是透過第一次設定次要屬性，然後封鎖對其所做的變更來表示。</span><span class="sxs-lookup"><span data-stu-id="7986f-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="7986f-113">在集合中的專案所公開的屬性清單中，全都列在 [Com + 系統管理集合](com--administration-collections.md)中，每個屬性都有相關的相依性和副作用。</span><span class="sxs-lookup"><span data-stu-id="7986f-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="7986f-114">當您設定 COM + 應用程式和元件時，您應該留意哪些條件約束在設定上有哪些限制。</span><span class="sxs-lookup"><span data-stu-id="7986f-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7986f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="7986f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7986f-116">取得和設定屬性</span><span class="sxs-lookup"><span data-stu-id="7986f-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="7986f-117">查詢可用的屬性</span><span class="sxs-lookup"><span data-stu-id="7986f-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="7986f-118">儲存或捨棄變更</span><span class="sxs-lookup"><span data-stu-id="7986f-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



