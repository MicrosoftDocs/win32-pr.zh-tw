---
description: Identity Manager API 可讓您建立要在對等網路中使用的對等身分識別。
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: 建立對等身分識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887818"
---
# <a name="creating-a-peer-identity"></a>建立對等身分識別

Identity Manager API 可讓您建立要在對等網路中使用的對等身分識別。

當您建立對等身分識別時，可以提供下列選擇性資訊：

-   [分類器](peer-names.md)
-   易記名稱
-   密碼編譯服務提供者

> [!Note]  
> 盡可能重複使用對等身分識別。

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>建立和刪除對等身分識別的範例

下列程式碼片段說明如何使用分類器和易記名稱來建立和刪除對等身分識別。


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



