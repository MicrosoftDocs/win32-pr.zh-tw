---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 BMP 編解碼器的相關資訊。
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: BMP 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693248"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="16972-103">BMP 格式總覽</span><span class="sxs-lookup"><span data-stu-id="16972-103">BMP Format Overview</span></span>

<span data-ttu-id="16972-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 BMP 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16972-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="16972-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="16972-105">Codec Identity</span></span>

<span data-ttu-id="16972-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="16972-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="16972-107"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="16972-107">Formal Name(s)</span></span>         | <span data-ttu-id="16972-108">Windows 點陣圖格式</span><span class="sxs-lookup"><span data-stu-id="16972-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="16972-109">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="16972-109">File Name Extension(s)</span></span> | <span data-ttu-id="16972-110">bmp、dib</span><span class="sxs-lookup"><span data-stu-id="16972-110">bmp, dib</span></span>              |
| <span data-ttu-id="16972-111">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="16972-111">MIME type</span></span>              | <span data-ttu-id="16972-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="16972-112">image/bmp</span></span>             |
| <span data-ttu-id="16972-113">規格支援</span><span class="sxs-lookup"><span data-stu-id="16972-113">Specification Support</span></span>  | <span data-ttu-id="16972-114">BMP 規格 v5</span><span class="sxs-lookup"><span data-stu-id="16972-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="16972-115">下表列出用來識別原生 BMP 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="16972-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="16972-116">元件</span><span class="sxs-lookup"><span data-stu-id="16972-116">Component</span></span>        | <span data-ttu-id="16972-117">易記名稱</span><span class="sxs-lookup"><span data-stu-id="16972-117">Friendly Name</span></span>            | <span data-ttu-id="16972-118">GUID</span><span class="sxs-lookup"><span data-stu-id="16972-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="16972-119">容器格式</span><span class="sxs-lookup"><span data-stu-id="16972-119">Container Format</span></span> | <span data-ttu-id="16972-120">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="16972-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="16972-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="16972-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="16972-122">解碼器</span><span class="sxs-lookup"><span data-stu-id="16972-122">Decoder</span></span>          | <span data-ttu-id="16972-123">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="16972-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="16972-124">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="16972-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="16972-125">編碼器</span><span class="sxs-lookup"><span data-stu-id="16972-125">Encoder</span></span>          | <span data-ttu-id="16972-126">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="16972-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="16972-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="16972-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="16972-128">編碼</span><span class="sxs-lookup"><span data-stu-id="16972-128">Encoding</span></span>

<span data-ttu-id="16972-129">WIC 編碼 API 設計成與編解碼器無關，因此支援 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="16972-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="16972-130">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="16972-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="16972-131">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="16972-131">Encoder Options</span></span>

<span data-ttu-id="16972-132">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="16972-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="16972-133">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="16972-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="16972-134">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="16972-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="16972-135">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="16972-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="16972-136">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="16972-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="16972-137">下表列出原生 BMP 編解碼器所支援的 WIC 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="16972-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="16972-138">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="16972-138">Property Name</span></span>               | <span data-ttu-id="16972-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="16972-139">VARTYPE</span></span>      | <span data-ttu-id="16972-140">值範圍</span><span class="sxs-lookup"><span data-stu-id="16972-140">Value Range</span></span>                      | <span data-ttu-id="16972-141">預設值</span><span class="sxs-lookup"><span data-stu-id="16972-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="16972-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="16972-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="16972-143">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="16972-143">**VT\_BOOL**</span></span> | <span data-ttu-id="16972-144">**VARIANT \_ TRUE/VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="16972-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="16972-145">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="16972-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="16972-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="16972-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="16972-147">指定是否允許以 GUID \_ WICPixelFormat32bppBGRA 像素格式來編碼資料。</span><span class="sxs-lookup"><span data-stu-id="16972-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="16972-148">如果這個選項設定為 **VARIANT \_ TRUE**，就會以 BITMAPV5HEADER 標頭寫出 BMP。</span><span class="sxs-lookup"><span data-stu-id="16972-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="16972-149">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="16972-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="16972-150">如果編碼器選項存在於編解碼器不支援的 IPropertyBag2 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="16972-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="16972-151">請注意，對於16位和32位的 Windows BMP 檔案，BMP 編解碼器會忽略任何 Alpha 色板，因為許多舊版影像檔案在此額外通道中包含不正確資料。</span><span class="sxs-lookup"><span data-stu-id="16972-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="16972-152">從 Windows 8 開始，使用 **BITMAPV5HEADER** 與有效 Alpha 通道內容撰寫的32位 Windows BMP 檔案會以 WICPixelFormat32bppBGRA 的形式讀取</span><span class="sxs-lookup"><span data-stu-id="16972-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="16972-153">解碼</span><span class="sxs-lookup"><span data-stu-id="16972-153">Decoding</span></span>

<span data-ttu-id="16972-154">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="16972-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="16972-155">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="16972-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="16972-156">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="16972-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
