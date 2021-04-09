---
title: 屬性集考慮
description: 強烈建議您保持較小的屬性集，因為在可以讀取或寫入單一屬性之前，會先將屬性集資料流程讀入記憶體中。
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- 屬性集考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675907"
---
# <a name="property-set-considerations"></a><span data-ttu-id="174ae-104">屬性集考慮</span><span class="sxs-lookup"><span data-stu-id="174ae-104">Property Set Considerations</span></span>

<span data-ttu-id="174ae-105">強烈建議您保持較小的屬性集，因為在可以讀取或寫入單一屬性之前，會先將屬性集資料流程讀入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="174ae-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="174ae-106">「小型」表示小於 32 kb 的資料。</span><span class="sxs-lookup"><span data-stu-id="174ae-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="174ae-107">這種情況很少會造成問題，因為一般而言，「內嵌」屬性會是很小的專案，例如描述性字串、關鍵字、時間戳記、計數、作者名稱、全域唯一識別碼 (Guid) 、類別識別碼 (Clsid) 等。</span><span class="sxs-lookup"><span data-stu-id="174ae-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="174ae-108">若要儲存較大的資料區塊，或在一組相關屬性的總大小超過建議數量的情況下，強烈建議使用簡單類型，例如 **vt \_ STREAM** 和 **vt \_ 儲存體** 。</span><span class="sxs-lookup"><span data-stu-id="174ae-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="174ae-109">這些不會儲存在屬性集資料流程中，因此不會大幅影響第一次存取和寫入屬性的初始額外負荷。</span><span class="sxs-lookup"><span data-stu-id="174ae-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="174ae-110">因為屬性集資料流程包含同級資料流程或儲存值屬性的名稱，而這需要額外的少量時間來處理，所以會有最少的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="174ae-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="174ae-111">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="174ae-111">For more information, see:</span></span>

-   [<span data-ttu-id="174ae-112">IPropertySetStorage 實行考慮</span><span class="sxs-lookup"><span data-stu-id="174ae-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="174ae-113">儲存屬性集</span><span class="sxs-lookup"><span data-stu-id="174ae-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="174ae-114">效能特色</span><span class="sxs-lookup"><span data-stu-id="174ae-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="174ae-115">執行摘要資訊屬性集</span><span class="sxs-lookup"><span data-stu-id="174ae-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




