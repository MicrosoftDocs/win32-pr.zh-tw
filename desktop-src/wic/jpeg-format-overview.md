---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 JPEG 編解碼器的相關資訊。
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: JPEG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444189"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="94f4a-103">JPEG 格式總覽</span><span class="sxs-lookup"><span data-stu-id="94f4a-103">JPEG Format Overview</span></span>

<span data-ttu-id="94f4a-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 JPEG 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="94f4a-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="94f4a-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="94f4a-105">Codec Identity</span></span>

<span data-ttu-id="94f4a-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="94f4a-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="94f4a-107">元件</span><span class="sxs-lookup"><span data-stu-id="94f4a-107">Component</span></span>            | <span data-ttu-id="94f4a-108">描述</span><span class="sxs-lookup"><span data-stu-id="94f4a-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="94f4a-109"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="94f4a-109">Formal Name(s)</span></span>         | <span data-ttu-id="94f4a-110">JPEG 格式 (JPEG)</span><span class="sxs-lookup"><span data-stu-id="94f4a-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="94f4a-111">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="94f4a-111">File Name Extension(s)</span></span> | <span data-ttu-id="94f4a-112">jpe、jpeg、jpg</span><span class="sxs-lookup"><span data-stu-id="94f4a-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="94f4a-113">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="94f4a-113">MIME type</span></span>              | <span data-ttu-id="94f4a-114">image/jpeg、image/jpe、image/jpg</span><span class="sxs-lookup"><span data-stu-id="94f4a-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="94f4a-115">規格支援</span><span class="sxs-lookup"><span data-stu-id="94f4a-115">Specification Support</span></span>  | <span data-ttu-id="94f4a-116">JFIF 規格1.02</span><span class="sxs-lookup"><span data-stu-id="94f4a-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="94f4a-117">下表列出用來識別原生 JPEG 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="94f4a-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="94f4a-118">元件</span><span class="sxs-lookup"><span data-stu-id="94f4a-118">Component</span></span>        | <span data-ttu-id="94f4a-119">易記名稱</span><span class="sxs-lookup"><span data-stu-id="94f4a-119">Friendly Name</span></span>             | <span data-ttu-id="94f4a-120">GUID</span><span class="sxs-lookup"><span data-stu-id="94f4a-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="94f4a-121">容器格式</span><span class="sxs-lookup"><span data-stu-id="94f4a-121">Container Format</span></span> | <span data-ttu-id="94f4a-122">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="94f4a-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="94f4a-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="94f4a-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="94f4a-124">解碼器</span><span class="sxs-lookup"><span data-stu-id="94f4a-124">Decoder</span></span>          | <span data-ttu-id="94f4a-125">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="94f4a-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="94f4a-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="94f4a-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="94f4a-127">編碼器</span><span class="sxs-lookup"><span data-stu-id="94f4a-127">Encoder</span></span>          | <span data-ttu-id="94f4a-128">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="94f4a-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="94f4a-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="94f4a-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="94f4a-130">編碼</span><span class="sxs-lookup"><span data-stu-id="94f4a-130">Encoding</span></span>

<span data-ttu-id="94f4a-131">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="94f4a-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="94f4a-132">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="94f4a-133">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-133">Encoder Options</span></span>

<span data-ttu-id="94f4a-134">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="94f4a-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="94f4a-135">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="94f4a-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="94f4a-136">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="94f4a-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="94f4a-137">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="94f4a-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="94f4a-138">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="94f4a-139">JPEG 編解碼器會使用基本的 WIC 選項。</span><span class="sxs-lookup"><span data-stu-id="94f4a-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="94f4a-140">下表列出原生 JPEG 編解碼器所支援的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="94f4a-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="94f4a-141">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="94f4a-141">Property Name</span></span>                                        | <span data-ttu-id="94f4a-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="94f4a-142">VARTYPE</span></span>           | <span data-ttu-id="94f4a-143">值範圍</span><span class="sxs-lookup"><span data-stu-id="94f4a-143">Value Range</span></span>                                                                       | <span data-ttu-id="94f4a-144">預設值</span><span class="sxs-lookup"><span data-stu-id="94f4a-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="94f4a-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="94f4a-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="94f4a-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="94f4a-146">VT\_R4</span></span>            | <span data-ttu-id="94f4a-147">0-1。0</span><span class="sxs-lookup"><span data-stu-id="94f4a-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="94f4a-148">0.9</span><span class="sxs-lookup"><span data-stu-id="94f4a-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="94f4a-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="94f4a-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="94f4a-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="94f4a-150">VT\_UI1</span></span>           | [<span data-ttu-id="94f4a-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="94f4a-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="94f4a-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="94f4a-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="94f4a-153">明亮度</span><span class="sxs-lookup"><span data-stu-id="94f4a-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="94f4a-154">VT \_ UI4/vt \_ 陣列</span><span class="sxs-lookup"><span data-stu-id="94f4a-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="94f4a-155">64專案 (DCT) </span><span class="sxs-lookup"><span data-stu-id="94f4a-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="94f4a-156">預設的亮度表。</span><span class="sxs-lookup"><span data-stu-id="94f4a-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="94f4a-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="94f4a-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="94f4a-158">VT \_ UI4/vt \_ 陣列</span><span class="sxs-lookup"><span data-stu-id="94f4a-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="94f4a-159">64專案 (DCT) </span><span class="sxs-lookup"><span data-stu-id="94f4a-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="94f4a-160">預設的色度資料表。</span><span class="sxs-lookup"><span data-stu-id="94f4a-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="94f4a-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="94f4a-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="94f4a-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="94f4a-162">VT\_UI1</span></span>           | [<span data-ttu-id="94f4a-163">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="94f4a-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="94f4a-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="94f4a-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="94f4a-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="94f4a-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="94f4a-166">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="94f4a-166">VT\_BOOL</span></span>          | <span data-ttu-id="94f4a-167">**TRUE** /**FALSE**</span><span class="sxs-lookup"><span data-stu-id="94f4a-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="94f4a-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="94f4a-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="94f4a-169">如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="94f4a-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="94f4a-170">ImageQuality 選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-170">ImageQuality Option</span></span>

<span data-ttu-id="94f4a-171">指定所需的影像精確度。</span><span class="sxs-lookup"><span data-stu-id="94f4a-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="94f4a-172">0.0 表示可能的精確度最低，而1.0 指定最高的精確度。</span><span class="sxs-lookup"><span data-stu-id="94f4a-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="94f4a-173">預設值為0.9。</span><span class="sxs-lookup"><span data-stu-id="94f4a-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="94f4a-174">BitmapTransform 選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-174">BitmapTransform Option</span></span>

<span data-ttu-id="94f4a-175">指定影像解碼期間影像的轉換方式。</span><span class="sxs-lookup"><span data-stu-id="94f4a-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="94f4a-176">此選項必須設定為其中一個 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="94f4a-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="94f4a-177">預設值為 [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="94f4a-178">亮度選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-178">Luminance Option</span></span>

<span data-ttu-id="94f4a-179">指定用於編碼的灰階亮度層級表格。</span><span class="sxs-lookup"><span data-stu-id="94f4a-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="94f4a-180">色度選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-180">Chrominance Option</span></span>

<span data-ttu-id="94f4a-181">指定要用於編碼的色度資料表。</span><span class="sxs-lookup"><span data-stu-id="94f4a-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="94f4a-182">JpegYCrCbSubsampling 選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="94f4a-183">指定用於 YCrCb 編碼的次取樣比例。</span><span class="sxs-lookup"><span data-stu-id="94f4a-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="94f4a-184">預設值為 [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="94f4a-185">SuppressApp0 選項</span><span class="sxs-lookup"><span data-stu-id="94f4a-185">SuppressApp0 Option</span></span>

<span data-ttu-id="94f4a-186">指定在編碼影像資料時，是否要隱藏 App0 中繼資料的寫入。</span><span class="sxs-lookup"><span data-stu-id="94f4a-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="94f4a-187">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="94f4a-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="94f4a-188">解碼</span><span class="sxs-lookup"><span data-stu-id="94f4a-188">Decoding</span></span>

<span data-ttu-id="94f4a-189">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="94f4a-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="94f4a-190">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="94f4a-191">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="94f4a-192">原生 JPEG 編解碼器也支援在畫面格解碼上 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ，以新增解碼影像串流的進階選項。</span><span class="sxs-lookup"><span data-stu-id="94f4a-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="94f4a-193">如需這些 advanced 選項的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="94f4a-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
