---
title: Direct3D 11 on 12
description: D3D11On12 是一種機制，開發人員可以使用 D3D11 介面和物件來驅動 D3D12 API。
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548355"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 on 12

D3D11On12 是一種機制，開發人員可以使用 D3D11 介面和物件來驅動 D3D12 API。 D3D11on12 可讓使用 D3D11 撰寫的元件 (例如，D2D 文字和 UI) 與以 D3D12 API 為目標的元件一起運作。 D3D11on12 也可讓應用程式從 D3D11 增量移植至 D3D12，方法是讓應用程式的某些部分繼續以較簡單的目標為目標，同時讓其他人以 D3D12 為效能，同時一律具有完整且正確的呈現。 D3D11On12 可讓您更輕鬆地使用 interop 技術來共用資源，並在兩個 Api 之間同步處理工作。

-   [正在初始化 D3D11On12](#initializing-d3d11on12)
-   [使用方式範例](#example-usage)
-   [背景](#background)
-   [清除](#cleaning-up)
-   [限制](#limitations)
-   [API](#apis)
-   [相關主題](#related-topics)

## <a name="initializing-d3d11on12"></a>正在初始化 D3D11On12

若要開始使用 D3D11On12，第一個步驟是建立 D3D12 裝置和命令佇列。 這些物件會以輸入的形式提供給初始化方法 [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice)。 您可以將此方法視為使用虛構驅動程式類型 D3D \_ 驅動程式 \_ 類型11ON12 來建立 D3D11 裝置 \_ ，其中 D3D11 驅動程式負責建立物件，並將命令清單提交至 D3D12 API。

當您有 D3D11 裝置和立即內容之後，您就可以 `QueryInterface` 關閉 [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) 介面的裝置。 這是用來在 D3D11 和 D3D12 之間進行 interop 的主要介面。 若要讓 D3D11 裝置內容和 D3D12 命令清單在相同的資源上運作，您必須使用 [**CreateWrappedResource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) API 來建立「包裝的資源」。 這個方法會「升級」 D3D12 資源，以便在 D3D11 中理解。 已包裝的資源會以「已取得」狀態開始，這是由 [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) 和 [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) 方法操作的屬性。

## <a name="example-usage"></a>使用方式範例

D3D11On12 的一般用法是使用 D2D，在 D3D12 背景緩衝區的上方呈現文字或影像。 如需範例程式碼，請參閱 D3D11On12 範例。 以下是執行此動作所需採取步驟的粗略概述：

-   使用 [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)作為輸入) ，建立 D3D12 裝置 ([**D3D12CREATEDEVICE**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) 和 D3D12 交換鏈 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) 。
-   使用 D3D12 裝置和與輸入相同的命令佇列來建立 D3D11On12 裝置。
-   取出交換鏈回緩衝區，並為每個緩衝區建立 D3D11 包裝的資源。 使用的輸入狀態應該是 D3D12 使用它的最後一種方式 (例如，轉譯 \_ 目標) 和輸出狀態應該是 D3D12 在 D3D11 (完成後使用它的方式，例如存在) 。
-   初始化 D2D，並將 D3D11 包裝的資源提供給 D2D，以準備進行轉譯。

然後，在每個畫面上，執行下列動作：

-   使用 D3D12 命令清單轉譯成目前的交換鏈回緩衝區，然後執行它。
-   取得目前的背景緩衝區包裝資源 ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)) 。
-   發出 D2D 轉譯命令。
-    ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)) 釋放包裝的資源。
-   清除 D3D11 立即內容。
-   提供 ([**IDXGISwapChain1：:P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) 。

## <a name="background"></a>背景

D3D11On12 有系統地運作。 每個 D3D11 API 呼叫都會經歷一般的執行時間驗證，並將其傳送至驅動程式。 在驅動層，特殊的11on12 驅動程式會將狀態和問題轉譯作業記錄到 D3D12 命令清單。 這些命令清單會視需要提交 (例如，查詢 `GetData` 或資源 `Map` 可能需要將命令排清) 或由排清要求。 建立 D3D11 物件通常會導致建立對應的 D3D12 物件。 D3D12 不支援 D3D11 中的某些固定函式轉譯作業（例如 `GenerateMips` 或） `DrawAuto` ，因此 D3D11On12 會使用著色器和其他資源來模擬它們。

針對 interop，請務必瞭解 D3D11On12 如何與應用程式建立並提供的 D3D12 物件互動。 為了確保工作會以正確的順序進行，必須先清除 D3D11 立即內容，才能將其他 D3D12 工作提交至該佇列。 也請務必確保提供給 D3D11On12 的佇列必須隨時 drainable。 這表示最後必須滿足佇列上的任何等候，即使 D3D11 轉譯執行緒無限期封鎖也是如此。 在 D3D11On12 插入排清或等候時，請務必小心，因為未來版本可能會變更。 此外，D3D11On12 會自行追蹤和操作資源狀態。 確保狀態轉換一致性的唯一方法，是利用取得/發行 Api 來操作狀態追蹤，以符合應用程式的需求。

## <a name="cleaning-up"></a>清除

若要釋放 D3D11On12 包裝的資源，必須依照下列順序進行兩件事：

-   所有對資源的參考（包括資源的任何視圖）都必須釋放。
-   必須進行延遲的銷毀處理。 確保發生此情況的最簡單方式是叫用立即內容 `Flush` API。

這兩個步驟都完成之後，應該釋出包裝資源所採取的任何參考，D3D12 資源就會成為 D3D12 元件的獨佔擁有者。 請注意，D3D12 仍然需要在完全釋出資源之前等候 GPU 完成，因此在執行上述兩個步驟之前，請務必先保留資源的參考，除非您已確認 GPU 不再使用該資源。

D3D11On12 所建立的所有其他資源或物件，會在 GPU 完成使用時（使用 D3D11's 延遲的銷毀機制），于適當的時間清除。 但是，如果您在 GPU 仍在執行時嘗試釋放 D3D11On12 裝置本身，則可能會封鎖終結，直到 GPU 完成為止。

## <a name="limitations"></a>限制

D3D11On12 層會實作為 D3D11 API 的一小部分，但除了可能會導致轉譯) 不正確的之外，還有一些已知的間隙 (。

從 Windows 10 版本 1809 (10.0;組建 17763) ，只要 D3D11On12 在支援著色器模型6.0 或更新版本的驅動程式上執行，就可以執行使用介面的著色器。 在舊版的 Windows 中，著色器介面功能不會在 D3D11On12 中執行，而且嘗試使用此功能將會造成錯誤和偵錯工具訊息。

從 Windows 10 版本 1803 (10.0;組建 17134) ，D3D11On12 裝置上支援交換鏈。 在舊版的 Windows 中，則不是。

D3D11On12 尚未針對效能優化。 相較于標準 D3D11 驅動程式、最少量的 GPU 額外負荷，以及已知的記憶體額外負荷，可能會有適中的 CPU 負擔。 因此，不建議將 D3D11On12 用於複雜的3D 場景，而是改為使用簡單的場景或2D 轉譯。

## <a name="apis"></a>API

組成11on12 層的 Api 說明于 [11On12 參考](direct3d-11on12-reference.md)中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 D3D11on12 逐步解說的 D2D](d2d-using-d3d11on12.md)
</dt> <dt>

[瞭解 Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[使用 Direct3D 11、Direct3D 10 和 Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 