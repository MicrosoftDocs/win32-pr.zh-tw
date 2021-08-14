---
title: 預設材質對應
description: 使用預設材質對應可減少在 GPU 和 CPU 之間共用映射資料時的複製和記憶體使用量。
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752288"
---
# <a name="default-texture-mapping"></a>預設材質對應

使用預設材質對應可減少在 GPU 和 CPU 之間共用映射資料時的複製和記憶體使用量。 不過，它應該只在特定情況下使用。 標準 swizzle 配置可避免複製或 swizzling 多個版面配置中的資料。

-   [概觀](#overview)
-   [D3D 11.3 Api](#d3d113-apis)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

對應預設紋理不應為開發人員的第一個選擇。 開發人員應先以獨立 GPU 易懂的方式撰寫程式碼 (也就是，在大部分的材質中都沒有任何 CPU 存取，並以 [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)) 上傳。 但在某些情況下，CPU 和 GPU 可能會在相同的資料上頻繁地互動，而對應的預設材質會變得很有用，以節省電力，或加速特定介面卡或架構上的特定設計。 應用程式應該會偵測到這些情況，並將不必要的複本優化。

在 D3D 11.3 中，使用 D3D11 材質配置所建立的紋理， \_ \_ \_ ([**D3D11 \_ 材質 \_ 版面**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) 配置) 列舉的其中一個成員，且沒有 CPU 存取最有效率的是經常進行 GPU 轉譯和取樣。 當效能測試時，應該針對 \_ \_ 未定義的 D3D11 紋理配置 \_ 與 cpu 存取進行比較，並使用 D3D11 \_ 材質配置 \_ \_ 64k \_ 標準 SWIZZLE （ \_ 具有 cpu 存取）和 D3D11 \_ 材質版面配置資料 \_ \_ 列 \_ 主要來取得跨介面卡支援。

使用 D3D11 \_ 材質 \_ 版面配置 \_ （未定義 CPU 存取）可讓 [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource)、 [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource)、 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (阻止應用程式存取指標) [](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)和取消對應，但可能會犧牲 GPU 存取的效率。 使用 D3D11 \_ 材質 \_ 配置 \_ 64k \_ STANDARD \_ SWIZZLE 搭配 CPU 存取，可讓 **WriteToSubresource**、 **ReadFromSubresource**、Map (傳回應用程式) 和取消 **對應** 的有效指標。 它也可以犧牲 GPU 存取的效率，而不是透過 \_ \_ \_ CPU 存取未定義的 D3D11 材質版面配置。

一般情況下，應用程式應該將大部分的材質建立為僅適用于 GPU 的可存取，而且 D3D11 \_ 材質配置 \_ \_ 未定義。

在對應預設紋理功能的先前，只有一個多維度資料的標準化配置：「線性」，也稱為「資料列主要」。 \_當對應預設值可用時，應用程式應該避免使用暫存和使用 \_ 動態紋理。 使用方式 \_ 暫存和使用 \_ 動態紋理使用線性版面配置。

D3D 11.3 (和 D3D12) 引進標準的多維度資料版面配置。 這樣做的目的是為了讓多個處理單位在相同的資料上運作，而不需要複製資料或在多個配置之間 swizzling 資料。 標準化配置可讓您透過網路效果提高效率，並允許演算法在採用特定模式時進行短暫的剪下。

不過請注意，這個標準 swizzle 是硬體功能，而且可能不受所有 Gpu 支援。

## <a name="d3d113-apis"></a>D3D 11.3 Api

不同于 D3D12，D3D 11.3 預設不支援材質對應，因此您需要查詢 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)。 使用 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 的呼叫以及檢查 `StandardSwizzle64KBSupported` **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2** 的欄位時，也需要查詢標準 swizzle。

下列 Api 參考紋理對應：

列舉

-   [**D3D11 \_材質 \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) 配置：控制預設材質的 swizzle 模式，並啟用預設材質的地圖支援。
-   [**D3D11 \_功能**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) ：參考 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)。
-   [**D3D11 \_磚 \_ 複製 \_ 旗**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) 標：包含可將 swizzled 並排顯示的資源複製到線性緩衝區的旗標。

結構

-   [**D3D11 \_TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) ：描述2d 材質。 請注意 CD3D11 \_ TEXTURE2D \_ DESC1 helper 結構。
-   [**D3D11 \_TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) ：描述3d 紋理。 請注意 CD3D11 \_ TEXTURE3D \_ DESC1 helper 結構。

方法

-   [**ID3D11Device3：： CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) ：建立2d 材質的陣列。
-   [**ID3D11Device3：： CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) ：建立單一3d 紋理。
-   [**ID3D11Device3：： WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) ：會將資料複製到 \_ \_ 使用 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)對應的 D3D11 使用預設材質中。
-   [**ID3D11Device3：： ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) ：從 \_ \_ 使用 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)對應的 D3D11 使用量預設材質複製資料。
-   [**>Id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) ：取得 subresource 中所含資料的指標，並拒絕該 SUBRESOURCE 的 GPU 存取。
-   [**>Id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應：使資源的指標失效，並 reenables GPU 對該資源的存取權。
-   [**ID3D11Texture2D1：： GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) ：取得2d 材質資源的屬性。
-   [**ID3D11Texture3D1：： GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) ：取得3d 紋理資源的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> </dl>

 

 




