---
description: 傳遞範例
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: 傳遞範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385843"
---
# <a name="delivering-samples"></a>傳遞範例

本文描述篩選準則如何提供範例。 它會使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)來描述推送模型、使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)方法和提取模型。

**推送模型：傳遞範例**

輸出釘選會藉由呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法或 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法來傳遞範例，這是相等的，但會傳遞範例的陣列。 輸入 pin 可以封鎖在 **接收** (或 **ReceiveMultiple**) 內。 如果 pin 可能會封鎖，其 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) 方法應該會傳回 S \_ OK。 如果 pin 保證永遠不會封鎖， **ReceiveCanBlock** 應該會傳回 \_ FALSE。 S \_ OK 傳回值並不表示 **Receive** 一律會封鎖，只是它可能會封鎖。

雖然 **Receive** 可以封鎖等候資源變成可用，但不應該封鎖以等候上游篩選器中的更多資料。 這樣做可能會造成鎖死，而上游篩選器會等候下游篩選器釋放範例，因為下游篩選器正在等候上游篩選器，所以永遠不會發生此情況。 不過，如果篩選器有多個輸入圖釘，則一個 pin 可以等候另一個 pin 來接收資料。 例如， [AVI Mux](avi-mux-filter.md) 篩選器會執行此動作，以便能夠交錯音訊和影片資料。

Pin 可能會因為許多原因而拒絕範例：

-   Pin 正在 [排清 (](flushing.md) 請參閱排清) 。
-   Pin 未連接。
-   篩選已停止。
-   發生其他錯誤。

在第一種情況下， **Receive** 方法應該會傳回 \_ FALSE，而在其他情況下則為失敗碼。 當傳回碼是 [否] 時，上游篩選應該會停止傳送範例 \_ 。

您可以將前三個案例視為「預期」失敗，因為篩選準則的狀態不正確，無法接收範例。 非預期的失敗會造成 pin 拒絕範例，即使 pin 處於接收狀態也一樣。 如果發生這種類型的錯誤，則 pin 應該會傳送下游的結束資料流程通知，然後將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送給篩選圖形管理員。

在 DirectShow 基類中， [**CBaseInputPin：： CheckStreaming**](cbaseinputpin-checkstreaming.md) 方法會檢查一般失敗案例（清除、停止等等）。 衍生類別需要檢查篩選準則的特定失敗。 如果發生錯誤， [**CBaseInputPin：： Receive 方法會**](cbaseinputpin-receive.md) 傳送資料流程結束通知和 EC \_ ERRORABORT 事件。

**提取模型：要求範例**

在 **IAsyncReader** 介面中，輸入 pin 會藉由呼叫下列其中一種方法，從輸出 pin 要求範例：

-   [**IAsyncReader：： Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

**要求** 方法為非同步;輸入 pin 會呼叫 [**IAsyncReader：： WaitForNext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext)來等候要求完成。 其他兩種方法是同步的。

**傳遞資料的時機**

篩選準則一律會在其處於執行中狀態時傳遞範例。 在大多數情況下，篩選準則也會在暫停時傳遞範例。 這可讓圖形提示資料，以便在呼叫 **Run** 時立即開始播放 (請參閱 [篩選狀態](filter-states.md)) 。 如果您的篩選準則不會在暫停時傳遞資料，則篩選的 **IMediaFilter：： >getstate** 方法應該會傳回 VFW \_ s，而無法 \_ \_ 提示處於暫停狀態。 此傳回碼表示篩選圖形不會在完成暫停轉換之前等候篩選圖形中的資料。 否則， **Pause** 方法將會無限期地封鎖。 如需範例程式碼，請參閱 [**CBaseFilter：： >getstate**](cbasefilter-getstate.md)。

以下是當篩選準則可能需要傳回 VFW 時無法提供提示的一些範例 \_ \_ \_ ：

-   即時來源（例如「捕捉」篩選）不應在暫停時傳送資料。 請參閱 [在 Capture 篩選器中產生資料](producing-data-in-a-capture-filter.md)。
-   分隔器篩選器可能會在暫停時傳送資料，視執行而定。 如果篩選使用不同的執行緒來將每個輸出釘選上的資料排入佇列，則它可以在暫停時傳送資料。 但是，如果篩選器針對每個輸出釘選使用單一執行緒，則第一個 pin 可能會在呼叫 **Receive** 時封鎖執行緒，這會防止其他 pin 傳送資料。 在這種情況下，您應該會傳回 VFW \_ S 無法 \_ \_ 提示。
-   篩選可能會偶爾傳遞資料。 例如，它可能會剖析自訂資料流程，並在提供其他封包時進行篩選。 在此情況下，篩選可能無法保證在暫停時傳遞資料。

使用推送模型) 的來源篩選 (，或使用推送/提取模型 (的剖析器篩選，) 建立一或多個串流執行緒，以儘快傳遞範例。 下游篩選器（例如，「解碼器」和「轉換」）通常只會在其輸入 pin 上呼叫 **Receive** 時傳送資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[接收和傳遞範例](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



