---
description: 檢查角色成員資格
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: 檢查角色成員資格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689012"
---
# <a name="checking-role-membership"></a><span data-ttu-id="90d7a-103">檢查角色成員資格</span><span class="sxs-lookup"><span data-stu-id="90d7a-103">Checking Role Membership</span></span>

<span data-ttu-id="90d7a-104">您可以呼叫 [**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 方法，判斷物件的直接呼叫端是否為特定角色的成員。</span><span class="sxs-lookup"><span data-stu-id="90d7a-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="90d7a-105">如果您想要確保特定的程式碼區塊不會執行，除非呼叫端是特定角色的成員，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="90d7a-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="90d7a-106">例如，您可以使用 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 來確保超過指定金額的交易（例如 $1000）只由管理員角色的成員執行。</span><span class="sxs-lookup"><span data-stu-id="90d7a-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="90d7a-107">如果呼叫端不是管理員，而且交易超過 $1000，則不會執行交易，且會顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="90d7a-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="90d7a-108">存取 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 的慣用方法是透過安全性呼叫內容物件，因為您可以使用安全性呼叫內容物件的相同參考來取得安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="90d7a-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="90d7a-109">不過，您也可以從 **ObjectCoNtext** 物件存取 **IsCallerInRole** 方法。</span><span class="sxs-lookup"><span data-stu-id="90d7a-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="90d7a-110">如需詳細資訊， (查看 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 或 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 。 ) </span><span class="sxs-lookup"><span data-stu-id="90d7a-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="90d7a-111">如果您正在開發 Microsoft Visual Basic 應用程式的元件，請呼叫 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) 函式，然後使用安全性呼叫內容來呼叫 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="90d7a-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="90d7a-112">如果您正在開發 C 或 c + + 應用程式，請使用 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) 來取出 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="90d7a-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="90d7a-113">然後您會呼叫 [**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="90d7a-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="90d7a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="90d7a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d7a-115">存取安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="90d7a-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="90d7a-116">判斷是否已啟用 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="90d7a-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="90d7a-117">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="90d7a-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
