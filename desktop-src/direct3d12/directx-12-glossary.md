---
title: Direct3D 12 詞彙
description: 這些詞彙是 Direct3D 12 的特色。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548447"
---
# <a name="direct3d-12-glossary"></a>Direct3D 12 詞彙

這些詞彙是 Direct3D 12 的特色。

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**綁定**
</dt> <dd>

將記憶體連接至圖形管線的程式。 例如，資源系結牽涉到將材質之類的資源系結至管線，以用於呈現物件。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**緩衝區**
</dt> <dd>

D3D 資源的類型，與連續的記憶體配置同義。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**束**
</dt> <dd>

圖形處理單位 (GPU) 的命令緩衝區只能透過 *直接命令清單* 來執行。 組合會繼承所有 GPU 狀態 (但目前設定的 *管線狀態物件* 和基本拓撲) 除外。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**命令配置器**
</dt> <dd>

儲存 GPU 命令的基礎記憶體配置。 命令配置器 *物件同時適用* 于 *直接命令清單* 和組合。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**命令清單**
</dt> <dd>

命令清單會對應至 GPU 執行的一組命令。 這些包括設定狀態、繪製、清除和複製等命令。 D3D12 命令清單介面明顯不同于 D3D11 命令清單介面。 D3D12 命令清單介面包含類似于 D3D11 裝置內容轉譯 Api 的 Api。

D3D12 命令清單不會對應或取消對應資源、變更磚對應、調整磚集區大小、取得查詢資料，也不會以隱含方式將命令提交至 GPU 進行執行。

不同于 D3D11 延遲的內容，D3D12 命令清單只支援兩個層級的間接取值。 *直接命令清單* 對應至 GPU 可執行檔命令緩衝區。 組合 *只能透過* 直接命令清單來執行。

直接命令清單不會繼承任何 GPU 狀態。 組合會繼承所有 GPU 狀態 (但目前設定的管線狀態物件和基本拓撲) 除外。

命令配置器會設定命令清單的記憶體 *。* 命令清單的目的是它們可以提交至 GPU 作為單一轉譯要求。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**命令佇列**
</dt> <dd>

GPU 會連續執行的 *命令清單* 佇列。 應用程式必須明確地將 *命令清單* 提交到命令佇列以供執行。 通常有三個命令佇列：3D 圖形、計算和複製，對應至 GPU 上的3D 圖形管線、計算引擎，以及一或多個複製引擎。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**保守的點陣化**
</dt> <dd>

保守的點陣化是適用于 Direct3D 圖形管線之轉譯器階段的操作模式。 它會停用標準以範例為基礎的點陣化，並改為以基本型別來點陣化任何數量所涵蓋的圖元。 其中一項重要的區別是，雖然任何涵蓋範圍都會產生柵格化圖元，但該涵蓋範圍不能以硬體為特性，因此涵蓋範圍一律會以二進位呈現給圖元著色器：完全涵蓋或未涵蓋。 它會保留給圖元著色器程式碼，以 analytically 判斷實際的涵蓋範圍。

保守的點陣化有助於解決衝突和點擊偵測、分類收納和遮蔽剔除等問題，其中圖元的色彩更特定且可以消除邊緣案例。 請參閱 [保守的光柵](conservative-rasterization.md)化。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**常數緩衝區視圖 (CBV)**
</dt> <dd>

常數緩衝區包含著色器常數資料，例如相機視圖、投射矩陣和世界矩陣。 「常數緩衝區視圖」是圖形管線所見之緩衝區的格式特定視圖。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**預設堆積**
</dt> <dd>

使用者模式堆積，著重于支援持續性 GPU 資源類型，包括 GPU 寫入的資源。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**描述 符**
</dt> <dd>

描述項是 D3D12 中單一資源的系結主要單位。 描述項是相當小的資料區塊，可完整描述 gpu 特定格式的 GPU 物件。 有許多不同類型的描述項：著色器資源檢視 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器是一些範例。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**描述元堆積**
</dt> <dd>

描述元堆積是描述項連續配置的集合，每個描述項的一個配置。 描述元堆積的主要點是為了將著色器參考最大的物件類型描述項規格，儲存在轉譯時所需的大量記憶體配置， (理想的轉譯或更) 的整個框架。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**描述項資料表**
</dt> <dd>

描述項資料表在邏輯上是描述項的陣列。 每個描述中繼資料表都會儲存一或多個類型的描述項，包括 SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置，它只是描述項堆積中的位移和長度。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**直接命令清單**
</dt> <dd>

GPU 可執行檔命令緩衝區。 直接命令清單不會繼承任何 GPU 狀態。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**柵欄**
</dt> <dd>

用來同步處理 GPU 和 CPU 的機制。 您可以指示 GPU 和 CPU 等待範圍，等候其他處理器趕上的作用。 請參閱 [多重引擎同步](./user-mode-heap-synchronization.md)處理。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**危險，危險追蹤**
</dt> <dd>

當資源已用於一個用途，且應用程式打算將它用於其他用途時，會發生危險。 若要再次使用資源，必須將中繼快取排清或失效，壓縮需求必須與第二次使用一致，而且資源應該處於所需的狀態，以避免在寫入資源之後讀取資源，並基於預期目的而使其失效。

維護資源和避免這些同步處理問題的程式稱為「危險追蹤」。 如果驅動程式沒有風險追蹤，則應用程式會負責這項工作。 在大部分舊版的 DirectX 中，風險追蹤是由驅動程式處理。 為了改善效能，DirectX 12 提供沒有危險追蹤的方法。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**高階著色器語言 (HLSL)**
</dt> <dd>

一種電腦語言，類似于 C 的許多方式，用於撰寫著色器程式碼。 頂點、圖元、幾何、計算、網域和輪廓著色器全都使用 HLSL 撰寫。 編譯器會將 HLSL 來源轉換成二進位格式，以供 GPU 取用。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**
</dt> <dd>

單一 GPU 中不同的引擎實例和類型。 引擎的類型包括：圖形、計算和複製。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

一種硬體設定，其中有一個以上的圖形配接器。 不同的介面卡有時也稱為節點。 擁有多個 Gpu 可以使其與 CPU 進行同步處理，而彼此的工作則比使用單一 GPU 更為複雜。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**管線狀態物件 (PSO)**
</dt> <dd>

GPU 狀態的重要部分。 此狀態包括目前設定的著色器和特定的固定函式狀態物件。 變更管線物件內所包含之狀態的唯一方式，就是變更目前系結的管線物件。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**預測**
</dt> <dd>

Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。 比方說，如果物件的周框方塊是由另一個物件完全 pixels occluded，或是將物件減少為小於圖元的大小，則根本不會嘗試繪製隱藏的物件。 請參閱 [Predication](predication.md)。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**(ROV) 的轉譯器訂單視圖**
</dt> <dd>

標準圖形管線可能無法正確地將多個包含透明度的材質組合在一起。 網路圍牆、冒煙、火、植被指數和彩色玻璃等物件會使用透明效果來取得所需的效果。 如果多個包含透明度的材質 (在包含植被指數的半透明大樓前方的範圍前面，有多個材質出現問題，就會發生問題，例如) 。 以轉譯器排序的視圖 (ROVs) 啟用基礎順序獨立透明度 (OIT) 演算法來使用硬體的功能，以嘗試正確地解析透明度順序。 透明度是由圖元著色器所處理。

以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將未排序的存取視圖標記 (UAV) 系結，以及改變 UAVs 圖形管線結果順序的一般需求。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback 堆積**
</dt> <dd>

將焦點放在從 GPU 傳輸回 CPU 的資料的使用者模式堆積。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**資源**
</dt> <dd>

提供資料給管線，並定義在場景中呈現內容的實體。 從您的遊戲媒體載入或在執行階段動態建立資源。 通常，資源包括紋理資料、頂點資料和著色器資料。 大部分的 Direct3D 應用程式會在其存留期內廣泛地建立和終結資源。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**資源屏障**
</dt> <dd>

資源關卡會通知驅動程式，可能需要對單一資源進行多個存取的同步處理，例如讀取和寫入相同的材質。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**資源系結**
</dt> <dd>

資源系結是將資源 (紋理、頂點緩衝區、索引緩衝區等) 上連結至圖形管線的程式，可讓管線的著色器處理正確的資源。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**資源堆積**
</dt> <dd>

資源堆積是堆積的一般詞彙，記憶體緩衝區會保留這些資源，因為它們會在 GPU 之間傳輸。 傳送至 GPU 需要一個上傳堆積，從 GPU 到 CPU 都需要 Readback 堆積，而 GPU 的持續性堆積會在多個轉譯畫面上維持，稱為預設堆積。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**根簽章**
</dt> <dd>

根簽章會定義要系結至圖形或計算管線的所有資源。 根簽章是由應用程式設定，並將命令清單連結至著色器通常需要的資源，每個應用程式都有一個圖形和一個計算根簽章。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**採樣**
</dt> <dd>

取樣器是從材質讀取的程式碼。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**(SRV) 的著色器資源檢視**
</dt> <dd>

在著色器資源中查看資料的格式特定方式，例如紋理。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**靜態堆積**
</dt> <dd>

將焦點放在多個 GPU 唯讀資源的使用者模式堆積，通常會同時使用，且不會經常變更。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**交換鏈**
</dt> <dd>

交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。 交換鏈是由低層級的 API set DXGI 所處理 (請參閱 [DXGI 總覽](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)) 。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

在記憶體中找出多維度資料的技巧，讓鄰近維度的資料通常會有鄰近的位址。 尤其是，一個資料列的所有資料，在下一個資料列的資料之前不會連續找出。 「參數化 Swizzle」描述描述 Swizzle 模式的標準化方式。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**紋理**
</dt> <dd>

一種類型的 D3D 資源，其為多維度，且具有已針對 GPU 的多維度存取優化的記憶體配置。 紋理通常會包含轉譯至表面上所需的原始影像，以進行光源和混色，但可以包含其他形式的資料，例如色彩漸層和參考色彩。 Direct3D 12 支援一、二和三個維度紋理。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**瓦**
</dt> <dd>

視訊記憶體的頁面，類似于記憶體的 CPU/系統分頁。 磚標記法有助於區別 GPU 虛擬記憶體子系統與 CPU 虛擬記憶體子系統。 Gpu 提供的虛擬記憶體功能與系統虛擬記憶體類似。 某些 Gpu 具有共用的虛擬記憶體功能，可讓您以 CPU 和 GPU 共用虛擬記憶體子系統的一些頁面。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**磚資源**
</dt> <dd>

需要有並排的資源，因此不會浪費較少的 GPU 記憶體來儲存應用程式知道將無法存取的介面區域，而且硬體可以瞭解如何在連續的磚之間進行篩選。 磚的資源是大型邏輯資源，但需要少量的實體記憶體。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**未排序的存取視圖 (UAV)**
</dt> <dd>

未排序的存取權會在資源 (中包含緩衝區、紋理和材質陣列，而不需要多取樣) ，可讓您從多個執行緒暫時未排序的讀取/寫入存取。 這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**上傳堆積**
</dt> <dd>

使用者模式堆積，著重于從 CPU 到 GPU 的資料傳輸。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**使用者模式堆積**
</dt> <dd>

在沒有任何核心元件感知的情況下回收的大型、連續記憶體組態集合：配置和終結方法不會在穩定狀態下呼叫核心配置和銷毀方法。 Upload、Readback 和 Default 堆積是使用者模式堆積的變體。

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**磁片區磚資源**
</dt> <dd>

三維並排顯示的 [資源](/windows)。

</dd> </dl>

 

 