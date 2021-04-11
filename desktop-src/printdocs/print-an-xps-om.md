---
description: 說明如何將 XPS OM 以 XPS 檔的形式傳送至印表機。
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: 列印 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026926"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="5408b-103">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-103">Print an XPS OM</span></span>

<span data-ttu-id="5408b-104">說明如何將 XPS OM 以 XPS 檔的形式傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="5408b-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="5408b-105">如需有關如何列印包含完整 XPS 檔的 XPS OM 的指示，請參閱 [列印完整的 XPS om](#print-a-complete-xps-om)。</span><span class="sxs-lookup"><span data-stu-id="5408b-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="5408b-106">若要包含 XPS 檔，XPS OM 必須包含「 [建立空白的 XPS om](create-a-blank-xps-om.md)」中所列的專案。</span><span class="sxs-lookup"><span data-stu-id="5408b-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="5408b-107">如需有關如何列印一次建立或處理一頁的 XPS OM 的指示，請參閱以累加 [方式列印 XPS om](#incrementally-print-an-xps-om)。</span><span class="sxs-lookup"><span data-stu-id="5408b-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="5408b-108">在您的程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="5408b-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="5408b-109">在本主題中，您將瞭解如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="5408b-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="5408b-110">列印完整的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="5408b-111">以累加方式列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="5408b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="5408b-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="5408b-113">列印完整的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-113">Print a complete XPS OM</span></span>

<span data-ttu-id="5408b-114">當 XPS OM 包含完整的 XPS 檔時， [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream)方法可將 XPS OM 的內容傳送至印表機或列印佇列。</span><span class="sxs-lookup"><span data-stu-id="5408b-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="5408b-115">若要偵測列印工作是否已完成，請建立事件處理常式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="5408b-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="5408b-116">若要列印完整的 XPS OM：</span><span class="sxs-lookup"><span data-stu-id="5408b-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="5408b-117">藉由呼叫 [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)來建立新的列印工作資料流程。</span><span class="sxs-lookup"><span data-stu-id="5408b-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="5408b-118">藉由呼叫封裝的 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) 方法，將 XPS OM 的內容傳送至資料流程。</span><span class="sxs-lookup"><span data-stu-id="5408b-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="5408b-119">藉由呼叫資料流程的 **Close** 方法來關閉列印工作資料流程。</span><span class="sxs-lookup"><span data-stu-id="5408b-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="5408b-120">等候列印工作通知它已完成。</span><span class="sxs-lookup"><span data-stu-id="5408b-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="5408b-121">檢查完成狀態。</span><span class="sxs-lookup"><span data-stu-id="5408b-121">Check the completion status.</span></span>
6.  <span data-ttu-id="5408b-122">關閉並釋放資源。</span><span class="sxs-lookup"><span data-stu-id="5408b-122">Close and release resources.</span></span>


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



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="5408b-123">以累加方式列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="5408b-124">您可以藉由建立 XPS 列印工作串流，然後將個別檔元件一次傳遞給列印工作串流，以累加方式將 XPS OM 的檔元件傳送至印表機工作。</span><span class="sxs-lookup"><span data-stu-id="5408b-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="5408b-125">傳送檔元件的順序會決定它們在完成的檔中的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="5408b-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="5408b-126">因此，在程式可以呼叫此範例中的程式碼之前，它必須正確地組織檔元件。</span><span class="sxs-lookup"><span data-stu-id="5408b-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="5408b-127">使用 XPS OM 介面之前，請先初始化執行緒中的 COM，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5408b-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="5408b-128">若要監視列印工作的完成，請建立事件處理常式，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5408b-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


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



<span data-ttu-id="5408b-129">建立新的列印工作串流和新的封裝寫入器。</span><span class="sxs-lookup"><span data-stu-id="5408b-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="5408b-130">將每個檔元件以相同順序傳遞給對應的封裝寫入器方法，如同它們在完成的檔中所顯示的一樣。</span><span class="sxs-lookup"><span data-stu-id="5408b-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="5408b-131">開始新增每個檔，然後將頁面新增至其中。</span><span class="sxs-lookup"><span data-stu-id="5408b-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="5408b-132">將所有檔元件傳遞至列印工作串流之後，請關閉資料流程、等候列印工作完成，然後關閉並釋放開啟的資源。</span><span class="sxs-lookup"><span data-stu-id="5408b-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="5408b-133">藉由呼叫 [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)來建立新的列印工作資料流程。</span><span class="sxs-lookup"><span data-stu-id="5408b-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="5408b-134">建立 FixedDocumentSequence 元件的元件 URI。</span><span class="sxs-lookup"><span data-stu-id="5408b-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="5408b-135">在列印工作資料流程上建立新的封裝寫入器。</span><span class="sxs-lookup"><span data-stu-id="5408b-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="5408b-136">針對要寫入的每份檔：</span><span class="sxs-lookup"><span data-stu-id="5408b-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="5408b-137">建立 FixedDocument 元件的新元件 URI。</span><span class="sxs-lookup"><span data-stu-id="5408b-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="5408b-138">在封裝寫入器中啟動新檔。</span><span class="sxs-lookup"><span data-stu-id="5408b-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="5408b-139">針對目前檔中的每個頁面，建立 FixedPage 部分的元件 URI，並將頁面加入至封裝寫入器。</span><span class="sxs-lookup"><span data-stu-id="5408b-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="5408b-140">在所有頁面都加入至封裝寫入器之後，請將其關閉。</span><span class="sxs-lookup"><span data-stu-id="5408b-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="5408b-141">關閉列印工作資料流程。</span><span class="sxs-lookup"><span data-stu-id="5408b-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="5408b-142">等候列印工作完成。</span><span class="sxs-lookup"><span data-stu-id="5408b-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="5408b-143">檢查完成狀態。</span><span class="sxs-lookup"><span data-stu-id="5408b-143">Check the completion status.</span></span>
9.  <span data-ttu-id="5408b-144">關閉並釋放開啟的資源。</span><span class="sxs-lookup"><span data-stu-id="5408b-144">Close and release open resources.</span></span>


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



<span data-ttu-id="5408b-145">當程式以累加方式撰寫檔元件時（如這個範例所示），它必須針對它傳送至列印工作資料流程的每個檔元件產生元件名稱。</span><span class="sxs-lookup"><span data-stu-id="5408b-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="5408b-146">在上述範例中，FixedDocumentSequence 元件 URI 是從靜態字串建立的，因為 XPS 檔中只有一個這類元件。</span><span class="sxs-lookup"><span data-stu-id="5408b-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="5408b-147">每位 FixedPage 和 FixedDocument 元件的 URI 在 XPS 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5408b-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="5408b-148">使用這些元件的索引建立元件 URI 有助於確保產生的 URI 字串在 XPS 檔內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5408b-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


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



<span data-ttu-id="5408b-149">如需 XPS 檔結構的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。</span><span class="sxs-lookup"><span data-stu-id="5408b-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5408b-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="5408b-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5408b-151">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="5408b-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5408b-152">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="5408b-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="5408b-153">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="5408b-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="5408b-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="5408b-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="5408b-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="5408b-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="5408b-156">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="5408b-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="5408b-157">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="5408b-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="5408b-158">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="5408b-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="5408b-159">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="5408b-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="5408b-160">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="5408b-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="5408b-161">**StartXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="5408b-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="5408b-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="5408b-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="5408b-163">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="5408b-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5408b-164">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5408b-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="5408b-165">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="5408b-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="5408b-166">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5408b-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
