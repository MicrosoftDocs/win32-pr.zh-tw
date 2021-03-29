---
title: 建立磚集區
description: 磚集區會透過 ID3D11Device CreateBuffer API 來建立，其方式是 \_ \_ \_ \_ 在 \_ D3D11 參數指向之 PDesc 緩衝區 DESC 結構的 MiscFlags 成員中傳遞 D3D11 資源其他磚集區旗標 \_ 。
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990590"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="7b2f5-103">建立磚集區</span><span class="sxs-lookup"><span data-stu-id="7b2f5-103">Tile pool creation</span></span>

<span data-ttu-id="7b2f5-104">磚集區會透過 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API 來建立，其方式是在 *D3D11* 參數指向之 [**PDesc \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構的 **MiscFlags** 成員中傳遞 [**D3D11 \_ 資源 \_ 其他 \_ 磚 \_ 集**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)區旗標。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="7b2f5-105">應用程式可以在每一個 Direct3D 裝置建立一個或多個磚集區。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="7b2f5-106">每個磚集區的大小總和限制為 Direct3D 11 的資源大小上限，也就是約為圖形處理器 (GPU) RAM 的 1/4。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="7b2f5-107">磚集區由 64 KB 磚所組成，但作業系統 (顯示驅動程式) 會在幕後將整個集區作為一或多個配置來管理，但應用程式看不到分解過程。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="7b2f5-108">並排顯示的資源會藉由指向磚集區內的磚來定義內容。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="7b2f5-109">將磚指向 **Null**，即可將磚從並排的資源取消對應。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="7b2f5-110">這類未對應的磚具有讀取或寫入行為的相關規則。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="7b2f5-111">如需詳細資訊，請參閱 [危險追蹤與磚集區資源](hazard-tracking-versus-tile-pool-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="7b2f5-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b2f5-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b2f5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2f5-113">對應在磚集區中</span><span class="sxs-lookup"><span data-stu-id="7b2f5-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




