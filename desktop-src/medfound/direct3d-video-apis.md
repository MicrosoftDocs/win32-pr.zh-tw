---
description: Direct3D 9 影片 Api
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: Direct3D 9 影片 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510800"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="7f20f-103">Direct3D 9 影片 Api</span><span class="sxs-lookup"><span data-stu-id="7f20f-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f20f-104">Windows Store 應用程式必須使用 Microsoft Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="7f20f-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="7f20f-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="7f20f-105">In this section</span></span>



| <span data-ttu-id="7f20f-106">主題</span><span class="sxs-lookup"><span data-stu-id="7f20f-106">Topic</span></span>                                                                       | <span data-ttu-id="7f20f-107">描述</span><span class="sxs-lookup"><span data-stu-id="7f20f-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f20f-108">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="7f20f-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="7f20f-109">描述圖形驅動程式可提供的影片內容-保護功能。</span><span class="sxs-lookup"><span data-stu-id="7f20f-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="7f20f-110">硬體覆蓋支援</span><span class="sxs-lookup"><span data-stu-id="7f20f-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="7f20f-111">說明如何在 Direct3D 9 中使用硬體覆蓋。</span><span class="sxs-lookup"><span data-stu-id="7f20f-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="7f20f-112">記憶體壓力報告</span><span class="sxs-lookup"><span data-stu-id="7f20f-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="7f20f-113">記憶體壓力報告可讓 Direct3D 應用程式判斷其影片記憶體工作集是否成長過大。</span><span class="sxs-lookup"><span data-stu-id="7f20f-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="7f20f-114">Direct3D Video 介面</span><span class="sxs-lookup"><span data-stu-id="7f20f-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="7f20f-115">描述 Microsoft Direct3D 9 video 介面。</span><span class="sxs-lookup"><span data-stu-id="7f20f-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="7f20f-116">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="7f20f-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="7f20f-117">描述 Direct3D 9 video 介面所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="7f20f-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="7f20f-118">Direct3D 影片列舉</span><span class="sxs-lookup"><span data-stu-id="7f20f-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="7f20f-119">描述 Direct3D 9 video 介面所使用的列舉。</span><span class="sxs-lookup"><span data-stu-id="7f20f-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="7f20f-120">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="7f20f-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="7f20f-121">列出 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法的命令。</span><span class="sxs-lookup"><span data-stu-id="7f20f-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="7f20f-122">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="7f20f-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="7f20f-123">列出 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的查詢。</span><span class="sxs-lookup"><span data-stu-id="7f20f-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="7f20f-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f20f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f20f-125">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="7f20f-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




