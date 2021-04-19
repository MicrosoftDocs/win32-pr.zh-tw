---
description: 將新功能安裝至記憶體可以改善效能。 CryptoAPI 函式會在搜尋 DLL 的登錄之前搜尋功能的記憶體。 安裝此功能之前必須先載入 DLL。
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: 安裝新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978140"
---
# <a name="installing-the-new-functionality"></a><span data-ttu-id="ba66d-105">安裝新功能</span><span class="sxs-lookup"><span data-stu-id="ba66d-105">Installing the New Functionality</span></span>

<span data-ttu-id="ba66d-106">將新功能安裝至記憶體可以改善效能。</span><span class="sxs-lookup"><span data-stu-id="ba66d-106">Installing new functionality into memory can improve performance.</span></span> <span data-ttu-id="ba66d-107">[*CryptoAPI*](../secgloss/c-gly.md) 函式會在搜尋 DLL 的登錄之前搜尋功能的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ba66d-107">[*CryptoAPI*](../secgloss/c-gly.md) functions search memory for the functionality before searching the registry for the DLL.</span></span> <span data-ttu-id="ba66d-108">安裝此功能之前必須先載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="ba66d-108">The DLL must be loaded before installing the functionality.</span></span>

<span data-ttu-id="ba66d-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) 會安裝新功能的位址。</span><span class="sxs-lookup"><span data-stu-id="ba66d-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installs the address of the new functionality.</span></span> <span data-ttu-id="ba66d-110">它應該放在 DLL 的 **DllMain** 函數中。</span><span class="sxs-lookup"><span data-stu-id="ba66d-110">It should be placed in the **DllMain** function of the DLL.</span></span>

<span data-ttu-id="ba66d-111">如果 *hModule* 傳遞至 [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)，在安裝之後，就不會卸載 DLL，直到卸載 Crypt32.dll 為止。</span><span class="sxs-lookup"><span data-stu-id="ba66d-111">If *hModule* is passed to [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), once installed, the DLL is not unloaded until the Crypt32.dll is unloaded.</span></span>

<span data-ttu-id="ba66d-112">下列範例會呼叫 [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) 函數。</span><span class="sxs-lookup"><span data-stu-id="ba66d-112">The following example calls the [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
