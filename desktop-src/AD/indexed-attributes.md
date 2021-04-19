---
title: '索引屬性 (AD DS) '
description: 可以編制屬性的索引。 編制屬性的索引可改善該屬性的查詢效能。
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- 已編制索引的屬性廣告
- 屬性 AD、索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106978575"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="f0c3a-106">索引屬性 (AD DS) </span><span class="sxs-lookup"><span data-stu-id="f0c3a-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="f0c3a-107">可以編制屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-107">Attributes may be indexed.</span></span> <span data-ttu-id="f0c3a-108">編制屬性的索引可改善該屬性的查詢效能。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="f0c3a-109">當屬性架構定義中的 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性將最小的位設定為1時，就會編制屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="f0c3a-110">將 **searchFlags** 屬性架構定義的最小有效位設定為1，將會動態建立索引。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="f0c3a-111">將 **searchFlags** 屬性架構定義的最小有效位設定為0，將會移除屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="f0c3a-112">索引將由網域控制站上的背景執行緒自動建立。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="f0c3a-113">在理想的情況下，索引屬性應該是具有高度唯一值的單一值，而這些值會平均分散到一組實例。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="f0c3a-114">屬性的唯一值越少，索引的效率就愈低。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="f0c3a-115">您也可以編制多值屬性的索引，但為多重值屬性建立索引的成本會比儲存體、更新和搜尋時間更大。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="f0c3a-116">多重值屬性的唯一性需求與單一值屬性的唯一性需求相同，唯一的值愈多，就越能有效地使用索引。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="f0c3a-117">類別所擁有的索引屬性愈多，建立類別的新實例需要更多時間。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="f0c3a-118">索引適用于屬性，不適用於類別。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="f0c3a-119">也就是說，當屬性標示為已編制索引時，會將屬性的所有實例加入至索引，而不只是特定類別的成員實例。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="f0c3a-120">若要確認伺服器是否使用索引來處理查詢，請將網域控制站上的下列登錄值設定為4。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="f0c3a-121">然後在該網域控制站上執行查詢，並在目錄事件記錄檔中查看用來處理查詢的索引相關資料（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="f0c3a-122">如需 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性中其他位的詳細資訊，請參閱 [屬性的特性](characteristics-of-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="f0c3a-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 