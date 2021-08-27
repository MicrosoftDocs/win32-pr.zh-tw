---
title: " (Direct3D 12 圖形) 的核心介面"
description: 下列介面是在 d3d12 中宣告。
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 0cc8fcecec2e2a0966ed34e23eb65ed9acd37e76
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812883"
---
# <a name="core-interfaces"></a>核心介面

下列介面是在 d3d12 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | 代表圖形處理單元的儲存體配置 (GPU) 命令。 |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)繼承自的目標介面。 它代表 GPU 執行的一組已排序命令組，同時允許延伸模組支援其他命令清單，而不只是圖形 (例如計算和複製) 。 |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | 提供提交命令清單、同步命令清單執行、檢測命令佇列，以及更新資源磚對應的方法。 |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | 命令簽名物件可讓應用程式指定間接繪圖，包括要使用的緩衝區格式、命令類型和資源系結。 |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | 描述元堆積是描述項連續配置的集合，每個描述項的一個配置。 描述元堆積包含許多不屬於管線狀態物件的物件類型 (PSO) ，例如著色器資源查看 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。 |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | 代表虛擬介面卡;它可用來建立命令配置器、命令清單、命令佇列、圍牆、資源、管線狀態物件、堆積、根簽章、取樣器和許多資源檢視。 |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | 代表虛擬介面卡，並擴充 [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)所提供的方法範圍。 |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | 代表虛擬配接器。 此介面會擴充 [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) ，以從管線狀態資料流程描述建立管線狀態物件。 |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | 代表虛擬配接器。 這個介面會擴充 [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) ，以支援在系統記憶體中建立特殊用途的診斷堆積，即使在發生 GPU 錯誤或裝置移除的情況下仍會保存。 |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3)。 |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4)。 |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5)。 |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device6](/windows/win32/api/d3d12/nn-d3d12-id3d12device6)。 |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device7](/windows/win32/api/d3d12/nn-d3d12-id3d12device7)。 |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | 代表虛擬配接器。 這個介面會擴充 [ID3D12Device8](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) ，以新增方法來管理著色器快取。 |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | 其他核心介面繼承自的介面，包括 [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)、 [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)、 [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)和 [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)。 它會提供方法，讓您回到所建立的裝置物件。 |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | 提供裝置的執行時間存取， (DR) 資料來移除擴充的資料。 |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | 此介面控制裝置已移除擴充的資料 (DR) 設定。 |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | 代表用來同步處理 CPU 的物件，以及一或多個 Gpu。  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | 表示隔離。 這個介面會擴充 [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)，並支援抓取用來建立原始範圍的旗標。  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | 封裝圖形命令清單以供轉譯。 包含用於檢測命令清單執行，以及設定和清除管線狀態的 Api。 |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | 封裝可供轉譯的圖形命令清單、擴充介面以支援可程式化的範例位置、可執行最晚閂鎖技術的不可部分完成的複製，以及選擇性的深度範圍測試。 |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | 封裝圖形命令清單以進行轉譯，擴充介面以支援直接將立即值寫入緩衝區。 |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | 封裝圖形命令清單以供轉譯。 |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | 封裝用於轉譯的圖形命令清單，擴充介面以支援光線追蹤和轉譯行程。 |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | 堆積是連續記憶體配置的抽象概念，用來管理實體記憶體。 此堆積可以與 [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) 物件搭配使用，以支援放置的資源或保留的資源。 |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | 表示應用程式定義的回呼，用來通知物件的存留期變更。 |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | 表示用來控制存留期追蹤物件存留期的功能。 |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | 表示中繼命令。 中繼命令是一個 Direct3D 12 物件，代表由獨立硬體廠商 (Ihv) 加速的演算法。 它是驅動程式所執行之命令產生器的不透明參考。 |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)和 [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild)從中繼承的介面。 它會提供方法來建立私用資料和批註物件名稱的關聯性。 |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | 許多其他核心介面繼承自的介面。 它指出物件型別會封裝一些 GPU 可存取的記憶體，但不會強烈指出應用程式是否可以操作物件的存放區。  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | 管理管線程式庫，特別是載入和取出個別的 Pso。 |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | 管理管線程式庫。 此介面會擴充 [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) 以從管線狀態資料流程描述載入 pso。 |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | 表示所有目前已設定著色器的狀態，以及某些固定函式狀態物件的狀態。 |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | 管理查詢堆積。 查詢堆積會保留索引所參考的查詢陣列。 |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | 封裝 CPU 和 GPU 讀取和寫入實體記憶體或堆積的一般化功能。 它包含用來組織和操作簡單資料陣列的抽象概念，以及針對著色器取樣優化的多維度資料。 |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | 根簽章會定義哪些資源系結至圖形管線。 根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。 目前每個應用程式都有一個圖形和一個計算根簽章。 |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | 包含方法，可傳回已還原序列化之根簽章版本1.0 的 [**D3D12 根目錄簽章-DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 資料結構。  |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | 表示著色器快取會話。 |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | 表示應用程式會以單一單位的形式來管理的設定狀態數量，包括著色器，並以不可部分完成的方式提供給驅動程式，例如編譯或優化。  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | 提供取得和設定 [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject)屬性的方法。  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | 此介面是用來設定工具（例如 PIX）的執行時間。 不適用於任何其他案例，或不支援。 |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | 包含方法，這些方法會傳回任何版本之序列化根簽章的還原序列化 [**D3D12 根目錄-簽章-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) 資料結構。  |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
* [介面階層](interface-hierarchy.md)