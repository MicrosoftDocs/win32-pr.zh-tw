---
title: 搜尋通用類別目錄
description: Active Directory Domain Services 也有通用類別目錄 (GC) ，其中包含目錄中所有物件的部分複本。
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- 搜尋通用類別目錄 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671239"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="44bfa-104">搜尋通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="44bfa-104">Searching the Global Catalog</span></span>

<span data-ttu-id="44bfa-105">Active Directory Domain Services 也有通用類別目錄 (GC) ，其中包含目錄中所有物件的部分複本。</span><span class="sxs-lookup"><span data-stu-id="44bfa-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="44bfa-106">它也包含架構和設定容器的部分複本。</span><span class="sxs-lookup"><span data-stu-id="44bfa-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="44bfa-107">網域中的一或多個網域控制站可以保留通用類別目錄的複本。</span><span class="sxs-lookup"><span data-stu-id="44bfa-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="44bfa-108">如需系結至通用類別目錄的詳細資訊，請參閱系結 [至通用類別目錄](binding-to-the-global-catalog.md)。</span><span class="sxs-lookup"><span data-stu-id="44bfa-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="44bfa-109">通用類別目錄會在 Active Directory Domain Services 中保存每個物件的複本，但其屬性只有少數幾個。</span><span class="sxs-lookup"><span data-stu-id="44bfa-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="44bfa-110">通用類別目錄中的屬性是搜尋作業中最常使用的屬性，例如使用者的名字和姓氏、登入名稱等等。</span><span class="sxs-lookup"><span data-stu-id="44bfa-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="44bfa-111">通用類別目錄屬性也包含找出物件完整複本所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="44bfa-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="44bfa-112">通用類別目錄可讓使用者快速找出感興趣的物件，而不需要知道有哪些網域保存這些物件，而不需要在企業中使用連續的延伸命名空間;也就是說，您可以搜尋整個樹系。</span><span class="sxs-lookup"><span data-stu-id="44bfa-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="44bfa-113">因此，如果您系結至全域類別目錄中的物件，您將會搜尋該物件和其下的整個階層，而不需要移至任何其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="44bfa-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="44bfa-114">不過，搜尋只能使用包含通用類別目錄屬性的查詢篩選準則，而且只能取出通用類別目錄中的屬性。</span><span class="sxs-lookup"><span data-stu-id="44bfa-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="44bfa-115">搜尋通用類別目錄有下列優點：</span><span class="sxs-lookup"><span data-stu-id="44bfa-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="44bfa-116">通用類別目錄可讓您搜尋整個樹系或樹系的任何部分，以及架構和設定容器。</span><span class="sxs-lookup"><span data-stu-id="44bfa-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="44bfa-117">通用類別目錄可讓您在單一伺服器上執行完整搜尋。</span><span class="sxs-lookup"><span data-stu-id="44bfa-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="44bfa-118">不需要任何參考或參考追蹤。</span><span class="sxs-lookup"><span data-stu-id="44bfa-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="44bfa-119">搜尋通用類別目錄有下列缺點：</span><span class="sxs-lookup"><span data-stu-id="44bfa-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="44bfa-120">通用類別目錄包含每個物件的一小部分屬性。</span><span class="sxs-lookup"><span data-stu-id="44bfa-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="44bfa-121">如果您的查詢篩選包含不在通用類別目錄中的屬性，則查詢會將包含這些屬性的運算式評估為 false。</span><span class="sxs-lookup"><span data-stu-id="44bfa-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="44bfa-122">如果您在要傳回的屬性清單中指定非通用類別目錄屬性，就不會抓取這些屬性。</span><span class="sxs-lookup"><span data-stu-id="44bfa-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="44bfa-123">若要搜尋通用類別目錄，必須要有包含通用類別目錄的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="44bfa-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="44bfa-124">如果無法使用，則無法執行通用類別目錄搜尋。</span><span class="sxs-lookup"><span data-stu-id="44bfa-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="44bfa-125">通用類別目錄是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="44bfa-125">The global catalog is read-only.</span></span> <span data-ttu-id="44bfa-126">這表示您無法系結至全域類別目錄中的物件，以建立、修改或刪除物件。</span><span class="sxs-lookup"><span data-stu-id="44bfa-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




