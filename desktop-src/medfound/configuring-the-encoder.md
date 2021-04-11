---
description: 編碼屬性
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: 編碼屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 093b72dc37501ca88882c6e3b530cda0eed1baa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111840"
---
# <a name="encoding-properties"></a><span data-ttu-id="624a3-103">編碼屬性</span><span class="sxs-lookup"><span data-stu-id="624a3-103">Encoding Properties</span></span>

<span data-ttu-id="624a3-104">Windows Media 音訊和 Windows Media 視訊編碼器支援各種編碼模式。</span><span class="sxs-lookup"><span data-stu-id="624a3-104">The Windows Media Audio and Windows Media Video encoders support a variety of encoding modes.</span></span> <span data-ttu-id="624a3-105">這些模式通常是藉由設定編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 的屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="624a3-105">These modes are generally configured by setting properties on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="624a3-106">若要執行檔案編碼，不論使用 WMContainer 層級元件或建立部分拓撲，您都必須根據編碼模式和資料流程的媒體類型設定屬性，以適當地設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="624a3-106">To perform file encoding, whether using WMContainer-level components or by building a partial topology, you must configure the encoder appropriately by setting properties depending on the mode of encoding and the media type of the stream.</span></span> <span data-ttu-id="624a3-107">您必須在編碼器和物件上設定相同的屬性集， (ASF 檔案接收或 ASF 多工器，) 您要用來寫入 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="624a3-107">The same set of properties must be set both on the encoder and the object (ASF file sink or ASF multiplexer) you are using to write the ASF file.</span></span>

<span data-ttu-id="624a3-108">編碼器屬性定義于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="624a3-108">The encoder properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="624a3-109">用來設定編碼器的特定屬性是使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的方法所設定。</span><span class="sxs-lookup"><span data-stu-id="624a3-109">The specific properties that are used to configure the encoder are set by using the methods of the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

-   [<span data-ttu-id="624a3-110">音訊串流屬性</span><span class="sxs-lookup"><span data-stu-id="624a3-110">Audio Stream Properties</span></span>](#audio-stream-properties)
-   [<span data-ttu-id="624a3-111">影片資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="624a3-111">Video Stream Properties</span></span>](#video-stream-properties)
-   [<span data-ttu-id="624a3-112">設定編碼器的屬性儲存區</span><span class="sxs-lookup"><span data-stu-id="624a3-112">Configuring the Encoder's Property Store</span></span>](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a><span data-ttu-id="624a3-113">音訊串流屬性</span><span class="sxs-lookup"><span data-stu-id="624a3-113">Audio Stream Properties</span></span>

<span data-ttu-id="624a3-114">下表顯示音訊串流的編碼器設定。</span><span class="sxs-lookup"><span data-stu-id="624a3-114">The following table shows the encoder configurations for an audio stream.</span></span>



| <span data-ttu-id="624a3-115">編碼類型</span><span class="sxs-lookup"><span data-stu-id="624a3-115">Encoding type</span></span>                                                                                        | <span data-ttu-id="624a3-116">屬性名稱-值</span><span class="sxs-lookup"><span data-stu-id="624a3-116">Property name - Value</span></span>                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="624a3-117">常數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-117">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="624a3-118">MFPKEY \_ VBRENABLED- **FALSE** (選擇性) 預設 \_ 會將 MFPKEY VBRENABLED 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="624a3-118">MFPKEY\_VBRENABLED - **FALSE** (Optional)By default, MFPKEY\_VBRENABLED is set to **FALSE**.</span></span><br/>                                                                                             |
| [<span data-ttu-id="624a3-119">以品質為基礎的變數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-119">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="624a3-120">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-120">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-121">MFPKEY \_ PASSESUSED-1 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="624a3-121">MFPKEY\_PASSESUSED - 1 (Optional)</span></span><br/> <span data-ttu-id="624a3-122">根據預設，MFPKEY \_ PASSESUSED 會設定為1。</span><span class="sxs-lookup"><span data-stu-id="624a3-122">By default, MFPKEY\_PASSESUSED is set to 1.</span></span><br/> <span data-ttu-id="624a3-123">MFPKEY \_ 所需 \_ 的 VBRQUALITY-從0到100</span><span class="sxs-lookup"><span data-stu-id="624a3-123">MFPKEY\_DESIRED\_VBRQUALITY - From 0 to 100</span></span><br/> |
| [<span data-ttu-id="624a3-124">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-124">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="624a3-125">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-125">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-126">MFPKEY \_ PASSESUSED-2</span><span class="sxs-lookup"><span data-stu-id="624a3-126">MFPKEY\_PASSESUSED - 2</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="624a3-127">尖峰限制的可變位速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-127">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="624a3-128">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-128">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-129">MFPKEY \_ PASSESUSED-2</span><span class="sxs-lookup"><span data-stu-id="624a3-129">MFPKEY\_PASSESUSED - 2</span></span><br/> <span data-ttu-id="624a3-130">MFPKEY \_ RMAX-最大位元速率</span><span class="sxs-lookup"><span data-stu-id="624a3-130">MFPKEY\_RMAX - Maximum bit rate</span></span><br/> <span data-ttu-id="624a3-131">MFPKEY \_ BMAX-最大緩衝區視窗</span><span class="sxs-lookup"><span data-stu-id="624a3-131">MFPKEY\_BMAX - Maximum buffer window</span></span><br/>                               |



 

### <a name="video-stream-properties"></a><span data-ttu-id="624a3-132">影片資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="624a3-132">Video Stream Properties</span></span>

<span data-ttu-id="624a3-133">下表顯示影片串流的編碼器設定。</span><span class="sxs-lookup"><span data-stu-id="624a3-133">The following table shows the encoder configurations for a video stream.</span></span>



| <span data-ttu-id="624a3-134">編碼類型</span><span class="sxs-lookup"><span data-stu-id="624a3-134">Encoding type</span></span>                                                                                        | <span data-ttu-id="624a3-135">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="624a3-135">Property name</span></span>                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="624a3-136">常數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-136">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="624a3-137">MFPKEY \_ VBRENABLED- **FALSE** (選用) </span><span class="sxs-lookup"><span data-stu-id="624a3-137">MFPKEY\_VBRENABLED - **FALSE** (Optional)</span></span><br/> <span data-ttu-id="624a3-138">根據預設，MFPKEY \_ VBRENABLED 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="624a3-138">By default, MFPKEY\_VBRENABLED is set to **FALSE**.</span></span><br/> <span data-ttu-id="624a3-139">MFPKEY \_ VIDEOWINDOW-緩衝區視窗</span><span class="sxs-lookup"><span data-stu-id="624a3-139">MFPKEY\_VIDEOWINDOW - Buffer window</span></span><br/>                                  |
| [<span data-ttu-id="624a3-140">以品質為基礎的變數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-140">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="624a3-141">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-141">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-142">MFPKEY \_ PASSESUSED-1 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="624a3-142">MFPKEY\_PASSESUSED - 1 (Optional)</span></span><br/> <span data-ttu-id="624a3-143">根據預設，MFPKEY \_ PASSESUSED 會設定為1。</span><span class="sxs-lookup"><span data-stu-id="624a3-143">By default, MFPKEY\_PASSESUSED is set to 1.</span></span><br/> <span data-ttu-id="624a3-144">MFPKEY \_ 所需 \_ 的 VBRQUALITY-從0到100</span><span class="sxs-lookup"><span data-stu-id="624a3-144">MFPKEY\_DESIRED\_VBRQUALITY - From 0 to 100</span></span><br/> |
| [<span data-ttu-id="624a3-145">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-145">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="624a3-146">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-146">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-147">MFPKEY \_ PASSESUSED-2</span><span class="sxs-lookup"><span data-stu-id="624a3-147">MFPKEY\_PASSESUSED - 2</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="624a3-148">尖峰限制的可變位速率編碼</span><span class="sxs-lookup"><span data-stu-id="624a3-148">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="624a3-149">MFPKEY \_ VBRENABLED- **TRUE**</span><span class="sxs-lookup"><span data-stu-id="624a3-149">MFPKEY\_VBRENABLED - **TRUE**</span></span><br/> <span data-ttu-id="624a3-150">MFPKEY \_ PASSESUSED-2</span><span class="sxs-lookup"><span data-stu-id="624a3-150">MFPKEY\_PASSESUSED - 2</span></span><br/> <span data-ttu-id="624a3-151">MFPKEY \_ RMAX-最大位元速率</span><span class="sxs-lookup"><span data-stu-id="624a3-151">MFPKEY\_RMAX - Maximum bit rate</span></span><br/> <span data-ttu-id="624a3-152">MFPKEY \_ BMAX-最大緩衝區視窗</span><span class="sxs-lookup"><span data-stu-id="624a3-152">MFPKEY\_BMAX - Maximum buffer window</span></span><br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a><span data-ttu-id="624a3-153">設定編碼器的屬性儲存區</span><span class="sxs-lookup"><span data-stu-id="624a3-153">Configuring the Encoder's Property Store</span></span>

<span data-ttu-id="624a3-154">您必須在編碼會話之前，指定編碼類型和各種資料流程特定設定，以設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="624a3-154">You must configure an encoder by specifying the type of encoding and the various stream-specific settings before the encoding session.</span></span> <span data-ttu-id="624a3-155">您也必須在 [ASF ContentInfo 物件](asf-contentinfo-object.md) 的屬性存放區中設定編碼器屬性，該物件代表輸出檔案的 Asf 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="624a3-155">You must also set the encoder properties in the property store of an [ASF ContentInfo Object](asf-contentinfo-object.md) that represents the ASF Header Object of the output file.</span></span>

<span data-ttu-id="624a3-156">如果您使用編碼器 MFT：</span><span class="sxs-lookup"><span data-stu-id="624a3-156">If you are using an encoder MFT:</span></span>

1.  <span data-ttu-id="624a3-157">取得編碼器 MFT [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的參考，如 [使用編碼器的 IMFTransform 介面](using-an-encoder-s-imftransform--interface.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="624a3-157">Get a reference to the encoder MFT's [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface as described in [Using an Encoder's IMFTransform Interface](using-an-encoder-s-imftransform--interface.md).</span></span>
2.  <span data-ttu-id="624a3-158">查詢編碼器 MFT 以取得 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="624a3-158">Querying the encoder MFT for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="624a3-159">藉由呼叫 **IPropertyStore：： SetValue** 來設定必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="624a3-159">Setting the required properties by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="624a3-160">如果您使用內建的編碼器啟用物件，並已建立已設定的 ASF 檔案接收，則可以將 ASF 媒體接收器的屬性存放區傳遞給 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)。</span><span class="sxs-lookup"><span data-stu-id="624a3-160">If you are using the built-in encoder activation objects and have already created an configured the ASF file sink, you can pass the ASF media sink's property store to [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span> <span data-ttu-id="624a3-161">編碼器會根據應用程式所指定的設定自動設定。</span><span class="sxs-lookup"><span data-stu-id="624a3-161">The encoder is configured automatically based on the settings specified by the application.</span></span> <span data-ttu-id="624a3-162">如需詳細資訊，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)中所述的程式。</span><span class="sxs-lookup"><span data-stu-id="624a3-162">For more information, see the procedure described in [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="624a3-163">如需使用啟用物件建立媒體基礎物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="624a3-163">For more information about creating Media Foundation objects by using activation objects, see [Activation Objects](activation-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="624a3-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="624a3-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="624a3-165">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="624a3-165">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="624a3-166">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="624a3-166">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
