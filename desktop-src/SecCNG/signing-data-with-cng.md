---
description: 資料簽署不會保護資料。 它只會驗證資料的完整性。
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: 使用 CNG 簽署資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115176"
---
# <a name="signing-data-with-cng"></a><span data-ttu-id="0fa95-104">使用 CNG 簽署資料</span><span class="sxs-lookup"><span data-stu-id="0fa95-104">Signing Data with CNG</span></span>

<span data-ttu-id="0fa95-105">資料簽署不會保護資料。</span><span class="sxs-lookup"><span data-stu-id="0fa95-105">Data signing does not protect the data.</span></span> <span data-ttu-id="0fa95-106">它只會驗證資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="0fa95-106">It only to verifies the integrity of the data.</span></span> <span data-ttu-id="0fa95-107">傳送者會使用私密金鑰來雜湊資料和簽署 (加密) 雜湊。</span><span class="sxs-lookup"><span data-stu-id="0fa95-107">The sender hashes that data and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="0fa95-108">預期的收件者會藉由建立所接收之資料的雜湊、解密簽章以取得原始雜湊，以及比較這兩個雜湊來執行驗證。</span><span class="sxs-lookup"><span data-stu-id="0fa95-108">The intended recipient performs verification by creating a hash of the data received, decrypting the signature to obtain the original hash, and comparing the two hashes.</span></span>

<span data-ttu-id="0fa95-109">當資料經過簽署時，傳送者會建立 [*雜湊*](/windows/desktop/SecGloss/h-gly) 值，並使用私密金鑰來簽署 (加密) 雜湊。</span><span class="sxs-lookup"><span data-stu-id="0fa95-109">When data is signed, the sender creates a [*hash*](/windows/desktop/SecGloss/h-gly) value and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="0fa95-110">此簽章接著會附加至資料，並傳送至收件者的訊息中。</span><span class="sxs-lookup"><span data-stu-id="0fa95-110">This signature is then attached to the data and sent in a message to a recipient.</span></span> <span data-ttu-id="0fa95-111">用來建立簽章的雜湊演算法必須由收件者事先知道，或在訊息中識別。</span><span class="sxs-lookup"><span data-stu-id="0fa95-111">The hashing algorithm that was used to create the signature must be known in advance by the recipient or identified in the message.</span></span> <span data-ttu-id="0fa95-112">這是如何完成的，取決於訊息通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0fa95-112">How this is done is up to the message protocol.</span></span>

<span data-ttu-id="0fa95-113">為了驗證簽章，收件者會從訊息中解壓縮資料和簽章。</span><span class="sxs-lookup"><span data-stu-id="0fa95-113">To verify the signature, the recipient extracts the data and the signature from the message.</span></span> <span data-ttu-id="0fa95-114">然後，收件者會從資料建立另一個雜湊值、使用傳送者的公開金鑰來解密簽署的雜湊，並比較這兩個雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0fa95-114">The recipient then creates another hash value from the data, decrypts the signed hash by using the sender's public key, and compares the two hash values.</span></span> <span data-ttu-id="0fa95-115">如果值相同，就會驗證簽章，並假設資料沒有改變。</span><span class="sxs-lookup"><span data-stu-id="0fa95-115">If the values are identical, the signature has been verified and the data is assumed to be unaltered.</span></span>

<span data-ttu-id="0fa95-116">**使用 CNG 建立簽章**</span><span class="sxs-lookup"><span data-stu-id="0fa95-116">**To create a signature by using CNG**</span></span>

1.  <span data-ttu-id="0fa95-117">使用 CNG 雜湊函數建立資料的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0fa95-117">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="0fa95-118">如需建立雜湊的詳細資訊，請參閱 [使用 CNG 建立雜湊](creating-a-hash-with-cng.md)。</span><span class="sxs-lookup"><span data-stu-id="0fa95-118">For more information about creating a hash, see [Creating a Hash With CNG](creating-a-hash-with-cng.md).</span></span>
2.  <span data-ttu-id="0fa95-119">建立非對稱金鑰來簽署雜湊。</span><span class="sxs-lookup"><span data-stu-id="0fa95-119">Create an asymmetric key to sign the hash.</span></span> <span data-ttu-id="0fa95-120">您可以使用 [Cng 金鑰儲存](cng-key-storage-functions.md) 函式建立持續性金鑰，或使用 [Cng 密碼編譯基本](cng-cryptographic-primitive-functions.md)函式來建立暫時金鑰。</span><span class="sxs-lookup"><span data-stu-id="0fa95-120">You can either create a persistent key with the [CNG Key Storage Functions](cng-key-storage-functions.md) or an ephemeral key with the [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>
3.  <span data-ttu-id="0fa95-121">您可以使用 [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) 或 [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) 函數來簽署 (加密) 雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0fa95-121">Use either the [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) or the [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) function to sign (encrypt) the hash value.</span></span> <span data-ttu-id="0fa95-122">此函數會使用非對稱金鑰來簽署雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0fa95-122">This function signs the hash value by using the asymmetric key.</span></span>
4.  <span data-ttu-id="0fa95-123">將資料和簽章合併成可以傳送給預定收件者的訊息。</span><span class="sxs-lookup"><span data-stu-id="0fa95-123">Combine the data and signature into a message which can be sent sent to the intended recipient.</span></span>

<span data-ttu-id="0fa95-124">**使用 CNG 驗證簽章**</span><span class="sxs-lookup"><span data-stu-id="0fa95-124">**To verify a signature by using CNG**</span></span>

1.  <span data-ttu-id="0fa95-125">從訊息中解壓縮資料和簽章。</span><span class="sxs-lookup"><span data-stu-id="0fa95-125">Extract the data and signature from the message.</span></span>
2.  <span data-ttu-id="0fa95-126">使用 CNG 雜湊函數建立資料的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="0fa95-126">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="0fa95-127">使用的雜湊演算法必須與用來簽署雜湊的演算法相同。</span><span class="sxs-lookup"><span data-stu-id="0fa95-127">The hashing algorithm used must be the same algorithm that was used to sign he hash.</span></span>
3.  <span data-ttu-id="0fa95-128">取得用來簽署雜湊之非對稱金鑰組的公開部分。</span><span class="sxs-lookup"><span data-stu-id="0fa95-128">Obtain the public portion of the asymmetric key pair that was used to sign the hash.</span></span> <span data-ttu-id="0fa95-129">您取得此金鑰的方式取決於金鑰的建立和保存方式。</span><span class="sxs-lookup"><span data-stu-id="0fa95-129">How you obtain this key depends on how the key was created and persisted.</span></span> <span data-ttu-id="0fa95-130">如果金鑰是使用 [CNG 金鑰儲存](cng-key-storage-functions.md)函式建立或載入，您將使用 [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 函式來載入保存的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0fa95-130">If the key was created or loaded with the [CNG Key Storage Functions](cng-key-storage-functions.md), you will use the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function to load the persisted key.</span></span> <span data-ttu-id="0fa95-131">如果金鑰是暫時金鑰，則必須將它儲存至金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="0fa95-131">If the key is an ephemeral key, then it would have to have been saved to a key BLOB.</span></span> <span data-ttu-id="0fa95-132">您必須將此金鑰 BLOB 傳遞給 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 或 [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) 函式。</span><span class="sxs-lookup"><span data-stu-id="0fa95-132">You need to pass this key BLOB to either the [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) or the [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) function.</span></span>
4.  <span data-ttu-id="0fa95-133">將新的雜湊值、簽章和金鑰控制碼傳遞至 [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) 或 [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) 函數。</span><span class="sxs-lookup"><span data-stu-id="0fa95-133">Pass the new hash value, the signature, and the key handle to either the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) or the [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) function.</span></span> <span data-ttu-id="0fa95-134">這些函式會使用公開金鑰來解密簽章，並比較解密的雜湊與步驟2中計算出的雜湊，以執行驗證。</span><span class="sxs-lookup"><span data-stu-id="0fa95-134">These functions perform verification by using the public key to decrypt the signature and comparing the decrypted hash to the hash computed in step 2.</span></span> <span data-ttu-id="0fa95-135">如果簽章符合雜湊或 **狀態 \_ 無效 \_** 的簽章（如果簽章不符合雜湊），則 BCryptVerifySignature 函式會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="0fa95-135">The **BCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **STATUS\_INVALID\_SIGNATURE** if the signature does not match the hash.</span></span> <span data-ttu-id="0fa95-136">如果簽章與雜湊或不相符的簽章不符，則 **NCryptVerifySignature** 函式會傳回 **狀態 \_ 成功**。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="0fa95-136">The **NCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **NTE\_BAD\_SIGNATURE** if the signature does not match the hash.</span></span>

## <a name="signing-and-verifying-data-example"></a><span data-ttu-id="0fa95-137">簽署和驗證資料範例</span><span class="sxs-lookup"><span data-stu-id="0fa95-137">Signing and Verifying Data Example</span></span>

<span data-ttu-id="0fa95-138">下列範例示範如何使用密碼編譯基本 Api，以保存的金鑰簽署資料，並使用暫時金鑰驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="0fa95-138">The following example shows how to use the cryptographic primitive APIs to sign data with a persisted key and verify the signature with an ephemeral key.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for ECDSA 256 signing using CNG
    
    Example for use of BCrypt/NCrypt API
    
    Persisted key for signing and ephemeral key for verification

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>
#include <ncrypt.h>


#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const  BYTE rgbMsg[] =
{
    0x04, 0x87, 0xec, 0x66, 0xa8, 0xbf, 0x17, 0xa6,
    0xe3, 0x62, 0x6f, 0x1a, 0x55, 0xe2, 0xaf, 0x5e,
    0xbc, 0x54, 0xa4, 0xdc, 0x68, 0x19, 0x3e, 0x94,
};

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{
    NCRYPT_PROV_HANDLE      hProv           = NULL;
    NCRYPT_KEY_HANDLE       hKey            = NULL;
    BCRYPT_KEY_HANDLE       hTmpKey         = NULL;
    SECURITY_STATUS         secStatus       = ERROR_SUCCESS;
    BCRYPT_ALG_HANDLE       hHashAlg        = NULL,
                            hSignAlg        = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbBlob          = 0,
                            cbSignature     = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL,
                            pbBlob          = NULL,
                            pbSignature     = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hHashAlg,
                                                BCRYPT_SHA1_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hSignAlg,
                                                BCRYPT_ECDSA_P256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hHashAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    //open handle to KSP
    if(FAILED(secStatus = NCryptOpenStorageProvider(
                                                &hProv, 
                                                MS_KEY_STORAGE_PROVIDER, 
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptOpenStorageProvider\n", secStatus);
        goto Cleanup;
    }

    //create a persisted key
    if(FAILED(secStatus = NCryptCreatePersistedKey(
                                                hProv,
                                                &hKey,
                                                NCRYPT_ECDSA_P256_ALGORITHM,
                                                L"my ecc key",
                                                0,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptCreatePersistedKey\n", secStatus);
        goto Cleanup;
    }

    //create key on disk
    if(FAILED(secStatus = NCryptFinalizeKey(hKey, 0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptFinalizeKey\n", secStatus);
        goto Cleanup;
    }

    //sign the hash
    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    NULL,
                                    0,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }


    //allocate the signature buffer
    pbSignature = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbSignature);
    if(NULL == pbSignature)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    pbSignature,
                                    cbSignature,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        pbBlob,
                                        cbBlob,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptImportKeyPair(
                                            hSignAlg,
                                            NULL,
                                            BCRYPT_ECCPUBLIC_BLOB,
                                            &hTmpKey,
                                            pbBlob,
                                            cbBlob,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptImportKeyPair\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptVerifySignature(
                                            hTmpKey,
                                            NULL,
                                            pbHash,
                                            cbHash,
                                            pbSignature,
                                            cbSignature,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptVerifySignature\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hHashAlg)
    {
        BCryptCloseAlgorithmProvider(hHashAlg,0);
    }

    if(hSignAlg)
    {
        BCryptCloseAlgorithmProvider(hSignAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

    if(pbSignature)
    {
        HeapFree(GetProcessHeap(), 0, pbSignature);
    }

    if(pbBlob)
    {
        HeapFree(GetProcessHeap(), 0, pbBlob);
    }

    if (hTmpKey)    
    {
        BCryptDestroyKey(hTmpKey);
    }

    if (hKey)    
    {
        NCryptDeleteKey(hKey, 0);
    }

    if (hProv)    
    {
        NCryptFreeObject(hProv);
    }    
}


```



 

 
