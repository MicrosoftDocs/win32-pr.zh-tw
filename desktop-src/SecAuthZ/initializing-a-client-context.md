---
description: 應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: 初始化用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908038"
---
# <a name="initializing-a-client-context"></a>初始化用戶端內容

應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。

應用程式必須呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) 函式來初始化資源管理員。 然後，應用程式可以呼叫數個函式的其中一個來建立用戶端內容。 此外，如果您要從遠端執行存取檢查或審核，就必須使用 [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) 函式。

若要根據現有的用戶端內容建立用戶端內容，請呼叫 [**AuthzInitializeCoNtextFromAuthzCoNtext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) 函數。

[**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)函式會使用登入權杖中的資訊來建立新的用戶端內容。 [**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)函式會使用指定的 [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)來建立新的用戶端內容。

可能的話，請呼叫 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) 函式，而不是 [**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)。 **AuthzInitializeCoNtextFromSid** 會嘗試取出登入權杖中的可用資訊，用戶端實際上是登入。 實際的登入權杖會提供更多的資訊，例如登入類型和登入內容，並反映用於登入的驗證封裝行為。 **AuthzInitializeCoNtextFromToken** 所建立的用戶端內容會使用登入權杖，而產生的用戶端內容會比 **AuthzInitializeCoNtextFromSid** 所建立的用戶端內容更完整且準確。

> [!Note]  
> 如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中;否則，參考它們的條件運算式詞彙將會評估為 unknown。 如需條件運算式的詳細資訊，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md) 主題。

 

## <a name="example"></a>範例

下列範例會初始化 Authz 資源管理員，並呼叫 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) 函式，從與目前進程相關聯的登入權杖建立用戶端內容。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Sid 新增至用戶端內容](adding-sids-to-a-client-context.md)
</dt> <dt>

[快取存取檢查](caching-access-checks.md)
</dt> <dt>

[使用 Authz API 檢查存取權](checking-access-with-authz-api.md)
</dt> <dt>

[AccessCheck 的運作方式](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[查詢用戶端內容](querying-a-client-context.md)
</dt> <dt>

[條件式 Ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



