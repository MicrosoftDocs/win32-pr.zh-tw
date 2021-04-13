---
title: 將接收器新增至寫入器
description: 將接收器新增至寫入器
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF) ，將接收器新增至寫入器
- ASF (Advanced Systems Format) ，將接收器新增至寫入器
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- Advanced Systems Format (ASF) 、寫入器接收
- ASF (Advanced 系統格式) 、寫入器接收
- 接收，加入寫入器
- 寫入器接收，加入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374466"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="0a4ac-111">將接收器新增至寫入器</span><span class="sxs-lookup"><span data-stu-id="0a4ac-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="0a4ac-112">寫入器接收是與寫入器不同的物件，而且必須加入至要使用的寫入器。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="0a4ac-113">如果您要寫入檔案，您可以直接呼叫 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)，這會自動設定 file sink。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="0a4ac-114">否則，若要將接收新增至寫入器，請呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) 方法。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="0a4ac-115">**AddSink** 需要接收器的 [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="0a4ac-116">當您完成使用接收時，您應該呼叫適當的方法來關閉它，視接收的類型而定，然後呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink)將它從寫入器中移除。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="0a4ac-117">下列範例程式碼示範如何建立寫入器檔案接收，並將其新增至寫入器。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="0a4ac-118">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="0a4ac-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="0a4ac-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a4ac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ac-120">**從接收取得錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="0a4ac-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="0a4ac-121">**IWMWriterAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="0a4ac-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="0a4ac-122">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="0a4ac-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




