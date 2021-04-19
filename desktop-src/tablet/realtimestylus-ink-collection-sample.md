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
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="83e0a-103">RealTimeStylus 筆墨集合範例</span><span class="sxs-lookup"><span data-stu-id="83e0a-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="83e0a-104">使用 [**RealTimeStylus**](realtimestylus-class.md) 類別時，此應用程式會示範筆墨收集和轉譯。</span><span class="sxs-lookup"><span data-stu-id="83e0a-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="83e0a-105">InkCollection 專案</span><span class="sxs-lookup"><span data-stu-id="83e0a-105">The InkCollection Project</span></span>

<span data-ttu-id="83e0a-106">此範例包含單一方案，其中包含一個專案 InkCollection。</span><span class="sxs-lookup"><span data-stu-id="83e0a-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="83e0a-107">應用程式會定義 `InkCollection` 包含單一類別（也稱為）的命名空間 `InkCollection` 。</span><span class="sxs-lookup"><span data-stu-id="83e0a-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="83e0a-108">類別繼承自 [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) 類別，並會執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面。</span><span class="sxs-lookup"><span data-stu-id="83e0a-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="83e0a-109">InkCollection 類別會定義一組用來指定各種筆墨粗細的私用常數。</span><span class="sxs-lookup"><span data-stu-id="83e0a-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="83e0a-110">類別也會宣告 [**RealTimeStylus**](realtimestylus-class.md)類別、 `myRealTimeStylus` 、 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))類別、和轉譯器類別的私用實例 `myDynamicRenderer` [](/previous-versions/ms828481(v=msdn.10)) `myRenderer` 。</span><span class="sxs-lookup"><span data-stu-id="83e0a-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="83e0a-111">**DynamicRenderer** 會呈現目前正在收集的 [筆劃](/previous-versions/ms552692(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="83e0a-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="83e0a-112">轉譯器物件會 `myRenderer` 呈現已收集的筆觸物件。</span><span class="sxs-lookup"><span data-stu-id="83e0a-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="83e0a-113">類別也會宣告 [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) 物件， `myPackets` 此物件是用來儲存由一個或多個資料 [指標](/previous-versions/ms552104(v=vs.100)) 物件所收集的封包資料。</span><span class="sxs-lookup"><span data-stu-id="83e0a-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="83e0a-114">[手寫筆](/previous-versions/ms824824(v=msdn.10))物件的[識別碼](/previous-versions/ms824826(v=msdn.10))值會用來做為雜湊表索引鍵，以便唯一識別針對指定的資料指標物件所收集的封包資料。</span><span class="sxs-lookup"><span data-stu-id="83e0a-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="83e0a-115">[筆墨](/previous-versions/aa515768(v=msdn.10))物件的私用實例，會 `myInk` 儲存所收集的[筆觸](/previous-versions/ms552692(v=vs.100))物件 `myRealTimeStylus` 。</span><span class="sxs-lookup"><span data-stu-id="83e0a-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="83e0a-116">表單載入事件</span><span class="sxs-lookup"><span data-stu-id="83e0a-116">The Form Load Event</span></span>

<span data-ttu-id="83e0a-117">在表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中， `myDynamicRenderer` 會使用接受控制項做為引數的 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 來具現化，並使用無引數的函 `myRenderer` 式來建立。</span><span class="sxs-lookup"><span data-stu-id="83e0a-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="83e0a-118">請注意轉譯器具現化之後的批註，因為在轉譯 `myDynamicRenderer` 筆墨時，會使用 [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) 的預設值。</span><span class="sxs-lookup"><span data-stu-id="83e0a-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="83e0a-119">這是標準行為。</span><span class="sxs-lookup"><span data-stu-id="83e0a-119">This is standard behavior.</span></span> <span data-ttu-id="83e0a-120">但是，如果您想要提供由所 `myDynamicRenderer` 呈現筆墨的不同外觀所呈現的筆墨 `myRenderer` ，您可以變更的 [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) 屬性 `myDynamicRenderer` 。</span><span class="sxs-lookup"><span data-stu-id="83e0a-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="83e0a-121">若要這樣做，請在建立並執行應用程式之前，先將下列幾行取消批註。</span><span class="sxs-lookup"><span data-stu-id="83e0a-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="83e0a-122">接下來，應用程式會建立用來接收手寫筆通知的 [**RealTimeStylus**](realtimestylus-class.md) 物件，並將 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件新增至同步外掛程式通知佇列。</span><span class="sxs-lookup"><span data-stu-id="83e0a-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="83e0a-123">具體而言，會 `myRealTimeStylus` 將加入 `myDynamicRenderer` 至 [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) 屬性。</span><span class="sxs-lookup"><span data-stu-id="83e0a-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="83e0a-124">然後，會將表單新增至非同步外掛程式通知佇列。</span><span class="sxs-lookup"><span data-stu-id="83e0a-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="83e0a-125">具體而言， `InkCollection` 會加入至 [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) 屬性。</span><span class="sxs-lookup"><span data-stu-id="83e0a-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="83e0a-126">最後， `myRealTimeStylus` 和已 `myDynamicRenderer` 啟用，且 MyPackets 和 myInk 會具現化。</span><span class="sxs-lookup"><span data-stu-id="83e0a-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="83e0a-127">除了連結功能表處理常式來變更筆墨色彩和大小之外，還需要一個簡單的程式碼區塊，才能執行介面。</span><span class="sxs-lookup"><span data-stu-id="83e0a-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="83e0a-128">範例必須處理表單的 [繪製](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) 事件。</span><span class="sxs-lookup"><span data-stu-id="83e0a-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="83e0a-129">在事件處理常式中，應用程式必須重新整理， `myDynamicRenderer` 因為可能會在繪製事件發生時收集 [筆觸](/previous-versions/ms552692(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="83e0a-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="83e0a-130">在此情況下，必須重新繪製已收集之筆劃物件的部分。</span><span class="sxs-lookup"><span data-stu-id="83e0a-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="83e0a-131">[靜態轉譯](/previous-versions/ms828481(v=msdn.10))器用來重新繪製已收集的筆觸物件。</span><span class="sxs-lookup"><span data-stu-id="83e0a-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="83e0a-132">這些筆觸是在 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件中，因為它們會在繪製時放置於其中，如下一節所示。</span><span class="sxs-lookup"><span data-stu-id="83e0a-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="83e0a-133">執行 IStylusAsyncPlugin 介面</span><span class="sxs-lookup"><span data-stu-id="83e0a-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="83e0a-134">範例應用程式會定義它在 [DataInterest](/previous-versions/ms824769(v=msdn.10)) 屬性的執行中所感興趣的通知類型。</span><span class="sxs-lookup"><span data-stu-id="83e0a-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="83e0a-135">因此，DataInterest 屬性會定義要將 [**RealTimeStylus**](realtimestylus-class.md) 物件轉送至表單的通知。</span><span class="sxs-lookup"><span data-stu-id="83e0a-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="83e0a-136">在此範例中，DataInterest 屬性會透過 [DataInterestMask](/previous-versions/ms824787(v=msdn.10))列舉來定義 **StylusDown**、封 **包**、 **StylusUp** 和 **錯誤** 通知中的興趣。</span><span class="sxs-lookup"><span data-stu-id="83e0a-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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



<span data-ttu-id="83e0a-137">當畫筆觸及數位化板介面時，就會發生 [StylusDown](/previous-versions/ms824779(v=msdn.10)) 通知。</span><span class="sxs-lookup"><span data-stu-id="83e0a-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="83e0a-138">當發生這種情況時，範例會配置用來儲存 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件之封包資料的陣列。</span><span class="sxs-lookup"><span data-stu-id="83e0a-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="83e0a-139">StylusDown 方法中的 [StylusDownData](/previous-versions/ms824107(v=msdn.10)) 會加入至陣列，並使用手寫筆物件的 [Id](/previous-versions/ms824826(v=msdn.10)) 屬性作為索引鍵，將陣列插入雜湊表中。</span><span class="sxs-lookup"><span data-stu-id="83e0a-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="83e0a-140">當畫筆在數位板上移動時，就會發生封 [包](/previous-versions/ms824773(v=msdn.10)) 通知。</span><span class="sxs-lookup"><span data-stu-id="83e0a-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="83e0a-141">發生這種情況時，應用程式會將新的 [StylusDownData](/previous-versions/ms824107(v=msdn.10)) 加入至 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件的封包陣列中。</span><span class="sxs-lookup"><span data-stu-id="83e0a-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="83e0a-142">它會使用手寫筆物件的 [Id](/previous-versions/ms824826(v=msdn.10)) 屬性做為索引鍵，從 hashtable 取出手寫筆的封包陣列。</span><span class="sxs-lookup"><span data-stu-id="83e0a-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="83e0a-143">新的封包資料接著會插入到已抓取的陣列中。</span><span class="sxs-lookup"><span data-stu-id="83e0a-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="83e0a-144">當畫筆離開數位化板介面時，就會發生 [StylusUp](/previous-versions/ms824782(v=msdn.10)) 通知。</span><span class="sxs-lookup"><span data-stu-id="83e0a-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="83e0a-145">當發生此通知時，此範例會從雜湊表中取出此 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件的封包陣列-從雜湊表中移除它，因為不再需要它，會加入新的封包資料，並使用封包資料的陣列來建立新的 [Stroke](/previous-versions/ms552692(v=vs.100)) 物件 `stroke` 。</span><span class="sxs-lookup"><span data-stu-id="83e0a-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


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



<span data-ttu-id="83e0a-146">如需更健全地使用 [**realtimestylus**](realtimestylus-class.md) 類別的範例，包括使用自訂外掛程式建立，請參閱 [realtimestylus 外掛程式範例](realtimestylus-plug-in-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="83e0a-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83e0a-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="83e0a-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="83e0a-148">[Microsoft Ink 轉譯器](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="83e0a-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="83e0a-149">[StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="83e0a-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="83e0a-150">[StylusInput](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="83e0a-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="83e0a-151">[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="83e0a-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="83e0a-152">存取和操作手寫筆輸入</span><span class="sxs-lookup"><span data-stu-id="83e0a-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
