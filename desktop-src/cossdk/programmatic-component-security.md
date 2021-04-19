---
description: 當您在包含元件的 COM + 應用程式中使用以角色為基礎的安全性時，您可以從元件記憶體取程式設計的安全性功能。
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: 程式設計元件安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971961"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="68bd3-103">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="68bd3-103">Programmatic Component Security</span></span>

<span data-ttu-id="68bd3-104">當您在包含元件的 COM + 應用程式中使用以角色為基礎的安全性時，您可以從元件記憶體取程式設計的安全性功能。</span><span class="sxs-lookup"><span data-stu-id="68bd3-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="68bd3-105">您可以檢查角色成員資格，判斷是否已執行特定的程式碼區段，您可以使用安全性呼叫內容物件來存取安全性資訊，也可以判斷是否已啟用目前呼叫的安全性。</span><span class="sxs-lookup"><span data-stu-id="68bd3-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="68bd3-106">您可以使用適用于 Microsoft Visual Basic 應用程式 ([**SecurityCallCoNtext**](securitycallcontext.md) 物件的參考來執行上述所有工作) 或針對 C 和 Microsoft Visual C++ 應用程式) 的 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面 (指標。</span><span class="sxs-lookup"><span data-stu-id="68bd3-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="68bd3-107">如需有關以程式設計的角色為基礎之安全性的詳細資訊，請參閱本節中的下列主題：</span><span class="sxs-lookup"><span data-stu-id="68bd3-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="68bd3-108">檢查角色成員資格</span><span class="sxs-lookup"><span data-stu-id="68bd3-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="68bd3-109">判斷是否已啟用 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="68bd3-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="68bd3-110">存取安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="68bd3-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="68bd3-111">模擬和 COM 安全性功能</span><span class="sxs-lookup"><span data-stu-id="68bd3-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="68bd3-112">如果您的元件是在不使用角色型安全性的 COM + 應用程式中使用，則無法使用程式設計的角色檢查和安全性呼叫內容資訊。</span><span class="sxs-lookup"><span data-stu-id="68bd3-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="68bd3-113">不過，您可以使用 COM 所提供的程式設計安全性功能。</span><span class="sxs-lookup"><span data-stu-id="68bd3-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="68bd3-114">如需詳細資訊，請參閱 [COM 中的安全性](/windows/desktop/com/security-in-com)。</span><span class="sxs-lookup"><span data-stu-id="68bd3-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="68bd3-115">雖然您可以使用 COM 提供的大部分安全性功能，但您無法從屬於 COM + 應用程式一部分的元件呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，因為 **CoInitializeSecurity** 是由 com + 應用程式執行所在的代理程式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="68bd3-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="68bd3-116">不過，您可以呼叫其他安全性功能，例如 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)，以抓取用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68bd3-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="68bd3-117">尤其是當您需要使用用戶端的身分識別來存取某些資源時（例如，存取受安全描述項保護的檔案，或將用戶端的身分識別傳播至資料庫），您可以用程式設計的方式執行模擬。</span><span class="sxs-lookup"><span data-stu-id="68bd3-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="68bd3-118">如需有關何時及如何進行此作業的詳細資訊，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="68bd3-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="68bd3-119">測試安全性功能</span><span class="sxs-lookup"><span data-stu-id="68bd3-119">Testing Security Functionality</span></span>

<span data-ttu-id="68bd3-120">如果您在元件中使用 COM + 程式設計安全性，當您準備好測試元件的安全性功能時，就必須將元件整合至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="68bd3-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="68bd3-121">如果在未整合至 COM + 應用程式的情況下執行使用 COM + 程式設計安全性的元件，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="68bd3-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="68bd3-122">因此，如果您想要確保這類元件也可以成功整合至不屬於 COM + 環境的應用程式，您必須確定這些例外狀況會適當地處理。</span><span class="sxs-lookup"><span data-stu-id="68bd3-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="68bd3-123">記錄安全性需求</span><span class="sxs-lookup"><span data-stu-id="68bd3-123">Documenting Security Requirements</span></span>

<span data-ttu-id="68bd3-124">如果您要為使用以角色為基礎之安全性的 COM + 應用程式撰寫獨立元件，則需要記載元件，以便在元件整合至 COM + 應用程式時適當地設定安全性。</span><span class="sxs-lookup"><span data-stu-id="68bd3-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="68bd3-125">例如，您應該識別必須新增的角色，並說明每個角色應指派給哪些方法和介面。</span><span class="sxs-lookup"><span data-stu-id="68bd3-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="68bd3-126">此外，如果呼叫如 IsCallerInRole ( "取款" ) 的方法，您應該描述只有 Tellers 可以存取的功能。</span><span class="sxs-lookup"><span data-stu-id="68bd3-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="68bd3-127">您也應該指定是否需要角色，以協助保護整個元件的存取權。</span><span class="sxs-lookup"><span data-stu-id="68bd3-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68bd3-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="68bd3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bd3-129">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="68bd3-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="68bd3-130">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="68bd3-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="68bd3-131">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="68bd3-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="68bd3-132">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="68bd3-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="68bd3-133">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="68bd3-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="68bd3-134">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="68bd3-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
