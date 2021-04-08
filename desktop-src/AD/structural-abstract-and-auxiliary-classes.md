---
title: 結構化、抽象類別和輔助類別
description: ClassSchema 物件的 objectClassCategory 屬性可以有值（如下表所示），指出類別是結構化、抽象或輔助。
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- 結構化、抽象類別和輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020824"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="e14c7-104">結構化、抽象類別和輔助類別</span><span class="sxs-lookup"><span data-stu-id="e14c7-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="e14c7-105">**ClassSchema** 物件的 **objectClassCategory** 屬性可以有值（如下表所示），指出類別是結構化、抽象或輔助。</span><span class="sxs-lookup"><span data-stu-id="e14c7-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="e14c7-106">值</span><span class="sxs-lookup"><span data-stu-id="e14c7-106">Value</span></span> | <span data-ttu-id="e14c7-107">描述</span><span class="sxs-lookup"><span data-stu-id="e14c7-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e14c7-108">1</span><span class="sxs-lookup"><span data-stu-id="e14c7-108">1</span></span>     | <span data-ttu-id="e14c7-109">結構化類別，這是唯一可在 Active Directory Domain Services 中具有實例的類別類型。</span><span class="sxs-lookup"><span data-stu-id="e14c7-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="e14c7-110">結構化類別可以是抽象或結構化類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="e14c7-111">結構化類別可在其定義中包含任意數目的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="e14c7-112">2</span><span class="sxs-lookup"><span data-stu-id="e14c7-112">2</span></span>     | <span data-ttu-id="e14c7-113">抽象類別，此類別是用來衍生新的抽象、輔助和結構化類別的範本。</span><span class="sxs-lookup"><span data-stu-id="e14c7-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="e14c7-114">抽象類別只能是抽象類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="e14c7-115">抽象類別無法在 Active Directory Domain Services 中具現化。</span><span class="sxs-lookup"><span data-stu-id="e14c7-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="e14c7-116">抽象類別可在其定義中包含任意數目的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="e14c7-117">3</span><span class="sxs-lookup"><span data-stu-id="e14c7-117">3</span></span>     | <span data-ttu-id="e14c7-118">輔助類別可包含在結構化、抽象或輔助類別的定義中，在此情況下，會將輔助類別的 **mustContain**、 **systemMustContain**、 **mayContain** 和 **systemMayContain** 值加入至類別的定義中。</span><span class="sxs-lookup"><span data-stu-id="e14c7-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="e14c7-119">輔助類別可以是抽象或輔助類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="e14c7-120">輔助類別無法在 Active Directory Domain Services 中具現化。</span><span class="sxs-lookup"><span data-stu-id="e14c7-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="e14c7-121">輔助類別可在其定義中包含任意數目的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="e14c7-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="e14c7-122">請勿將 **objectClassCategory** 與 [物件類別](object-class-and-object-category.md)混淆。</span><span class="sxs-lookup"><span data-stu-id="e14c7-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




