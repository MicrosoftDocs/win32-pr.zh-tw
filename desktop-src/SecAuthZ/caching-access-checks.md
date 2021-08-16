---
description: 當應用程式藉由呼叫 AuthzAccessCheck 函數來執行存取檢查時，可以快取該存取檢查的結果。
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: 快取存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783553"
---
# <a name="caching-access-checks"></a>快取存取檢查

當應用程式藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函數來執行存取檢查時，可以快取該存取檢查的結果。 當 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函式的 *pAuthzHandle* 參數不是 **Null** 時，此函式會執行個別的存取檢查，並要求允許的 **最 \_ 大**[**存取 \_ 遮罩**](access-mask.md)，並快取該檢查的結果。 然後，可以將該檢查的結果控制碼作為 *AuthzHandle* 參數傳遞至 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) 函式。 這可讓您更快速地存取指定用戶端和 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的存取權。

只有存取檢查的靜態部分可以快取。 任何回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 或包含 **主體 \_ 自我** SID 的 ace 都必須針對每個存取檢查進行評估。

使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。

## <a name="example"></a>範例

下列範例會根據先前的存取檢查來檢查快取結果的存取權。 先前的存取檢查是在 [使用 Authz API 檢查存取](checking-access-with-authz-api.md)的範例中執行。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Sid 新增至用戶端內容](adding-sids-to-a-client-context.md)
</dt> <dt>

[使用 Authz API 檢查存取權](checking-access-with-authz-api.md)
</dt> <dt>

[初始化用戶端內容](initializing-a-client-context.md)
</dt> <dt>

[查詢用戶端內容](querying-a-client-context.md)
</dt> </dl>

 

 
