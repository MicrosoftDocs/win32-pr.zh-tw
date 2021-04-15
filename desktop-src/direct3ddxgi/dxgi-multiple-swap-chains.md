---
description: 為了改善效能，您可能會想要為每個 Direct3D 轉譯裝置建立一個以上的交換鏈。
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: 改善每個轉譯裝置的多個交換鏈效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e356434521054bc13b553c8ae3d6e43d8d98ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467751"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>改善每個轉譯裝置的多個交換鏈效能

為了改善效能，您可能會想要為每個 Direct3D 轉譯裝置建立一個以上的交換鏈。 您可以使用此方法來節省建立其他裝置所需的記憶體，或減少轉譯時間以個別的個別裝置交換鏈呈現，或是節省記憶體並縮短轉譯時間。

-   [每一裝置具有多個交換鏈的應用程式案例](#app-scenarios-with-multiple-swap-chains-per-device)
-   [管理每個裝置的多個交換鏈](#managing-multiple-swap-chains-per-device)
    -   [設定最大框架延遲](#setting-maximum-frame-latency)
    -   [針對每個裝置使用具有多個交換鏈的翻轉模型](#using-flip-model-with-multiple-swap-chains-per-device)
-   [相關主題](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>每一裝置具有多個交換鏈的應用程式案例

當應用程式場景包含個別呈現和更新的顯示物件時，請考慮使用多個鏈。 例如，應用程式經常變更動畫，例如在一側邊的影片和另一端的可滾動文字。 若要儲存通常需要建立額外裝置，並在兩個交換鏈之間共用內容的記憶體，您可以建立系結至相同 Direct3D 轉譯裝置的交換鏈。 針對動畫使用一個交換鏈，並針對文字使用一個交換鏈。 此案例的常見範例是也使用 [DirectComposition](../directcomp/directcomposition-portal.md) API 的 Direct3D 應用程式。

另一種情況是，您想要在多個交換鏈上同時設定多個轉譯目標，以節省轉譯時間。 例如，假設您想要轉譯具有許多材質和幾何的複雜場景，例如軌跡上的賽車，而您想要讓應用程式視窗在兩個顯示視窗中，顯示由兩個交換鏈所轉譯的後端和側面鏡像的視圖。 如果您將多個交換鏈設定為轉譯目標，則您的應用程式不需要分別在每個交換鏈上重複轉譯時間。

## <a name="managing-multiple-swap-chains-per-device"></a>管理每個裝置的多個交換鏈

使用本節中的指導方針來管理您為單一 Direct3D 轉譯裝置所建立的多個交換鏈。

### <a name="setting-maximum-frame-latency"></a>設定最大框架延遲

您可以使用 [**IDXGIDevice1：： SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) 方法來設定作業系統可進行佇列以轉譯至顯示器的最大目前作業數目。 此最大值為每個 Direct3D 轉譯裝置，而不是每個交換鏈。 因此，若要確定作業系統會以預期的 vsync 間隔顯示目前的作業，建議您在每個裝置建立多個翻轉或 bitblt 模型交換鏈時，以及針對每個畫面格呈現多個交換鏈時，不要將畫面格延遲上限設為1。 一般而言，如果您在相同裝置的所有交換鏈之間，每個畫面可靠地只提交2個目前的作業，您可以將畫面格延遲上限設為2。 如果您無法可靠地提交並計算每個畫面格的目前作業，您可以使用 [ [目前的統計資料]](dxgi-flip-model.md) 來追蹤作業系統顯示目前作業的時間。

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>針對每個裝置使用具有多個交換鏈的翻轉模型

當您將 [DXGI 翻轉模型](dxgi-flip-model.md) 與您為單一 Direct3D 轉譯裝置建立的多個交換鏈搭配使用時，請使用這些指導方針。

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>以特定 vsync 間隔作為每個交換鏈目前作業的目標

當您在每個裝置上建立兩個或多個翻轉模型交換鏈時，請注意當您管理裝置狀態的順序，以及所有交換鏈的 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 方法的呼叫順序時，請注意顯示差異。 若要確保作業系統在預期的 vsync 間隔顯示每個交換鏈的現狀，建議您確定已佇列的目前作業數目一律至少小於具有最少重送緩衝區數目之交換鏈的後端緩衝區數目。

### <a name="flip-model-swap-chains-with-two-buffers"></a>使用兩個緩衝區翻轉模型交換鏈

當您的應用程式已排入佇列的目前作業數目小於或等於背景緩衝區的數目時，您的應用程式可以將目標設為特定的 vsync 間隔-1。 此外，您必須個別使用或轉譯為每個交換鏈，然後結束使用每個交換鏈與目前的作業。 因此，當您提交2個緩衝區翻轉模型交換鏈的每一項作業時，您會達到您必須特別注意的背景緩衝區數目閾值，如果您想要讓應用程式以特定 vsync 間隔為目標。

在2個緩衝區交換鏈的案例中，若要以特定 vsync 間隔為目標，您必須確定作業系統在轉譯至下一個緩衝區之前，先完成每個交換鏈目前的作業顯示。 建議您完成設定轉譯目標視圖和其他轉譯狀態、下一次轉譯，然後針對一個交換鏈的兩個緩衝區分別呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) ，然後再對另一個交換鏈執行相同動作。 當您使用兩個或多個交換鏈時，您需要針對每個交換鏈重設裝置上的呈現目標和轉譯狀態。 這種方法的優點是避免一或多個交換鏈的現有作業遺漏其預期的 vsync 間隔。 在第一個範例中，如果應用程式有 [依裝置的多個交換鏈](#app-scenarios-with-multiple-swap-chains-per-device)來變更動畫和文字（以特定的目前間隔為目標），您保證當動畫在一個顯示視窗中更新時，個別交換鏈所轉譯的對應文字也會同時顯示在另一個顯示視窗中。 如果您的應用程式需要以特定 vsync 間隔為目標，您必須遵循此指引。

下圖顯示應用程式中交換鏈轉譯和呈現的程式碼流程範例，其中每個交換鏈都有兩個緩衝區。 在此情況下，您必須針對每個目前的作業，以特定的出現間隔為目標。

![具有兩個緩衝區之翻轉模型的圖例](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>同時將多個交換鏈設定為轉譯目標，以減少轉譯時間

在第二個範例中，賽車是在一張課程上，如 [每個裝置具有多個交換鏈的應用程式案例](#app-scenarios-with-multiple-swap-chains-per-device)中所述，您可能會想要以您在所有交換鏈上同時設定多個轉譯目標所獲得的轉譯時間來達成目標，以節省 vsync 間隔。 在此情況下，您可以同時設定多個轉譯目標、轉譯每個交換鏈上的場景，然後在場景中使用的每個交換鏈上，呼叫 [**IDXGISwapChain1：:P resent1。**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 這種方法的優點是減少轉譯時間。 這種方法的限制是，當您使用2個緩衝區交換鏈時，您的同時交換鏈目前的作業無法以相同的 vsync 為目標。 例如，作業系統將不會顯示競爭汽車並排顯示鏡像的內容，直到從競賽車輛後視圖鏡像看到相同內容之後的 1 vsync 為止。

下圖顯示應用程式中交換鏈轉譯和簡報的程式碼流程範例，其中每個交換鏈都有兩個緩衝區的長度。 在這種類型的範例中，您可以儲存轉譯時間，以交換 A 和 C 的鏈1和2。但是，您無法同步處理緩衝區 A 和 C 的目前作業顯示的 vsync 間隔。 這種模式會針對畫面格2重複。

![同時將多個交換鏈設定為呈現目標的圖解](images/multi-swap-chains-as-render-targets.png)

為了避免因為許多佇列的目前作業而遺失預期的 vsync 間隔，您可以增加每個交換鏈中的背景緩衝區數目。 但這項技術會使用更多的視訊記憶體。 為了避免遺失目標 vsync 間隔，我們建議您一律將排入佇列的作業數目，保持在交換鏈中的緩衝區數目小於最少的後端緩衝區數目。 當您將兩個交換鏈設定為多個轉譯目標時，因為您同時在兩個交換鏈上將兩個目前的作業排入佇列，所以建議您建立至少有三個緩衝區長度的交換鏈。

下圖顯示應用程式中交換鏈轉譯和呈現的程式碼流程範例，其中每個交換鏈都有三個緩衝區的長度。 在這裡，因為任何特定畫面格的佇列顯示數目是2，小於每個交換鏈的後置緩衝區數目，所以您的應用程式可以設定多個轉譯目標，並且仍以相同的 vsync 間隔針對框架2中的緩衝區 A 和 D，以及後續畫面中的緩衝區。

![同時將多個交換鏈設定為轉譯目標的圖例瞄準相同的 vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用翻轉模型、中途矩形和捲動區域增強簡報](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
