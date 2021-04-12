---
description: 應用程式可以藉由呼叫 AuthzAddSidsToCoNtext 函式，將安全識別碼 (Sid) 新增至現有的用戶端內容。
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: 將 Sid 新增至用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513813"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="bdfa1-103">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="bdfa1-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="bdfa1-104">應用程式可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式，將 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 新增至現有的用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="bdfa1-105">[**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式可讓應用程式指定 sid 的清單，以及指定的用戶端內容限制 sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="bdfa1-106">當系統檢查安全物件的權杖存取權時，系統會使用限制 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="bdfa1-107">當受限制的進程或執行緒嘗試存取安全物件時，系統會執行兩項存取檢查：一個使用權杖啟用的 Sid，另一個使用限制 Sid 的清單。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="bdfa1-108">只有在這兩個存取檢查都允許要求的存取權限時，才會授與存取權。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="bdfa1-109">使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="bdfa1-110">範例</span><span class="sxs-lookup"><span data-stu-id="bdfa1-110">Example</span></span>

<span data-ttu-id="bdfa1-111">下列範例會將 SID 和限制 SID 加入範例中所建立的用戶端內容，以 [初始化用戶端內容](initializing-a-client-context.md)。</span><span class="sxs-lookup"><span data-stu-id="bdfa1-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="bdfa1-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdfa1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdfa1-113">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="bdfa1-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="bdfa1-114">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="bdfa1-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="bdfa1-115">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="bdfa1-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="bdfa1-116">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="bdfa1-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
