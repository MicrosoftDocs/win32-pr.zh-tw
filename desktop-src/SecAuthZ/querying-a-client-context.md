---
description: 應用程式可以呼叫 AuthzGetInformationFromCoNtext 函數來查詢現有用戶端內容的相關資訊。
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: 查詢用戶端內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e944939baae45236c914da7d11b6cedd6623ea132363ec86e1bf6f340644ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912077"
---
# <a name="querying-a-client-context"></a>查詢用戶端內容

應用程式可以呼叫 [**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) 函數來查詢現有用戶端內容的相關資訊。

[**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext)函數的 *InfoClass* 參數會接受來自 [**AUTHZ \_ 內容 \_ 資訊 \_ 類別**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class)列舉的值，以指定函數所查詢的資訊類型。

如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中;否則，參考它們的條件運算式詞彙將會評估為 unknown。 如需條件運算式的詳細資訊，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md) 主題。

## <a name="example"></a>範例

下列範例會查詢範例中所建立的用戶端內容，從 [初始化用戶端內容](initializing-a-client-context.md) 到取得與該用戶端內容相關聯之群組的 [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) 清單。


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

[初始化用戶端內容](initializing-a-client-context.md)
</dt> <dt>

[條件式 Ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



