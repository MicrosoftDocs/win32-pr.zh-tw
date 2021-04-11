---
title: 索引子物件
description: 索引子物件
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK，索引子物件
- Advanced Systems Format (ASF) 、索引子物件
- ASF (Advanced 系統格式) 、索引子物件
- 物件、索引子物件
- 索引子物件
- 索引，索引子物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104023153"
---
# <a name="indexer-object"></a><span data-ttu-id="a2a87-109">索引子物件</span><span class="sxs-lookup"><span data-stu-id="a2a87-109">Indexer Object</span></span>

<span data-ttu-id="a2a87-110">索引子物件會在 ASF 檔案中建立索引。</span><span class="sxs-lookup"><span data-stu-id="a2a87-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="a2a87-111">索引是一種 ASF 檔案的標準部分，其等同于具有時間、框架數位或 (的影片樣本（如果適用) 的運動圖片和電視工程師 (SMPTE) 標準時間戳）。</span><span class="sxs-lookup"><span data-stu-id="a2a87-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="a2a87-112">如果沒有索引，讀取器物件和同步讀取器物件都無法搜尋檔案中間的某個點。</span><span class="sxs-lookup"><span data-stu-id="a2a87-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="a2a87-113">只有當檔案包含一或多個影片資料流程時，才需要這個物件所建立的索引。</span><span class="sxs-lookup"><span data-stu-id="a2a87-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="a2a87-114">這是因為音訊資料未暫時壓縮，因此可讓您輕鬆地在音訊串流中尋找指定的時間。</span><span class="sxs-lookup"><span data-stu-id="a2a87-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="a2a87-115">索引子物件是由 [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) 函式所建立，它會將指標設定為 **IWMIndexer** 介面。</span><span class="sxs-lookup"><span data-stu-id="a2a87-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="a2a87-116">您可以藉由呼叫 **QueryInterface** 方法來取得索引子物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="a2a87-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="a2a87-117">下列是索引子物件支援的介面。</span><span class="sxs-lookup"><span data-stu-id="a2a87-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="a2a87-118">介面</span><span class="sxs-lookup"><span data-stu-id="a2a87-118">Interface</span></span>                          | <span data-ttu-id="a2a87-119">描述</span><span class="sxs-lookup"><span data-stu-id="a2a87-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2a87-120">**IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="a2a87-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="a2a87-121">啟動和停止編制索引程式。</span><span class="sxs-lookup"><span data-stu-id="a2a87-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="a2a87-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="a2a87-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="a2a87-123">設定索引子，依框架、時間或 SMPTE 時間程式碼啟用索引編制。</span><span class="sxs-lookup"><span data-stu-id="a2a87-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="a2a87-124">下列回呼介面必須由應用程式執行，才能使用索引子物件。</span><span class="sxs-lookup"><span data-stu-id="a2a87-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="a2a87-125">介面</span><span class="sxs-lookup"><span data-stu-id="a2a87-125">Interface</span></span>                                      | <span data-ttu-id="a2a87-126">描述</span><span class="sxs-lookup"><span data-stu-id="a2a87-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a2a87-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="a2a87-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="a2a87-128">接收在個別執行緒中執行之進程的狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="a2a87-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a2a87-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2a87-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a87-130">**物件**</span><span class="sxs-lookup"><span data-stu-id="a2a87-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="a2a87-131">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="a2a87-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




