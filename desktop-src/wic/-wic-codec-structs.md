---
title: WIC 結構
description: 本節包含 Windows 影像處理元件 (WIC) 結構的相關資訊。
ms.assetid: 85025aee-6ce3-45ae-bc53-45988b6622ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffffa3e9f7ae66192eba1dba747532af9b7a2c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980995"
---
# <a name="wic-structures"></a><span data-ttu-id="370b7-103">WIC 結構</span><span class="sxs-lookup"><span data-stu-id="370b7-103">WIC structures</span></span>

<span data-ttu-id="370b7-104">本節包含 Windows 影像處理元件 (WIC) 結構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="370b7-104">This section contains information about the Windows Imaging Component (WIC) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="370b7-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="370b7-105">In this section</span></span>



| <span data-ttu-id="370b7-106">主題</span><span class="sxs-lookup"><span data-stu-id="370b7-106">Topic</span></span>                                                                          | <span data-ttu-id="370b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="370b7-107">Description</span></span>                                                                                                                   |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="370b7-108">**WICBitmapPattern**</span><span class="sxs-lookup"><span data-stu-id="370b7-108">**WICBitmapPattern**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmappattern)<br/>             | <span data-ttu-id="370b7-109">包含成員，這些成員可在影像檔案中識別可用於識別特定格式的模式。</span><span class="sxs-lookup"><span data-stu-id="370b7-109">Contains members that identify a pattern within an image file which can be used to identify a particular format.</span></span><br/>   |
| [<span data-ttu-id="370b7-110">**WICBitmapPlane**</span><span class="sxs-lookup"><span data-stu-id="370b7-110">**WICBitmapPlane**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane)<br/>                            | <span data-ttu-id="370b7-111">指定平面像素格式之元件平面的像素格式、緩衝區、跨距和大小。</span><span class="sxs-lookup"><span data-stu-id="370b7-111">Specifies the pixel format, buffer, stride and size of a component plane for a planar pixel format.</span></span><br/>                |
| [<span data-ttu-id="370b7-112">**WICBitmapPlaneDescription**</span><span class="sxs-lookup"><span data-stu-id="370b7-112">**WICBitmapPlaneDescription**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplanedescription)<br/>      | <span data-ttu-id="370b7-113">指定元件平面的像素格式和大小。</span><span class="sxs-lookup"><span data-stu-id="370b7-113">Specifies the pixel format and size of a component plane.</span></span><br/>                                                          |
| [<span data-ttu-id="370b7-114">**WICDdsFormatInfo**</span><span class="sxs-lookup"><span data-stu-id="370b7-114">**WICDdsFormatInfo**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicddsformatinfo)<br/>                        | <span data-ttu-id="370b7-115">指定 DDS 格式的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 和區塊資訊。</span><span class="sxs-lookup"><span data-stu-id="370b7-115">Specifies the [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and block information of a DDS format.</span></span><br/>                  |
| [<span data-ttu-id="370b7-116">**WICDdsParameters**</span><span class="sxs-lookup"><span data-stu-id="370b7-116">**WICDdsParameters**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicddsparameters)<br/>                        | <span data-ttu-id="370b7-117">指定包含資料的 DDS 影像維度、 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 和 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="370b7-117">Specifies the DDS image dimension, [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and alpha mode of contained data.</span></span><br/>  |
| [<span data-ttu-id="370b7-118">**WICImageParameters**</span><span class="sxs-lookup"><span data-stu-id="370b7-118">**WICImageParameters**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicimageparameters)<br/>                    | <span data-ttu-id="370b7-119">這會定義參數，您可以用來覆寫在編碼影像時通常使用的預設參數。</span><span class="sxs-lookup"><span data-stu-id="370b7-119">This defines parameters that you can use to override the default parameters normally used when encoding an image.</span></span> <br/> |
| [<span data-ttu-id="370b7-120">**WICJpegFrameHeader**</span><span class="sxs-lookup"><span data-stu-id="370b7-120">**WICJpegFrameHeader**</span></span>](/windows/desktop/api/wincodec/ns-wincodec-wicjpegframeheader)<br/>                    | <span data-ttu-id="370b7-121">表示 JPEG 框架標題。</span><span class="sxs-lookup"><span data-stu-id="370b7-121">Represents a JPEG frame header.</span></span><br/>                                                                                    |
| [<span data-ttu-id="370b7-122">**WICJpegScanHeader**</span><span class="sxs-lookup"><span data-stu-id="370b7-122">**WICJpegScanHeader**</span></span>](/windows/desktop/api/wincodec/ns-wincodec-wicjpegscanheader)<br/>                      | <span data-ttu-id="370b7-123">表示 JPEG 框架標題。</span><span class="sxs-lookup"><span data-stu-id="370b7-123">Represents a JPEG frame header.</span></span><br/>                                                                                    |
| [<span data-ttu-id="370b7-124">**WICMetadataHeader**</span><span class="sxs-lookup"><span data-stu-id="370b7-124">**WICMetadataHeader**</span></span>](/windows/desktop/api/Wincodecsdk/ns-wincodecsdk-wicmetadataheader)<br/>           | <span data-ttu-id="370b7-125">表示中繼資料標頭。</span><span class="sxs-lookup"><span data-stu-id="370b7-125">Represents metadata header.</span></span><br/>                                                                                        |
| [<span data-ttu-id="370b7-126">**WICMetadataPattern**</span><span class="sxs-lookup"><span data-stu-id="370b7-126">**WICMetadataPattern**</span></span>](/windows/desktop/api/Wincodecsdk/ns-wincodecsdk-wicmetadatapattern)<br/>         | <span data-ttu-id="370b7-127">表示中繼資料模式。</span><span class="sxs-lookup"><span data-stu-id="370b7-127">Represents a metadata pattern.</span></span><br/>                                                                                     |
| [<span data-ttu-id="370b7-128">**WICRawCapabilitiesInfo**</span><span class="sxs-lookup"><span data-stu-id="370b7-128">**WICRawCapabilitiesInfo**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo)<br/> | <span data-ttu-id="370b7-129">定義原始編解碼器的能力。</span><span class="sxs-lookup"><span data-stu-id="370b7-129">Defines raw codec capabilites.</span></span><br/>                                                                                     |
| [<span data-ttu-id="370b7-130">**WICRawToneCurve**</span><span class="sxs-lookup"><span data-stu-id="370b7-130">**WICRawToneCurve**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve)<br/>               | <span data-ttu-id="370b7-131">表示原始影像音調曲線。</span><span class="sxs-lookup"><span data-stu-id="370b7-131">Represents a raw image tone curve.</span></span><br/>                                                                                 |
| [<span data-ttu-id="370b7-132">**WICRawToneCurvePoint**</span><span class="sxs-lookup"><span data-stu-id="370b7-132">**WICRawToneCurvePoint**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint)<br/>     | <span data-ttu-id="370b7-133">表示原始影像音調曲線點。</span><span class="sxs-lookup"><span data-stu-id="370b7-133">Represents a raw image tone curve point.</span></span><br/>                                                                           |
| [<span data-ttu-id="370b7-134">**WICRect**</span><span class="sxs-lookup"><span data-stu-id="370b7-134">**WICRect**</span></span>](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)<br/>                               | <span data-ttu-id="370b7-135">表示 WIC API 的矩形。</span><span class="sxs-lookup"><span data-stu-id="370b7-135">Represents a rectangle for WIC API.</span></span><br/>                                                                                |



 

 

