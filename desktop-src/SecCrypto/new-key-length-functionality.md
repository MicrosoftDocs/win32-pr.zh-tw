---
description: 基底提供者僅使用40位的對稱金鑰。
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: 新的索引鍵長度功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194736"
---
# <a name="new-key-length-functionality"></a><span data-ttu-id="089a0-103">新的索引鍵長度功能</span><span class="sxs-lookup"><span data-stu-id="089a0-103">New Key-length Functionality</span></span>

<span data-ttu-id="089a0-104">基底提供者僅使用40位的 [*對稱金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="089a0-104">The Base Provider used only 40-bit [*symmetric keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="089a0-105">在增強型提供者中新增較長的索引鍵，而匯入的索引鍵可以是任意長度的事實，需要查詢特定索引鍵長度的方法。</span><span class="sxs-lookup"><span data-stu-id="089a0-105">The addition of longer keys in the Enhanced Provider, and the fact that imported keys can be of arbitrary length requires a method of querying the length for a specific key.</span></span> <span data-ttu-id="089a0-106">若要尋找金鑰的實際長度（以位為單位），使用者[](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam)可以使用 KP \_ KEYLEN 參數值來呼叫 CryptGetKeyParam。</span><span class="sxs-lookup"><span data-stu-id="089a0-106">To find the actual length of a key in bits, a user can call [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) with the KP\_KEYLEN parameter value.</span></span> <span data-ttu-id="089a0-107">索引鍵的長度會在 *>pbdata* 參數所指向的 **DWORD** 中傳回。</span><span class="sxs-lookup"><span data-stu-id="089a0-107">The length of the key is returned in the **DWORD** pointed to by the *pbData* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="089a0-108">為了防範逐步 [*加密分析*](../secgloss/c-gly.md) 攻擊，應用程式必須檢查 [*金鑰長度*](../secgloss/k-gly.md) 是否不足，並在遇到錯誤時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="089a0-108">To protect against stepping-down [*cryptanalysis*](../secgloss/c-gly.md) attacks, applications must check for insufficient [*key lengths*](../secgloss/k-gly.md) and notify the user when one is encountered.</span></span>

 

<span data-ttu-id="089a0-109">下列範例顯示如何查詢索引鍵的長度。</span><span class="sxs-lookup"><span data-stu-id="089a0-109">The following example shows how to query the length of a key.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
