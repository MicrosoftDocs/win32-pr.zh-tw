---
description: 此應用程式示範如何使用 RealTimeStylus 類別。
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: RealTimeStylus 外掛程式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195319"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="e32b8-103">RealTimeStylus 外掛程式範例</span><span class="sxs-lookup"><span data-stu-id="e32b8-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="e32b8-104">此應用程式示範如何使用 [**RealTimeStylus**](realtimestylus-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="e32b8-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="e32b8-105">如需 StylusInput Api （包括 **RealTimeStylus** 類別）的詳細總覽，請參閱 [存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)。</span><span class="sxs-lookup"><span data-stu-id="e32b8-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="e32b8-106">如需同步與非同步外掛程式的詳細資訊，請參閱 [外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)。</span><span class="sxs-lookup"><span data-stu-id="e32b8-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="e32b8-107">範例總覽</span><span class="sxs-lookup"><span data-stu-id="e32b8-107">Overview of the Sample</span></span>

<span data-ttu-id="e32b8-108">外掛程式，可將實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的物件加入至 [**RealTimeStylus**](realtimestylus-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e32b8-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="e32b8-109">這個範例應用程式會使用數種類型的外掛程式：</span><span class="sxs-lookup"><span data-stu-id="e32b8-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="e32b8-110">封包篩選外掛程式：修改封包。</span><span class="sxs-lookup"><span data-stu-id="e32b8-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="e32b8-111">此範例中的封包篩選外掛程式會限制矩形區域內的所有 (x，y) 封包資料，以修改封包資訊。</span><span class="sxs-lookup"><span data-stu-id="e32b8-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="e32b8-112">自訂動態轉譯器外掛程式：修改動態轉譯品質。</span><span class="sxs-lookup"><span data-stu-id="e32b8-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="e32b8-113">此範例中的自訂動態轉譯外掛程式會以筆劃上的每個 (x，y) 點為中心繪製一個小圓圈，以修改筆墨的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="e32b8-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="e32b8-114">動態轉譯器外掛程式：修改動態轉譯品質。</span><span class="sxs-lookup"><span data-stu-id="e32b8-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="e32b8-115">這個範例示範如何使用 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件做為外掛程式，以處理筆墨的動態呈現。</span><span class="sxs-lookup"><span data-stu-id="e32b8-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="e32b8-116">手勢辨識器外掛程式：辨識應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="e32b8-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="e32b8-117">此範例示範如何使用 [**GestureRecognizer**](gesturerecognizer-class.md) 物件做為外掛程式，以辨識應用程式手勢 (在具有 Microsoft 手勢辨識器的系統上執行時) 。</span><span class="sxs-lookup"><span data-stu-id="e32b8-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="e32b8-118">此外，這個範例也提供使用者介面，讓使用者可以加入、移除和變更集合中每個外掛程式的順序。</span><span class="sxs-lookup"><span data-stu-id="e32b8-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="e32b8-119">範例方案包含兩個專案： RealTimeStylusPluginApp 和 RealTimeStylusPlugins。</span><span class="sxs-lookup"><span data-stu-id="e32b8-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="e32b8-120">RealTimeStylusPluginApp 包含此範例的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e32b8-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="e32b8-121">RealTimeStylusPlugins 包含外掛程式的執行。RealTimeStylusPlugins 專案會定義 RealTimeStylusPlugins 命名空間，其中包含封包篩選器和自訂動態轉譯器外掛程式。RealTimeStylusPluginApp 專案會參考此命名空間。</span><span class="sxs-lookup"><span data-stu-id="e32b8-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="e32b8-122">RealTimeStylusPlugins 專案會使用[StylusInput](/previous-versions/ms824750(v=msdn.10)) [，以及](/previous-versions/ms826516(v=msdn.10)) [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))命名空間。</span><span class="sxs-lookup"><span data-stu-id="e32b8-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="e32b8-123">如需 [StylusInput](/previous-versions/ms824750(v=msdn.10)) 和 [StylusInput PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間的總覽，請參閱 [StylusInput api 的架構](architecture-of-the-stylusinput-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="e32b8-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="e32b8-124">封包篩選外掛程式</span><span class="sxs-lookup"><span data-stu-id="e32b8-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="e32b8-125">封包篩選外掛程式是可示範封包修改的同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e32b8-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="e32b8-126">具體而言，它會在表單上定義矩形。</span><span class="sxs-lookup"><span data-stu-id="e32b8-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="e32b8-127">在區域外部繪製的任何封包都會在區域內轉譯。</span><span class="sxs-lookup"><span data-stu-id="e32b8-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="e32b8-128">外掛程式類別會 `PacketFilterPlugin` 註冊 `StylusDown` 、 `StylusUp` 和 `Packets` 畫筆輸入事件的通知。</span><span class="sxs-lookup"><span data-stu-id="e32b8-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="e32b8-129">類別會實 [StylusDown](/previous-versions/ms824761(v=msdn.10))、 [StylusUp](/previous-versions/ms824764(v=msdn.10))和 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)類別上定義的封 [包](/previous-versions/ms824756(v=msdn.10))方法。</span><span class="sxs-lookup"><span data-stu-id="e32b8-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="e32b8-130">的公用函式 `PacketFilterPlugin` 需要 [矩形](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) 結構。</span><span class="sxs-lookup"><span data-stu-id="e32b8-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="e32b8-131">這個矩形會定義以筆墨空間座標 ( 的矩形區域。 01mm = 1 HIMETRIC unit) ，其中包含封包。</span><span class="sxs-lookup"><span data-stu-id="e32b8-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="e32b8-132">矩形會保留在私用欄位中 `rectangle` 。</span><span class="sxs-lookup"><span data-stu-id="e32b8-132">The rectangle is held in a private field, `rectangle`.</span></span>


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



<span data-ttu-id="e32b8-133">`PacketFilterPlugin`類別會針對[DataInterest](/previous-versions/ms824752(v=msdn.10))屬性執行 get 存取子，以註冊事件通知。</span><span class="sxs-lookup"><span data-stu-id="e32b8-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="e32b8-134">在此情況下，外掛程式有興趣回應 `StylusDown` 、 `Packets` 、 `StylusUp` 和 `Error` 通知。</span><span class="sxs-lookup"><span data-stu-id="e32b8-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="e32b8-135">此範例會傳回這些值，如 [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) 列舉中所定義。</span><span class="sxs-lookup"><span data-stu-id="e32b8-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="e32b8-136">當畫筆提示聯絡數位板介面時，就會呼叫 [StylusDown](/previous-versions/ms824761(v=msdn.10)) 方法。</span><span class="sxs-lookup"><span data-stu-id="e32b8-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="e32b8-137">當畫筆提示離開數位化板介面時，就會呼叫 [StylusUp](/previous-versions/ms824764(v=msdn.10)) 方法。</span><span class="sxs-lookup"><span data-stu-id="e32b8-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="e32b8-138">當 [**RealTimeStylus**](realtimestylus-class.md)物件接收封包時，會呼叫封 [包](/previous-versions/ms824756(v=msdn.10))方法。</span><span class="sxs-lookup"><span data-stu-id="e32b8-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="e32b8-139">當目前的外掛程式或先前的外掛程式擲回例外狀況時，就會呼叫 [Error](/previous-versions/ms585069(v=vs.100)) 方法。</span><span class="sxs-lookup"><span data-stu-id="e32b8-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


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



<span data-ttu-id="e32b8-140">`PacketFilterPlugin`類別會在 helper 方法中處理大部分的通知 `ModifyPacketData` 。</span><span class="sxs-lookup"><span data-stu-id="e32b8-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="e32b8-141">`ModifyPacketData`方法會從[PacketsData](/previous-versions/ms824590(v=msdn.10))類別取得每個新封包的 x 和 y 值。</span><span class="sxs-lookup"><span data-stu-id="e32b8-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="e32b8-142">如果任一個值在矩形外，此方法就會以仍落在矩形內的最接近點來取代該值。</span><span class="sxs-lookup"><span data-stu-id="e32b8-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="e32b8-143">這是一個範例，說明外掛程式如何取代從畫筆輸入資料流程收到的封包資料。</span><span class="sxs-lookup"><span data-stu-id="e32b8-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


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



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="e32b8-144">自訂動態轉譯器外掛程式</span><span class="sxs-lookup"><span data-stu-id="e32b8-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="e32b8-145">`CustomDynamicRenderer`類別也會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)類別來接收畫筆輸入通知。</span><span class="sxs-lookup"><span data-stu-id="e32b8-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="e32b8-146">然後，它會處理 `Packets` 通知，以在每個新的封包點周圍繪製一個小圓圈。</span><span class="sxs-lookup"><span data-stu-id="e32b8-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="e32b8-147">類別包含的 [圖形](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) 變數，會保存傳遞至類別的函式之繪圖物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e32b8-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="e32b8-148">這是用於動態呈現的繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="e32b8-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="e32b8-149">當自訂動態轉譯器外掛程式收到封包通知時，它會將 (x，y) 資料解壓縮，並在該點周圍繪製一個小綠色圓圈。</span><span class="sxs-lookup"><span data-stu-id="e32b8-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="e32b8-150">這是根據畫筆輸入資料流程的自訂呈現範例。</span><span class="sxs-lookup"><span data-stu-id="e32b8-150">This is an example of custom rendering based on the pen-input stream.</span></span>


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



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="e32b8-151">RealTimeStylusPluginApp 專案</span><span class="sxs-lookup"><span data-stu-id="e32b8-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="e32b8-152">RealTimeStylusPluginApp 專案會示範先前所述的外掛程式，以及 [**GestureRecognizer**](gesturerecognizer-class.md) 和 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 外掛程式。專案的使用者介面包含：</span><span class="sxs-lookup"><span data-stu-id="e32b8-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="e32b8-153">包含用來定義筆跡輸入區域之 [分組](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) 控制項的表單。</span><span class="sxs-lookup"><span data-stu-id="e32b8-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="e32b8-154">[CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1)控制項，可列出並選取可用的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e32b8-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="e32b8-155">一組 [按鈕物件](/dotnet/api/system.windows.forms.button?view=netcore-3.1) ，可讓您重新排列外掛程式的順序。</span><span class="sxs-lookup"><span data-stu-id="e32b8-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="e32b8-156">專案會定義結構， `PlugInListItem` 讓您更輕鬆地管理專案中使用的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e32b8-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="e32b8-157">`PlugInListItem`結構包含外掛程式和描述。</span><span class="sxs-lookup"><span data-stu-id="e32b8-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="e32b8-158">`RealTimeStylusPluginApp`類別本身會實 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)類別。</span><span class="sxs-lookup"><span data-stu-id="e32b8-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="e32b8-159">這是必要的，如此一來， `RealTimeStylusPluginApp` 當 [**GestureRecognizer**](gesturerecognizer-class.md) 外掛程式將手勢資料新增至輸出佇列時，就可以通知類別。</span><span class="sxs-lookup"><span data-stu-id="e32b8-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="e32b8-160">應用程式會註冊 [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))的通知。</span><span class="sxs-lookup"><span data-stu-id="e32b8-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="e32b8-161">收到手勢資料時，會將 `RealTimeStylusPluginApp` 其描述放在表單底部的狀態列上。</span><span class="sxs-lookup"><span data-stu-id="e32b8-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


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
> 在 [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) 的執行中，您可以使用 [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) 欄位) ，或使用 as 語句) 的結果 (型別，在輸出 (佇列中識別自訂筆勢資料。 此範例會使用這兩種識別技術進行示範。 <span data-ttu-id="e32b8-164">這兩種方法本身也有效。</span><span class="sxs-lookup"><span data-stu-id="e32b8-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="e32b8-165">在表單的 Load 事件處理常式中，應用程式會建立 `PacketFilter` 和類別的實例， `CustomDynamicRenderer` 並將它們加入清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="e32b8-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="e32b8-166">然後，應用程式會嘗試建立 [**GestureRecognizer**](gesturerecognizer-class.md) 類別的實例，如果成功，則會將它加入清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="e32b8-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="e32b8-167">如果系統上沒有筆勢辨識器，就會失敗。</span><span class="sxs-lookup"><span data-stu-id="e32b8-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="e32b8-168">接下來，應用程式會具現化 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件，並將它加入清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="e32b8-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="e32b8-169">最後，應用程式會啟用每一項外掛程式和 [**RealTimeStylus**](realtimestylus-class.md) 物件本身。</span><span class="sxs-lookup"><span data-stu-id="e32b8-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="e32b8-170">關於此範例的另一個重要事項是在 helper 方法中，在新增或移除外掛程式之前，會先停用 [**RealTimeStylus**](realtimestylus-class.md) 物件，然後在新增或移除完成後重新啟用。</span><span class="sxs-lookup"><span data-stu-id="e32b8-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e32b8-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="e32b8-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e32b8-172">[StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32b8-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-173">[StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e32b8-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-174">[StylusInput](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e32b8-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-175">[StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32b8-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-176">[StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e32b8-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-177">[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e32b8-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="e32b8-178">[StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32b8-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="e32b8-179">存取和操作手寫筆輸入</span><span class="sxs-lookup"><span data-stu-id="e32b8-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="e32b8-180">外掛程式和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="e32b8-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="e32b8-181">RealTimeStylus 筆墨集合範例</span><span class="sxs-lookup"><span data-stu-id="e32b8-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
