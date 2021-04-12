---
title: WIC 程式設計指南
description: 說明如何使用 WIC Api。
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386234"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="0762e-103">WIC 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0762e-103">WIC programming guide</span></span>

<span data-ttu-id="0762e-104">本節包含描述如何使用 Windows 影像處理元件 (WIC) Api 的概念性主題。</span><span class="sxs-lookup"><span data-stu-id="0762e-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0762e-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="0762e-105">In this section</span></span>



| <span data-ttu-id="0762e-106">主題</span><span class="sxs-lookup"><span data-stu-id="0762e-106">Topic</span></span>                                                                                 | <span data-ttu-id="0762e-107">描述</span><span class="sxs-lookup"><span data-stu-id="0762e-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0762e-108">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="0762e-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="0762e-109">WIC 提供可延伸的架構，可用於處理影像和影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0762e-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="0762e-110">WIC API 總覽</span><span class="sxs-lookup"><span data-stu-id="0762e-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="0762e-111">WIC 提供元件物件模型 (COM) 型 API，以用於 C 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="0762e-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="0762e-112">解碼數位影像</span><span class="sxs-lookup"><span data-stu-id="0762e-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="0762e-113">本節包含描述 WIC 點陣圖解碼器的概念和使用說明主題，這些是用來解碼數位影像。</span><span class="sxs-lookup"><span data-stu-id="0762e-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="0762e-114">使用影像資料</span><span class="sxs-lookup"><span data-stu-id="0762e-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="0762e-115">本節包含描述 WIC 點陣圖來源的概念和使用說明主題，以及如何操作它們。</span><span class="sxs-lookup"><span data-stu-id="0762e-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="0762e-116">編碼影像資料</span><span class="sxs-lookup"><span data-stu-id="0762e-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="0762e-117">本節包含描述 WIC 點陣圖編碼器的概念和使用說明主題，這些編碼器是用來編碼數位影像。</span><span class="sxs-lookup"><span data-stu-id="0762e-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="0762e-118">原生 WIC 編解碼器</span><span class="sxs-lookup"><span data-stu-id="0762e-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="0762e-119">本節包含 WIC 中可用之原生映射編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0762e-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="0762e-120">處理影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="0762e-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="0762e-121">本節包含描述 WIC 中繼資料系統的概念主題。</span><span class="sxs-lookup"><span data-stu-id="0762e-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="0762e-122">JPEG YCbCr 支援</span><span class="sxs-lookup"><span data-stu-id="0762e-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="0762e-123">從 Windows 8.1 開始， [Windows 影像處理元件 (WIC) ](-wic-about-windows-imaging-codec.md) JPEG 編解碼器可支援在其原生 YC<sub>b</sub>C<sub>r</sub> 表單中讀取和寫入影像資料。</span><span class="sxs-lookup"><span data-stu-id="0762e-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="0762e-124">色彩管理</span><span class="sxs-lookup"><span data-stu-id="0762e-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="0762e-125">WIC 提供 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 介面和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) 介面，以簡化色彩管理。</span><span class="sxs-lookup"><span data-stu-id="0762e-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="0762e-126">元件開發</span><span class="sxs-lookup"><span data-stu-id="0762e-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="0762e-127">WIC 是可擴充的平臺，可提供低層級的 API 來進行數位映射。</span><span class="sxs-lookup"><span data-stu-id="0762e-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="0762e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0762e-128">See Also</span></span>

[<span data-ttu-id="0762e-129">WIC 參考</span><span class="sxs-lookup"><span data-stu-id="0762e-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="0762e-130">WIC 範例</span><span class="sxs-lookup"><span data-stu-id="0762e-130">WIC Samples</span></span>](-wic-samples.md)


 

 




