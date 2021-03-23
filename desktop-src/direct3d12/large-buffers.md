---
title: 在緩衝區內進行子分配
description: 緩衝區具有 D3D12 for applications 中所需的所有功能，以將大量暫時性資料從 CPU 傳送至 GPU。 本節涵蓋使用和管理資源和緩衝區的四個常見案例。
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104117"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="aedf6-104">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="aedf6-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="aedf6-105">緩衝區具有 D3D12 for applications 中所需的所有功能，以將大量暫時性資料從 CPU 傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="aedf6-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="aedf6-106">本節涵蓋使用和管理資源和緩衝區的四個常見案例。</span><span class="sxs-lookup"><span data-stu-id="aedf6-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="aedf6-107">與 D3D11 類似，D3D12 中的應用程式在 D3D12 中配置緩衝區時，仍需要宣告記憶體使用量（相較于 D3D11 中的動態/暫存資源），但在 D3D12 中，開發人員有更大的彈性，而且能更嚴密地控制記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="aedf6-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="aedf6-108">透過子分配的緩衝區具有低層級記憶體管理所需的所有功能。</span><span class="sxs-lookup"><span data-stu-id="aedf6-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aedf6-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="aedf6-109">In this section</span></span>



| <span data-ttu-id="aedf6-110">主題</span><span class="sxs-lookup"><span data-stu-id="aedf6-110">Topic</span></span>                                                                                        | <span data-ttu-id="aedf6-111">描述</span><span class="sxs-lookup"><span data-stu-id="aedf6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aedf6-112">上傳不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="aedf6-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="aedf6-113">示範如何使用一個緩衝區，將常數緩衝區資料和頂點緩衝區資料上傳至 GPU，以及如何適當地子配置和將資料放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="aedf6-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="aedf6-114">使用單一緩衝區可增加記憶體使用量的彈性，並提供應用程式更緊密地控制記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="aedf6-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="aedf6-115">也會顯示 D3D11 和 D3D12 模型之間的差異，以便上傳不同類型的資源。</span><span class="sxs-lookup"><span data-stu-id="aedf6-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="aedf6-116">透過緩衝區上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="aedf6-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="aedf6-117">上傳2D 或3D 紋理資料與上傳1D 資料類似，不同之處在于應用程式必須特別注意與資料列間距相關的資料對齊。</span><span class="sxs-lookup"><span data-stu-id="aedf6-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="aedf6-118">您可以從圖形管線的多個部分 orthogonally 和並行使用緩衝區，而且非常有彈性。</span><span class="sxs-lookup"><span data-stu-id="aedf6-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="aedf6-119">透過緩衝區讀回資料</span><span class="sxs-lookup"><span data-stu-id="aedf6-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="aedf6-120">從 GPU 讀回資料（例如，捕捉螢幕擷取畫面）牽涉到使用 Readback 堆積。</span><span class="sxs-lookup"><span data-stu-id="aedf6-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="aedf6-121">以隔離為基礎的資源管理</span><span class="sxs-lookup"><span data-stu-id="aedf6-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="aedf6-122">示範如何透過延伸來追蹤 GPU 進度，以管理資源資料的生命週期。</span><span class="sxs-lookup"><span data-stu-id="aedf6-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="aedf6-123">記憶體可以有效地重複使用，以管理記憶體中可用空間的可用性，例如在上傳堆積的通道緩衝區執行中。</span><span class="sxs-lookup"><span data-stu-id="aedf6-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="aedf6-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="aedf6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aedf6-125">記憶體管理</span><span class="sxs-lookup"><span data-stu-id="aedf6-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





