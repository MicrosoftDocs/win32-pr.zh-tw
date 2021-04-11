---
description: Identity Manager API 可讓您建立要在對等網路中使用的對等身分識別。
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: 建立對等身分識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944285"
---
# <a name="creating-a-peer-identity"></a><span data-ttu-id="04748-103">建立對等身分識別</span><span class="sxs-lookup"><span data-stu-id="04748-103">Creating a Peer Identity</span></span>

<span data-ttu-id="04748-104">Identity Manager API 可讓您建立要在對等網路中使用的對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="04748-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="04748-105">當您建立對等身分識別時，可以提供下列選擇性資訊：</span><span class="sxs-lookup"><span data-stu-id="04748-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="04748-106">分類器</span><span class="sxs-lookup"><span data-stu-id="04748-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="04748-107">易記名稱</span><span class="sxs-lookup"><span data-stu-id="04748-107">Friendly name</span></span>
-   <span data-ttu-id="04748-108">密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="04748-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="04748-109">盡可能重複使用對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="04748-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="04748-110">建立和刪除對等身分識別的範例</span><span class="sxs-lookup"><span data-stu-id="04748-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="04748-111">下列程式碼片段說明如何使用分類器和易記名稱來建立和刪除對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="04748-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


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



 

 



