---
description: RealTimeStylus 物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: 外掛程式和 RealTimeStylus 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843378"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>外掛程式和 RealTimeStylus 類別

[**RealTimeStylus**](realtimestylus-class.md)物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。 外掛程式、可執行 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的物件，都可以新增至 **RealTimeStylus** 物件。 同步外掛程式通常會直接在高優先順序的執行緒上由 **RealTimeStylus** 物件呼叫，而非同步外掛程式通常會在應用程式的使用者介面上呼叫， (UI) 執行緒。 針對需要即時存取資料流程和 undemanding 的工作（例如封包篩選），建立或使用同步外掛程式。 針對不需要即時存取資料流程的工作建立或使用非同步外掛程式，例如筆墨收集。

某些工作可能會需要大量運算，但需要即時存取資料流程，例如 multistroke 手勢辨識。 為了滿足這些需求，StylusInput Api 提供了串聯的 [**realtimestylus**](realtimestylus-class.md) 模型，可讓您使用兩個 **realtimestylus** 物件，每個都在自己的執行緒上執行。 如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)和 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面都會定義相同的方法。 這些方法可讓 [**RealTimeStylus**](realtimestylus-class.md) 物件將畫筆資料傳遞至每個外掛程式，不論它是非同步或同步的外掛程式。 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10))和[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824769(v=msdn.10))屬性可讓每個外掛程式訂閱 tablet 畫筆資料流程中的特定資料。 外掛程式只應訂閱執行其工作所需的資料，將效能需求降至最低。 如需有關執行緒和 **RealTimeStylus** 類別的詳細資訊，請參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。

[**RealTimeStylus**](realtimestylus-class.md)物件會使用 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))命名空間中的物件，將畫筆資料傳遞給其外掛程式。**RealTimeStylus** 也會捕捉外掛程式擲回的例外狀況。當 **RealTimeStylus** 攔截到例外狀況時，它會呼叫 [IStylusSyncPlugin](/previous-versions/ms824754(v=msdn.10))或 [IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10))方法來通知外掛程式。 如需使用外掛程式資料的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) 類別。 如需有關錯誤處理的詳細資訊，請參閱 [StylusInput api 的錯誤處理考慮](error-handling-considerations-for-the-stylusinput-apis.md) 和外掛程式資料和 RealTimeStylus 類別的錯誤資料區段。

> [!Note]  
> 必須先將一個外掛程式附加到 [**realtimestylus**](realtimestylus-class.md) 物件，才能啟用 **realtimestylus** 物件。

 

下列主題將說明一些常見的外掛程式類別。

-   [筆墨-集合外掛程式](ink-collection-plug-ins.md)
-   [動態轉譯器外掛程式](dynamic-renderer-plug-ins.md)
-   [辨識器外掛程式](recognizer-plug-ins.md)

## <a name="special-considerations"></a>特殊考慮

因為 [**RealTimeStylus**](realtimestylus-class.md) 物件的複雜本質，所以您應該注意下列事項。

如果外掛程式修改附加的外掛程式集合，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會擲回例外狀況。 只有當外掛程式 **以該集合** 的成員身分呼叫它時，才會發生這種情況。

下列 C \# 範例是導致 [**RealTimeStylus**](realtimestylus-class.md) 物件擲回例外狀況的程式碼。


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



如果外掛程式呼叫 **RealTimeStylus** 物件的 [Dispose](/previous-versions/ms825891(v=msdn.10))方法，則 [**RealTimeStylus**](realtimestylus-class.md)物件會擲回例外狀況。 只有當外掛程式在由 **RealTimeStylus** 物件呼叫時，才會發生這種情況。

下列 C \# 範例是導致 [**RealTimeStylus**](realtimestylus-class.md) 物件擲回例外狀況的程式碼。


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時，可以修改外掛程式集合;不過，這可能會讓應用程式的行為難以預測。 當啟用了 **realtimestylus** 物件時，加入外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) 或 [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) 方法。 當啟用 **realtimestylus** 物件時移除外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) 或 [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) 方法。 這可讓外掛程式維持適當的狀態，而不需要檢查 **RealTimeStylus** 物件的 [Enabled](/previous-versions/ms824832(v=msdn.10))屬性。

當您在啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時加入外掛程式時，外掛程式所接收的外掛程式資料可能不會包含足夠的資訊，以充分建立初始資料的內容。 例如，新加入的外掛程式可能會開始從中間筆劃的畫筆接收封包資料。 同樣地，當啟用 **RealTimeStylus** 物件時移除外掛程式時，外掛程式所收到的外掛程式資料可能不足以完成處理資料。

> [!Note]  
> 若要取得整體穩定性，請在呼叫其 [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) 或 [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) 方法時重設外掛程式的內部狀態。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串聯的 RealTimeStylus 模型](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[StylusInput Api 的錯誤處理考慮](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
