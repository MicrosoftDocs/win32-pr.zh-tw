---
description: CNG 可讓您使用最少的函式呼叫來加密資料，並可讓您執行所有的記憶體管理。
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: 使用 CNG 加密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b264518c2a0ccfe0f626c869ba3062c0429941234ca0c286f9e7801961485b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907736"
---
# <a name="encrypting-data-with-cng"></a>使用 CNG 加密資料

任何密碼編譯 API 的主要用途是加密和解密資料。 CNG 可讓您使用最少的函式呼叫來加密資料，並可讓您執行所有的記憶體管理。 雖然許多通訊協定的執行細節都是由使用者所組成，但是 CNG 提供了執行實際資料加密和解密工作的基本專案。

-   [加密資料](#encrypting-data-with-cng)
-   [加密資料範例](#encrypting-data-example)
-   [解密資料](#decrypting-data)

## <a name="encrypting-data"></a>加密資料

若要加密資料，請執行下列步驟：

1.  開啟支援加密的演算法提供者，例如 **BCRYPT \_ DES \_ 演算法**。
2.  建立用來加密資料的金鑰。 您可以使用下列任何一項功能來建立金鑰：
    -   非對稱提供者的 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)或 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 。
    -   對稱提供者的 [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey)或 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 。

    > [!Note]  
    > 使用非對稱金鑰進行資料加密和解密，相較于對稱金鑰加密，需要大量計算。 如果您需要使用非對稱金鑰來加密資料，您應該使用對稱金鑰來加密資料、使用非對稱金鑰來加密對稱金鑰，並在訊息中包含加密的對稱金鑰。 然後，收件者可以解密對稱金鑰，並使用對稱金鑰來解密資料。

     

3.  取得加密資料的大小。 這是根據加密演算法、填補配置 (是否有任何) ，以及要加密之資料的大小。 您可以使用 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt)函式來取得加密的資料大小，並為 *PbOutput* 參數傳遞 **Null** 。 除了 *pbInput* 參數（在此案例中不會使用），所有其他參數都必須與資料實際加密一樣。
4.  您可以使用相同的緩衝區將資料加密，或將資料加密為個別的緩衝區。

    如果您想要將資料加密，請在 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt)函數中傳遞 *pbInput* 和 *pbOutput* 參數的純文字緩衝區指標。 加密的資料大小可能會大於未加密的資料大小，因此純文字緩衝區必須夠大，才能容納加密的資料，而不只是純文字。 您可以使用在步驟3中取得的大小來配置純文字緩衝區。

    如果您想要將資料加密為不同的緩衝區，請使用在步驟3中取得的大小為加密資料配置記憶體緩衝區。

5.  呼叫 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 函數來加密資料。 此函數會將加密的資料寫入 *pbOutput* 參數中提供的位置。
6.  視需要保存加密的資料。
7.  重複步驟5和6，直到所有資料都已加密為止。

## <a name="encrypting-data-example"></a>加密資料範例

下列範例示範如何使用 advanced encryption standard 對稱式加密演算法，透過 CNG 加密資料。


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a>解密資料

若要將資料解密，請執行下列步驟：

1.  開啟支援加密的演算法提供者，例如 **BCRYPT \_ DES \_ 演算法**。
2.  取得用來加密資料的金鑰，然後使用該金鑰來取得金鑰的控制碼。
3.  取得解密資料的大小。 這是根據加密演算法、填補配置 (是否有任何) ，以及要解密的資料大小。 您可以使用 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)函式來取得加密的資料大小，並為 *PbOutput* 參數傳遞 **Null** 。 指定填補配置和 [*初始化向量*](/windows/desktop/SecGloss/i-gly) (IV) 的參數必須與加密資料時相同，除非 *pbInput* 參數，在此情況下不會使用此參數。
4.  配置已解密資料的記憶體緩衝區。
5.  您可以使用相同的緩衝區就地解密資料，或將資料解密成個別的緩衝區。

    如果您想要就地解密資料，請在 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)函數中傳遞 *pbInput* 和 *pbOutput* 參數的加密文字緩衝區指標。

    如果您想要將資料解密成不同的緩衝區，請使用在步驟3中取得的大小來配置解密資料的記憶體緩衝區。

6.  呼叫 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) 函數來解密資料。 指定填補配置和 IV 的參數必須與資料加密時相同。 此函數會將解密的資料寫入 *pbOutput* 參數中提供的位置。
7.  視需要保存解密的資料。
8.  重複步驟5和6，直到所有資料都已解密為止。

 

 
