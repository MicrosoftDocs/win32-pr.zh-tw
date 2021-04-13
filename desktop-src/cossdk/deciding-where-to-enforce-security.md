---
description: 取捨是強制執行安全性的固有功能。
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: 決定要在哪裡強制執行安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510476"
---
# <a name="deciding-where-to-enforce-security"></a><span data-ttu-id="7b2ac-103">決定要在哪裡強制執行安全性</span><span class="sxs-lookup"><span data-stu-id="7b2ac-103">Deciding Where to Enforce Security</span></span>

<span data-ttu-id="7b2ac-104">取捨是強制執行安全性的固有功能。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-104">Trade-offs are inherent in enforcing security.</span></span> <span data-ttu-id="7b2ac-105">資料庫可以是放置安全性邏輯的自然位置，因為最終資料是要保護的最重要的一件事。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-105">A database can be a natural place to put security logic, given that ultimately that data is the most important thing to protect.</span></span> <span data-ttu-id="7b2ac-106">不過，這麼做會造成顯著的效能影響。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-106">However, doing so has significant performance implications.</span></span> <span data-ttu-id="7b2ac-107">在資料庫上強制執行安全性可能會非常昂貴、規模不佳，而且沒有彈性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-107">Enforcing security at the database can be very expensive, scales poorly, and is inflexible.</span></span>

## <a name="enforcing-security-in-the-middle-tier"></a><span data-ttu-id="7b2ac-108">在中介層強制執行安全性</span><span class="sxs-lookup"><span data-stu-id="7b2ac-108">Enforcing Security in the Middle Tier</span></span>

<span data-ttu-id="7b2ac-109">使用 COM + 進行可擴充的多層式應用程式要遵循的一般規則，可能的話，您應該盡可能在中介層的 COM + 應用程式中強制執行詳細的安全性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-109">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="7b2ac-110">這樣做可讓您充分利用 COM + 所提供的可擴充服務。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-110">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="7b2ac-111">只有在您絕對需要時，才在資料庫上強制執行驗證，並完全衡量這麼做的效能含意。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-111">Enforce authentication at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="7b2ac-112">最佳情況是能夠保護資料庫資料表，讓 COM + 應用程式能夠以自己的身分識別來存取它們。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-112">The optimal situation is to be able to secure database tables so that the COM+ application is able to access them under its own identity.</span></span> <span data-ttu-id="7b2ac-113">資料庫應只驗證 COM + 應用程式，並信任它以正確驗證及授權將存取資料的用戶端。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-113">The database should just authenticate the COM+ application and trust it to correctly authenticate and authorize clients that will be accessing data.</span></span> <span data-ttu-id="7b2ac-114">這種方法的優點如下：</span><span class="sxs-lookup"><span data-stu-id="7b2ac-114">The benefits of this approach are as follows:</span></span>

-   <span data-ttu-id="7b2ac-115">它會啟用所有用戶端之間的連接共用，因為連接是完全泛型的。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-115">It enables connection pooling among all clients, as connections are completely generic.</span></span>
-   <span data-ttu-id="7b2ac-116">它通常會將資料存取優化，通常是在調整應用程式時有問題的扼點。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-116">It generally optimizes data access, often a problematic choke point when scaling applications.</span></span>
-   <span data-ttu-id="7b2ac-117">它可以將強制執行安全性的邏輯負擔降至最低，特別是在可以使用宣告式角色型安全性的情況下。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-117">It can minimize the logic overhead for enforcing security, particularly if declarative role-based security can be used.</span></span>
-   <span data-ttu-id="7b2ac-118">它可以在安全性原則中提供絕佳的彈性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-118">It can provide great flexibility in a security policy.</span></span> <span data-ttu-id="7b2ac-119">您可以輕鬆地設定和重新設定，如以 [角色為基礎的安全性管理](role-based-security-administration.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-119">You can configure and reconfigure it easily, as described in [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="7b2ac-120">但是，如同 [有效設計角色](designing-roles-effectively.md)所述，雖然角色可以輕鬆且有效地套用至某些使用者資料的關聯性，但它們並不是安全性存取決策的通用解決方案。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-120">But, as discussed in [Designing Roles Effectively](designing-roles-effectively.md), while roles can be easily and effectively applied to some user-data relationships, they are not a universal solution for security access decisions.</span></span>

## <a name="enforcing-security-at-the-database"></a><span data-ttu-id="7b2ac-121">在資料庫中強制執行安全性</span><span class="sxs-lookup"><span data-stu-id="7b2ac-121">Enforcing Security at the Database</span></span>

<span data-ttu-id="7b2ac-122">儘管在中介層強制執行安全性的 preferability，還是有許多原因會在資料庫上強制執行安全性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7b2ac-122">Despite the preferability of enforcing security at the middle tier, there are a number of reasons to enforce security at the database, such as the following:</span></span>

-   <span data-ttu-id="7b2ac-123">您沒有任何選擇，可能是基於舊版的原因，或可能是因為決策其實不是您的手。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-123">You don't have a choice, perhaps for legacy reasons or perhaps because the decision is simply not in your hands.</span></span>
-   <span data-ttu-id="7b2ac-124">資料庫是由各種不同的應用程式存取，而且無法以單一應用程式為基礎來設定其安全性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-124">The database is accessed by a wide variety of applications, and its security can't be configured on the basis of a single application.</span></span>
-   <span data-ttu-id="7b2ac-125">資料庫可透過可預測的方式進行保護。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-125">A database can be made predictably protected.</span></span> <span data-ttu-id="7b2ac-126">如果您將企業關鍵資料保留在資料庫中，您可以在其周圍繪製緊密旅行車，並協助控制誰可以看到它。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-126">If you keep enterprise-critical data in a database, you can draw a tight wagon around it and help control who gets to see it.</span></span>
-   <span data-ttu-id="7b2ac-127">在資料庫中驗證原始用戶端，可以詳細記錄資料庫中已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-127">Authenticating original clients at the database enables detailed logging of who has done what in the database.</span></span>
-   <span data-ttu-id="7b2ac-128">有些資料會本質系結至特定的使用者，而進行極細微存取決策的邏輯可能會在資料庫本身最有效率地執行，接近資料。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-128">Some data is innately bound to particular users, and the logic of making extremely fine-grained access decisions might be most efficiently carried out at the database itself, close to the data.</span></span>

<span data-ttu-id="7b2ac-129">當您在一起設計資料庫和 COM + 應用程式的安全性時，大部分的問題都是關於資料本身的特性，以及其與存取它的使用者之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-129">When you do have the luxury of designing the security of the database and the COM+ application in tandem, most of these issues pertain to characteristics of the data itself and its relationship to the users accessing it.</span></span> <span data-ttu-id="7b2ac-130">使用可預測的使用者類別可存取的資料，可讓您有效率地使用角色來控制仲介層中的存取。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-130">With data that can be accessed by predictable categories of users, it is efficient to control access in the middle tier using roles.</span></span> <span data-ttu-id="7b2ac-131">使用 intricately 系結至極小使用者類別的資料時，這些關聯性通常必須以資料本身表示，因此您必須在資料庫中強制執行某些安全性。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-131">With data that is intricately bound to very small classes of users, those relationships must often be expressed with the data itself and hence you must enforce some security at the database.</span></span>

### <a name="performance-implications-of-enforcing-security-at-the-database"></a><span data-ttu-id="7b2ac-132">在資料庫中強制執行安全性的效能含意</span><span class="sxs-lookup"><span data-stu-id="7b2ac-132">Performance Implications of Enforcing Security at the Database</span></span>

<span data-ttu-id="7b2ac-133">如果您在資料庫上驗證或授權使用者，則必須將使用者身分識別傳播至資料庫以支援這種情況。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-133">If you authenticate or authorize users at the database, the user identity needs to be propagated through to the database to support this.</span></span> <span data-ttu-id="7b2ac-134">如果資料庫信任中介層應用程式，則可以在參數中傳遞使用者安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-134">If the database trusts the middle-tier application to do so, it is possible to pass in user security information in parameters.</span></span> <span data-ttu-id="7b2ac-135">否則，必須在使用者的身分識別下進行對資料庫的呼叫，這表示伺服器應用程式必須模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-135">Otherwise, the call through to the database must be made under the user's identity, meaning that the server application must impersonate the client.</span></span> <span data-ttu-id="7b2ac-136">這可能會影響效能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7b2ac-136">This can have performance implications such as the following:</span></span>

-   <span data-ttu-id="7b2ac-137">模擬用戶端可能會比直接在應用程式識別下進行呼叫更慢。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-137">Impersonating the client can be much slower than making the call directly under the application identity.</span></span> <span data-ttu-id="7b2ac-138">如需詳細資訊，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-138">For more detail, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>
-   <span data-ttu-id="7b2ac-139">在特定使用者身分識別下建立的資料庫連接無法共用。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-139">A database connection made under a specific user identity cannot be pooled.</span></span>
-   <span data-ttu-id="7b2ac-140">在資料庫本身中新增邏輯，會造成建立調整瓶頸的風險。</span><span class="sxs-lookup"><span data-stu-id="7b2ac-140">Adding logic in the database itself runs the risk of creating a scaling bottleneck.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b2ac-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b2ac-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2ac-142">在多層式應用程式中保護資料的基本案例</span><span class="sxs-lookup"><span data-stu-id="7b2ac-142">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[<span data-ttu-id="7b2ac-143">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="7b2ac-143">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



