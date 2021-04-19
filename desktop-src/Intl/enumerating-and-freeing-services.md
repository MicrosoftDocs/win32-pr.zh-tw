---
description: 列舉和釋放服務
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: 列舉和釋放服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984682"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="a00ce-103">列舉和釋放服務</span><span class="sxs-lookup"><span data-stu-id="a00ce-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="a00ce-104">ELS 應用程式會呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 函數來判斷作業系統上可用的服務。</span><span class="sxs-lookup"><span data-stu-id="a00ce-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="a00ce-105">函數可以用來列舉所有可用的 ELS 服務，或根據應用程式提供的搜尋準則來篩選服務。</span><span class="sxs-lookup"><span data-stu-id="a00ce-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="a00ce-106">當不再需要服務時，應用程式會呼叫 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)。</span><span class="sxs-lookup"><span data-stu-id="a00ce-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="a00ce-107">取得所有支援的服務</span><span class="sxs-lookup"><span data-stu-id="a00ce-107">Get All Supported Services</span></span>

<span data-ttu-id="a00ce-108">此程式碼範例說明如何使用 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 和 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 來列舉和釋放作業系統上所有可用的服務。</span><span class="sxs-lookup"><span data-stu-id="a00ce-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="a00ce-109">若要這樣做，應用程式會針對 **MappingGetServices** 的 *POptions* 參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a00ce-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


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



## <a name="get-specific-services"></a><span data-ttu-id="a00ce-110">取得特定服務</span><span class="sxs-lookup"><span data-stu-id="a00ce-110">Get Specific Services</span></span>

<span data-ttu-id="a00ce-111">下一個範例說明如何使用 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) 和 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 來列舉和釋放 "語言偵測" 類別的所有服務。</span><span class="sxs-lookup"><span data-stu-id="a00ce-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="a00ce-112">如需此服務類別的詳細資訊，請參閱 [**Microsoft 語言偵測**](microsoft-language-detection.md)。</span><span class="sxs-lookup"><span data-stu-id="a00ce-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a00ce-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="a00ce-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00ce-114">使用擴充語言服務</span><span class="sxs-lookup"><span data-stu-id="a00ce-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="a00ce-115">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="a00ce-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="a00ce-116">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="a00ce-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



