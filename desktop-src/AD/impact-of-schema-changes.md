---
title: 架構變更的影響
description: 本主題說明架構延伸如何影響 Active Directory 樹系。
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- 架構變更的影響 AD
- 架構 AD，變更架構的影響
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967806"
---
# <a name="impact-of-schema-changes"></a><span data-ttu-id="73c52-105">架構變更的影響</span><span class="sxs-lookup"><span data-stu-id="73c52-105">Impact of Schema Changes</span></span>

<span data-ttu-id="73c52-106">架構延伸會影響以數種方式 Active Directory Domain Services 所控制的網域樹系：</span><span class="sxs-lookup"><span data-stu-id="73c52-106">A schema extension impacts a domain forest controlled by Active Directory Domain Services in several ways:</span></span>

-   <span data-ttu-id="73c52-107">架構變更是全域的。</span><span class="sxs-lookup"><span data-stu-id="73c52-107">Schema changes are global.</span></span> <span data-ttu-id="73c52-108">整個樹系都有一個架構。</span><span class="sxs-lookup"><span data-stu-id="73c52-108">There is a single schema for an entire forest.</span></span> <span data-ttu-id="73c52-109">架構會全域複寫：樹系中的每個 DC 上都有架構的複本。</span><span class="sxs-lookup"><span data-stu-id="73c52-109">The schema is globally replicated: a copy of the schema exists on every DC in the forest.</span></span> <span data-ttu-id="73c52-110">當您擴充架構時，它會針對整個樹系進行延伸。</span><span class="sxs-lookup"><span data-stu-id="73c52-110">When you extend the schema, it is extended for the entire forest.</span></span>
-   <span data-ttu-id="73c52-111">無法反轉架構物件的新增專案。</span><span class="sxs-lookup"><span data-stu-id="73c52-111">Schema object additions cannot be reversed.</span></span> <span data-ttu-id="73c52-112">當新的類別或屬性物件加入至架構時，就無法將它移除。</span><span class="sxs-lookup"><span data-stu-id="73c52-112">When a new class or attribute object is added to the schema, it cannot be removed.</span></span> <span data-ttu-id="73c52-113">現有的屬性或類別可以停用，但不能移除。</span><span class="sxs-lookup"><span data-stu-id="73c52-113">An existing attribute or class can be disabled, but not removed.</span></span> <span data-ttu-id="73c52-114">如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="73c52-114">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span> <span data-ttu-id="73c52-115">停用類別或屬性不會影響現有的類別或屬性實例，但是會防止建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="73c52-115">Disabling a class or attribute does not affect existing instances of the class or attribute, but prevents the creation of new instances.</span></span> <span data-ttu-id="73c52-116">如果屬性包含在未停用的任何類別中，就無法停用屬性。</span><span class="sxs-lookup"><span data-stu-id="73c52-116">You cannot disable an attribute if it is included in any class that is not disabled.</span></span>
-   <span data-ttu-id="73c52-117">Oid 必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="73c52-117">OIDs must be unique.</span></span> <span data-ttu-id="73c52-118">當屬性或類別加入至架構時，不能加入具有相同 OID 的屬性或類別。</span><span class="sxs-lookup"><span data-stu-id="73c52-118">When an attribute or class is added to the schema, no attribute or class with the same OID can be added.</span></span> <span data-ttu-id="73c52-119">即使已停用類別或屬性，也是如此。</span><span class="sxs-lookup"><span data-stu-id="73c52-119">This is true even if a class or attribute has been disabled.</span></span> <span data-ttu-id="73c52-120">基於這個理由，您必須使用有效的 Oid。</span><span class="sxs-lookup"><span data-stu-id="73c52-120">For this reason it is you must use valid OIDs.</span></span> <span data-ttu-id="73c52-121">請勿合成 OID，也不會重複使用現有的 OID。</span><span class="sxs-lookup"><span data-stu-id="73c52-121">Do not synthesize an OID, and do not reuse an existing OID.</span></span> <span data-ttu-id="73c52-122">如需取得有效 OID 的詳細資訊，請參閱 [取得根物件識別碼](obtaining-an-object-identifier.md)。</span><span class="sxs-lookup"><span data-stu-id="73c52-122">For more information about obtaining a valid OID, see [Obtaining a Root Object Identifier](obtaining-an-object-identifier.md).</span></span>
-   <span data-ttu-id="73c52-123">建立之後，您可以進行一些變更：</span><span class="sxs-lookup"><span data-stu-id="73c52-123">Some changes can be made after creation:</span></span>

    -   <span data-ttu-id="73c52-124">針對類別1或類別2類別，您可以在 **possSuperiors** 屬性中新增或移除值。</span><span class="sxs-lookup"><span data-stu-id="73c52-124">For a category 1 or category 2 class, you can add or remove values in the **possSuperiors** attribute.</span></span> <span data-ttu-id="73c52-125">**PossSuperiors** 值會指定可包含類別的物件類別。</span><span class="sxs-lookup"><span data-stu-id="73c52-125">The **possSuperiors** values specify the object classes that can contain the class.</span></span>
    -   <span data-ttu-id="73c52-126">針對類別1或類別2類別，您可以在 **mayContain** 屬性中新增或移除值。</span><span class="sxs-lookup"><span data-stu-id="73c52-126">For a category 1 or category 2 class, you can add or remove values in the **mayContain** attribute.</span></span> <span data-ttu-id="73c52-127">**MayContain** 值會指定選擇性屬性，但可能存在於類別的實例中。</span><span class="sxs-lookup"><span data-stu-id="73c52-127">The **mayContain** values specify the optional attributes, but may be present in an instance of the class.</span></span>

-   <span data-ttu-id="73c52-128">類別2類別或屬性的 **lDAPDisplayName** 在建立之後可以變更。</span><span class="sxs-lookup"><span data-stu-id="73c52-128">The **lDAPDisplayName** for a Category 2 class or attribute can be changed after it has been created.</span></span> <span data-ttu-id="73c52-129">一般來說，您不應該變更 **lDAPDisplayName**。</span><span class="sxs-lookup"><span data-stu-id="73c52-129">Typically, you should not change the **lDAPDisplayName**.</span></span> <span data-ttu-id="73c52-130">不過，變更 LDAP 名稱有一個合法的原因，也就是如果您在定義屬性或類別時犯了錯誤，必須建立一個新的，以取代舊的名稱。</span><span class="sxs-lookup"><span data-stu-id="73c52-130">However, there is one legitimate reason for changing the LDAP name and that is if you made a mistake in defining the attribute or class and must create a new one to replace the old one.</span></span> <span data-ttu-id="73c52-131">您不需要重新命名屬性或類別架構 (RDN) 的相對辨別名稱即可完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="73c52-131">You do not have to rename the relative distinguished name (RDN) of the attribute or class schema to do this.</span></span> <span data-ttu-id="73c52-132">當 LDAP 名稱變更時，這可讓您解決錯誤，而不是重建整個 Windows 2000 基礎結構。</span><span class="sxs-lookup"><span data-stu-id="73c52-132">When the LDAP name is changed this enables you to work around a mistake rather than rebuilding your whole Windows 2000 infrastructure.</span></span> <span data-ttu-id="73c52-133">如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="73c52-133">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

    <span data-ttu-id="73c52-134">預先定義 (類別 1) 類別或屬性的 **lDAPDisplayName** 無法變更。</span><span class="sxs-lookup"><span data-stu-id="73c52-134">The **lDAPDisplayName** for predefined (category 1) classes or attributes cannot be changed.</span></span> <span data-ttu-id="73c52-135">如需類別1和2架構物件的詳細資訊，請參閱 [架構延伸的限制](restrictions-on-schema-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="73c52-135">For more information about category 1 and 2 schema objects, see [Restrictions on Schema Extension](restrictions-on-schema-extension.md).</span></span>

 

 




