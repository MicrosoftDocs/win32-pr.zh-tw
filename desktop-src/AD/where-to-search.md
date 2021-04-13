---
title: 決定要搜尋的位置
description: 本主題說明可以在 Active Directory Domain Services 中執行的不同搜尋。
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- 決定要在哪裡搜尋 AD
- Active Directory AD、搜尋、決定要搜尋的位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314596"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="ff7b5-105">決定要搜尋的位置</span><span class="sxs-lookup"><span data-stu-id="ff7b5-105">Deciding Where to Search</span></span>

<span data-ttu-id="ff7b5-106">本主題說明可以在 Active Directory Domain Services 中執行的不同搜尋。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="ff7b5-107">所有搜尋都是在下列其中一個命名內容中執行：</span><span class="sxs-lookup"><span data-stu-id="ff7b5-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="ff7b5-108">網域，包括應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="ff7b5-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="ff7b5-109">架構容器</span><span class="sxs-lookup"><span data-stu-id="ff7b5-109">Schema container</span></span>
-   <span data-ttu-id="ff7b5-110">設定容器</span><span class="sxs-lookup"><span data-stu-id="ff7b5-110">Configuration container</span></span>
-   <span data-ttu-id="ff7b5-111">通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="ff7b5-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="ff7b5-112">搜尋定義域</span><span class="sxs-lookup"><span data-stu-id="ff7b5-112">Searching a Domain</span></span>

<span data-ttu-id="ff7b5-113">網域包含大部分高度使用的物件，例如使用者、連絡人、群組、組織單位、電腦等等。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="ff7b5-114">大部分的查詢都會搜尋網域。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-114">Most queries will search a domain.</span></span> <span data-ttu-id="ff7b5-115">如需搜尋網域的詳細資訊，請參閱 [搜尋定義域內容](searching-domain-contents.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="ff7b5-116">搜尋架構容器</span><span class="sxs-lookup"><span data-stu-id="ff7b5-116">Searching the Schema Container</span></span>

<span data-ttu-id="ff7b5-117">架構容器包含 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 和 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件，這些物件會提供可存在於 Active Directory Domain Services 中的每個類別和屬性的正式定義。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="ff7b5-118">若要搜尋架構容器中的物件，請系結至任何網域控制站上的架構容器。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="ff7b5-119">架構容器可在所有網域控制站上使用。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="ff7b5-120">架構容器的分辨名稱是從 rootDSE 的 **schemaNamingCoNtext** 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="ff7b5-121">如需 rootDSE 和 **schemaNamingCoNtext** 屬性的詳細資訊，請參閱 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="ff7b5-122">如需有關從架構或抽象架構容器讀取的詳細資訊，請參閱系結 [至架構的指導方針](guidelines-for-binding-to-the-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="ff7b5-123">搜尋設定容器</span><span class="sxs-lookup"><span data-stu-id="ff7b5-123">Searching the Configuration Container</span></span>

<span data-ttu-id="ff7b5-124">Configuration 容器包含整個樹系的設定資訊，例如網站、服務和顯示規範。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="ff7b5-125">若要搜尋設定容器中的物件，請系結至任何網域控制站上的設定容器。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="ff7b5-126">Configuration 容器可在所有網域控制站上使用。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="ff7b5-127">設定容器的分辨名稱是從 rootDSE 的 **configurationNamingCoNtext** 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="ff7b5-128">如需 rootDSE 和 **configurationNamingCoNtext** 屬性的詳細資訊，請參閱 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="ff7b5-129">搜尋通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="ff7b5-129">Searching the Global Catalog</span></span>

<span data-ttu-id="ff7b5-130">通用類別目錄會在 Active Directory Domain Services 中保存每個物件的複本，但其屬性只有少數幾個。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="ff7b5-131">通用類別目錄中的屬性是搜尋作業中最常使用的屬性，例如使用者的名字和姓氏、登入名稱等等。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="ff7b5-132">如需有關搜尋通用類別目錄的詳細資訊，請參閱 [搜尋通用類別目錄](searching-global-catalog-contents.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7b5-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 