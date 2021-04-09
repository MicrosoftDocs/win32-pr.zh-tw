---
title: 使用自訂接收器
description: 使用自訂接收器
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF) 、自訂接收器
- ASF (Advanced Systems Format) ，自訂接收器
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收器，自訂接收器
- 自訂接收，關於
- 寫入器接收、自訂接收器
- 自訂接收，IWMWriterSink 介面
- IWMWriterSink
- 寫入器接收、IWMWriterSink 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681404"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="e6ec5-113">使用自訂接收器</span><span class="sxs-lookup"><span data-stu-id="e6ec5-113">Using Custom Sinks</span></span>

<span data-ttu-id="e6ec5-114">如果您有特殊的撰寫需求，可以建立自己的寫入器接收器。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="e6ec5-115">寫入器會藉由呼叫 [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)的方法，來與接收保持單向通訊。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="e6ec5-116">若要建立您自己的接收，請在應用程式的類別中執行 **IWMWriterSink** 介面。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="e6ec5-117">此程式非常類似于執行 Windows Media 格式 SDK 的物件所使用的任何其他回呼介面。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="e6ec5-118">如需回呼的詳細資訊，請參閱 [使用回呼方法](using-the-callback-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="e6ec5-119">[**IWMWriterSink：： OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader)中收到的緩衝區應寫入至檔案的開頭，而在 [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit)中接收的所有緩衝區都應依序寫出。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="e6ec5-120">**OnHeader** 會在一開始就呼叫，但可能也會在其他時間呼叫，如果可能的話，您應該覆寫原始的標頭。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="e6ec5-121">如果您的應用程式因某些原因而無法這麼做，請直接忽略後續的 **OnHeader** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="e6ec5-122">您的自訂接收應該呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法，以將其狀態傳達給您的寫入應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="e6ec5-123">如果您將接收器實作為 COM 物件，您可能會想要公開 [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="e6ec5-124">不過，您可以將 **OnStatus** 回呼的位址傳遞至接收器，並以任何您喜歡的方式設定內容。</span><span class="sxs-lookup"><span data-stu-id="e6ec5-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6ec5-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6ec5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ec5-126">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




