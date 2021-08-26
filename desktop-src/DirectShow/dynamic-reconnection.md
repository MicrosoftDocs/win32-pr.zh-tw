---
description: 動態重新連接
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: 動態重新連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966151"
---
# <a name="dynamic-reconnection"></a>動態重新連接

在大部分的 DirectShow 篩選準則中，當圖形正在主動串流資料時，無法重新連接 pin。 應用程式必須在重新連接釘選之前停止圖形。 不過，某些篩選器在圖形執行時支援 pin 重新連接，這項程式稱為動態重新連接。 這可以透過應用程式或圖形中的篩選來完成。

例如，請考慮下圖中的圖表。

![動態圖形-建立圖表](images/dyngraph.png)

動態重新連線的其中一個案例可能是在圖形執行時從圖形移除篩選2，然後將它取代為另一個篩選準則。 若要讓此案例正常運作，必須符合下列條件：

-   篩選 3 (pin D) 的輸入 pin 必須支援 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面。 此介面可讓您在不停止篩選的情況下重新連接 pin。
-   篩選 1 (釘選) 的輸出釘選，必須能夠在進行重新連線時封鎖媒體資料的流程。 在重新連線期間，pin A 與 pin D 之間不會有任何資料移動。 一般來說，這表示輸出的 pin 必須支援 [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) 介面。 但是，如果篩選1是起始重新連線的篩選，它可能會有一些內部機制來封鎖其本身的資料流程。

動態重新連接將牽涉到下列步驟：

1.  封鎖來自 pin A 的資料流程。
2.  重新連接釘選至 pin D，可能是透過新的中繼篩選。
3.  解除封鎖 pin A，讓資料再次開始流動。

**步驟1。封鎖資料流程**

若要封鎖資料流程，請呼叫釘選上的 [**IPinFlowControl：： block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 。您可以非同步或同步方式呼叫這個方法。 若要以 *非同步* 方式呼叫方法，請建立 Win32 事件物件，並將事件控制碼傳遞給 **Block** 方法。 方法將會立即傳回。 使用 **WaitForSingleObject** 之類的函式，等候事件收到信號。 Pin 會在事件封鎖資料流程時發出信號。 例如：


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



若要 *同步* 呼叫方法，只要傳遞 **Null** 值，而不是事件控制碼。 現在方法會封鎖，直到作業完成為止。 在 pin 準備好傳遞新的範例之前，可能不會發生這種情況。 如果已暫停篩選，這可能會花費任意的時間長度。 因此，請勿從主應用程式執行緒進行同步呼叫。 請使用背景工作執行緒，否則請以非同步方式呼叫方法。

**步驟2。重新連接釘選**

若要重新連接 pin，請查詢 **IGraphConfig** 介面的篩選 Graph 管理員，然後呼叫 [**IGraphConfig：： reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect)或 [**IGraphConfig：：重新**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure)設定。 **Reconnect** 方法更容易使用;它會執行下列動作：

-   在範例) 中停止中繼篩選 (篩選2，並將其從圖形中移除。
-   視需要新增中繼篩選準則。
-   連接所有的釘選。
-   暫停或執行任何新的篩選準則，以符合圖形的狀態。

**Reconnect** 方法有幾個選擇性參數，可用來指定要使用的 pin 連接和中繼篩選的媒體類型。 例如：


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



如需詳細資訊，請參閱參考頁面。 如果 **重新連接** 方法沒有足夠的彈性，您可以使用 **重新** 設定方法，它會呼叫應用程式定義的回呼方法來重新連接釘選。 若要使用此方法，請在您的應用程式中執行 [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) 介面。

在呼叫 **重新** 設定之前，請依先前所述，封鎖輸出釘選的資料流程。 然後在您要重新連接的圖表區段中，推送仍在擱置中的任何資料，如下所示：

1.  在) 範例中， (pin D 的輸入 pin 上呼叫 [**IPinConnection：： NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) 。 傳入 Win32 事件的控制碼。
2.  在輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ，這會從您封鎖資料流程的輸出 pin 立即下游。  (在此範例中，資料流程被封鎖在釘選 A 上，因此您會在 pin B 上呼叫 **EndOfStream** 。 ) 
3.  等候事件收到信號。 輸入 pin (pin D) 在接收到資料流程結束通知時，對事件發出信號。 這表示 pin 之間沒有任何資料正在移動，且呼叫者可以安全地重新連接 pin。

請注意， **IGraphConfig：： Reconnect** 方法會自動處理先前的步驟。 如果您使用 [ **重新** 設定] 方法，則只需要執行這些步驟。

資料透過圖形推送之後，請呼叫 **重新** 設定，並將指標傳遞至您的 **IGraphConfigCallback** 回呼介面。 篩選 Graph 管理員將會呼叫您所提供的 [**IGraphConfigCallback：：重新**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure)設定方法。

**步驟3。解除封鎖資料 Flow**

當您重新連接釘選之後，請呼叫 **IPinFlowControl：： Block** ，將第一個參數的值為零，以解除封鎖資料流程。

> [!Note]  
> 如果動態重新連接是由篩選執行，則有一些您必須注意的執行緒問題。 如果篩選 Graph 管理員嘗試停止篩選，可能會因為圖形等候篩選停止，同時篩選器可能正在等候資料透過圖形推送，而導致鎖死。 為了避免可能的鎖死，本節所述的部分方法會採取 Win32 事件的控制碼。 如果篩選準則 Graph 管理員嘗試停止篩選，則篩選準則應該會通知事件。 如需詳細資訊，請參閱 [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) 和 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態 Graph 大樓](dynamic-graph-building.md)
</dt> </dl>

 

 



