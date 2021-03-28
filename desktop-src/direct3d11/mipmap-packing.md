---
title: Mipmap 封裝
description: 根據並排顯示資源的支援層級，具有特定維度的 mipmap 不會遵循標準磚圖形，而且會被視為以不透明的方式將它們封裝在一起。
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021158"
---
# <a name="mipmap-packing"></a><span data-ttu-id="e5aba-103">Mipmap 封裝</span><span class="sxs-lookup"><span data-stu-id="e5aba-103">Mipmap packing</span></span>

<span data-ttu-id="e5aba-104">根據並排顯示資源的支援 [層級](tiled-resources-features-tiers.md) ，具有特定維度的 mipmap 不會遵循標準磚圖形，而且會被視為以不透明的方式將它們封裝在一起。</span><span class="sxs-lookup"><span data-stu-id="e5aba-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="e5aba-105">較高階層的支援更加保證何種表面維度類型符合標準磚外形 (應用程式可因此個別對應)。</span><span class="sxs-lookup"><span data-stu-id="e5aba-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="e5aba-106">在實值之間有何不同之處，就是在指定並排資源的維度、格式、mipmap 和陣列配量的情況下，每個陣列配量的 mips (的每個數位 M，) 可以封裝成一些 N 個磚。</span><span class="sxs-lookup"><span data-stu-id="e5aba-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="e5aba-107">[**ID3D11Device2：： GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API 存在，可讓驅動程式向應用程式報告 M 和 N (與此 API 所報告的介面相關的其他詳細資料有關，而不會因硬體廠商) 而有所不同。</span><span class="sxs-lookup"><span data-stu-id="e5aba-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="e5aba-108">已封裝的 Mips 的磚組合仍是 64 KB，可以個別對應到磚集區中的不同位置。</span><span class="sxs-lookup"><span data-stu-id="e5aba-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="e5aba-109">但是動態磚的像素形狀，以及 Mipmaps 如何跨過磚組合進行調整因硬體廠商而異，因複雜度過高而無法公開。</span><span class="sxs-lookup"><span data-stu-id="e5aba-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="e5aba-110">因此，應用程式需要每次對應到指定封裝的所有磚，或是都不對應。</span><span class="sxs-lookup"><span data-stu-id="e5aba-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="e5aba-111">否則，用來存取並排資源的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="e5aba-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="e5aba-112">對於陣列式表面，已封裝的 mips 組合以及儲存那些 mips 封裝磚數 (前面描述的 M 和 N)，會針對各陣列配量單獨套用。</span><span class="sxs-lookup"><span data-stu-id="e5aba-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="e5aba-113">用來複製磚的專用 Api ([**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) 和 [**ID3D11DeviceCoNtext2：： UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) 無法存取已封裝的 mips。</span><span class="sxs-lookup"><span data-stu-id="e5aba-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="e5aba-114">想要將資料複製到壓縮的 mips 或從中複製資料的應用程式，可以使用所有非磚資源專屬 Api 來複製和轉譯至表面。</span><span class="sxs-lookup"><span data-stu-id="e5aba-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5aba-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5aba-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5aba-116">磚式資源的區域如何並排顯示</span><span class="sxs-lookup"><span data-stu-id="e5aba-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




