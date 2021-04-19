---
description: 本主題提供幾個構成區塊的案例，其中說明決定要如何強制執行安全性的準則。
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: 在多層式應用程式中保護資料的基本案例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972563"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="4796e-103">在多層式應用程式中保護資料的基本案例</span><span class="sxs-lookup"><span data-stu-id="4796e-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="4796e-104">本主題提供幾個構成區塊的案例， [其中說明決定要如何強制執行安全性](deciding-where-to-enforce-security.md)的準則。</span><span class="sxs-lookup"><span data-stu-id="4796e-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="4796e-105">信任的伺服器案例</span><span class="sxs-lookup"><span data-stu-id="4796e-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="4796e-106">資料庫會完全信任 COM + 應用程式，以驗證和授權終端使用者存取資料庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="4796e-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="4796e-107">最好的情況是，資料庫會受到保護，除非透過應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="4796e-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="4796e-108">COM + 應用程式會使用以角色為基礎的安全性來授權使用者。</span><span class="sxs-lookup"><span data-stu-id="4796e-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="4796e-109">連接會以 COM + 應用程式的身分識別來開啟，並完全共用。</span><span class="sxs-lookup"><span data-stu-id="4796e-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="4796e-110">您可以透過 COM + 應用程式來完成審核和記錄，也可以由應用程式將這項資訊傳遞到資料庫中。</span><span class="sxs-lookup"><span data-stu-id="4796e-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="4796e-111">此案例最適用于可透過可預測的使用者類別（可在角色中封裝）存取的資料。</span><span class="sxs-lookup"><span data-stu-id="4796e-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="4796e-112">例如，只有「管理員」、「Tellers」和「會計」具有存取帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="4796e-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="4796e-113">在中介層強制執行每個精確的商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="4796e-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="4796e-114">模擬案例</span><span class="sxs-lookup"><span data-stu-id="4796e-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="4796e-115">資料庫會自行驗證及授權使用者，以協助限制資料庫中資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="4796e-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="4796e-116">COM + 應用程式會在每次存取資料庫時模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="4796e-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="4796e-117">連接是以每次呼叫為基礎進行，無法重複使用。</span><span class="sxs-lookup"><span data-stu-id="4796e-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="4796e-118">此案例最適用于緊密系結至極小使用者類別的資料。</span><span class="sxs-lookup"><span data-stu-id="4796e-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="4796e-119">例如，每個員工只能存取自己的人員檔案，而且每個經理只能存取其報表的人員檔案。</span><span class="sxs-lookup"><span data-stu-id="4796e-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="4796e-120"> 混合式案例</span><span class="sxs-lookup"><span data-stu-id="4796e-120">Hybrid Scenario</span></span>

<span data-ttu-id="4796e-121">上述兩個案例的組合，其中只會在需要時使用模擬。</span><span class="sxs-lookup"><span data-stu-id="4796e-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="4796e-122">在您有混合式使用者資料關聯性的情況下，此案例的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="4796e-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="4796e-123">例如，您有「經理」、「Tellers」、「會計」和數千個個別的 Web 用戶端，他們只可以存取自己的帳戶。</span><span class="sxs-lookup"><span data-stu-id="4796e-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="4796e-124">您可以透過應用程式來分隔邏輯路徑（可能使用個別的元件）來處理後者的使用者類別，特別是在這些使用者的效能假設不同的情況下。</span><span class="sxs-lookup"><span data-stu-id="4796e-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="4796e-125">使用 Microsoft SQL Server 角色的信任案例</span><span class="sxs-lookup"><span data-stu-id="4796e-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="4796e-126">Microsoft SQL Server 7.0 和更新版本可以使用角色來授與特定資料列的存取權，但信任 COM + 應用程式來驗證和授權使用者，以及將它們對應到資料庫中的正確角色。</span><span class="sxs-lookup"><span data-stu-id="4796e-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="4796e-127">COM + 應用程式會使用以角色為基礎的安全性來授與使用者，而且應用程式角色也適合資料庫角色。</span><span class="sxs-lookup"><span data-stu-id="4796e-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="4796e-128">您可以開啟特定資料庫角色的特定連接。</span><span class="sxs-lookup"><span data-stu-id="4796e-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="4796e-129">如果在 COM + 應用程式中的集區物件持有這些連線，就可以重複使用這些連接。</span><span class="sxs-lookup"><span data-stu-id="4796e-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="4796e-130">如需如何進行此作業的詳細資訊，請參閱 [Com + 物件](com--object-pooling.md)共用。</span><span class="sxs-lookup"><span data-stu-id="4796e-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="4796e-131">您可以透過 COM + 應用程式來完成審核和記錄，也可以由應用程式將這項資訊傳遞給資料庫。</span><span class="sxs-lookup"><span data-stu-id="4796e-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="4796e-132">此案例最適合一般與第一個受信任的伺服器案例中相同類型的使用者和資料，因為 COM + 應用程式仍然會受到信任，以正確地處理授權。</span><span class="sxs-lookup"><span data-stu-id="4796e-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="4796e-133">不過，它可協助保護資料庫免于遭受未經授權的存取，同時允許來自 COM + 應用程式外部多個來源的存取，而不會導致模擬案例的調整和效能受到影響。</span><span class="sxs-lookup"><span data-stu-id="4796e-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4796e-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="4796e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4796e-135">決定要在哪裡強制執行安全性</span><span class="sxs-lookup"><span data-stu-id="4796e-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="4796e-136">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="4796e-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



