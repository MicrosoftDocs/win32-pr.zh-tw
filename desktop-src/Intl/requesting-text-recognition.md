---
description: 要求文字辨識
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: 要求文字辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970796"
---
# <a name="requesting-text-recognition"></a><span data-ttu-id="a3570-103">要求文字辨識</span><span class="sxs-lookup"><span data-stu-id="a3570-103">Requesting Text Recognition</span></span>

<span data-ttu-id="a3570-104">應用程式會呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 函式，以向特定的 ELS 服務要求文字辨識。</span><span class="sxs-lookup"><span data-stu-id="a3570-104">The application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to request text recognition from a specific ELS service.</span></span> <span data-ttu-id="a3570-105">在先前的 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)呼叫中，必須已探索到此服務，如 [**列舉和釋放服務**](enumerating-and-freeing-services.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="a3570-105">The service must have been discovered in a previous call to [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), as described in [**Enumerating and Freeing Services**](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3570-106">平臺可以同步或非同步方式處理 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3570-106">The platform can process [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) calls either synchronously or asynchronously.</span></span>

 

<span data-ttu-id="a3570-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 會處理下列類型的文字：</span><span class="sxs-lookup"><span data-stu-id="a3570-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) handles the following types of text:</span></span>

-   <span data-ttu-id="a3570-108">Microsoft 語言偵測。</span><span class="sxs-lookup"><span data-stu-id="a3570-108">Microsoft language detection.</span></span> <span data-ttu-id="a3570-109">UTF-16、正規化表單 C、用來決定語言的文字。</span><span class="sxs-lookup"><span data-stu-id="a3570-109">UTF-16, normalization form C, text for which to determine the language.</span></span>
-   <span data-ttu-id="a3570-110">Microsoft 腳本偵測。</span><span class="sxs-lookup"><span data-stu-id="a3570-110">Microsoft script detection.</span></span> <span data-ttu-id="a3570-111">要決定腳本範圍的 UTF-16 文字。</span><span class="sxs-lookup"><span data-stu-id="a3570-111">UTF-16 text for which to determine script ranges.</span></span>
-   <span data-ttu-id="a3570-112">音譯服務。</span><span class="sxs-lookup"><span data-stu-id="a3570-112">Transliteration services.</span></span> <span data-ttu-id="a3570-113">以來源腳本撰寫的 UTF-16 文字 (撰寫系統) 。</span><span class="sxs-lookup"><span data-stu-id="a3570-113">UTF-16 text written in source script (writing system).</span></span>

## <a name="use-synchronous-text-recognition"></a><span data-ttu-id="a3570-114">使用同步文字辨識</span><span class="sxs-lookup"><span data-stu-id="a3570-114">Use Synchronous Text Recognition</span></span>

<span data-ttu-id="a3570-115">本節提供數種方式來執行同步文字辨識的指示。</span><span class="sxs-lookup"><span data-stu-id="a3570-115">This section provides instructions for several ways to perform synchronous text recognition.</span></span>

<span data-ttu-id="a3570-116">**使用 Microsoft 語言偵測 Service 進行同步文字辨識**</span><span class="sxs-lookup"><span data-stu-id="a3570-116">**Synchronous Text Recognition with Microsoft Language Detection Service**</span></span>

<span data-ttu-id="a3570-117">下列範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 語言偵測服務，並列印服務所抓取的所有結果。</span><span class="sxs-lookup"><span data-stu-id="a3570-117">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Language Detection service, and prints all the results retrieved by the service.</span></span> <span data-ttu-id="a3570-118">這項服務的輸出格式是單一 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構，其 **.pdata** 成員指向 Unicode 雙 null 結束、登錄格式的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="a3570-118">The output format of this service is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to a Unicode double-null-terminated, registry-formatted array of strings.</span></span> <span data-ttu-id="a3570-119">陣列的每個字串都是以 null 終止，且會使用空字串來指定陣列的結尾。</span><span class="sxs-lookup"><span data-stu-id="a3570-119">Every string of the array is null-terminated and an empty string is used to specify the end of the array.</span></span> <span data-ttu-id="a3570-120">陣列的內容是依信心排序的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="a3570-120">The contents of the array are language names sorted by confidence.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



<span data-ttu-id="a3570-121">**使用 Microsoft 腳本偵測服務進行同步文字辨識**</span><span class="sxs-lookup"><span data-stu-id="a3570-121">**Synchronous Text Recognition with Microsoft Script Detection Service**</span></span>

<span data-ttu-id="a3570-122">下一個範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 腳本偵測服務，並列印所有已取出的結果。</span><span class="sxs-lookup"><span data-stu-id="a3570-122">The next example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Script Detection service, and prints all the retrieved results.</span></span> <span data-ttu-id="a3570-123">這項服務的輸出格式是 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構的陣列，每個都指定在相同腳本中撰寫的文字。</span><span class="sxs-lookup"><span data-stu-id="a3570-123">The output format of this service is an array of [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structures, each specifying text written in the same script.</span></span> <span data-ttu-id="a3570-124">Common (Zyyy) 字元會加入至先前的範圍，如果前一個範圍不存在，則為下一個範圍。</span><span class="sxs-lookup"><span data-stu-id="a3570-124">Common (Zyyy) characters are added to the previous range, or to the next range if the previous range does not exist.</span></span> <span data-ttu-id="a3570-125">每個結構的 **.pdata** 成員會指向 Unicode 以 null 終止的字串，其中包含特定範圍之腳本的標準 Unicode 名稱。</span><span class="sxs-lookup"><span data-stu-id="a3570-125">The **pData** member of each structure points to a Unicode null-terminated string containing the standard Unicode name of the script for the particular range.</span></span>

> [!Note]  
> <span data-ttu-id="a3570-126">從 Windows 7 開始，Microsoft 腳本偵測服務符合 Unicode 5.1。</span><span class="sxs-lookup"><span data-stu-id="a3570-126">As of Windows 7, the Microsoft Script Detection service complies with Unicode 5.1.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



<span data-ttu-id="a3570-127">**使用 Microsoft 斯拉夫的同步文字辨識至拉丁音譯服務**</span><span class="sxs-lookup"><span data-stu-id="a3570-127">**Synchronous Text Recognition with Microsoft Cyrillic to Latin Transliteration Service**</span></span>

<span data-ttu-id="a3570-128">下列範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 斯拉夫至拉丁音譯服務，並列印已取出的結果。</span><span class="sxs-lookup"><span data-stu-id="a3570-128">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Cyrillic to Latin transliteration service, and prints the retrieved results.</span></span> <span data-ttu-id="a3570-129">請注意以 GUID 或依類別和輸入腳本列舉這項服務的兩種不同方式。</span><span class="sxs-lookup"><span data-stu-id="a3570-129">Note the two different ways to enumerate this service, either by GUID or by category and input script.</span></span>

<span data-ttu-id="a3570-130">所有可用的音譯服務的輸出格式都相同。</span><span class="sxs-lookup"><span data-stu-id="a3570-130">The output format is the same for all available transliteration services.</span></span> <span data-ttu-id="a3570-131">它是單一 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構，其 **.pdata** 成員指向 Unicode 字元陣列，這些字元表示藉由只套用特定音譯服務的規則來轉譯成輸出腳本的原始文字。</span><span class="sxs-lookup"><span data-stu-id="a3570-131">It is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to an array of Unicode characters representing the original text transliterated into the output script by applying only the rules of the specific transliteration service.</span></span> <span data-ttu-id="a3570-132">如果輸入不包含終止的 null 字元，則此服務不會以 null 結束其輸出。</span><span class="sxs-lookup"><span data-stu-id="a3570-132">This service does not null-terminate its output if the input does not contain the terminating null character.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



<span data-ttu-id="a3570-133">**透過呼叫所有可用服務的同步文字辨識**</span><span class="sxs-lookup"><span data-stu-id="a3570-133">**Synchronous Text Recognition with a Call to All Available Services**</span></span>

<span data-ttu-id="a3570-134">下列範例示範如何使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 搭配所有可用的服務，並列印所有服務的已抓取結果。</span><span class="sxs-lookup"><span data-stu-id="a3570-134">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with all available services, and prints the retrieved results for all the services.</span></span> <span data-ttu-id="a3570-135">此範例提供每項服務作業的良好說明。</span><span class="sxs-lookup"><span data-stu-id="a3570-135">This example provides a good illustration of the operation of each service.</span></span> <span data-ttu-id="a3570-136">藉由查看範例應用程式的輸出，很容易就能找出服務內部發生的狀況。</span><span class="sxs-lookup"><span data-stu-id="a3570-136">By looking at the output of the example application, it is easy to find out what is happening internally with the services.</span></span> <span data-ttu-id="a3570-137">此範例也會顯示幾乎所有用來呼叫任何 ELS 服務的程式碼都相同。</span><span class="sxs-lookup"><span data-stu-id="a3570-137">This example also shows that almost all code used to call any of the ELS services is the same.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a><span data-ttu-id="a3570-138">使用非同步文字辨識</span><span class="sxs-lookup"><span data-stu-id="a3570-138">Use Asynchronous Text Recognition</span></span>

<span data-ttu-id="a3570-139">下列範例示範如何使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 進行非同步文字辨識。</span><span class="sxs-lookup"><span data-stu-id="a3570-139">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) for asynchronous text recognition.</span></span> <span data-ttu-id="a3570-140">使用回呼時，應用程式必須確保屬性包、輸入文字、選項和服務都有效，直到回呼完成執行為止。</span><span class="sxs-lookup"><span data-stu-id="a3570-140">When the callback is used, the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback has finished executing.</span></span>

<span data-ttu-id="a3570-141">當回呼函式取用包之後，應用程式必須立即呼叫 [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) 。</span><span class="sxs-lookup"><span data-stu-id="a3570-141">The application must call [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immediately after the bag is consumed by the callback function.</span></span> <span data-ttu-id="a3570-142">如需詳細資訊，請參閱 [提供 ELS 服務的回呼](providing-callbacks-for-els-services.md)。</span><span class="sxs-lookup"><span data-stu-id="a3570-142">For more information, see [Providing Callbacks for ELS Services](providing-callbacks-for-els-services.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="a3570-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3570-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3570-144">使用擴充語言服務</span><span class="sxs-lookup"><span data-stu-id="a3570-144">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="a3570-145">提供 ELS 服務的回呼</span><span class="sxs-lookup"><span data-stu-id="a3570-145">Providing Callbacks for ELS Services</span></span>](providing-callbacks-for-els-services.md)
</dt> <dt>

[<span data-ttu-id="a3570-146">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="a3570-146">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="a3570-147">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="a3570-147">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[<span data-ttu-id="a3570-148">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="a3570-148">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



