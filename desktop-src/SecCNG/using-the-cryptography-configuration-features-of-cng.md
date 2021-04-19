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
# <a name="using-the-cryptography-configuration-features-of-cng"></a>使用 CNG 的密碼編譯設定功能

CNG API 提供的函式可列舉和取得已註冊之提供者的相關資訊。

-   [列舉提供者](#enumerating-providers)
-   [取得提供者註冊資訊](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>列舉提供者

您可以使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式來列舉已註冊的提供者。 您可以透過下列兩種方式之一來呼叫 **BCryptEnumRegisteredProviders** 函數：

1.  第一個是讓 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函數配置記憶體。 這可透過傳遞 *ppBuffer* 參數的 **Null** 指標位址來完成。 此程式碼會配置 [**CRYPT \_ 提供者**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) 結構和相關聯字串所需的記憶體。 以這種方式使用 **BCryptEnumRegisteredProviders** 函式時，您必須將 *PpBuffer* 傳遞給 [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) 函式，以釋放不再需要的記憶體。

    下列範例示範如何使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函數為您配置緩衝區。

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

    

2.  第二種方法是自行配置所需的記憶體。 這可透過針對 *ppBuffer* 參數呼叫 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders)函式（ **Null** ）來完成。 **BCryptEnumRegisteredProviders** 函式會放在 *pcbBuffer* 參數所指向的值，以及 [**CRYPT \_ 提供者**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers)結構和所有字串所需的大小（以位元組為單位）。 然後，您可以在第二次呼叫 **BCryptEnumRegisteredProviders** 函式時，配置所需的記憶體，並將這個緩衝區指標的位址傳遞給 *ppBuffer* 參數。

    下列範例示範如何使用 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式來配置和使用您自己的緩衝區。

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

    

## <a name="getting-provider-registration-information"></a>取得提供者註冊資訊

[**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration)函式可用來取得關於提供者的其他註冊特定資訊。 此函式會採用您要取得資訊的提供者名稱、所需的提供者模式 (核心模式、使用者模式或) ，以及提供者介面的識別碼，以取得的註冊資訊。 例如，若要取得「Microsoft 基本提供者」提供者之加密介面的使用者模式註冊資訊，您可以進行類似下面的呼叫。


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



如同 [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) 函式， [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) 函數可以為您配置記憶體，您也可以自行配置記憶體。 這兩個函式的處理常式相同。

 

 



