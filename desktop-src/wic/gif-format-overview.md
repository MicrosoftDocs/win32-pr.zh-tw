---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 GIF 編解碼器的相關資訊。
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: GIF 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444449"
---
# <a name="gif-format-overview"></a><span data-ttu-id="d2a2f-103">GIF 格式總覽</span><span class="sxs-lookup"><span data-stu-id="d2a2f-103">GIF Format Overview</span></span>

<span data-ttu-id="d2a2f-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 GIF 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="d2a2f-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="d2a2f-105">Codec Identity</span></span>

<span data-ttu-id="d2a2f-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="d2a2f-107">元件</span><span class="sxs-lookup"><span data-stu-id="d2a2f-107">Component</span></span>             | <span data-ttu-id="d2a2f-108">描述</span><span class="sxs-lookup"><span data-stu-id="d2a2f-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="d2a2f-109"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="d2a2f-109">Formal Name(s)</span></span>         | <span data-ttu-id="d2a2f-110">圖形交換格式 89a (GIF) </span><span class="sxs-lookup"><span data-stu-id="d2a2f-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="d2a2f-111">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="d2a2f-111">File Name Extension(s)</span></span> | <span data-ttu-id="d2a2f-112">GIF</span><span class="sxs-lookup"><span data-stu-id="d2a2f-112">gif</span></span>                                   |
| <span data-ttu-id="d2a2f-113">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="d2a2f-113">MIME type</span></span>              | <span data-ttu-id="d2a2f-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="d2a2f-114">image/gif</span></span>                             |
| <span data-ttu-id="d2a2f-115">規格支援</span><span class="sxs-lookup"><span data-stu-id="d2a2f-115">Specification Support</span></span>  | <span data-ttu-id="d2a2f-116">GIF 規格 89a/89m</span><span class="sxs-lookup"><span data-stu-id="d2a2f-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="d2a2f-117">下表列出用來識別原生 GIF 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="d2a2f-118">元件</span><span class="sxs-lookup"><span data-stu-id="d2a2f-118">Component</span></span>        | <span data-ttu-id="d2a2f-119">易記名稱</span><span class="sxs-lookup"><span data-stu-id="d2a2f-119">Friendly Name</span></span>            | <span data-ttu-id="d2a2f-120">GUID</span><span class="sxs-lookup"><span data-stu-id="d2a2f-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="d2a2f-121">容器格式</span><span class="sxs-lookup"><span data-stu-id="d2a2f-121">Container Format</span></span> | <span data-ttu-id="d2a2f-122">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="d2a2f-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="d2a2f-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="d2a2f-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="d2a2f-124">解碼器</span><span class="sxs-lookup"><span data-stu-id="d2a2f-124">Decoder</span></span>          | <span data-ttu-id="d2a2f-125">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="d2a2f-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="d2a2f-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="d2a2f-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="d2a2f-127">編碼器</span><span class="sxs-lookup"><span data-stu-id="d2a2f-127">Encoder</span></span>          | <span data-ttu-id="d2a2f-128">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="d2a2f-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="d2a2f-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="d2a2f-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="d2a2f-130">編碼</span><span class="sxs-lookup"><span data-stu-id="d2a2f-130">Encoding</span></span>

<span data-ttu-id="d2a2f-131">WIC 編碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d2a2f-132">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="d2a2f-133">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="d2a2f-133">Encoder Options</span></span>

<span data-ttu-id="d2a2f-134">已啟用 WIC 的編解碼器在編碼選項層級不同。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="d2a2f-135">編碼器選項反映影像編碼器的功能，而每個原生編解碼器都支援一組這些編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="d2a2f-136">編碼器選項可以是基本的 WIC 支援選項，可供所有 WIC 啟用的程式碼使用 (但不一定支援) 或由影像格式編解碼器所設計的編解碼器專用選項。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="d2a2f-137">為了在編碼過程中管理這些編碼選項，WIC 會使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="d2a2f-138">如需有關使用 **IPropertyBag2** 介面進行 WIC 編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="d2a2f-139">GIF 編碼器不支援任何基本的 WIC 選項，也不會提供自訂編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="d2a2f-140">如果編碼器選項是在 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 選項清單中，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="d2a2f-141">解碼</span><span class="sxs-lookup"><span data-stu-id="d2a2f-141">Decoding</span></span>

<span data-ttu-id="d2a2f-142">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d2a2f-143">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d2a2f-144">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
