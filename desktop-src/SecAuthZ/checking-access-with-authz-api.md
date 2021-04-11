---
description: 應用程式會藉由呼叫 AuthzAccessCheck 函式來判斷是否要授與安全物件的存取權。
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: 使用 Authz API 檢查存取權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848157"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="e2933-103">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="e2933-103">Checking Access with Authz API</span></span>

<span data-ttu-id="e2933-104">應用程式會藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式來判斷是否要授與安全物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="e2933-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="e2933-105">[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函式會採用 [**AUTHZ \_ 存取 \_ 要求**](/windows/desktop/api/Authz/ns-authz-authz_access_request)和 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor)結構作為參數。</span><span class="sxs-lookup"><span data-stu-id="e2933-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="e2933-106">**AUTHZ \_ 存取 \_ 要求** 結構會指定所要求的存取層級。</span><span class="sxs-lookup"><span data-stu-id="e2933-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="e2933-107">**AuthzAccessCheck** 函式會針對指定的用戶端內容，針對指定的 **安全 \_ 描述項** 來評估要求的存取權。</span><span class="sxs-lookup"><span data-stu-id="e2933-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="e2933-108">如需安全描述項如何控制物件存取的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="e2933-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="e2933-109">使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="e2933-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="e2933-110">回呼函式</span><span class="sxs-lookup"><span data-stu-id="e2933-110">Callback Function</span></span>

<span data-ttu-id="e2933-111">如果要檢查的物件之 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor)的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 包含任何 (ace) 的回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)， [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)會針對 DACL 中包含的每個回呼 ACE 呼叫 [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md)函數。</span><span class="sxs-lookup"><span data-stu-id="e2933-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="e2933-112">回呼 ACE 是其 ACE 型別包含 "callback" 這個字的任何 ACE 結構。</span><span class="sxs-lookup"><span data-stu-id="e2933-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="e2933-113">**AuthzAccessCheckCallback** 函式是一種應用程式定義的函式，當資源管理員透過呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)函式進行初始化時，必須註冊此函數。</span><span class="sxs-lookup"><span data-stu-id="e2933-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="e2933-114">回呼函數可讓應用程式定義要在執行時間評估的商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="e2933-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="e2933-115">呼叫 [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) 函式時，會將造成呼叫的回呼 ACE 傳遞給回呼函式進行評估。</span><span class="sxs-lookup"><span data-stu-id="e2933-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="e2933-116">如果應用程式定義的邏輯評估為 **TRUE**，則會在存取檢查中包含回呼 ACE。</span><span class="sxs-lookup"><span data-stu-id="e2933-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="e2933-117">否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="e2933-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="e2933-118">快取存取結果</span><span class="sxs-lookup"><span data-stu-id="e2933-118">Caching Access Results</span></span>

<span data-ttu-id="e2933-119">存取檢查的結果可以快取，並在後續呼叫 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) 函數時使用。</span><span class="sxs-lookup"><span data-stu-id="e2933-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="e2933-120">如需快取存取檢查的詳細資訊，包括範例，請參閱快取 [存取檢查](caching-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="e2933-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="e2933-121">範例</span><span class="sxs-lookup"><span data-stu-id="e2933-121">Example</span></span>

<span data-ttu-id="e2933-122">下列範例會建立 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) ，以允許內建系統管理員的 **讀取 \_ 控制** 存取權。</span><span class="sxs-lookup"><span data-stu-id="e2933-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="e2933-123">它會使用該安全描述項來檢查用戶端內容所指定用戶端的存取權，該用戶端內容是在 [初始化用戶端內容](initializing-a-client-context.md)時的範例中所建立。</span><span class="sxs-lookup"><span data-stu-id="e2933-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="e2933-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2933-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2933-125">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="e2933-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="e2933-126">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="e2933-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="e2933-127">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="e2933-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="e2933-128">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="e2933-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
