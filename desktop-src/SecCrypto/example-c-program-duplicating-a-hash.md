---
description: 下列範例會建立並複製一些文字的雜湊。 然後，它會將額外的文字加入至原始的雜湊，並將不同的文字加入重複的文字。
ms.assetid: 7aa7c9a1-471b-4b40-9967-b1da946c83a5
title: 範例 C 程式：複製雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a418f1e5e615d8c4b4c0e8a0af3061b9b6f860e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991758"
---
# <a name="example-c-program-duplicating-a-hash"></a>範例 C 程式：複製雜湊

下列範例會建立並複製一些文字的 [*雜湊*](../secgloss/h-gly.md) 。 然後，它會將額外的文字加入至原始的雜湊，並將不同的文字加入重複的文字。

此範例使用下列 CryptoAPI 函數：

-   [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
-   [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)
-   [**CryptDuplicateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash)
-   [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam)
-   [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash)
-   [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。 此函式的程式碼會包含在範例的結尾。 這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void Get_And_Print_Hash(HCRYPTHASH hHash);

void main(void)
{
    //--------------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.
    HCRYPTPROV   hCryptProv = NULL;
    HCRYPTHASH   hOriginalHash;
    HCRYPTHASH   hDuplicateHash;

    //--------------------------------------------------------------------
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
        MyHandleError("Error during CryptAcquireContext!");
    }

    //--------------------------------------------------------------------
    // Create a hash.
    if (CryptCreateHash(
        hCryptProv,
        CALG_SHA1,
        0,
        0,
        &hOriginalHash))
    {
       printf("An empty hash object has been created. \n");
    }
    else
    {
       MyHandleError("Error during CryptCreateHash.");
    }

    //--------------------------------------------------------------------
    // Hash a BYTE string.
    if (CryptHashData(
        hOriginalHash,
        (BYTE*)"Some Common Data",
        sizeof("Some Common Data"), 0))
    {
       printf("An original hash has been created. \n");
    }
    else
    {
       MyHandleError("Error during CryptHashData.");
    }

    //--------------------------------------------------------------------
    // Duplicate the hash.
    if (CryptDuplicateHash(
       hOriginalHash,
       NULL,
       0,
       &hDuplicateHash))
    {
       printf("The hash has been duplicated. \n");
    }
    else
    {
       MyHandleError("Error during CryptDuplicateHash.");
    }

    printf("The original hash -- phase 1.\n");
    Get_And_Print_Hash(hOriginalHash);

    printf("The duplicate hash -- phase 1.\n");
    Get_And_Print_Hash(hDuplicateHash);

    //--------------------------------------------------------------------
    // Hash some data with the original hash.
    if (CryptHashData(
         hOriginalHash,
         (BYTE*)"Some Data",
         sizeof("Some Data"),
         0))
    {
        printf("Additional data has been hashed with the original. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashData.");
    }

    //--------------------------------------------------------------------
    // Hash other data with the duplicate hash.
    if (CryptHashData(
         hDuplicateHash,
         (BYTE*)"Other Data",
         sizeof("Other Data"),
         0))
    {
       printf("More data has been hashed with the duplicate. \n");
    }
    else
    {
       MyHandleError("Error during CryptHashData.");
    }

    printf("The original hash -- phase 2.\n");
    Get_And_Print_Hash(hOriginalHash);

    printf("The duplicate hash -- phase 2.\n");
    Get_And_Print_Hash(hDuplicateHash);

    // Destroy the original hash.
    if(CryptDestroyHash(hOriginalHash))
    {
       printf("The original hash has been destroyed. \n");
    }
    else
    {
       MyHandleError("ERROR during CryptDestroyHash");
    }

    //--------------------------------------------------------------------
    // Destroy the duplicate hash.
    if (CryptDestroyHash(hDuplicateHash))
    {
       printf("The duplicate hash has been destroyed. \n");
    }
    else
    {
       MyHandleError("Error -- CryptDestroyHash");
    }

    //--------------------------------------------------------------------
    // Release the CSP.

    if(hCryptProv)
       CryptReleaseContext(hCryptProv,0);

    printf("The program ran to completion without error. \n");
} // end main

//--------------------------------------------------------------------
// Define the function Get_And_Print_Hash.
void Get_And_Print_Hash(HCRYPTHASH hOHash)
{
    //--------------------------------------------------------------------
    // Declare and initialize local variables.
    HCRYPTHASH   hHash;
    BYTE         *pbHash;
    DWORD        dwHashLen;
    DWORD        dwHashLenSize = sizeof(DWORD);
    DWORD        i;

    //--------------------------------------------------------------------
    // Duplicate the hash passed in.
    // The hash is duplicated to leave the original hash intact.

    if (CryptDuplicateHash(
       hOHash,
       NULL,
       0,
       &hHash))
    {
        // It worked. Do nothing.
    }
    else
    {
       MyHandleError("Error during CryptDuplicateHash.");
    }

    if(CryptGetHashParam(
       hHash,
       HP_HASHSIZE,
       (BYTE *)&dwHashLen,
       &dwHashLenSize,
       0))
    {
        // It worked. Do nothing.
    }
    else
    {
        MyHandleError("CryptGetHashParam failed to get size.");
    }

    if(pbHash = (BYTE*)malloc(dwHashLen))
    {
        // It worked. Do nothing.
    }
    else
    {
         MyHandleError("Allocation failed.");
    }

    if(CryptGetHashParam(
       hHash,
       HP_HASHVAL,
       pbHash,
       &dwHashLen,
       0))
    {
        // Print the hash value.
        printf("The hash is:  ");
        for(i = 0 ; i < dwHashLen ; i++)
        {
           printf("%02x ",pbHash[i]);
        }
        printf("\n");
    }
    else
    {
        MyHandleError("Error during reading hash value.");
    }

    free(pbHash);
    if (CryptDestroyHash(hHash))
    {
        // It worked. Do nothing.
    }
    else
    {
       MyHandleError("ERROR - CryptDestroyHash");
    }
} // end Get_And_Print_Hash


//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
