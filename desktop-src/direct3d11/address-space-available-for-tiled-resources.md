---
title: 磚資源可用的位址空間
description: 此區段會指定可用於並排顯示資源的虛擬位址空間。
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "103679084"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="01753-103">磚資源可用的位址空間</span><span class="sxs-lookup"><span data-stu-id="01753-103">Address space available for tiled resources</span></span>

<span data-ttu-id="01753-104">此區段會指定可用於並排顯示資源的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="01753-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="01753-105">在 64 位元作業系統上，有至少 40 位元的虛擬位址空間 (1 Tb) 可用。</span><span class="sxs-lookup"><span data-stu-id="01753-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="01753-106">若為 32 位元的作業系統，位址空間為 32 位元 (4 GB)。</span><span class="sxs-lookup"><span data-stu-id="01753-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="01753-107">針對32位 ARM 系統，如果配置使用超過27位的位址空間 (128 MB) ，則建立個別的磚資源可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="01753-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="01753-108">這包括位址中任何隱藏的邊框間距，硬體空間可能會將其用於 Mipmap、壓縮磚邊框間距，以及 2 之乘冪的邊框間距表面維度。</span><span class="sxs-lookup"><span data-stu-id="01753-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="01753-109">在使用不同分頁表的圖形處理器 (GPU) 圖形系統上，應用程式所做的 GPU 資源將可使用多數此種位址空間，即便顯示器驅動程式所做的 GPU 配置可納於相同的空間。</span><span class="sxs-lookup"><span data-stu-id="01753-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="01753-110">在 CPU 和 GPU 所共用之分頁表的未來系統上，處理程序的所有 CPU 和 GPU 配置會共用可用位址空間。</span><span class="sxs-lookup"><span data-stu-id="01753-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01753-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="01753-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01753-112">磚資源建立參數</span><span class="sxs-lookup"><span data-stu-id="01753-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




