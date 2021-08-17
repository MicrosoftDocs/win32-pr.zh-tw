---
description: 說明如何將 XPS OM 以 XPS 檔的形式傳送至印表機。
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: 列印 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f1386352cff1556a5ce2403f34ebe4258c4110d4c3bf455990f3f1eb226d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470901"
---
# <a name="print-an-xps-om"></a>列印 XPS OM

說明如何將 XPS OM 以 XPS 檔的形式傳送至印表機。

如需有關如何列印包含完整 XPS 檔的 XPS OM 的指示，請參閱 [列印完整的 XPS om](#print-a-complete-xps-om)。 若要包含 XPS 檔，XPS OM 必須包含「 [建立空白的 XPS om](create-a-blank-xps-om.md)」中所列的專案。

如需有關如何列印一次建立或處理一頁的 XPS OM 的指示，請參閱以累加 [方式列印 XPS om](#incrementally-print-an-xps-om)。

在您的程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

在本主題中，您將瞭解如何執行下列工作：

-   [列印完整的 XPS OM](#print-a-complete-xps-om)
-   [以累加方式列印 XPS OM](#incrementally-print-an-xps-om)
-   [相關主題](#related-topics)

## <a name="print-a-complete-xps-om"></a>列印完整的 XPS OM

當 XPS OM 包含完整的 XPS 檔時， [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream)方法可將 XPS OM 的內容傳送至印表機或列印佇列。

若要偵測列印工作是否已完成，請建立事件處理常式，如下列範例所示。


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



若要列印完整的 XPS OM：

1.  藉由呼叫 [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)來建立新的列印工作資料流程。
2.  藉由呼叫封裝的 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) 方法，將 XPS OM 的內容傳送至資料流程。
3.  藉由呼叫資料流程的 **Close** 方法來關閉列印工作資料流程。
4.  等候列印工作通知它已完成。
5.  檢查完成狀態。
6.  關閉並釋放資源。


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a>以累加方式列印 XPS OM

您可以藉由建立 XPS 列印工作串流，然後將個別檔元件一次傳遞給列印工作串流，以累加方式將 XPS OM 的檔元件傳送至印表機工作。 傳送檔元件的順序會決定它們在完成的檔中的顯示方式。 因此，在程式可以呼叫此範例中的程式碼之前，它必須正確地組織檔元件。

使用 XPS OM 介面之前，請先初始化執行緒中的 COM，如下列範例程式碼所示。


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



若要監視列印工作的完成，請建立事件處理常式，如下列範例程式碼所示。


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



建立新的列印工作串流和新的封裝寫入器。 將每個檔元件以相同順序傳遞給對應的封裝寫入器方法，如同它們在完成的檔中所顯示的一樣。

開始新增每個檔，然後將頁面新增至其中。 將所有檔元件傳遞至列印工作串流之後，請關閉資料流程、等候列印工作完成，然後關閉並釋放開啟的資源。

1.  藉由呼叫 [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)來建立新的列印工作資料流程。
2.  建立 FixedDocumentSequence 元件的元件 URI。
3.  在列印工作資料流程上建立新的封裝寫入器。
4.  針對要寫入的每份檔：
    1.  建立 FixedDocument 元件的新元件 URI。
    2.  在封裝寫入器中啟動新檔。
    3.  針對目前檔中的每個頁面，建立 FixedPage 部分的元件 URI，並將頁面加入至封裝寫入器。
5.  在所有頁面都加入至封裝寫入器之後，請將其關閉。
6.  關閉列印工作資料流程。
7.  等候列印工作完成。
8.  檢查完成狀態。
9.  關閉並釋放開啟的資源。


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



當程式以累加方式撰寫檔元件時（如這個範例所示），它必須針對它傳送至列印工作資料流程的每個檔元件產生元件名稱。 在上述範例中，FixedDocumentSequence 元件 URI 是從靜態字串建立的，因為 XPS 檔中只有一個這類元件。 每位 FixedPage 和 FixedDocument 元件的 URI 在 XPS 檔中必須是唯一的。 使用這些元件的索引建立元件 URI 有助於確保產生的 URI 字串在 XPS 檔內是唯一的。


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



如需 XPS 檔結構的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[將 XPS OM 寫入 XPS 檔](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsPrintJob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**IXpsPrintJobStream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
