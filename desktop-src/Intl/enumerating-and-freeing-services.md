---
description: 列舉和釋放服務
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: 列舉和釋放服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6472851fbf5f7f84a499d2e9e04804279d397f31452d9617a8868e05cb8ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086608"
---
# <a name="enumerating-and-freeing-services"></a>列舉和釋放服務

ELS 應用程式會呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 函數來判斷作業系統上可用的服務。 函數可以用來列舉所有可用的 ELS 服務，或根據應用程式提供的搜尋準則來篩選服務。 當不再需要服務時，應用程式會呼叫 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)。

## <a name="get-all-supported-services"></a>取得所有支援的服務

此程式碼範例說明如何使用 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 和 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 來列舉和釋放作業系統上所有可用的服務。 若要這樣做，應用程式會針對 **MappingGetServices** 的 *POptions* 參數傳遞 **Null** 。


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a>取得特定服務

下一個範例說明如何使用 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 和 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 來列舉和釋放 "語言偵測" 類別的所有服務。 如需此服務類別的詳細資訊，請參閱 [**Microsoft 語言偵測**](microsoft-language-detection.md)。


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用擴充語言服務](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



