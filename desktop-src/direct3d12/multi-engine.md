---
title: 多個介面卡系統
description: 說明在安裝多個介面卡的系統中，Direct3D 12 的支援，其中涵蓋了應用程式明確以多個 GPU 介面卡為目標的案例，以及驅動程式會代表您的應用程式隱含使用多個 GPU 介面卡的案例。
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: 9d530b0a2396f2274e9ed693c1f5f10556aadebb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2020
ms.locfileid: "104548359"
---
# <a name="multi-adapter-systems"></a>多個介面卡系統

說明在安裝多個介面卡的系統中，Direct3D 12 的支援，其中涵蓋了應用程式明確以多個 GPU 介面卡為目標的案例，以及驅動程式會代表您的應用程式隱含使用多個 GPU 介面卡的案例。

## <a name="multi-adapter-overview"></a>多介面卡總覽

GPU 介面卡可以是任何支援 Direct3D 12 的製造商 (圖形或計算、離散或整合式) 。

多個介面卡會被參考為 *節點*。 有幾個專案（例如佇列）會套用至每個節點，因此如果有兩個節點，則會有兩個預設的3D 佇列。 其他元素（例如管線狀態和根和命令簽章）可以參考一或多個或所有節點，如圖所示。

![佇列適用于每個圖形配接器](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>跨介面卡共用堆積

請參閱 [共用](shared-heaps.md) 堆積主題。

## <a name="multi-adapter-apis-and-node-masks"></a>多個介面卡 Api 和節點遮罩

與先前的 Direct3D Api 類似，會將每組連結的介面卡列舉為單一 [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) 物件。 連結到連結中任何介面卡的所有輸出都會列舉為附加至單一 **IDXGIAdapter3** 物件。

您的應用程式可以藉由呼叫 [**ID3D12Device：： GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)，判斷與指定裝置相關聯的實體介面卡數目。

Direct3D 12 中的許多 Api 都接受 *節點遮罩* (位遮罩) ，這表示 API 呼叫所參考的節點集合。 每個節點都有以零為基底的索引。 但在節點遮罩中，零會轉譯為位 1;1可轉換為 bit 2;依此類推。

### <a name="single-nodes"></a>單一節點

呼叫下列 (單一節點) Api 時，您的應用程式會指定與 API 呼叫相關聯的單一節點。 大部分的情況下，這是由節點遮罩所指定。 遮罩中的每個位都對應至單一節點。 針對本節所述的所有 Api，您必須在節點遮罩中剛好設定一個位。

-   [**D3D12 \_命令 \_ 佇列 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) ：有 *NodeMask* 成員。
-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) ：從 [**D3D12 \_ 命令 \_ 佇列 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) 結構建立佇列。
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ：接受 *nodeMask* 參數。
-   [**D3D12 \_描述元 \_ 堆積 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) ：有 *NodeMask* 成員。
-   [**CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) ：從 [**D3D12 \_ 描述元 \_ 堆積 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) 結構建立描述元堆積。
-   [**D3D12 \_查詢 \_ 堆積 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) ：具有 *NodeMask* 成員。
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) ：從 [**D3D12 \_ 查詢 \_ 堆積 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) 結構建立查詢堆積。

### <a name="multiple-nodes"></a>多個節點

呼叫下列 (多個節點) Api 時，您的應用程式會指定一組與 API 呼叫相關聯的節點。 您可以指定節點親和性作為節點遮罩，可能會設定多個位。 如果您的應用程式針對此位遮罩傳遞0，則 Direct3D 12 驅動程式會將它轉換成位元遮罩 1 (表示物件與節點 0) 相關聯。

-   [**D3D12 \_跨 \_ 節點 \_ 共用 \_ 層**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) ：判斷跨節點共用的支援。
-   [**D3D12 \_功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) ：參考 [**D3D12 \_ 跨 \_ 節點 \_ 共用 \_ 層**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)的結構。
-   [**D3D12 \_功能 \_ 資料 \_ 結構**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) ：包含 *NodeIndex* 成員。
-   [**D3D12 \_圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ：具有 *NodeMask* 成員。
-   [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) ：從 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 結構建立圖形管線狀態物件。
-   [**D3D12 \_計算 \_ 管線 \_ 狀態 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) ：有 *NodeMask* 成員。
-   [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ：從 [**D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) 結構建立計算管線狀態物件。
-   [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)：接受 *nodeMask* 參數。
-   [**D3D12 \_命令 \_ 簽名 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)：有 *NodeMask* 成員。
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) ：從 [**D3D12 \_ 命令 \_ 簽名 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) 結構建立命令簽名物件。

### <a name="resource-creation-apis"></a>資源建立 Api

下列 Api 參考節點遮罩。

-   [**D3D12 \_堆積 \_ 屬性**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) ：同時具有 *CreationNodeMask* 和 *VisibleNodeMask* 成員。
-   [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) ：有 *visibleMask* 參數。
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) ：有 *nodeMask* 參數。

建立保留的資源時，不會指定任何節點索引或遮罩。 保留的資源可以對應到任何節點上的堆積， (遵循跨節點共用規則) 。

方法 [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) 在內部與介面卡佇列搭配運作，您的應用程式不需要為此指定任何功能。

呼叫下列 [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) api 時，您的應用程式不需要指定一組與 api 呼叫相關聯的節點，因為 api 呼叫會套用至所有節點。

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) ： *具有作為參數的範圍* 。 使用 *資源* 或 *堆積* 做為參數時，此方法不接受節點作為參數，因為節點遮罩繼承自先前建立的物件。
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>相關主題

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)