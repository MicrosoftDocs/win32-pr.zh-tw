---
title: 抽象架構
description: 架構容器包含所有的 classSchema 和 attributeSchema 物件，這些物件會定義可存在於目錄樹系中的類別和屬性。
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- 抽象架構 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020822"
---
# <a name="the-abstract-schema"></a><span data-ttu-id="6f26b-104">抽象架構</span><span class="sxs-lookup"><span data-stu-id="6f26b-104">The Abstract Schema</span></span>

<span data-ttu-id="6f26b-105">架構容器包含所有的 **classSchema** 和 **attributeSchema** 物件，這些物件會定義可存在於目錄樹系中的類別和屬性。</span><span class="sxs-lookup"><span data-stu-id="6f26b-105">The schema container contains all of the **classSchema** and **attributeSchema** objects that define the classes and attributes that can exist in a directory forest.</span></span> <span data-ttu-id="6f26b-106">架構容器也包含名為 Aggregate of 類別 **ubschema** 的物件。</span><span class="sxs-lookup"><span data-stu-id="6f26b-106">The schema container also contains an object named Aggregate of class **subSchema**.</span></span> <span data-ttu-id="6f26b-107">這個 **ubschema** 物件稱為抽象架構。</span><span class="sxs-lookup"><span data-stu-id="6f26b-107">This **subSchema** object is known as the abstract schema.</span></span>

<span data-ttu-id="6f26b-108">抽象架構包含 **classSchema** 和 **attributeSchema** 物件中所儲存之資料的子集。</span><span class="sxs-lookup"><span data-stu-id="6f26b-108">The abstract schema contains a subset of the data stored in the **classSchema** and **attributeSchema** objects.</span></span> <span data-ttu-id="6f26b-109">其目的是要提供簡單且有效率的機制，以供您用來抓取類別和屬性定義的常用元素。</span><span class="sxs-lookup"><span data-stu-id="6f26b-109">Its purpose is to provide a simple and efficient mechanism for retrieving the frequently used elements of the class and attribute definitions.</span></span> <span data-ttu-id="6f26b-110">例如，若要抓取物件類別的選擇性和強制屬性，請系結至多個物件，以從類別及其所有的超類收集 **mayContain**、 **mustContain**、 **systemMayContain** 和 **systemMustContain** 值，以及從類別的任何輔助類別和其超類收集。</span><span class="sxs-lookup"><span data-stu-id="6f26b-110">For example, to retrieve the optional and mandatory attributes of an object class, bind to multiple objects to collect the **mayContain**, **mustContain**, **systemMayContain**, and **systemMustContain** values from the class and all its superclasses, as well as from any auxiliary classes of the class and its superclasses.</span></span> <span data-ttu-id="6f26b-111">抽象架構可方便地收集單一物件中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="6f26b-111">The abstract schema conveniently collects all this data in a single object.</span></span>

<span data-ttu-id="6f26b-112">如同 Active Directory Domain Services 中的任何物件，您可以系結至 **ubschema** 物件並讀取其屬性，以剖析字串值以取得所需的資料。</span><span class="sxs-lookup"><span data-stu-id="6f26b-112">As with any object in Active Directory Domain Services, you can bind to the **subSchema** object and read its attributes, parsing the string values to retrieve the desired data.</span></span> <span data-ttu-id="6f26b-113">不過，ADSI 會提供一組介面，讓您更輕鬆地讀取抽象架構。</span><span class="sxs-lookup"><span data-stu-id="6f26b-113">However, ADSI provides a set of interfaces that make it much easier to read the abstract schema.</span></span> <span data-ttu-id="6f26b-114">如需詳細資訊，請參閱 [讀取抽象架構](reading-the-abstract-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="6f26b-114">For more information, see [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="6f26b-115">下表列出 **ubschema** 物件的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="6f26b-115">The following table lists key attributes of a **subSchema** object.</span></span>



| <span data-ttu-id="6f26b-116">屬性</span><span class="sxs-lookup"><span data-stu-id="6f26b-116">Attribute</span></span>                 | <span data-ttu-id="6f26b-117">描述</span><span class="sxs-lookup"><span data-stu-id="6f26b-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f26b-118">**attributeTypes**</span><span class="sxs-lookup"><span data-stu-id="6f26b-118">**attributeTypes**</span></span>        | <span data-ttu-id="6f26b-119">包含字串的多重值屬性，這些字串代表架構中的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="6f26b-119">A multi-valued attribute that contains strings that represent each attribute in the schema.</span></span> <span data-ttu-id="6f26b-120">每個值都包含 **attributeID**、 **lDAPDisplayName**、 **attributeSyntax**、 **rangeLower**、 **rangeUpper**，以及指出屬性是否可以有多個值的專案。</span><span class="sxs-lookup"><span data-stu-id="6f26b-120">Each value contains the **attributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper**, and an item that indicates whether the attribute can have multiple values.</span></span> |
| <span data-ttu-id="6f26b-121">**extendedAttributeInfo**</span><span class="sxs-lookup"><span data-stu-id="6f26b-121">**extendedAttributeInfo**</span></span> | <span data-ttu-id="6f26b-122">多值屬性，其中包含代表每個屬性之其他資料的字串。</span><span class="sxs-lookup"><span data-stu-id="6f26b-122">A multi-valued attribute that contains strings that represent additional data for each attribute.</span></span> <span data-ttu-id="6f26b-123">每個值都包含 **attributeID**、 **lDAPDisplayName**、 **schemaIDGUID** 和 **attributeSecurityGUID**。</span><span class="sxs-lookup"><span data-stu-id="6f26b-123">Each value contains the **attributeID**, **lDAPDisplayName**, **schemaIDGUID**, and **attributeSecurityGUID**.</span></span>                                                                          |
| <span data-ttu-id="6f26b-124">**extendedClassInfo**</span><span class="sxs-lookup"><span data-stu-id="6f26b-124">**extendedClassInfo**</span></span>     | <span data-ttu-id="6f26b-125">多值屬性，其中包含代表每個類別之其他資料的字串。</span><span class="sxs-lookup"><span data-stu-id="6f26b-125">A multi-valued attribute that contains strings that represent additional data for each class.</span></span> <span data-ttu-id="6f26b-126">每個值都包含類別的 **governsID**、 **lDAPDisplayName** 和 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="6f26b-126">Each value contains the **governsID**, **lDAPDisplayName**, and **schemaIDGUID** of the class.</span></span>                                                                                              |
| <span data-ttu-id="6f26b-127">**objectClasses**</span><span class="sxs-lookup"><span data-stu-id="6f26b-127">**objectClasses**</span></span>         | <span data-ttu-id="6f26b-128">多值屬性，其中包含表示架構中每個類別的字串。</span><span class="sxs-lookup"><span data-stu-id="6f26b-128">A multi-valued attribute that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="6f26b-129">每個值都包含 **governsID**、 **lDAPDisplayName**、 **mustContain**、 **mayContain** 等等。</span><span class="sxs-lookup"><span data-stu-id="6f26b-129">Each value contains the **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain**, and so on.</span></span>                                                                                           |



 

 

 




