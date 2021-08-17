---
description: 篩選狀態
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: 篩選狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015736"
---
# <a name="filter-states"></a>篩選狀態

篩選器有三種可能的狀態：已停止、已暫停且正在執行。 暫停狀態的目的是在圖形中提示資料，讓 run 命令立即回應。 篩選 Graph 管理員會控制所有狀態轉換。 當應用程式呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)、 [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)或 [**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)時，篩選 Graph 管理員會在所有篩選準則上呼叫對應的 [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)方法。 [已停止] 和 [執行] 之間的轉換一律會通過暫停狀態，因此，如果應用程式呼叫在停止的圖形上執行，則篩選 Graph 管理員會在 **執行** 之前暫停圖形。

在大部分的篩選準則下，執行中和暫停狀態都相同。 請考慮下列篩選圖形：

來源 > 轉換 > 轉譯器

現在假設來源篩選準則不是即時的捕獲來源。 當來源篩選暫停時，它會建立一個執行緒，以產生新的資料並儘快將其寫入媒體範例。 執行緒會在轉換篩選的輸入釘上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ，藉以「推送」這些樣本。 轉換篩選器會接收來源篩選準則的執行緒上的範例。 它可能會使用背景工作執行緒將範例傳遞給轉譯器，但通常會在相同的執行緒上傳遞這些範例。 當轉譯器暫停時，它會等候接收範例。 收到一個之後，它會無限期地封鎖並保存該範例。 如果是影片轉譯器，它會將範例顯示為海報影像，並視需要重新繪製影像。

此時，資料流程已完全 cued 且可供轉譯。 如果圖形維持暫停，範例會在第一個範例後方的圖形中「堆積」，直到每個篩選準則在 [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 或 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)中封鎖為止。 但是，不會遺失任何資料。 解除封鎖來源執行緒之後，它就會從它封鎖的點繼續進行。

來源篩選和轉換篩選會忽略從暫停轉換成執行中的轉換，它們只是盡可能快速地處理資料。 但是，當轉譯器執行時，它會啟動轉譯範例。 首先，它會轉譯它暫停時所持有的範例。 然後，每次收到新的範例時，它會計算樣本的呈現時間。  (需詳細資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。 ) 轉譯器會將每個樣本保存到呈現時間，此時會轉譯範例。 當它等候呈現時間時，它會在 [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法中封鎖，或在具有佇列的背景工作執行緒上接收新的範例。 從轉譯器進行上游篩選不牽涉到排程。

即時來源（例如「捕獲裝置」）是此一般架構的例外狀況。 使用即時來源時，不適合事先提示所有資料。 應用程式可能會暫停圖形，然後在執行之前等候很長的時間。 圖形不應該呈現「過時」範例。 因此，在執行時，即時來源不會在暫停的情況下產生樣本。 若要將此事實告知 Graph Manager 的篩選準則，來源篩選的 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)方法會傳回 VFW \_ s 無法 \_ \_ 提示。 這個傳回碼表示篩選已經切換到暫停的狀態，即使轉譯器並未接收任何資料。

當篩選準則停止時，它會拒絕其他傳遞給它的範例。 來源篩選器會關閉串流執行緒，而其他篩選器會關閉任何可能已建立的背景工作執行緒。 Pin 取消認可其配置器。

### <a name="state-transitions"></a>狀態轉換

篩選 Graph 管理員會以上游循序執行所有狀態轉換，從轉譯器開始，然後回到來源篩選器。 這是為了避免卸載樣本，以及防止圖形死結的必要順序。 最重要的狀態轉換介於暫停和停止之間：

-   停止暫停：當每個篩選準則暫停時，就可以開始從下一個篩選器接收樣本。 來源篩選是最後一個要暫停的。 它會建立串流執行緒，並開始傳遞範例。 由於所有下游篩選都已暫停，因此沒有任何篩選器會拒絕任何範例。 篩選 Graph 管理員不會完成轉換，除非圖形中的每個轉譯器都收到具有即時來源例外狀況的範例 (，如先前的) 所述。
-   暫停至已停止：當篩選準則停止時，它會釋出它所保留的任何範例，以解除封鎖任何在 [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)中等候的上游篩選。 如果篩選準則正在等候 [**receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法內的資源，它會停止等待並從 **接收** 傳回，這會解除封鎖呼叫的篩選。 因此，當篩選 Graph 管理員停止下一個上游篩選器時，不會在 **GetBuffer** 或 **Receive** 中封鎖該篩選，而且可以回應停止命令。 上游篩選器可能會在取得停止命令之前提供一些額外的範例，但下游篩選器只會拒絕它們，因為它已停止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選 Graph 中的資料 Flow](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



