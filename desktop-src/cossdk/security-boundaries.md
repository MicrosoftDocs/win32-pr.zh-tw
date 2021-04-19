---
description: 只會在應用程式界限檢查安全性。
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: 安全性界限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972148"
---
# <a name="security-boundaries"></a><span data-ttu-id="3c809-103">安全性界限</span><span class="sxs-lookup"><span data-stu-id="3c809-103">Security Boundaries</span></span>

<span data-ttu-id="3c809-104">只會在應用程式界限檢查安全性。</span><span class="sxs-lookup"><span data-stu-id="3c809-104">Security is checked only at application boundaries.</span></span> <span data-ttu-id="3c809-105">也就是說，在同一個應用程式的兩個元件中，當某個元件呼叫另一個元件時，不會執行任何安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="3c809-105">That is, for two components in the same application, when one component calls the other, no security check will be done.</span></span> <span data-ttu-id="3c809-106">不過，如果兩個應用程式共用相同的進程，而其中一個元件呼叫另一個元件，則會進行安全性檢查，因為已超過應用程式界限。</span><span class="sxs-lookup"><span data-stu-id="3c809-106">However, if two applications share the same process and a component in one calls a component in the other, a security check is done because an application boundary is crossed.</span></span> <span data-ttu-id="3c809-107">同樣地，如果有兩個應用程式位於不同的伺服器進程，而第一個應用程式中的元件呼叫第二個應用程式中的元件，則會完成安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="3c809-107">Likewise, if two applications reside in different server processes and a component in the first application calls a component in the second application, a security check is done.</span></span>

<span data-ttu-id="3c809-108">因此，如果您有兩個元件，而且您想要在一個呼叫另一個元件時完成安全性檢查，您必須將元件放在不同的 COM + 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="3c809-108">Therefore, if you have two components and you want security checks to be done when one calls the other, you need to put the components in separate COM+ applications.</span></span>

<span data-ttu-id="3c809-109">由於 COM + 程式庫應用程式是由其他進程所裝載，因此程式庫應用程式和裝載進程之間會有一個安全性界限。</span><span class="sxs-lookup"><span data-stu-id="3c809-109">Because COM+ library applications are hosted by other processes, there is a security boundary between the library application and the hosting process.</span></span> <span data-ttu-id="3c809-110">此外，程式庫應用程式不會控制進程層級的安全性，這會影響您需要為其設定安全性的方式。</span><span class="sxs-lookup"><span data-stu-id="3c809-110">Additionally, the library application doesn't control process-level security, which affects how you need to configure security for it.</span></span> <span data-ttu-id="3c809-111">如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-111">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="3c809-112">決定是否必須在呼叫元件時執行安全性檢查，是根據設定的元件具現化時所建立物件內容上的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="3c809-112">Determining whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span> <span data-ttu-id="3c809-113">如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-113">For more information, see [Security Context Property](security-context-property.md).</span></span>

## <a name="component-level-access-checks"></a><span data-ttu-id="3c809-114">Component-Level 存取檢查</span><span class="sxs-lookup"><span data-stu-id="3c809-114">Component-Level Access Checks</span></span>

<span data-ttu-id="3c809-115">若是 COM + 伺服器應用程式，您可以選擇在元件層級或在進程層級強制執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="3c809-115">For a COM+ server application, you have the choice of enforcing access checks either at the component level or at the process level.</span></span>

<span data-ttu-id="3c809-116">當您選取元件層級存取檢查時，您會啟用更細緻的角色指派。</span><span class="sxs-lookup"><span data-stu-id="3c809-116">When you select component-level access checking, you enable fine-grained role assignments.</span></span> <span data-ttu-id="3c809-117">您可以將角色指派給元件、介面和方法，並達成有明確的授權原則。</span><span class="sxs-lookup"><span data-stu-id="3c809-117">You can assign roles to components, interfaces, and methods and achieve an articulated authorization policy.</span></span> <span data-ttu-id="3c809-118">這會是使用以角色為基礎的安全性之應用程式的標準設定。</span><span class="sxs-lookup"><span data-stu-id="3c809-118">This will be the standard configuration for applications using role-based security.</span></span>

<span data-ttu-id="3c809-119">若是 COM + 程式庫應用程式，如果您想要使用角色，則必須選取元件層級安全性。</span><span class="sxs-lookup"><span data-stu-id="3c809-119">For COM+ library applications, you must select component-level security if you want to use roles.</span></span> <span data-ttu-id="3c809-120">程式庫應用程式無法使用進程層級安全性。</span><span class="sxs-lookup"><span data-stu-id="3c809-120">Library applications cannot use process-level security.</span></span>

<span data-ttu-id="3c809-121">如果您使用以程式設計的角色為基礎的安全性，則應該選取元件層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="3c809-121">You should select component-level access checking if you are using programmatic role-based security.</span></span> <span data-ttu-id="3c809-122">只有在啟用元件層級安全性時，才可使用安全性呼叫內容資訊。</span><span class="sxs-lookup"><span data-stu-id="3c809-122">Security call context information is available only when component-level security is enabled.</span></span> <span data-ttu-id="3c809-123">如需詳細資訊，請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-123">For more information, see [Security Call Context Information](security-call-context-information.md).</span></span>

<span data-ttu-id="3c809-124">此外，當您選取元件層級存取檢查時，安全性屬性將會包含在物件內容中。</span><span class="sxs-lookup"><span data-stu-id="3c809-124">Additionally, when you select component-level access checking, the security property will be included on the object context.</span></span> <span data-ttu-id="3c809-125">這表示安全性設定可以在物件啟動的方式中扮演角色。</span><span class="sxs-lookup"><span data-stu-id="3c809-125">This means that security configuration can play a role in how the object is activated.</span></span> <span data-ttu-id="3c809-126">如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-126">For more information, see [Security Context Property](security-context-property.md).</span></span>

## <a name="process-level-access-checks"></a><span data-ttu-id="3c809-127">Process-Level 存取檢查</span><span class="sxs-lookup"><span data-stu-id="3c809-127">Process-Level Access Checks</span></span>

<span data-ttu-id="3c809-128">進程層級檢查只適用于應用程式界限。</span><span class="sxs-lookup"><span data-stu-id="3c809-128">Process-level checks apply only to the application boundary.</span></span> <span data-ttu-id="3c809-129">也就是說，您針對整個 COM + 應用程式所定義的角色，將會決定誰被授與應用程式內任何資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="3c809-129">That is, the roles that you have defined for the whole COM+ application will determine who is granted access to any resource within the application.</span></span> <span data-ttu-id="3c809-130">不會套用更細緻的角色指派。</span><span class="sxs-lookup"><span data-stu-id="3c809-130">No finer-grained role assignments apply.</span></span> <span data-ttu-id="3c809-131">基本上，角色是用來建立安全描述項，以針對應用程式元件的任何呼叫進行驗證。</span><span class="sxs-lookup"><span data-stu-id="3c809-131">Essentially, the roles are used to create a security descriptor against which any call into the application's components is validated.</span></span> <span data-ttu-id="3c809-132">在此情況下，您不會想要建立具有多個角色的詳細授權原則。</span><span class="sxs-lookup"><span data-stu-id="3c809-132">In this case, you would not want to construct a detailed authorization policy with multiple roles.</span></span> <span data-ttu-id="3c809-133">應用程式會使用單一安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3c809-133">The application will use a single security descriptor.</span></span>

<span data-ttu-id="3c809-134">若是 COM + 程式庫應用程式，則不會選取進程層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="3c809-134">For COM+ library applications, you would not select process-level access checks.</span></span> <span data-ttu-id="3c809-135">程式庫應用程式將會在用戶端的進程中執行，因此不會控制進程層級安全性。</span><span class="sxs-lookup"><span data-stu-id="3c809-135">The library application will run hosted in the client's process and hence will not control process-level security.</span></span> <span data-ttu-id="3c809-136">如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-136">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="3c809-137">啟用進程層級的存取檢查後，就無法使用安全性呼叫內容資訊。</span><span class="sxs-lookup"><span data-stu-id="3c809-137">With process-level access checks enabled, security call context information is not available.</span></span> <span data-ttu-id="3c809-138">這表示，當您只使用進程層級安全性時，不能以程式設計的方式進行安全性。</span><span class="sxs-lookup"><span data-stu-id="3c809-138">This means that you cannot do programmatic security when using only process-level security.</span></span> <span data-ttu-id="3c809-139">如需詳細資訊，請參閱 [安全性呼叫內容資訊](security-call-context-information.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-139">For more information, see [Security Call Context Information](security-call-context-information.md).</span></span>

<span data-ttu-id="3c809-140">此外，安全性屬性不會包含在物件內容中。</span><span class="sxs-lookup"><span data-stu-id="3c809-140">Additionally, the security property will not be included on the object context.</span></span> <span data-ttu-id="3c809-141">這表示，在只使用進程層級的存取檢查時，安全性設定永遠不會在物件的啟用方式中扮演角色。</span><span class="sxs-lookup"><span data-stu-id="3c809-141">This means that when using only process-level access checks, security configuration will never play a role in how the object is activated.</span></span> <span data-ttu-id="3c809-142">如需詳細資訊，請參閱 [資訊安全內容屬性](security-context-property.md)。</span><span class="sxs-lookup"><span data-stu-id="3c809-142">For more information, see [Security Context Property](security-context-property.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c809-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c809-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c809-144">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="3c809-144">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="3c809-145">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="3c809-145">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="3c809-146">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="3c809-146">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="3c809-147">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="3c809-147">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



