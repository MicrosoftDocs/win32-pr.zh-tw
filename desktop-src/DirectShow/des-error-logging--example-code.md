---
description: DES 錯誤記錄：範例程式碼
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: DES 錯誤記錄：範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510356"
---
# <a name="des-error-logging-example-code"></a><span data-ttu-id="a33ec-103">DES 錯誤記錄：範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a33ec-103">DES Error Logging: Example Code</span></span>

<span data-ttu-id="a33ec-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a33ec-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a33ec-105">下列範例程式碼顯示完整的主控台應用程式，該應用程式會使用本節所述的錯誤記錄類別來載入和預覽 [DirectShow 編輯服務](directshow-editing-services.md) XML 專案檔。</span><span class="sxs-lookup"><span data-stu-id="a33ec-105">The following sample code presents a complete console application that loads and previews a [DirectShow Editing Services](directshow-editing-services.md) XML project file, using the error logging class described in this section.</span></span> <span data-ttu-id="a33ec-106"> (查看 [記錄錯誤](logging-errors.md)。 ) 專案檔的名稱已硬式編碼到應用程式中。</span><span class="sxs-lookup"><span data-stu-id="a33ec-106">(See [Logging Errors](logging-errors.md).) The name of the project file is hard-coded into the application.</span></span>

<span data-ttu-id="a33ec-107">為了讓程式碼變得更短，主控台應用程式會使用 ATL 智慧型指標，而不需要呼叫 **QueryInterface** 和 **釋放**。</span><span class="sxs-lookup"><span data-stu-id="a33ec-107">To make the code shorter, the console application uses ATL smart pointers, which removes the need to call **QueryInterface** and **Release**.</span></span> <span data-ttu-id="a33ec-108">如果您想要的話，可以在 [載入和預覽專案](loading-and-previewing-a-project.md)時修改範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="a33ec-108">If you prefer, you can modify the sample application in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span> <span data-ttu-id="a33ec-109">只要新增上一節所示的程式碼即可。</span><span class="sxs-lookup"><span data-stu-id="a33ec-109">Simply add the code shown in the previous section.</span></span>


```C++
#include <atlbase.h>
#include <dshow.h>
#include <qedit.h>
#include <stdio.h>

// Declare error logging class.
class CErrReporter;

// (The implementation of CErrReporter was given previously.)

void __cdecl main(void)
{
    HRESULT hr = CoInitialize(NULL);

    if (FAILED(hr))
    {
        // Error handling is omitted for clarity.
    }

    { // Scope for smart pointers.

    CComPtr<IAMTimeline>   pTL;
    CComPtr<IRenderEngine> pRenderEngine; 
    CComPtr<IXml2Dex>      pXML; 
    CComPtr<IGraphBuilder> pGraph;

    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**) &pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**) &pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**) &pRenderEngine);

    // Set the error log.
    CComQIPtr<IAMSetErrorLog, &IID_IAMSetErrorLog> pSetLog(pTL);
    if (pSetLog)
    {
        IAMErrorLog *pLog = new CErrReporter;    
        pSetLog->put_ErrorLog(pLog);
    }
   
    // Load and preview the project.
    CComBSTR bstrFile(OLESTR("C:\\example.xtl"));
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    if (SUCCEEDED(hr))
    {
        hr = pRenderEngine->SetTimelineObject(pTL);
        hr = pRenderEngine->ConnectFrontEnd( );
        hr = pRenderEngine->RenderOutputPins( );
        hr = pRenderEngine->GetFilterGraph(&pGraph);

        CComQIPtr<IMediaControl, &IID_IMediaControl> pControl(pGraph);
        CComQIPtr<IMediaEvent, &IID_IMediaEvent> pEvent(pGraph);
        pControl->Run();

        long evCode;
        hr = pEvent->WaitForCompletion(INFINITE, &evCode);
        pControl->Stop();
    }
    // Clean up.
    pRenderEngine->ScrapIt();
    }
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="a33ec-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a33ec-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a33ec-111">記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="a33ec-111">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



