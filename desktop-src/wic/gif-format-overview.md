---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 GIF 編解碼器的相關資訊。
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: GIF 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193708"
---
# <a name="gif-format-overview"></a><span data-ttu-id="98395-103">GIF 格式總覽</span><span class="sxs-lookup"><span data-stu-id="98395-103">GIF Format Overview</span></span>

<span data-ttu-id="98395-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 GIF 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98395-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="98395-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="98395-105">Codec Identity</span></span>

<span data-ttu-id="98395-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="98395-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="98395-107"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="98395-107">Formal Name(s)</span></span>         | <span data-ttu-id="98395-108">圖形交換格式 89a (GIF) </span><span class="sxs-lookup"><span data-stu-id="98395-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="98395-109">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="98395-109">File Name Extension(s)</span></span> | <span data-ttu-id="98395-110">GIF</span><span class="sxs-lookup"><span data-stu-id="98395-110">gif</span></span>                                   |
| <span data-ttu-id="98395-111">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="98395-111">MIME type</span></span>              | <span data-ttu-id="98395-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="98395-112">image/gif</span></span>                             |
| <span data-ttu-id="98395-113">規格支援</span><span class="sxs-lookup"><span data-stu-id="98395-113">Specification Support</span></span>  | <span data-ttu-id="98395-114">GIF 規格 89a/89m</span><span class="sxs-lookup"><span data-stu-id="98395-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="98395-115">下表列出用來識別原生 GIF 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="98395-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="98395-116">元件</span><span class="sxs-lookup"><span data-stu-id="98395-116">Component</span></span>        | <span data-ttu-id="98395-117">易記名稱</span><span class="sxs-lookup"><span data-stu-id="98395-117">Friendly Name</span></span>            | <span data-ttu-id="98395-118">GUID</span><span class="sxs-lookup"><span data-stu-id="98395-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="98395-119">容器格式</span><span class="sxs-lookup"><span data-stu-id="98395-119">Container Format</span></span> | <span data-ttu-id="98395-120">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="98395-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="98395-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="98395-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="98395-122">解碼器</span><span class="sxs-lookup"><span data-stu-id="98395-122">Decoder</span></span>          | <span data-ttu-id="98395-123">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="98395-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="98395-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="98395-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="98395-125">編碼器</span><span class="sxs-lookup"><span data-stu-id="98395-125">Encoder</span></span>          | <span data-ttu-id="98395-126">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="98395-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="98395-127">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="98395-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="98395-128">編碼</span><span class="sxs-lookup"><span data-stu-id="98395-128">Encoding</span></span>

<span data-ttu-id="98395-129">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="98395-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="98395-130">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="98395-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="98395-131">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="98395-131">Encoder Options</span></span>

<span data-ttu-id="98395-132">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="98395-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="98395-133">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="98395-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="98395-134">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="98395-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="98395-135">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="98395-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="98395-136">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="98395-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="98395-137">GIF 編碼器不支援任何基本的 WIC 選項，也不會提供自訂編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="98395-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="98395-138">如果編碼器選項是在 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="98395-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="98395-139">解碼</span><span class="sxs-lookup"><span data-stu-id="98395-139">Decoding</span></span>

<span data-ttu-id="98395-140">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="98395-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="98395-141">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="98395-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="98395-142">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="98395-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
