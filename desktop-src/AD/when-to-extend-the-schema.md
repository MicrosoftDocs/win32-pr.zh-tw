---
title: 延伸架構的時機
description: 只有在沒有任何現有的物件類別滿足您的應用程式需求時，才擴充架構。 延伸架構是一項複雜的作業;架構變更會複寫至企業樹系中的每個網域控制站。 請仔細考慮。
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- 何時擴充架構 AD
- 架構 AD，何時擴充
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967398"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="cf331-107">延伸架構的時機</span><span class="sxs-lookup"><span data-stu-id="cf331-107">When to Extend the Schema</span></span>

<span data-ttu-id="cf331-108">只有在沒有任何現有的物件類別滿足您的應用程式需求時，才擴充架構。</span><span class="sxs-lookup"><span data-stu-id="cf331-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="cf331-109">延伸架構是一項複雜的作業;架構變更會複寫至企業樹系中的每個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="cf331-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="cf331-110">請仔細考慮。</span><span class="sxs-lookup"><span data-stu-id="cf331-110">Consider this carefully.</span></span>

<span data-ttu-id="cf331-111">您可以透過下列三種方式來擴充架構：</span><span class="sxs-lookup"><span data-stu-id="cf331-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="cf331-112">從現有的類別衍生新的子類別-子類別具有超類別的所有屬性，以及您指定的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="cf331-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="cf331-113">衍生自現有的類別：</span><span class="sxs-lookup"><span data-stu-id="cf331-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="cf331-114">當現有的類別需要其他屬性時，否則為可接受的。</span><span class="sxs-lookup"><span data-stu-id="cf331-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="cf331-115">不需要將類別的現有物件轉換成新類別的能力。</span><span class="sxs-lookup"><span data-stu-id="cf331-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="cf331-116">您無法將子類別新增至現有的物件。</span><span class="sxs-lookup"><span data-stu-id="cf331-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="cf331-117">使用現有的目錄管理員嵌入式管理單元來管理物件的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="cf331-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="cf331-118">將屬性加入至現有的類別及/或加入類別的父物件。</span><span class="sxs-lookup"><span data-stu-id="cf331-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="cf331-119">新增多個屬性時，藉由定義輔助類別並將該輔助類別加入至現有的類別，以結構化的方式執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="cf331-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="cf331-120">當應用程式需要能夠擴充類別的現有物件時，需要修改現有的類別。</span><span class="sxs-lookup"><span data-stu-id="cf331-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="cf331-121">例如，若要將應用程式特定資料加入至使用者物件，請正常地擴充類別使用者，因為您必須處理現有的使用者，而不是您應用程式所建立的特殊使用者。</span><span class="sxs-lookup"><span data-stu-id="cf331-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="cf331-122">使用必要的屬性建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="cf331-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="cf331-123">建立新的類別;亦即，當沒有現有類別可滿足操作需求時，衍生自 "Top" 的類別。</span><span class="sxs-lookup"><span data-stu-id="cf331-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="cf331-124">當您將現有類別子類別化時，子類別將不會繼承與原始類別相關聯的任何使用者介面專案。</span><span class="sxs-lookup"><span data-stu-id="cf331-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="cf331-125">例如，如果您將使用者物件設為子類別，則不會繼承與使用者相關聯的屬性頁面和功能表項目。</span><span class="sxs-lookup"><span data-stu-id="cf331-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="cf331-126">基於這個理由，最好是擴充現有的物件或建立輔助類別，而不是建立子類別。</span><span class="sxs-lookup"><span data-stu-id="cf331-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="cf331-127">無論您是將現有類別的子類別或修改現有的類別，都要擴充 Active Directory 消費者和電腦嵌入式管理單元之類的工具來管理物件的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="cf331-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="cf331-128">如需詳細資訊，請參閱 [擴充目錄物件的消費者介面](extending-the-user-interface-for-directory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cf331-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 




