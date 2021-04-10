---
description: 建立命名的金鑰容器，並將簽章金鑰組和交換金鑰組新增至容器。
ms.assetid: b9d13024-0e53-4930-9962-a2a0d0cb88de
title: 範例 C 程式：建立金鑰容器並產生金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e389df22cb4e745cf1c1a65542a17eeabe9b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193896"
---
# <a name="example-c-program-creating-a-key-container-and-generating-keys"></a><span data-ttu-id="9dd11-103">範例 C 程式：建立金鑰容器並產生金鑰</span><span class="sxs-lookup"><span data-stu-id="9dd11-103">Example C Program: Creating a Key Container and Generating Keys</span></span>

<span data-ttu-id="9dd11-104">下列範例會建立名為 [*key 容器*](../secgloss/k-gly.md) ，並將簽章 [*金鑰*](../secgloss/s-gly.md) 組和 [*交換金鑰*](../secgloss/e-gly.md) 組新增至容器。</span><span class="sxs-lookup"><span data-stu-id="9dd11-104">The following example creates a named [*key container*](../secgloss/k-gly.md) and adds a [*signature key pair*](../secgloss/s-gly.md) and an [*exchange key pair*](../secgloss/e-gly.md) to the container.</span></span> <span data-ttu-id="9dd11-105">即使已有名稱相同的金鑰容器和密碼編譯金鑰，此範例也可以執行而不會發生問題。</span><span class="sxs-lookup"><span data-stu-id="9dd11-105">This example can be run without problem even if the named key container and cryptographic keys already exist.</span></span>

> [!Note]  
> <span data-ttu-id="9dd11-106">應用程式不應使用預設金鑰容器來儲存私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="9dd11-106">An application should not use the default key container to store private keys.</span></span> <span data-ttu-id="9dd11-107">當多個應用程式使用相同的容器時，一個應用程式可能會變更或終結另一個應用程式必須提供的金鑰。</span><span class="sxs-lookup"><span data-stu-id="9dd11-107">When multiple applications use the same container, one application may change or destroy the keys that another application needs to have available.</span></span> <span data-ttu-id="9dd11-108">建議應用程式使用連結至應用程式的金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="9dd11-108">It is recommended that applications use key containers that are linked to the application.</span></span> <span data-ttu-id="9dd11-109">這麼做可降低其他應用程式使用應用程式正常運作所需的金鑰進行篡改的風險。</span><span class="sxs-lookup"><span data-stu-id="9dd11-109">Doing so reduces the risk of other applications tampering with keys that are necessary for an application to function properly.</span></span>

 

<span data-ttu-id="9dd11-110">此範例示範下列工作和 CryptoAPI 函式：</span><span class="sxs-lookup"><span data-stu-id="9dd11-110">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

1.  <span data-ttu-id="9dd11-111">它會嘗試取得命名的金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="9dd11-111">It attempts to acquire the named key container.</span></span> <span data-ttu-id="9dd11-112">如果已命名的金鑰容器不存在，則會建立該容器。</span><span class="sxs-lookup"><span data-stu-id="9dd11-112">If the named key container does not already exist, it is created.</span></span>
2.  <span data-ttu-id="9dd11-113">如果金鑰容器中不存在簽章金鑰組，則會在金鑰容器內建立簽章金鑰組。</span><span class="sxs-lookup"><span data-stu-id="9dd11-113">If a signature key pair does not exist in the key container, it creates a signature key pair within the key container.</span></span>
3.  <span data-ttu-id="9dd11-114">如果金鑰容器中不存在 exchange 金鑰組，則會在金鑰容器內建立交換金鑰組。</span><span class="sxs-lookup"><span data-stu-id="9dd11-114">If an exchange key pair does not exist in the key container, it creates an exchange key pair within the key container.</span></span>

<span data-ttu-id="9dd11-115">每一部電腦上的每個使用者都只需要執行一次這些作業。</span><span class="sxs-lookup"><span data-stu-id="9dd11-115">These operations only need to be performed once for each user on each computer.</span></span> <span data-ttu-id="9dd11-116">如果已建立名為的金鑰容器和金鑰組，此範例不會執行任何作業。</span><span class="sxs-lookup"><span data-stu-id="9dd11-116">If the named key container and key pairs have already been created, this sample performs no operations.</span></span>

<span data-ttu-id="9dd11-117">此範例使用下列 CryptoAPI 函數：</span><span class="sxs-lookup"><span data-stu-id="9dd11-117">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="9dd11-118">**CryptAcquireCoNtext**</span><span class="sxs-lookup"><span data-stu-id="9dd11-118">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [<span data-ttu-id="9dd11-119">**CryptDestroyKey**</span><span class="sxs-lookup"><span data-stu-id="9dd11-119">**CryptDestroyKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)
-   [<span data-ttu-id="9dd11-120">**CryptGenKey**</span><span class="sxs-lookup"><span data-stu-id="9dd11-120">**CryptGenKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
-   [<span data-ttu-id="9dd11-121">**CryptGetUserKey**</span><span class="sxs-lookup"><span data-stu-id="9dd11-121">**CryptGetUserKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)
-   [<span data-ttu-id="9dd11-122">**CryptReleaseCoNtext**</span><span class="sxs-lookup"><span data-stu-id="9dd11-122">**CryptReleaseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

<span data-ttu-id="9dd11-123">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="9dd11-123">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="9dd11-124">這個函式的程式碼會包含在範例中。</span><span class="sxs-lookup"><span data-stu-id="9dd11-124">The code for this function is included with the sample.</span></span> <span data-ttu-id="9dd11-125">這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="9dd11-125">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void main(void) 
{ 
    // Handle for the cryptographic provider context.
    HCRYPTPROV hCryptProv;        
    
    // The name of the container.
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    //---------------------------------------------------------------
    // Begin processing. Attempt to acquire a context by using the 
    // specified key container.
    if(CryptAcquireContext(
        &hCryptProv,
        pszContainerName,
        NULL,
        PROV_RSA_FULL,
        0))
    {
        _tprintf(
            TEXT("A crypto context with the %s key container ")
            TEXT("has been acquired.\n"), 
            pszContainerName);
    }
    else
    { 
        //-----------------------------------------------------------
        // Some sort of error occurred in acquiring the context. 
        // This is most likely due to the specified container 
        // not existing. Create a new key container.
        if(GetLastError() == NTE_BAD_KEYSET)
        {
            if(CryptAcquireContext(
                &hCryptProv, 
                pszContainerName, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("A new key container has been ")
                    TEXT("created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create a new key ")
                    TEXT("container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("CryptAcquireContext failed.\n"));
        }
    }

    //---------------------------------------------------------------
    // A context with a key container is available.
    // Attempt to get the handle to the signature key. 

    // Public/private key handle.
    HCRYPTKEY hKey;               
    
    if(CryptGetUserKey(
        hCryptProv,
        AT_SIGNATURE,
        &hKey))
    {
        _tprintf(TEXT("A signature key is available.\n"));
    }
    else
    {
        _tprintf(TEXT("No signature key is available.\n"));
        if(GetLastError() == NTE_NO_KEY) 
        {
            //-------------------------------------------------------
            // The error was that there is a container but no key.

            // Create a signature key pair. 
            _tprintf(TEXT("The signature key does not exist.\n"));
            _tprintf(TEXT("Create a signature key pair.\n")); 
            if(CryptGenKey(
                hCryptProv,
                AT_SIGNATURE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Created a signature key pair.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred creating a ")
                    TEXT("signature key.\n")); 
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("getting a signature key.\n"));
        }
    } // End if.

    _tprintf(TEXT("A signature key pair existed, or one was ")
        TEXT("created.\n\n"));

    // Destroy the signature key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    } 

    // Next, check the exchange key. 
    if(CryptGetUserKey(
        hCryptProv,
        AT_KEYEXCHANGE,
        &hKey)) 
    {
        _tprintf(TEXT("An exchange key exists.\n"));
    }
    else
    {
        _tprintf(TEXT("No exchange key is available.\n"));

        // Check to determine whether an exchange key 
        // needs to be created.
        if(GetLastError() == NTE_NO_KEY) 
        { 
            // Create a key exchange key pair.
            _tprintf(TEXT("The exchange key does not exist.\n"));
            _tprintf(TEXT("Attempting to create an exchange key ")
                TEXT("pair.\n"));
            if(CryptGenKey(
                hCryptProv,
                AT_KEYEXCHANGE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Exchange key pair created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred attempting to ")
                    TEXT("create an exchange key.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("occurred.\n"));
        }
    }

    // Destroy the exchange key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    }

    // Release the CSP.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv, 0)))
        {
            MyHandleError(TEXT("Error during CryptReleaseContext."));
        }
    } 
    
    _tprintf(TEXT("Everything is okay. A signature key "));
    _tprintf(TEXT("pair and an exchange key exist in "));
    _tprintf(TEXT("the %s key container.\n"), pszContainerName);  
} // End main.
```



 

 
