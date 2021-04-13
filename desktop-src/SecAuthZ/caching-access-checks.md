---
description: 當應用程式藉由呼叫 AuthzAccessCheck 函數來執行存取檢查時，可以快取該存取檢查的結果。
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: 快取存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321211"
---
# <a name="caching-access-checks"></a><span data-ttu-id="24413-103">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="24413-103">Caching Access Checks</span></span>

<span data-ttu-id="24413-104">當應用程式藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函數來執行存取檢查時，可以快取該存取檢查的結果。</span><span class="sxs-lookup"><span data-stu-id="24413-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="24413-105">當 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函式的 *pAuthzHandle* 參數不是 **Null** 時，此函式會執行個別的存取檢查，並要求允許的 **最 \_ 大**[**存取 \_ 遮罩**](access-mask.md)，並快取該檢查的結果。</span><span class="sxs-lookup"><span data-stu-id="24413-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="24413-106">然後，可以將該檢查的結果控制碼作為 *AuthzHandle* 參數傳遞至 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) 函式。</span><span class="sxs-lookup"><span data-stu-id="24413-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="24413-107">這可讓您更快速地存取指定用戶端和 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的存取權。</span><span class="sxs-lookup"><span data-stu-id="24413-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="24413-108">只有存取檢查的靜態部分可以快取。</span><span class="sxs-lookup"><span data-stu-id="24413-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="24413-109">任何回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 或包含 **主體 \_ 自我** SID 的 ace 都必須針對每個存取檢查進行評估。</span><span class="sxs-lookup"><span data-stu-id="24413-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="24413-110">使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="24413-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="24413-111">範例</span><span class="sxs-lookup"><span data-stu-id="24413-111">Example</span></span>

<span data-ttu-id="24413-112">下列範例會根據先前的存取檢查來檢查快取結果的存取權。</span><span class="sxs-lookup"><span data-stu-id="24413-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="24413-113">先前的存取檢查是在 [使用 Authz API 檢查存取](checking-access-with-authz-api.md)的範例中執行。</span><span class="sxs-lookup"><span data-stu-id="24413-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="24413-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="24413-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24413-115">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="24413-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="24413-116">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="24413-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="24413-117">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="24413-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="24413-118">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="24413-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
