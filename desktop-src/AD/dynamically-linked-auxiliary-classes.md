---
title: 動態連結的輔助類別
description: 動態連結的輔助類別是附加至個別物件的類別，而不是附加至物件類別的類別。
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- 動態連結的輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183021"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="89d58-104">動態連結的輔助類別</span><span class="sxs-lookup"><span data-stu-id="89d58-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="89d58-105">動態連結的輔助類別是附加至個別物件的類別，而不是附加至物件類別的類別。</span><span class="sxs-lookup"><span data-stu-id="89d58-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="89d58-106">動態連結可讓您以個別物件儲存其他屬性，而不會對整個類別的架構定義進行延伸整個樹系的影響。</span><span class="sxs-lookup"><span data-stu-id="89d58-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="89d58-107">例如，企業可以使用動態連結，將銷售特定的輔助類別附加至其銷售人員的使用者物件，以及其他部門專屬的輔助類別附加至其他部門中員工的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="89d58-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="89d58-108">動態連結不復雜：將輔助類別的名稱加入至物件的 **objectClass** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="89d58-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="89d58-109">如果輔助類別具有任何必要屬性 (**mustHave** 或 **SystemMustHave**) ，您必須同時設定它們。</span><span class="sxs-lookup"><span data-stu-id="89d58-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="89d58-110">如需詳細資訊和程式碼範例，請參閱 [將輔助類別加入至物件實例](adding-an-auxiliary-class-to-an-object-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="89d58-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="89d58-111">若要移除動態連結的輔助類別，請清除輔助類別中所有屬性的值，然後從物件的 **objectClass** 屬性中移除輔助類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="89d58-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="89d58-112">如果您動態加入的輔助類別是另一個輔助類別的子類別，則會將這兩個輔助類別新增至目標物件。</span><span class="sxs-lookup"><span data-stu-id="89d58-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="89d58-113">不過，移除子輔助類別並不會移除其父系;每個類別都必須明確移除。</span><span class="sxs-lookup"><span data-stu-id="89d58-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




