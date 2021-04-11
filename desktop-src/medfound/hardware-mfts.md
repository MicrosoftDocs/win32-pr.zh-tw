---
description: 本主題說明如何撰寫媒體基礎轉換 (MFT) ，作為硬體編碼器、解碼器或數位訊號處理器 (DSP) 的 proxy。
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: 硬體 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191710"
---
# <a name="hardware-mfts"></a><span data-ttu-id="0e395-103">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="0e395-103">Hardware MFTs</span></span>

> [!Note]  
> <span data-ttu-id="0e395-104">本主題適用于 Windows 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0e395-104">This topic applies to Windows 7 or later.</span></span>

 

<span data-ttu-id="0e395-105">本主題說明如何撰寫媒體基礎轉換 (MFT) ，作為硬體編碼器、解碼器或數位訊號處理器 (DSP) 的 proxy。</span><span class="sxs-lookup"><span data-stu-id="0e395-105">This topic describes how to write a Media Foundation transform (MFT) that acts as a proxy to a hardware encoder, decoder, or digital signal processor (DSP).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e395-106">如果硬體編解碼器使用 AVStream 多媒體類別驅動程式，則不需要自訂的 MFT。</span><span class="sxs-lookup"><span data-stu-id="0e395-106">If a hardware codec uses the AVStream multimedia class driver, it does not require a custom MFT.</span></span> <span data-ttu-id="0e395-107">媒體基礎為此用途提供 AVStream proxy。</span><span class="sxs-lookup"><span data-stu-id="0e395-107">Media Foundation provides an AVStream proxy for this purpose.</span></span> <span data-ttu-id="0e395-108">本主題中的資訊僅適用于硬體編解碼器未使用 AVStream 的特殊情況。</span><span class="sxs-lookup"><span data-stu-id="0e395-108">The information in this topic applies only in the special case where the hardware codec does not use AVStream.</span></span> <span data-ttu-id="0e395-109">如需詳細資訊，請參閱 [AVStream 中的硬體編解碼器支援](https://msdn.microsoft.com/library/dd568169.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0e395-109">For more information, see [Hardware Codec Support in AVStream](https://msdn.microsoft.com/library/dd568169.aspx).</span></span>

 

<span data-ttu-id="0e395-110">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="0e395-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0e395-111">簡介</span><span class="sxs-lookup"><span data-stu-id="0e395-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0e395-112">硬體 MFT 屬性</span><span class="sxs-lookup"><span data-stu-id="0e395-112">Hardware MFT Attributes</span></span>](#hardware-mft-attributes)
-   [<span data-ttu-id="0e395-113">硬體交握順序</span><span class="sxs-lookup"><span data-stu-id="0e395-113">Hardware Handshake Sequence</span></span>](#hardware-handshake-sequence)
-   [<span data-ttu-id="0e395-114">資料處理</span><span class="sxs-lookup"><span data-stu-id="0e395-114">Data Processing</span></span>](#data-processing)
-   [<span data-ttu-id="0e395-115">配對的解碼器/編碼器</span><span class="sxs-lookup"><span data-stu-id="0e395-115">Paired Decoder/Encoder</span></span>](#paired-decoderencoder)
-   [<span data-ttu-id="0e395-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e395-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0e395-117">簡介</span><span class="sxs-lookup"><span data-stu-id="0e395-117">Introduction</span></span>

<span data-ttu-id="0e395-118">任何不是以 AVStream 為基礎的硬體編解碼器都必須提供自己的 MFT 作為驅動程式的 proxy。</span><span class="sxs-lookup"><span data-stu-id="0e395-118">Any hardware codec that is not based on AVStream must provide its own MFT to act as a proxy to the driver.</span></span> <span data-ttu-id="0e395-119">硬體編解碼器可能包含數個不同的功能區塊：</span><span class="sxs-lookup"><span data-stu-id="0e395-119">A hardware codec might incorporate several distinct functional blocks:</span></span>

-   <span data-ttu-id="0e395-120">編碼器</span><span class="sxs-lookup"><span data-stu-id="0e395-120">Encoder</span></span>
-   <span data-ttu-id="0e395-121">解碼器</span><span class="sxs-lookup"><span data-stu-id="0e395-121">Decoder</span></span>
-   <span data-ttu-id="0e395-122">框架縮放/格式轉換</span><span class="sxs-lookup"><span data-stu-id="0e395-122">Frame scaling/format conversion</span></span>

<span data-ttu-id="0e395-123">這些函式都應該由個別的 MFT 管理。</span><span class="sxs-lookup"><span data-stu-id="0e395-123">Each of these functions should be managed by a separate MFT.</span></span> <span data-ttu-id="0e395-124">硬體 MFT 絕對不能做為多用途的「轉碼程式」。</span><span class="sxs-lookup"><span data-stu-id="0e395-124">A hardware MFT should never act as a multi-purpose "transcoder."</span></span> <span data-ttu-id="0e395-125">相反地，請將編碼函式放入編碼器 MFT，然後將函式解碼成解碼器 MFT。</span><span class="sxs-lookup"><span data-stu-id="0e395-125">Instead, put encoding functions into an encoder MFT and decoding functions into a decoder MFT.</span></span> <span data-ttu-id="0e395-126">如果硬體提供畫面縮放和格式轉換，請將這些函式放在個別的視頻處理器中，並在 [ **MFT \_ 類別的 \_ 視頻 \_ 處理器** ] 類別中註冊。</span><span class="sxs-lookup"><span data-stu-id="0e395-126">If the hardware offers frame scaling and format conversions, place those functions in a separate video processor, registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span> <span data-ttu-id="0e395-127">如果硬體不支援框架縮放或格式轉換，媒體基礎提供軟體視頻處理器。</span><span class="sxs-lookup"><span data-stu-id="0e395-127">If the hardware does not support frame scaling or format conversion, Media Foundation provides a software video processor.</span></span>

<span data-ttu-id="0e395-128">硬體 MFTs 具有下列一般需求：</span><span class="sxs-lookup"><span data-stu-id="0e395-128">Hardware MFTs have the following general requirements:</span></span>

-   <span data-ttu-id="0e395-129">硬體 MFTs 必須使用新的非同步處理模型，如 [非同步 MFTs](asynchronous-mfts.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="0e395-129">Hardware MFTs must use the new asynchronous processing model, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>
-   <span data-ttu-id="0e395-130">硬體 MFTs 必須支援動態格式變更，如 [動態格式變更](basic-mft-processing-model.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="0e395-130">Hardware MFTs must support dynamic format changes, as described in [Dynamic Format Changes](basic-mft-processing-model.md).</span></span>

## <a name="hardware-mft-attributes"></a><span data-ttu-id="0e395-131">硬體 MFT 屬性</span><span class="sxs-lookup"><span data-stu-id="0e395-131">Hardware MFT Attributes</span></span>

<span data-ttu-id="0e395-132">硬體 MFT 必須執行下列與屬性相關的方法：</span><span class="sxs-lookup"><span data-stu-id="0e395-132">A hardware MFT must implement following methods related to attributes:</span></span>

-   <span data-ttu-id="0e395-133">[**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)：傳回全域 MFT 屬性的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="0e395-133">[**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): Returns an attribute store for global MFT attributes.</span></span>
-   <span data-ttu-id="0e395-134">[**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)：傳回輸入資料流程的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="0e395-134">[**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): Returns an attribute store for an input stream.</span></span>
-   <span data-ttu-id="0e395-135">[**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)：傳回輸出資料流程的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="0e395-135">[**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): Returns an attribute store for an output stream.</span></span>

<span data-ttu-id="0e395-136">第一次建立 MFT 時，它必須在自己的全域屬性存放區上設定下列屬性 (也就是 [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)) 所傳回的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="0e395-136">When the MFT is first created, it must set the following attributes on its own global attribute store (that is, the attribute store returned by [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):</span></span>



| <span data-ttu-id="0e395-137">屬性</span><span class="sxs-lookup"><span data-stu-id="0e395-137">Attribute</span></span>                                                                                    | <span data-ttu-id="0e395-138">描述</span><span class="sxs-lookup"><span data-stu-id="0e395-138">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e395-139">MF \_ 轉換 \_ 非同步</span><span class="sxs-lookup"><span data-stu-id="0e395-139">MF\_TRANSFORM\_ASYNC</span></span>](mf-transform-async.md)                                               | <span data-ttu-id="0e395-140">必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0e395-140">Must be set to **TRUE**.</span></span> <span data-ttu-id="0e395-141">指出 MFT 會執行非同步處理。</span><span class="sxs-lookup"><span data-stu-id="0e395-141">Indicates that the MFT performs asynchronous processing.</span></span>                                                                                                      |
| [<span data-ttu-id="0e395-142">MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="0e395-142">MFT\_ENUM\_HARDWARE\_URL\_Attribute</span></span>](mft-enum-hardware-url-attribute.md)                   | <span data-ttu-id="0e395-143">包含硬體裝置的符號連結。</span><span class="sxs-lookup"><span data-stu-id="0e395-143">Contains the symbolic link for the hardware device.</span></span><br/> <span data-ttu-id="0e395-144">拓撲載入器會使用此屬性的存在，來測試 MFT 是否代表硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="0e395-144">The topology loader uses the presence of this attribute to test whether an MFT represents a hardware device.</span></span><br/> |
| [<span data-ttu-id="0e395-145">**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="0e395-145">**MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE**</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="0e395-146">必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0e395-146">Must be set to **TRUE**.</span></span> <span data-ttu-id="0e395-147">指出此 MFT 支援動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="0e395-147">Indicates that the MFT supports dynamic format changes.</span></span>                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a><span data-ttu-id="0e395-148">硬體交握順序</span><span class="sxs-lookup"><span data-stu-id="0e395-148">Hardware Handshake Sequence</span></span>

<span data-ttu-id="0e395-149">如果兩個 MFTs 代表相同的實體裝置，則它們可以交換硬體內的資料（例如，透過硬體匯流排）。</span><span class="sxs-lookup"><span data-stu-id="0e395-149">If two MFTs represent the same physical device, they can exchange data within the hardware—for example, over a hardware bus.</span></span> <span data-ttu-id="0e395-150">不需要將資料複製到系統記憶體中，然後再複製到裝置上。</span><span class="sxs-lookup"><span data-stu-id="0e395-150">There is no need to copy the data into system memory and then back to the device.</span></span>

<span data-ttu-id="0e395-151">在下圖中，標示為 "A" 和 "B" 的 MFTs 代表相同硬體內的功能區塊。</span><span class="sxs-lookup"><span data-stu-id="0e395-151">In the following diagram, the MFTs labeled "A" and "B" represent functional blocks within the same hardware.</span></span> <span data-ttu-id="0e395-152">例如，在轉碼案例中，「A」可能代表硬體解碼，而「B」可能代表硬體編碼器。</span><span class="sxs-lookup"><span data-stu-id="0e395-152">For example, in a transcoding scenario, "A" might represent a hardware decoder and "B" might represent a hardware encoder.</span></span> <span data-ttu-id="0e395-153">"A" 和 "B" 之間的資料流程發生于硬體內。</span><span class="sxs-lookup"><span data-stu-id="0e395-153">The data flow between "A" and "B" occurs within the hardware.</span></span> <span data-ttu-id="0e395-154">標示為 "C" 的 MFT 是軟體 MFT。</span><span class="sxs-lookup"><span data-stu-id="0e395-154">The MFT labeled "C" is a software MFT.</span></span> <span data-ttu-id="0e395-155">從 "B" 到 "C" 的資料流程會使用系統記憶體。</span><span class="sxs-lookup"><span data-stu-id="0e395-155">Data flow from "B" to "C" uses system memory.</span></span>

![圖表顯示標示為 a 到 c 的方塊，以及硬體編解碼器：指向 b 和編解碼器的點、編解碼器指向 b，而 b 指向 c](images/proxy-mft.png)

<span data-ttu-id="0e395-157">若要建立硬體連線，這兩個硬體 MFTs 必須使用私用通道。</span><span class="sxs-lookup"><span data-stu-id="0e395-157">To establish a hardware connection, the two hardware MFTs must use a private communication channel.</span></span> <span data-ttu-id="0e395-158">此連接是在格式協商期間建立，在設定媒體類型之前，以及在第一次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)之前建立。</span><span class="sxs-lookup"><span data-stu-id="0e395-158">This connection is established during format negotiation, before the media types are set and before the first call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="0e395-159">連接程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="0e395-159">The connection process works as follows:</span></span>

1.  <span data-ttu-id="0e395-160">拓撲載入器會檢查兩個 MFTs 是否有 [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e395-160">The topology loader checks both MFTs for the presence of the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute.</span></span> <span data-ttu-id="0e395-161">請注意，它不會檢查這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0e395-161">Note that it does not examine the value of this attribute.</span></span>
2.  <span data-ttu-id="0e395-162">如果兩個 MFTs 都有 [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) ，拓撲載入器會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="0e395-162">If [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) is present on both MFTs, the topology loader does the following:</span></span>
    1.  <span data-ttu-id="0e395-163">拓撲載入器會在上游 MFT 上呼叫 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) () 。</span><span class="sxs-lookup"><span data-stu-id="0e395-163">The topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT (A).</span></span> <span data-ttu-id="0e395-164">這個方法會傳回 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="0e395-164">This method returns an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span> <span data-ttu-id="0e395-165">讓此指標以 *pUpstream* 表示。</span><span class="sxs-lookup"><span data-stu-id="0e395-165">Let this pointer be denoted *pUpstream*.</span></span>
    2.  <span data-ttu-id="0e395-166">拓撲載入器會在下游 MFT (B) 上呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 。</span><span class="sxs-lookup"><span data-stu-id="0e395-166">The topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT (B).</span></span> <span data-ttu-id="0e395-167">此呼叫也會傳回 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="0e395-167">This call also returns an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span> <span data-ttu-id="0e395-168">讓此指標以 *pDownstream* 表示。</span><span class="sxs-lookup"><span data-stu-id="0e395-168">Let this pointer be denoted *pDownstream*.</span></span>
    3.  <span data-ttu-id="0e395-169">拓撲載入器會藉由呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)，在 *PDownstream* 上設定 [MFT \_ 連線 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="0e395-169">The topology loader sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on *pDownstream* by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="0e395-170">屬性的值是 *pUpstream* 指標。</span><span class="sxs-lookup"><span data-stu-id="0e395-170">The value of the attribute is the *pUpstream* pointer.</span></span>
    4.  <span data-ttu-id="0e395-171">拓撲載入器會在 *pDownstream* 和 *pUpstream* 上將 [ \_ 連接 \_ 至 \_ HW \_ STREAM](mft-connected-to-hw-stream.md)屬性的 MFT 設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0e395-171">The topology loader sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both *pDownstream* and *pUpstream*.</span></span>
3.  <span data-ttu-id="0e395-172">此時，下游 MFT 具有上游 MFT 屬性存放區的指標，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0e395-172">At this point, the downstream MFT has a pointer to the upstream MFT's attribute store, as shown in the following diagram.</span></span>

    ![每個 mfts 指向其資料流程、指向其存放區的每個資料流程，以及輸出存放區中有虛線的輸入存放區的圖表](images/proxy-mft2.png)

    > [!Note]  
    > <span data-ttu-id="0e395-174">為了清楚起見，此圖表會將資料流程和屬性存放區顯示為不同的物件，但不需要執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="0e395-174">For clarity, this diagram shows the streams and the attribute stores as distinct objects, but that is not required for the implementation.</span></span>

     

4.  <span data-ttu-id="0e395-175">下游 MFT 會使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標來建立與上游 mft 之間的私人通道。</span><span class="sxs-lookup"><span data-stu-id="0e395-175">The downstream MFT uses the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to establish a private communication channel with the upstream MFT.</span></span> <span data-ttu-id="0e395-176">因為通道是私用的，所以確切的機制是由實作為定義。</span><span class="sxs-lookup"><span data-stu-id="0e395-176">Because the channel is private, the exact mechanism is defined by the implementation.</span></span> <span data-ttu-id="0e395-177">例如，MFT 可能會查詢私用 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0e395-177">For example, the MFT might query for a private COM interface.</span></span>

<span data-ttu-id="0e395-178">在步驟4中，下游 MFT 必須確認兩個 MFTs 是否共用相同的實體裝置。</span><span class="sxs-lookup"><span data-stu-id="0e395-178">During step 4, the downstream MFT must verify whether the two MFTs share the same physical device.</span></span> <span data-ttu-id="0e395-179">如果沒有，則必須切換回使用系統記憶體進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="0e395-179">If not, they must fall back to using system memory for data transport.</span></span> <span data-ttu-id="0e395-180">這可讓 MFT 在軟體 MFTs 和其他硬體裝置上正確運作。</span><span class="sxs-lookup"><span data-stu-id="0e395-180">This enables the MFT to operate correctly with software MFTs and other hardware devices.</span></span>

<span data-ttu-id="0e395-181">如果交握成功，而且兩個 MFTs 共用私用資料通道，則不會使用標準資料處理模型 (下一節) 在連接點中所述。</span><span class="sxs-lookup"><span data-stu-id="0e395-181">If the handshake succeeds and the two MFTs share a private data channel, they do not use the standard data processing model (described in the next section) at the connection point.</span></span> <span data-ttu-id="0e395-182">具體而言，下游 MFT 不會傳送 [METransformNeedInput](metransformneedinput.md) 事件;如需詳細資訊，請參閱本主題的下一節。</span><span class="sxs-lookup"><span data-stu-id="0e395-182">Specifically, the downstream MFT does not send [METransformNeedInput](metransformneedinput.md) events; for more details, refer to the next section in this topic.</span></span>

## <a name="data-processing"></a><span data-ttu-id="0e395-183">資料處理</span><span class="sxs-lookup"><span data-stu-id="0e395-183">Data Processing</span></span>

<span data-ttu-id="0e395-184">當硬體 MFT 使用系統記憶體進行資料傳輸時，此程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="0e395-184">When a hardware MFT uses system memory for data transport, the process works as follows:</span></span>

1.  <span data-ttu-id="0e395-185">為了要求更多輸入，MFT 會傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0e395-185">To request more input, the MFT sends an [METransformNeedInput](metransformneedinput.md) event.</span></span>
2.  <span data-ttu-id="0e395-186">[METransformNeedInput](metransformneedinput.md)事件會導致管線呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)。</span><span class="sxs-lookup"><span data-stu-id="0e395-186">The [METransformNeedInput](metransformneedinput.md) event causes the pipeline to call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>
3.  <span data-ttu-id="0e395-187">當 MFT 有輸出資料時，MFT 會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0e395-187">When the MFT has output data, the MFT sends an [METransformHaveOutput](metransformhaveoutput.md) event.</span></span>
4.  <span data-ttu-id="0e395-188">[METransformHaveOutput](metransformhaveoutput.md)事件會導致管線呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="0e395-188">The [METransformHaveOutput](metransformhaveoutput.md) event causes the pipeline to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span>

<span data-ttu-id="0e395-189">如需詳細資訊，請參閱 [非同步 MFTs](asynchronous-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="0e395-189">For details, refer to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

<span data-ttu-id="0e395-190">但是，如果 MFT 使用硬體通道，它就不會在硬體連接點傳送這些事件，因為所有資料傳輸都是在硬體內部發生。</span><span class="sxs-lookup"><span data-stu-id="0e395-190">If the MFT uses a hardware channel, however, it does not send these events at the hardware connection point, because all data transfer happens internally within the hardware.</span></span> <span data-ttu-id="0e395-191">因此，管線不會在連接點呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 或 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="0e395-191">Therefore, the pipeline does not call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) or [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) at the connection point.</span></span>

<span data-ttu-id="0e395-192">例如，請考慮本主題中的第一個圖表。</span><span class="sxs-lookup"><span data-stu-id="0e395-192">For example, consider the first diagram in this topic.</span></span> <span data-ttu-id="0e395-193">在此設定中，資料處理會如下所示：</span><span class="sxs-lookup"><span data-stu-id="0e395-193">Given this configuration, data processing would occur as follows:</span></span>

1.  <span data-ttu-id="0e395-194">「A」會傳送 [METransformNeedInput](metransformneedinput.md) 來要求資料。</span><span class="sxs-lookup"><span data-stu-id="0e395-194">"A" sends [METransformNeedInput](metransformneedinput.md) to request data.</span></span>
2.  <span data-ttu-id="0e395-195">管線會在 "A" 上呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 。</span><span class="sxs-lookup"><span data-stu-id="0e395-195">The pipeline calls [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) on "A".</span></span>
3.  <span data-ttu-id="0e395-196">"A" 和 "B" 處理硬體中的資料。</span><span class="sxs-lookup"><span data-stu-id="0e395-196">"A" and "B" process the data in hardware.</span></span>
4.  <span data-ttu-id="0e395-197">當處理完成時，"B" 會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0e395-197">When the processing is complete, "B" sends an [METransformHaveOutput](metransformhaveoutput.md) event.</span></span>
5.  <span data-ttu-id="0e395-198">管線會在 "B" 上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="0e395-198">The pipeline calls [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on "B".</span></span>

## <a name="paired-decoderencoder"></a><span data-ttu-id="0e395-199">配對的解碼器/編碼器</span><span class="sxs-lookup"><span data-stu-id="0e395-199">Paired Decoder/Encoder</span></span>

<span data-ttu-id="0e395-200">如果解碼器和編碼器都位於相同的硬體晶片上，則在轉碼時最好將它們一起使用。</span><span class="sxs-lookup"><span data-stu-id="0e395-200">If a decoder and encoder are located on the same hardware chip, it may be preferable to use them together when transcoding.</span></span> <span data-ttu-id="0e395-201">也就是說，選取其中一個應該會導致在轉碼管線中選取另一個。</span><span class="sxs-lookup"><span data-stu-id="0e395-201">That is, selecting one should cause the other to be selected in the transcoding pipeline.</span></span> <span data-ttu-id="0e395-202">為了確保已選擇相符的硬體編解碼器，這兩個編解碼器 MFTs 應該提供自訂媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0e395-202">To ensure that matching hardware codecs are chosen, both codec MFTs should offer a custom media type.</span></span> <span data-ttu-id="0e395-203">若要建立自訂媒體類型：</span><span class="sxs-lookup"><span data-stu-id="0e395-203">To create a custom media type:</span></span>

-   <span data-ttu-id="0e395-204">視需要將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為 **MFMediaType \_ 音訊** 或 **MFMediaType \_ 影片**。</span><span class="sxs-lookup"><span data-stu-id="0e395-204">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio** or **MFMediaType\_Video**, as appropriate.</span></span>
-   <span data-ttu-id="0e395-205">將 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性設定為自訂 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="0e395-205">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to a custom GUID value.</span></span>

<span data-ttu-id="0e395-206">其他類型屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0e395-206">Other type attributes are optional.</span></span> <span data-ttu-id="0e395-207">此解碼器會從其 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)傳回自訂類型，而編碼器會從其 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 方法傳回自訂類型。</span><span class="sxs-lookup"><span data-stu-id="0e395-207">The decoder returns the custom type from its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), and the encoder returns the custom type from its [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method.</span></span> <span data-ttu-id="0e395-208">在這兩種情況下，自訂類型都必須是清單中的第一個專案 (*dwTypeIndex* = 0) 。</span><span class="sxs-lookup"><span data-stu-id="0e395-208">In both cases, the custom type must be the first entry in the list (*dwTypeIndex* = 0).</span></span>

<span data-ttu-id="0e395-209">若要使用軟體編解碼器，編解碼器應該也會傳回至少一個標準格式，例如影片的 NV12。</span><span class="sxs-lookup"><span data-stu-id="0e395-209">To work with software codecs, the codec should also return at least one standard format, such as NV12 for video.</span></span> <span data-ttu-id="0e395-210">標準格式應出現在自訂類型 (*dwTypeIndex* > 0) 之後。</span><span class="sxs-lookup"><span data-stu-id="0e395-210">Standard formats should appear after the custom type (*dwTypeIndex* > 0).</span></span> <span data-ttu-id="0e395-211">如果這兩個編解碼器必須永遠配對且無法與軟體編解碼器交互操作，則 MFTs 只會傳回自訂格式，而不會傳回任何標準格式。</span><span class="sxs-lookup"><span data-stu-id="0e395-211">If the two codecs must always be paired and cannot interoperate with software codecs, the MFTs should return only the custom format and not return any standard formats.</span></span>

> [!Note]  
> <span data-ttu-id="0e395-212">如果解碼器沒有傳回任何標準格式，它就無法用於使用 [增強型影片](enhanced-video-renderer.md)轉譯器進行播放。</span><span class="sxs-lookup"><span data-stu-id="0e395-212">If a decoder does not return any standard formats, it cannot be used for playback with the [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span> <span data-ttu-id="0e395-213">在此情況下，它應該註冊為僅限轉碼的解碼器。</span><span class="sxs-lookup"><span data-stu-id="0e395-213">In that case, it should be registered as a transcode-only decoder.</span></span> <span data-ttu-id="0e395-214">請參閱 [僅限轉碼的解碼器](implementing-a-codec-mft.md)。</span><span class="sxs-lookup"><span data-stu-id="0e395-214">See [Transcode-Only Decoders](implementing-a-codec-mft.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0e395-215">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e395-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e395-216">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="0e395-216">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> <dt>

[<span data-ttu-id="0e395-217">執行編解碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="0e395-217">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
</dt> <dt>

[<span data-ttu-id="0e395-218">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="0e395-218">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




