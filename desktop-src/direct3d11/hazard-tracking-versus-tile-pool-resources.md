---
title: 危險追蹤與磚集區資源
description: 針對非並排顯示的資源，Direct3D 可以在轉譯期間防止特定的危險情況，但因為危險追蹤是在並排顯示的資源圖層級上，所以在呈現並排顯示的資源時追蹤危險的情況可能會太昂貴。
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371914"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="cda30-103">危險追蹤與磚集區資源</span><span class="sxs-lookup"><span data-stu-id="cda30-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="cda30-104">針對非並排顯示的資源，Direct3D 可以在轉譯期間防止特定的危險情況，但因為危險追蹤是在並排顯示的資源圖層級上，所以在呈現並排顯示的資源時追蹤危險的情況可能會太昂貴。</span><span class="sxs-lookup"><span data-stu-id="cda30-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="cda30-105">例如，針對非並排顯示的資源，執行時間不允許將任何指定的 SubResource 系結為輸入 (例如 ShaderResourceView) 和輸出 (，例如 RenderTargetView) 。</span><span class="sxs-lookup"><span data-stu-id="cda30-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="cda30-106">如果遇到這種情況，則執行時間會將輸入解除系結。</span><span class="sxs-lookup"><span data-stu-id="cda30-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="cda30-107">執行時間中的這項追蹤額外負荷很便宜，而且是在 SubResource 層級進行。</span><span class="sxs-lookup"><span data-stu-id="cda30-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="cda30-108">此追蹤額外負荷的其中一個優點是意外降低應用的機率，根據硬體著色器執行順序而定。</span><span class="sxs-lookup"><span data-stu-id="cda30-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="cda30-109">硬體著色器執行順序可能不同，如果不在特定圖形處理單元 (GPU) 上，那麼當然會跨不同的 GPU。</span><span class="sxs-lookup"><span data-stu-id="cda30-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="cda30-110">追蹤資源系結的方式可能太昂貴，因為追蹤是在磚層級上。</span><span class="sxs-lookup"><span data-stu-id="cda30-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="cda30-111">出現新的問題，例如，可能會驗證嘗試轉譯至 RenderTargetView，而其中一個圖格同時對應至介面中的多個區域。</span><span class="sxs-lookup"><span data-stu-id="cda30-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="cda30-112">如果這類每個磚危險追蹤對於執行階段來說太昂貴，理想上至少會是偵錯層的選項。</span><span class="sxs-lookup"><span data-stu-id="cda30-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="cda30-113">當應用程式發出寫入或讀取作業給已並排的資源（參考磚集區記憶體）時，應用程式必須通知顯示驅動程式，而這項作業在後續的讀取或寫入作業中，將會被個別的並排顯示資源參考，讓您在執行下列作業之前必須先完成第一項作業。</span><span class="sxs-lookup"><span data-stu-id="cda30-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="cda30-114">如需此狀況的詳細資訊，請參閱 [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) 備註。</span><span class="sxs-lookup"><span data-stu-id="cda30-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cda30-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="cda30-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cda30-116">對應在磚集區中</span><span class="sxs-lookup"><span data-stu-id="cda30-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




