---
title: 從 Direct3D 11 到 Direct3D 12 的重要變更
description: Direct3D 12 代表來自 Direct3D 11 程式設計模型的重大起飛。 Direct3D 12 讓應用程式比以往更接近硬體。
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3afc5fe9a451addf1d1f7b9aeddf1f55ca40a22db99134ba71d8195c72ad2b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123831"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>從 Direct3D 11 到 Direct3D 12 的重要變更

Direct3D 12 代表來自 Direct3D 11 程式設計模型的重大起飛。 Direct3D 12 讓應用程式比以往更接近硬體。 藉由更接近硬體，Direct3D 12 的速度更快且更有效率。 但是，使用 Direct3D 12 提高速度和效率的應用程式取捨，就是您負責比使用 Direct3D 11 更多的工作。

-   [明確同步處理](#explicit-synchronization)
-   [實體記憶體常駐管理](#physical-memory-residency-management)
-   [管線狀態物件](#pipeline-state-objects)
-   [命令清單和套件組合](#command-lists-and-bundles)
-   [描述元堆積和資料表](#descriptor-heaps-and-tables)
-   [從 Direct3D 11 移植](#porting-from-direct3d-11)
-   [相關主題](#related-topics)

Direct3D 12 會傳回低層級的程式設計;藉由引進下列新功能，可讓您更充分掌控遊戲和應用程式的圖形元素：代表管線整體狀態的物件、用於工作提交的命令清單和組合，以及用來存取資源的描述項堆積和資料表。

您的應用程式透過 Direct3D 12 提高速度和效率，但您必須負責比使用 Direct3D 11 更多的工作。

## <a name="explicit-synchronization"></a>明確同步處理

-   在 Direct3D 12 中，CPU-GPU 同步處理現在是應用程式的明確責任，而且執行時間不再隱含地執行，因為它在 Direct3D 11 中。 這項事實也表示，Direct3D 12 不會執行管線風險的自動檢查，因此這是應用程式的責任。
-   在 Direct3D 12 中，應用程式負責管線資料更新。 也就是說，Direct3D 11 中的「對應/鎖定-捨棄」模式必須在 Direct3D 12 中以手動方式執行。 在 Direct3D 11 中，如果您在呼叫 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) 與 [**D3D11 \_ Map \_ WRITE \_ 捨棄**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map)時，GPU 仍在使用緩衝區，則執行時間會傳回新的記憶體區域的指標，而不是舊的緩衝區資料。 這可讓 GPU 在應用程式將資料放在新的緩衝區時，繼續使用舊的資料。 應用程式不需要額外的記憶體管理;當 GPU 完成時，會自動重複使用或終結舊的緩衝區。
-   在 Direct3D 12 中，所有動態更新 (包括常數緩衝區、動態頂點緩衝區、動態紋理等) 都是由應用程式明確控制。 這些動態更新包含任何必要的 GPU GPU 或緩衝。 應用程式會負責保持可用的記憶體，直到不再需要為止。
-   Direct3D 12 只針對介面存留期使用 COM 樣式的參考計數， (使用與裝置) 的存留期系結的 Direct3D 的弱式參考模型。 所有資源和描述記憶體存留期都是由應用程式負責維持適當期間的唯一責任，而且不會被參考計數。 Direct3D 11 也會使用參考計數來管理介面相依性的存留期。

## <a name="physical-memory-residency-management"></a>實體記憶體常駐管理

Direct3D 12 應用程式必須防止多個佇列、多個介面卡和 CPU 執行緒之間的競爭條件。 D3D12 不會再同步處理 CPU 和 GPU，也不支援資源重新命名或多重緩衝的便利機制。 在另一個處理單位完成使用之前，必須使用 gpu 來避免多個處理單位從多個記憶體單元寫入記憶體。

在 GPU 讀取資料時，Direct3D 12 應用程式必須確保資料會常駐在記憶體中。 每個物件所使用的記憶體，會在建立物件時成為常駐。 呼叫這些方法的應用程式必須使用 GPU，以確保 GPU 不會存取已收回的物件。

資源障礙是所需的另一種同步處理類型，可用來同步處理資源和 subresource 轉換（在非常細微的層級）。

請參閱 [Direct3D 12 中的記憶體管理](memory-management.md)。

## <a name="pipeline-state-objects"></a>管線狀態物件

Direct3D 11 可讓您透過一組大型的獨立物件來操作管線狀態。 例如，輸入組合語言狀態、圖元著色器狀態、轉譯器狀態和輸出合併狀態都可以獨立修改。 這項設計提供圖形管線的方便且相對高階的標記法，但它並不會利用新式硬體的功能，主要是因為各種狀態通常是相互依存的。 例如，許多 Gpu 將圖元著色器和輸出合併狀態合併成單一硬體標記法。 但由於 Direct3D 11 API 允許個別設定這些管線階段，因此顯示驅動程式無法解決管線狀態的問題，直到狀態完成為止，而不是在繪製時間之前。 此配置會延遲硬體狀態設定，這表示每個框架有額外的額外負荷和最多繪製呼叫數。

Direct3D 12 藉由將許多管線狀態整合至不可變的管線狀態物件 (Pso) （在建立時完成）來解決此配置。 然後，硬體和驅動程式就可以立即將 PSO 轉換為執行 GPU 工作所需的任何硬體原生指示和狀態。 您仍然可以動態地變更正在使用的 PSO，但若要這麼做，硬體只需要將最少量的預先計算狀態直接複製到硬體暫存器，而不是即時計算硬體狀態。 藉由使用 Pso，繪製呼叫的額外負荷會大幅減少，而且每個框架可能會發生許多繪製呼叫。 如需 Pso 的詳細資訊，請參閱 [管理 Direct3D 12 中的圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)。

## <a name="command-lists-and-bundles"></a>命令清單和套件組合

在 Direct3D 11 中，所有的工作提交都是透過 [立即內容](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render)來完成，這代表一種可移至 GPU 的命令資料流程。 為了達成多執行緒調整，遊戲也有 [延遲](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) 的內容可供使用。 Direct3D 11 中的延遲內容無法完美地對應到硬體，因此可以在這些環境中執行相對較少的工作。

Direct3D 12 根據命令清單導入了新的工作提交模型，其中包含在 GPU 上執行特定工作負載所需的完整資訊。 每個新的命令清單都包含資訊，例如要使用的 PSO、所需的材質和緩衝區資源，以及所有繪製呼叫的引數。 因為每個命令清單都是獨立的，而且不會繼承任何狀態，所以驅動程式可以預先預先計算所有必要的 GPU 命令，並以無限制執行緒的方式預先計算。 唯一需要的序列程式是透過命令佇列最終將命令清單提交至 GPU 的程式。

除了命令清單之外，Direct3D 12 還引進了第二層的工作預先計算：配套 *。* 不同于完全獨立且通常會進行程式化、提交一次和捨棄的命令清單，配套提供允許重複使用的狀態繼承形式。 例如，如果遊戲想要使用不同的紋理來繪製兩個字元模型，其中一個方法是使用兩組完全相同的繪製呼叫來記錄命令清單。 但另一種方法是「錄製」一個組合來繪製單一字元模型，然後使用不同的資源在命令清單上「播放」組合兩次。 在後者的情況下，顯示驅動程式只需要計算適當的指示一次，而建立的命令清單基本上相當於兩個低成本的函式呼叫。

如需命令清單和組合的詳細資訊，請參閱 [Direct3D 12 中的工作提交](command-queues-and-command-lists.md)。

## <a name="descriptor-heaps-and-tables"></a>描述元堆積和資料表

Direct3D 11 中的資源系結是高度抽象化且方便的，但會使許多新式硬體功能的使用量變低。 在 Direct3D 11 中，遊戲會建立資源的 *view* 物件，然後將這些視圖系結至管線中不同著色器階段 *的數個* 位置。 著色器接著會從這些明確系結位置讀取資料，這些位置是在繪製時固定的。 此模型表示每當遊戲使用不同的資源繪製時，它必須將不同的視圖重新系結至不同的位置，然後再次呼叫 draw。 這種情況也代表可透過充分利用新式硬體功能來消除的額外負荷。

Direct3D 12 將系結模型變更為符合新式硬體，並大幅提升效能。 Direct3D 12 不需要獨立的資源查看和明確對應至位置，而是會提供描述項堆積，讓遊戲建立各種資源檢視。 此配置提供一種機制，可讓 GPU 直接將硬體原生資源描述 (描述元) 預先寫入記憶體。 為了宣告管線針對特定繪製呼叫所使用的資源，遊戲會指定一或多個描述中繼資料表，代表完整描述元堆積的子範圍。 由於描述項堆積已經填入適當的硬體特定描述中繼資料，因此變更描述中繼資料表是極低成本的作業。

除了描述項堆積和資料表所提供的效能改進之外，Direct3D 12 還可讓您以著色器動態編制資源的索引，以提供前所未有的彈性並解除新的轉譯技巧。 例如，新式延遲轉譯引擎通常會將某種類型的材質或物件識別碼編碼為中繼 g 緩衝區。 在 Direct3D 11 中，這些引擎必須小心避免使用過多的資料，因為在一個 g 緩衝區中包含太多資料可能會大幅降低最終轉譯行程的速度。 使用動態可編制索引的資源時，具有上千個材質的場景可以像只有十個數據一樣快速完成。

如需描述元堆積和資料表的詳細資訊，請參閱 [資源](resource-binding.md)系結，以及 [來自 Direct3D 11 的系結模型差異](binding-model.md)。

## <a name="porting-from-direct3d-11"></a>從 Direct3D 11 移植

從 Direct3D 11 移植是在 [從 direct3d 11 移植到 direct3d 12](porting-from-direct3d-11-to-direct3d-12.md)中所述的程式。 另請參閱 [使用 direct3d 11、direct3d 10 和 Direct2D](direct3d-12-interop.md)的選項範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解 Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 