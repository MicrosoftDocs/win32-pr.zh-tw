---
description: 在許多案例中，以角色為基礎的安全性是一種非常有效的機制，但在某些情況下，它的效率較低。
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: 有效設計角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510473"
---
# <a name="designing-roles-effectively"></a><span data-ttu-id="e88f1-103">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="e88f1-103">Designing Roles Effectively</span></span>

<span data-ttu-id="e88f1-104">在許多案例中，以角色為基礎的安全性是一種非常有效的機制，但在某些情況下，它的效率較低。</span><span class="sxs-lookup"><span data-stu-id="e88f1-104">In many scenarios, role-based security is a very effective mechanism, but there are situations where it is less effective.</span></span> <span data-ttu-id="e88f1-105">在決定將角色型安全性套用至特定應用程式的位置和方式時，您應該考慮幾個因素。</span><span class="sxs-lookup"><span data-stu-id="e88f1-105">You should take a number of factors into consideration when deciding where and how to apply role-based security to a particular application.</span></span>

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a><span data-ttu-id="e88f1-106">使用者和資料特性以及角色的適用性</span><span class="sxs-lookup"><span data-stu-id="e88f1-106">User and Data Characteristics and the Suitability of Roles</span></span>

<span data-ttu-id="e88f1-107">角色非常適合用來排列使用者群組的特性，而且也可以篩選這些使用者可以執行的動作。</span><span class="sxs-lookup"><span data-stu-id="e88f1-107">Roles work very well to characterize groups of users and, on that basis, filter what actions those users can perform.</span></span> <span data-ttu-id="e88f1-108">通常，這是藉由建立可反映組織內使用者位置的角色來執行，例如角色「經理」和「Tellers」、「系統管理員」和「讀者」、「專案 One 員工」和「專案兩個員工」。</span><span class="sxs-lookup"><span data-stu-id="e88f1-108">Often, this is carried out in practice by creating roles that reflect a user's place within an organization—for example, the roles "Managers" and "Tellers," "Administrators" and "Readers," "Project One Employees" and "Project Two Employees."</span></span> <span data-ttu-id="e88f1-109">在這種情況下，要存取的資料與使用者是相當的一般，您可以有效率地使用角色來強制執行商務規則，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e88f1-109">In such cases, where the data being accessed is fairly generic relative to the users, roles can be used efficiently to enforce business rules such as the following:</span></span>

-   <span data-ttu-id="e88f1-110">「經理可以轉移任何數量的金錢。</span><span class="sxs-lookup"><span data-stu-id="e88f1-110">"Managers can transfer any amount of money.</span></span> <span data-ttu-id="e88f1-111">Tellers 最多隻能傳送 $10000。」</span><span class="sxs-lookup"><span data-stu-id="e88f1-111">Tellers can transfer only up to $10,000."</span></span>

-   <span data-ttu-id="e88f1-112">「系統管理員可以變更任何變更。</span><span class="sxs-lookup"><span data-stu-id="e88f1-112">"Administrators can change anything.</span></span> <span data-ttu-id="e88f1-113">其他人只能讀取。」</span><span class="sxs-lookup"><span data-stu-id="e88f1-113">Everyone else can only read."</span></span>

-   <span data-ttu-id="e88f1-114">「Project One 員工可以存取特定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e88f1-114">"Project One employees can access a certain database.</span></span> <span data-ttu-id="e88f1-115">沒有人可以。」</span><span class="sxs-lookup"><span data-stu-id="e88f1-115">No one else can."</span></span>

<span data-ttu-id="e88f1-116">使用者可以自然地分為多個角色，視角色如何建立企業組織結構的模型而定。</span><span class="sxs-lookup"><span data-stu-id="e88f1-116">Users might naturally fall into multiple roles, depending on how the roles model the organizational structure of a business.</span></span>

<span data-ttu-id="e88f1-117">不過，當安全性存取決策有特定資料片段的特性時，角色就無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e88f1-117">However, roles don't work very well when a security access decision rests on the characteristics of a particular piece of data.</span></span> <span data-ttu-id="e88f1-118">例如，您很難使用角色來反映複雜的使用者資料關聯性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e88f1-118">For example, it would be difficult to use roles to reflect complicated user-data relationships such as the following:</span></span>

-   <span data-ttu-id="e88f1-119">「特定的管理員只能存取她的報表的人員資料。」</span><span class="sxs-lookup"><span data-stu-id="e88f1-119">"A particular manager can access personnel data for only her reports."</span></span>

-   <span data-ttu-id="e88f1-120">「Joe 消費者可以查詢帳戶餘額」。</span><span class="sxs-lookup"><span data-stu-id="e88f1-120">"Joe Consumer can look up his account balance."</span></span>

<span data-ttu-id="e88f1-121">在這種情況下，您通常必須在資料庫本身完成安全性檢查，以便更容易考慮所存取資料的固有特性。</span><span class="sxs-lookup"><span data-stu-id="e88f1-121">In such cases, security checking must often be done at the database itself, where it is easier to take into account innate characteristics of the data being accessed.</span></span> <span data-ttu-id="e88f1-122">這表示您 *必須使用模擬將客戶* 端身分識別傳遞至資料庫，並讓資料庫驗證要求。</span><span class="sxs-lookup"><span data-stu-id="e88f1-122">This means that you must use *impersonation* to pass the client identity along to the database and let the database validate the request.</span></span> <span data-ttu-id="e88f1-123">這可能會影響效能，而且可能會影響應用程式的設計，例如，在特定使用者身分識別下開啟連接時，連接共用可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="e88f1-123">This can affect performance and can affect the application's design—for example, connection pooling might not work when a connection is opened under a particular user identity.</span></span> <span data-ttu-id="e88f1-124">如需相關問題的討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md) 和 [用戶端模擬與委派](client-impersonation-and-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="e88f1-124">For a discussion of issues involved, see [Multi-Tier Application Security](multi-tier-application-security.md) and [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a><span data-ttu-id="e88f1-125">Role-Based 授權原則的複雜性和擴充性</span><span class="sxs-lookup"><span data-stu-id="e88f1-125">Complexity and Scalability of a Role-Based Authorization Policy</span></span>

<span data-ttu-id="e88f1-126">無論您放置的安全性原則為何，只有在系統管理員部署應用程式時才會生效。</span><span class="sxs-lookup"><span data-stu-id="e88f1-126">Whatever security policy you put in place will be only as effective as its implementation by the system administrators deploying your application.</span></span> <span data-ttu-id="e88f1-127">如果系統管理員基於您的安全性原則，將使用者指派給正確的角色時，您的原則將不會如預期運作。</span><span class="sxs-lookup"><span data-stu-id="e88f1-127">If administrators make mistakes in assigning users to the correct roles according to your security policy, your policy won't work as intended.</span></span> <span data-ttu-id="e88f1-128">在下列情況下，最有可能發生問題：</span><span class="sxs-lookup"><span data-stu-id="e88f1-128">Problems are most likely to occur under the following circumstances:</span></span>

-   <span data-ttu-id="e88f1-129">您已建立一個非常複雜的角色型原則，其中有許多角色和使用者對應到許多角色。</span><span class="sxs-lookup"><span data-stu-id="e88f1-129">You have made a very intricate role-based policy, with many roles and users mapping to numerous roles.</span></span>
-   <span data-ttu-id="e88f1-130">您可以使用不明確的準則來建立角色。</span><span class="sxs-lookup"><span data-stu-id="e88f1-130">You create roles with ambiguous criteria for who should belong to them.</span></span>
-   <span data-ttu-id="e88f1-131">在網站上有許多使用者會安裝應用程式，而使用者經常在組織內移動，並根據您所建立的角色進行變更。</span><span class="sxs-lookup"><span data-stu-id="e88f1-131">There are many users at the site where the application is installed, and users are frequently moving within the organization, changing with respect to the roles you have created.</span></span>
-   <span data-ttu-id="e88f1-132">在安裝應用程式的網站上，有許多系統管理員都有責任劃分，所以熟悉應用程式安全性需求的系統管理員可能不熟悉必須使用它的大型使用者群組。</span><span class="sxs-lookup"><span data-stu-id="e88f1-132">There are many administrators at the site where the application is installed, with division of responsibilities, so that an administrator familiar with the security requirements of your application is potentially unfamiliar with the large groups of users that must use it.</span></span> <span data-ttu-id="e88f1-133">當使用者在組織內移動時，這一點特別重要，這類資訊必須妥善傳達。</span><span class="sxs-lookup"><span data-stu-id="e88f1-133">This is of particular concern as users move within the organization—such information needs to be well communicated.</span></span>

<span data-ttu-id="e88f1-134">此外，當指派給應用程式的角色數目增加時，COM + 必須花點時間來查閱這些角色中的呼叫者成員資格，而效能可能會降低。</span><span class="sxs-lookup"><span data-stu-id="e88f1-134">Additionally, as the number of roles assigned to an application increases, so does the amount of time COM+ must spend looking up caller membership in those roles, with a likely degradation in performance.</span></span>

<span data-ttu-id="e88f1-135">若要管理複雜性並減輕這些考慮，您可以使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="e88f1-135">To manage complexity and mitigate these concerns, you can use the following guidelines:</span></span>

-   <span data-ttu-id="e88f1-136">選擇自我描述性的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="e88f1-136">Choose role names that are self-descriptive.</span></span> <span data-ttu-id="e88f1-137">使其盡可能明顯地成為哪些使用者應該屬於哪些角色。</span><span class="sxs-lookup"><span data-stu-id="e88f1-137">Make it as obvious as possible which users should belong to which roles.</span></span>
-   <span data-ttu-id="e88f1-138">將以角色為基礎的原則盡可能簡單 (，且沒有較簡單的) 。</span><span class="sxs-lookup"><span data-stu-id="e88f1-138">Make your role-based policy as simple as possible (and no simpler).</span></span> <span data-ttu-id="e88f1-139">您可以選擇盡可能少的角色，同時維持有效的原則。</span><span class="sxs-lookup"><span data-stu-id="e88f1-139">Choose as few roles as you can, while maintaining an effective policy.</span></span>
-   <span data-ttu-id="e88f1-140">清楚記載您為系統管理員所建立之以角色為基礎的原則，無論角色成員資格是否很明顯 (您) 。</span><span class="sxs-lookup"><span data-stu-id="e88f1-140">Clearly document the role-based policy that you construct for administrators, whether role membership is obvious (to you).</span></span> <span data-ttu-id="e88f1-141">尤其是，請使用每個角色可用的描述欄位來描述角色的意圖。</span><span class="sxs-lookup"><span data-stu-id="e88f1-141">In particular, use the description field available for each role to describe the intent of the role.</span></span> <span data-ttu-id="e88f1-142">如果您在幾個句子中通常不能描述屬於該角色的使用者，可能會太複雜。</span><span class="sxs-lookup"><span data-stu-id="e88f1-142">If you can't describe generally who should belong to the role in a couple of sentences, it is probably too complicated.</span></span>
-   <span data-ttu-id="e88f1-143">強烈建議您應用程式的系統管理員以使用者群組（而非個別使用者）填入角色。</span><span class="sxs-lookup"><span data-stu-id="e88f1-143">Strongly suggest that administrators of your application populate roles with user groups instead of individual users.</span></span> <span data-ttu-id="e88f1-144">這是可調整規模更高的解決方案。</span><span class="sxs-lookup"><span data-stu-id="e88f1-144">This is a much more scalable solution.</span></span> <span data-ttu-id="e88f1-145">這可讓您更輕鬆地重新指派或移除使用者，因為他們會在組織內移動，並讓系統管理員隔離特定數量的監督和通訊問題。</span><span class="sxs-lookup"><span data-stu-id="e88f1-145">It makes it easier to reassign or remove users as they move within the organization and insulates administrators from a certain amount of oversight and problems in communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e88f1-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="e88f1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e88f1-147">安全性界限</span><span class="sxs-lookup"><span data-stu-id="e88f1-147">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="e88f1-148">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="e88f1-148">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="e88f1-149">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="e88f1-149">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="e88f1-150">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="e88f1-150">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



