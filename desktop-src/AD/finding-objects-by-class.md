---
title: 依類別尋找物件
description: 特定物件類別的一般搜尋查詢。
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- 依類別 AD 尋找物件
- 依類別 Active Directory、使用、搜尋
- 物件廣告，依類別搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999570"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="301cd-106">依類別尋找物件</span><span class="sxs-lookup"><span data-stu-id="301cd-106">Finding Objects by Class</span></span>

<span data-ttu-id="301cd-107">特定物件類別的一般搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="301cd-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="301cd-108">下列程式碼範例會在組建7N 中搜尋具有位置的電腦。</span><span class="sxs-lookup"><span data-stu-id="301cd-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="301cd-109">考慮不使用 **objectClass** 的原因。</span><span class="sxs-lookup"><span data-stu-id="301cd-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="301cd-110">請勿使用 **objectClass** ，而不需要包含已編制索引之屬性的另一個比較。</span><span class="sxs-lookup"><span data-stu-id="301cd-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="301cd-111">索引屬性可以提高查詢的效率。</span><span class="sxs-lookup"><span data-stu-id="301cd-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="301cd-112">**ObjectClass** 屬性是多重值，且未建立索引。</span><span class="sxs-lookup"><span data-stu-id="301cd-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="301cd-113">若要指定物件的類型或類別，請使用 **objectCategory**。</span><span class="sxs-lookup"><span data-stu-id="301cd-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="301cd-114">效率較低：</span><span class="sxs-lookup"><span data-stu-id="301cd-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="301cd-115">更有效率：</span><span class="sxs-lookup"><span data-stu-id="301cd-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="301cd-116">請注意，在某些情況下，必須使用 **objectClass** 和 **objectCategory** 的組合。</span><span class="sxs-lookup"><span data-stu-id="301cd-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="301cd-117">User 類別和 contact 類別應該依照下列方式指定。</span><span class="sxs-lookup"><span data-stu-id="301cd-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="301cd-118">請注意，您可以使用下列程式來搜尋使用者和連絡人。</span><span class="sxs-lookup"><span data-stu-id="301cd-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




