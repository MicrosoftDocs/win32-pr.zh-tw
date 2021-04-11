---
description: 使用以角色為基礎的安全性時，安全性呼叫內容物件可以用來存取目前呼叫的安全性資訊。
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: 存取安全性呼叫內容資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190966"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="47b0a-103">存取安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="47b0a-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="47b0a-104">使用以角色為基礎的安全性時，安全性呼叫內容物件可以用來存取目前呼叫的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="47b0a-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="47b0a-105">下列屬性集合可從安全性呼叫內容物件取得：</span><span class="sxs-lookup"><span data-stu-id="47b0a-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="47b0a-106">SecurityCallCoNtext 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="47b0a-107">SecurityCallers 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="47b0a-108">SecurityIdentity 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="47b0a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="47b0a-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="47b0a-110">SecurityCallCoNtext 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="47b0a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="47b0a-111">Property</span></span>                          | <span data-ttu-id="47b0a-112">描述</span><span class="sxs-lookup"><span data-stu-id="47b0a-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47b0a-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="47b0a-113">NumCallers</span></span><br/>             | <span data-ttu-id="47b0a-114">呼叫鏈中的呼叫端數目。</span><span class="sxs-lookup"><span data-stu-id="47b0a-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="47b0a-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="47b0a-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="47b0a-116">鏈中所有呼叫端最不安全的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="47b0a-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="47b0a-117">來電</span><span class="sxs-lookup"><span data-stu-id="47b0a-117">Callers</span></span><br/>                | <span data-ttu-id="47b0a-118">上游呼叫端身分識別的相關資訊，以 [**SecurityCallers**](securitycallers.md) 集合的形式呈現。</span><span class="sxs-lookup"><span data-stu-id="47b0a-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="47b0a-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="47b0a-119">DirectCaller</span></span><br/>           | <span data-ttu-id="47b0a-120">呼叫物件的呼叫端會直接 (，) 不會有中間的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="47b0a-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="47b0a-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="47b0a-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="47b0a-122">發出呼叫之物件的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="47b0a-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="47b0a-123">如需有關如何使用此集合的詳細資訊，Microsoft Visual Basic 開發人員應該會看到 [**SecurityCallCoNtext**](securitycallcontext.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="47b0a-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="47b0a-124">C 和 c + + 開發人員應該參考 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)。</span><span class="sxs-lookup"><span data-stu-id="47b0a-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="47b0a-125">SecurityCallers 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-125">SecurityCallers Collection</span></span>

<span data-ttu-id="47b0a-126">[**SecurityCallers**](securitycallers.md)集合表示可以使用介於0和1（含）之間的索引來取出的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="47b0a-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="47b0a-127">每個呼叫端都會以 [**SecurityIdentity**](securityidentity.md) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="47b0a-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="47b0a-128">如需此集合的詳細資訊，Visual Basic 開發人員應該會看到 [**SecurityCallers**](securitycallers.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="47b0a-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="47b0a-129">C 和 c + + 開發人員應該參考 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)。</span><span class="sxs-lookup"><span data-stu-id="47b0a-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="47b0a-130">SecurityIdentity 集合</span><span class="sxs-lookup"><span data-stu-id="47b0a-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="47b0a-131">屬性</span><span class="sxs-lookup"><span data-stu-id="47b0a-131">Property</span></span>                         | <span data-ttu-id="47b0a-132">描述</span><span class="sxs-lookup"><span data-stu-id="47b0a-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47b0a-133">SID</span><span class="sxs-lookup"><span data-stu-id="47b0a-133">SID</span></span><br/>                   | <span data-ttu-id="47b0a-134">呼叫端的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="47b0a-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="47b0a-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="47b0a-135">AccountName</span></span><br/>           | <span data-ttu-id="47b0a-136">呼叫端的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="47b0a-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="47b0a-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="47b0a-137">AuthenticationService</span></span><br/> | <span data-ttu-id="47b0a-138">使用的驗證服務，例如 NTLMSSP、Kerberos 或 SSL。</span><span class="sxs-lookup"><span data-stu-id="47b0a-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="47b0a-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="47b0a-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="47b0a-140">使用的驗證層級，代表與物件通訊時使用的保護量。</span><span class="sxs-lookup"><span data-stu-id="47b0a-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="47b0a-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="47b0a-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="47b0a-142">用戶端設定的模擬層級（如果使用了模擬）。</span><span class="sxs-lookup"><span data-stu-id="47b0a-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="47b0a-143">此層級表示用戶端提供給伺服器的授權數量。</span><span class="sxs-lookup"><span data-stu-id="47b0a-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="47b0a-144">如需此集合的詳細資訊，Visual Basic 開發人員應該會看到 [**SecurityIdentity**](securityidentity.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="47b0a-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="47b0a-145">C 和 c + + 開發人員應該參考 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)。</span><span class="sxs-lookup"><span data-stu-id="47b0a-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47b0a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="47b0a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47b0a-147">檢查角色成員資格</span><span class="sxs-lookup"><span data-stu-id="47b0a-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="47b0a-148">判斷是否已啟用 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="47b0a-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="47b0a-149">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="47b0a-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




