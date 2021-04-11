---
title: 從接收取得錯誤訊息
description: 從接收取得錯誤訊息
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Advanced Systems Format (ASF) 、接收的錯誤訊息
- ASF (Advanced 系統格式) 、接收的錯誤訊息
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，錯誤訊息
- 錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092544"
---
# <a name="getting-error-messages-from-a-sink"></a><span data-ttu-id="f9643-109">從接收取得錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f9643-109">Getting Error Messages from a Sink</span></span>

<span data-ttu-id="f9643-110">寫入器物件不會將訊息傳送至 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法。</span><span class="sxs-lookup"><span data-stu-id="f9643-110">The writer object does not send messages to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="f9643-111">不過，您可以設定寫入器接收，以將訊息傳送至 OnStatus。</span><span class="sxs-lookup"><span data-stu-id="f9643-111">However, you can set writer sinks to send messages to OnStatus.</span></span> <span data-ttu-id="f9643-112">每個接收都必須設定為個別傳遞狀態，但所有接收都可以報告給相同的回呼。</span><span class="sxs-lookup"><span data-stu-id="f9643-112">Each sink must be set to deliver status separately, but all sinks can report to the same callback.</span></span>

<span data-ttu-id="f9643-113">若要設定接收以將狀態訊息傳遞給 **OnStatus**，請呼叫 [**IWMRegisterCallback：： Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) 方法。</span><span class="sxs-lookup"><span data-stu-id="f9643-113">To set a sink to deliver status messages to **OnStatus**, call the [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) method.</span></span>

<span data-ttu-id="f9643-114">下列範例程式碼示範如何設定所有接收器，以將狀態訊息傳遞給 **OnStatus** 回呼。</span><span class="sxs-lookup"><span data-stu-id="f9643-114">The following example code demonstrates how to set all of the sinks to deliver status messages to an **OnStatus** callback.</span></span> <span data-ttu-id="f9643-115">在此範例中，會使用每個接收的索引做為內容參數，讓 **OnStatus** 方法可以區分不同接收的訊息。</span><span class="sxs-lookup"><span data-stu-id="f9643-115">In this example, the index of each sink will be used as the context parameter so that the **OnStatus** method can differentiate between messages from the different sinks.</span></span> <span data-ttu-id="f9643-116">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="f9643-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="f9643-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9643-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9643-118">**IWMRegisterCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="f9643-118">**IWMRegisterCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[<span data-ttu-id="f9643-119">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="f9643-119">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




