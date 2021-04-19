---
description: 多層式應用程式安全性
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: 多層式應用程式安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972553"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="c7e4b-103">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="c7e4b-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="c7e4b-104">在資料庫中，您可以在決定要于多層式元件型應用程式中強制執行安全性的情況下，面對困難的選擇：</span><span class="sxs-lookup"><span data-stu-id="c7e4b-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="c7e4b-105">在中介層？</span><span class="sxs-lookup"><span data-stu-id="c7e4b-105">At the middle tier?</span></span> <span data-ttu-id="c7e4b-106">在元件中嗎？</span><span class="sxs-lookup"><span data-stu-id="c7e4b-106">In the components?</span></span> <span data-ttu-id="c7e4b-107">別處？</span><span class="sxs-lookup"><span data-stu-id="c7e4b-107">Somewhere else?</span></span> <span data-ttu-id="c7e4b-108">到處？</span><span class="sxs-lookup"><span data-stu-id="c7e4b-108">Everywhere?</span></span> <span data-ttu-id="c7e4b-109">隨著安全性機制的數量和複雜性增加，效能會降低，而應用程式行為會變得更不容易預測。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="c7e4b-110">不過，您必須確保資料受到保護、遵循商務規則，以及記錄重要的活動，而且您的應用程式仍可在預期的情況下為用戶端工作。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="c7e4b-111">您必須確定透過應用程式的每個用戶端路徑都正確無誤，而且您備妥的安全性檢查點也足夠。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="c7e4b-112">最困難的決策通常是要在資料庫上強制執行安全性。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="c7e4b-113">在過去，這就是安全性嚴謹的地方，因為它被認為是一台需要真正安全的那個，而且資料庫管理員很不願意信任其他人來強制執行安全性。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="c7e4b-114">但是，在資料庫上強制執行安全性可能相當昂貴，而且很難調整規模，而這是一開始撰寫多層式應用程式的重點。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="c7e4b-115">使用 COM + 進行可擴充的多層式應用程式要遵循的一般規則，可能的話，您應該盡可能在中介層的 COM + 應用程式中強制執行詳細的安全性。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="c7e4b-116">這樣做可讓您充分利用 COM + 所提供的可擴充服務。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="c7e4b-117">只有在您絕對需要時才在資料庫上進行驗證，並且完全衡量這麼做的效能含意。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="c7e4b-118">如需決定要在何處執行安全性檢查的相關問題討論，請參閱 [決定要](deciding-where-to-enforce-security.md)在哪裡強制執行安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="c7e4b-119">如需保護多層式應用程式之基本案例的討論，請參閱 [在多層式應用程式中保護資料的基本案例](basic-scenarios-for-securing-data-in-multi-tier-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e4b-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7e4b-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7e4b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e4b-121">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="c7e4b-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="c7e4b-122">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="c7e4b-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="c7e4b-123">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="c7e4b-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="c7e4b-124">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="c7e4b-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="c7e4b-125">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="c7e4b-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="c7e4b-126">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="c7e4b-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



