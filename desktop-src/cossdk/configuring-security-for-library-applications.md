---
description: 針對程式庫應用程式設定以角色為基礎的安全性和驗證時，有一些特殊考慮。
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: 設定程式庫應用程式的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102d6a0f102bfd19da0073bca14df8a8211203b1
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "103945552"
---
# <a name="configuring-security-for-library-applications"></a><span data-ttu-id="fb737-103">設定程式庫應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="fb737-103">Configuring Security for Library Applications</span></span>

<span data-ttu-id="fb737-104">針對程式庫應用程式設定以角色為基礎的安全性和驗證時，有一些特殊考慮。</span><span class="sxs-lookup"><span data-stu-id="fb737-104">There are special considerations in configuring role-based security and authentication for library applications.</span></span>

## <a name="enabling-or-disabling-authentication"></a><span data-ttu-id="fb737-105">啟用或停用驗證</span><span class="sxs-lookup"><span data-stu-id="fb737-105">Enabling or Disabling Authentication</span></span>

<span data-ttu-id="fb737-106">其中一個要考慮的因素是，程式庫應用程式的呼叫端是否應受限於裝載進程的進程層級安全性檢查，也就是是否要啟用或停用驗證。</span><span class="sxs-lookup"><span data-stu-id="fb737-106">One of the factors to consider is whether callers of the library application should be subject to the process-level security checks of the hosting process—that is, whether to enable or disable authentication.</span></span>

<span data-ttu-id="fb737-107">例如，如果程式庫應用程式將由瀏覽器主控，則可能需要接收未經驗證的回呼。</span><span class="sxs-lookup"><span data-stu-id="fb737-107">For example, if the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span> <span data-ttu-id="fb737-108">若要解決此需求，您可以停用驗證，讓裝載進程不會針對程式庫應用程式的呼叫端執行安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-108">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="fb737-109">當您停用驗證時，程式庫應用程式會有效地未經驗證，而且所有對它的呼叫都會成功。</span><span class="sxs-lookup"><span data-stu-id="fb737-109">When you disable authentication, the library application effectively goes unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="fb737-110">程式庫應用程式的呼叫端不受限於裝載進程的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-110">Callers of the library application are not subject to the security checks of the hosting process.</span></span> <span data-ttu-id="fb737-111">基本上，程式庫應用程式會標記為「未經驗證」，而且會針對程式庫應用程式的呼叫省略安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-111">Basically, the library application is tagged as "unauthenticated", and security checks are omitted for calls to the library application.</span></span>

<span data-ttu-id="fb737-112">如需如何啟用或停用驗證的詳細資訊，請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。</span><span class="sxs-lookup"><span data-stu-id="fb737-112">For information about how to enable or disable authentication, see [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span>

## <a name="enforcing-role-checks"></a><span data-ttu-id="fb737-113">強制執行角色檢查</span><span class="sxs-lookup"><span data-stu-id="fb737-113">Enforcing Role Checks</span></span>

<span data-ttu-id="fb737-114">另一個要做的決定是程式庫應用程式是否應該使用以 [角色為基礎的安全性](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="fb737-114">Another decision to make is whether the library application should use [role-based security](role-based-security-administration.md).</span></span> <span data-ttu-id="fb737-115">如果使用以角色為基礎的安全性，您必須使用元件層級安全性，才能執行任何存取檢查。指派給程式庫應用程式的角色不會反映在進程安全描述項中。</span><span class="sxs-lookup"><span data-stu-id="fb737-115">If role-based security is used, you must be using component-level security for any access checks to be carried out. The roles assigned to the library application are not reflected in the process security descriptor.</span></span> <span data-ttu-id="fb737-116">程式庫應用程式可以控制的唯一授權是在元件層級。</span><span class="sxs-lookup"><span data-stu-id="fb737-116">The only authorization that the library application can control is at the component level.</span></span> <span data-ttu-id="fb737-117">如需元件層級安全性的詳細資訊，請參閱 [安全性界限](security-boundaries.md)。</span><span class="sxs-lookup"><span data-stu-id="fb737-117">For more information about component-level security, see [Security Boundaries](security-boundaries.md).</span></span>

<span data-ttu-id="fb737-118">若要瞭解如何設定元件層級安全性，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="fb737-118">To see how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

## <a name="configuration-scenarios"></a><span data-ttu-id="fb737-119">設定案例</span><span class="sxs-lookup"><span data-stu-id="fb737-119">Configuration Scenarios</span></span>

<span data-ttu-id="fb737-120">若要進一步瞭解如何決定程式庫應用程式是否應該使用以角色為基礎的安全性，以及程式庫應用程式是否應該未經驗證，請考慮下列案例：</span><span class="sxs-lookup"><span data-stu-id="fb737-120">To better understand the implications of deciding whether the library application should use role-based security and whether the library application should be unauthenticated, consider the following scenarios:</span></span>

-   <span data-ttu-id="fb737-121">**驗證已啟用，而且會使用以角色為基礎的安全性。**</span><span class="sxs-lookup"><span data-stu-id="fb737-121">**Authentication is enabled, and role-based security is used.**</span></span> <span data-ttu-id="fb737-122">在此案例中，安全性檢查是由裝載進程進行，而某些呼叫端在進程層級遭到拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="fb737-122">In this scenario, security checks are made by the hosting process and some callers are denied access at the process level.</span></span> <span data-ttu-id="fb737-123">此外，也會在程式庫應用層級進行角色檢查，以便在檢查角色成員資格時，讓它透過處理層級安全性檢查的某些呼叫者拒絕存取程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb737-123">Also, role checking is done at the library application level so that some callers who make it through the process-level security check are denied access to the library application when role membership is checked.</span></span> <span data-ttu-id="fb737-124">這是使用以角色為基礎之安全性的 COM + 程式庫應用程式的一般案例。</span><span class="sxs-lookup"><span data-stu-id="fb737-124">This is the usual scenario for a COM+ library application that uses role-based security.</span></span>

    <span data-ttu-id="fb737-125">下圖顯示啟用驗證和使用角色檢查的案例。</span><span class="sxs-lookup"><span data-stu-id="fb737-125">The following illustration shows the scenario where authentication is enabled and role checking is used.</span></span>

    ![顯示在主機進程內進行驗證的圖表。](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   <span data-ttu-id="fb737-127">**驗證已啟用，且未使用以角色為基礎的安全性。**</span><span class="sxs-lookup"><span data-stu-id="fb737-127">**Authentication is enabled, and role-based security is not used.**</span></span> <span data-ttu-id="fb737-128">在此案例中，安全性檢查是在進程層級完成，但不會在程式庫應用層級檢查角色成員資格。</span><span class="sxs-lookup"><span data-stu-id="fb737-128">In this scenario, security checks are done at the process level but role membership is not checked at the library application level.</span></span> <span data-ttu-id="fb737-129">因此，程式庫應用程式的任何呼叫端會透過處理層級的安全性檢查來存取程式庫應用程式，因為不會檢查角色成員資格。</span><span class="sxs-lookup"><span data-stu-id="fb737-129">Therefore, any caller of the library application that makes it through the process-level security check will be given access to the library application because role membership is not being checked.</span></span> <span data-ttu-id="fb737-130">當未使用以角色為基礎的安全性的 COM 應用程式遷移至 COM + 程式庫應用程式時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="fb737-130">This situation would exist when a COM application that doesn't use role-based security is migrated to a COM+ library application.</span></span>

    <span data-ttu-id="fb737-131">下圖顯示已啟用驗證且未使用角色檢查的案例。</span><span class="sxs-lookup"><span data-stu-id="fb737-131">The following illustration shows the scenario where authentication is enabled and role checking is not being used.</span></span>

    ![此圖顯示主機進程內程式庫應用程式的進程層級驗證。](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   <span data-ttu-id="fb737-133">**驗證已停用，並使用以角色為基礎的安全性。**</span><span class="sxs-lookup"><span data-stu-id="fb737-133">**Authentication is disabled, and role-based security is used.**</span></span> <span data-ttu-id="fb737-134">在此案例中，系統會在進程層級進行安全性檢查，但不會驗證程式庫應用程式的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="fb737-134">In this scenario, security checks are being done at the process level but callers to the library application are unauthenticated.</span></span> <span data-ttu-id="fb737-135">實際上，程式庫應用程式的呼叫端豁免于進程層級的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-135">In effect, callers of the library application are exempt from the process-level security check.</span></span> <span data-ttu-id="fb737-136">由於已啟用角色檢查，角色成員資格會自行決定誰可以存取程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb737-136">Because role checking is enabled, role membership alone determines who is given access to the library application.</span></span> <span data-ttu-id="fb737-137">當裝載進程所執行的安全性檢查過於嚴格，但您在程式庫應用程式或特定介面或方法上需要有一些存取限制時，此案例可能很適合。</span><span class="sxs-lookup"><span data-stu-id="fb737-137">This scenario might be appropriate when the security check that would be done by the hosting process is too restrictive but you need to have some access restriction on the library application or on specific interfaces or methods.</span></span> <span data-ttu-id="fb737-138">此案例可讓您有效地關閉進程安全性，並使用以角色為基礎的安全性，仍具有適當的層級存取檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-138">This scenario enables you to effectively turn off process security and still have an appropriate level access checks using role-based security.</span></span>

    <span data-ttu-id="fb737-139">下圖顯示已停用驗證和角色檢查的案例。</span><span class="sxs-lookup"><span data-stu-id="fb737-139">The scenario where authentication is disabled and role checking is being used is shown in the following illustration.</span></span>

    ![在主機進程內的程式庫應用程式中顯示「檢查角色成員資格」的圖表。](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   <span data-ttu-id="fb737-141">**驗證已停用，且未使用以角色為基礎的安全性。**</span><span class="sxs-lookup"><span data-stu-id="fb737-141">**Authentication is disabled, and role-based security is not used.**</span></span> <span data-ttu-id="fb737-142">在此案例中，安全性檢查仍會在進程層級進行，但在上述案例中，程式庫應用程式的呼叫端一律會通過此安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="fb737-142">In this scenario, security checks are still done at the process level but, as in the preceding scenario, callers of the library application always pass this security check.</span></span> <span data-ttu-id="fb737-143">因為也會停用角色檢查，所以不會在程式庫應用層級檢查角色成員資格。</span><span class="sxs-lookup"><span data-stu-id="fb737-143">Because role checking is also disabled, role membership is not checked at the library application level.</span></span> <span data-ttu-id="fb737-144">基本上，任何人都可以呼叫程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb737-144">Essentially, anyone can call the library application.</span></span> <span data-ttu-id="fb737-145">當您的 COM 物件需要接收未經驗證的回呼時，應選擇此案例，例如 Internet Explorer 所裝載的 ActiveX 控制項和 Microsoft Management Console 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="fb737-145">This scenario should be chosen when your COM object needs to receive unauthenticated callbacks, as might be the case with an ActiveX control hosted by Internet Explorer and with a Microsoft Management Console snap-in.</span></span> <span data-ttu-id="fb737-146">當然，這個 COM 物件必須受到信任，才能在接收未驗證的呼叫時適當地運作。</span><span class="sxs-lookup"><span data-stu-id="fb737-146">Of course, this COM object must be trusted to behave appropriately when receiving unauthenticated calls.</span></span> <span data-ttu-id="fb737-147">例如，它不應該代表其呼叫端存取任意檔案。</span><span class="sxs-lookup"><span data-stu-id="fb737-147">For example, it should not access arbitrary files on behalf of its callers.</span></span>

    <span data-ttu-id="fb737-148">下圖顯示已停用驗證和角色檢查的案例。</span><span class="sxs-lookup"><span data-stu-id="fb737-148">The scenario where authentication is disabled and role checking is not being used is shown in the following illustration.</span></span>

    ![顯示在主機進程內未經驗證的程式庫應用程式呼叫的圖表。](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

<span data-ttu-id="fb737-150">當您決定要啟用或停用 COM + 程式庫應用程式的驗證之後，請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md) ，以取得說明如何停用 (或使用 [元件服務] 系統管理工具啟用) 驗證的逐步程式。</span><span class="sxs-lookup"><span data-stu-id="fb737-150">After you have decided whether to enable or disable authentication for your COM+ library application, see [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md) for a step-by-step procedure that explains how to disable (or enable) authentication using the Component Services administrative tool.</span></span> <span data-ttu-id="fb737-151">如果您的程式庫應用程式將會使用以角色為基礎的安全性，請參閱設定 [Role-Based 安全性](configuring-role-based-security.md)。</span><span class="sxs-lookup"><span data-stu-id="fb737-151">If your library application will use role-based security, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb737-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb737-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb737-153">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="fb737-153">Library Application Security</span></span>](library-application-security.md)
</dt> </dl>

 

 



