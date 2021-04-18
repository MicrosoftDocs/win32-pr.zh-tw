---
title: 擴充架構
description: Active Directory Directory 服務架構會定義 Active Directory Domain Services 中所使用的屬性和類別。
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory，使用架構，擴充架構
- 架構 AD，擴充架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106965836"
---
# <a name="extending-the-schema"></a><span data-ttu-id="903db-105">擴充架構</span><span class="sxs-lookup"><span data-stu-id="903db-105">Extending the Schema</span></span>

<span data-ttu-id="903db-106">Active Directory Directory 服務架構會定義 Active Directory Domain Services 中所使用的屬性和類別。</span><span class="sxs-lookup"><span data-stu-id="903db-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="903db-107">包含在系統中的基底架構包含一組豐富的類別定義，例如 **使用者**、 **電腦** 和 **organizationalUnit**，以及屬性定義，例如 **userPrincipalName**、 **telephoneNumber** 和 **objectSid**。</span><span class="sxs-lookup"><span data-stu-id="903db-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="903db-108">現有的類別和屬性集合對大部分的應用程式都已足夠。</span><span class="sxs-lookup"><span data-stu-id="903db-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="903db-109">不過，架構是可擴充的，這表示您可以定義新的類別和屬性。</span><span class="sxs-lookup"><span data-stu-id="903db-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="903db-110">本節討論如何延伸 Active Directory 架構。</span><span class="sxs-lookup"><span data-stu-id="903db-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="903db-111">延伸架構的時機</span><span class="sxs-lookup"><span data-stu-id="903db-111">When to Extend the Schema</span></span>

<span data-ttu-id="903db-112">如果現有的類別和屬性不符合您想要儲存的資料類型，您應該擴充架構。</span><span class="sxs-lookup"><span data-stu-id="903db-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="903db-113">請務必注意，架構新增是永久性的;您可以停用類別和屬性，但是絕對不能從架構中移除它們。</span><span class="sxs-lookup"><span data-stu-id="903db-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="903db-114">當您測試程式碼時，請記住這一點。</span><span class="sxs-lookup"><span data-stu-id="903db-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="903db-115">也請考慮您要儲存的資料大小。</span><span class="sxs-lookup"><span data-stu-id="903db-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="903db-116">Microsoft 建議沒有任何屬性值超過 500 kb，包括多值屬性的總和。</span><span class="sxs-lookup"><span data-stu-id="903db-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="903db-117">此外，物件的大小不能超過 1 mb。</span><span class="sxs-lookup"><span data-stu-id="903db-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="903db-118">也請考慮資料的實例數目;如果您在具有100000使用者的系統上，將新屬性新增至 [**使用者**](/windows/desktop/ADSchema/c-user) 類別，這可能會佔用相當大的空間。</span><span class="sxs-lookup"><span data-stu-id="903db-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="903db-119">本節中的主題包括：</span><span class="sxs-lookup"><span data-stu-id="903db-119">Topics in this section include:</span></span>

-   <span data-ttu-id="903db-120">如何系結至架構容器，以及讀取現有類別和屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="903db-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="903db-121">如何及何時透過定義新的屬性和類別來延伸架構。</span><span class="sxs-lookup"><span data-stu-id="903db-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="903db-122">如何使用 LDIFDE、CSVDE 或以程式設計方式使用 ADSI 安裝架構延伸。</span><span class="sxs-lookup"><span data-stu-id="903db-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="903db-123">如需 Active Directory 架構的詳細資訊和總覽，包括架構執行、類別定義和屬性定義的相關資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="903db-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="903db-124">如需詳細資訊，包括預先定義之架構類別、屬性和屬性語法的參考頁面，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)中的 Active Directory 架構參考。</span><span class="sxs-lookup"><span data-stu-id="903db-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 