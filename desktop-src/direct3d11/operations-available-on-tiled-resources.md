---
title: 磚資源上可用的作業
description: 此區段會列出您可以在並排顯示的資源上執行的作業。
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021872"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="5c273-103">磚資源上可用的作業</span><span class="sxs-lookup"><span data-stu-id="5c273-103">Operations available on tiled resources</span></span>

<span data-ttu-id="5c273-104">此區段會列出您可以在並排顯示的資源上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="5c273-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="5c273-105">void [**ID3D11DeviceCoNtext2：： UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) 和 [**ID3D11DeviceCoNtext2：： CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) 作業-這些作業會將並排資源中的磚位置指向磚集區中的位置，或指向 Null 或兩者。</span><span class="sxs-lookup"><span data-stu-id="5c273-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="5c273-106">這些作業可以更新不相鄰子集的磚指標。</span><span class="sxs-lookup"><span data-stu-id="5c273-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="5c273-107">複製 \* () 和更新 \* () 作業-所有可將資料複製到預設集區介面或從中複製資料的 api (例如， [**ID3D11DeviceCoNtext1：： CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) 和 [**ID3D11DeviceCoNtext1：： UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) 適用于磚化的資源。</span><span class="sxs-lookup"><span data-stu-id="5c273-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="5c273-108">從未對應的磚讀取會產生 0，而對未對應的磚寫入則會捨棄。</span><span class="sxs-lookup"><span data-stu-id="5c273-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="5c273-109">[**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) 和 [**ID3D11DeviceCoNtext2：： UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) 作業-這些作業都是用來在每個磚的資源和標準記憶體配置中的緩衝區資源之間，複製圖格和64kb 的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="5c273-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="5c273-110">顯示器驅動程式和硬體會執行磚資源所需的任何「swizzling」記憶體。</span><span class="sxs-lookup"><span data-stu-id="5c273-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="5c273-111">Direct3D 管線系結和可在非並排顯示的資源上運作的建立/系結，也會在已平鋪的資源上運作。</span><span class="sxs-lookup"><span data-stu-id="5c273-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="5c273-112">磚控制項適用於即時或延遲內容 (就像一般資源的更新)，並且在執行時會影響後續對於磚的存取 (非先前提交的作業)。</span><span class="sxs-lookup"><span data-stu-id="5c273-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c273-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c273-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c273-114">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="5c273-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




