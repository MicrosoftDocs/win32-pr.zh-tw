---
description: 下列範例示範如何從密碼的雜湊以及使用函數 CryptDeriveKey 和相關函式來建立會話密碼編譯金鑰。
ms.assetid: f4748725-2a47-487c-b18c-7b27112d1090
title: 範例 C 程式：從密碼衍生工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46884fa40a3a5682ca21229048004314bf03609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194744"
---
# <a name="example-c-program-deriving-a-session-key-from-a-password"></a><span data-ttu-id="b80e0-103">範例 C 程式：從密碼衍生工作階段金鑰</span><span class="sxs-lookup"><span data-stu-id="b80e0-103">Example C Program: Deriving a Session Key from a Password</span></span>

<span data-ttu-id="b80e0-104">下列範例示範如何從密碼的 [*雜湊*](../secgloss/h-gly.md)以及使用函數 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)和相關函式來建立會話密碼編譯 [*金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b80e0-104">The following example demonstrates creating a [*session cryptographic key*](../secgloss/s-gly.md) from the [*hash*](../secgloss/h-gly.md) of a password as well as the use of the function [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) and related functions.</span></span>

<span data-ttu-id="b80e0-105">此範例說明下列工作和 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="b80e0-105">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="b80e0-106">呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得預設 CSP 和預設 [*金鑰容器*](../secgloss/k-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b80e0-106">Calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) to acquiring a handle for the default CSP and the default [*key container*](../secgloss/k-gly.md).</span></span>
-   <span data-ttu-id="b80e0-107">使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) 建立空的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="b80e0-107">Using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) to create an empty hash object.</span></span>
-   <span data-ttu-id="b80e0-108">使用 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)來雜湊密碼文字。</span><span class="sxs-lookup"><span data-stu-id="b80e0-108">Hashing the text of a password using [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span></span>
-   <span data-ttu-id="b80e0-109">使用 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)從雜湊密碼衍生工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="b80e0-109">Deriving a session key from the hashed password using [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>
-   <span data-ttu-id="b80e0-110">摧毀雜湊和密碼。</span><span class="sxs-lookup"><span data-stu-id="b80e0-110">Destroying the hash and the password.</span></span>
-   <span data-ttu-id="b80e0-111">使用 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) 來發行 CSP。</span><span class="sxs-lookup"><span data-stu-id="b80e0-111">Using [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) to release the CSP.</span></span>

<span data-ttu-id="b80e0-112">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="b80e0-112">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="b80e0-113">此範例包含此函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b80e0-113">Code for this function is included with the sample.</span></span>

<span data-ttu-id="b80e0-114">這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="b80e0-114">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void GetConsoleInput(char*, UINT);
#define PASSWORD_LENGTH 512

void main()
{
    //----------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.

    HCRYPTPROV hCryptProv;
    HCRYPTKEY hKey;
    HCRYPTHASH hHash;
    CHAR szPassword[PASSWORD_LENGTH] = "";
    DWORD dwLength;

    //----------------------------------------------------------------
    // Get the password from the user.

    fprintf(stderr,"Enter a password to be used to create a key:");

    // Get a password while printing only asterisks to the screen.
    GetConsoleInput(szPassword, PASSWORD_LENGTH);
    printf("The password has been stored.\n");
    dwLength = (DWORD) strlen(szPassword);

    //----------------------------------------------------------------
    // Acquire a cryptographic provider context handle.

    if(CryptAcquireContext(
       &hCryptProv,
       NULL,
       NULL,
       PROV_RSA_FULL,
       0))
    {
        printf("A context has been acquired. \n");
    }
    else
    {
         MyHandleError("Error during CryptAcquireContext!");
    }
    //----------------------------------------------------------------
    // Create an empty hash object.

    if(CryptCreateHash(
       hCryptProv,
       CALG_MD5,
       0,
       0,
       &hHash))
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptCreateHash!");
    }
    //----------------------------------------------------------------
    // Hash the password string.

    if(CryptHashData(
       hHash,
       (BYTE *)szPassword,
       dwLength,
       0))
    {
         printf("The password has been hashed. \n");
    }
    else
    {
         MyHandleError("Error during CryptHashData!");
    }
    //----------------------------------------------------------------
    // Create a session key based on the hash of the password.

    if(CryptDeriveKey(
       hCryptProv,
       CALG_RC2,
       hHash,
       CRYPT_EXPORTABLE,
       &hKey))
    {
        printf("The key has been derived. \n");
    }
    else
    {
        MyHandleError("Error during CryptDeriveKey!");
    }
    //----------------------------------------------------------------
    // Use hKey as appropriate to encrypt or decrypt a message.

    //----------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
       if(!(CryptDestroyHash(hHash)))
           MyHandleError("Error during CryptDestroyHash");
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
            MyHandleError("Error during CryptDestroyKey");
    }

    // Release the provider handle.
    if(hCryptProv)
    {
       if(!(CryptReleaseContext(hCryptProv, 0)))
           MyHandleError("Error during CryptReleaseContext");
    }
    printf("The program to derive a key completed without error. \n");
} // end main

//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}

//--------------------------------------------------------------------
// The GetConsoleInput function gets an array of characters from the
// keyboard, while printing only asterisks to the screen.

void GetConsoleInput(char* strInput,
                    UINT  intMaxChars)
{
    char ch;
    char minChar = ' ';
    minChar++;

    ch = (char)_getch();
    while (ch != '\r')
    {
        if (ch == '\b' && strlen(strInput) > 0)
        {
            strInput[strlen(strInput)-1]   = '\0';
            printf("\b \b");
        }
        else if ((ch >= minChar) && (strlen(strInput) < intMaxChars))
        {
            strInput[strlen(strInput)+1] = '\0';
            strInput[strlen(strInput)]   = ch;
            _putch('*');
        }
        ch = (char)_getch();
    }
    _putch('\n');
}

```



 

 
