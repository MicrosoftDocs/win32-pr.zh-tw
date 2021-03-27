---
title: 第 1 層
description: 本節描述第 1 層支援。
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683019"
---
# <a name="tier-1"></a>第 1 層

本節描述第 1 層支援。

-   硬體至少為功能層級 11.0。
-   無退出支援。
-   無 Texture1D 或 Texture3D 支援。
-   無 2、8 或 16 倍多重採樣消除鋸齒 (MSAA) 支援。 僅需 4x，除非不具 128 bpp 格式。
-   無任何標準拌和模式 (64 KB 磚和結尾 MIP 封裝中的配置依硬體廠商而定)。
-   當有重複的對應時，可以存取磚的限制，如 [圖格存取限制](tile-access-limitations-with-duplicate-mappings-.md)中有重複對應的說明。

### <a name="limitations-affecting-tier-1-only"></a>僅影響第1層的限制

-   並排顯示的資源可以有 **Null** 對應，但是從中讀取或寫入它們都會產生未定義的結果，包括移除的裝置。 應用程式能將虛設頁對應至所有空白的區域來避免發生此情況。 如果您要撰寫和轉譯至對應至多個轉譯目標位置的頁面，請務必小心，因為寫入順序將會是未定義的。
-   無著色器指示可供鉗制 LOD 與對應狀態回應使用。 如需詳細資訊，請參閱 HLSL 並排顯示 [資源暴露](hlsl-tiled-resources-exposure.md)。
-   標準磚圖形的對齊條件約束：只保證 mips (從最精細的) 開始，其維度是標準圖格大小的倍數都支援標準磚圖形，而且可以有任意對應/取消對應的個別磚。 磚資源中的第一個 mipmap，其維度不是標準磚大小的倍數，而且所有的 mipmap 都有很大的，可以有非標準的並排顯示圖形，一次就能為這組 mips 設定 N 64KB 的磚， (N 回報給應用程式) 。 這些 N 磚被壓縮為一個單位，而且在任何時候都必須由應用程式完全對應或完全不對應，但是每個 N 磚都可以對應至磚集區中的任意斷續位置。
-   在所有維度中，以任何 mipmap 不是標準磚大小的倍數來分割資源，都不能有大於1的陣列大小。
-   若要透過 [緩衝區](overviews-direct3d-11-resources-buffers.md) 資源切換磚集區中的圖格，以透過 [材質](overviews-direct3d-11-resources-textures.md) 資源參考相同的圖格，或相反的，則最新的 [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) 或 [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) 呼叫，會將對應加入至這些磚集區磚的相同資源維度， (緩衝區和材質 \*) 作為用來存取磚的資源維度。 否則，行為未定義，包括裝置重設的機會。 舉例來說，例如，呼叫 **UpdateTileMappings** 來定義緩衝區的圖格對應，然後透過 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)資源 **UpdateTileMappings** 至磚集區中的相同磚，然後透過緩衝區存取磚就會無效。 您可以在切換緩衝區和紋理 (反之亦然) 之間分享的磚時為資源重新定義磚，或是不在緩衝區資源和紋理資源之間分享磚集區中的磚，以避免這種情形。
-   不支援最小/最大削減篩選。 如需 Min/Max 縮減篩選的詳細資訊，請參閱並排顯示的 [資源紋理取樣功能](tiled-resources-texture-sampling-features.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源功能層級](tiled-resources-features-tiers.md)
</dt> </dl>

 

 