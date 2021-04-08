---
description: 複製及存取 (Direct3D 10) 的資源資料
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: 複製及存取 (Direct3D 10) 的資源資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688936"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>複製及存取 (Direct3D 10) 的資源資料

您不再需要考慮在影片記憶體或系統記憶體中建立的資源。 或執行時間是否應該管理記憶體。 由於新的 WDDM (Windows 顯示驅動程式模型) 的架構，應用程式現在會使用不同的 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 方式旗標來建立 Direct3D 10 資源，以指出應用程式如何使用資源資料。 新的驅動程式模型會虛擬化資源所使用的記憶體;然後，作業系統/驅動程式/記憶體管理員會負責將資源放在最具效能的記憶體區域中，以提供預期的使用量。

在預設案例下，資源可供 GPU 使用。 當然，在某些情況下，CPU 的資源資料必須可供使用。 若要將資源予以複製，使適當的處理器可在不影響效能的情況下進行存取，您需要具備 API 方法運作方式的基本知識。

-   [複製資源資料](#copying-and-accessing-resource-data-direct3d-10)
-   [存取資源資料](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>複製資源資料

Direct3D 執行建立呼叫時，會在記憶體中建立資源。 他們可以在視訊記憶體、系統記憶體，或任何其他類型的記憶體之中建立。 由於 WDDM 驅動程式模型會把此記憶體虛擬化，應用程式不再需要追蹤資源究竟是建立於哪一種記憶體之中。

理想中，所有資源最好都位於視訊記憶體之中，以供 GPU 立即存取。 然而，有時候資源資料必須供 CPU 進行讀取，或是讓 CPU 已寫入的資源資料供 GPU 進行存取。 Direct3D 10 會要求應用程式指定使用方式來處理這些不同的情況，然後在必要時提供數個方法來複製資源資料。

根據建立資源的方式，並不一定都可以直接存取基礎資料。 這表示資源資料必須從來源資源中複製到另一個可供適當處理器進行存取的資源。 就 Direct3D 10 而言，GPU 可以直接存取預設資源，CPU 可直接存取動態和暫存資源。

一旦建立資源之後，就無法變更其 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 方式。 但您可以將一個資源的內容複製到另一個被指定為不同使用方式的資源之中。 Direct3D 10 以三種不同的方法提供這項功能。 前兩個方法 ( [**ID3D10Device：： CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) 是設計用來將資源資料從某個資源複製到另一個資源。 第三種方法 ([**ID3D10Device：： UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) 設計來將資料從記憶體複製到資源。

資源可分為兩種︰可對應與不可對應。 以動態或暫存使用方式建立的資源為可對應資源，而以預設或不可變動使用方式建立的資源為不可對應資源。

在不可對應資源之間複製資料非常迅速，因為這是最常見的案例，其執行也已最佳化。 由於這些資源無法由 CPU 直接存取，因此其已進行最佳化，使 GPU 可以快速地對其進行操作。

在可對應資源之間複製資料則可能較容易發生問題，因為其效能將會取決於資源建立時指定的使用方式。 例如：GPU 可以快速地讀取動態資源，但卻無法對其進行寫入，並且 GPU 無法直接地讀取或寫入暫存資源。

如果應用程式想要將資料從具有預設使用量的資源複製到具有暫存使用量的資源 (以允許 CPU 讀取資料（亦即，GPU readback 問題) 必須小心執行此動作。 如需此最後一個案例的詳細資訊，請參閱 [存取資源資料](#copying-and-accessing-resource-data-direct3d-10) 。

## <a name="accessing-resource-data"></a>存取資源資料

存取資源需必須先對應該資源。基本上，「對應」即表示應用程式正在嘗試讓 CPU 對記憶體進行存取。 為使 CPU 能存取基本記憶體而對資源進行對應的程序，可能會導致某些效能瓶頸。基於這個原因，應注意如何及何時執行這項工作。

若應用程式嘗試在錯誤的時間點進行對應資源，其執行效能可能會降低到停止的程度。 若應用程式嘗試在作業完成之前對其結果進行存取，將可能導致管線停頓。

若在錯誤的時間點進行對應作業，可能會因為強制 GPU 與 CPU 互相同步而導致效能嚴重下降 。 此同步動作會在應用程式嘗試在 GPU 完成將資源複製到另一個 CPU 可以對應的資源前對其進行存取時發生。

CPU 只能從使用 D3D10 \_ 使用量暫存旗標建立的資源讀取 \_ 。 由於使用此旗標建立的資源無法設定為管線的輸出，因此，如果 CPU 想要讀取 GPU 所產生之資源中的資料，則必須將資料複製到以預備旗標建立的資源。 應用程式可以使用 [**ID3D10Device：： CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 或 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) 方法將某個資源的內容複寫到另一個資源。 然後，應用程式可以藉由呼叫適當的 Map 方法來取得此資源的存取權。 當不再需要存取資源時，應用程式應該呼叫對應的取消對應方法。 例如， [**ID3D10Texture2D：： Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) 和 [**ID3D10Texture2D：：**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap)Map。 不同的對應方法會根據輸入旗標傳回一些特定的值。 如需詳細資訊，請參閱 [**地圖備註一節**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) 。

> [!Note]  
> 當應用程式呼叫 Map 方法時，它會接收要存取的資源資料指標。 執行時間可確保指標具有特定的對齊方式，視 [功能等級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)而定。 針對 [**D3D \_ 功能 \_ 層級 \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) 和更高，指標會對齊16個位元組。 若低於 [**D3D \_ 功能 \_ 層級 \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)，指標會對齊4個位元組。 16位元組的對齊可讓應用程式以原生方式對資料執行 [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))優化的作業，而不需要重做或複製。

 

### <a name="performance-considerations"></a>效能考量

建議您將您的電腦視為一台以兩種不同類型處理器構成的平行結構運作的機器︰一個或多個 CPU，以及一個或多個 GPU。 如同任何平行結構一樣，當每個處理器都排程了足夠的工作，以避免其進入閒置狀態或等待別的處理器完成工作時，運作才可達到最佳效能。

GPU/CPU 平行處理原則中最糟的情況，就是強制一個處理器等候另一個處理器工作完成的結果。 Direct3D 10 會嘗試將 [**ID3D10Device：： CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) 方法設為非同步，以移除這項成本;在方法傳回時，不一定會執行複製。 其優點在於應用程式不需要在 CPU 存取資料時才付出效能降低的成本，即呼叫 Map 方法時。 若 Map 方法在資料確實複製後才被呼叫，便不會造成任何效能上的損失。 另一方面，若 Map 方法在資料複製之前就被呼叫，便會發生管線停頓。

Direct3D 10 中的非同步呼叫 (是大部分的方法，尤其是轉譯呼叫) 會儲存在所謂的命令緩衝區中。 這個緩衝區位於圖形驅動程式的內部，並用來對基礎硬體進行批次呼叫，使 Microsoft Windows 從使用者模式切換至核心模式這種極為耗費成本狀況的發生能夠盡量減少。

命令緩衝區在下列四種情況下會被排清，並造成使用者/核心模式的切換。

1.  會呼叫 [**目前**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present)的。
2.  呼叫 [**ID3D10Device：： Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) 。
3.  命令緩衝區已滿。其大小為動態且由作業系統及圖形驅動程式控制。
4.  CPU 需要存取命令緩衝區中一個尚待執行命令的結果。

在以上四種情況中，第四種情況會對效能造成最嚴重的影響。 如果應用程式發出 [**ID3D10Device：： CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 或 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) 呼叫，此呼叫會在命令緩衝區中排入佇列。 如果應用程式接著在清除命令緩衝區之前，嘗試對應做為複製呼叫目標的預備資源，將會發生管線延遲，因為不僅需要執行複製方法呼叫，還必須執行命令緩衝區中所有其他已緩衝處理的命令。 這將會導致 GPU 與 CPU 進行同步，因為 CPU 將會等待 GPU 清空命令緩衝區並填滿 CPU 需要的資源後，才能存取暫存資源。 當 GPU 完成複製之後，CPU 才會開始存取暫存資源，然而此期間 GPU 就會進入閒置狀態。

若經常性地在執行階段進行此動作，將會大幅降低效能。 基於這個原因，對應以預設使用方式建立的資源時，應小心謹慎。 應用程式必須等候夠長的時間，讓命令緩衝區被清空並且完成執行佇列中所有的命令，才能嘗試對應相對應的暫存資源。 應用程式應該等候多久才行？ 至少需要等待兩個影格的時間，因為這樣才能使 CPU 和 GPU 之間的平行處理原則得到最大且有效率的調控。 GPU 的運作方式，是當應用程式藉由送出呼叫到命令緩衝區中以處理第 N 個影格時，GPU 正忙碌於執行前一個影格 (N-1) 的呼叫。

因此，如果應用程式想要對應源自于影片記憶體的資源，並在畫面格 N 呼叫 [**ID3D10Device：： CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 或 [**ID3D10Device：： CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) ，則當應用程式提交下一個框架的呼叫時，此呼叫實際上會開始在畫面格 n + 1 上執行。 複製應會在應用程式正在處理第 N+2 個影格時完成。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frame</th>
<th>GPU/CPU 狀態</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>CPU 為目前的影格送出轉譯呼叫。</li>
</ul></td>
</tr>
<tr class="even">
<td>N+1</td>
<td><ul>
<li>GPU 執行 CPU 在第 N 個影格時送出的呼叫。</li>
<li>CPU 為目前的影格送出轉譯呼叫。</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+2</td>
<td><ul>
<li>GPU 完成執行 CPU 在第 N 個影格時送出的呼叫。結果準備就緒。</li>
<li>GPU 執行 CPU 在第 N+1 個影格時送出的呼叫。</li>
<li>CPU 為目前的影格送出轉譯呼叫。</li>
</ul></td>
</tr>
<tr class="even">
<td>N+3</td>
<td><ul>
<li>GPU 完成執行 CPU 在第 N+1 個影格時送出的呼叫。 結果準備就緒。</li>
<li>GPU 執行 CPU 在第 N+2 個影格時送出的呼叫。</li>
<li>CPU 為目前的影格送出轉譯呼叫。</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
