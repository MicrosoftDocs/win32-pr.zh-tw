---
title: 堆積中的子分配
description: 資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103960"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="02985-103">堆積中的子分配</span><span class="sxs-lookup"><span data-stu-id="02985-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="02985-104">資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。</span><span class="sxs-lookup"><span data-stu-id="02985-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02985-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="02985-105">In this section</span></span>



| <span data-ttu-id="02985-106">主題</span><span class="sxs-lookup"><span data-stu-id="02985-106">Topic</span></span>                                                                                       | <span data-ttu-id="02985-107">描述</span><span class="sxs-lookup"><span data-stu-id="02985-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02985-108">記憶體別名和資料繼承</span><span class="sxs-lookup"><span data-stu-id="02985-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="02985-109">放置和保留的資源可能會在堆積內為實體記憶體加上別名。</span><span class="sxs-lookup"><span data-stu-id="02985-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="02985-110">當堆積已設定共用旗標，或當別名的資源有完整定義的記憶體配置時，放置的資源可提供比保留資源更多的資料繼承案例。</span><span class="sxs-lookup"><span data-stu-id="02985-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="02985-111">共用堆積</span><span class="sxs-lookup"><span data-stu-id="02985-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="02985-112">共用適用于多進程和多介面卡架構。</span><span class="sxs-lookup"><span data-stu-id="02985-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="02985-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="02985-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02985-114">**ID3D12Device::CreateHeap**</span><span class="sxs-lookup"><span data-stu-id="02985-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="02985-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="02985-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="02985-116">記憶體管理</span><span class="sxs-lookup"><span data-stu-id="02985-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





