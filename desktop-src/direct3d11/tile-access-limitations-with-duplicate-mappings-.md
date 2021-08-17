---
title: 重複對應的磚存取限制
description: 本節說明重複對應的磚存取限制。
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ea4839b8115ccffe1993d767bc19d2d7c3db0c230aff65f8dd0fd9f74d3cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124116"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>重複對應的磚存取限制

本節說明重複對應的磚存取限制。

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>使用重迭的來源和目的地複製並排顯示的資源

如果複製作業的 [來源] 和 [目的地] 區域中的圖格在 \* 複製區域中有重複的對應，即使這兩個資源並未並排顯示資源，而複製作業 \* 支援重迭的複本，複製作業的 \* 行為會 (，就像是在進入目的地) 之前，將來源複製到暫存位置一樣。 但如果重疊不明顯 (例如來源和目的地資源不同，但給定表面上的共用對應或對應重複)，則不會定義共用磚上複製作業的結果。

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>複製到具有重複磚的已並排資源，目的區域中有重複的磚

除非資料本身相同，否則複製到目的區域中具有重複磚的磚資源會在這些磚中產生未定義的結果;不同的磚可能會以不同的順序來撰寫磚。

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>UAV 對重複磚對應的存取

假設未排序的存取視圖 (磚上的 UAV) 在其區域中有重複的磚對應，或與其他系結至管線的資源相同。 若由不同執行緒則執行，則不會定義這些重複磚的存取順序，就像任何 UAV 記憶體存取的順序通常都未排序。

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>磚對應變更或內容從對應外部更新後轉譯

如果並排顯示的資源圖格對應已變更，或已對應的磚化集區磚中的內容已透過另一個已並排的資源對應變更，而並排顯示的資源將會透過轉譯目標視圖或深度樣板視圖來呈現，應用程式必須使用固定的函式 Clear Api 來清除 (，) 或使用複製/Update api 完整複製已在轉譯 \* \* 的區域中變更的磚 (對應或不) 。 在這些情況下，如果應用程式無法清除或複製，會導致指定的轉譯目標視圖或深度樣板視圖的硬體優化結構過時，並且會導致在不同硬體上的一些硬體和不一致的情況下產生垃圾收集結果。 硬體所使用的這些隱藏的最佳化資料結構可能對個別對應而言為本機項目，而不會對其他記憶體相同的對應顯示。

[**ID3D11DeviceCoNtext1：： ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)作業支援清除具有矩形的呈現目標視圖。 針對支援並排顯示資源的硬體， **ClearView** 也必須支援清除具有矩形的深度樣板視圖，以取得沒有樣板) 的深度 (表面。 這項作業可讓應用程式只清除表面的必要區域。

如果應用程式需要在對應已變更的磚資源中保留區域的現有記憶體內容，則該應用程式必須解決清楚的需求。 應用程式可以藉由將圖格對應變更 (的內容（例如，使用 [**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)) 、發出必要的 clear 命令，然後將內容複寫回來），來完成這項工作。 雖然這可完成為遞增轉譯保存表面內容的工作，但缺點是表面的後續轉譯效能可能效能降低，因為轉譯最佳化可能遺失。

如果圖格同時對應到多個並排顯示的資源，並透過任何方式來操作磚內容， (透過其中一個並排顯示的資源轉譯、複製等) ，而且如果相同磚是透過任何其他並排顯示的資源轉譯，則必須先清除磚，如先前所述。

## <a name="rendering-to-tiles-shared-outside-render-area"></a>轉譯至在轉譯區域以外共用的磚

假設正在將並排顯示的資源中的某個區域轉譯為，而且轉譯區域所參考的磚集區磚也會從呈現區域外對應到， (包括透過其他並排顯示的資源，而不是) 。 透過其他對應檢視時，轉譯至這些磚的資料並不保證會正確顯示，即使基礎記憶體配置相容也一樣。 這是因為某些硬體所使用的最佳化資料結構對可轉譯表面的個別對應而言可能為本機，但不會對記憶體位置相同的其他對應顯示。 您可以從轉譯對應複製到所有其他可能存取之記憶體相同的對應 (或者若不再需要舊的內容，即可清除該記憶體或將其他資料複製到其中) 來因應這項限制。 雖然這項因應措施看起來很冗餘，但可讓所有其他記憶體相同的對應正確了解如何存取其內容，且至少因為只有單一實體記憶體備份保持不變而節省記憶體。 此外，當您在使用 (共用對應的不同並排顯示資源之間切換時，除非唯讀取) ，否則您必須在參數之間呼叫 [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) API。

## <a name="rendering-to-tiles-shared-within-render-area"></a>轉譯至在轉譯區域以內共用的磚

如果並排顯示資源中的區域正在轉譯，且在轉譯區域內有多個圖格對應到相同的磚集區位置，則轉譯結果在這些磚上不會定義。

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>跨磚資源分享磚的資料相容性

假設有多個並排顯示的資源對應至相同的磚集區位置，而每個資源都用來存取相同的資料。 這種情況只有在避免硬體優化結構發生問題的其他規則被避免、適當呼叫 [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) ，以及並排顯示的資源彼此相容時，才有效。 在這裡會說明後者，以將共用磚的並排資源視為不相容的意義。 存取重複磚對應之間相同資料的不相容情況是使用不同的表面維度或格式，或是資源上轉譯目標或深度樣板繫結旗標呈現的差異。 若您後續透過來自不相容資源的對應進行讀取或轉譯，則使用一種對應寫入記憶體會產生未定義的結果。 若另一個資源共用對應首先使用新資料初始化 (回收記憶體作為其他用途)，則後續讀取或轉譯作業會運作正常，因為資料不會在不相容的解譯間洩出。 但是，當您在存取像這樣的不相容對應之間切換時，必須呼叫 **TiledResourceBarrier** API。

如果在任何資源共用對應上彼此都未設定轉譯目標或深度樣板繫結旗標，則限制大為降低。 只要格式及表面類型 (例如 Texture2D) 相同，即可共用磚。 不同的格式是相容的案例，例如 BC 介面 \* ，以及每個元件格式的相等大小未壓縮32位或16位，例如 BC6H 和 R32G32B32A32。 許多32位的每個元素格式也可以使用 R32 來加上別名， \_ \* (R10G10B10A2 \_ \* 、R8G8B8A8 \_ \* 、B8G8R8A8 \_ \* 、B8G8R8X8 \_ \* 、R16G16 \_ \*) ; 這項作業一律允許用於非並排的資源。

如果格式相容且磚會填入純色，則壓縮與非壓縮磚之間的共用會運作良好。

最後，如果資源共用磚對應之間唯一的共同點是其皆不具轉譯目標或深度樣板繫結旗標，則僅可安全地共用填入 0 的記憶體；對應會顯示為任何 0 針對給定資源格式定義的解碼目標 (通常僅為 0)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




