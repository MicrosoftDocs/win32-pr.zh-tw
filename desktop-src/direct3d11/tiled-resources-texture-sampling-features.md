---
title: 磚資源紋理取樣功能
description: 本節說明並排顯示的資源紋理取樣功能。
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682714"
---
# <a name="tiled-resources-texture-sampling-features"></a>磚資源紋理取樣功能

本節說明並排顯示的資源紋理取樣功能。

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>磚資源紋理取樣功能的需求

此處所述的材質取樣功能需要 [第2層層](tier-2.md) 級的並排資源支援。

## <a name="shader-feedback-about-mapped-areas"></a>對應區域的著色器意見反應

讀取及/或寫入磚資源的任何著色器指令都會導致狀態資訊記錄。 這個狀態公開為進入 32 位元暫時暫存器之每個資源存取指令的選擇性額外傳回值。 傳回值的內容是不透明。 也就是，不允許著色器程式直接讀取。 但是，您可以使用 [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) 函式來擷取狀態資訊。

## <a name="fully-mapped-check"></a>完全對應檢查

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) 函式解譯從記憶體存取傳回的狀態，並指出存取的所有資料是否都在資源中對應。 如果資料已對應，**CheckAccessFullyMapped** 傳回 true (0xFFFFFFFF)，如果資料未對應則傳回 false (0x00000000)。

在篩選作業時，有時候特定紋素的加權會變成 0.0。 一個範例是紋理座標直接落在紋素中心的線性樣本：3 個其他紋素 (有哪些可能因硬體而不同) 貢獻到篩選，但具有 0 加權。 這些 0 加權紋素完全不會貢獻到篩選結果，如果它們恰巧落在 **NULL** 磚，它們不算是未對應的存取。 請注意，相同的保證適用於包括多個 mip 層級的紋理篩選；如果其中一個 mipmap 的紋素未對應，但在那些紋素的加權是 0，那些紋素不算是未對應的存取。

從具有少於4個元件的格式進行取樣 (例如 DXGI \_ 格式 \_ R8 \_ UNORM) ，任何落在 **null** 磚上的材質都會導致回報 **null** 對應存取，不論著色器實際在結果中查看哪些元件。 例如，從 R8 UNORM 讀取 \_ 和遮罩著色器中的讀取結果（使用. gba/. yzw 根本不需要讀取紋理）。 但如果紋素位址是 **NULL** 對應磚，作業仍然算是 **NULL** 對應存取。

著色器可以檢查狀態，並在失敗時追求任何您想要的動作過程。 例如，動作過程可以是記錄「遺漏」(例如透過 UAV 寫入) 和/或發出另一個讀取 (鉗制到已知對應的更粗略 LOD)。 應用程式可能也要追蹤成功存取，以了解對應磚集的哪個部分被存取。

記錄的一個複雜問題是沒有機制存在回報一組確切的磚被存取。 應用程式可以根據其用於存取的座標來進行保守猜測，以及使用」 LOD 指令 (例如， [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)) 傳回硬體」 lod 計算。

另一個問題是，許多存取會到同一個磚，所以會發生許多重複記錄和可能記憶體競爭。 如果硬體有選項，在之前其他地方有報告時，不需要為了報告磚存取而擔心，則可能很便利。 或許這類追蹤的狀態可能從 API 重設 (可能在畫面界限)。

## <a name="per-sample-minlod-clamp"></a>每個樣本 MinLOD 鉗制

為了協助著色器避免 mipmapped 中的區域被視為非對應的資源，大部分涉及使用取樣器 (篩選) 的著色器指令都有新的模式，可讓著色器將額外的 float32 MinLOD 夾具參數傳遞給紋理範例。 這個值位於檢視的 mipmap 數字空間，而不是基礎資源。

硬體會在」 LOD 計算中的相同位置執行 [**最大**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max) (FShaderMinLODClamp、fComputedLOD) ，其中每個資源 MinLOD 的夾具也是 **最大** () 。

如果套用每個樣本 LOD 鉗制和定義於取樣器之任何其他 LOD 鉗制的結果是空集合，結果是和每個資源 minLOD 鉗制相同的超出範圍存取結果：0 表示表面格式中的元件，預設值表示遺失元件。

」 LOD 指令 (例如， [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)) ，它會比此處所述的每個樣本 minLOD 夾具，同時傳回壓制和 unclamped」 lod。 從這個 LOD 指令傳回的鉗制 LOD 反映所有鉗制，包括每個資源鉗制，但不是每個樣本鉗制。 每個樣本鉗制是由著色器控制和所知，因此著色器作者如有需要可以手動將該鉗制套用至 LOD 指令的傳回值。

## <a name="minmax-reduction-filtering"></a>最小/最大削減篩選

應用程式可以選擇管理自己的資料結構，以通知它們對應的磚資源外觀。 其中一個範例就是一個介面，其中包含的材質可保存磚資源內每個磚的資訊。 有人可能會儲存在特定磚位置對應的第一個 LOD。 藉由仔細取樣此資料結構的方式，就像是要取樣並排顯示的資源，可能會發現完全對應的最小」 LOD 是整個材質篩選器使用量的最小值。 為了讓這個程序更容易，Direct3D 11.2 引進新的通用取樣器模式，最小/最大篩選。

LOD 追蹤的最小/最大篩選公用程式可能對其他用途有用，例如，也許是深度表面篩選。

最小/最大減少篩選是取樣器上的模式，會擷取一般紋理篩選擷取的一組相同的紋素。 但是，它會依據每個元素傳回所擷取紋素的 min() 或 max() (例如，所有 R 值的最小值，與所有 G 值的最小值分開，以此類推)，而不是混合值以產生答案。

最小/最大作業遵循 Direct3D 算術精確度規則。 比較的順序並不重要。

在不是最小/最大的篩選作業時，有時候特定紋素的加權會變成 0.0。 其中一個範例是具有材質座標的線性範例，直接落在材質 center-3 個其他材質 (它們可能會因硬體而異) 對篩選準則有所差異，但有0權數。 對於在非最小/最大篩選上 0 加權的任何紋素，如果篩選是最小/最大，這些紋素仍然不會貢獻到結果 (而且加權不會影響最小/最大篩選作業)。

篩選模式的完整清單會以列舉值的最小值和最大值顯示在 [**D3D11 \_ 濾波器**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) 列舉中。

這項功能的支援取決於圖層資源的 [第2層](tier-2.md) 支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 