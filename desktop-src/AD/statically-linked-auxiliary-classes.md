---
title: 靜態連結的輔助類別
description: 靜態連結的輔助類別是一種，包含在架構中物件類別之 classSchema 定義的 auxiliaryClass 或 systemAuxiliaryClass 屬性中。
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- 靜態連結的輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671224"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="f2acc-104">靜態連結的輔助類別</span><span class="sxs-lookup"><span data-stu-id="f2acc-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="f2acc-105">靜態連結的輔助類別是一種，包含在架構中物件類別之 **classSchema** 定義的 **auxiliaryClass** 或 **systemAuxiliaryClass** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="f2acc-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="f2acc-106">這表示輔助類別是與其相關聯之類別的每個實例的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2acc-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="f2acc-107">在定義類別時，輔助類別可以靜態連結到物件類別，也就是將其 **classSchema** 物件加入至架構容器時。</span><span class="sxs-lookup"><span data-stu-id="f2acc-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="f2acc-108">這是唯一可以使用 **systemAuxiliaryClass** 的時間;建立 **classSchema** 物件之後，就無法修改其 **systemAuxiliaryClass** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2acc-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="f2acc-109">此時靜態連結的輔助類別可以具有強制 (**mustHave**) 和/或選擇性 (**mayHave**) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2acc-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="f2acc-110">具有延伸架構所需許可權的特殊許可權使用者，可以從現有 **classSchema** 物件的 **systemAuxiliaryClass** 屬性新增或移除輔助類別。</span><span class="sxs-lookup"><span data-stu-id="f2acc-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="f2acc-111">這樣做會從物件類別的每個現有實例加入或移除輔助類別。</span><span class="sxs-lookup"><span data-stu-id="f2acc-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="f2acc-112">此時靜態連結的輔助類別可以有選擇性屬性，但不能有必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2acc-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="f2acc-113">這是因為可能有物件類別的現有實例，在這種情況下，加入新的強制屬性會造成問題。</span><span class="sxs-lookup"><span data-stu-id="f2acc-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="f2acc-114">具有特殊許可權的使用者之後可以從 **classSchema** 物件的 **auxiliaryClass** 屬性中移除輔助類別。</span><span class="sxs-lookup"><span data-stu-id="f2acc-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




