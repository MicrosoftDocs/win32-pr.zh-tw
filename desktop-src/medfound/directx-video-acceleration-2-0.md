---
description: DirectX Video 加速2。0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: DirectX Video 加速2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191057"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="2a6a6-103">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="2a6a6-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="2a6a6-104">DirectX Video 加速 (DXVA) 是 API 和對應的 DDI，可使用硬體加速來加速影片編解碼器處理。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="2a6a6-105">軟體編解碼器和軟體視頻處理器可以使用 DXVA，將某些需要大量 CPU 的作業卸載至 GPU。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="2a6a6-106">例如，軟體解碼器可以卸載反向離散余弦轉換 (iDCT) 至 GPU。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="2a6a6-107">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2a6a6-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="2a6a6-108">In this section</span></span>



| <span data-ttu-id="2a6a6-109">主題</span><span class="sxs-lookup"><span data-stu-id="2a6a6-109">Topic</span></span>                                                                                             | <span data-ttu-id="2a6a6-110">描述</span><span class="sxs-lookup"><span data-stu-id="2a6a6-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a6a6-111">關於 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="2a6a6-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="2a6a6-112">DXVA 2 以及其與 DXVA 1 的關聯性總覽。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="2a6a6-113">Direct3D 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="2a6a6-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="2a6a6-114">Microsoft Direct3D 裝置管理員可讓兩個或多個物件共用相同的 Microsoft Direct3D 9 裝置。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2a6a6-115">支援 DirectShow 中的 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="2a6a6-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="2a6a6-116">本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="2a6a6-117">媒體基礎中支援 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="2a6a6-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="2a6a6-118">本主題說明如何在使用 Direct3D 9 的媒體基礎轉換 (MFT) 中，支援 DXVA) 2.0 的 DirectX 影片加速 (</span><span class="sxs-lookup"><span data-stu-id="2a6a6-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="2a6a6-119">DXVA 影片處理</span><span class="sxs-lookup"><span data-stu-id="2a6a6-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="2a6a6-120">DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="2a6a6-121">影片處理服務包含去交錯和影片混合。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="2a6a6-122">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="2a6a6-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="2a6a6-123">Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。</span><span class="sxs-lookup"><span data-stu-id="2a6a6-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="2a6a6-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a6a6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a6a6-125">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2a6a6-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2a6a6-126">DXVA 1 規格</span><span class="sxs-lookup"><span data-stu-id="2a6a6-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
