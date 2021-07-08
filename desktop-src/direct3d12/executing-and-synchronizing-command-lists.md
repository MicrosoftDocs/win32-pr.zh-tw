---
title: 執行和同步處理命令清單
description: 在 Microsoft Direct3D 12 中，不再有舊版的立即模式。
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- 命令清單
- 同步處理 - synchronization
- 執行
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d5362d0f093c7c1034e03d396ad28c40d4d600
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489176"
---
# <a name="executing-and-synchronizing-command-lists"></a>執行和同步處理命令清單

在 Microsoft Direct3D 12 中，不再有舊版的立即模式。 相反地，應用程式會建立命令清單和套件組合，然後記錄 GPU 命令集。 命令佇列可用來提交要執行的命令清單。 這種模型可讓開發人員更充分掌控圖形處理器 (GPU) 和 CPU 的使用效率。

-   [命令佇列總覽](#command-queue-overview)
-   [初始化命令佇列](#initializing-a-command-queue)
-   [執行命令清單](#executing-command-lists)
-   [從多個命令佇列存取資源](#accessing-resources-from-multiple-command-queues)
-   [使用命令佇列圍牆同步處理命令清單執行](#synchronizing-command-list-execution-using-command-queue-fences)
-   [同步處理命令佇列所存取的資源](#synchronizing-resources-accessed-by-command-queues)
-   [磚資源的命令佇列支援](#command-queue-support-for-tiled-resources)
-   [相關主題](#related-topics)

## <a name="command-queue-overview"></a>命令佇列總覽

Direct3D 12 命令佇列取代立即模式工作提交的執行時間和驅動程式同步處理，先前不公開給開發人員，並使用 Api 來明確管理平行存取、平行處理原則和同步處理。 命令佇列為開發人員提供下列改良功能：

-   允許開發人員避免非預期的同步處理造成意外的低效率。
-   可讓開發人員在較高的層級引進同步處理，以便更有效率且更精確地判斷所需的同步處理。 這表示執行時間和圖形驅動程式將花費較少的時間被動工程平行處理原則。
-   更明確地進行昂貴的作業。

這些增強功能可啟用或增強下列案例：

-   提高的平行處理原則：當背景工作負載有個別的佇列可用於前景工作時，應用程式可以使用更深入的佇列，例如影片解碼。
-   非同步和低優先順序的 GPU 工作-命令佇列模型可讓您同時執行低優先順序的 GPU 工作和不可部分完成的作業，讓一個 GPU 執行緒在不封鎖的情況下，使用另一個未同步處理的執行緒的結果。
-   高優先順序的計算工作-這項設計可讓需要中斷3D 轉譯的案例，以執行少量的高優先順序計算工作，讓您可以提早取得結果，以在 CPU 上進行額外的處理。

## <a name="initializing-a-command-queue"></a>初始化命令佇列

您可以藉由呼叫 [**ID3D12Device：： CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)來建立命令佇列。 這個方法會採用 [**D3D12 \_ 命令 \_ 清單 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) ，指出應該建立哪一種類型的佇列，因此可以將哪些類型的命令提交至該佇列。 請記住，您只能從直接命令清單呼叫套件組合，而且無法直接提交至佇列。 支援的佇列類型為：

-   [**D3D12 \_ 命令 \_ 清單 \_ 類型 \_ DIRECT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ 命令 \_ 清單 \_ 類型 \_ 計算**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ 命令 \_ 清單 \_ 類型 \_ 複製**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

一般情況下，直接佇列和命令清單都會接受任何命令、計算佇列和命令清單接受計算和複製相關命令，而複製佇列和命令清單只接受複製命令。

## <a name="executing-command-lists"></a>執行命令清單

在您錄製命令清單並取出預設的命令佇列或建立新的佇列之後，您可以藉由呼叫 [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)來執行命令清單。

應用程式可以從多個執行緒將命令清單提交至任何命令佇列。 執行時間會依照提交循序執行序列化這些要求的工作。

執行時間會驗證提交的命令清單，如果違反任何限制，則會捨棄 [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 的呼叫。 由於下列原因，將會捨棄呼叫：

-   提供的命令清單是組合，而不是直接命令清單。
-   未在提供的命令清單上呼叫 [**ID3D12GraphicsCommandList：： Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) ，以完成錄製。
-   已在命令建立器上呼叫 [**ID3D12CommandAllocator：： Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) ，因為它已記錄。 如需有關命令配置器的詳細資訊，請參閱 [建立和錄製命令清單和](recording-command-lists-and-bundles.md)組合。
-   命令佇列隔離表示之前的命令清單執行尚未完成。 以下將詳細討論命令佇列的範圍。
-   查詢的前後狀態（使用 [**ID3D12GraphicsCommandList：： BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**ID3D12GraphicsCommandList：： EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)的呼叫設定）未正確地相符。
-   資源轉換屏障的前後狀態未正確地相符。 如需詳細資訊，請參閱 [使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)。

## <a name="accessing-resources-from-multiple-command-queues"></a>從多個命令佇列存取資源

執行時間有幾個規則會限制來自多個命令佇列的資源存取。 這些規則如下：

1. 無法同時從多個命令佇列寫入資源。 當資源轉換為佇列上的可寫入狀態時，該佇列會被視為獨佔擁有，而且必須轉換到讀取或一般狀態 (請參閱 [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) ，才能讓另一個佇列存取該資源。

2. 處於讀取狀態時，可以從多個命令佇列同時讀取資源（包括跨進程），並以其讀取狀態為基礎。

如需資源存取限制和使用資源阻礙來同步存取資源的詳細資訊，請參閱 [使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)。

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>使用命令佇列圍牆同步處理命令清單執行

在 Direct3D 12 中對多個平行命令佇列的支援，可讓您更靈活地控制 GPU 上非同步工作的優先順序。 這種設計也表示應用程式必須明確管理工作的同步處理，特別是當命令清單中的命令清單相依于另一個命令佇列正在操作的資源時。 其中一些範例包括等候計算佇列上的作業完成，讓結果可用於3D 佇列上的轉譯作業，並等候3D 作業完成，讓計算佇列上的作業可以存取資源以進行寫入。 為了讓佇列之間的工作同步處理，Direct3D 12 使用了 [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) 介面在 API 中表示的圍牆概念。

範圍是一個整數，代表目前正在處理的工作單位。 當應用程式透過呼叫 [**ID3D12CommandQueue：：信號**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)來推進範圍時，會更新整數。 應用程式可以檢查範圍的值，並判斷是否已完成工作單位，以決定是否可以啟動後續作業。

## <a name="synchronizing-resources-accessed-by-command-queues"></a>同步處理命令佇列所存取的資源

在 Direct3D 12 中，將某些資源的狀態同步處理時，會有資源阻礙。 在每個資源屏障中，應用程式會宣告資源的前後狀態。 常見的範例是讓資源在著色器資源檢視之間轉換成轉譯目標視圖。 在大部分的情況下，這些資源阻礙都是在命令清單中進行管理。 啟用調試層時，系統會強制所有資源的之前和之後狀態相符，以保證資源在關卡轉換時處於特定作業的正確狀態。

如需有關同步處理資源狀態的詳細資訊，請參閱 [使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)。

## <a name="command-queue-support-for-tiled-resources"></a>磚資源的命令佇列支援

管理透過 Direct3D 11 中的 [**ID3D11DeviceCoNtext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) 介面公開之磚資源的方法，是由 direct3d 12 中的 [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) 介面所提供。 這些方法包括：



| 方法                                                              | 描述                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | 將來源磚資源的對應複製到已並排顯示的資源。<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | 將並排顯示資源中的磚位置對應更新為資源堆積中的記憶體位置。<br/> |



 

如需在 Direct3D 12 應用程式中使用已磚資源的詳細資訊，請參閱 Direct3D11 並排顯示的 [資源](/windows/desktop/direct3d11/tiled-resources)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)
</dt> </dl>

 

