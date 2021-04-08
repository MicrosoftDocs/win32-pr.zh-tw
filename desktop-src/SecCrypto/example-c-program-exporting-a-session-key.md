---
description: 下列範例會建立隨機工作階段金鑰，並建立可匯出的金鑰 BLOB。 此範例說明如何使用 CryptGetUserKey、CryptExportKey 和相關函數。
ms.assetid: a7f2fdd1-9514-4cda-bae2-2f379dd9a27d
title: 範例 C 程式：匯出工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e5eced86dd4e671f5080cf6dab5e1ec96b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692463"
---
# <a name="example-c-program-exporting-a-session-key"></a><span data-ttu-id="054c2-104">範例 C 程式：匯出工作階段金鑰</span><span class="sxs-lookup"><span data-stu-id="054c2-104">Example C Program: Exporting a Session Key</span></span>

<span data-ttu-id="054c2-105">下列範例會建立隨機工作階段金鑰，並建立可匯出的 [*金鑰 BLOB*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="054c2-105">The following example creates a random session key and creates an exportable [*key BLOB*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="054c2-106">此範例說明如何使用 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)、 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)和相關函數。</span><span class="sxs-lookup"><span data-stu-id="054c2-106">The example illustrates the use of [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey), [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), and related functions.</span></span>

<span data-ttu-id="054c2-107">此範例說明下列工作和 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="054c2-107">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="054c2-108">使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)取得 CSP 內容。</span><span class="sxs-lookup"><span data-stu-id="054c2-108">Acquiring a CSP context using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="054c2-109">使用 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)取得兩組不同的公開/私密金鑰存取權。</span><span class="sxs-lookup"><span data-stu-id="054c2-109">Gaining access to two different pairs of public/private keys using [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).</span></span>
-   <span data-ttu-id="054c2-110">使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)產生可匯出的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="054c2-110">Generating an exportable session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="054c2-111">使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)建立包含工作階段金鑰的 [*簡單金鑰 BLOB*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="054c2-111">Creating a [*simple key BLOB*](../secgloss/s-gly.md) containing a session key using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>
-   <span data-ttu-id="054c2-112">使用 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)終結工作階段金鑰，並存取兩組公開/私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="054c2-112">Destroying a session key and access to the two pairs of public/private keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="054c2-113">使用 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)發行 CSP 內容。</span><span class="sxs-lookup"><span data-stu-id="054c2-113">Releasing the CSP context using [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="054c2-114">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="054c2-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="054c2-115">這個函式的程式碼會包含在範例中。</span><span class="sxs-lookup"><span data-stu-id="054c2-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="054c2-116">這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="054c2-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This example program creates a session key and a simple key 
// BLOB holding that session key. The key BLOB can be written to disk 
// and later read from a disk file.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//--------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hProv;       // CSP handle
HCRYPTKEY hSignKey;     // Signature key pair handle
HCRYPTKEY hXchgKey;     // Exchange key pair handle
HCRYPTKEY hKey;         // Session key handle
BYTE *pbKeyBlob;        // Pointer to a simple key BLOB
DWORD dwBlobLen;        // The length of the key BLOB

//--------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
   &hProv, 
   NULL, 
   NULL, 
   PROV_RSA_FULL, 
   0)) 
{
    printf("The CSP has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext.");
}
//--------------------------------------------------------------------
// Get a handle to the signature key.
// The signature key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_SIGNATURE, 
   &hSignKey)) 
{
    printf("The signature key has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptGetUserKey for signkey.");
}
//--------------------------------------------------------------------
// Get a handle to the key exchange key.
// The key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_KEYEXCHANGE, 
   &hXchgKey)) 
{
    printf("The key exchange key has been acquired. \n");
}
else
{
    printf("Error during CryptGetUserKey exchange key.");
}
// hSignKey may be used to verify a signature. hXchgKey will be used
// to export a session key.

//--------------------------------------------------------------------
// Generate a session key.

if (CryptGenKey(     
    hProv,      
    CALG_RC4,      
    CRYPT_EXPORTABLE, 
    &hKey))
{   
    printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR -- CryptGenKey.");
}
// Determine the size of the key BLOB and allocate memory.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   NULL, 
   &dwBlobLen)) 
{
     printf("Size of the BLOB for the session key determined. \n");
}
else
{
     MyHandleError("Error computing BLOB length.");
}

if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Out of memory. \n");
}
//--------------------------------------------------------------------
// Export the key into a simple key BLOB.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   pbKeyBlob, 
   &dwBlobLen))
{
     printf("Contents have been written to the BLOB. \n");
}
else
{
    MyHandleError("Error during CryptExportKey.");
}
//--------------------------------------------------------------------
//   At this point, other processing such as writing the key BLOB to
//   a file could be done.

//--------------------------------------------------------------------
// After all processing, clean up.

//--------------------------------------------------------------------
//  Free the memory used by the key BLOB.

free(pbKeyBlob);

// Destroy the session key.
if(hKey)
    CryptDestroyKey(hKey);

// Destroy the signature key handle.
if(hSignKey)
    CryptDestroyKey(hSignKey);

// Destroy the key exchange key handle.
if(hXchgKey)
     CryptDestroyKey(hXchgKey);

// Release the provider handle.
if(hProv) 
   CryptReleaseContext(hProv, 0);
printf("The program ran to completion without error. \n");

}// End of main                                                    

//--------------------------------------------------------------------
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



 

 
