---
description: 要求文字辨識
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: 要求文字辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8efd4fe8b2f37c134480aa1b057705af8826bbf7490b1dc4d40fb5a2755b043
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147050"
---
# <a name="requesting-text-recognition"></a>要求文字辨識

應用程式會呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 函式，以向特定的 ELS 服務要求文字辨識。 在先前的 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)呼叫中，必須已探索到此服務，如 [**列舉和釋放服務**](enumerating-and-freeing-services.md)中所述。

> [!Note]  
> 平臺可以同步或非同步方式處理 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 呼叫。

 

[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 會處理下列類型的文字：

-   Microsoft 語言偵測。 UTF-16、正規化表單 C、用來決定語言的文字。
-   Microsoft 腳本偵測。 要決定腳本範圍的 UTF-16 文字。
-   音譯服務。 以來源腳本撰寫的 UTF-16 文字 (撰寫系統) 。

## <a name="use-synchronous-text-recognition"></a>使用同步文字辨識

本節提供數種方式來執行同步文字辨識的指示。

**使用 Microsoft 語言偵測 Service 進行同步文字辨識**

下列範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 語言偵測服務，並列印服務所抓取的所有結果。 這項服務的輸出格式是單一 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構，其 **.pdata** 成員指向 Unicode 雙 null 結束、登錄格式的字串陣列。 陣列的每個字串都是以 null 終止，且會使用空字串來指定陣列的結尾。 陣列的內容是依信心排序的語言名稱。


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



**使用 Microsoft 腳本偵測服務進行同步文字辨識**

下一個範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 腳本偵測服務，並列印所有已取出的結果。 這項服務的輸出格式是 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構的陣列，每個都指定在相同腳本中撰寫的文字。 Common (Zyyy) 字元會加入至先前的範圍，如果前一個範圍不存在，則為下一個範圍。 每個結構的 **.pdata** 成員會指向 Unicode 以 null 終止的字串，其中包含特定範圍之腳本的標準 Unicode 名稱。

> [!Note]  
> 從 Windows 7 開始，Microsoft 腳本偵測服務符合 Unicode 5.1。

 


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



**使用 Microsoft 斯拉夫的同步文字辨識至拉丁音譯服務**

下列範例說明如何搭配使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 與 Microsoft 斯拉夫至拉丁音譯服務，並列印已取出的結果。 請注意以 GUID 或依類別和輸入腳本列舉這項服務的兩種不同方式。

所有可用的音譯服務的輸出格式都相同。 它是單一 [**對應 \_ 資料 \_ 範圍**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) 結構，其 **.pdata** 成員指向 Unicode 字元陣列，這些字元表示藉由只套用特定音譯服務的規則來轉譯成輸出腳本的原始文字。 如果輸入不包含終止的 null 字元，則此服務不會以 null 結束其輸出。


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



**透過呼叫所有可用服務的同步文字辨識**

下列範例示範如何使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 搭配所有可用的服務，並列印所有服務的已抓取結果。 此範例提供每項服務作業的良好說明。 藉由查看範例應用程式的輸出，很容易就能找出服務內部發生的狀況。 此範例也會顯示幾乎所有用來呼叫任何 ELS 服務的程式碼都相同。


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



## <a name="use-asynchronous-text-recognition"></a>使用非同步文字辨識

下列範例示範如何使用 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 進行非同步文字辨識。 使用回呼時，應用程式必須確保屬性包、輸入文字、選項和服務都有效，直到回呼完成執行為止。

當回呼函式取用包之後，應用程式必須立即呼叫 [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) 。 如需詳細資訊，請參閱 [提供 ELS 服務的回呼](providing-callbacks-for-els-services.md)。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用擴充語言服務](using-extended-linguistic-services.md)
</dt> <dt>

[提供 ELS 服務的回呼](providing-callbacks-for-els-services.md)
</dt> <dt>

[**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



