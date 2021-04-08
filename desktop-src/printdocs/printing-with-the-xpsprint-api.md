---
description: 本主題說明如何使用 XPS 列印 API 從 Windows 應用程式進行列印。
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 如何：使用 XPS 列印 API 進行列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851420"
---
# <a name="how-to-print-with-the-xps-print-api"></a>如何：使用 XPS 列印 API 進行列印

本主題說明如何使用 [XPS 列印 API](xpsprint-api.md) 從 Windows 應用程式進行列印。

[Xps 列印 API](xpsprint-api.md)可讓原生 Windows 應用程式列印 XPS 檔。 應用程式可以使用 [Xps 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))來建立 xps 檔。 [常見的 XPS 檔程式設計](/previous-versions/windows/desktop/dd316968(v=vs.85))工作說明主題會說明如何進行此作業。 一旦建立 XPS 檔之後，應用程式便可使用 XPS 列印 API 進行列印。

使用 [XPS 列印 API](xpsprint-api.md) 從應用程式列印檔案時，需要執行下列步驟。

-   [初始化 COM 介面](#initialize-com-interface)
-   [建立完成事件](#create-a-completion-event)
-   [啟動 XPS 列印工作](#start-an-xps-print-job)
-   [建立 IXpsOMPackageWriter 介面](#create-an-ixpsompackagewriter-interface)
-   [關閉 IXpsOMPackageWriter 介面](#close-the-ixpsompackagewriter-interface)
-   [關閉列印工作串流](#close-the-print-job-stream)
-   [等候完成事件](#wait-for-the-completion-event)
-   [釋放資源](#release-resources)

[Xps 列印 API](xpsprint-api.md)需要列印 xps 檔。 在下列範例中，xps 檔會在 XPS 列印 API 傳送至印表機時建立。 您也可以建立 XPS 檔，而不需要使用 [Xps 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85)) 將它傳送至印表機，並將其維護為 xps om 或將 xps om 儲存為 xps 檔。 如需有關使用 XPS OM 的詳細資訊，請參閱 XPS 檔 API。

### <a name="initialize-com-interface"></a>初始化 COM 介面

如果應用程式尚未執行，請將 COM 介面初始化。


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a>建立完成事件

建立完成事件，當列印多工緩衝處理器從應用程式收到整份檔時， [XPS 列印 API](xpsprint-api.md) 會使用此專案來通知應用程式。 XPS 列印 API 也支援進度事件，讓應用程式可以知道其他的離線處理活動。


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a>啟動 XPS 列印工作

藉由呼叫 [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob)來啟動 XPS 列印工作。 **StartXpsPrintJob** 會傳回資料流程，應用程式會在其中傳送要列印的檔。


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a>建立 IXpsOMPackageWriter 介面

在 [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob)傳回的資料流程上呼叫 [**IXpsOMObjectFactory：： CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) ，以建立 [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面。


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



針對此列印工作中的每個檔，啟動新檔，然後將頁面新增至該檔。

### <a name="start-a-new-document"></a>開始新檔

藉由呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)，在封裝寫入器中啟動新檔。 當呼叫這個方法時，如果檔是開啟的，則會關閉並開啟新檔。


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a>新增頁面

呼叫 [**IXpsOMPackageWriter：： AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) ，將檔的每個頁面從應用程式寫入封裝寫入器中的新檔。

> [!Note]  
> 應用程式會假設在這個步驟之前已建立頁面。 如需有關建立檔頁面以及將內容新增至其中的詳細資訊，請參閱 [一般 XPS 檔程式設計](/previous-versions/windows/desktop/dd316968(v=vs.85))工作。

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a>關閉 IXpsOMPackageWriter 介面

針對此列印工作撰寫所有檔之後，請呼叫 [**IXpsOMPackageWriter：： close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) 以關閉套件。


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a>關閉列印工作串流

藉由呼叫 [**close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close)來關閉列印工作串流，這會告知列印多工緩衝處理器，應用程式已傳送整個列印工作。


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a>等候完成事件

等候列印工作的完成事件。


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



通知完成事件之後，請呼叫 [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) 以取得作業狀態。


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a>釋放資源

作業狀態指出完成後，請釋放用於此列印工作的介面和資源。


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
