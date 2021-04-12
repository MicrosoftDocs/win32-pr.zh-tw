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
# <a name="adding-sids-to-a-client-context"></a>將 Sid 新增至用戶端內容

應用程式可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式，將 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 新增至現有的用戶端內容。 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式可讓應用程式指定 sid 的清單，以及指定的用戶端內容限制 sid 的清單。

當系統檢查安全物件的權杖存取權時，系統會使用限制 Sid 的清單。 當受限制的進程或執行緒嘗試存取安全物件時，系統會執行兩項存取檢查：一個使用權杖啟用的 Sid，另一個使用限制 Sid 的清單。 只有在這兩個存取檢查都允許要求的存取權限時，才會授與存取權。

使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。

## <a name="example"></a>範例

下列範例會將 SID 和限制 SID 加入範例中所建立的用戶端內容，以 [初始化用戶端內容](initializing-a-client-context.md)。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[快取存取檢查](caching-access-checks.md)
</dt> <dt>

[使用 Authz API 檢查存取權](checking-access-with-authz-api.md)
</dt> <dt>

[初始化用戶端內容](initializing-a-client-context.md)
</dt> <dt>

[查詢用戶端內容](querying-a-client-context.md)
</dt> </dl>

 

 
