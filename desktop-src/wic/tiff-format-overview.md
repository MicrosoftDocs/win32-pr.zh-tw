---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 TIFF 編解碼器的相關資訊。
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: TIFF 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444419"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="8ca47-103">TIFF 格式總覽</span><span class="sxs-lookup"><span data-stu-id="8ca47-103">TIFF Format Overview</span></span>

<span data-ttu-id="8ca47-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 TIFF 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ca47-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="8ca47-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="8ca47-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="8ca47-106">編碼方式</span><span class="sxs-lookup"><span data-stu-id="8ca47-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="8ca47-107">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="8ca47-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="8ca47-108">解碼</span><span class="sxs-lookup"><span data-stu-id="8ca47-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="8ca47-109">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="8ca47-109">Codec Identity</span></span>

<span data-ttu-id="8ca47-110">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="8ca47-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="8ca47-111">元件</span><span class="sxs-lookup"><span data-stu-id="8ca47-111">Component</span></span>            |   <span data-ttu-id="8ca47-112">描述</span><span class="sxs-lookup"><span data-stu-id="8ca47-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="8ca47-113"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="8ca47-113">Formal Name(s)</span></span>         | <span data-ttu-id="8ca47-114">標記的影像檔案格式 (TIFF)</span><span class="sxs-lookup"><span data-stu-id="8ca47-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="8ca47-115">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="8ca47-115">File Name Extension(s)</span></span> | <span data-ttu-id="8ca47-116">tiff、.tif</span><span class="sxs-lookup"><span data-stu-id="8ca47-116">tiff, tif</span></span>                       |
| <span data-ttu-id="8ca47-117">MIME 類型 (s) </span><span class="sxs-lookup"><span data-stu-id="8ca47-117">MIME type(s)</span></span>           | <span data-ttu-id="8ca47-118">影像/tiff、影像/.tif</span><span class="sxs-lookup"><span data-stu-id="8ca47-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="8ca47-119">規格支援</span><span class="sxs-lookup"><span data-stu-id="8ca47-119">Specification Support</span></span>  | <span data-ttu-id="8ca47-120">TIFF 規格6。0</span><span class="sxs-lookup"><span data-stu-id="8ca47-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="8ca47-121">下表列出用來識別原生 TIFF 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="8ca47-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="8ca47-122">元件</span><span class="sxs-lookup"><span data-stu-id="8ca47-122">Component</span></span>        | <span data-ttu-id="8ca47-123">易記名稱</span><span class="sxs-lookup"><span data-stu-id="8ca47-123">Friendly Name</span></span>             | <span data-ttu-id="8ca47-124">GUID</span><span class="sxs-lookup"><span data-stu-id="8ca47-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="8ca47-125">容器格式</span><span class="sxs-lookup"><span data-stu-id="8ca47-125">Container Format</span></span> | <span data-ttu-id="8ca47-126">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="8ca47-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="8ca47-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="8ca47-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="8ca47-128">解碼器</span><span class="sxs-lookup"><span data-stu-id="8ca47-128">Decoder</span></span>          | <span data-ttu-id="8ca47-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="8ca47-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="8ca47-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="8ca47-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="8ca47-131">編碼器</span><span class="sxs-lookup"><span data-stu-id="8ca47-131">Encoder</span></span>          | <span data-ttu-id="8ca47-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="8ca47-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="8ca47-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="8ca47-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="8ca47-134">編碼</span><span class="sxs-lookup"><span data-stu-id="8ca47-134">Encoding</span></span>

<span data-ttu-id="8ca47-135">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="8ca47-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8ca47-136">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca47-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="8ca47-137">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="8ca47-137">Encoder Options</span></span>

<span data-ttu-id="8ca47-138">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="8ca47-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="8ca47-139">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="8ca47-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="8ca47-140">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="8ca47-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="8ca47-141">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="8ca47-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="8ca47-142">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca47-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="8ca47-143">TIFF 編解碼器會使用基本的 WIC 選項。</span><span class="sxs-lookup"><span data-stu-id="8ca47-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="8ca47-144">下表列出原生 TIFF 編解碼器所支援的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="8ca47-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="8ca47-145">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="8ca47-145">Property Name</span></span>         | <span data-ttu-id="8ca47-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8ca47-146">VARTYPE</span></span> | <span data-ttu-id="8ca47-147">值範圍</span><span class="sxs-lookup"><span data-stu-id="8ca47-147">Value Range</span></span> | <span data-ttu-id="8ca47-148">預設值</span><span class="sxs-lookup"><span data-stu-id="8ca47-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="8ca47-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="8ca47-149">CompressionQuality</span></span>    | <span data-ttu-id="8ca47-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="8ca47-150">VT\_R4</span></span>  | <span data-ttu-id="8ca47-151">0-1。0</span><span class="sxs-lookup"><span data-stu-id="8ca47-151">0 - 1.0</span></span>     | <span data-ttu-id="8ca47-152">0</span><span class="sxs-lookup"><span data-stu-id="8ca47-152">0</span></span>                |
| <span data-ttu-id="8ca47-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="8ca47-153">TiffCompressionMethod</span></span> | <span data-ttu-id="8ca47-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="8ca47-154">VT\_UI1</span></span> | [<span data-ttu-id="8ca47-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="8ca47-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="8ca47-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="8ca47-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="8ca47-157">如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="8ca47-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="8ca47-158">CompressionQuality 選項</span><span class="sxs-lookup"><span data-stu-id="8ca47-158">CompressionQuality Option</span></span>

<span data-ttu-id="8ca47-159">指定所需的壓縮品質。</span><span class="sxs-lookup"><span data-stu-id="8ca47-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="8ca47-160">0.0 表示可用的最有效率壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="8ca47-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="8ca47-161">一般而言，此配置會產生更快速的編碼，但較大的輸出。</span><span class="sxs-lookup"><span data-stu-id="8ca47-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="8ca47-162">值為1.0 時，可指定最有效率的壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="8ca47-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="8ca47-163">一般而言，此配置會導致較長的編碼，但會產生較小的輸出。</span><span class="sxs-lookup"><span data-stu-id="8ca47-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="8ca47-164">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="8ca47-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="8ca47-165">TiffCompressionMethod 選項</span><span class="sxs-lookup"><span data-stu-id="8ca47-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="8ca47-166">指定 TIFF 壓縮方法。</span><span class="sxs-lookup"><span data-stu-id="8ca47-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="8ca47-167">預設值為 [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)。</span><span class="sxs-lookup"><span data-stu-id="8ca47-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="8ca47-168">解碼</span><span class="sxs-lookup"><span data-stu-id="8ca47-168">Decoding</span></span>

<span data-ttu-id="8ca47-169">WIC 解碼 Api 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="8ca47-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8ca47-170">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca47-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8ca47-171">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca47-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
