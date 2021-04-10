---
description: 啟用存取檢查之後，您必須為您的 COM + 應用程式選取您要執行存取檢查的層級。
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: 設定存取檢查的安全性等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111280"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="d173a-103">設定存取檢查的安全性等級</span><span class="sxs-lookup"><span data-stu-id="d173a-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="d173a-104">啟用 [存取檢查](enabling-access-checks-for-an-application.md)之後，您必須為您的 com + 應用程式選取您要執行存取檢查的層級。</span><span class="sxs-lookup"><span data-stu-id="d173a-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="d173a-105">**若要選取安全性等級**</span><span class="sxs-lookup"><span data-stu-id="d173a-105">**To select a security level**</span></span>

1.  <span data-ttu-id="d173a-106">在 [元件服務] 系統管理工具的主控台樹中，以滑鼠 **按右鍵您** 要啟用存取檢查的 com + 應用程式，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="d173a-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="d173a-107">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="d173a-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="d173a-108">在 [ **安全性等級**] 底下，選取下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d173a-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="d173a-109">**只有在處理層級執行存取檢查**，此設定表示指派給應用程式的角色中的使用者將會新增至流程安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d173a-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="d173a-110">這有下列效果和含意：</span><span class="sxs-lookup"><span data-stu-id="d173a-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="d173a-111">在元件、方法和介面層級關閉更細緻的角色檢查。</span><span class="sxs-lookup"><span data-stu-id="d173a-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="d173a-112">安全性檢查只會在應用層級執行。</span><span class="sxs-lookup"><span data-stu-id="d173a-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="d173a-113">安全性屬性不會包含在應用程式中執行之任何物件的內容上。</span><span class="sxs-lookup"><span data-stu-id="d173a-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="d173a-114">這可能會影響物件的啟用方式。</span><span class="sxs-lookup"><span data-stu-id="d173a-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="d173a-115">請參閱 [資訊安全內容屬性](security-context-property.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="d173a-116">安全性呼叫內容將無法使用。</span><span class="sxs-lookup"><span data-stu-id="d173a-116">The security call context will not be made available.</span></span> <span data-ttu-id="d173a-117">依賴安全性呼叫內容資訊的程式設計安全性將無法運作。</span><span class="sxs-lookup"><span data-stu-id="d173a-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="d173a-118">請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="d173a-119">**在程式和元件層級執行存取檢查**，此設定表示將會執行進程層級的安全性描述項檢查和以角色為基礎的完整安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="d173a-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="d173a-120">這有下列效果和含意：</span><span class="sxs-lookup"><span data-stu-id="d173a-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="d173a-121">若要啟用特定元件的角色檢查，您必須 [在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="d173a-122">安全性屬性包含在應用程式內執行之任何物件的內容中。</span><span class="sxs-lookup"><span data-stu-id="d173a-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="d173a-123">這可能會影響物件的啟用方式。</span><span class="sxs-lookup"><span data-stu-id="d173a-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="d173a-124">請參閱 [資訊安全內容屬性](security-context-property.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="d173a-125">可以使用安全性呼叫內容。</span><span class="sxs-lookup"><span data-stu-id="d173a-125">The security call context is available.</span></span> <span data-ttu-id="d173a-126">啟用以程式設計的角色為基礎的安全性。</span><span class="sxs-lookup"><span data-stu-id="d173a-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="d173a-127">請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="d173a-128">針對 COM + 程式庫應用程式，您必須選擇在進程和元件層級檢查，以確定任何有意義的存取檢查可運作。</span><span class="sxs-lookup"><span data-stu-id="d173a-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="d173a-129">程式庫應用程式依賴進程層級安全性的主機進程。</span><span class="sxs-lookup"><span data-stu-id="d173a-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="d173a-130">您可以藉由 [設定驗證](enabling-authentication-for-a-library-application.md)，判斷程式庫應用程式如何與主機進程所執行的驗證互動。</span><span class="sxs-lookup"><span data-stu-id="d173a-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="d173a-131">如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="d173a-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="d173a-132">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="d173a-132">Click **OK**.</span></span>

<span data-ttu-id="d173a-133">下次啟動應用程式時，系統會在指定的層級自動檢查安全性。</span><span class="sxs-lookup"><span data-stu-id="d173a-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="d173a-134">只有指派給指派給應用程式角色的使用者才會獲得應用程式的存取權。</span><span class="sxs-lookup"><span data-stu-id="d173a-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d173a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d173a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d173a-136">將角色指派給元件、介面或方法</span><span class="sxs-lookup"><span data-stu-id="d173a-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="d173a-137">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="d173a-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="d173a-138">定義應用程式的角色</span><span class="sxs-lookup"><span data-stu-id="d173a-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="d173a-139">啟用應用程式的存取檢查</span><span class="sxs-lookup"><span data-stu-id="d173a-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="d173a-140">在元件層級啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="d173a-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



