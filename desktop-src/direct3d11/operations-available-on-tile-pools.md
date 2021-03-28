---
title: 磚集區可用的作業
description: 此區段會列出您可以在磚集區上執行的作業。
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104185998"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="71aba-103">磚集區可用的作業</span><span class="sxs-lookup"><span data-stu-id="71aba-103">Operations available on tile pools</span></span>

<span data-ttu-id="71aba-104">此區段會列出您可以在磚集區上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="71aba-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="71aba-105">磚集區的存留期與任何其他 Direct3D 資源的運作方式相同，它是由參考計數所支援，包括在此案例中追蹤來自並排顯示資源的對應。</span><span class="sxs-lookup"><span data-stu-id="71aba-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="71aba-106">當應用程式不再參考磚集區以及對於記憶體的任何磚對應消失，並且圖形處理單元 (GPU) 的存取完成時，作業系統便會解除配置磚集區。</span><span class="sxs-lookup"><span data-stu-id="71aba-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="71aba-107">與介面共用相關的 Api 以及磚集區的同步處理工作， (但不直接在) 的磚資源上。</span><span class="sxs-lookup"><span data-stu-id="71aba-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="71aba-108">類似于所提供之磚集區的行為，如果磚集區已共用且目前由其他裝置和處理常式取得，則會卸載可存取指向磚集區之磚化資源的 Direct3D 命令。</span><span class="sxs-lookup"><span data-stu-id="71aba-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="71aba-109">[**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) 作業</span><span class="sxs-lookup"><span data-stu-id="71aba-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="71aba-110">[**IDXGIDevice2：： OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) 和 [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) 作業-這些 api 可讓您暫時將記憶體提供給系統， (，且不適用於個別的並排資源) 。</span><span class="sxs-lookup"><span data-stu-id="71aba-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="71aba-111">如果已並排的資源指向所提供磚集區中的圖格，則並排顯示的資源行為會如同 (所提供的一樣，例如執行時間會卸載參考它的命令) 。</span><span class="sxs-lookup"><span data-stu-id="71aba-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="71aba-112">資料無法直接在磚集區記憶體中來回複製。</span><span class="sxs-lookup"><span data-stu-id="71aba-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="71aba-113">記憶體的存取一律是透過並排顯示的資源來完成。</span><span class="sxs-lookup"><span data-stu-id="71aba-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71aba-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="71aba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71aba-115">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="71aba-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 