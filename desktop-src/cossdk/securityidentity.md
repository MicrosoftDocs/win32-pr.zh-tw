---
description: 提供安全性資訊集合的存取，代表呼叫者的身分識別。 使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: 'SecurityIdentity 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103696321"
---
# <a name="securityidentity-class"></a><span data-ttu-id="012c8-104">SecurityIdentity 類別</span><span class="sxs-lookup"><span data-stu-id="012c8-104">SecurityIdentity class</span></span>

<span data-ttu-id="012c8-105">提供安全性資訊集合的存取，代表呼叫者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="012c8-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="012c8-106">使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="012c8-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="012c8-107">如需如何存取安全性呼叫內容資訊的詳細資訊，請參閱程式設計元件安全性。</span><span class="sxs-lookup"><span data-stu-id="012c8-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="012c8-108">只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityIdentity** 類別。</span><span class="sxs-lookup"><span data-stu-id="012c8-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="012c8-109">如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="012c8-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="012c8-110">執行時機</span><span class="sxs-lookup"><span data-stu-id="012c8-110">When to implement</span></span>

<span data-ttu-id="012c8-111">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="012c8-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="012c8-112">需求</span><span class="sxs-lookup"><span data-stu-id="012c8-112">Requirement</span></span> | <span data-ttu-id="012c8-113">值</span><span class="sxs-lookup"><span data-stu-id="012c8-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="012c8-114">介面</span><span class="sxs-lookup"><span data-stu-id="012c8-114">Interfaces</span></span> | [<span data-ttu-id="012c8-115">**ISecurityIdentityColl**</span><span class="sxs-lookup"><span data-stu-id="012c8-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="012c8-116">使用時機</span><span class="sxs-lookup"><span data-stu-id="012c8-116">When to use</span></span>

<span data-ttu-id="012c8-117">您可以使用這個類別來存取 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)的方法。</span><span class="sxs-lookup"><span data-stu-id="012c8-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="012c8-118">備註</span><span class="sxs-lookup"><span data-stu-id="012c8-118">Remarks</span></span>

<span data-ttu-id="012c8-119">您無法直接建立 **SecurityIdentity** 物件。</span><span class="sxs-lookup"><span data-stu-id="012c8-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="012c8-120">若要使用 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。</span><span class="sxs-lookup"><span data-stu-id="012c8-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="012c8-121">接下來，呼叫 [**ISecurityCallCoNtext：： get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) ，要求 (安全性識別集合的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。</span><span class="sxs-lookup"><span data-stu-id="012c8-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="012c8-122">然後呼叫 [**ISecurityIdentityColl：： get \_ 專案**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) 以抓取 (的安全性識別專案，例如 "Name" 或 "AuthenticationService" ) 。</span><span class="sxs-lookup"><span data-stu-id="012c8-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="012c8-123">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="012c8-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="012c8-124">您無法直接建立 SecurityIdentity 物件。</span><span class="sxs-lookup"><span data-stu-id="012c8-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="012c8-125">若要使用其屬性，您必須使用 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來取得其執行的參考。</span><span class="sxs-lookup"><span data-stu-id="012c8-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="012c8-126">接下來，取得物件的 Item 屬性，要求安全性識別集合 (的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。</span><span class="sxs-lookup"><span data-stu-id="012c8-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="012c8-127">然後，使用 SecurityIdentity 物件的 Item 屬性來取出安全性識別專案 (例如 "Name" 或 "AuthenticationService" ) 。</span><span class="sxs-lookup"><span data-stu-id="012c8-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="012c8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="012c8-128">Requirements</span></span>



| <span data-ttu-id="012c8-129">需求</span><span class="sxs-lookup"><span data-stu-id="012c8-129">Requirement</span></span> | <span data-ttu-id="012c8-130">值</span><span class="sxs-lookup"><span data-stu-id="012c8-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="012c8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="012c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="012c8-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="012c8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="012c8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="012c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="012c8-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="012c8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="012c8-135">標頭</span><span class="sxs-lookup"><span data-stu-id="012c8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="012c8-136"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="012c8-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="012c8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="012c8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012c8-138">**GetSecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="012c8-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="012c8-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="012c8-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="012c8-140">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="012c8-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="012c8-141">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="012c8-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="012c8-142">**SecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="012c8-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="012c8-143">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="012c8-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

