---
description: 下列範例會建立隨機工作階段金鑰、複製金鑰、在原始金鑰上設定一些額外的參數，並終結原始和重複的索引鍵。
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 範例 C 程式：複製工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4116a021b358864da27b2eb94d66a0f74f1462232f58441e7af5c2c7b91e114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007786"
---
# <a name="example-c-program-duplicating-a-session-key"></a>範例 C 程式：複製工作階段金鑰

下列範例會建立隨機 [*工作階段金鑰*](../secgloss/s-gly.md)、複製金鑰、在原始金鑰上設定一些額外的參數，並終結原始和重複的索引鍵。 此範例說明如何使用 [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) 和相關函數。

此範例說明下列工作和 CryptoAPI 函數：

-   使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta))  (CSP 存取 [*密碼編譯服務提供者*](../secgloss/c-gly.md)。
-   使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)建立工作階段金鑰。
-   複製使用 [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey)建立的金鑰。
-   使用 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 以兩種不同的方式來改變金鑰產生流程。
-   使用 [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom)填滿具有隨機位元組的緩衝區。
-   使用 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)終結金鑰。
-   使用 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)發行 CSP。

這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。 這個函式的程式碼會包含在範例中。 這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(    
   &hCryptProv,
   NULL,
   NULL,
   PROV_RSA_FULL,
   0)) 
{    
    printf("CryptAcquireContext succeeded. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
