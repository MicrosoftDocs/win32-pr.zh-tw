---
description: CNG 可讓您使用最少的函式呼叫來加密資料，並可讓您執行所有的記憶體管理。
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: 使用 CNG 加密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000238"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="2e7da-103">使用 CNG 加密資料</span><span class="sxs-lookup"><span data-stu-id="2e7da-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="2e7da-104">任何密碼編譯 API 的主要用途是加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="2e7da-105">CNG 可讓您使用最少的函式呼叫來加密資料，並可讓您執行所有的記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="2e7da-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="2e7da-106">雖然許多通訊協定的執行細節都是由使用者所組成，但是 CNG 提供了執行實際資料加密和解密工作的基本專案。</span><span class="sxs-lookup"><span data-stu-id="2e7da-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="2e7da-107">加密資料</span><span class="sxs-lookup"><span data-stu-id="2e7da-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="2e7da-108">加密資料範例</span><span class="sxs-lookup"><span data-stu-id="2e7da-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="2e7da-109">解密資料</span><span class="sxs-lookup"><span data-stu-id="2e7da-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="2e7da-110">加密資料</span><span class="sxs-lookup"><span data-stu-id="2e7da-110">Encrypting Data</span></span>

<span data-ttu-id="2e7da-111">若要加密資料，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2e7da-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2e7da-112">開啟支援加密的演算法提供者，例如 **BCRYPT \_ DES \_ 演算法**。</span><span class="sxs-lookup"><span data-stu-id="2e7da-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2e7da-113">建立用來加密資料的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e7da-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="2e7da-114">您可以使用下列任何一項功能來建立金鑰：</span><span class="sxs-lookup"><span data-stu-id="2e7da-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="2e7da-115">非對稱提供者的 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)或 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 。</span><span class="sxs-lookup"><span data-stu-id="2e7da-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="2e7da-116">對稱提供者的 [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey)或 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 。</span><span class="sxs-lookup"><span data-stu-id="2e7da-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="2e7da-117">使用非對稱金鑰進行資料加密和解密，相較于對稱金鑰加密，需要大量計算。</span><span class="sxs-lookup"><span data-stu-id="2e7da-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="2e7da-118">如果您需要使用非對稱金鑰來加密資料，您應該使用對稱金鑰來加密資料、使用非對稱金鑰來加密對稱金鑰，並在訊息中包含加密的對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e7da-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="2e7da-119">然後，收件者可以解密對稱金鑰，並使用對稱金鑰來解密資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="2e7da-120">取得加密資料的大小。</span><span class="sxs-lookup"><span data-stu-id="2e7da-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="2e7da-121">這是根據加密演算法、填補配置 (是否有任何) ，以及要加密之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="2e7da-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="2e7da-122">您可以使用 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt)函式來取得加密的資料大小，並為 *PbOutput* 參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2e7da-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2e7da-123">除了 *pbInput* 參數（在此案例中不會使用），所有其他參數都必須與資料實際加密一樣。</span><span class="sxs-lookup"><span data-stu-id="2e7da-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2e7da-124">您可以使用相同的緩衝區將資料加密，或將資料加密為個別的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2e7da-125">如果您想要將資料加密，請在 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt)函數中傳遞 *pbInput* 和 *pbOutput* 參數的純文字緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="2e7da-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="2e7da-126">加密的資料大小可能會大於未加密的資料大小，因此純文字緩衝區必須夠大，才能容納加密的資料，而不只是純文字。</span><span class="sxs-lookup"><span data-stu-id="2e7da-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="2e7da-127">您可以使用在步驟3中取得的大小來配置純文字緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="2e7da-128">如果您想要將資料加密為不同的緩衝區，請使用在步驟3中取得的大小為加密資料配置記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="2e7da-129">呼叫 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 函數來加密資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="2e7da-130">此函數會將加密的資料寫入 *pbOutput* 參數中提供的位置。</span><span class="sxs-lookup"><span data-stu-id="2e7da-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="2e7da-131">視需要保存加密的資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="2e7da-132">重複步驟5和6，直到所有資料都已加密為止。</span><span class="sxs-lookup"><span data-stu-id="2e7da-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="2e7da-133">加密資料範例</span><span class="sxs-lookup"><span data-stu-id="2e7da-133">Encrypting Data Example</span></span>

<span data-ttu-id="2e7da-134">下列範例示範如何使用 advanced encryption standard 對稱式加密演算法，透過 CNG 加密資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


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



## <a name="decrypting-data"></a><span data-ttu-id="2e7da-135">解密資料</span><span class="sxs-lookup"><span data-stu-id="2e7da-135">Decrypting Data</span></span>

<span data-ttu-id="2e7da-136">若要將資料解密，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2e7da-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2e7da-137">開啟支援加密的演算法提供者，例如 **BCRYPT \_ DES \_ 演算法**。</span><span class="sxs-lookup"><span data-stu-id="2e7da-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2e7da-138">取得用來加密資料的金鑰，然後使用該金鑰來取得金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e7da-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="2e7da-139">取得解密資料的大小。</span><span class="sxs-lookup"><span data-stu-id="2e7da-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="2e7da-140">這是根據加密演算法、填補配置 (是否有任何) ，以及要解密的資料大小。</span><span class="sxs-lookup"><span data-stu-id="2e7da-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="2e7da-141">您可以使用 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)函式來取得加密的資料大小，並為 *PbOutput* 參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2e7da-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2e7da-142">指定填補配置和 [*初始化向量*](/windows/desktop/SecGloss/i-gly) (IV) 的參數必須與加密資料時相同，除非 *pbInput* 參數，在此情況下不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="2e7da-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2e7da-143">配置已解密資料的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="2e7da-144">您可以使用相同的緩衝區就地解密資料，或將資料解密成個別的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2e7da-145">如果您想要就地解密資料，請在 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)函數中傳遞 *pbInput* 和 *pbOutput* 參數的加密文字緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="2e7da-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="2e7da-146">如果您想要將資料解密成不同的緩衝區，請使用在步驟3中取得的大小來配置解密資料的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2e7da-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="2e7da-147">呼叫 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) 函數來解密資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="2e7da-148">指定填補配置和 IV 的參數必須與資料加密時相同。</span><span class="sxs-lookup"><span data-stu-id="2e7da-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="2e7da-149">此函數會將解密的資料寫入 *pbOutput* 參數中提供的位置。</span><span class="sxs-lookup"><span data-stu-id="2e7da-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="2e7da-150">視需要保存解密的資料。</span><span class="sxs-lookup"><span data-stu-id="2e7da-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="2e7da-151">重複步驟5和6，直到所有資料都已解密為止。</span><span class="sxs-lookup"><span data-stu-id="2e7da-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 
