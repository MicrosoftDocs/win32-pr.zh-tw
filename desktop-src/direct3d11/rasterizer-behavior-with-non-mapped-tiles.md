---
title: 非對應磚的轉譯器行為
description: 本節說明非對應磚的轉譯器行為。
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990630"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>非對應磚的轉譯器行為

本節說明非對應磚的轉譯器行為。

## <a name="depthstencilview"></a>DepthStencilView

深度樣板檢視 (DSV) 的行為會根據硬體支援程度讀取和寫入。 如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。

以下是理想的行為︰

如果磚在 DepthStencilView 中未對應，讀取深度的傳回值為 0，然後饋入為深度讀取值設定的任何作業。 對遺失的深度磚的寫入會捨棄。 [第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。

## <a name="rendertargetview"></a>RenderTargetView

轉譯目標檢視 (RTV) 的行為會根據硬體支援的層級讀取和寫入。 如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。

在所有實作上，同時繫結的不同 RTV (和 DSV) 可能會有已對應和未對應的不同區域，也會有不同大小的表面格式 (亦即不同磚圖形)。

以下是理想的行為︰

在遺失磚中從 RTV 的讀取傳回 0，寫入會捨棄。 [第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




