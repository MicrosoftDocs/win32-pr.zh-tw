---
title: Direct3D 12 中的記憶體管理
description: 移至 D3D12 牽涉到適當的同步處理和管理記憶體存放區。
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481803"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="e603d-103">Direct3D 12 中的記憶體管理</span><span class="sxs-lookup"><span data-stu-id="e603d-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="e603d-104">移至 D3D12 牽涉到適當的同步處理和管理記憶體存放區。</span><span class="sxs-lookup"><span data-stu-id="e603d-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="e603d-105">管理記憶體存放區表示需要進行更多的同步處理。</span><span class="sxs-lookup"><span data-stu-id="e603d-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="e603d-106">本節涵蓋記憶體管理原則，以及在堆積和緩衝區內的子分配。</span><span class="sxs-lookup"><span data-stu-id="e603d-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="e603d-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="e603d-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="e603d-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="e603d-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="e603d-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="e603d-109">In this section</span></span>



| <span data-ttu-id="e603d-110">主題</span><span class="sxs-lookup"><span data-stu-id="e603d-110">Topic</span></span>                                                                       | <span data-ttu-id="e603d-111">描述</span><span class="sxs-lookup"><span data-stu-id="e603d-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e603d-112">記憶體管理原則</span><span class="sxs-lookup"><span data-stu-id="e603d-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="e603d-113">適用于 Direct3D 12 的記憶體管理員可能會因為所有不同的支援層級（適用于 UMA 或離散 (非 UMA) 介面卡）而變得非常複雜，並且在 GPU 介面卡之間有很大的架構差異。</span><span class="sxs-lookup"><span data-stu-id="e603d-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="e603d-114">本章節所述之 Direct3D 12 記憶體管理的建議策略是「分類、預算和串流」。</span><span class="sxs-lookup"><span data-stu-id="e603d-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="e603d-115">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="e603d-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="e603d-116">緩衝區具有 D3D12 for applications 中所需的所有功能，以將大量暫時性資料從 CPU 傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="e603d-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="e603d-117">本節涵蓋使用和管理資源和緩衝區的四個常見案例。</span><span class="sxs-lookup"><span data-stu-id="e603d-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="e603d-118">堆積中的子分配</span><span class="sxs-lookup"><span data-stu-id="e603d-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="e603d-119">資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。</span><span class="sxs-lookup"><span data-stu-id="e603d-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="e603d-120">居住</span><span class="sxs-lookup"><span data-stu-id="e603d-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="e603d-121">當 GPU 可存取物件時，會將物件視為 *駐留* 。</span><span class="sxs-lookup"><span data-stu-id="e603d-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="e603d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e603d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e603d-123">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e603d-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e603d-124">資源系結</span><span class="sxs-lookup"><span data-stu-id="e603d-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





