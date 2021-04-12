---
description: 使用 HCRYPTKEY 控制碼來識別索引鍵。
ms.assetid: 23569104-a302-40de-a31a-a4ee22d5f7f2
title: 範例 C 程式：匯入純文字金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92341f4118770b963a9ea3dd47a153da0fe406b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321028"
---
# <a name="example-c-program-importing-a-plaintext-key"></a><span data-ttu-id="62f28-103">範例 C 程式：匯入純文字金鑰</span><span class="sxs-lookup"><span data-stu-id="62f28-103">Example C Program: Importing a Plaintext Key</span></span>

<span data-ttu-id="62f28-104">此 SDK 中的許多功能都需要您使用 **HCRYPTKEY** 控制碼來識別金鑰。</span><span class="sxs-lookup"><span data-stu-id="62f28-104">Many of the functions in this SDK require that you identify a key by using an **HCRYPTKEY** handle.</span></span> <span data-ttu-id="62f28-105">如果您的金鑰包含在位元組陣列中，您可以使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式來建立控制碼，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="62f28-105">If your key is contained in a byte array, you can create a handle by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function as shown in the following example.</span></span>

<span data-ttu-id="62f28-106">此範例示範下列工作和 CryptoAPI 函式：</span><span class="sxs-lookup"><span data-stu-id="62f28-106">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="62f28-107">藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62f28-107">Acquiring a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) by calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="62f28-108">藉由呼叫 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)將純文字金鑰匯入 CSP 金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="62f28-108">Importing a plaintext key into the CSP key container by calling [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>
-   <span data-ttu-id="62f28-109">藉由呼叫 [**CyptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)從金鑰容器匯出金鑰。</span><span class="sxs-lookup"><span data-stu-id="62f28-109">Exporting a key from the key container by calling [**CyptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>
-   <span data-ttu-id="62f28-110">將匯出的金鑰列印到主控台，以確認純文字金鑰確實已匯入至容器中。</span><span class="sxs-lookup"><span data-stu-id="62f28-110">Printing the exported key to the console to verify that the plaintext key was indeed imported into the container.</span></span>
-   <span data-ttu-id="62f28-111">釋放保留給純文字金鑰的記憶體。</span><span class="sxs-lookup"><span data-stu-id="62f28-111">Releasing the memory reserved for the plaintext key.</span></span>
-   <span data-ttu-id="62f28-112">藉由呼叫 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)來發行 CSP。</span><span class="sxs-lookup"><span data-stu-id="62f28-112">Releasing the CSP by calling [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// DesKeyBlob:      A plaintext key BLOB stored in a byte array. The 
//                  byte array  must have the following format:
//                      BLOBHEADER hdr;
//                      DWORD dwKeySize;
//                      BYTE rgbKeyData [];

BYTE DesKeyBlob[] = {
    0x08,0x02,0x00,0x00,0x01,0x66,0x00,0x00, // BLOB header 
    0x08,0x00,0x00,0x00,                     // key length, in bytes
    0xf1,0x0e,0x25,0x7c,0x6b,0xce,0x0d,0x34  // DES key with parity
    };

int _tmain()
{
//--------------------------------------------------------------------
// Declare variables.
//
// hProv:           Cryptographic service provider (CSP). This example
//                  uses the Microsoft Enhanced Cryptographic 
//                  Provider.
// hKey:            Key to be used. In this example, you import the 
//                  key as a PLAINTEXTKEYBLOB.
// dwBlobLen:       Length of the plaintext key.
// pbKeyBlob:       Pointer to the exported key.

HCRYPTPROV hProv  = NULL;
HCRYPTKEY hKey    = NULL;
DWORD dwBlobLen;
BYTE* pbKeyBlob;

//--------------------------------------------------------------------
// Acquire a handle to the CSP.

if(!CryptAcquireContext(
   &hProv,
   NULL,
   MS_ENHANCED_PROV,
   PROV_RSA_FULL,
   CRYPT_VERIFYCONTEXT))
   {
      // If the key container cannot be opened, try creating a new
      // container by specifying a container name and setting the 
      // CRYPT_NEWKEYSET flag.
      if(NTE_BAD_KEYSET == GetLastError())
      {
         if(!CryptAcquireContext(
            &hProv,
            L"mytestcontainer",
            MS_ENHANCED_PROV,
            PROV_RSA_FULL,
            CRYPT_NEWKEYSET | CRYPT_VERIFYCONTEXT))
            {
               printf("Error in AcquireContext 0x%08x \n",
                  GetLastError());
               return 1;
            }
      }
      else 
      {
         printf(" Error in AcquireContext 0x%08x \n",GetLastError());
         return 1;
      }
   }

   // Use the CryptImportKey function to import the PLAINTEXTKEYBLOB
   // BYTE array into the key container. The function returns a 
   // pointer to an HCRYPTKEY variable that contains the handle of
   // the imported key.

   if (!CryptImportKey(
       hProv,
       DesKeyBlob,
       sizeof(DesKeyBlob),
       0,
       CRYPT_EXPORTABLE,
       &hKey ) )
   {
      printf("Error 0x%08x in importing the Des key \n",
         GetLastError());
   }

   // For the purpose of this example, you can export the key and 
   // print it to verify that the plain text key created above is  
   // the key that was imported into the CSP.
   // Call CryptExportKey once to determine the length of the key.
   // Allocate memory for the BLOB, and call CryptExportKey again
   // to retrieve the key from the CSP key container.

   if(!CryptExportKey(   
      hKey,    
      NULL,    
      PLAINTEXTKEYBLOB,
      0,    
      NULL, 
      &dwBlobLen)) 
      {
         printf("Error 0x%08x computing BLOB length.\n",
            GetLastError());
         return 1;
      }

   if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
   {
      printf("Memory has been allocated for the BLOB. \n");
   }
   else
   {
      printf("Out of memory. \n");
      return 1;
   }

   if(!CryptExportKey(   
      hKey, 
      NULL,    
      PLAINTEXTKEYBLOB,    
      0,    
      pbKeyBlob,    
      &dwBlobLen))
      {
         printf("Error 0x%08x exporting key.\n", GetLastError());
         return 1;
      }

   DWORD count = 0;
   printf("Printing Key BLOB for verification \n");
   for(count=0; count < dwBlobLen;)
   {
      printf("%02x",pbKeyBlob[count]);
      count ++;
   }

   // Free resources.

   if(pbKeyBlob)
   {
      free(pbKeyBlob);
   }

   if(hProv)
   {
      CryptReleaseContext(hProv, 0);
   }

    return 0;
}
```



 

 
