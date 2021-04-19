---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: PNG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994451"
---
# <a name="png-format-overview"></a><span data-ttu-id="21db4-103">PNG 格式總覽</span><span class="sxs-lookup"><span data-stu-id="21db4-103">PNG Format Overview</span></span>

<span data-ttu-id="21db4-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="21db4-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="21db4-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="21db4-105">Codec Identity</span></span>

<span data-ttu-id="21db4-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="21db4-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="21db4-107"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="21db4-107">Formal Name(s)</span></span>         | <span data-ttu-id="21db4-108">可攜式網路圖形 (PNG)</span><span class="sxs-lookup"><span data-stu-id="21db4-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="21db4-109">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="21db4-109">File Name Extension(s)</span></span> | <span data-ttu-id="21db4-110">png</span><span class="sxs-lookup"><span data-stu-id="21db4-110">png</span></span>                             |
| <span data-ttu-id="21db4-111">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="21db4-111">MIME type</span></span>              | <span data-ttu-id="21db4-112">image/png</span><span class="sxs-lookup"><span data-stu-id="21db4-112">image/png</span></span>                       |
| <span data-ttu-id="21db4-113">規格支援</span><span class="sxs-lookup"><span data-stu-id="21db4-113">Specification Support</span></span>  | <span data-ttu-id="21db4-114">PNG 規格1。2</span><span class="sxs-lookup"><span data-stu-id="21db4-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="21db4-115">下表列出用來識別原生 PNG 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="21db4-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="21db4-116">元件</span><span class="sxs-lookup"><span data-stu-id="21db4-116">Component</span></span>        | <span data-ttu-id="21db4-117">易記名稱</span><span class="sxs-lookup"><span data-stu-id="21db4-117">Friendly Name</span></span>            | <span data-ttu-id="21db4-118">GUID</span><span class="sxs-lookup"><span data-stu-id="21db4-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="21db4-119">容器格式</span><span class="sxs-lookup"><span data-stu-id="21db4-119">Container Format</span></span> | <span data-ttu-id="21db4-120">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="21db4-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="21db4-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="21db4-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="21db4-122">解碼器</span><span class="sxs-lookup"><span data-stu-id="21db4-122">Decoder</span></span>          | <span data-ttu-id="21db4-123">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="21db4-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="21db4-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="21db4-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="21db4-125">編碼器</span><span class="sxs-lookup"><span data-stu-id="21db4-125">Encoder</span></span>          | <span data-ttu-id="21db4-126">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="21db4-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="21db4-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="21db4-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="21db4-128">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="21db4-128">Windows 8 and later</span></span>

<span data-ttu-id="21db4-129">從 Windows 8 WIC 開始提供額外的 PNG 解碼器</span><span class="sxs-lookup"><span data-stu-id="21db4-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="21db4-130">編碼</span><span class="sxs-lookup"><span data-stu-id="21db4-130">Encoding</span></span>

<span data-ttu-id="21db4-131">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="21db4-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="21db4-132">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="21db4-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="21db4-133">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="21db4-133">Encoder Options</span></span>

<span data-ttu-id="21db4-134">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="21db4-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="21db4-135">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="21db4-136">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="21db4-137">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="21db4-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="21db4-138">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="21db4-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="21db4-139">PNG 編解碼器使用基本的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="21db4-140">下表列出原生 PNG 編解碼器所支援的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="21db4-141">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="21db4-141">Property Name</span></span>   | <span data-ttu-id="21db4-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="21db4-142">VARTYPE</span></span>  | <span data-ttu-id="21db4-143">值範圍</span><span class="sxs-lookup"><span data-stu-id="21db4-143">Value Range</span></span>                                                 | <span data-ttu-id="21db4-144">預設值</span><span class="sxs-lookup"><span data-stu-id="21db4-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="21db4-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="21db4-145">InterlaceOption</span></span> | <span data-ttu-id="21db4-146">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="21db4-146">VT\_BOOL</span></span> | <span data-ttu-id="21db4-147">**TRUE** /**FALSE**</span><span class="sxs-lookup"><span data-stu-id="21db4-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="21db4-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="21db4-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="21db4-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="21db4-149">FilterOption</span></span>    | <span data-ttu-id="21db4-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="21db4-150">VT\_UI1</span></span>  | [<span data-ttu-id="21db4-151">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="21db4-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="21db4-152">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="21db4-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="21db4-153">如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="21db4-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="21db4-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="21db4-154">InterlaceOption</span></span>

<span data-ttu-id="21db4-155">指定是否將影像資料編碼為交錯式。</span><span class="sxs-lookup"><span data-stu-id="21db4-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="21db4-156">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="21db4-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="21db4-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="21db4-157">FilterOption</span></span>

<span data-ttu-id="21db4-158">指定用於影像壓縮的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="21db4-159">預設值為 [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)。</span><span class="sxs-lookup"><span data-stu-id="21db4-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="21db4-160">解碼</span><span class="sxs-lookup"><span data-stu-id="21db4-160">Decoding</span></span>

<span data-ttu-id="21db4-161">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="21db4-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="21db4-162">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="21db4-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="21db4-163">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="21db4-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="21db4-164">原生 PNG 編解碼器也支援畫面上的 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ，以新增解碼影像資料流程的 advanced 選項。</span><span class="sxs-lookup"><span data-stu-id="21db4-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="21db4-165">如需這些 advanced 選項的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="21db4-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
