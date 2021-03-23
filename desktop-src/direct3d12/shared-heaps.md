---
title: 共用堆積
description: 共用適用于多進程和多介面卡架構。
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2019
ms.locfileid: "74104113"
---
# <a name="shared-heaps"></a>共用堆積

共用適用于多進程和多介面卡架構。

-   [共用總覽](#sharing-overview)
-   [跨進程共用堆積](#sharing-heaps-across-processes)
-   [跨介面卡共用堆積](#sharing-heaps-across-adapters)
-   [相關主題](#related-topics)

## <a name="sharing-overview"></a>共用總覽

共用堆積有兩項功能：在一或多個進程之間共用堆積中的資料，以及針對堆積內的資源阻止不具決定性的非定義材質配置選項。 在介面卡之間共用堆積也可免除資料的 CPU 封送處理需求。

堆積和認可的資源都可以共用。 共用認可的資源實際上會與認可的資源描述共用隱含堆積，讓相容的資源描述可以對應到另一部裝置的堆積。

所有方法都可自由執行緒，並繼承 NT 控制碼共用設計的現有 D3D11 語義。

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>跨進程共用堆積

共用堆積會以 \_ \_ \_ [**D3D12 \_ 堆積 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) 列舉的 D3D12 堆積旗標共用成員來指定。

在可存取 CPU 的堆積上，不支援共用堆積： D3D12 \_ 堆積 \_ 類型 \_ 上傳、D3D12 \_ 堆積 \_ 類型 \_ READBACK 和 D3D12 \_ 堆積 \_ 類型 \_ 自訂，不含 D3D12 \_ CPU \_ 頁面 \_ 屬性 \_ \_ 。

阻止不具決定性的未定義材質版面配置，可能會大幅影響某些 Gpu 上的延遲轉譯案例，因此它不是放置和認可資源的預設行為。 某些 GPU 架構上的延遲轉譯受損，因為具決定性的材質版面配置會降低在轉譯為相同格式和大小的多個轉譯目標紋理時所達到的有效記憶體頻寬。 GPU 架構不斷演進，無法利用非決定性的材質配置來支援標準化的 swizzle 模式和標準化的版面配置，以進行延遲的呈現。

共用堆積也會伴隨其他小成本：

-   由於有資訊洩漏的問題，因此無法將共用堆積資料回收為彈性，因為同進程堆積會導致實體記憶體的 zero'ed 更頻繁。
-   在建立和終結共用堆積期間，會有額外的 CPU 額外負荷和系統記憶體使用量增加。

## <a name="sharing-heaps-across-adapters"></a>跨介面卡共用堆積

您可以使用 \_ \_ \_ \_ \_ [**D3D12 \_ 堆積 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) 列舉的 D3D12 堆積旗標共用交叉配接器成員，指定跨介面卡的共用堆積。

跨介面卡共用堆積可讓多個介面卡共用資料，而不會在 CPU 之間將資料封送處理。 雖然不同的介面卡功能會判斷介面卡在兩者之間傳遞資料的效率，但只是啟用 GPU 複本可增加達到的有效頻寬。 即使不支援這類材質配置，跨介面卡堆積還是允許某些材質配置來支援材質資料的交換。 某些限制可能適用于這類紋理，例如僅支援複製。

跨介面卡共用可搭配呼叫 [**ID3D12Device：： CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)所建立的堆積運作。 然後，應用程式可以透過 [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)來建立資源。 [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)所建立的資源/堆積也會允許此功能，但只有資料列主要 D3D12 \_ 資源 \_ 維度 \_ TEXTURE2D 資源， (參閱 [**D3D12 \_ 資源 \_ 維度**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)) 。 跨介面卡共用無法與 [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)搭配使用。

針對跨介面卡共用，所有一般的跨佇列資源分享規則仍然適用。 應用程式必須發出適當的阻礙，以確保這兩張介面卡之間有適當的同步處理和連貫性。 應用程式應該使用跨介面卡的圍牆來協調提交給多個介面卡的命令清單排程。 沒有任何機制可跨 D3D API 版本共用跨介面卡資源。 只有系統記憶體支援跨介面卡共用資源。 D3D12 \_ 堆積 \_ 型別預設堆積 \_ 和 D3D12 \_ 堆積類型自訂堆積 (使用 L0 記憶體集區時，支援跨介面卡共用堆積/資源 \_ \_ ，) 的寫入合併 CPU 頁面屬性。 驅動程式必須確定跨介面卡共用堆積的 GPU 讀取/寫入作業與系統上的其他 Gpu 一致。 例如，驅動程式可能需要將堆積資料排除在 GPU 快取中，而當 CPU 無法直接存取堆積資料時，通常不需要清除這些資料。

應用程式應該限制只有在需要所提供功能的情況下，才會使用跨介面卡堆積。 跨介面卡堆積位於 D3D12 \_ MEMORY \_ POOL L0 中 \_ ，這不一定是 [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) 所建議的。 針對離散/NUMA 介面卡架構，該記憶體集區的效率不高。 而且，最有效率的材質版面配置不一定都可以使用。

同時適用下列限制：

-   堆積層的相關堆積旗標必須是 D3D12 \_ 堆積旗標，才能 \_ \_ 允許 \_ 所有 \_ 緩衝區 \_ 和 \_ 紋理。
-   您 \_ \_ \_ 也必須設定共用的 D3D12 堆積旗標。
-   您必須 \_ 設定 D3D12 堆積 \_ 類型 \_ 的預設值，或 D3D12 \_ \_ \_ 無法使用的 D3D12 記憶體集區 \_ \_ \_ L0 和 D3D12 \_ CPU \_ 頁面 \_ 屬性 \_ \_ 的自訂堆積類型。
-   只有具有 D3D12 資源旗標的資源 \_ \_ ，才能 \_ \_ \_ 在跨介面卡堆積上放置。

如需使用多個介面卡的詳細資訊，請參閱 [多介面卡系統](multi-engine.md) 一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[堆積中的子分配](suballocation-within-heaps.md)
</dt> </dl>

 

 




