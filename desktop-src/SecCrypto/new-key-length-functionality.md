---
description: 基底提供者僅使用40位的對稱金鑰。
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: 新的索引鍵長度功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1da54be20e2b7e238cc99e787a2871bea54b40b0c46e214b7280482dcd8232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407008"
---
# <a name="new-key-length-functionality"></a>新的索引鍵長度功能

基底提供者僅使用40位的 [*對稱金鑰*](../secgloss/s-gly.md)。 在增強型提供者中新增較長的索引鍵，而匯入的索引鍵可以是任意長度的事實，需要查詢特定索引鍵長度的方法。 若要尋找金鑰的實際長度（以位為單位），使用者[](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam)可以使用 KP \_ KEYLEN 參數值來呼叫 CryptGetKeyParam。 索引鍵的長度會在 *>pbdata* 參數所指向的 **DWORD** 中傳回。

> [!Note]  
> 為了防範逐步 [*加密分析*](../secgloss/c-gly.md) 攻擊，應用程式必須檢查 [*金鑰長度*](../secgloss/k-gly.md) 是否不足，並在遇到錯誤時通知使用者。

 

下列範例顯示如何查詢索引鍵的長度。


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



 

 
