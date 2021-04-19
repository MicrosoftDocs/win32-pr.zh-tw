---
title: 為 ASF 檔案編制索引
description: 為 ASF 檔案編制索引
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK，為 ASF 檔案編制索引
- Advanced Systems Format (ASF) 、編制檔案索引
- ASF (Advanced 系統格式) 、編制檔案索引
- 索引，為 ASF 檔案編制索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966021"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="13cd5-107">為 ASF 檔案編制索引</span><span class="sxs-lookup"><span data-stu-id="13cd5-107">To Index an ASF File</span></span>

<span data-ttu-id="13cd5-108">為 ASF 檔案編制索引的程式非常簡單。</span><span class="sxs-lookup"><span data-stu-id="13cd5-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="13cd5-109">呼叫 [**IWMIndexer：： StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) 並傳遞檔案名。</span><span class="sxs-lookup"><span data-stu-id="13cd5-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="13cd5-110">索引子會執行其餘工作。</span><span class="sxs-lookup"><span data-stu-id="13cd5-110">The indexer does the rest.</span></span> <span data-ttu-id="13cd5-111">對 **StartIndexing** 的呼叫是非同步，因此必須使用 **OnStatus** 回呼來監視狀態。</span><span class="sxs-lookup"><span data-stu-id="13cd5-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="13cd5-112">下列程式碼說明如何編制 ASF 檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="13cd5-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="13cd5-113">如果您想要在為檔案編制索引之前設定索引子，您必須包含包含在中的範例程式碼， [以設定索引子](to-configure-the-indexer.md)。</span><span class="sxs-lookup"><span data-stu-id="13cd5-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="13cd5-114">在此範例中，指向事件的控制碼必須建立為全域變數，才能讓回呼存取它。</span><span class="sxs-lookup"><span data-stu-id="13cd5-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="13cd5-115">下列宣告應該會出現在全域範圍中。</span><span class="sxs-lookup"><span data-stu-id="13cd5-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="13cd5-116">在更實際的案例中，事件控制碼應該是類別的資料成員，其中包含回呼和啟動索引子的邏輯。</span><span class="sxs-lookup"><span data-stu-id="13cd5-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="13cd5-117">在呼叫 **IWMIndexer：： StartIndexing** 之後，索引子會將數個事件傳送至 **OnStatus** 回呼。</span><span class="sxs-lookup"><span data-stu-id="13cd5-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="13cd5-118">您可以視需要為您的應用程式加以攔截。</span><span class="sxs-lookup"><span data-stu-id="13cd5-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="13cd5-119">您至少需要在索引完成時，將 WMT 設為 [ \_ 已關閉]。</span><span class="sxs-lookup"><span data-stu-id="13cd5-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="13cd5-120">在 **OnStatus** 回呼的執行中，于訊息切換內使用下列邏輯。</span><span class="sxs-lookup"><span data-stu-id="13cd5-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="13cd5-121">在這個範例中，假設您是透過名為 MyCallback 的物件來存取 **OnStatus** 回呼的實作為。</span><span class="sxs-lookup"><span data-stu-id="13cd5-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="13cd5-122">如需有關搭配此 SDK 使用事件和回呼的詳細資訊，請參閱 [使用回呼方法](using-the-callback-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="13cd5-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="13cd5-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="13cd5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cd5-124">**IWMIndexer 介面**</span><span class="sxs-lookup"><span data-stu-id="13cd5-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="13cd5-125">**設定索引子**</span><span class="sxs-lookup"><span data-stu-id="13cd5-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="13cd5-126">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="13cd5-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="13cd5-127">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="13cd5-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




