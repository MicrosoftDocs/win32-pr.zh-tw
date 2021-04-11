---
description: 提供呼叫端集合中個別呼叫端的相關資訊。 集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: 'SecurityCallers 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317852"
---
# <a name="securitycallers-class"></a><span data-ttu-id="3f124-104">SecurityCallers 類別</span><span class="sxs-lookup"><span data-stu-id="3f124-104">SecurityCallers class</span></span>

<span data-ttu-id="3f124-105">提供呼叫端集合中個別呼叫端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f124-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="3f124-106">集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="3f124-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="3f124-107">只有跨越已檢查安全性之界限的呼叫端才會包含在呼叫端鏈中。</span><span class="sxs-lookup"><span data-stu-id="3f124-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="3f124-108"> (在 COM + 環境中，系統會在應用程式界限檢查安全性。您可以透過 [**SecurityIdentity**](securityidentity.md) 類別（身分識別集合）提供有關特定呼叫端身分識別的資訊 ) 存取。</span><span class="sxs-lookup"><span data-stu-id="3f124-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="3f124-109">只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityCallers** 類別。</span><span class="sxs-lookup"><span data-stu-id="3f124-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="3f124-110">如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="3f124-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="3f124-111">執行時機</span><span class="sxs-lookup"><span data-stu-id="3f124-111">When to implement</span></span>

<span data-ttu-id="3f124-112">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="3f124-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="3f124-113">需求</span><span class="sxs-lookup"><span data-stu-id="3f124-113">Requirement</span></span> | <span data-ttu-id="3f124-114">值</span><span class="sxs-lookup"><span data-stu-id="3f124-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="3f124-115">介面</span><span class="sxs-lookup"><span data-stu-id="3f124-115">Interfaces</span></span> | [<span data-ttu-id="3f124-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="3f124-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="3f124-117">使用時機</span><span class="sxs-lookup"><span data-stu-id="3f124-117">When to use</span></span>

<span data-ttu-id="3f124-118">您可以使用這個類別來存取 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)的方法。</span><span class="sxs-lookup"><span data-stu-id="3f124-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f124-119">備註</span><span class="sxs-lookup"><span data-stu-id="3f124-119">Remarks</span></span>

<span data-ttu-id="3f124-120">您無法直接建立 **SecurityCallers** 物件。</span><span class="sxs-lookup"><span data-stu-id="3f124-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="3f124-121">若要使用 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。</span><span class="sxs-lookup"><span data-stu-id="3f124-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="3f124-122">接下來，呼叫 [**ISecurityCallCoNtext：： get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) ，要求 (安全性識別集合的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。</span><span class="sxs-lookup"><span data-stu-id="3f124-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="3f124-123">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="3f124-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="3f124-124">您無法直接建立 SecurityCallers 物件。</span><span class="sxs-lookup"><span data-stu-id="3f124-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="3f124-125">若要使用其屬性，您必須使用 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來取得其執行的參考。</span><span class="sxs-lookup"><span data-stu-id="3f124-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="3f124-126">接下來，取得物件的 Item 屬性，要求安全性識別集合 (的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。</span><span class="sxs-lookup"><span data-stu-id="3f124-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="3f124-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f124-127">Requirements</span></span>



| <span data-ttu-id="3f124-128">需求</span><span class="sxs-lookup"><span data-stu-id="3f124-128">Requirement</span></span> | <span data-ttu-id="3f124-129">值</span><span class="sxs-lookup"><span data-stu-id="3f124-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f124-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f124-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3f124-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f124-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3f124-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f124-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3f124-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f124-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3f124-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3f124-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f124-135"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f124-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f124-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f124-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f124-137">**GetSecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="3f124-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="3f124-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="3f124-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="3f124-139">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="3f124-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="3f124-140">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="3f124-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="3f124-141">**SecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="3f124-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="3f124-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="3f124-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

