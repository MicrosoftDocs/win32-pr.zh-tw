---
title: 在 OnStatus 回呼中執行讀取器訊息
description: 在 OnStatus 回呼中執行讀取器訊息
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF) ，執行讀取器訊息
- ASF (Advanced Systems Format) ，執行讀取器訊息
- Advanced Systems Format (ASF) 、OnStatus 回呼
- ASF (Advanced Systems Format) 、OnStatus 回呼
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，執行讀取器訊息
- OnStatus 回呼方法，執行讀取器訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023030"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="7357a-111">在 OnStatus 回呼中執行讀取器訊息</span><span class="sxs-lookup"><span data-stu-id="7357a-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="7357a-112">若要使用非同步讀取器從 ASF 檔案傳遞內容，您必須至少執行兩個回呼方法： [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 和 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)。</span><span class="sxs-lookup"><span data-stu-id="7357a-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="7357a-113">本節說明如何執行 **IWMStatusCallback：： OnStatus** ，以接收和回應讀取器所傳送的狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="7357a-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="7357a-114">Windows Media 格式 SDK 中的其他物件會使用 **OnStatus** 。</span><span class="sxs-lookup"><span data-stu-id="7357a-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="7357a-115">如需 **OnStatus** 的一般資訊，請參閱 [使用 OnStatus 回呼](using-the-onstatus-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="7357a-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="7357a-116">使用非同步讀取器時，您必須在 **IWMStatusCallback：： OnStatus** 中將下列訊息設為陷阱。</span><span class="sxs-lookup"><span data-stu-id="7357a-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="7357a-117">狀態訊息</span><span class="sxs-lookup"><span data-stu-id="7357a-117">Status message</span></span> | <span data-ttu-id="7357a-118">Description</span><span class="sxs-lookup"><span data-stu-id="7357a-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="7357a-119">WMT \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="7357a-119">WMT\_OPENED</span></span>    | <span data-ttu-id="7357a-120">檔案開啟作業完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="7357a-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="7357a-121">WMT \_ 已關閉</span><span class="sxs-lookup"><span data-stu-id="7357a-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="7357a-122">在檔案關閉作業完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="7357a-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="7357a-123">您應該使用上列的狀態訊息來控制讀取應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="7357a-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="7357a-124">例如，您必須等到收到 **WMT \_ 開啟** 的訊息，才能啟動讀取器，或呼叫需要讀取器備妥檔案的其他方法。</span><span class="sxs-lookup"><span data-stu-id="7357a-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="7357a-125">通常，使用非同步讀取器建立的應用程式會使用事件來表示非同步呼叫完成，並繼續處理。</span><span class="sxs-lookup"><span data-stu-id="7357a-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="7357a-126">如需使用事件來通知作業完成的詳細資訊，請參閱 [使用事件與非同步呼叫](using-events-with-asynchronous-calls.md)。</span><span class="sxs-lookup"><span data-stu-id="7357a-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="7357a-127">讀取器物件會將許多其他訊息傳送至 **OnStatus** ，讓應用程式能夠回應讀取作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7357a-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="7357a-128">可能的狀態訊息值是在 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 列舉類型中定義。</span><span class="sxs-lookup"><span data-stu-id="7357a-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7357a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="7357a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7357a-130">**IWMStatusCallback：： OnStatus**</span><span class="sxs-lookup"><span data-stu-id="7357a-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="7357a-131">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="7357a-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="7357a-132">**使用 OnStatus 回呼**</span><span class="sxs-lookup"><span data-stu-id="7357a-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




