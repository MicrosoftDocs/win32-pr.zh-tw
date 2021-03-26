---
title: 緩衝區拼貼
description: 緩衝資源分為 64KB 的磚，若大小不是 64 KB 的倍數，則最後一個磚會有某些空白空間。
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842356"
---
# <a name="buffer-tiling"></a><span data-ttu-id="2d268-103">緩衝區拼貼</span><span class="sxs-lookup"><span data-stu-id="2d268-103">Buffer tiling</span></span>

<span data-ttu-id="2d268-104">如果大小不是64KB 的倍數，則 [緩衝區](overviews-direct3d-11-resources-buffers.md) 資源會分割成64kb 個磚，並在最後一個磚中顯示一些空白空間。</span><span class="sxs-lookup"><span data-stu-id="2d268-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="2d268-105">結構化的緩衝區對於要並排顯示的分散必須無限制。</span><span class="sxs-lookup"><span data-stu-id="2d268-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="2d268-106">但若一開始就將其並排顯示，便可能失去利用 [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) 所達到的可能硬體效能最佳化。</span><span class="sxs-lookup"><span data-stu-id="2d268-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d268-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d268-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d268-108">磚式資源的區域如何並排顯示</span><span class="sxs-lookup"><span data-stu-id="2d268-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 