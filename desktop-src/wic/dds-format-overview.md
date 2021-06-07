---
description: 提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: DDS 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444949"
---
# <a name="dds-format-overview"></a><span data-ttu-id="6d630-103">DDS 格式總覽</span><span class="sxs-lookup"><span data-stu-id="6d630-103">DDS Format Overview</span></span>

<span data-ttu-id="6d630-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d630-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="6d630-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="6d630-105">Codec Identity</span></span>

<span data-ttu-id="6d630-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="6d630-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="6d630-107">元件</span><span class="sxs-lookup"><span data-stu-id="6d630-107">Component</span></span>              | <span data-ttu-id="6d630-108">描述</span><span class="sxs-lookup"><span data-stu-id="6d630-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="6d630-109"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="6d630-109">Formal Name(s)</span></span>         | <span data-ttu-id="6d630-110">DirectDraw 介面</span><span class="sxs-lookup"><span data-stu-id="6d630-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="6d630-111">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="6d630-111">File Name Extension(s)</span></span> | <span data-ttu-id="6d630-112">Dds</span><span class="sxs-lookup"><span data-stu-id="6d630-112">dds</span></span>                |
| <span data-ttu-id="6d630-113">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="6d630-113">MIME type</span></span>              | <span data-ttu-id="6d630-114">image/vnd-ms</span><span class="sxs-lookup"><span data-stu-id="6d630-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="6d630-115">下表列出用來識別原生 DDS 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="6d630-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="6d630-116">元件</span><span class="sxs-lookup"><span data-stu-id="6d630-116">Component</span></span>        | <span data-ttu-id="6d630-117">易記名稱</span><span class="sxs-lookup"><span data-stu-id="6d630-117">Friendly Name</span></span>            | <span data-ttu-id="6d630-118">GUID</span><span class="sxs-lookup"><span data-stu-id="6d630-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="6d630-119">容器格式</span><span class="sxs-lookup"><span data-stu-id="6d630-119">Container Format</span></span> | <span data-ttu-id="6d630-120">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="6d630-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="6d630-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="6d630-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="6d630-122">解碼器</span><span class="sxs-lookup"><span data-stu-id="6d630-122">Decoder</span></span>          | <span data-ttu-id="6d630-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="6d630-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="6d630-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="6d630-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="6d630-125">編碼器</span><span class="sxs-lookup"><span data-stu-id="6d630-125">Encoder</span></span>          | <span data-ttu-id="6d630-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="6d630-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="6d630-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="6d630-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="6d630-128">像素格式支援</span><span class="sxs-lookup"><span data-stu-id="6d630-128">Pixel Format Support</span></span>

<span data-ttu-id="6d630-129">請注意，DDS 格式支援任何有效的 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值。</span><span class="sxs-lookup"><span data-stu-id="6d630-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="6d630-130">不過，WIC DDS 編解碼器只支援解碼和編碼包含下列格式的檔案：</span><span class="sxs-lookup"><span data-stu-id="6d630-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="6d630-131">DXGI \_ 格式 \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6d630-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="6d630-132">DXGI \_ 格式 \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6d630-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="6d630-133">DXGI \_ 格式 \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6d630-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="6d630-134">編碼</span><span class="sxs-lookup"><span data-stu-id="6d630-134">Encoding</span></span>

<span data-ttu-id="6d630-135">WIC 編碼 Api 設計成與編解碼器無關，因此支援 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="6d630-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="6d630-136">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="6d630-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="6d630-137">DDS 檔案格式有獨特的需求，從其對 mipmap 和材質陣列等概念的支援而產生。</span><span class="sxs-lookup"><span data-stu-id="6d630-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="6d630-138">若要完全控制 DDS 影像編碼的控制權，您應該使用 [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) 介面設定 dds 特定的編碼參數。</span><span class="sxs-lookup"><span data-stu-id="6d630-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="6d630-139">解碼</span><span class="sxs-lookup"><span data-stu-id="6d630-139">Decoding</span></span>

<span data-ttu-id="6d630-140">WIC 解碼 Api 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="6d630-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="6d630-141">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="6d630-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="6d630-142">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="6d630-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="6d630-143">封鎖壓縮的資料存取</span><span class="sxs-lookup"><span data-stu-id="6d630-143">Block compressed data access</span></span>

<span data-ttu-id="6d630-144">除了支援標準 WIC 編解碼器介面之外，DDS 解碼器還可讓您使用特定的 DDS 介面（ [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) 和 [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)），直接存取原生區塊壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="6d630-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="6d630-145">若要使用這些介面，請分別呼叫 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 和 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)的 QueryInterface。</span><span class="sxs-lookup"><span data-stu-id="6d630-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
