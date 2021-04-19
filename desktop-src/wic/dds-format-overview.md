---
description: 提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: DDS 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986962"
---
# <a name="dds-format-overview"></a><span data-ttu-id="11369-103">DDS 格式總覽</span><span class="sxs-lookup"><span data-stu-id="11369-103">DDS Format Overview</span></span>

<span data-ttu-id="11369-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 DDS 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="11369-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="11369-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="11369-105">Codec Identity</span></span>

<span data-ttu-id="11369-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="11369-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="11369-107"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="11369-107">Formal Name(s)</span></span>         | <span data-ttu-id="11369-108">DirectDraw 介面</span><span class="sxs-lookup"><span data-stu-id="11369-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="11369-109">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="11369-109">File Name Extension(s)</span></span> | <span data-ttu-id="11369-110">Dds</span><span class="sxs-lookup"><span data-stu-id="11369-110">dds</span></span>                |
| <span data-ttu-id="11369-111">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="11369-111">MIME type</span></span>              | <span data-ttu-id="11369-112">image/vnd-ms</span><span class="sxs-lookup"><span data-stu-id="11369-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="11369-113">下表列出用來識別原生 DDS 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11369-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="11369-114">元件</span><span class="sxs-lookup"><span data-stu-id="11369-114">Component</span></span>        | <span data-ttu-id="11369-115">易記名稱</span><span class="sxs-lookup"><span data-stu-id="11369-115">Friendly Name</span></span>            | <span data-ttu-id="11369-116">GUID</span><span class="sxs-lookup"><span data-stu-id="11369-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="11369-117">容器格式</span><span class="sxs-lookup"><span data-stu-id="11369-117">Container Format</span></span> | <span data-ttu-id="11369-118">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="11369-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="11369-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="11369-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="11369-120">解碼器</span><span class="sxs-lookup"><span data-stu-id="11369-120">Decoder</span></span>          | <span data-ttu-id="11369-121">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="11369-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="11369-122">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="11369-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="11369-123">編碼器</span><span class="sxs-lookup"><span data-stu-id="11369-123">Encoder</span></span>          | <span data-ttu-id="11369-124">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="11369-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="11369-125">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="11369-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="11369-126">像素格式支援</span><span class="sxs-lookup"><span data-stu-id="11369-126">Pixel Format Support</span></span>

<span data-ttu-id="11369-127">請注意，DDS 格式支援任何有效的 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值。</span><span class="sxs-lookup"><span data-stu-id="11369-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="11369-128">不過，WIC DDS 編解碼器只支援解碼和編碼包含下列格式的檔案：</span><span class="sxs-lookup"><span data-stu-id="11369-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="11369-129">DXGI \_ 格式 \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="11369-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="11369-130">DXGI \_ 格式 \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="11369-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="11369-131">DXGI \_ 格式 \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="11369-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="11369-132">編碼</span><span class="sxs-lookup"><span data-stu-id="11369-132">Encoding</span></span>

<span data-ttu-id="11369-133">WIC 編碼 Api 設計成與編解碼器無關，因此支援 WIC 的編解碼器影像編碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="11369-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="11369-134">如需使用 WIC API 進行映射編碼的詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="11369-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="11369-135">DDS 檔案格式有獨特的需求，從其對 mipmap 和材質陣列等概念的支援而產生。</span><span class="sxs-lookup"><span data-stu-id="11369-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="11369-136">若要完全控制 DDS 影像編碼的控制權，您應該使用 [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) 介面設定 dds 特定的編碼參數。</span><span class="sxs-lookup"><span data-stu-id="11369-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="11369-137">解碼</span><span class="sxs-lookup"><span data-stu-id="11369-137">Decoding</span></span>

<span data-ttu-id="11369-138">WIC 解碼 Api 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="11369-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="11369-139">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="11369-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="11369-140">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="11369-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="11369-141">封鎖壓縮的資料存取</span><span class="sxs-lookup"><span data-stu-id="11369-141">Block compressed data access</span></span>

<span data-ttu-id="11369-142">除了支援標準 WIC 編解碼器介面之外，DDS 解碼器還可讓您使用特定的 DDS 介面（ [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) 和 [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)），直接存取原生區塊壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="11369-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="11369-143">若要使用這些介面，請分別呼叫 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 和 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)的 QueryInterface。</span><span class="sxs-lookup"><span data-stu-id="11369-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
