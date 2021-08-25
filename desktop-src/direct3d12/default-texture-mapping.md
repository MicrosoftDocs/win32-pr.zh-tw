---
title: UMA 優化 CPU 可存取的材質和標準 Swizzle
description: 通用記憶體架構 (UMA) Gpu 可提供比離散 Gpu 更高的效率，尤其是在針對行動裝置進行優化的情況下。
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2624a300811b4d4a1eef70873a31af89b0546224fd9b4f3ba06ecb1fbd2fac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894668"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>UMA 優化：可存取 CPU 的材質和標準 Swizzle

通用記憶體架構 (UMA) Gpu 可提供比離散 Gpu 更高的效率，尤其是在針對行動裝置進行優化的情況下。 當 GPU 為 UMA 時提供資源 CPU 存取權，可減少在 CPU 與 GPU 之間發生的複製量。 雖然我們不建議應用程式盲目將 CPU 存取權提供給 UMA 設計上的所有資源，但有機會藉由提供正確的資源 CPU 存取來提高效率。 與離散 Gpu 不同的是，CPU 可以有 GPU 可存取的所有資源指標。

-   [瞭解可存取 CPU 的材質](#overview-of-cpu-accessible-textures)
-   [標準 Swizzle 總覽](#overview-of-standard-swizzle)
-   [API](#apis)
-   [相關主題](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>瞭解可存取 CPU 的材質

圖形管線中的 CPU 可存取材質是 UMA 架構的功能，可讓 Cpu 讀取和寫入紋理的存取權。 在較常見的離散 Gpu 上，CPU 無法存取圖形管線中的材質。

紋理的一般最佳作法建議是容納離散 Gpu，通常需要遵循 [透過緩衝區上傳材質資料](upload-and-readback-of-texture-data.md)的程式，摘要如下：

-   大部分的材質都沒有 CPU 存取權。
-   設定紋理配置以 D3D12 \_ 材質配置 \_ \_ 未知。
-   使用 [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)將材質上傳到 GPU。

不過，在某些情況下，CPU 和 GPU 可能會在相同的資料上頻繁地互動，而對應的材質會變得很有用，以節省電力，或加速特定介面卡或架構上的特定設計。 應用程式應該會偵測到這些情況，並將不必要的複本優化。 在此情況下，為了獲得最佳效能，請考慮下列事項：

-   當 [**D3D12 \_ 功能 \_ 資料 \_ 結構**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)：： UMA 為 TRUE 時，只會啟動更好的地圖紋理效能。 如果決定要在堆積上選擇哪些 CPU 快取屬性，請注意 *CacheCoherentUMA* 。

-   運用紋理的 CPU 存取比緩衝區更複雜。 最有效率的 Gpu 材質版面配置很少是資料列的 \_ 主要。 事實上，某些 Gpu 在複製材質資料時，只能支援資料列 \_ 主要紋理。

-   UMA Gpu 應廣泛受益于簡單的優化，以減少層級載入時間。 辨識 UMA 之後，應用程式可以將初始 [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 優化，以填入 GPU 不會修改的材質。 \_ \_ \_ 應用程式可以使用 [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)來避免瞭解實際的材質配置，而不是使用 D3D12 堆積類型的預設值來建立堆積的材質，以及透過將材質資料封送處理。

-   在 D3D12 中，使用 D3D12 材質配置來建立的材質 \_ \_ \_ 未知，而且沒有 CPU 存取最有效率的是經常進行 GPU 轉譯和取樣。 當效能測試時，應該將這些紋理與 \_ cpu 存取的 D3D12 紋理配置 \_ \_ ，以及 \_ 具有 cpu 存取的 D3D12 材質配置 \_ \_ 標準 \_ SWIZZLE 和 D3D12 \_ 材質版面配置資料 \_ \_ 列主要進行比較， \_ 以取得跨介面卡支援。

-   使用 D3D12 \_ 材質 \_ 配置 \_ 與 CPU 存取的「未知」，可讓 [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)、 [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)、 [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (阻止應用程式存取指標 [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)) 和取消對應，但可能會犧牲 GPU 存取的效率。

-   使用 D3D12 \_ 材質 \_ 配置 \_ 標準 \_ SWIZZLE 搭配 CPU 存取，可讓 [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)、 [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)、Map (傳回應用程式) 和取消 [**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)的 [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)有效指標。 它也可以犧牲 GPU 存取的效率，而不是 \_ 透過 \_ CPU 存取的未知 D3D12 材質配置 \_ 。

## <a name="overview-of-standard-swizzle"></a>標準 Swizzle 總覽

D3D12 (和 D3D 11.3) 引進標準的多維度資料版面配置。 這樣做的目的是為了讓多個處理單位在相同的資料上運作，而不需要複製資料或在多個配置之間 swizzling 資料。 標準化配置可讓您透過網路效果提高效率，並允許演算法在採用特定模式時進行短暫的剪下。

如需材質配置的詳細說明，請參閱 [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)配置。

不過請注意，這個標準 swizzle 是硬體功能，而且可能不受所有 Gpu 支援。

如需 swizzling 的背景資訊，請參閱 [Z 順序曲線](https://en.wikipedia.org/wiki/Z-order_curve)。

## <a name="apis"></a>API

與 D3D 11.3 不同的是，D3D12 預設支援材質對應，因此不需要查詢 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)。 不過，D3D12 不一定會支援標準 swizzle-這項功能必須透過呼叫來進行查詢，以 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)和檢查 **D3D12 \_ feature \_ DATA \_ D3D12 \_ 選項** 的 *StandardSwizzle64KBSupported* 欄位。

下列 Api 參考紋理對應：

列舉

-   [**D3D12 \_材質 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置：控制預設材質的 swizzle 模式，並啟用可存取 CPU 的材質的地圖支援。

結構

-   [**D3D12 \_資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) ：描述資源，例如紋理，這是廣泛使用的結構。
-   [**D3D12 \_堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) ：描述堆積。

方法

-   [**ID3D12Device：： CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) ：建立單一資源，並支援正確大小和對齊方式的堆積。
-   [**ID3D12Device：： CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) ：建立緩衝區或材質的堆積。
-   [**ID3D12Device：： CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) ：建立放置於特定堆積中的資源，通常比 [**CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)更快建立資源的方法。
-   [**ID3D12Device：： CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) ：建立已保留但尚未認可或放在堆積中的資源。
-   [**ID3D12CommandQueue：： UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) ：將並排顯示的資源中的磚位置對應更新為資源堆積中的記憶體位置。
-   [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ：取得資源中指定資料的指標，並拒絕 SUBRESOURCE 的 GPU 存取。
-   [**ID3D12Resource：： GetDesc**](id3d12resource-getdesc.md) ：取得資源屬性。
-   [**ID3D12Heap：： GetDesc**](id3d12heap-getdesc.md) 會取得堆積屬性。
-   [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ：從使用 [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)所對應的材質複製資料。
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) ：將資料複製到使用 [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)對應的材質。

資源和父堆積有對齊需求：

-   D3D12 \_ \_ \_ \_ \_ 多重範例紋理的預設 MSAA 資源放置對齊 (4mb) 。
-   D3D12 \_ \_ \_ \_ 單一範例紋理和緩衝區的預設資源位置對齊 (64kb) 。
-   線性 subresource 複製必須對齊 D3D12 \_ 材質 \_ 資料 \_ 放置 \_ 對齊 (512 個位元組) ，而且資料列間距會對齊 D3D12 \_ 材質 \_ 資料 \_ 音調 \_ 對齊 (256 個位元組) 。
-   常數緩衝區視圖必須對齊 D3D12 \_ 常數 \_ 緩衝區 \_ 資料 \_ 放置對齊， \_ (256 個位元組) 。

小於64KB 的材質應該透過 [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)來處理。

使用動態紋理 (材質變更每個畫面格) CPU 會以線性方式寫入上傳堆積，然後再進行 GPU 複製作業。

一般而言，若要建立動態資源，請在上傳堆積中建立大型緩衝區 (請參閱 [緩衝區內](large-buffers.md) 的子分配) 。 若要建立暫存資源，請在 readback 堆積中建立大型緩衝區。 若要建立預設靜態資源，請在預設堆積中建立連續的資源。 若要建立預設的別名資源，請在預設堆積中建立重迭的資源。

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) 和 [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) 會在資料列的版面配置和未定義的資源版面配置之間重新排列材質資料。 作業是同步的，因此應用程式應記住 CPU 排程。 應用程式一律會將複製分割成較小的區域，或在另一項工作中排程這項作業。 這些 CPU 複製作業不支援具有不透明資源版面配置的 MSAA 資源和深度樣板資源，且會造成失敗。 也不支援不具雙線元素大小的格式，而且也會造成失敗。 可能會發生記憶體不足的傳回碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**核心常數**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> </dl>

 

 




