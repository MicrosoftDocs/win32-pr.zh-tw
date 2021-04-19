---
description: 應用程式可以呼叫 AuthzGetInformationFromCoNtext 函數來查詢現有用戶端內容的相關資訊。
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: 查詢用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974946"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="66676-103">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="66676-103">Querying a Client Context</span></span>

<span data-ttu-id="66676-104">應用程式可以呼叫 [**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) 函數來查詢現有用戶端內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="66676-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="66676-105">[**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext)函數的 *InfoClass* 參數會接受來自 [**AUTHZ \_ 內容 \_ 資訊 \_ 類別**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class)列舉的值，以指定函數所查詢的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="66676-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="66676-106">如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中;否則，參考它們的條件運算式詞彙將會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="66676-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="66676-107">如需條件運算式的詳細資訊，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="66676-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="66676-108">範例</span><span class="sxs-lookup"><span data-stu-id="66676-108">Example</span></span>

<span data-ttu-id="66676-109">下列範例會查詢範例中所建立的用戶端內容，從 [初始化用戶端內容](initializing-a-client-context.md) 到取得與該用戶端內容相關聯之群組的 [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) 清單。</span><span class="sxs-lookup"><span data-stu-id="66676-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="66676-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="66676-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66676-111">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="66676-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="66676-112">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="66676-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="66676-113">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="66676-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="66676-114">AccessCheck 的運作方式</span><span class="sxs-lookup"><span data-stu-id="66676-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="66676-115">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="66676-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="66676-116">條件式 Ace 的安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="66676-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



