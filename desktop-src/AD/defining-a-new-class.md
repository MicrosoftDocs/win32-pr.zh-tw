---
title: 定義新的類別
description: 當您定義新的類別時，請指定新類別的合法父類別，也就是可以包含新類別實例的類別。
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931900"
---
# <a name="defining-a-new-class"></a><span data-ttu-id="ee347-103">定義新的類別</span><span class="sxs-lookup"><span data-stu-id="ee347-103">Defining a New Class</span></span>

<span data-ttu-id="ee347-104">當您定義新的類別時，請指定新類別的合法父類別，也就是可以包含新類別實例的類別。</span><span class="sxs-lookup"><span data-stu-id="ee347-104">When you define a new class, specify the legal parent classes of the new class, that is, the classes that can contain instances of your new class.</span></span> <span data-ttu-id="ee347-105">合法的父類別是在新類別的 **possSuperiors** 和 **systemPossSuperiors** 屬性中指定，也會在繼承自其超類的可能 superiors 中指定，但不能從輔助類別繼承。</span><span class="sxs-lookup"><span data-stu-id="ee347-105">The legal parent classes are specified in the **possSuperiors** and **systemPossSuperiors** attributes of the new class, as well as in the possible superiors inherited from its superclasses, but not from auxiliary classes.</span></span>

<span data-ttu-id="ee347-106">在定義新類別的合法父類別時，請務必指定。</span><span class="sxs-lookup"><span data-stu-id="ee347-106">Be specific when defining the legal parent classes for the new class.</span></span> <span data-ttu-id="ee347-107">決定您要讓使用者建立類別實例的位置。</span><span class="sxs-lookup"><span data-stu-id="ee347-107">Decide where you want users to create instances of your class.</span></span> <span data-ttu-id="ee347-108">例如，指定 "container" 作為合法父系將可讓使用者在任何標準容器（ (**container**、 **organizationalUnit** 等）下建立實例，而) 在指定 "computer" 時，會讓實例只在 **電腦** 物件的實例底下建立。</span><span class="sxs-lookup"><span data-stu-id="ee347-108">For example, specifying "container" as a legal parent will enable the user create instances under any of the standard containers (**container**, **organizationalUnit**, and so on), while specifying "computer" would enable instances to be created only under instances of the **computer** object.</span></span>

<span data-ttu-id="ee347-109">**建立類別**</span><span class="sxs-lookup"><span data-stu-id="ee347-109">**To Create a Class**</span></span>

1.  <span data-ttu-id="ee347-110">選擇類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee347-110">Choose a name for the class.</span></span> <span data-ttu-id="ee347-111">如需撰寫新類別的通用名稱和 LDAP 顯示名稱的詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-111">For more information about composing a common-name and an LDAP display name for a new class, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>
2.  <span data-ttu-id="ee347-112">取得類別 (OID) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee347-112">Obtain an object identifier (OID) for the class.</span></span> <span data-ttu-id="ee347-113">如需詳細資訊，請參閱 [取得物件識別碼](obtaining-an-object-identifier.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-113">For more information, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
3.  <span data-ttu-id="ee347-114">選擇類別的 [預設物件類別]。</span><span class="sxs-lookup"><span data-stu-id="ee347-114">Choose a "default object category" for the class.</span></span> <span data-ttu-id="ee347-115">如需詳細資訊，請參閱 [物件類別和物件類別](object-class-and-object-category.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-115">For more information, see [Object Class and Object Category](object-class-and-object-category.md).</span></span>
4.  <span data-ttu-id="ee347-116">選擇類別的 [物件類別類別目錄]。</span><span class="sxs-lookup"><span data-stu-id="ee347-116">Choose an "object class category" for the class.</span></span> <span data-ttu-id="ee347-117">這會指出類別是抽象、結構化或輔助。</span><span class="sxs-lookup"><span data-stu-id="ee347-117">This indicates whether the class is abstract, structural, or auxiliary.</span></span> <span data-ttu-id="ee347-118">如需詳細資訊，請參閱 [結構化、抽象概念和輔助類別](structural-abstract-and-auxiliary-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-118">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span>
5.  <span data-ttu-id="ee347-119">建立新的 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="ee347-119">Create a new **classSchema** object.</span></span> <span data-ttu-id="ee347-120">您可以針對 **classSchema** 物件設定許多屬性。</span><span class="sxs-lookup"><span data-stu-id="ee347-120">Many attributes can be set for an **classSchema** object.</span></span> <span data-ttu-id="ee347-121">下列屬性對於新類別的定義而言是不可或缺的：</span><span class="sxs-lookup"><span data-stu-id="ee347-121">The following attributes are critical to the definition of a new class:</span></span>

    -   <span data-ttu-id="ee347-122">新類別所繼承的類別： **subClassOf**、 **auxiliaryClass** 和 **systemAuxiliaryClass**</span><span class="sxs-lookup"><span data-stu-id="ee347-122">Classes from which the new class inherits: **subClassOf**, **auxiliaryClass**, and **systemAuxiliaryClass**</span></span>
    -   <span data-ttu-id="ee347-123">新類別的名稱和識別碼： **cn**、 **lDAPDisplayName**、 **adminDisplayName**、 **schemaIDGUID**、 **governsID**</span><span class="sxs-lookup"><span data-stu-id="ee347-123">Names and identifiers for the new class: **cn**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**</span></span>
    -   <span data-ttu-id="ee347-124">新類別的可能屬性： **mustContain**、 **systemMustContain**、 **mayContain**、 **systemMayContain**</span><span class="sxs-lookup"><span data-stu-id="ee347-124">Possible attributes of the new class: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**</span></span>
    -   <span data-ttu-id="ee347-125">新類別的可能父系： **possSuperiors**、 **systemPossSuperiors**</span><span class="sxs-lookup"><span data-stu-id="ee347-125">Possible parents of the new class: **possSuperiors**, **systemPossSuperiors**</span></span>
    -   <span data-ttu-id="ee347-126">**objectClassCategory**</span><span class="sxs-lookup"><span data-stu-id="ee347-126">**objectClassCategory**</span></span>
    -   <span data-ttu-id="ee347-127">**defaultObjectCategory**</span><span class="sxs-lookup"><span data-stu-id="ee347-127">**defaultObjectCategory**</span></span>
    -   <span data-ttu-id="ee347-128">**defaultHidingValue**</span><span class="sxs-lookup"><span data-stu-id="ee347-128">**defaultHidingValue**</span></span>
    -   <span data-ttu-id="ee347-129">**rDnAttId**</span><span class="sxs-lookup"><span data-stu-id="ee347-129">**rDnAttId**</span></span>
    -   <span data-ttu-id="ee347-130">**defaultSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ee347-130">**defaultSecurityDescriptor**</span></span>
    -   <span data-ttu-id="ee347-131">**描述** (選擇性) </span><span class="sxs-lookup"><span data-stu-id="ee347-131">**description** (optional)</span></span>

    <span data-ttu-id="ee347-132">如需詳細資訊以及這些屬性的說明，請參閱 [物件類別的特性](characteristics-of-object-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-132">For more information, and descriptions of these attributes, see [Characteristics of Object Classes](characteristics-of-object-classes.md).</span></span>

    <span data-ttu-id="ee347-133">請注意，當新類別寫入目錄時， **subClassOf**、 **possSuperiors**、 **systemPossSuperiors**、 **auxiliaryClass** 和 **systemAuxiliaryClass** 中指定的類別必須存在;否則， **classSchema** 物件將無法新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="ee347-133">Be aware that the classes specified in **subClassOf**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass**, and **systemAuxiliaryClass**, must exist when the new class is written to the directory; otherwise, the **classSchema** object will fail to be added to the directory.</span></span> <span data-ttu-id="ee347-134">同樣地， **mustContain**、 **systemMustContain**、 **mayContain** 和 **systemMayContain** 中指定的屬性必須存在，否則類別建立作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ee347-134">Similarly, the attributes specified in **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain**, must exist or the class creation operation will fail.</span></span>

6.  <span data-ttu-id="ee347-135">將新的 **classSchema** 物件寫入目錄。</span><span class="sxs-lookup"><span data-stu-id="ee347-135">Write the new **classSchema** object to the directory.</span></span>

<span data-ttu-id="ee347-136">**將屬性加入至 mayContain 屬性**</span><span class="sxs-lookup"><span data-stu-id="ee347-136">**To add an attribute to the mayContain property**</span></span>

1.  <span data-ttu-id="ee347-137">取得要修改之類別的 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="ee347-137">Obtain the **classSchema** object for the class to modify.</span></span>
2.  <span data-ttu-id="ee347-138">將新屬性新增至 **mayContain** 多重值屬性。</span><span class="sxs-lookup"><span data-stu-id="ee347-138">Add the new attribute to the **mayContain** multi-valued property.</span></span>
3.  <span data-ttu-id="ee347-139">將已變更的 **classSchema** 物件寫回目錄。</span><span class="sxs-lookup"><span data-stu-id="ee347-139">Write the changed **classSchema** object back to the directory.</span></span>

<span data-ttu-id="ee347-140">新的屬性可以和新的類別同時建立;建立新屬性和類別的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="ee347-140">New attributes can be created at the same time as new classes; the order of creating the new attributes and classes is important.</span></span> <span data-ttu-id="ee347-141">如需詳細資訊，請參閱 [安裝的功能](what-the-installation-must-do.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-141">For more information, see [What the Installation Must Do](what-the-installation-must-do.md).</span></span>

<span data-ttu-id="ee347-142">**同時加入新的屬性和新的類別**</span><span class="sxs-lookup"><span data-stu-id="ee347-142">**To add new attributes and new classes at the same time**</span></span>

1.  <span data-ttu-id="ee347-143">先定義所有的新屬性。</span><span class="sxs-lookup"><span data-stu-id="ee347-143">Define all of the new attributes first.</span></span> <span data-ttu-id="ee347-144">如需詳細資訊，請參閱 [定義新屬性](defining-a-new-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="ee347-144">For more information, see [Defining a New Attribute](defining-a-new-attribute.md).</span></span>
2.  <span data-ttu-id="ee347-145">在定義任何新的類別之前，請先更新架構快取。</span><span class="sxs-lookup"><span data-stu-id="ee347-145">Update the Schema Cache before defining any new classes.</span></span> <span data-ttu-id="ee347-146">如需詳細資訊，請參閱 [更新架構](updating-the-schema-cache.md)快取。</span><span class="sxs-lookup"><span data-stu-id="ee347-146">For more information, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
3.  <span data-ttu-id="ee347-147">建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="ee347-147">Create the new classes.</span></span>
4.  <span data-ttu-id="ee347-148">將所需的屬性新增至新的類別。</span><span class="sxs-lookup"><span data-stu-id="ee347-148">Add the desired attributes to the new classes.</span></span>
5.  <span data-ttu-id="ee347-149">重新更新架構快取。</span><span class="sxs-lookup"><span data-stu-id="ee347-149">Update the Schema Cache again.</span></span>

 

 




