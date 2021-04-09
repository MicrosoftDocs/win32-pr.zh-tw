---
description: 交錯式影片編碼
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: '交錯式影片編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fafacb56f29964e81b040c59cdb75d8ebb35830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945086"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a><span data-ttu-id="d6f67-103">交錯式影片編碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="d6f67-103">Interlaced Video Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="d6f67-104">用於電腦的影片資料通常是 *漸進式* 的，這表示每個畫面格都會編碼為單一影像。</span><span class="sxs-lookup"><span data-stu-id="d6f67-104">Video data intended for use with computers is typically *progressive*, meaning that each frame is encoded as a single image.</span></span> <span data-ttu-id="d6f67-105">有些裝置（像是電視）不會一次顯示一個框架，而是兩個影像。</span><span class="sxs-lookup"><span data-stu-id="d6f67-105">Some devices, like televisions, do not display a frame all at once, but as two images.</span></span> <span data-ttu-id="d6f67-106">其中一個影像或欄位包含所有偶數的資料列。</span><span class="sxs-lookup"><span data-stu-id="d6f67-106">One of the images, or fields, contains all of the even numbered rows.</span></span> <span data-ttu-id="d6f67-107">另一個欄位包含所有奇數編號資料列的資料。</span><span class="sxs-lookup"><span data-stu-id="d6f67-107">The other field contains the data for all of the odd numbered rows.</span></span> <span data-ttu-id="d6f67-108">針對每個畫面格使用多個欄位編碼的影片稱為交錯式，因為它是透過在偶數位段和奇數位段之間切換來呈現。</span><span class="sxs-lookup"><span data-stu-id="d6f67-108">Video encoded with more than one field per frame is called interlaced, because it is rendered by switching between the even field and the odd field.</span></span>

<span data-ttu-id="d6f67-109">在過去，交錯式影片內容在使用 Windows Media 視訊編解碼器進行編碼之前，一律會先取消交錯。</span><span class="sxs-lookup"><span data-stu-id="d6f67-109">In the past, interlaced video content was always de-interlaced before encoding with the Windows Media Video codec.</span></span> <span data-ttu-id="d6f67-110">不過，從 Windows Media 9 系列開始，影片編碼器支援壓縮交錯內容，而不需要先將它轉換成漸進式內容。</span><span class="sxs-lookup"><span data-stu-id="d6f67-110">Beginning with Windows Media 9 Series, however, the video encoder supports compression of interlaced content without first converting it to progressive.</span></span> <span data-ttu-id="d6f67-111">如果內容是在交錯顯示（例如電視）上轉譯，則維護編碼檔案中的交錯是很重要的。</span><span class="sxs-lookup"><span data-stu-id="d6f67-111">Maintaining interlacing in an encoded file is important if the content is ever rendered on an interlaced display, such as a television.</span></span> <span data-ttu-id="d6f67-112">這項功能的重要性很高，因為支援 Windows Media 內容散佈至 DVD 播放機、機上盒和其他家用電子產品。</span><span class="sxs-lookup"><span data-stu-id="d6f67-112">This feature is of increasing importance, as support for Windows Media-based content spreads to DVD players, set-top boxes, and other home electronics.</span></span>

<span data-ttu-id="d6f67-113">編碼和提供交錯式影片最簡單的方式，就是使用 Windows Media 格式 SDK 來開發應用程式，並將內容儲存在 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="d6f67-113">The easiest way to encode and deliver interlaced video is to develop your application using the Windows Media Format SDK and storing the content in ASF files.</span></span> <span data-ttu-id="d6f67-114">有關框架的交錯式資訊會使用資料單位延伸模組傳遞給編解碼器，這適用于 ASF 內容，但在其他容器中的支援也比較棘手。</span><span class="sxs-lookup"><span data-stu-id="d6f67-114">The interlaced information about frames is passed to the codec using data unit extensions, which work well for ASF content, but are a little trickier to support in other containers.</span></span> <span data-ttu-id="d6f67-115">如需有關資料單位延伸的詳細資訊，請參閱 [使用資料單位延伸](usingdataunitextensions.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f67-115">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="d6f67-116">為了支援交錯編碼，需要兩個主要步驟：將畫面格資訊取得至編碼器，並將資訊傳遞至轉譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="d6f67-116">To support interlaced encoding involves two major steps: getting the frame information to the encoder, and delivering the information to the rendering application.</span></span> <span data-ttu-id="d6f67-117">下列段落會描述這些步驟。</span><span class="sxs-lookup"><span data-stu-id="d6f67-117">These steps are described in the following paragraphs.</span></span>

## <a name="interlaced-video-and-the-encoder"></a><span data-ttu-id="d6f67-118">交錯式影片和編碼器</span><span class="sxs-lookup"><span data-stu-id="d6f67-118">Interlaced Video and the Encoder</span></span>

<span data-ttu-id="d6f67-119">編碼影片的第一個步驟是使用維護的交錯，將編碼器設定成將交錯欄位編碼。</span><span class="sxs-lookup"><span data-stu-id="d6f67-119">The first step in encoding video with maintained interlacing is to configure the encoder to encode interlaced fields.</span></span> <span data-ttu-id="d6f67-120">若要這樣做，請將 [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d6f67-120">To do this, set the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property to **TRUE**.</span></span> <span data-ttu-id="d6f67-121">這會準備編碼器以接收交錯式範例。</span><span class="sxs-lookup"><span data-stu-id="d6f67-121">This prepares the encoder to receive interlaced samples.</span></span> <span data-ttu-id="d6f67-122">每個輸入範例都必須包含這兩個欄位。</span><span class="sxs-lookup"><span data-stu-id="d6f67-122">Each input sample must contain both fields.</span></span>

<span data-ttu-id="d6f67-123">啟用交錯編碼之後，您使用編碼器處理的每個範例都應該已附加資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="d6f67-123">Each sample that you process with the encoder after activating interlaced encoding should have a data unit extension attached.</span></span> <span data-ttu-id="d6f67-124">沒有預期資料單位延伸的範例會假設為漸進式。</span><span class="sxs-lookup"><span data-stu-id="d6f67-124">Samples without the expected data unit extension are assumed to be progressive.</span></span> <span data-ttu-id="d6f67-125">識別延伸模組的 GUID 是 D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC。</span><span class="sxs-lookup"><span data-stu-id="d6f67-125">The GUID identifying the extension is D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC.</span></span> <span data-ttu-id="d6f67-126">下表定義了 Windows Media Format SDK 的物件所傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="d6f67-126">The values passed by the objects of the Windows Media Format SDK are defined in the following table.</span></span>



| <span data-ttu-id="d6f67-127">值</span><span class="sxs-lookup"><span data-stu-id="d6f67-127">Value</span></span>      | <span data-ttu-id="d6f67-128">描述</span><span class="sxs-lookup"><span data-stu-id="d6f67-128">Description</span></span>                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f67-129">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d6f67-129">0x00000020</span></span> | <span data-ttu-id="d6f67-130">指定範例先以底部欄位編碼。</span><span class="sxs-lookup"><span data-stu-id="d6f67-130">Specifies that the sample is encoded with the bottom field first.</span></span> <span data-ttu-id="d6f67-131">此值只有在結合交錯值時才有意義。</span><span class="sxs-lookup"><span data-stu-id="d6f67-131">This value is only meaningful when combined with the interlaced value.</span></span> |
| <span data-ttu-id="d6f67-132">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d6f67-132">0x00000040</span></span> | <span data-ttu-id="d6f67-133">指定範例會先使用頂端欄位進行編碼。</span><span class="sxs-lookup"><span data-stu-id="d6f67-133">Specifies that the sample is encoded with the top field first.</span></span> <span data-ttu-id="d6f67-134">此值只有在結合交錯值時才有意義。</span><span class="sxs-lookup"><span data-stu-id="d6f67-134">This value is only meaningful when combined with the interlaced value.</span></span>    |
| <span data-ttu-id="d6f67-135">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d6f67-135">0x00000080</span></span> | <span data-ttu-id="d6f67-136">指定此範例為交錯式。</span><span class="sxs-lookup"><span data-stu-id="d6f67-136">Specifies that the sample is interlaced.</span></span> <span data-ttu-id="d6f67-137">這是對編解碼器 DMOs 有意義的唯一值。</span><span class="sxs-lookup"><span data-stu-id="d6f67-137">This is the only value that is meaningful to the codec DMOs.</span></span>                                    |



 

<span data-ttu-id="d6f67-138">前兩個值的其中一個，一律會使用位 Or， **或** 在取樣上進行設定，而結合0x80。</span><span class="sxs-lookup"><span data-stu-id="d6f67-138">One of the first two values is always combined with 0x80 using a bitwise **OR** before being set on the sample.</span></span> <span data-ttu-id="d6f67-139">不過，編碼器只會檢查0x80，並忽略其餘的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d6f67-139">However, the encoder only checks for 0x80 and disregards the rest of the extension.</span></span> <span data-ttu-id="d6f67-140">如果延伸模組將範例識別為交錯式，則編碼器會在壓縮的資料流程中維持範例交錯，並在資料流程中內嵌指示旗標，讓解碼器可以識別交錯的框架。</span><span class="sxs-lookup"><span data-stu-id="d6f67-140">If the extension identifies the sample as interlaced, the encoder maintains the sample interlacing in the compressed stream, and embeds an indication flag in the stream so that the decoder can identify interlaced frames.</span></span> <span data-ttu-id="d6f67-141">每個交錯範例都會標示為，因此混合漸進和交錯的來源內容可以一起編碼為數據流。</span><span class="sxs-lookup"><span data-stu-id="d6f67-141">Each interlaced sample is marked, so that source content that is a mix of progressive and interlaced can be encoded into a stream together.</span></span>

<span data-ttu-id="d6f67-142">Windows Media Format SDK 寫入器物件包含範例中的內容類型資料單位延伸模組，其會寫入至 ASF 容器的 data 區段，以便在轉譯時使用。</span><span class="sxs-lookup"><span data-stu-id="d6f67-142">The Windows Media Format SDK writer object includes the content type data unit extensions in the samples that it writes to the data section of the ASF container for use at the time of rendering.</span></span>

## <a name="reading-and-rendering-interlaced-video"></a><span data-ttu-id="d6f67-143">閱讀和轉譯交錯式影片</span><span class="sxs-lookup"><span data-stu-id="d6f67-143">Reading and Rendering Interlaced Video</span></span>

<span data-ttu-id="d6f67-144">此解碼器會根據編碼器在資料流程中設定的旗標來識別交錯樣本。</span><span class="sxs-lookup"><span data-stu-id="d6f67-144">The decoder identifies interlaced samples based on the flag set in the stream by the encoder.</span></span> <span data-ttu-id="d6f67-145">在預設情況下，此解碼器會 deinterlaces 範例並傳遞漸進式輸出。</span><span class="sxs-lookup"><span data-stu-id="d6f67-145">As a default, the decoder deinterlaces the samples and delivers progressive outputs.</span></span> <span data-ttu-id="d6f67-146">播放程式應用程式可以設定 [MFPKEY \_ 解碼器 \_ 去交錯](mfpkey-decoder-deinterlacingproperty.md) 屬性，以設定使用交錯來處理輸出的輸出。</span><span class="sxs-lookup"><span data-stu-id="d6f67-146">The player application can configure the decoder to process outputs with interlacing maintained by setting the [MFPKEY\_DECODER\_DEINTERLACING](mfpkey-decoder-deinterlacingproperty.md) property.</span></span>

<span data-ttu-id="d6f67-147">在解碼影片傳遞範例之後，會發生交錯播放影片的困難。</span><span class="sxs-lookup"><span data-stu-id="d6f67-147">The difficulty in interlaced video playback arises after the decoder delivers the samples.</span></span> <span data-ttu-id="d6f67-148">裝置中的轉譯器 (視訊卡或晶片) 無法正確地顯示影片內容，而不知道哪個欄位是什麼。</span><span class="sxs-lookup"><span data-stu-id="d6f67-148">The renderer (video card or chip in a device) cannot properly display the video content without knowing which field is which.</span></span> <span data-ttu-id="d6f67-149">在使用 Windows Media 格式 SDK 的應用程式中，內容類型資料單位延伸會從未壓縮的範例中取出，並可傳遞至裝置。</span><span class="sxs-lookup"><span data-stu-id="d6f67-149">In applications using the Windows Media Format SDK, the content type data unit extension is retrieved from the uncompressed samples, and can be passed to the device.</span></span>

<span data-ttu-id="d6f67-150">直接使用編解碼器物件時，不會自動傳送此資料。</span><span class="sxs-lookup"><span data-stu-id="d6f67-150">When using the codec objects directly, none of this data transfer is automatic.</span></span> <span data-ttu-id="d6f67-151">您必須在您的緩衝區物件和用於編碼內容的容器中，執行資料單位延伸模組支援。</span><span class="sxs-lookup"><span data-stu-id="d6f67-151">You must implement data-unit-extension support, both in your buffer objects and in the container that you use for your encoded content.</span></span> <span data-ttu-id="d6f67-152">最常見的媒體容器類型 (例如 AVI) 不支援範例層級的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d6f67-152">Most common types of media containers (like AVI) do not support sample-level metadata.</span></span> <span data-ttu-id="d6f67-153">您可以執行自己的系統來將資料儲存在檔案中，並將其與個別的範例產生關聯，但只有自訂的讀取器才能取得它。</span><span class="sxs-lookup"><span data-stu-id="d6f67-153">You can implement your own system to store the data in the file and associate it with individual samples, but only a customized reader would be able to retrieve it.</span></span>

> [!Note]  
> <span data-ttu-id="d6f67-154">將 [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) 屬性設定為 **TRUE**，然後不傳送任何附加了 content-type 資料單位延伸的範例，可能會導致編碼器損毀。</span><span class="sxs-lookup"><span data-stu-id="d6f67-154">Setting the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property to **TRUE**, and then not sending any samples with the content-type data-unit extension attached can cause the encoder to crash.</span></span> <span data-ttu-id="d6f67-155">只有在您有可傳遞的交錯式取樣時，才會設定交錯編碼的編碼器。</span><span class="sxs-lookup"><span data-stu-id="d6f67-155">Set the encoder for interlaced encoding only if you have interlaced samples to deliver.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d6f67-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6f67-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f67-157">使用影片</span><span class="sxs-lookup"><span data-stu-id="d6f67-157">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



