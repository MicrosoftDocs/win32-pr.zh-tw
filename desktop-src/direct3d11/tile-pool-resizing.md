---
title: 調整磚集區大小
description: 如果應用程式需要更多的工作集，以將並排顯示的資源對應至磚集區，或如果需要較少的空間，請使用 ID3D11DeviceCoNtext2 ResizeTilePool API 來放大磚集區。
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839436"
---
# <a name="tile-pool-resizing"></a><span data-ttu-id="2b14a-103">調整磚集區大小</span><span class="sxs-lookup"><span data-stu-id="2b14a-103">Tile pool resizing</span></span>

<span data-ttu-id="2b14a-104">如果應用程式需要更多的工作集，以將並排顯示的資源對應至磚集區，或如果需要較少的空間，請使用 [**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) API 來放大磚集區。</span><span class="sxs-lookup"><span data-stu-id="2b14a-104">Use the [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) API to grow a tile pool if the application needs more working set for the tiled resources mapping into it or to shrink if less space is needed.</span></span> <span data-ttu-id="2b14a-105">應用程式的另一個選項是為新的磚資源配置額外的磚集區。</span><span class="sxs-lookup"><span data-stu-id="2b14a-105">Another option for applications is to allocate additional tile pools for new tiled resources.</span></span> <span data-ttu-id="2b14a-106">但是，如果任何單一併排顯示的資源需要的空間比其磚集區一開始提供的空間還要多，則成長圖格集區是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="2b14a-106">But if any single tiled resource needs more space than initially available in its tile pool, growing the tile pool is a good option.</span></span> <span data-ttu-id="2b14a-107">並排顯示的資源無法同時對應到多個磚集區。</span><span class="sxs-lookup"><span data-stu-id="2b14a-107">A tiled resource can't have mappings into multiple tile pools at the same time.</span></span>

<span data-ttu-id="2b14a-108">當磚集區大小增加時，顯示驅動程式會透過一個或多個新配置，以在尾端新增額外的磚。</span><span class="sxs-lookup"><span data-stu-id="2b14a-108">When a tile pool is grown, additional tiles are added to the end via one or more new allocations by the display driver.</span></span> <span data-ttu-id="2b14a-109">應用程式看不到這項分解至配置的過程。</span><span class="sxs-lookup"><span data-stu-id="2b14a-109">This breakdown into allocations isn't visible to the application.</span></span> <span data-ttu-id="2b14a-110">磚集區中的現有記憶體保持不變，而且現有的並排資源對應會維持不變。</span><span class="sxs-lookup"><span data-stu-id="2b14a-110">Existing memory in the tile pool is left untouched, and existing tiled resource mappings into that memory remain intact.</span></span>

<span data-ttu-id="2b14a-111">當磚集區縮小時，會從尾端移除磚。</span><span class="sxs-lookup"><span data-stu-id="2b14a-111">When a tile pool is shrunk, tiles are removed from the end.</span></span> <span data-ttu-id="2b14a-112">磚的數量甚至能低於初始配置大小，最小至 0，這表示新的對應無法超過新的大小。</span><span class="sxs-lookup"><span data-stu-id="2b14a-112">Tiles are removed even below the initial allocation size, down to 0, which means new mappings can't be made past the new size.</span></span> <span data-ttu-id="2b14a-113">不過，超過新大小的現有對應會維持不變，而且依然可以使用。</span><span class="sxs-lookup"><span data-stu-id="2b14a-113">But, existing mappings past the end of the new size remain intact and useable.</span></span> <span data-ttu-id="2b14a-114">只要驅動程式為磚集區記憶體所使用的任何配置對應保持不變，顯示驅動程式就會保留記憶體。</span><span class="sxs-lookup"><span data-stu-id="2b14a-114">The display driver will keep the memory around as long as mappings to any part of the allocations that the driver uses for the tile pool memory remains.</span></span> <span data-ttu-id="2b14a-115">如果在進行縮小後，有一些記憶體因為磚的對應指向它們而保留，然後磚集區大小因應狀況而再次增加的話 (任何數量都算)，則現有的記憶體會被重新使用，之後才會為增加作業提供額外的配置。</span><span class="sxs-lookup"><span data-stu-id="2b14a-115">If after shrinking some memory has been kept alive because tile mappings are pointing to it and then the tile pool is regrown again (by any amount), the existing memory is reused first before any additional allocations occur to service the size of the grow operation.</span></span>

<span data-ttu-id="2b14a-116">若要節省記憶體，應用程式不僅需要縮小磚集區，也需針對最新的小型磚集區大小移除或重新對應現有對應。</span><span class="sxs-lookup"><span data-stu-id="2b14a-116">To be able to save memory, an application has to not only shrink a tile pool but also remove/remap existing mappings past the end of the new smaller tile pool size.</span></span>

<span data-ttu-id="2b14a-117">縮小的動作 (和移除對應) 並不一定會立即省下記憶體。</span><span class="sxs-lookup"><span data-stu-id="2b14a-117">The act of shrinking (and removing mappings) doesn't necessarily produce immediate memory savings.</span></span> <span data-ttu-id="2b14a-118">釋出的記憶體會依顯示驅動程式磚集區基礎配置的細微程度而定。</span><span class="sxs-lookup"><span data-stu-id="2b14a-118">Freeing of memory depends on how granular the display driver's underlying allocations for the tile pool are.</span></span> <span data-ttu-id="2b14a-119">當縮小記憶體的行動會使顯示驅動程式配置無法使用時，顯示驅動程式就無法釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="2b14a-119">When shrinking happens to be enough to make a display driver allocation unused, the display driver can free it.</span></span> <span data-ttu-id="2b14a-120">如果磚集區已經增加的話，縮小至之前的大小 (並相對地移除/重新對應磚對應) 很可能會節省記憶體的空間，但在大小不完全符合顯示驅動程式所選的基礎配置大小時，則不一定。</span><span class="sxs-lookup"><span data-stu-id="2b14a-120">If a tile pool was grown, shrinking to previous sizes (and removing/remapping tile mappings correspondingly) is most likely to yield memory savings, though not guaranteed in the case that the sizes don't exactly align with the underlying allocation sizes chosen by the display driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b14a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b14a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b14a-122">對應在磚集區中</span><span class="sxs-lookup"><span data-stu-id="2b14a-122">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




