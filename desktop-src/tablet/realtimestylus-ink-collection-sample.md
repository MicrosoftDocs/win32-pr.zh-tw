---
description: 使用 RealTimeStylus 類別時，此應用程式會示範筆墨收集和轉譯。
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: RealTimeStylus 筆墨集合範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975385"
---
# <a name="realtimestylus-ink-collection-sample"></a>RealTimeStylus 筆墨集合範例

使用 [**RealTimeStylus**](realtimestylus-class.md) 類別時，此應用程式會示範筆墨收集和轉譯。

## <a name="the-inkcollection-project"></a>InkCollection 專案

此範例包含單一方案，其中包含一個專案 InkCollection。 應用程式會定義 `InkCollection` 包含單一類別（也稱為）的命名空間 `InkCollection` 。 類別繼承自 [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) 類別，並會執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面。


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



InkCollection 類別會定義一組用來指定各種筆墨粗細的私用常數。 類別也會宣告 [**RealTimeStylus**](realtimestylus-class.md)類別、 `myRealTimeStylus` 、 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))類別、和轉譯器類別的私用實例 `myDynamicRenderer` [](/previous-versions/ms828481(v=msdn.10)) `myRenderer` 。 **DynamicRenderer** 會呈現目前正在收集的 [筆劃](/previous-versions/ms552692(v=vs.100))。 轉譯器物件會 `myRenderer` 呈現已收集的筆觸物件。


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



類別也會宣告 [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) 物件， `myPackets` 此物件是用來儲存由一個或多個資料 [指標](/previous-versions/ms552104(v=vs.100)) 物件所收集的封包資料。 [手寫筆](/previous-versions/ms824824(v=msdn.10))物件的[識別碼](/previous-versions/ms824826(v=msdn.10))值會用來做為雜湊表索引鍵，以便唯一識別針對指定的資料指標物件所收集的封包資料。

[筆墨](/previous-versions/aa515768(v=msdn.10))物件的私用實例，會 `myInk` 儲存所收集的[筆觸](/previous-versions/ms552692(v=vs.100))物件 `myRealTimeStylus` 。


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>表單載入事件

在表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中， `myDynamicRenderer` 會使用接受控制項做為引數的 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 來具現化，並使用無引數的函 `myRenderer` 式來建立。


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



請注意轉譯器具現化之後的批註，因為在轉譯 `myDynamicRenderer` 筆墨時，會使用 [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) 的預設值。 這是標準行為。 但是，如果您想要提供由所 `myDynamicRenderer` 呈現筆墨的不同外觀所呈現的筆墨 `myRenderer` ，您可以變更的 [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) 屬性 `myDynamicRenderer` 。 若要這樣做，請在建立並執行應用程式之前，先將下列幾行取消批註。


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



接下來，應用程式會建立用來接收手寫筆通知的 [**RealTimeStylus**](realtimestylus-class.md) 物件，並將 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件新增至同步外掛程式通知佇列。 具體而言，會 `myRealTimeStylus` 將加入 `myDynamicRenderer` 至 [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) 屬性。


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



然後，會將表單新增至非同步外掛程式通知佇列。 具體而言， `InkCollection` 會加入至 [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) 屬性。 最後， `myRealTimeStylus` 和已 `myDynamicRenderer` 啟用，且 MyPackets 和 myInk 會具現化。


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



除了連結功能表處理常式來變更筆墨色彩和大小之外，還需要一個簡單的程式碼區塊，才能執行介面。 範例必須處理表單的 [繪製](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) 事件。 在事件處理常式中，應用程式必須重新整理， `myDynamicRenderer` 因為可能會在繪製事件發生時收集 [筆觸](/previous-versions/ms552692(v=vs.100)) 物件。 在此情況下，必須重新繪製已收集之筆劃物件的部分。 [靜態轉譯](/previous-versions/ms828481(v=msdn.10))器用來重新繪製已收集的筆觸物件。 這些筆觸是在 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件中，因為它們會在繪製時放置於其中，如下一節所示。


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>執行 IStylusAsyncPlugin 介面

範例應用程式會定義它在 [DataInterest](/previous-versions/ms824769(v=msdn.10)) 屬性的執行中所感興趣的通知類型。 因此，DataInterest 屬性會定義要將 [**RealTimeStylus**](realtimestylus-class.md) 物件轉送至表單的通知。 在此範例中，DataInterest 屬性會透過 [DataInterestMask](/previous-versions/ms824787(v=msdn.10))列舉來定義 **StylusDown**、封 **包**、 **StylusUp** 和 **錯誤** 通知中的興趣。


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
```



當畫筆觸及數位化板介面時，就會發生 [StylusDown](/previous-versions/ms824779(v=msdn.10)) 通知。 當發生這種情況時，範例會配置用來儲存 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件之封包資料的陣列。 StylusDown 方法中的 [StylusDownData](/previous-versions/ms824107(v=msdn.10)) 會加入至陣列，並使用手寫筆物件的 [Id](/previous-versions/ms824826(v=msdn.10)) 屬性作為索引鍵，將陣列插入雜湊表中。


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



當畫筆在數位板上移動時，就會發生封 [包](/previous-versions/ms824773(v=msdn.10)) 通知。 發生這種情況時，應用程式會將新的 [StylusDownData](/previous-versions/ms824107(v=msdn.10)) 加入至 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件的封包陣列中。 它會使用手寫筆物件的 [Id](/previous-versions/ms824826(v=msdn.10)) 屬性做為索引鍵，從 hashtable 取出手寫筆的封包陣列。 新的封包資料接著會插入到已抓取的陣列中。


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



當畫筆離開數位化板介面時，就會發生 [StylusUp](/previous-versions/ms824782(v=msdn.10)) 通知。 當發生此通知時，此範例會從雜湊表中取出此 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件的封包陣列-從雜湊表中移除它，因為不再需要它，會加入新的封包資料，並使用封包資料的陣列來建立新的 [Stroke](/previous-versions/ms552692(v=vs.100)) 物件 `stroke` 。


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



如需更健全地使用 [**realtimestylus**](realtimestylus-class.md) 類別的範例，包括使用自訂外掛程式建立，請參閱 [realtimestylus 外掛程式範例](realtimestylus-plug-in-sample.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft Ink 轉譯器](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[StylusInput](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
