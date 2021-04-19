---
description: 應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: 初始化用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988382"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="4fe58-103">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="4fe58-103">Initializing a Client Context</span></span>

<span data-ttu-id="4fe58-104">應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。</span><span class="sxs-lookup"><span data-stu-id="4fe58-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="4fe58-105">應用程式必須呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) 函式來初始化資源管理員。</span><span class="sxs-lookup"><span data-stu-id="4fe58-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="4fe58-106">然後，應用程式可以呼叫數個函式的其中一個來建立用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="4fe58-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="4fe58-107">此外，如果您要從遠端執行存取檢查或審核，就必須使用 [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) 函式。</span><span class="sxs-lookup"><span data-stu-id="4fe58-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="4fe58-108">若要根據現有的用戶端內容建立用戶端內容，請呼叫 [**AuthzInitializeCoNtextFromAuthzCoNtext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="4fe58-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="4fe58-109">[**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)函式會使用登入權杖中的資訊來建立新的用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="4fe58-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="4fe58-110">[**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)函式會使用指定的 [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)來建立新的用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="4fe58-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="4fe58-111">可能的話，請呼叫 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) 函式，而不是 [**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)。</span><span class="sxs-lookup"><span data-stu-id="4fe58-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="4fe58-112">**AuthzInitializeCoNtextFromSid** 會嘗試取出登入權杖中的可用資訊，用戶端實際上是登入。</span><span class="sxs-lookup"><span data-stu-id="4fe58-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="4fe58-113">實際的登入權杖會提供更多的資訊，例如登入類型和登入內容，並反映用於登入的驗證封裝行為。</span><span class="sxs-lookup"><span data-stu-id="4fe58-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="4fe58-114">**AuthzInitializeCoNtextFromToken** 所建立的用戶端內容會使用登入權杖，而產生的用戶端內容會比 **AuthzInitializeCoNtextFromSid** 所建立的用戶端內容更完整且準確。</span><span class="sxs-lookup"><span data-stu-id="4fe58-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="4fe58-115">如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中;否則，參考它們的條件運算式詞彙將會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="4fe58-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="4fe58-116">如需條件運算式的詳細資訊，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="4fe58-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="4fe58-117">範例</span><span class="sxs-lookup"><span data-stu-id="4fe58-117">Example</span></span>

<span data-ttu-id="4fe58-118">下列範例會初始化 Authz 資源管理員，並呼叫 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) 函式，從與目前進程相關聯的登入權杖建立用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="4fe58-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="4fe58-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="4fe58-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fe58-120">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="4fe58-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="4fe58-121">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="4fe58-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="4fe58-122">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="4fe58-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="4fe58-123">AccessCheck 的運作方式</span><span class="sxs-lookup"><span data-stu-id="4fe58-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="4fe58-124">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="4fe58-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="4fe58-125">條件式 Ace 的安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="4fe58-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="4fe58-126">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="4fe58-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="4fe58-127">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="4fe58-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



