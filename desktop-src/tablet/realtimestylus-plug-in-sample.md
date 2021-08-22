---
description: 此應用程式示範如何使用 RealTimeStylus 類別。
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: RealTimeStylus 外掛程式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a05fd9c70c11130011352d8c16d30abee672e4cd56c000c21b7fbfd2704babe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966877"
---
# <a name="realtimestylus-plug-in-sample"></a>RealTimeStylus 外掛程式範例

此應用程式示範如何使用 [**RealTimeStylus**](realtimestylus-class.md) 類別。 如需 StylusInput Api （包括 **RealTimeStylus** 類別）的詳細總覽，請參閱 [存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)。 如需同步與非同步外掛程式的詳細資訊，請參閱 [外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)。

## <a name="overview-of-the-sample"></a>範例總覽

外掛程式，可將實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的物件加入至 [**RealTimeStylus**](realtimestylus-class.md) 物件。 這個範例應用程式會使用數種類型的外掛程式：

-   封包篩選外掛程式：修改封包。 此範例中的封包篩選外掛程式會限制矩形區域內的所有 (x，y) 封包資料，以修改封包資訊。
-   自訂動態轉譯器外掛程式：修改動態轉譯品質。 此範例中的自訂動態轉譯外掛程式會以筆劃上的每個 (x，y) 點為中心繪製一個小圓圈，以修改筆墨的呈現方式。
-   動態轉譯器外掛程式：修改動態轉譯品質。 這個範例示範如何使用 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件做為外掛程式，以處理筆墨的動態呈現。
-   手勢辨識器外掛程式：辨識應用程式手勢。 此範例示範如何使用 [**GestureRecognizer**](gesturerecognizer-class.md) 物件做為外掛程式，以辨識應用程式手勢 (在具有 Microsoft 手勢辨識器的系統上執行時) 。

此外，這個範例也提供使用者介面，讓使用者可以加入、移除和變更集合中每個外掛程式的順序。 範例方案包含兩個專案： RealTimeStylusPluginApp 和 RealTimeStylusPlugins。 RealTimeStylusPluginApp 包含此範例的使用者介面。 RealTimeStylusPlugins 包含外掛程式的執行。RealTimeStylusPlugins 專案會定義 RealTimeStylusPlugins 命名空間，其中包含封包篩選器和自訂動態轉譯器外掛程式。RealTimeStylusPluginApp 專案會參考此命名空間。 RealTimeStylusPlugins 專案會使用[StylusInput](/previous-versions/ms824750(v=msdn.10)) [，以及](/previous-versions/ms826516(v=msdn.10)) [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))命名空間。

如需 [StylusInput](/previous-versions/ms824750(v=msdn.10)) 和 [StylusInput PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間的總覽，請參閱 [StylusInput api 的架構](architecture-of-the-stylusinput-apis.md)。

## <a name="packet-filter-plug-in"></a>封包篩選外掛程式

封包篩選外掛程式是可示範封包修改的同步外掛程式。 具體而言，它會在表單上定義矩形。 在區域外部繪製的任何封包都會在區域內轉譯。 外掛程式類別會 `PacketFilterPlugin` 註冊 `StylusDown` 、 `StylusUp` 和 `Packets` 畫筆輸入事件的通知。 類別會實 [StylusDown](/previous-versions/ms824761(v=msdn.10))、 [StylusUp](/previous-versions/ms824764(v=msdn.10))和 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)類別上定義的封 [包](/previous-versions/ms824756(v=msdn.10))方法。

的公用函式 `PacketFilterPlugin` 需要 [矩形](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) 結構。 這個矩形會定義以筆墨空間座標 ( 的矩形區域。 01mm = 1 HIMETRIC unit) ，其中包含封包。 矩形會保留在私用欄位中 `rectangle` 。


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



`PacketFilterPlugin`類別會針對[DataInterest](/previous-versions/ms824752(v=msdn.10))屬性執行 get 存取子，以註冊事件通知。 在此情況下，外掛程式有興趣回應 `StylusDown` 、 `Packets` 、 `StylusUp` 和 `Error` 通知。 此範例會傳回這些值，如 [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) 列舉中所定義。 當畫筆提示聯絡數位板介面時，就會呼叫 [StylusDown](/previous-versions/ms824761(v=msdn.10)) 方法。 當畫筆提示離開數位化板介面時，就會呼叫 [StylusUp](/previous-versions/ms824764(v=msdn.10)) 方法。 當 [**RealTimeStylus**](realtimestylus-class.md)物件接收封包時，會呼叫封 [包](/previous-versions/ms824756(v=msdn.10))方法。 當目前的外掛程式或先前的外掛程式擲回例外狀況時，就會呼叫 [Error](/previous-versions/ms585069(v=vs.100)) 方法。


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



`PacketFilterPlugin`類別會在 helper 方法中處理大部分的通知 `ModifyPacketData` 。 `ModifyPacketData`方法會從[PacketsData](/previous-versions/ms824590(v=msdn.10))類別取得每個新封包的 x 和 y 值。 如果任一個值在矩形外，此方法就會以仍落在矩形內的最接近點來取代該值。 這是一個範例，說明外掛程式如何取代從畫筆輸入資料流程收到的封包資料。


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a>自訂動態轉譯器外掛程式

`CustomDynamicRenderer`類別也會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)類別來接收畫筆輸入通知。 然後，它會處理 `Packets` 通知，以在每個新的封包點周圍繪製一個小圓圈。

類別包含的 [圖形](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) 變數，會保存傳遞至類別的函式之繪圖物件的參考。 這是用於動態呈現的繪圖物件。


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



當自訂動態轉譯器外掛程式收到封包通知時，它會將 (x，y) 資料解壓縮，並在該點周圍繪製一個小綠色圓圈。 這是根據畫筆輸入資料流程的自訂呈現範例。


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a>RealTimeStylusPluginApp Project

RealTimeStylusPluginApp 專案會示範先前所述的外掛程式，以及 [**GestureRecognizer**](gesturerecognizer-class.md) 和 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 外掛程式。專案的使用者介面包含：

-   包含用來定義筆跡輸入區域之 [分組](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) 控制項的表單。
-   [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1)控制項，可列出並選取可用的外掛程式。
-   一組 [按鈕物件](/dotnet/api/system.windows.forms.button?view=netcore-3.1) ，可讓您重新排列外掛程式的順序。

專案會定義結構， `PlugInListItem` 讓您更輕鬆地管理專案中使用的外掛程式。 `PlugInListItem`結構包含外掛程式和描述。

`RealTimeStylusPluginApp`類別本身會實 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)類別。 這是必要的，如此一來， `RealTimeStylusPluginApp` 當 [**GestureRecognizer**](gesturerecognizer-class.md) 外掛程式將手勢資料新增至輸出佇列時，就可以通知類別。 應用程式會註冊 [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))的通知。 收到手勢資料時，會將 `RealTimeStylusPluginApp` 其描述放在表單底部的狀態列上。


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> 在 [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) 的執行中，您可以使用 [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) 欄位) ，或使用 as 語句) 的結果 (型別，在輸出 (佇列中識別自訂筆勢資料。 此範例會使用這兩種識別技術進行示範。 這兩種方法本身也有效。

 

在表單的 Load 事件處理常式中，應用程式會建立 `PacketFilter` 和類別的實例， `CustomDynamicRenderer` 並將它們加入清單方塊中。 然後，應用程式會嘗試建立 [**GestureRecognizer**](gesturerecognizer-class.md) 類別的實例，如果成功，則會將它加入清單方塊中。 如果系統上沒有筆勢辨識器，就會失敗。 接下來，應用程式會具現化 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件，並將它加入清單方塊中。 最後，應用程式會啟用每一項外掛程式和 [**RealTimeStylus**](realtimestylus-class.md) 物件本身。

關於此範例的另一個重要事項是在 helper 方法中，在新增或移除外掛程式之前，會先停用 [**RealTimeStylus**](realtimestylus-class.md) 物件，然後在新增或移除完成後重新啟用。


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[StylusInput](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[RealTimeStylus 筆墨集合範例](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
