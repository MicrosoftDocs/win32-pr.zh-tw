---
title: 若要執行 OnSample 回呼
description: 若要執行 OnSample 回呼
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- 先進的系統格式 (ASF) ，實 OnStatus 回呼
- ASF (Advanced Systems Format) ，執行 OnStatus 回呼
- Advanced Systems Format (ASF) 、OnStatus 回呼
- ASF (Advanced Systems Format) 、OnStatus 回呼
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，執行 OnStatus 回呼
- OnStatus 回呼方法，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314514"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="a4bc8-111">若要執行 OnSample 回呼</span><span class="sxs-lookup"><span data-stu-id="a4bc8-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="a4bc8-112">非同步讀取器會呼叫 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 回呼方法，以展示時間順序提供範例給控制應用程式。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="a4bc8-113">當您使用非同步讀取器來建立應用程式時，您必須執行 **OnSample** 來處理未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="a4bc8-114">通常會從 **OnSample** 中呼叫為了轉譯內容而建立的函式或方法。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="a4bc8-115">**OnSample** 回呼的一般實作為包含下列步驟。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="a4bc8-116">藉由在傳遞為 *pSample* 的緩衝區上呼叫 [**INSSBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) ，以抓取包含範例的緩衝區位置和大小。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="a4bc8-117">根據輸出編號來分支您的邏輯。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="a4bc8-118">輸出編號會以 *dwOutputNumber* 的形式傳遞至 **OnSample** 。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="a4bc8-119">針對您想要支援的每個輸出編號，包含轉譯邏輯。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="a4bc8-120">如果您要從多個輸出呈現範例，您可能需要同步處理您的轉譯。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="a4bc8-121">從 ASF 檔案傳遞壓縮範例的應用程式需要執行 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼方法。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="a4bc8-122">**OnStreamSample** 函式幾乎與 **OnSample** 相同，不同之處在于它會依串流號碼接收壓縮的樣本，而不是依輸出編號來取得未壓縮的樣本。</span><span class="sxs-lookup"><span data-stu-id="a4bc8-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4bc8-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4bc8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4bc8-124">**IWMReaderCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="a4bc8-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="a4bc8-125">**IWMReaderCallbackAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="a4bc8-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="a4bc8-126">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="a4bc8-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="a4bc8-127">**使用回呼方法**</span><span class="sxs-lookup"><span data-stu-id="a4bc8-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




