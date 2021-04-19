---
description: 雜湊在搭配非對稱式簽署演算法使用時，最適合用來確認資料的完整性。
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: 使用 CNG 建立雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972158"
---
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="f3bad-103">使用 CNG 建立雜湊</span><span class="sxs-lookup"><span data-stu-id="f3bad-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="f3bad-104">[*雜湊*](/windows/desktop/SecGloss/h-gly)是在資料區塊上執行的單向作業，用來建立代表資料內容的唯一雜湊值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="f3bad-105">無論何時執行雜湊，相同資料上執行的相同 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly) 一律會產生相同的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="f3bad-106">如果有任何資料變更，雜湊值將會適當地變更。</span><span class="sxs-lookup"><span data-stu-id="f3bad-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="f3bad-107">雜湊不適合用來加密資料，因為它們並非用來從雜湊值重現原始資料。</span><span class="sxs-lookup"><span data-stu-id="f3bad-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="f3bad-108">雜湊在搭配非對稱式簽署演算法使用時，最適合用來確認資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f3bad-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="f3bad-109">例如，如果您雜湊文字訊息、簽署雜湊，並且將簽署的雜湊值包含在原始訊息中，收件者可以驗證已簽署的雜湊、建立所接收訊息的雜湊值，然後將此雜湊值與原始訊息中包含的帶正負號雜湊值進行比較。</span><span class="sxs-lookup"><span data-stu-id="f3bad-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="f3bad-110">如果兩個雜湊值相同，收件者可以合理確定原始訊息尚未經過修改。</span><span class="sxs-lookup"><span data-stu-id="f3bad-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="f3bad-111">雜湊值的大小是針對特定雜湊演算法而固定的。</span><span class="sxs-lookup"><span data-stu-id="f3bad-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="f3bad-112">這表示無論資料區塊的大小或小，雜湊值一律會是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="f3bad-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="f3bad-113">例如，SHA256 雜湊演算法的雜湊值大小為256位。</span><span class="sxs-lookup"><span data-stu-id="f3bad-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="f3bad-114">建立雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="f3bad-115">建立可重複使用的雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="f3bad-116">複製雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="f3bad-117">建立雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-117">Creating a Hashing Object</span></span>

<span data-ttu-id="f3bad-118">若要使用 CNG 建立雜湊，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f3bad-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="f3bad-119">開啟支援所需演算法的演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="f3bad-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="f3bad-120">典型的雜湊演算法包括 MD2、MD4、MD5、SHA-1 和 SHA256。</span><span class="sxs-lookup"><span data-stu-id="f3bad-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="f3bad-121">呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) 函數，並在 *pszAlgId* 參數中指定適當的演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3bad-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="f3bad-122">函數會傳回提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3bad-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="f3bad-123">請執行下列步驟來建立雜湊物件：</span><span class="sxs-lookup"><span data-stu-id="f3bad-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="f3bad-124">藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函式來取出 **BCRYPT \_ 物件 \_ 長度** 屬性，以取得物件的大小。</span><span class="sxs-lookup"><span data-stu-id="f3bad-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="f3bad-125">配置記憶體來保存雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="f3bad-126">藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數來建立物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="f3bad-127">雜湊資料。</span><span class="sxs-lookup"><span data-stu-id="f3bad-127">Hash the data.</span></span> <span data-ttu-id="f3bad-128">這牽涉到呼叫 [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) 函數一或多次。</span><span class="sxs-lookup"><span data-stu-id="f3bad-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="f3bad-129">每個呼叫都會將指定的資料附加到雜湊中。</span><span class="sxs-lookup"><span data-stu-id="f3bad-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="f3bad-130">請執行下列步驟來取得雜湊值：</span><span class="sxs-lookup"><span data-stu-id="f3bad-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="f3bad-131">藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數來取得 **BCRYPT \_ HASH \_ LENGTH** 屬性，以抓取值的大小。</span><span class="sxs-lookup"><span data-stu-id="f3bad-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="f3bad-132">配置記憶體以保留值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="f3bad-133">藉由呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) 函數來取得雜湊值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="f3bad-134">呼叫這個函數之後，雜湊物件就不再有效。</span><span class="sxs-lookup"><span data-stu-id="f3bad-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="f3bad-135">若要完成此程式，您必須執行下列清除步驟：</span><span class="sxs-lookup"><span data-stu-id="f3bad-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="f3bad-136">將雜湊控制碼傳遞至 [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) 函式，以關閉雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="f3bad-137">釋放您配置給雜湊物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f3bad-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="f3bad-138">如果您不會建立任何其他雜湊物件，請將提供者控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式，以關閉演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="f3bad-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="f3bad-139">如果您要建立更杜哈希物件，建議您重複使用演算法提供者，而不是多次建立和終結相同類型的演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="f3bad-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="f3bad-140">當您完成使用雜湊值記憶體時，請釋放它。</span><span class="sxs-lookup"><span data-stu-id="f3bad-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="f3bad-141">下列範例顯示如何使用 CNG 建立雜湊值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-141">The following example shows how to create a hash value by using CNG.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
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
                                        hAlg, 
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
                                        hAlg, 
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

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
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

}

```



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="f3bad-142">建立可重複使用的雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="f3bad-143">從 Windows 8 和 Windows Server 2012 開始，您可以在需要您快速計算多個雜湊或 Hmac 的案例中，建立可重複使用的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="f3bad-144">若要這麼做，請在呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式時指定 **BCRYPT \_ HASH \_ 可重複使用的 \_ 旗** 標。</span><span class="sxs-lookup"><span data-stu-id="f3bad-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="f3bad-145">所有 Microsoft 雜湊演算法提供者都支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="f3bad-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="f3bad-146">使用這個旗標建立的雜湊物件，可以在呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) 之後立即重複使用，就像是藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)來最近建立的一樣。</span><span class="sxs-lookup"><span data-stu-id="f3bad-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="f3bad-147">請執行下列步驟來建立可重複使用的雜湊物件：</span><span class="sxs-lookup"><span data-stu-id="f3bad-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="f3bad-148">開啟支援所需雜湊演算法的演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="f3bad-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="f3bad-149">呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式，並在 *pszAlgId* 參數中指定適當的演算法識別碼，並在 *dwFlags* 參數中 **BCRYPT \_ 雜湊 \_ 可重複使用的 \_ 旗** 標。</span><span class="sxs-lookup"><span data-stu-id="f3bad-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="f3bad-150">函數會傳回提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3bad-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="f3bad-151">請執行下列步驟來建立雜湊物件：</span><span class="sxs-lookup"><span data-stu-id="f3bad-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="f3bad-152">藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函式來取出 **BCRYPT \_ 物件 \_ 長度** 屬性，以取得物件的大小。</span><span class="sxs-lookup"><span data-stu-id="f3bad-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="f3bad-153">配置記憶體來保存雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="f3bad-154">藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數來建立物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="f3bad-155">在 *dwFlags* 參數中指定 **BCRYPT \_ HASH \_ 可重複使用的 \_ 旗** 標。</span><span class="sxs-lookup"><span data-stu-id="f3bad-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="f3bad-156">藉由呼叫 [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) 函數來雜湊資料。</span><span class="sxs-lookup"><span data-stu-id="f3bad-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="f3bad-157">請執行下列步驟來取得雜湊值：</span><span class="sxs-lookup"><span data-stu-id="f3bad-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="f3bad-158">藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數取得雜湊值的大小，以取得 **BCRYPT \_ 雜湊 \_ 長度** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f3bad-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="f3bad-159">配置記憶體以保留值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="f3bad-160">藉由呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)來取得雜湊值。</span><span class="sxs-lookup"><span data-stu-id="f3bad-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="f3bad-161">若要重複使用具有新資料的雜湊物件，請移至步驟3。</span><span class="sxs-lookup"><span data-stu-id="f3bad-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="f3bad-162">若要完成此程式，您必須執行下列清除步驟：</span><span class="sxs-lookup"><span data-stu-id="f3bad-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="f3bad-163">將雜湊控制碼傳遞至 [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) 函式，以關閉雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="f3bad-164">釋放您配置給雜湊物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f3bad-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="f3bad-165">如果您不會建立任何其他雜湊物件，請將提供者控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式，以關閉演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="f3bad-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="f3bad-166">當您完成使用雜湊值記憶體時，請釋放它。</span><span class="sxs-lookup"><span data-stu-id="f3bad-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="f3bad-167">複製雜湊物件</span><span class="sxs-lookup"><span data-stu-id="f3bad-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="f3bad-168">在某些情況下，雜湊一些常見的資料可能會很有用，然後再從一般資料建立兩個不同的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="f3bad-169">您不需要建立兩個不同的雜湊物件，並將一般資料雜湊兩次，即可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="f3bad-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="f3bad-170">您可以建立單一雜湊物件，並將所有的通用資料新增至雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="f3bad-171">然後，您可以使用 [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) 函式來建立原始雜湊物件的重複項。</span><span class="sxs-lookup"><span data-stu-id="f3bad-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="f3bad-172">複製的雜湊物件包含所有相同的狀態資訊和雜湊的資料做為原始資料，但它是完全獨立的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="f3bad-173">您現在可以將唯一資料新增至每個雜湊物件，並取得雜湊值（如範例所示）。</span><span class="sxs-lookup"><span data-stu-id="f3bad-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="f3bad-174">這項技術在雜湊可能有大量的一般資料時很實用。</span><span class="sxs-lookup"><span data-stu-id="f3bad-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="f3bad-175">您只需將通用資料新增至原始雜湊一次，然後就可以複製雜湊物件來取得唯一的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="f3bad-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 
