---
description: 本主題說明 (MFTs) 之媒體基礎轉換的非同步資料處理。
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: 非同步 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972362"
---
# <a name="asynchronous-mfts"></a><span data-ttu-id="448ae-103">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="448ae-103">Asynchronous MFTs</span></span>

<span data-ttu-id="448ae-104">本主題說明 (MFTs) 之媒體基礎轉換的非同步資料處理。</span><span class="sxs-lookup"><span data-stu-id="448ae-104">This topic describes asynchronous data processing for Media Foundation transforms (MFTs).</span></span>

> [!Note]  
> <span data-ttu-id="448ae-105">本主題適用于 Windows 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="448ae-105">This topic applies to Windows 7 or later.</span></span>

 

-   [<span data-ttu-id="448ae-106">關於非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="448ae-106">About Asynchronous MFTs</span></span>](#about-asynchronous-mfts)
-   [<span data-ttu-id="448ae-107">一般需求</span><span class="sxs-lookup"><span data-stu-id="448ae-107">General Requirements</span></span>](#general-requirements)
-   [<span data-ttu-id="448ae-108">事件</span><span class="sxs-lookup"><span data-stu-id="448ae-108">Events</span></span>](#events)
-   [<span data-ttu-id="448ae-109">ProcessInput</span><span class="sxs-lookup"><span data-stu-id="448ae-109">ProcessInput</span></span>](#processinput)
-   [<span data-ttu-id="448ae-110">ProcessOutput</span><span class="sxs-lookup"><span data-stu-id="448ae-110">ProcessOutput</span></span>](#processoutput)
-   [<span data-ttu-id="448ae-111">排水</span><span class="sxs-lookup"><span data-stu-id="448ae-111">Draining</span></span>](#draining)
-   [<span data-ttu-id="448ae-112">沖洗</span><span class="sxs-lookup"><span data-stu-id="448ae-112">Flushing</span></span>](#flushing)
-   [<span data-ttu-id="448ae-113">標記</span><span class="sxs-lookup"><span data-stu-id="448ae-113">Markers</span></span>](#markers)
-   [<span data-ttu-id="448ae-114">格式變更</span><span class="sxs-lookup"><span data-stu-id="448ae-114">Format Changes</span></span>](#format-changes)
-   [<span data-ttu-id="448ae-115">屬性</span><span class="sxs-lookup"><span data-stu-id="448ae-115">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="448ae-116">解除鎖定非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="448ae-116">Unlocking Asynchronous MFTs</span></span>](#unlocking-asynchronous-mfts)
-   [<span data-ttu-id="448ae-117">關閉 MFT</span><span class="sxs-lookup"><span data-stu-id="448ae-117">Shutting Down the MFT</span></span>](#shutting-down-the-mft)
-   [<span data-ttu-id="448ae-118">註冊和列舉</span><span class="sxs-lookup"><span data-stu-id="448ae-118">Registration and Enumeration</span></span>](#registration-and-enumeration)
-   [<span data-ttu-id="448ae-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="448ae-119">Related topics</span></span>](#related-topics)

## <a name="about-asynchronous-mfts"></a><span data-ttu-id="448ae-120">關於非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="448ae-120">About Asynchronous MFTs</span></span>

<span data-ttu-id="448ae-121">在 Windows Vista 中引進 MFTs 時，API 是針對 *同步* 資料處理而設計。</span><span class="sxs-lookup"><span data-stu-id="448ae-121">When MFTs were introduced in Windows Vista, the API was designed for *synchronous* data processing.</span></span> <span data-ttu-id="448ae-122">在該模型中，MFT 一律是等候取得輸入或等候產生輸出。</span><span class="sxs-lookup"><span data-stu-id="448ae-122">In that model, the MFT is always either waiting to get input, or waiting to produce output.</span></span>

<span data-ttu-id="448ae-123">請考慮一般的影片解碼。</span><span class="sxs-lookup"><span data-stu-id="448ae-123">Consider a typical video decoder.</span></span> <span data-ttu-id="448ae-124">為了取得已解碼的框架，用戶端會呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="448ae-124">To get a decoded frame, the client calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="448ae-125">如果此解碼器有足夠的資料來解碼框架， **ProcessOutput** 會在 MFT 解碼框架時區塊。</span><span class="sxs-lookup"><span data-stu-id="448ae-125">If the decoder has enough data to decode a frame, **ProcessOutput** blocks while the MFT decodes the frame.</span></span> <span data-ttu-id="448ae-126">否則， **ProcessOutput** 會傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT**，指出用戶端應該呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)。</span><span class="sxs-lookup"><span data-stu-id="448ae-126">Otherwise, **ProcessOutput** returns **MF_E_TRANSFORM_NEED_MORE_INPUT**, indicating that the client should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="448ae-127">如果解碼器在一個執行緒上執行所有的解碼作業，此模型就會順利運作。</span><span class="sxs-lookup"><span data-stu-id="448ae-127">This model works well if the decoder performs all of its decoding operations on one thread.</span></span> <span data-ttu-id="448ae-128">但假設解碼器使用多個執行緒來平行解碼框架。</span><span class="sxs-lookup"><span data-stu-id="448ae-128">But suppose the decoder uses several threads to decode frames in parallel.</span></span> <span data-ttu-id="448ae-129">為了達到最佳效能，每當解碼執行緒變成閒置時，應該會收到新的輸入。</span><span class="sxs-lookup"><span data-stu-id="448ae-129">For the best performance, the decoder should receive new input whenever a decoding thread becomes idle.</span></span> <span data-ttu-id="448ae-130">但是，執行緒完成解碼作業的速率不會與用戶端對 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)的呼叫完全一致，因而導致執行緒等待工作。</span><span class="sxs-lookup"><span data-stu-id="448ae-130">But the rate at which threads complete decoding operations will not align exactly with the client's calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), resulting in threads waiting for work.</span></span>

<span data-ttu-id="448ae-131">Windows 7 引進 MFTs 的事件驅動、 *非同步* 處理。</span><span class="sxs-lookup"><span data-stu-id="448ae-131">Windows 7 introduces event-driven, *asynchronous* processing for MFTs.</span></span> <span data-ttu-id="448ae-132">在此模型中，每當 MFT 需要輸入或有輸出時，它就會將事件傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="448ae-132">In this model, whenever the MFT needs input or has output, it sends an event to the client.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="448ae-133">一般需求</span><span class="sxs-lookup"><span data-stu-id="448ae-133">General Requirements</span></span>

<span data-ttu-id="448ae-134">本主題說明非同步 MFTs 與同步的 MFT 有何不同。</span><span class="sxs-lookup"><span data-stu-id="448ae-134">This topic describes how asynchronous MFTs differ from synchronous MFT.</span></span> <span data-ttu-id="448ae-135">除了本主題中注明的，這兩個處理模型是相同的。</span><span class="sxs-lookup"><span data-stu-id="448ae-135">Except where noted in this topic, the two processing models are the same.</span></span> <span data-ttu-id="448ae-136"> (特別是，格式協商相同。 ) </span><span class="sxs-lookup"><span data-stu-id="448ae-136">(In particular, format negotiation is the same.)</span></span>

<span data-ttu-id="448ae-137">非同步 MFT 必須執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="448ae-137">An asynchronous MFT must implement the following interfaces:</span></span>

-   [<span data-ttu-id="448ae-138">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="448ae-138">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="448ae-139">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="448ae-139">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="448ae-140">**IMFShutdown**</span><span class="sxs-lookup"><span data-stu-id="448ae-140">**IMFShutdown**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a><span data-ttu-id="448ae-141">事件</span><span class="sxs-lookup"><span data-stu-id="448ae-141">Events</span></span>

<span data-ttu-id="448ae-142">非同步 MFT 會使用下列事件來表示其資料處理狀態：</span><span class="sxs-lookup"><span data-stu-id="448ae-142">An asynchronous MFT uses the following events to signal its data-processing status:</span></span>



| <span data-ttu-id="448ae-143">事件</span><span class="sxs-lookup"><span data-stu-id="448ae-143">Event</span></span>                                                    | <span data-ttu-id="448ae-144">描述</span><span class="sxs-lookup"><span data-stu-id="448ae-144">Description</span></span>                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="448ae-145">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="448ae-145">METransformNeedInput</span></span>](metransformneedinput.md)         | <span data-ttu-id="448ae-146">當 MFT 可以接受更多輸入時傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-146">Sent when the MFT can accept more input.</span></span>                          |
| [<span data-ttu-id="448ae-147">METransformHaveOutput</span><span class="sxs-lookup"><span data-stu-id="448ae-147">METransformHaveOutput</span></span>](metransformhaveoutput.md)       | <span data-ttu-id="448ae-148">在 MFT 有輸出時傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-148">Sent when the MFT has output.</span></span>                                     |
| [<span data-ttu-id="448ae-149">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="448ae-149">METransformDrainComplete</span></span>](metransformdraincomplete.md) | <span data-ttu-id="448ae-150">清空作業完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-150">Sent when a drain operation completes.</span></span> <span data-ttu-id="448ae-151">請參閱 [清空](#draining)。</span><span class="sxs-lookup"><span data-stu-id="448ae-151">See [Draining](#draining).</span></span> |
| [<span data-ttu-id="448ae-152">METransformMarker</span><span class="sxs-lookup"><span data-stu-id="448ae-152">METransformMarker</span></span>](metransformmarker.md)               | <span data-ttu-id="448ae-153">當標記為「處理中」時傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-153">Sent when a marker is process.</span></span> <span data-ttu-id="448ae-154">請參閱 [標記](#markers)。</span><span class="sxs-lookup"><span data-stu-id="448ae-154">See [Markers](#markers).</span></span>           |



 

<span data-ttu-id="448ae-155">這些事件會在頻外傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-155">These events are sent out-of-band.</span></span> <span data-ttu-id="448ae-156">請務必瞭解 MFT 內容中的頻外和頻外事件之間的差異。</span><span class="sxs-lookup"><span data-stu-id="448ae-156">It is important to understand the difference between in-band and out-of-band events in the context of an MFT.</span></span>

<span data-ttu-id="448ae-157">原始的 MFT 設計支援 *內建* 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-157">The original MFT design supports *in-band* events.</span></span> <span data-ttu-id="448ae-158">內建事件包含有關資料流程的資訊，例如格式變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="448ae-158">An in-band event contains information about the data stream, such as information about a format change.</span></span> <span data-ttu-id="448ae-159">用戶端會藉由呼叫 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)，將內建事件傳送到 MFT。</span><span class="sxs-lookup"><span data-stu-id="448ae-159">The client sends in-band events to the MFT by calling [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span> <span data-ttu-id="448ae-160">MFT 可以在 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法中將內建事件傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="448ae-160">The MFT can send in-band events back to the client in the [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="448ae-161"> (明確地說，事件是在 [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)結構的 **pEvents** 成員中傳達。 ) </span><span class="sxs-lookup"><span data-stu-id="448ae-161">(Specifically, events are conveyed in the **pEvents** member of the [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) structure.)</span></span>

<span data-ttu-id="448ae-162">MFT 會透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送頻外事件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="448ae-162">An MFT sends out-of-band events through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface as follows:</span></span>

1.  <span data-ttu-id="448ae-163">MFT 會實 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，如 [媒體事件](media-event-generators.md)產生器中所述。</span><span class="sxs-lookup"><span data-stu-id="448ae-163">The MFT implements the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface, as described in [Media Event Generators](media-event-generators.md).</span></span>
2.  <span data-ttu-id="448ae-164">用戶端會在 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面的 MFT 上呼叫 **IUnknown：： QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="448ae-164">The client calls **IUnknown::QueryInterface** on the MFT for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="448ae-165">非同步 MFT 必須公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="448ae-165">An asynchronous MFT must expose this interface.</span></span> <span data-ttu-id="448ae-166">同步 MFTs 不應公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="448ae-166">Synchronous MFTs should not expose this interface.</span></span>
3.  <span data-ttu-id="448ae-167">用戶端會呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 和 [**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) ，以接收來自 MFT 的頻外事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-167">The client calls [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) and [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to receive out-of-band events from the MFT.</span></span>

## <a name="processinput"></a><span data-ttu-id="448ae-168">ProcessInput</span><span class="sxs-lookup"><span data-stu-id="448ae-168">ProcessInput</span></span>

<span data-ttu-id="448ae-169">[**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)方法的修改方式如下：</span><span class="sxs-lookup"><span data-stu-id="448ae-169">The [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method is modified as follows:</span></span>

1.  <span data-ttu-id="448ae-170">串流處理開始時，用戶端會傳送 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="448ae-170">When streaming starts, the client sends the [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) message.</span></span>
2.  <span data-ttu-id="448ae-171">在串流處理期間，MFT 會藉由傳送 [METransformNeedInput](metransformneedinput.md) 事件來要求資料。</span><span class="sxs-lookup"><span data-stu-id="448ae-171">During streaming, the MFT requests data by sending an [METransformNeedInput](metransformneedinput.md) event.</span></span> <span data-ttu-id="448ae-172">事件資料是資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="448ae-172">The event data is the stream identifier.</span></span>
3.  <span data-ttu-id="448ae-173">針對每個 [METransformNeedInput](metransformneedinput.md) 事件，用戶端會呼叫指定資料流程的 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 。</span><span class="sxs-lookup"><span data-stu-id="448ae-173">For each [METransformNeedInput](metransformneedinput.md) event, the client calls [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) for the specified stream.</span></span>
4.  <span data-ttu-id="448ae-174">在串流結束時，用戶端可能會使用 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)訊息來呼叫 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。</span><span class="sxs-lookup"><span data-stu-id="448ae-174">At the end of streaming, the client may call [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) message.</span></span>

<span data-ttu-id="448ae-175">執行附注：</span><span class="sxs-lookup"><span data-stu-id="448ae-175">Implementation notes:</span></span>

-   <span data-ttu-id="448ae-176">在接收 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息之前，此 MFT 必須傳送任何 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-176">The MFT must not send any [METransformNeedInput](metransformneedinput.md) events until it receives the [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) message.</span></span>
-   <span data-ttu-id="448ae-177">在串流處理期間，MFT 可能會在任何時間傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-177">During streaming, the MFT may send [METransformNeedInput](metransformneedinput.md) events at any time.</span></span>
-   <span data-ttu-id="448ae-178">此 MFT 應維持暫止 [METransformNeedInput](metransformneedinput.md) 事件的計數。</span><span class="sxs-lookup"><span data-stu-id="448ae-178">The MFT should maintain a count of pending [METransformNeedInput](metransformneedinput.md) events.</span></span> <span data-ttu-id="448ae-179">任何未對應至 METransformNeedInput 事件的 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 呼叫都必須傳回 **MF_E_NOTACCEPTING**。</span><span class="sxs-lookup"><span data-stu-id="448ae-179">Any call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) that does not correspond to an METransformNeedInput event must return **MF_E_NOTACCEPTING**.</span></span>
-   <span data-ttu-id="448ae-180">當 MFT 收到 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) 訊息時，它會將擱置中 [METransformNeedInput](metransformneedinput.md) 事件的計數重設為零。</span><span class="sxs-lookup"><span data-stu-id="448ae-180">When the MFT receives the [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) message, it resets the count of pending [METransformNeedInput](metransformneedinput.md) events to zero.</span></span>
-   <span data-ttu-id="448ae-181">當 MFT 收到 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)訊息之後，就不能傳送任何 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-181">The MFT must not send any [METransformNeedInput](metransformneedinput.md) events after it receives the [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) message.</span></span>
-   <span data-ttu-id="448ae-182">如果在 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)之前或 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)之後呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，此方法必須傳回 **MF_E_NOTACCEPTING**。</span><span class="sxs-lookup"><span data-stu-id="448ae-182">If [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) is called before [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) or after [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), the method must return **MF_E_NOTACCEPTING**.</span></span>

## <a name="processoutput"></a><span data-ttu-id="448ae-183">ProcessOutput</span><span class="sxs-lookup"><span data-stu-id="448ae-183">ProcessOutput</span></span>

<span data-ttu-id="448ae-184">[**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法的修改方式如下：</span><span class="sxs-lookup"><span data-stu-id="448ae-184">The [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method is modified as follows:</span></span>

1.  <span data-ttu-id="448ae-185">只要 MFT 有輸出，它就會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-185">Whenever the MFT has output, it sends an [METransformHaveOutput](metransformhaveoutput.md) event.</span></span>
2.  <span data-ttu-id="448ae-186">針對每個 [METransformHaveOutput](metransformhaveoutput.md) 事件，用戶端會呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="448ae-186">For each [METransformHaveOutput](metransformhaveoutput.md) event, the client calls [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span>

<span data-ttu-id="448ae-187">執行附注：</span><span class="sxs-lookup"><span data-stu-id="448ae-187">Implementation notes:</span></span>

-   <span data-ttu-id="448ae-188">如果用戶端在任何其他時間呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ，此方法會傳回 **E_UNEXPECTED**。</span><span class="sxs-lookup"><span data-stu-id="448ae-188">If the client calls [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) at any other time, the method returns **E_UNEXPECTED**.</span></span>
-   <span data-ttu-id="448ae-189">非同步 MFT 絕對不應該從 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT** 。</span><span class="sxs-lookup"><span data-stu-id="448ae-189">An asynchronous MFT should never return **MF_E_TRANSFORM_NEED_MORE_INPUT** from the [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="448ae-190">如果 MFT 需要更多輸入，則會傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-190">If the MFT requires more input, it sends an [METransformNeedInput](metransformneedinput.md) event.</span></span>

## <a name="draining"></a><span data-ttu-id="448ae-191">排水</span><span class="sxs-lookup"><span data-stu-id="448ae-191">Draining</span></span>

<span data-ttu-id="448ae-192">清空 MFT 會使 MFT 產生的輸出數量，與任何已傳送的輸入資料相同。</span><span class="sxs-lookup"><span data-stu-id="448ae-192">Draining an MFT causes the MFT to produce as much output as it can from whatever input data has already been sent.</span></span> <span data-ttu-id="448ae-193">清空非同步 MFT 的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="448ae-193">Draining an asynchronous MFT works as follows:</span></span>

1.  <span data-ttu-id="448ae-194">用戶端會傳送 [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="448ae-194">The client sends the [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) message.</span></span>
2.  <span data-ttu-id="448ae-195">MFT 會繼續傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件，直到它沒有其他要處理的資料為止。</span><span class="sxs-lookup"><span data-stu-id="448ae-195">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="448ae-196">它不會在這段時間內傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-196">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
3.  <span data-ttu-id="448ae-197">在 MFT 傳送最後一個 [METransformHaveOutput](metransformhaveoutput.md) 事件之後，它會傳送 [METransformDrainComplete](metransformdraincomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-197">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>

<span data-ttu-id="448ae-198">完成清空之後，除非從用戶端收到 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息，否則 MFT 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-198">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="flushing"></a><span data-ttu-id="448ae-199">沖洗</span><span class="sxs-lookup"><span data-stu-id="448ae-199">Flushing</span></span>

<span data-ttu-id="448ae-200">用戶端可以藉由傳送 [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) 訊息來清除 MFT。</span><span class="sxs-lookup"><span data-stu-id="448ae-200">The client can flush the MFT by sending the [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="448ae-201">MFT 會卸載其所持有的所有輸入和輸出範例。</span><span class="sxs-lookup"><span data-stu-id="448ae-201">The MFT drops all of the input and output samples it is holding.</span></span>

<span data-ttu-id="448ae-202">在接收來自用戶端的 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息之前，不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-202">The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="markers"></a><span data-ttu-id="448ae-203">標記</span><span class="sxs-lookup"><span data-stu-id="448ae-203">Markers</span></span>

<span data-ttu-id="448ae-204">用戶端可以藉由傳送 [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) 訊息來標記資料流程中的某個點。</span><span class="sxs-lookup"><span data-stu-id="448ae-204">The client can mark a point in the stream by sending the [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) message.</span></span> <span data-ttu-id="448ae-205">MFT 會以下列方式回應：</span><span class="sxs-lookup"><span data-stu-id="448ae-205">The MFT responds as follows:</span></span>

1.  <span data-ttu-id="448ae-206">MFT 會從現有的輸入資料產生任意數量的輸出範例，並為每個輸出範例傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-206">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="448ae-207">產生所有輸出之後，MFT 會傳送 [METransformMarker](metransformmarker.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-207">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="448ae-208">此事件必須在所有 [METransformHaveOutput](metransformhaveoutput.md) 事件之後傳送。</span><span class="sxs-lookup"><span data-stu-id="448ae-208">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="448ae-209">例如，假設某個解碼器有足夠的輸入資料來產生四個輸出範例。</span><span class="sxs-lookup"><span data-stu-id="448ae-209">For example, suppose that a decoder has enough input data to produce four output samples.</span></span> <span data-ttu-id="448ae-210">如果用戶端傳送 [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) 訊息，則此 MFT 會將四個 [METransformHaveOutput](metransformhaveoutput.md) 事件排在佇列中，每個輸出範例 (一個) ，然後是 [METransformMarker](metransformmarker.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-210">If the client sends the [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) message, the MFT will queue four [METransformHaveOutput](metransformhaveoutput.md) events (one per output sample), followed by an [METransformMarker](metransformmarker.md) event.</span></span>

<span data-ttu-id="448ae-211">標記訊息類似于清空訊息。</span><span class="sxs-lookup"><span data-stu-id="448ae-211">The marker message is similar to the drain message.</span></span> <span data-ttu-id="448ae-212">不過，清空會視為資料流程中的中斷，而標記則不會。</span><span class="sxs-lookup"><span data-stu-id="448ae-212">However, a drain is considered a break in the stream, whereas a marker is not.</span></span> <span data-ttu-id="448ae-213">清空和標記具有下列差異。</span><span class="sxs-lookup"><span data-stu-id="448ae-213">Draining and markers have the following differences.</span></span>

<span data-ttu-id="448ae-214">排水：</span><span class="sxs-lookup"><span data-stu-id="448ae-214">Draining:</span></span>

-   <span data-ttu-id="448ae-215">在清空時，MFT 不會傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-215">While draining, the MFT does not send [METransformNeedInput](metransformneedinput.md) events.</span></span>
-   <span data-ttu-id="448ae-216">MFT 會捨棄無法用來建立輸出範例的任何輸入資料。</span><span class="sxs-lookup"><span data-stu-id="448ae-216">The MFT discards any input data that cannot be used to create an output sample.</span></span>
-   <span data-ttu-id="448ae-217">某些 MFTs 會在資料的結尾處產生「結尾」。</span><span class="sxs-lookup"><span data-stu-id="448ae-217">Some MFTs produce a "tail" at the end of the data.</span></span> <span data-ttu-id="448ae-218">例如，當輸入資料停止之後，會產生額外的資料等音訊效果。</span><span class="sxs-lookup"><span data-stu-id="448ae-218">For example, audio effects such as reverb or echo produce extra data after the input data has stopped.</span></span> <span data-ttu-id="448ae-219">產生結尾的 MFT 應該在清空作業結束時這麼做。</span><span class="sxs-lookup"><span data-stu-id="448ae-219">An MFT that generates a tail should do so at the end of a drain operation.</span></span>
-   <span data-ttu-id="448ae-220">在 MFT 完成清空之後，它會將下一個輸出範例標示 [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) 屬性，以表示資料流程中的不連續。</span><span class="sxs-lookup"><span data-stu-id="448ae-220">After the MFT has finished draining, it marks the next output sample with the [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute, to indicate a discontinuity in the stream.</span></span>

<span data-ttu-id="448ae-221">標記：</span><span class="sxs-lookup"><span data-stu-id="448ae-221">Marker:</span></span>

-   <span data-ttu-id="448ae-222">MFT 會繼續傳送 [METransformNeedInput](metransformneedinput.md) 事件，然後再傳送標記事件。</span><span class="sxs-lookup"><span data-stu-id="448ae-222">The MFT continues to send [METransformNeedInput](metransformneedinput.md) events before sending the marker event.</span></span>
-   <span data-ttu-id="448ae-223">MFT 不會捨棄任何輸入資料。</span><span class="sxs-lookup"><span data-stu-id="448ae-223">The MFT does not discard any input data.</span></span> <span data-ttu-id="448ae-224">如果有部分資料，則應該在標記點之後處理。</span><span class="sxs-lookup"><span data-stu-id="448ae-224">If there is partial data, it should be processed after the marker point.</span></span>
-   <span data-ttu-id="448ae-225">MFT 不會在標記點產生結尾。</span><span class="sxs-lookup"><span data-stu-id="448ae-225">The MFT does not produce a tail at the marker point.</span></span>
-   <span data-ttu-id="448ae-226">此 MFT 不會在標記點之後設定不中斷旗標。</span><span class="sxs-lookup"><span data-stu-id="448ae-226">The MFT does not set the discontinuity flag after the marker point.</span></span>

## <a name="format-changes"></a><span data-ttu-id="448ae-227">格式變更</span><span class="sxs-lookup"><span data-stu-id="448ae-227">Format Changes</span></span>

<span data-ttu-id="448ae-228">非同步 MFT 必須支援動態格式變更，如 [處理資料流程變更](handling-stream-changes.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="448ae-228">An asynchronous MFT must support dynamic format changes, as described in [Handling Stream Changes](handling-stream-changes.md).</span></span>

## <a name="attributes"></a><span data-ttu-id="448ae-229">屬性</span><span class="sxs-lookup"><span data-stu-id="448ae-229">Attributes</span></span>

<span data-ttu-id="448ae-230">非同步 MFT 必須執行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法，以傳回有效的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="448ae-230">An asynchronous MFT must implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method to return a valid attribute store.</span></span> <span data-ttu-id="448ae-231">下列屬性適用于非同步 MFTs：</span><span class="sxs-lookup"><span data-stu-id="448ae-231">The following attributes apply to asynchronous MFTs:</span></span>



| <span data-ttu-id="448ae-232">屬性</span><span class="sxs-lookup"><span data-stu-id="448ae-232">Attribute</span></span>                                                                                    | <span data-ttu-id="448ae-233">描述</span><span class="sxs-lookup"><span data-stu-id="448ae-233">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="448ae-234">MF_TRANSFORM_ASYNC</span><span class="sxs-lookup"><span data-stu-id="448ae-234">MF_TRANSFORM_ASYNC</span></span>](mf-transform-async.md)                                               | <span data-ttu-id="448ae-235">MFT 必須將此屬性設定為 **TRUE** (1) 。</span><span class="sxs-lookup"><span data-stu-id="448ae-235">The MFT must set this attribute to **TRUE** (1).</span></span> <span data-ttu-id="448ae-236">用戶端可以查詢這個屬性，以找出 MFT 是否為非同步。</span><span class="sxs-lookup"><span data-stu-id="448ae-236">The client can query this attribute to discover whether the MFT is asynchronous.</span></span> |
| [<span data-ttu-id="448ae-237">MF_TRANSFORM_ASYNC_UNLOCK</span><span class="sxs-lookup"><span data-stu-id="448ae-237">MF_TRANSFORM_ASYNC_UNLOCK</span></span>](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [<span data-ttu-id="448ae-238">**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="448ae-238">**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="448ae-239">MFT 必須將此屬性設定為 **TRUE** (1) 。</span><span class="sxs-lookup"><span data-stu-id="448ae-239">The MFT must set this attribute to **TRUE** (1).</span></span> <span data-ttu-id="448ae-240">用戶端可以假設已設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="448ae-240">The client can assume that this attribute is set.</span></span>                                |



 

## <a name="unlocking-asynchronous-mfts"></a><span data-ttu-id="448ae-241">解除鎖定非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="448ae-241">Unlocking Asynchronous MFTs</span></span>

<span data-ttu-id="448ae-242">非同步 MFTs 與原始的 MFT 資料處理模型不相容。</span><span class="sxs-lookup"><span data-stu-id="448ae-242">Asynchronous MFTs are not compatible with the original MFT data processing model.</span></span> <span data-ttu-id="448ae-243">為了防止非同步 MFTs 中斷現有的應用程式，會定義下列機制：</span><span class="sxs-lookup"><span data-stu-id="448ae-243">To prevent asynchronous MFTs from breaking existing applications, the following mechanism is defined:</span></span>

<dl> <span data-ttu-id="448ae-244">用戶端會在 MFT 上呼叫 <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform：： GetAttributes</a> 。</span><span class="sxs-lookup"><span data-stu-id="448ae-244">The client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform::GetAttributes</a> on the MFT.</span></span>  
<span data-ttu-id="448ae-245">用戶端會查詢這個 <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> 屬性的。</span><span class="sxs-lookup"><span data-stu-id="448ae-245">The client queries the for this <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> attribute.</span></span> <span data-ttu-id="448ae-246">若為非同步 MFT，此屬性的值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="448ae-246">For an asynchronous MFT, the value of this attribute is **TRUE**.</span></span>  
<span data-ttu-id="448ae-247">若要解除鎖定 MFT，用戶端必須將 <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="448ae-247">To unlock the MFT, the client must sets the <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> attribute to **TRUE**.</span></span>  
</dl>

<span data-ttu-id="448ae-248">在用戶端解除鎖定 MFT 之前，所有 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法應該會傳回 **MF_E_TRANSFORM_ASYNC_LOCKED**，但有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="448ae-248">Until the client unlocks the MFT, all [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods should return **MF_E_TRANSFORM_ASYNC_LOCKED**, with the following exceptions:</span></span>

-   <span data-ttu-id="448ae-249">[**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (所有非同步 MFTs) </span><span class="sxs-lookup"><span data-stu-id="448ae-249">[**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (all asynchronous MFTs)</span></span>
-   <span data-ttu-id="448ae-250">[**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (所有非同步 MFTs) </span><span class="sxs-lookup"><span data-stu-id="448ae-250">[**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (all asynchronous MFTs)</span></span>
-   <span data-ttu-id="448ae-251">[**IMFTransform：： GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (編碼器僅) </span><span class="sxs-lookup"><span data-stu-id="448ae-251">[**IMFTransform::GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (encoders only)</span></span>
-   <span data-ttu-id="448ae-252">[**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (編碼器僅) </span><span class="sxs-lookup"><span data-stu-id="448ae-252">[**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (encoders only)</span></span>
-   <span data-ttu-id="448ae-253">[**IMFTransform：： GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (所有非同步 MFTs) </span><span class="sxs-lookup"><span data-stu-id="448ae-253">[**IMFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (all asynchronous MFTs)</span></span>
-   <span data-ttu-id="448ae-254">[**IMFTransform：： GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (所有非同步 MFTs) </span><span class="sxs-lookup"><span data-stu-id="448ae-254">[**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (all asynchronous MFTs)</span></span>

<span data-ttu-id="448ae-255">下列程式碼顯示如何解除鎖定非同步 MFT：</span><span class="sxs-lookup"><span data-stu-id="448ae-255">The following code shows how to unlock an asynchronous MFT:</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a><span data-ttu-id="448ae-256">關閉 MFT</span><span class="sxs-lookup"><span data-stu-id="448ae-256">Shutting Down the MFT</span></span>

<span data-ttu-id="448ae-257">非同步 MFTs 必須執行 [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) 介面。</span><span class="sxs-lookup"><span data-stu-id="448ae-257">Asynchronous MFTs must implement the [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) interface.</span></span>

-   <span data-ttu-id="448ae-258">[**關機**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)： MFT 必須關閉其事件佇列。</span><span class="sxs-lookup"><span data-stu-id="448ae-258">[**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): The MFT must shut down its event queue.</span></span> <span data-ttu-id="448ae-259">如果使用標準事件佇列，請呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="448ae-259">If using the standard event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown).</span></span> <span data-ttu-id="448ae-260">（選擇性） MFT 可能會釋放其他資源。</span><span class="sxs-lookup"><span data-stu-id="448ae-260">Optionally, the MFT may release other resources.</span></span> <span data-ttu-id="448ae-261">呼叫 **關機** 之後，用戶端不能使用 MFT。</span><span class="sxs-lookup"><span data-stu-id="448ae-261">The client must not use the MFT after calling **Shutdown**.</span></span>
-   <span data-ttu-id="448ae-262">[**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)：呼叫 [**關機**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)之後，MFT 應傳回 *pStatus* 參數中 **MFSHUTDOWN_COMPLETED** 的值。</span><span class="sxs-lookup"><span data-stu-id="448ae-262">[**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): After [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) has been called, the MFT should return the value **MFSHUTDOWN_COMPLETED** in the *pStatus* parameter.</span></span> <span data-ttu-id="448ae-263">它不應該傳回 **MFSHUTDOWN_INITIATED** 的值。</span><span class="sxs-lookup"><span data-stu-id="448ae-263">It should not return the value **MFSHUTDOWN_INITIATED**.</span></span>

## <a name="registration-and-enumeration"></a><span data-ttu-id="448ae-264">註冊和列舉</span><span class="sxs-lookup"><span data-stu-id="448ae-264">Registration and Enumeration</span></span>

<span data-ttu-id="448ae-265">若要註冊非同步 MFT，請呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)函式，並在 *旗標* 參數中設定 **MFT_ENUM_FLAG_ASYNCMFT** 旗標。</span><span class="sxs-lookup"><span data-stu-id="448ae-265">To register an asynchronous MFT, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function and set the **MFT_ENUM_FLAG_ASYNCMFT** flag in the *Flags* parameter.</span></span> <span data-ttu-id="448ae-266"> (先前已保留此旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="448ae-266">(Previously this flag was reserved.)</span></span>

<span data-ttu-id="448ae-267">若要列舉非同步 MFTs，請呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數，並在 Flags 參數中設定 **MFT_ENUM_FLAG_ASYNCMFT** 旗 *標* 。</span><span class="sxs-lookup"><span data-stu-id="448ae-267">To enumerate asynchronous MFTs, call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function and set the **MFT_ENUM_FLAG_ASYNCMFT** flag in the *Flags* parameter.</span></span> <span data-ttu-id="448ae-268">為了回溯相容性， [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數不會列舉非同步 MFTs。</span><span class="sxs-lookup"><span data-stu-id="448ae-268">For backward compatibility, the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function does not enumerate asynchronous MFTs.</span></span> <span data-ttu-id="448ae-269">否則，在使用者的電腦上安裝非同步 MFT 可能會中斷現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="448ae-269">Otherwise, installing an asynchronous MFT on the user's computer could break existing applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="448ae-270">相關主題</span><span class="sxs-lookup"><span data-stu-id="448ae-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="448ae-271">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="448ae-271">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



