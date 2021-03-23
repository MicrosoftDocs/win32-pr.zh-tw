---
title: 居住
description: 當 GPU 可存取物件時，會將物件視為駐留。
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548426"
---
# <a name="residency"></a>居住

當 GPU 可存取物件時，會將物件視為 *駐留* 。

-   [常駐預算](#residency-budget)
-   [堆積資源](#heap-resources)
-   [常駐優先順序](#residency-priorities)
    -   [預設優先權演算法](#default-priority-algorithm)
-   [設計常駐管理](#programming-residency-management)
-   [相關主題](#related-topics)

## <a name="residency-budget"></a>常駐預算

Gpu 尚不支援分頁錯誤，因此應用程式必須在 GPU 可以存取的情況下，將資料認可到實體記憶體。 此程式稱為「進行某些作業」，且必須針對實體系統記憶體和物理離散視訊記憶體進行。 在 D3D12 中，大部分的 API 物件都會封裝一些 GPU 可存取的記憶體。 在 api 物件的建立期間，會將 GPU 可存取的記憶體設為常駐，並在 API 物件終結時收回。

此進程可用的實體記憶體數量稱為「影片記憶體預算」。 在背景進程喚醒和睡眠的情況下，預算可能會明顯波動;當使用者切換到另一個應用程式時，就會大幅波動。 當預算變更時，應用程式可以收到通知，而且會輪詢目前的預算和目前耗用的記憶體數量。 如果應用程式不在其預算內，則會間歇性凍結程式以允許其他應用程式執行，並/或建立 Api 將會傳回失敗。 [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3)介面提供與這項功能有關的方法，特別是 [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo)和 [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)。

建議應用程式使用保留來代表它們無法移出的記憶體數量。 在理想情況下，使用者指定的「低」圖形設定或更低的值，是這類保留的正確值。 設定保留將不會讓應用程式的預算高於通常會收到的預算。 相反地，保留資訊可協助作業系統核心快速將大型記憶體壓力情況的影響降到最低。 即使應用程式不是前景應用程式，仍無法保證應用程式使用保留。

## <a name="heap-resources"></a>堆積資源

雖然許多 API 物件會封裝一些 GPU 可存取的記憶體，但堆積 & 資源預期是應用程式取用和管理實體記憶體的最有效方式。 堆積是管理實體記憶體的最低層級單位，因此最好先熟悉它們的常駐屬性。

-   堆積無法進行部分常駐，但保留的資源有因應措施。
-   堆積應預算為特定集區的一部分。 UMA 介面卡有一個集區，而離散介面卡有兩個集區。 雖然核心可以將離散配接器上的一些堆積從影片記憶體移至系統記憶體，但它只是最大的最後手段。 應用程式不應該依賴核心的過度預算行為，而應專注于良好的預算管理。
-   您可以從常駐中收回堆積，讓其內容可以分頁至磁片。 但是，在所有介面卡架構上釋出落地是更可靠的方法。 在 [**D3D12 \_ 功能 \_ 資料 \_ GPU \_ 虛擬 \_ 位址 \_ 支援**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support)的 *theMaxGPUVirtualAddressBitsPerProcess* 欄位接近預算大小的介面卡上，[**收回**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict)將無法可靠地回收常駐。
-   堆積建立可能很慢;但它已針對背景執行緒優化。 建議您在背景執行緒上建立堆積，以避免瑕疵轉譯執行緒。 在 D3D12 中，多個執行緒可以安全地同時呼叫 create 常式。

D3D12 為其資源模型帶來更多的彈性和 orthogonality，以便為應用程式啟用更多選項。 D3D12 中有三種高層級的資源類型：已認可、已放置和已保留。

-   認可的資源會同時建立資源和堆積。 堆積是隱含的，無法直接存取。 堆積會適當地調整大小，以找出堆積內的整個資源。
-   放置的資源允許在堆積內的非零位移放置資源。 位移通常必須對齊 64KB;但是，這兩個方向都有一些例外狀況。 MSAA 資源需要4MB 位移對齊，而小材質可以使用 4 KB 位移對齊。 放置的資源無法直接重新放置或重新對應到另一個堆積;但它們可讓您在堆積之間進行資源資料的簡單重做。 在不同堆積中建立新的放置資源並複製資源資料之後，新的資源描述元將必須用於新的資源資料位置。
-   只有在介面卡支援並排顯示的資源層級1或更大時，才可使用保留的資源。 如果有的話，則提供最先進的常駐管理技術;但並非所有的介面卡目前都支援它們。 它們可讓您重新對應資源，而不需要重新產生資源描述項、部分 mip 層級常駐和稀疏材質案例等等。即使保留的資源可供使用，但並非所有資源類型都受到支援，因此，完全以頁面為基礎的開放管理員尚不可行。

## <a name="residency-priorities"></a>常駐優先順序

Windows 10 建立者更新可讓開發人員在記憶體壓力需要降級某些資源時，影響哪些堆積和資源要保持常駐。 這可協助開發人員藉由充分利用執行時間無法從 API 使用方式推斷的知識，來建立更好的應用程式。 開發人員預期當開發人員從使用認可的資源轉換為 resereved 和並排顯示的資源時，將會更熟悉且能夠指定優先順序。

套用這些優先順序必須比 manageing 兩個動態記憶體預算更容易，因為應用程式已經可以這麼做，所以請手動降級並提升資源 bettween。 因此，「主機優先順序 API」的設計會以 coursely 的方式，將合理的預設優先順序指派給每個堆積或建立的資源。 如需詳細資訊，請參閱 [**ID3D12Device1：： SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) 和 [**D3D12 \_ 常駐 \_ 優先權**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority) 列舉。

有了優先權，開發人員預期會有下列其中一項：

-   提高一些例外堆積的優先順序，以便更快地降級這些堆積比其自然存取模式需要更快或更頻繁的效能影響。 從像是 Direct3D 11 或 OpenGL 等圖形 Api 所移植的應用程式，其資源管理模型與 Direct3D 12 的資源管理模型截然不同。
-   使用應用程式本身的 bucketization 配置來覆寫幾乎所有的堆積優先順序（根據程式設計人員對於存取頻率或動態的知識而定）：固定配置比動態配置更容易管理，但可能較不有效率，而且需要程式設計人員操作，因為在開發過程中會改變使用模式。 使用 Direct3D 12 樣式的資源管理所建立的應用程式（例如使用落地程式庫的應用程式）會使用這種方法， (特別是) 的動態配置。

### <a name="default-priority-algorithm"></a>預設優先權演算法

應用程式無法在不先 understaning 預設優先權演算法的情況下，為任何嘗試管理的堆積指定有用的優先順序。 這是因為將特定優先權指派給堆積的值，是從競爭相同記憶體的其他優先順序堆積衍生而來的。

為產生預設優先順序所選擇的策略是將堆積分類成兩個值區，favoring (給予較高優先順序的) 堆積，而這些堆積會假設 GPU 不是經常寫入。

高優先順序的值區包含以旗標建立的堆積和資源，這些旗標會將它們識別為轉譯目標、深度樣板緩衝區或未排序的存取視圖 (UAVs) 。 這些是從 **D3D12 落地 \_ \_ 優先權 \_ 高** 的範圍中指派的優先順序值; 若要進一步設定這些堆積和資源的優先順序，則優先順序的最低16位會設定為堆積或資源的大小，除以 10mb (飽和，相當大型堆積) 。 這種額外的優先順序偏好較大型的堆積和資源。

低優先順序值區包含所有其他堆積和資源，這些堆積和資源都會被指派優先順序值為 [D3D12] 的 [ **\_ \_ \_ 一般**]。 在這些堆積與資源之間，不會有進一步的優先順序。

## <a name="programming-residency-management"></a>設計常駐管理

簡單的應用程式可能只需要建立認可的資源，直到遇到記憶體不足的失敗為止。 失敗時，應用程式可能會損毀其他已認可的資源或 API 物件，以使資源建立成功。 但是，即使是簡單的應用程式，也強烈建議監看是否有負面的預算變更，以及在框架中大約一次終結未使用的 API 物件。

當您嘗試將介面卡架構優化或納入落地優先順序時，仍會有常駐管理設計的複雜度。 分開預算和管理兩個離散記憶體集區會比只管理一個集區更複雜，而且在大規模指派固定優先順序可能會在使用模式演進時成為維護的負擔。 將材質溢出至系統記憶體會增加複雜度，因為系統記憶體中錯誤的資源可能會嚴重影響畫面播放速率。 而且，沒有任何簡單的功能可協助您找出可受益于較高 GPU 頻寬或容許較低 GPU 頻寬的資源。

更複雜的設計也會查詢目前介面卡的功能。 這項資訊適用于 [**D3D12 \_ 功能 \_ 資料 \_ GPU \_ 虛擬 \_ 位址 \_ 支援**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support)、 [**D3D12 \_ 功能 \_ 資料 \_ 結構**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)、 [**D3D12 \_ 並排 \_ 資源 \_ 層**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)和 [**D3D12 \_ 資源 \_ 堆積 \_ 層**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier)。

應用程式的多個部分可能會使用不同的技術。 例如，某些大型紋理和很少使用的程式碼路徑可能會使用認可的資源，而許多材質可以使用串流屬性來指定，並使用一般的放置資源技術。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[記憶體管理](memory-management.md)
</dt> </dl>

 

 