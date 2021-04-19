---
description: 提供函式來列舉和取得已註冊之提供者的相關資訊。
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: 使用 CNG 的密碼編譯設定功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966718"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="ee06f-103">使用 CNG 的密碼編譯設定功能</span><span class="sxs-lookup"><span data-stu-id="ee06f-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="ee06f-104">CNG API 提供的函式可列舉和取得已註冊之提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee06f-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="ee06f-105">列舉提供者</span><span class="sxs-lookup"><span data-stu-id="ee06f-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="ee06f-106">取得提供者註冊資訊</span><span class="sxs-lookup"><span data-stu-id="ee06f-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="ee06f-107">列舉提供者</span><span class="sxs-lookup"><span data-stu-id="ee06f-107">Enumerating Providers</span></span>

<span data-ttu-id="ee06f-108">您可以使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式來列舉已註冊的提供者。</span><span class="sxs-lookup"><span data-stu-id="ee06f-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="ee06f-109">您可以透過下列兩種方式之一來呼叫 **BCryptEnumRegisteredProviders** 函數：</span><span class="sxs-lookup"><span data-stu-id="ee06f-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="ee06f-110">第一個是讓 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函數配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee06f-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="ee06f-111">這可透過傳遞 *ppBuffer* 參數的 **Null** 指標位址來完成。</span><span class="sxs-lookup"><span data-stu-id="ee06f-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="ee06f-112">此程式碼會配置 [**CRYPT \_ 提供者**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) 結構和相關聯字串所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee06f-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="ee06f-113">以這種方式使用 **BCryptEnumRegisteredProviders** 函式時，您必須將 *PpBuffer* 傳遞給 [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) 函式，以釋放不再需要的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee06f-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="ee06f-114">下列範例示範如何使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函數為您配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee06f-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  <span data-ttu-id="ee06f-115">第二種方法是自行配置所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee06f-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="ee06f-116">這可透過針對 *ppBuffer* 參數呼叫 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders)函式（ **Null** ）來完成。</span><span class="sxs-lookup"><span data-stu-id="ee06f-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="ee06f-117">**BCryptEnumRegisteredProviders** 函式會放在 *pcbBuffer* 參數所指向的值，以及 [**CRYPT \_ 提供者**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers)結構和所有字串所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee06f-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="ee06f-118">然後，您可以在第二次呼叫 **BCryptEnumRegisteredProviders** 函式時，配置所需的記憶體，並將這個緩衝區指標的位址傳遞給 *ppBuffer* 參數。</span><span class="sxs-lookup"><span data-stu-id="ee06f-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="ee06f-119">下列範例示範如何使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式來配置和使用您自己的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee06f-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="ee06f-120">取得提供者註冊資訊</span><span class="sxs-lookup"><span data-stu-id="ee06f-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="ee06f-121">[**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration)函式可用來取得關於提供者的其他註冊特定資訊。</span><span class="sxs-lookup"><span data-stu-id="ee06f-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="ee06f-122">此函式會採用您要取得資訊的提供者名稱、所需的提供者模式 (核心模式、使用者模式或) ，以及提供者介面的識別碼，以取得的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="ee06f-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="ee06f-123">例如，若要取得「Microsoft 基本提供者」提供者之加密介面的使用者模式註冊資訊，您可以進行類似下面的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ee06f-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="ee06f-124">如同 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式， [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) 函數可以為您配置記憶體，您也可以自行配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee06f-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="ee06f-125">這兩個函式的處理常式相同。</span><span class="sxs-lookup"><span data-stu-id="ee06f-125">The process is the same for the two functions.</span></span>

 

 



