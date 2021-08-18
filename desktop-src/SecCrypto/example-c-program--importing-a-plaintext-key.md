---
description: 使用 HCRYPTKEY 控制碼來識別索引鍵。
ms.assetid: 23569104-a302-40de-a31a-a4ee22d5f7f2
title: 範例 C 程式：匯入純文字金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58632d7dd3f7411788e26538906c41d1b33ce30888696516e29642f8dbaf00c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874018"
---
# <a name="example-c-program-importing-a-plaintext-key"></a>範例 C 程式：匯入純文字金鑰

此 SDK 中的許多功能都需要您使用 **HCRYPTKEY** 控制碼來識別金鑰。 如果您的金鑰包含在位元組陣列中，您可以使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式來建立控制碼，如下列範例所示。

此範例示範下列工作和 CryptoAPI 函式：

-   藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的控制碼。
-   藉由呼叫 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)將純文字金鑰匯入 CSP 金鑰容器。
-   藉由呼叫 [**CyptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)從金鑰容器匯出金鑰。
-   將匯出的金鑰列印到主控台，以確認純文字金鑰確實已匯入至容器中。
-   釋放保留給純文字金鑰的記憶體。
-   藉由呼叫 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)來發行 CSP。


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



 

 
