---
description: 應用程式會藉由呼叫 AuthzAccessCheck 函式來判斷是否要授與安全物件的存取權。
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: 使用 Authz API 檢查存取權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876c3b5305e33969f63932fdc9e1e4f6767c95a64b11272283420a377b39f795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783094"
---
# <a name="checking-access-with-authz-api"></a>使用 Authz API 檢查存取權

應用程式會藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式來判斷是否要授與安全物件的存取權。

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函式會採用 [**AUTHZ \_ 存取 \_ 要求**](/windows/desktop/api/Authz/ns-authz-authz_access_request)和 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor)結構作為參數。 **AUTHZ \_ 存取 \_ 要求** 結構會指定所要求的存取層級。 **AuthzAccessCheck** 函式會針對指定的用戶端內容，針對指定的 **安全 \_ 描述項** 來評估要求的存取權。 如需安全描述項如何控制物件存取的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。

使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。

## <a name="callback-function"></a>回呼函式

如果要檢查的物件之 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor)的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 包含任何 (ace) 的回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)， [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)會針對 DACL 中包含的每個回呼 ACE 呼叫 [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md)函數。 回呼 ACE 是其 ACE 型別包含 "callback" 這個字的任何 ACE 結構。 **AuthzAccessCheckCallback** 函式是一種應用程式定義的函式，當資源管理員透過呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)函式進行初始化時，必須註冊此函數。

回呼函數可讓應用程式定義要在執行時間評估的商務邏輯。 呼叫 [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) 函式時，會將造成呼叫的回呼 ACE 傳遞給回呼函式進行評估。 如果應用程式定義的邏輯評估為 **TRUE**，則會在存取檢查中包含回呼 ACE。 否則會予以忽略。

## <a name="caching-access-results"></a>快取存取結果

存取檢查的結果可以快取，並在後續呼叫 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) 函數時使用。 如需快取存取檢查的詳細資訊，包括範例，請參閱快取 [存取檢查](caching-access-checks.md)。

## <a name="example"></a>範例

下列範例會建立 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) ，以允許內建系統管理員的 **讀取 \_ 控制** 存取權。 它會使用該安全描述項來檢查用戶端內容所指定用戶端的存取權，該用戶端內容是在 [初始化用戶端內容](initializing-a-client-context.md)時的範例中所建立。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Sid 新增至用戶端內容](adding-sids-to-a-client-context.md)
</dt> <dt>

[快取存取檢查](caching-access-checks.md)
</dt> <dt>

[初始化用戶端內容](initializing-a-client-context.md)
</dt> <dt>

[查詢用戶端內容](querying-a-client-context.md)
</dt> </dl>

 

 
