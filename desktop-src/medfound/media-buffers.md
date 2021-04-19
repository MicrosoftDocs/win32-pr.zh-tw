---
description: 媒體緩衝區
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: 媒體緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106979855"
---
# <a name="media-buffers"></a><span data-ttu-id="3df8e-103">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="3df8e-103">Media Buffers</span></span>

<span data-ttu-id="3df8e-104">媒體緩衝區是管理記憶體區塊的 COM 物件，通常是用來保存媒體資料。</span><span class="sxs-lookup"><span data-stu-id="3df8e-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="3df8e-105">媒體緩衝區可用來將資料從一個管線元件移至下一個管線元件。</span><span class="sxs-lookup"><span data-stu-id="3df8e-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="3df8e-106">大部分的應用程式不會直接使用媒體緩衝區，因為媒體會話會處理管線物件之間的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="3df8e-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="3df8e-107">如果您要撰寫自己的管線元件，或直接使用管線元件而不使用媒體會話，則必須使用媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df8e-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="3df8e-108">媒體緩衝區會公開 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="3df8e-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="3df8e-109">這個介面是設計用來讀取或寫入任何類型的資料。</span><span class="sxs-lookup"><span data-stu-id="3df8e-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="3df8e-110">未壓縮的影片畫面需要特殊處理，因為它們可能會儲存在位於視訊記憶體的 Direct3D 介面中。</span><span class="sxs-lookup"><span data-stu-id="3df8e-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="3df8e-111">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="3df8e-111">This section contains the following topics.</span></span>



| <span data-ttu-id="3df8e-112">主題</span><span class="sxs-lookup"><span data-stu-id="3df8e-112">Topic</span></span>                                                        | <span data-ttu-id="3df8e-113">描述</span><span class="sxs-lookup"><span data-stu-id="3df8e-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3df8e-114">使用媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="3df8e-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="3df8e-115">描述所有媒體類型之媒體緩衝區的一般行為。</span><span class="sxs-lookup"><span data-stu-id="3df8e-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="3df8e-116">未壓縮的影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="3df8e-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="3df8e-117">如何使用包含未壓縮影片畫面的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3df8e-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="3df8e-118">DirectX 介面緩衝區</span><span class="sxs-lookup"><span data-stu-id="3df8e-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="3df8e-119">說明如何將 Direct3D 介面儲存在媒體緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="3df8e-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="3df8e-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="3df8e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3df8e-121">媒體基礎基本</span><span class="sxs-lookup"><span data-stu-id="3df8e-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



