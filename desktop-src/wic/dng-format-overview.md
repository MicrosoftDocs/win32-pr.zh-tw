---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DNG 編解碼器的相關資訊。
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: DNG 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319303"
---
# <a name="dng-format-overview"></a><span data-ttu-id="2d0a6-103">DNG 格式總覽</span><span class="sxs-lookup"><span data-stu-id="2d0a6-103">DNG Format Overview</span></span>

<span data-ttu-id="2d0a6-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2d0a6-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2d0a6-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2d0a6-106">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DNG 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="2d0a6-107">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="2d0a6-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="2d0a6-108">解碼</span><span class="sxs-lookup"><span data-stu-id="2d0a6-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="2d0a6-109">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="2d0a6-109">Codec Identity</span></span>

<span data-ttu-id="2d0a6-110">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2d0a6-111"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="2d0a6-111">Formal Name(s)</span></span>         | <span data-ttu-id="2d0a6-112">數位負面 (DNG) </span><span class="sxs-lookup"><span data-stu-id="2d0a6-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="2d0a6-113">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="2d0a6-113">File Name Extension(s)</span></span> | <span data-ttu-id="2d0a6-114">.dng</span><span class="sxs-lookup"><span data-stu-id="2d0a6-114">.dng</span></span>                                                 |
| <span data-ttu-id="2d0a6-115">MIME 類型 (s) </span><span class="sxs-lookup"><span data-stu-id="2d0a6-115">MIME type(s)</span></span>           | <span data-ttu-id="2d0a6-116">image/DNG</span><span class="sxs-lookup"><span data-stu-id="2d0a6-116">image/DNG</span></span>                                            |
| <span data-ttu-id="2d0a6-117">規格支援</span><span class="sxs-lookup"><span data-stu-id="2d0a6-117">Specification Support</span></span>  | <span data-ttu-id="2d0a6-118">數位負面 (DNG) 規格版本1.4.0。0</span><span class="sxs-lookup"><span data-stu-id="2d0a6-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="2d0a6-119">下表列出用來識別原生 DNG 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="2d0a6-120">元件</span><span class="sxs-lookup"><span data-stu-id="2d0a6-120">Component</span></span>        | <span data-ttu-id="2d0a6-121">易記名稱</span><span class="sxs-lookup"><span data-stu-id="2d0a6-121">Friendly Name</span></span>             | <span data-ttu-id="2d0a6-122">GUID</span><span class="sxs-lookup"><span data-stu-id="2d0a6-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="2d0a6-123">容器格式</span><span class="sxs-lookup"><span data-stu-id="2d0a6-123">Container Format</span></span> | <span data-ttu-id="2d0a6-124">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="2d0a6-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="2d0a6-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="2d0a6-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="2d0a6-126">解碼器</span><span class="sxs-lookup"><span data-stu-id="2d0a6-126">Decoder</span></span>          | <span data-ttu-id="2d0a6-127">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="2d0a6-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="2d0a6-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="2d0a6-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="2d0a6-129">解碼</span><span class="sxs-lookup"><span data-stu-id="2d0a6-129">Decoding</span></span>

<span data-ttu-id="2d0a6-130">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2d0a6-131">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="2d0a6-132">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="2d0a6-133">此解碼器不支援解碼原始感應器資料，而且只支援在 NewSubFileType 等於1的 IFD 中內嵌非原始影像表示的檔案。</span><span class="sxs-lookup"><span data-stu-id="2d0a6-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



