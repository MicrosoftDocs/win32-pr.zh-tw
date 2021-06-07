---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: PNG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444439"
---
# <a name="png-format-overview"></a><span data-ttu-id="49953-103">PNG 格式總覽</span><span class="sxs-lookup"><span data-stu-id="49953-103">PNG Format Overview</span></span>

<span data-ttu-id="49953-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 PNG 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49953-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="49953-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="49953-105">Codec Identity</span></span>

<span data-ttu-id="49953-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="49953-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="49953-107">元件</span><span class="sxs-lookup"><span data-stu-id="49953-107">Component</span></span>          | <span data-ttu-id="49953-108">描述</span><span class="sxs-lookup"><span data-stu-id="49953-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="49953-109"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="49953-109">Formal Name(s)</span></span>         | <span data-ttu-id="49953-110">可攜式網路圖形 (PNG)</span><span class="sxs-lookup"><span data-stu-id="49953-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="49953-111">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="49953-111">File Name Extension(s)</span></span> | <span data-ttu-id="49953-112">png</span><span class="sxs-lookup"><span data-stu-id="49953-112">png</span></span>                             |
| <span data-ttu-id="49953-113">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="49953-113">MIME type</span></span>              | <span data-ttu-id="49953-114">image/png</span><span class="sxs-lookup"><span data-stu-id="49953-114">image/png</span></span>                       |
| <span data-ttu-id="49953-115">規格支援</span><span class="sxs-lookup"><span data-stu-id="49953-115">Specification Support</span></span>  | <span data-ttu-id="49953-116">PNG 規格1。2</span><span class="sxs-lookup"><span data-stu-id="49953-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="49953-117">下表列出用來識別原生 PNG 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="49953-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="49953-118">元件</span><span class="sxs-lookup"><span data-stu-id="49953-118">Component</span></span>        | <span data-ttu-id="49953-119">易記名稱</span><span class="sxs-lookup"><span data-stu-id="49953-119">Friendly Name</span></span>            | <span data-ttu-id="49953-120">GUID</span><span class="sxs-lookup"><span data-stu-id="49953-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="49953-121">容器格式</span><span class="sxs-lookup"><span data-stu-id="49953-121">Container Format</span></span> | <span data-ttu-id="49953-122">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="49953-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="49953-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="49953-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="49953-124">解碼器</span><span class="sxs-lookup"><span data-stu-id="49953-124">Decoder</span></span>          | <span data-ttu-id="49953-125">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="49953-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="49953-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="49953-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="49953-127">編碼器</span><span class="sxs-lookup"><span data-stu-id="49953-127">Encoder</span></span>          | <span data-ttu-id="49953-128">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="49953-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="49953-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="49953-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="49953-130">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="49953-130">Windows 8 and later</span></span>

<span data-ttu-id="49953-131">從 Windows 8 WIC 開始提供額外的 PNG 解碼器</span><span class="sxs-lookup"><span data-stu-id="49953-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="49953-132">編碼</span><span class="sxs-lookup"><span data-stu-id="49953-132">Encoding</span></span>

<span data-ttu-id="49953-133">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="49953-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="49953-134">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="49953-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="49953-135">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="49953-135">Encoder Options</span></span>

<span data-ttu-id="49953-136">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="49953-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="49953-137">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="49953-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="49953-138">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="49953-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="49953-139">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="49953-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="49953-140">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="49953-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="49953-141">PNG 編解碼器使用基本的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="49953-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="49953-142">下表列出原生 PNG 編解碼器所支援的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="49953-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="49953-143">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="49953-143">Property Name</span></span>   | <span data-ttu-id="49953-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="49953-144">VARTYPE</span></span>  | <span data-ttu-id="49953-145">值範圍</span><span class="sxs-lookup"><span data-stu-id="49953-145">Value Range</span></span>                                                 | <span data-ttu-id="49953-146">預設值</span><span class="sxs-lookup"><span data-stu-id="49953-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="49953-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="49953-147">InterlaceOption</span></span> | <span data-ttu-id="49953-148">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="49953-148">VT\_BOOL</span></span> | <span data-ttu-id="49953-149">**TRUE** /**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49953-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="49953-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="49953-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="49953-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="49953-151">FilterOption</span></span>    | <span data-ttu-id="49953-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="49953-152">VT\_UI1</span></span>  | [<span data-ttu-id="49953-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="49953-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="49953-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="49953-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="49953-155">如果編碼器選項存在於編解碼器不支援的 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="49953-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="49953-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="49953-156">InterlaceOption</span></span>

<span data-ttu-id="49953-157">指定是否將影像資料編碼為交錯式。</span><span class="sxs-lookup"><span data-stu-id="49953-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="49953-158">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="49953-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="49953-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="49953-159">FilterOption</span></span>

<span data-ttu-id="49953-160">指定用於影像壓縮的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="49953-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="49953-161">預設值為 [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)。</span><span class="sxs-lookup"><span data-stu-id="49953-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="49953-162">解碼</span><span class="sxs-lookup"><span data-stu-id="49953-162">Decoding</span></span>

<span data-ttu-id="49953-163">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="49953-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="49953-164">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="49953-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="49953-165">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="49953-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="49953-166">原生 PNG 編解碼器也支援畫面上的 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ，以新增解碼影像資料流程的 advanced 選項。</span><span class="sxs-lookup"><span data-stu-id="49953-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="49953-167">如需這些 advanced 選項的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="49953-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
