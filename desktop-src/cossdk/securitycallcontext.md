---
description: 提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: 'SecurityCallCoNtext 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106998962"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="e89e5-103">SecurityCallCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="e89e5-103">SecurityCallContext class</span></span>

<span data-ttu-id="e89e5-104">提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e89e5-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="e89e5-105">您也可以使用這個類別，找出物件的直接呼叫端是否為特定角色的成員，以及物件是否啟用安全性。</span><span class="sxs-lookup"><span data-stu-id="e89e5-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="e89e5-106">只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityCallCoNtext** 類別。</span><span class="sxs-lookup"><span data-stu-id="e89e5-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="e89e5-107">如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="e89e5-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="e89e5-108">執行時機</span><span class="sxs-lookup"><span data-stu-id="e89e5-108">When to implement</span></span>

<span data-ttu-id="e89e5-109">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="e89e5-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="e89e5-110">需求</span><span class="sxs-lookup"><span data-stu-id="e89e5-110">Requirement</span></span> | <span data-ttu-id="e89e5-111">值</span><span class="sxs-lookup"><span data-stu-id="e89e5-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="e89e5-112">介面</span><span class="sxs-lookup"><span data-stu-id="e89e5-112">Interfaces</span></span> | [<span data-ttu-id="e89e5-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="e89e5-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="e89e5-114">使用時機</span><span class="sxs-lookup"><span data-stu-id="e89e5-114">When to use</span></span>

<span data-ttu-id="e89e5-115">您可以使用這個類別來存取 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)的方法。</span><span class="sxs-lookup"><span data-stu-id="e89e5-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="e89e5-116">備註</span><span class="sxs-lookup"><span data-stu-id="e89e5-116">Remarks</span></span>

<span data-ttu-id="e89e5-117">您無法直接建立 **SecurityCallCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e89e5-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="e89e5-118">若要使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。</span><span class="sxs-lookup"><span data-stu-id="e89e5-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="e89e5-119">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="e89e5-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="e89e5-120">您可以使用 "COMSVCSLib. SecurityCallCoNtext" 將 SecurityCallCoNtext 物件宣告為類別名稱;它是透過呼叫 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來建立。</span><span class="sxs-lookup"><span data-stu-id="e89e5-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="e89e5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e89e5-121">Requirements</span></span>



| <span data-ttu-id="e89e5-122">需求</span><span class="sxs-lookup"><span data-stu-id="e89e5-122">Requirement</span></span> | <span data-ttu-id="e89e5-123">值</span><span class="sxs-lookup"><span data-stu-id="e89e5-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e89e5-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e89e5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e89e5-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e89e5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e89e5-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e89e5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e89e5-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e89e5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e89e5-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e89e5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89e5-129"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="e89e5-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e89e5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e89e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89e5-131">**GetSecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e89e5-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="e89e5-132">**ISecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e89e5-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="e89e5-133">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="e89e5-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="e89e5-134">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="e89e5-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="e89e5-135">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="e89e5-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="e89e5-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="e89e5-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

