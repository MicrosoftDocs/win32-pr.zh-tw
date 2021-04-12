---
description: 提供 ELS 服務的回呼
ms.assetid: 48609c55-9e82-4407-ae28-41b07b1e1161
title: 提供 ELS 服務的回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d22091f666649aab43c66f3d532f8e8f971d49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192109"
---
# <a name="providing-callbacks-for-els-services"></a><span data-ttu-id="fa7b9-103">提供 ELS 服務的回呼</span><span class="sxs-lookup"><span data-stu-id="fa7b9-103">Providing Callbacks for ELS Services</span></span>

<span data-ttu-id="fa7b9-104">如果您的應用程式使用非同步作業進行文字辨識，則必須提供回呼函式，讓 ELS 服務能夠使用。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-104">If your application is using asynchronous operations for text recognition, it must provide a callback function for the ELS service to use.</span></span> <span data-ttu-id="fa7b9-105">回呼函數是以 [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) 原型為基礎。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-105">The callback function is based on the [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) prototype.</span></span>

<span data-ttu-id="fa7b9-106">[要求文字](requesting-text-recognition.md)辨識主題描述您的應用程式如何向 ELS 服務要求非同步文字辨識。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-106">The [Requesting Text Recognition](requesting-text-recognition.md) topic describes how your application can request asynchronous text recognition from an ELS service.</span></span> <span data-ttu-id="fa7b9-107">下列範例顯示對 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)進行非同步呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-107">The following example shows an application that makes an asynchronous call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="fa7b9-108">文字辨識的回呼函數稱為 **RecognizeCallback**。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-108">The callback function for text recognition is called **RecognizeCallback**.</span></span> <span data-ttu-id="fa7b9-109">請注意，應用程式必須確保屬性包、輸入文字、選項和服務都有效，直到回呼函式完成執行為止。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-109">Note that the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback function has finished executing.</span></span> <span data-ttu-id="fa7b9-110">此外，應用程式必須確保在回呼函數取用包之後立即呼叫 [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) 。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-110">Additionally, the application must ensure that [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) is called immediately after the bag is consumed by the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="fa7b9-111">最好讓您的應用程式在完成處理或複製資源之後，使用回呼函式來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="fa7b9-111">It might be a good idea for your application to use the callback function to free the resources after it has finished processing or copying them.</span></span>

 


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
void RecognizeCallback(
     PMAPPING_PROPERTY_BAG pBag, 
     LPVOID data, DWORD dwDataSize, 
     HRESULT Result); 

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



## <a name="related-topics"></a><span data-ttu-id="fa7b9-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa7b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa7b9-113">使用擴充語言服務</span><span class="sxs-lookup"><span data-stu-id="fa7b9-113">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="fa7b9-114">要求文字辨識</span><span class="sxs-lookup"><span data-stu-id="fa7b9-114">Requesting Text Recognition</span></span>](requesting-text-recognition.md)
</dt> <dt>

[<span data-ttu-id="fa7b9-115">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="fa7b9-115">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)
</dt> <dt>

[<span data-ttu-id="fa7b9-116">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="fa7b9-116">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="fa7b9-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="fa7b9-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



