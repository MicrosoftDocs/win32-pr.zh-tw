---
description: 本主題說明媒體基礎轉換 (MFT) 應該如何處理串流期間的格式變更。
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: 處理資料流程變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191711"
---
# <a name="handling-stream-changes"></a><span data-ttu-id="84f68-103">處理資料流程變更</span><span class="sxs-lookup"><span data-stu-id="84f68-103">Handling Stream Changes</span></span>

<span data-ttu-id="84f68-104">本主題說明媒體基礎轉換 (MFT) 應該如何處理串流期間的格式變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-104">This topic describes how a Media Foundation transform (MFT) should handle format changes during streaming.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="84f68-105">本主題不適用於編碼器。</span><span class="sxs-lookup"><span data-stu-id="84f68-105">This topic does not apply to encoders.</span></span> <span data-ttu-id="84f68-106">編碼器不應傳播格式變更，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="84f68-106">Encoders should not propagate format changes as described in this topic.</span></span> <span data-ttu-id="84f68-107">編碼器應該只接受符合目前設定之輸出類型的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-107">Encoders should only accept an input type that matches the currently configured output type.</span></span>

 

## <a name="overview-of-format-changes"></a><span data-ttu-id="84f68-108">格式變更總覽</span><span class="sxs-lookup"><span data-stu-id="84f68-108">Overview of Format Changes</span></span>

<span data-ttu-id="84f68-109">一般來說，在串流處理期間可能會變更格式的兩個原因。</span><span class="sxs-lookup"><span data-stu-id="84f68-109">Generally, there are two reasons that a format can change during streaming.</span></span>

-   <span data-ttu-id="84f68-110">用戶端可能會切換至具有新格式的資料流程。</span><span class="sxs-lookup"><span data-stu-id="84f68-110">The client might switch to a stream with a new format.</span></span> <span data-ttu-id="84f68-111">例如，在數位電視中，這可能是因為通道變更所造成。</span><span class="sxs-lookup"><span data-stu-id="84f68-111">For example, in digital television, this can occur due to a channel change.</span></span>
-   <span data-ttu-id="84f68-112">在某些影片格式（例如 h.264）中，位流可以指示格式變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-112">In some video formats, such as H.264, the bitstream can signal a format change.</span></span> <span data-ttu-id="84f68-113">這類變更可能包括欄位支配、視頻解析度或圖元外觀比例的變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-113">Such changes might include changes in field dominance, video resolution, or pixel aspect ratio.</span></span>

<span data-ttu-id="84f68-114">如果編碼類型變更，用戶端可能需要從管線中移除 MFT，並將它取代為另一個 MFT。</span><span class="sxs-lookup"><span data-stu-id="84f68-114">If the encoding type changes, the client might need to remove the MFT from the pipeline and replace it with another MFT.</span></span> <span data-ttu-id="84f68-115"> (例如，用戶端可能需要換成新的解碼器。 ) 本主題未涵蓋這種情況。</span><span class="sxs-lookup"><span data-stu-id="84f68-115">(For example, the client might need to swap in a new decoder.) This topic does not cover that situation.</span></span> <span data-ttu-id="84f68-116">本主題僅涵蓋目前的 MFT 可以處理新格式的情況。</span><span class="sxs-lookup"><span data-stu-id="84f68-116">This topic covers only the case where the current MFT can handle the new format.</span></span>

<span data-ttu-id="84f68-117">如果格式有所變更，則 MFT 可能需要新的輸入類型、新的輸出類型或兩者。</span><span class="sxs-lookup"><span data-stu-id="84f68-117">If the format changes, the MFT might require a new input type, a new output type, or both.</span></span>

-   <span data-ttu-id="84f68-118">輸入類型的變更是由用戶端所起始。</span><span class="sxs-lookup"><span data-stu-id="84f68-118">Changes to input type are initiated by the client.</span></span> <span data-ttu-id="84f68-119">MFT 絕不會變更自己的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-119">An MFT never changes its own input type.</span></span>
-   <span data-ttu-id="84f68-120">對輸出類型所做的變更是由 MFT 所起始。</span><span class="sxs-lookup"><span data-stu-id="84f68-120">Changes to output type are initiated by the MFT.</span></span> <span data-ttu-id="84f68-121">MFT 表示它需要新的輸出類型，而且用戶端會以 MFT 協商新的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-121">The MFT signals that it requires a new output type, and the client negotiates the new output type with the MFT.</span></span>

<span data-ttu-id="84f68-122">因此，可能有三種不同的案例：</span><span class="sxs-lookup"><span data-stu-id="84f68-122">Thus, three distinct cases are possible:</span></span>

-   <span data-ttu-id="84f68-123">用戶端會設定新的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-123">The client sets a new input type.</span></span> <span data-ttu-id="84f68-124">MFT 會取用新的格式，而不會變更其輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-124">The MFT consumes the new format, with no change to its output type.</span></span>
-   <span data-ttu-id="84f68-125">用戶端會設定新的輸入型別，而這會觸發輸出型別中的變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-125">The client sets a new input type, and this triggers a change in the output type.</span></span>
-   <span data-ttu-id="84f68-126">輸入類型不會變更，但 MFT 會偵測到位流中的格式變更，這需要新的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-126">The input type does not change, but the MFT detects a format change in the bitstream, which requires a new output type.</span></span>

## <a name="implementing-format-changes"></a><span data-ttu-id="84f68-127">執行格式變更</span><span class="sxs-lookup"><span data-stu-id="84f68-127">Implementing Format Changes</span></span>

<span data-ttu-id="84f68-128">本主題的其餘部分將說明用戶端應該如何處理格式變更，以及如何在 MFT 中執行格式變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-128">The remainder of this topic describes how the client should process a format change, and how to implement format changes in an MFT.</span></span>

### <a name="output-type"></a><span data-ttu-id="84f68-129">輸出類型</span><span class="sxs-lookup"><span data-stu-id="84f68-129">Output Type</span></span>

<span data-ttu-id="84f68-130">任何 MFT 都可以起始其輸出類型的變更，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84f68-130">Any MFT can initiate a change to its output type, as follows:</span></span>

1.  <span data-ttu-id="84f68-131">用戶端會呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="84f68-131">The client calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="84f68-132">MFT 會以下列方式回應：</span><span class="sxs-lookup"><span data-stu-id="84f68-132">The MFT responds as follows:</span></span>
    1.  <span data-ttu-id="84f68-133">MFT 不會在 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)中產生輸出範例。</span><span class="sxs-lookup"><span data-stu-id="84f68-133">The MFT does not produce an output sample in [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span>
    2.  <span data-ttu-id="84f68-134">MFT 會在 [**mft \_ 輸出 \_ 資料 \_ 緩衝區**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)結構的 **dwStatus** 成員中設定 **mft \_ 輸出 \_ 資料 \_ 緩衝區 \_ 格式 \_ 變更** 旗標。</span><span class="sxs-lookup"><span data-stu-id="84f68-134">The MFT sets the **MFT\_OUTPUT\_DATA\_BUFFER\_FORMAT\_CHANGE** flag in the **dwStatus** member of the [**MFT\_OUTPUT\_DATA\_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) structure.</span></span>
    3.  <span data-ttu-id="84f68-135">[**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法會傳回錯誤碼 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。</span><span class="sxs-lookup"><span data-stu-id="84f68-135">The [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns the error code **MF\_E\_TRANSFORM\_STREAM\_CHANGE**.</span></span>
2.  <span data-ttu-id="84f68-136">用戶端會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)。</span><span class="sxs-lookup"><span data-stu-id="84f68-136">The client calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="84f68-137">這個方法會傳回一組更新的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-137">This method returns an updated set of output types.</span></span>
3.  <span data-ttu-id="84f68-138">用戶端會呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定新的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-138">The client calls [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set a new output type.</span></span>
4.  <span data-ttu-id="84f68-139">用戶端會繼續呼叫 [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="84f68-139">The client resumes calling [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput)/[**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span>

### <a name="input-type"></a><span data-ttu-id="84f68-140">輸入類型</span><span class="sxs-lookup"><span data-stu-id="84f68-140">Input Type</span></span>

<span data-ttu-id="84f68-141">輸入類型的變更是由用戶端所起始，而不是由 MFT 所起始。</span><span class="sxs-lookup"><span data-stu-id="84f68-141">Changes to the input type are initiated by the client, never by the MFT.</span></span> <span data-ttu-id="84f68-142">如果輸入類型變更，它可能會觸發輸出類型的變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-142">If the input type changes, it might trigger a change to the output type.</span></span>

<span data-ttu-id="84f68-143">確切的事件順序取決於 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="84f68-143">The exact sequence of events depends on the value of the [**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**](mft-support-dynamic-format-change-attribute.md) attribute.</span></span>



| <span data-ttu-id="84f68-144">值</span><span class="sxs-lookup"><span data-stu-id="84f68-144">Value</span></span>     | <span data-ttu-id="84f68-145">描述</span><span class="sxs-lookup"><span data-stu-id="84f68-145">Description</span></span>                                                     |
|-----------|-----------------------------------------------------------------|
| <span data-ttu-id="84f68-146">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84f68-146">**FALSE**</span></span> | <span data-ttu-id="84f68-147">在用戶端設定新的輸入類型之前，必須先清空 MFT。</span><span class="sxs-lookup"><span data-stu-id="84f68-147">Before the client sets a new input type, it must drain the MFT.</span></span> |
| <span data-ttu-id="84f68-148">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84f68-148">**TRUE**</span></span>  | <span data-ttu-id="84f68-149">用戶端可以設定新的輸入類型，而不需要清空 MFT。</span><span class="sxs-lookup"><span data-stu-id="84f68-149">The client can set a new input type without draining the MFT.</span></span>   |



 

<span data-ttu-id="84f68-150">MFT 會透過其 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法來公開這個屬性。</span><span class="sxs-lookup"><span data-stu-id="84f68-150">An MFT exposes this attribute through its [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="84f68-151">這個屬性的預設值為 **FALSE**;如果 MFT 未設定此屬性，請將值視為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="84f68-151">The default value of this attribute is **FALSE**; if the MFT does not set the attribute, treat the value as **FALSE**.</span></span>

<span data-ttu-id="84f68-152">**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更為 FALSE**</span><span class="sxs-lookup"><span data-stu-id="84f68-152">**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE is FALSE**</span></span>

1.  <span data-ttu-id="84f68-153">用戶端傳送 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="84f68-153">The client sends the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span>
2.  <span data-ttu-id="84f68-154">用戶端會藉由呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來清空 MFT，直到 **ProcessOutput** 傳回 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**。</span><span class="sxs-lookup"><span data-stu-id="84f68-154">The client drains the MFT by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) until **ProcessOutput** returns **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
3.  <span data-ttu-id="84f68-155">用戶端會呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定新的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-155">The client calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the new input type.</span></span>
4.  <span data-ttu-id="84f68-156">MFT 會驗證輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-156">The MFT validates the input type.</span></span> <span data-ttu-id="84f68-157">如果類型無效， [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 會傳回 **MF \_ E \_ INVALIDMEDIATYPE** 或其他錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f68-157">If the type is invalid, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) returns **MF\_E\_INVALIDMEDIATYPE** or another error code.</span></span> <span data-ttu-id="84f68-158">否則， **SetInputType** 會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="84f68-158">Otherwise, **SetInputType** returns S\_OK.</span></span>
5.  <span data-ttu-id="84f68-159">假設輸入類型有效，則 MFT 會評估輸出類型是否也會變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-159">Assuming the input type is valid, the MFT evaluates whether the output type also changes.</span></span> <span data-ttu-id="84f68-160">如果不是，則資料流程會繼續進行，不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="84f68-160">If not, streaming continues, and no further action is required.</span></span>
6.  <span data-ttu-id="84f68-161">如果輸出類型變更：</span><span class="sxs-lookup"><span data-stu-id="84f68-161">If the output type changes:</span></span>
    1.  <span data-ttu-id="84f68-162">MFT 會使其目前的輸出媒體類型失效，並更新可用輸出媒體類型的清單。</span><span class="sxs-lookup"><span data-stu-id="84f68-162">The MFT invalidates its current output media type, and updates the list of available output media types.</span></span>
    2.  <span data-ttu-id="84f68-163">[**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)的下一個呼叫會傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**，如上一節中所述。</span><span class="sxs-lookup"><span data-stu-id="84f68-163">The next call to [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) returns **MF\_E\_TRANSFORM\_STREAM\_CHANGE**, as described in the previous section.</span></span>
    3.  <span data-ttu-id="84f68-164">用戶端會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取得更新的輸出類型清單。</span><span class="sxs-lookup"><span data-stu-id="84f68-164">The client calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the updated list of output types.</span></span>
    4.  <span data-ttu-id="84f68-165">用戶端會呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。</span><span class="sxs-lookup"><span data-stu-id="84f68-165">The client calls [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="84f68-166">**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更為 TRUE**</span><span class="sxs-lookup"><span data-stu-id="84f68-166">**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE is TRUE**</span></span>

1.  <span data-ttu-id="84f68-167">用戶端會呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定新的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-167">The client calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the new input type.</span></span>
2.  <span data-ttu-id="84f68-168">MFT 會驗證輸入類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-168">The MFT validates the input type.</span></span> <span data-ttu-id="84f68-169">如果類型無效， [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 會傳回 **MF \_ E \_ INVALIDMEDIATYPE** 或其他錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f68-169">If the type is invalid, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) returns **MF\_E\_INVALIDMEDIATYPE** or another error code.</span></span> <span data-ttu-id="84f68-170">否則， **SetInputType** 會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="84f68-170">Otherwise, **SetInputType** returns S\_OK.</span></span>
3.  <span data-ttu-id="84f68-171">假設輸入類型有效，則 MFT 會評估輸出類型是否也會變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-171">Assuming the input type is valid, the MFT evaluates whether the output type also changes.</span></span> <span data-ttu-id="84f68-172">如果不是，則資料流程會繼續進行，不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="84f68-172">If not, streaming continues, and no further action is required.</span></span>
4.  <span data-ttu-id="84f68-173">在輸出類型變更之前，MFT 必須處理任何快取的輸入範例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84f68-173">Before the output type changes, the MFT must process any cached input samples, as follows:</span></span>
    1.  <span data-ttu-id="84f68-174">MFT 不會使其目前的輸出類型無效。</span><span class="sxs-lookup"><span data-stu-id="84f68-174">The MFT does not invalidate its current output type.</span></span>
    2.  <span data-ttu-id="84f68-175">從快取的輸入範例中，MFT 產生的輸出越多。</span><span class="sxs-lookup"><span data-stu-id="84f68-175">The MFT produces as much output as it can from the cached input samples.</span></span>
    3.  <span data-ttu-id="84f68-176">無論是在處理快取的範例時，MFT 是否接受新的輸入範例都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="84f68-176">It is optional whether the MFT accepts new input samples while it processes the cached samples.</span></span> <span data-ttu-id="84f68-177">如果是，新的輸入範例將會使用新的輸入格式，因此 MFT 必須在格式變更時追蹤點。</span><span class="sxs-lookup"><span data-stu-id="84f68-177">If so, the new input samples will use the new input format, so the MFT must keep track of the point when the format changed.</span></span>
5.  <span data-ttu-id="84f68-178">在 MFT 處理輸入類型變更之前所收到的所有範例之後， [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 會傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。</span><span class="sxs-lookup"><span data-stu-id="84f68-178">After the MFT processes all of the samples that it received before the input type changed, the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) returns **MF\_E\_TRANSFORM\_STREAM\_CHANGE**.</span></span>
6.  <span data-ttu-id="84f68-179">MFT 會使其目前的輸出類型失效，並更新可用輸出媒體類型的清單。</span><span class="sxs-lookup"><span data-stu-id="84f68-179">The MFT invalidates its current output type, and updates the list of available output media types.</span></span>
7.  <span data-ttu-id="84f68-180">如先前所述，用戶端會協商新的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="84f68-180">The client negotiates the new output type, as described previously.</span></span>

<span data-ttu-id="84f68-181">針對 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md)屬性，[非同步 MFTs](asynchronous-mfts.md)必須傳回 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="84f68-181">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE** for the [**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**](mft-support-dynamic-format-change-attribute.md) attribute.</span></span> <span data-ttu-id="84f68-182">使用非同步 MFT 時，用戶端可以假設 [ **MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更** ] 屬性設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="84f68-182">When using an asynchronous MFT, the client can assume that the **MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE** attribute is set to **TRUE**.</span></span>

<span data-ttu-id="84f68-183">當 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 為 **TRUE** 時，主要的差異在於，用戶端不需要在設定新的輸入類型之前清空 MFT。</span><span class="sxs-lookup"><span data-stu-id="84f68-183">When [**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**](mft-support-dynamic-format-change-attribute.md) is **TRUE**, the main difference is that the client is not required to drain the MFT before setting a new input type.</span></span> <span data-ttu-id="84f68-184">因此，當 MFT 在輸入範例上時，輸入類型可能會變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-184">As a result, the input type might change while the MFT is holding onto input samples.</span></span> <span data-ttu-id="84f68-185">請務必不要只卸載這些範例。</span><span class="sxs-lookup"><span data-stu-id="84f68-185">It is important that the MFT does not simply drop these samples.</span></span> <span data-ttu-id="84f68-186">此外，在 MFT 處理其所有快取的資料之前，輸出類型無法變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-186">Also, the output type cannot change until the MFT processes all of its cached data.</span></span>

<span data-ttu-id="84f68-187">先前的段落特別適用于影片解碼器，它可以從時態順序接收程式碼框架，因此需要加以快取。</span><span class="sxs-lookup"><span data-stu-id="84f68-187">The previous paragraph applies especially to video decoders, which can receive inter-coded frames out of temporal order, and thus need to cache them.</span></span> <span data-ttu-id="84f68-188">如果 MFT 未快取輸入範例，則清空其實是無作業。</span><span class="sxs-lookup"><span data-stu-id="84f68-188">If an MFT does not cache input samples, draining is essentially a no-op.</span></span> <span data-ttu-id="84f68-189">在此情況下，MFT 可以將 [**(\_ \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 為 **FALSE** ，或將屬性保留為未設定) 。</span><span class="sxs-lookup"><span data-stu-id="84f68-189">In that case, the MFT can set [**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**](mft-support-dynamic-format-change-attribute.md) to **FALSE** (or leave the attribute unset).</span></span>

<span data-ttu-id="84f68-190">此外，請注意，在清空之後，每個 MFT 都應該正確地處理格式變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-190">Also, note that every MFT is expected to handle format changes correctly after being drained.</span></span> <span data-ttu-id="84f68-191">[**Mft \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md)屬性指出 mft 是否支援格式變更，而不需要清空。</span><span class="sxs-lookup"><span data-stu-id="84f68-191">The [**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**](mft-support-dynamic-format-change-attribute.md) attribute indicates whether the MFT supports format changes without draining.</span></span>

## <a name="change-in-interlace-mode"></a><span data-ttu-id="84f68-192">以交錯模式變更</span><span class="sxs-lookup"><span data-stu-id="84f68-192">Change in Interlace Mode</span></span>

<span data-ttu-id="84f68-193">影片交錯模式中的變更是特殊案例，因為它們不會使目前的媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="84f68-193">Changes in the video interlacing mode are a special case, because they do not invalidate the current media type.</span></span> <span data-ttu-id="84f68-194">相反地，您可以藉由設定媒體範例上的屬性，為每個影片框架指定交錯模式。</span><span class="sxs-lookup"><span data-stu-id="84f68-194">Instead, the interlace mode is specified for each video frame by setting attributes on the media sample.</span></span> <span data-ttu-id="84f68-195">影片 MFT 應檢查每個輸入範例是否有這些旗標。</span><span class="sxs-lookup"><span data-stu-id="84f68-195">A video MFT should check each input sample for the presence of these flags.</span></span>

<span data-ttu-id="84f68-196">當欄位支配從最上層欄位切換至底部欄位，或影片在漸進式和交錯式圖片之間切換時，交錯模式可能會變更。</span><span class="sxs-lookup"><span data-stu-id="84f68-196">The interlace mode can change when the field dominance switches from top-field to bottom-field, or when the video switches between progressive and interlaced pictures.</span></span>

<span data-ttu-id="84f68-197">如需詳細資訊，請參閱 [在範例上交錯旗標](video-interlacing.md)。</span><span class="sxs-lookup"><span data-stu-id="84f68-197">For more information, see [Interlace Flags on Samples](video-interlacing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84f68-198">相關主題</span><span class="sxs-lookup"><span data-stu-id="84f68-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f68-199">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="84f68-199">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



