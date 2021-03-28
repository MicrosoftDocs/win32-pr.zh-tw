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
# <a name="hazard-tracking-versus-tile-pool-resources"></a>危險追蹤與磚集區資源

針對非並排顯示的資源，Direct3D 可以在轉譯期間防止特定的危險情況，但因為危險追蹤是在並排顯示的資源圖層級上，所以在呈現並排顯示的資源時追蹤危險的情況可能會太昂貴。

例如，針對非並排顯示的資源，執行時間不允許將任何指定的 SubResource 系結為輸入 (例如 ShaderResourceView) 和輸出 (，例如 RenderTargetView) 。 如果遇到這種情況，則執行時間會將輸入解除系結。 執行時間中的這項追蹤額外負荷很便宜，而且是在 SubResource 層級進行。 此追蹤額外負荷的其中一個優點是意外降低應用的機率，根據硬體著色器執行順序而定。 硬體著色器執行順序可能不同，如果不在特定圖形處理單元 (GPU) 上，那麼當然會跨不同的 GPU。

追蹤資源系結的方式可能太昂貴，因為追蹤是在磚層級上。 出現新的問題，例如，可能會驗證嘗試轉譯至 RenderTargetView，而其中一個圖格同時對應至介面中的多個區域。 如果這類每個磚危險追蹤對於執行階段來說太昂貴，理想上至少會是偵錯層的選項。

當應用程式發出寫入或讀取作業給已並排的資源（參考磚集區記憶體）時，應用程式必須通知顯示驅動程式，而這項作業在後續的讀取或寫入作業中，將會被個別的並排顯示資源參考，讓您在執行下列作業之前必須先完成第一項作業。 如需此狀況的詳細資訊，請參閱 [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) 備註。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對應在磚集區中](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




