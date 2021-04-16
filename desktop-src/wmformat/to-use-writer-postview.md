---
title: 使用寫入器 Postview
description: 使用寫入器 Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF) 、writer postview
- ASF (Advanced Systems Format) 、writer postview
- Advanced Systems Format (ASF) ，postviewing
- ASF (Advanced Systems Format) ，postviewing
- 寫入器 postview
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104507836"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="6d81a-109">使用寫入器 Postview</span><span class="sxs-lookup"><span data-stu-id="6d81a-109">To Use Writer Postview</span></span>

<span data-ttu-id="6d81a-110">寫入器物件提供 postviewing 功能，讓您可以驗證撰寫的內容，而不需要設定 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="6d81a-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="6d81a-111">寫入器物件不支援音訊內容的 postviewing。</span><span class="sxs-lookup"><span data-stu-id="6d81a-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="6d81a-112">寫入器 postviewer 的運作方式與非同步讀取器物件的方式大致相同，只是使用較少的功能。</span><span class="sxs-lookup"><span data-stu-id="6d81a-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="6d81a-113">如需有關讀取數位媒體的詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="6d81a-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="6d81a-114">若要執行 postviewer，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6d81a-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="6d81a-115">執行 [**IWMWriterPostViewCallback：： OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) 回呼。</span><span class="sxs-lookup"><span data-stu-id="6d81a-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="6d81a-116">這個方法基本上與 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 相同，不同之處在于它會指定資料流程號碼，而不是輸出。</span><span class="sxs-lookup"><span data-stu-id="6d81a-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="6d81a-117">設定為正常寫入。</span><span class="sxs-lookup"><span data-stu-id="6d81a-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="6d81a-118">藉由呼叫 **IWMWriter：： QueryInterface**，取得寫入器物件之 [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6d81a-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="6d81a-119">藉由呼叫 [**IWMWriterPostView：： SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)，設定要使用之 postviewer 的回呼。</span><span class="sxs-lookup"><span data-stu-id="6d81a-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="6d81a-120">針對您想要接收 postview 範例的每個資料流程，呼叫 [**IWMWriterPostView：： SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples)。</span><span class="sxs-lookup"><span data-stu-id="6d81a-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="6d81a-121">您可以藉由呼叫 [**IWMWriterPostView：： GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)，查看資料流程是否已設定為接收 postview 範例。</span><span class="sxs-lookup"><span data-stu-id="6d81a-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="6d81a-122">您可以操作範例格式，就像是讀取器物件或同步讀取器物件中的輸出格式一樣。</span><span class="sxs-lookup"><span data-stu-id="6d81a-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="6d81a-123">當您開始寫入檔案時，您將開始在 **OnPostViewSample** 回呼方法的執行中收到範例。</span><span class="sxs-lookup"><span data-stu-id="6d81a-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d81a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d81a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d81a-125">**IWMWriterPostViewCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="6d81a-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="6d81a-126">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="6d81a-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




