---
description: 串流和應用程式執行緒
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: 串流和應用程式執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432e613ff0322377c042e796d84ef7affdda99c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514157"
---
# <a name="the-streaming-and-application-threads"></a>串流和應用程式執行緒

任何 DirectShow 應用程式都包含至少兩個重要的執行緒：應用程式執行緒，以及一或多個串流執行緒。 範例會在串流處理執行緒上傳遞，並在應用程式執行緒上發生狀態變更。 主要串流執行緒是由來源或剖析器篩選器所建立。 其他篩選器可能會建立傳遞範例的背景工作執行緒，而這些執行緒也會被視為串流執行緒。

某些方法會在應用程式執行緒上呼叫，而其他方法則是在串流執行緒上呼叫。 例如：

-   串流執行緒 (s) ： [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)、 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)、 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)、 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)。
-   應用程式執行緒： [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)、 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)、 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)、 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)、 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)、 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)。
-   可能是： [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)。

擁有個別的串流執行緒可讓資料在應用程式執行緒等候使用者輸入時流經圖形。 不過，多個執行緒的風險是，當篩選暫停應用程式執行緒上的 (時，可能會建立資源) 、在串流方法內使用它們，並在停止 (應用程式執行緒) 時終結它們。 如果您不小心，串流執行緒可能會在終結之後嘗試使用這些資源。 解決方法是使用重要區段來保護資源，並同步處理具有狀態變更的串流方法。

篩選準則需要一個重要區段來保護篩選狀態。 [**CBaseFilter**](cbasefilter.md)類別具有這個重要區段的成員變數， [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)。 此重要區段稱為篩選鎖定。 此外，每個輸入 pin 都需要重要的區段，以保護串流執行緒所使用的資源。 這些重要區段稱為串流鎖定;您必須在衍生的 pin 類別中宣告它們。 最簡單的方法是使用 [**CCritSec**](ccritsec.md) 類別，此類別會包裝 Windows **重要 \_ 區段** 物件，並可使用 [**CAutoLock**](cautolock.md) 類別來鎖定。 **CCritSec** 類別也會提供一些實用的調試函數。 如需詳細資訊，請參閱 [重要區段的調試](critical-section-debugging-functions.md)程式。

當篩選準則停止或清除時，它必須與串流執行緒同步處理應用程式執行緒。 為了避免死結，它必須先解除封鎖串流執行緒，這可能是因為下列幾個原因所造成：

-   它正在等候取得 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法內的範例，因為配置器的所有範例都在使用中。
-   正在等候另一個篩選器從串流方法傳回，例如 **Receive**。
-   它正在等候其中一個串流方法，讓某些資源變成可用。
-   它是等候下一個範例呈現時間的轉譯器篩選器
-   它是在暫停時，于 **接收** 方法內等候的轉譯器篩選準則。

因此，當篩選準則停止或排清時，必須執行下列動作：

-   釋放任何因任何原因而保留的範例。 這樣做會解除封鎖 **GetBuffer** 方法。
-   儘快從任何串流方法返回。 如果串流方法正在等候資源，它必須立即停止等候。
-   開始拒絕 **接收** 中的範例，讓串流執行緒不會存取其他資源。  ([**CBaseInputPin**](cbaseinputpin.md) 類別會自動處理這種情況。 ) 
-   **Stop** 方法必須取消認可所有篩選準則的配置器。  (**CBaseInputPin** 類別會自動處理這種情況。 ) 

清除和停止兩者都會在應用程式執行緒上發生。 篩選準則會停止，以回應 [**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) 方法。 篩選圖形管理員會以上游順序發出 stop 命令，從轉譯器開始，然後回溯至來源篩選器。 Stop 命令會完全在篩選器的 **CBaseFilter：： stop** 方法內執行。 當方法傳回時，篩選準則應該會處於已停止狀態。

通常會因為搜尋命令而發生排清。 Flush 命令會從來源或剖析器篩選開始，然後傳輸下游。 清除會以兩個階段進行： [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法會通知篩選器捨棄所有暫止和傳入的資料; [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法表示篩選準則會再次接受資料。 排清需要兩個階段，因為 **BeginFlush** 呼叫是在應用程式執行緒上，在這段期間，串流執行緒會繼續傳遞資料。 因此，某些範例可能會在 **BeginFlush** 呼叫之後抵達。 篩選應捨棄這些。 在 **EndFlush** 呼叫之後抵達的任何範例保證都是新的，而且應該傳遞。

接下來的章節包含程式碼範例，示範如何以避免鎖死和競爭條件的方式來執行最重要的篩選方法，例如 **暫停**、 **接收** 等等。 不過，每個篩選準則都有不同的需求，因此您必須將這些範例調整成特定的篩選準則。

> [!Note]  
> [**CTransformFilter**](ctransformfilter.md)和 [**CTransInPlaceFilter**](ctransinplacefilter.md)基類會處理本文中所述的許多問題。 如果您要撰寫轉換篩選，而且您的篩選不會等候串流方法內的事件，或在 **接收** 之外保留樣本，則這些基類應該就已足夠。

 

 

 



