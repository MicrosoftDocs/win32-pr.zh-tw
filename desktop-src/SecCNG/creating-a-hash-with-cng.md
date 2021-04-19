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
# <a name="creating-a-hash-with-cng"></a>使用 CNG 建立雜湊

[*雜湊*](/windows/desktop/SecGloss/h-gly)是在資料區塊上執行的單向作業，用來建立代表資料內容的唯一雜湊值。 無論何時執行雜湊，相同資料上執行的相同 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly) 一律會產生相同的雜湊值。 如果有任何資料變更，雜湊值將會適當地變更。

雜湊不適合用來加密資料，因為它們並非用來從雜湊值重現原始資料。 雜湊在搭配非對稱式簽署演算法使用時，最適合用來確認資料的完整性。 例如，如果您雜湊文字訊息、簽署雜湊，並且將簽署的雜湊值包含在原始訊息中，收件者可以驗證已簽署的雜湊、建立所接收訊息的雜湊值，然後將此雜湊值與原始訊息中包含的帶正負號雜湊值進行比較。 如果兩個雜湊值相同，收件者可以合理確定原始訊息尚未經過修改。

雜湊值的大小是針對特定雜湊演算法而固定的。 這表示無論資料區塊的大小或小，雜湊值一律會是相同的大小。 例如，SHA256 雜湊演算法的雜湊值大小為256位。

-   [建立雜湊物件](#creating-a-hashing-object)
-   [建立可重複使用的雜湊物件](#creating-a-reusable-hashing-object)
-   [複製雜湊物件](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>建立雜湊物件

若要使用 CNG 建立雜湊，請執行下列步驟：

1.  開啟支援所需演算法的演算法提供者。 典型的雜湊演算法包括 MD2、MD4、MD5、SHA-1 和 SHA256。 呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) 函數，並在 *pszAlgId* 參數中指定適當的演算法識別碼。 函數會傳回提供者的控制碼。
2.  請執行下列步驟來建立雜湊物件：

    1.  藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函式來取出 **BCRYPT \_ 物件 \_ 長度** 屬性，以取得物件的大小。
    2.  配置記憶體來保存雜湊物件。
    3.  藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數來建立物件。

3.  雜湊資料。 這牽涉到呼叫 [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) 函數一或多次。 每個呼叫都會將指定的資料附加到雜湊中。
4.  請執行下列步驟來取得雜湊值：

    1.  藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數來取得 **BCRYPT \_ HASH \_ LENGTH** 屬性，以抓取值的大小。
    2.  配置記憶體以保留值。
    3.  藉由呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) 函數來取得雜湊值。 呼叫這個函數之後，雜湊物件就不再有效。

5.  若要完成此程式，您必須執行下列清除步驟：

    1.  將雜湊控制碼傳遞至 [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) 函式，以關閉雜湊物件。
    2.  釋放您配置給雜湊物件的記憶體。
    3.  如果您不會建立任何其他雜湊物件，請將提供者控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式，以關閉演算法提供者。

        如果您要建立更杜哈希物件，建議您重複使用演算法提供者，而不是多次建立和終結相同類型的演算法提供者。

    4.  當您完成使用雜湊值記憶體時，請釋放它。

下列範例顯示如何使用 CNG 建立雜湊值。


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



## <a name="creating-a-reusable-hashing-object"></a>建立可重複使用的雜湊物件

從 Windows 8 和 Windows Server 2012 開始，您可以在需要您快速計算多個雜湊或 Hmac 的案例中，建立可重複使用的雜湊物件。 若要這麼做，請在呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式時指定 **BCRYPT \_ HASH \_ 可重複使用的 \_ 旗** 標。 所有 Microsoft 雜湊演算法提供者都支援此旗標。 使用這個旗標建立的雜湊物件，可以在呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) 之後立即重複使用，就像是藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)來最近建立的一樣。 請執行下列步驟來建立可重複使用的雜湊物件：

1.  開啟支援所需雜湊演算法的演算法提供者。 呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式，並在 *pszAlgId* 參數中指定適當的演算法識別碼，並在 *dwFlags* 參數中 **BCRYPT \_ 雜湊 \_ 可重複使用的 \_ 旗** 標。 函數會傳回提供者的控制碼。
2.  請執行下列步驟來建立雜湊物件：

    1.  藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函式來取出 **BCRYPT \_ 物件 \_ 長度** 屬性，以取得物件的大小。
    2.  配置記憶體來保存雜湊物件。
    3.  藉由呼叫 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) 函數來建立物件。 在 *dwFlags* 參數中指定 **BCRYPT \_ HASH \_ 可重複使用的 \_ 旗** 標。

3.  藉由呼叫 [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) 函數來雜湊資料。
4.  請執行下列步驟來取得雜湊值：

    1.  藉由呼叫 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數取得雜湊值的大小，以取得 **BCRYPT \_ 雜湊 \_ 長度** 屬性。
    2.  配置記憶體以保留值。
    3.  藉由呼叫 [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)來取得雜湊值。

5.  若要重複使用具有新資料的雜湊物件，請移至步驟3。
6.  若要完成此程式，您必須執行下列清除步驟：

    1.  將雜湊控制碼傳遞至 [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) 函式，以關閉雜湊物件。
    2.  釋放您配置給雜湊物件的記憶體。
    3.  如果您不會建立任何其他雜湊物件，請將提供者控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式，以關閉演算法提供者。
    4.  當您完成使用雜湊值記憶體時，請釋放它。

## <a name="duplicating-a-hash-object"></a>複製雜湊物件

在某些情況下，雜湊一些常見的資料可能會很有用，然後再從一般資料建立兩個不同的雜湊物件。 您不需要建立兩個不同的雜湊物件，並將一般資料雜湊兩次，即可完成此作業。 您可以建立單一雜湊物件，並將所有的通用資料新增至雜湊物件。 然後，您可以使用 [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) 函式來建立原始雜湊物件的重複項。 複製的雜湊物件包含所有相同的狀態資訊和雜湊的資料做為原始資料，但它是完全獨立的雜湊物件。 您現在可以將唯一資料新增至每個雜湊物件，並取得雜湊值（如範例所示）。 這項技術在雜湊可能有大量的一般資料時很實用。 您只需將通用資料新增至原始雜湊一次，然後就可以複製雜湊物件來取得唯一的雜湊物件。

 

 
