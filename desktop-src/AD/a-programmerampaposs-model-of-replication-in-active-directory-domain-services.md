---
title: 程式設計人員在 Active Directory Domain Services 中的複寫模型
description: 以下是 Active Directory Domain Services 的複寫模型描述。
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- 程式設計師的 Active Directory 複寫 AD 模型
- 程式設計人員在 Active Directory Domain Services 中的複寫模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020755"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a><span data-ttu-id="20c52-105">程式設計人員在 Active Directory Domain Services 中的複寫模型</span><span class="sxs-lookup"><span data-stu-id="20c52-105">A Programmer's Model of Replication in Active Directory Domain Services</span></span>

<span data-ttu-id="20c52-106">以下是 Active Directory Domain Services 的複寫模型描述。</span><span class="sxs-lookup"><span data-stu-id="20c52-106">The following is a description of the replication model for Active Directory Domain Services.</span></span>

<span data-ttu-id="20c52-107">Active Directory 網網域控制站 (DC) 的所有更新都會使用 LDAP 要求來執行，以針對每個要求建立、修改或刪除一個物件。</span><span class="sxs-lookup"><span data-stu-id="20c52-107">All updates to the Active Directory Domain Controller (DC) are performed using LDAP requests that create, modify, or delete one object for each request.</span></span> <span data-ttu-id="20c52-108">單一要求可以設定或修改物件上的多個屬性。</span><span class="sxs-lookup"><span data-stu-id="20c52-108">A single request can set or modify multiple attributes on an object.</span></span>

<span data-ttu-id="20c52-109">更新要求會在某個 DC 上以不可部分完成的交易形式處理。</span><span class="sxs-lookup"><span data-stu-id="20c52-109">An update request is processed as an atomic transaction at some DC.</span></span> <span data-ttu-id="20c52-110">發生整個更新或不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="20c52-110">Either the entire update happens or none of it does.</span></span> <span data-ttu-id="20c52-111">如果要求者收到更新要求的成功回應，則表示整個要求已成功 (認可) 。</span><span class="sxs-lookup"><span data-stu-id="20c52-111">If the requester receives a successful response to an update request, that entire request has succeeded (committed).</span></span> <span data-ttu-id="20c52-112">這稱為「原始寫入」。</span><span class="sxs-lookup"><span data-stu-id="20c52-112">This is called an "originating write."</span></span> <span data-ttu-id="20c52-113">多個 LDAP 要求無法分組為一個較大的交易。</span><span class="sxs-lookup"><span data-stu-id="20c52-113">Multiple LDAP requests cannot be grouped into a single larger transaction.</span></span>

<span data-ttu-id="20c52-114">在原始寫入中，DC 會針對每個新的或已修改的屬性值計算「戳記」，並將此戳記附加至值，因此當複寫值時，戳記也會進行複寫。</span><span class="sxs-lookup"><span data-stu-id="20c52-114">In an originating write, a DC computes a "stamp" for each new or modified attribute value, and attaches this stamp to the value so when the value is replicated, the stamp is replicated too.</span></span> <span data-ttu-id="20c52-115">新的戳記是唯一的，而且在更新時，新的戳記會大於該 DC 上舊值的戳記。</span><span class="sxs-lookup"><span data-stu-id="20c52-115">The new stamp is unique, and in case of an update, the new stamp is larger than the stamp on the old value at that DC.</span></span>

<span data-ttu-id="20c52-116">在此情況下，DC 會選取上次執行複寫之後變更的物件集合。</span><span class="sxs-lookup"><span data-stu-id="20c52-116">Occasionally, a DC selects the set of objects that have changed since the last time the DC performed replication.</span></span> <span data-ttu-id="20c52-117">然後，針對每個物件，它會將單一訊息傳送至所有其他 Dc，其中包含自上次複寫物件之後變更的所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="20c52-117">Then, for each object, it sends a single message to all other DCs that contain all the current values of attributes changed since the last time the object was replicated.</span></span> <span data-ttu-id="20c52-118">複寫訊息是可靠的，並且會依序傳遞，但可能需要更多時間才能傳遞。</span><span class="sxs-lookup"><span data-stu-id="20c52-118">Replication messages are reliable and are delivered in order, but may require more time to be delivered.</span></span>

<span data-ttu-id="20c52-119">當某個 DC 接收來自另一個 DC 的複寫訊息時，它會依照下列方式處理它：針對每個修改的屬性，如果複寫訊息中值的戳記大於目前值的戳記，則 DC 會套用更新;否則 DC 會捨棄更新。</span><span class="sxs-lookup"><span data-stu-id="20c52-119">When one DC receives a replication message from another DC, it processes it as follows: For each modified attribute, if the stamp on the value in the replication message is larger than the stamp on the current value, the DC applies the update; otherwise the DC discards the update.</span></span> <span data-ttu-id="20c52-120">每個複寫訊息都會套用為不可部分完成的交易，就像原始寫入一樣。</span><span class="sxs-lookup"><span data-stu-id="20c52-120">Each replication message is applied as an atomic transaction, just like an originating write.</span></span>

<span data-ttu-id="20c52-121">這是 Active Directory Domain Services 複寫模型。</span><span class="sxs-lookup"><span data-stu-id="20c52-121">That is the Active Directory Domain Services replication model.</span></span> <span data-ttu-id="20c52-122">此模型的重要屬性包括：</span><span class="sxs-lookup"><span data-stu-id="20c52-122">Key properties of this model include:</span></span>

-   <span data-ttu-id="20c52-123">單一物件的原始寫入是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="20c52-123">An originating write to a single object is atomic.</span></span>
-   <span data-ttu-id="20c52-124">複寫變更時，會傳送原始寫入所做的所有變更，或不是任何變更。</span><span class="sxs-lookup"><span data-stu-id="20c52-124">When replicating changes, either all the changes made by an originating write are sent or none of them are.</span></span>
-   <span data-ttu-id="20c52-125">單一物件的複寫寫入是不可部分完成的，但衝突則是依屬性解析。</span><span class="sxs-lookup"><span data-stu-id="20c52-125">A replicated write to a single object is atomic, but conflicts are resolved attribute-by-attribute.</span></span>

<span data-ttu-id="20c52-126">模型不保證對不同物件所做之變更的複寫順序。</span><span class="sxs-lookup"><span data-stu-id="20c52-126">The model does not guarantee the replication ordering of changes made to different objects.</span></span> <span data-ttu-id="20c52-127">請勿撰寫採用原始寫入順序來複寫變更的應用程式。</span><span class="sxs-lookup"><span data-stu-id="20c52-127">Do not write applications that assume that changes are replicated in originating-write order.</span></span> <span data-ttu-id="20c52-128">模型不保證如果物件的屬性變更兩次，則會複寫兩個值;複寫時只會傳送目前的值。</span><span class="sxs-lookup"><span data-stu-id="20c52-128">The model does not guarantee that if an attribute of an object is changed twice, both values will be replicated; Replication sends only the current value at the time of replication.</span></span>

<span data-ttu-id="20c52-129">這種模型與現實的不同之處在于，它只會影響效能。</span><span class="sxs-lookup"><span data-stu-id="20c52-129">The model differs from reality in several ways that only affect performance.</span></span> <span data-ttu-id="20c52-130">例如，Active Directory 伺服器會將包含變更的複寫訊息傳送至多個物件，但會處理這類多物件訊息的內容，就像是一系列的單一物件訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="20c52-130">For example, the Active Directory Server sends replication messages containing the changes to multiple objects, but processes the contents of such a multi-object message as if it were a series of single-object messages.</span></span> <span data-ttu-id="20c52-131">Active Directory 伺服器不會執行模型中所述的點對點複寫，而是會執行功能相當於模型的更複雜且更有效率的可轉移複寫。</span><span class="sxs-lookup"><span data-stu-id="20c52-131">The Active Directory Server does not perform point-to-point replication as described in the model, but instead performs a more complex and more efficient transitive replication that is functionally equivalent to the model.</span></span>

 

 




