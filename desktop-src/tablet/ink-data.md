---
description: 在收集筆墨之後，應用程式可以管理、操作及/或將該資料傳輸到其他媒體。
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: 筆墨資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de73291269398ae42a47ee26897c8da9bac8abe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511304"
---
# <a name="ink-data"></a><span data-ttu-id="944af-103">筆墨資料</span><span class="sxs-lookup"><span data-stu-id="944af-103">Ink Data</span></span>

<span data-ttu-id="944af-104">在收集筆墨之後，應用程式可以管理、操作及/或將該資料傳輸到其他媒體。</span><span class="sxs-lookup"><span data-stu-id="944af-104">After the ink is collected, applications can manage, manipulate, and/or transfer that data to other media.</span></span> <span data-ttu-id="944af-105">選取、複製、移動、儲存、觀看及變更筆墨的動作會在 [**筆跡**](inkdisp-class.md) 物件和其包含的成員上進行，例如 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合和 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。</span><span class="sxs-lookup"><span data-stu-id="944af-105">The actions of selecting, copying, moving, saving, viewing, and altering of the ink take place on the [**Ink**](inkdisp-class.md) object and its contained members, such as the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects.</span></span>

> [!Note]  
> <span data-ttu-id="944af-106">使用 Real-Time 手寫筆，應用程式可以選擇以自己的格式維護資料， (例如儲存筆劃) 。</span><span class="sxs-lookup"><span data-stu-id="944af-106">Using Real-Time Stylus, applications may choose to maintain data in its own format (such as saving strokes).</span></span>

 

## <a name="ink-strokes-and-packets"></a><span data-ttu-id="944af-107">筆墨、筆劃和封包</span><span class="sxs-lookup"><span data-stu-id="944af-107">Ink, Strokes, and Packets</span></span>

<span data-ttu-id="944af-108">[**筆墨**](inkdisp-class.md)物件是管理、操作和儲存從 [**InkCollector**](inkcollector-class.md)物件收集之輸入的基本資料類型。</span><span class="sxs-lookup"><span data-stu-id="944af-108">An [**Ink**](inkdisp-class.md) object is the fundamental data type that manages, manipulates, and stores the input collected from the [**InkCollector**](inkcollector-class.md) object.</span></span> <span data-ttu-id="944af-109">**筆墨** 物件包含一個或多個 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件，以及用來管理和操作這些筆觸的一般方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="944af-109">An **Ink** object contains one or more [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects and common methods and properties to manage and manipulate those strokes.</span></span> <span data-ttu-id="944af-110">筆劃會定義為一組資料，而該資料集會在單一的向下筆、畫筆移動和畫筆序列中捕捉。</span><span class="sxs-lookup"><span data-stu-id="944af-110">A stroke is defined as the set of data that is captured in a single pen-down, pen-move, and pen-up sequence.</span></span> <span data-ttu-id="944af-111">筆劃資料包含封包集合。</span><span class="sxs-lookup"><span data-stu-id="944af-111">The stroke data contains a collection of packets.</span></span> <span data-ttu-id="944af-112">封包是一組 tablet 裝置在每個範例點傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="944af-112">A packet is the set of data that the tablet device sends at each sample point.</span></span> <span data-ttu-id="944af-113">此資料包含座標、畫筆壓力、畫筆角度，以及硬體可以傳輸的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="944af-113">This data contains information such as coordinates, pen pressure, pen angle, and anything else that the hardware can transmit.</span></span> <span data-ttu-id="944af-114">**筆觸** 物件的 [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription)屬性描述 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)電腦產生的封包。</span><span class="sxs-lookup"><span data-stu-id="944af-114">The [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) property of the **Stroke** object describes the packets that a [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) generates.</span></span>

## <a name="strokes"></a><span data-ttu-id="944af-115">中風</span><span class="sxs-lookup"><span data-stu-id="944af-115">Strokes</span></span>

<span data-ttu-id="944af-116">您可以使用 **筆墨** 物件的 [[**筆觸**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes)] 屬性，取得 [**筆跡**](inkdisp-class.md)物件中筆劃的快照。</span><span class="sxs-lookup"><span data-stu-id="944af-116">You can obtain a snapshot of the strokes in a [**Ink**](inkdisp-class.md) object by using the **Ink** object's [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) property.</span></span> <span data-ttu-id="944af-117">[**筆劃**] 屬性是在讀取 **筆觸** 屬性時 **筆跡** 物件中筆劃的參考集合。</span><span class="sxs-lookup"><span data-stu-id="944af-117">The **Strokes** property is a collection of references to the strokes in the **Ink** object at the time the **Strokes** property is read.</span></span> <span data-ttu-id="944af-118">如果後續在 **筆跡** 物件中新增或刪除筆劃，則不會更新先前取得的 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="944af-118">If strokes are subsequently added to or deleted from the **Ink** object, a previously obtained [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is not updated.</span></span> <span data-ttu-id="944af-119">此外，[ **筆劃** ] 屬性是一個值，如同任何值，除非指派給變數，否則不會超出範圍。</span><span class="sxs-lookup"><span data-stu-id="944af-119">Furthermore, the **Strokes** property is a value and, like any value, goes out of scope unless it is assigned to a variable.</span></span>

<span data-ttu-id="944af-120">若要讓 [**筆觸**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes)屬性與 [**Ink**](inkdisp-class.md)物件同步，請將其包裝在 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合上 [**StrokesAdded**](inkstrokes-strokesadded.md)和 [**StrokesRemoved**](inkstrokes-strokesremoved.md)事件的事件處理常式中。</span><span class="sxs-lookup"><span data-stu-id="944af-120">To keep a [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) property synchronized with an [**Ink**](inkdisp-class.md) object, wrap it in an event handler for the [**StrokesAdded**](inkstrokes-strokesadded.md) and [**StrokesRemoved**](inkstrokes-strokesremoved.md) events on the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="944af-121">引發任何事件時，處理常式應該取得 **筆劃** 屬性的新複本。</span><span class="sxs-lookup"><span data-stu-id="944af-121">The handler should obtain a new copy of the **Strokes** property when either event is fired.</span></span> <span data-ttu-id="944af-122">請小心不要將事件處理常式新增至在引發事件之前超出範圍的 **筆劃** 集合。</span><span class="sxs-lookup"><span data-stu-id="944af-122">Be careful not to add the event handler to a **Strokes** collection that is out of scope before the event is fired.</span></span>

<span data-ttu-id="944af-123">請注意，在此範例中， `theAddedStrokesIDs` 會在處理常式中使用新的筆觸屬性複本來更新 `StrokesAdded_Event` 。</span><span class="sxs-lookup"><span data-stu-id="944af-123">Notice in this example that `theAddedStrokesIDs` is updated with a new copy of the strokes property in the `StrokesAdded_Event` handler.</span></span>


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a><span data-ttu-id="944af-124">PacketDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="944af-124">PacketDescription Property</span></span>

<span data-ttu-id="944af-125">[**筆墨**](inkdisp-class.md)物件的 [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription)屬性會定義每個封包中的一組資訊，應用程式會從 Tablet PC 裝置取得這些資訊。</span><span class="sxs-lookup"><span data-stu-id="944af-125">The [**Ink**](inkdisp-class.md) object's [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) property defines the set of information in each packet that the application gets from a Tablet PC device.</span></span> <span data-ttu-id="944af-126">這項資訊通常包含座標，但它可以包含更詳細的資訊 (根據 Tablet PC 數位板) 的功能，例如畫筆壓力或畫筆角度。</span><span class="sxs-lookup"><span data-stu-id="944af-126">The information typically includes coordinates, but it can include much more detailed information (depending on what the capabilities of Tablet PC digitizer) such as pen pressure or pen angle.</span></span> <span data-ttu-id="944af-127">藉由在 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上設定封包描述，再收集任何筆墨 (使用 DesiredPacketDescription 屬性) ，您可以完全控制要接收的 Tablet PC 裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="944af-127">By setting packet descriptions on the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object before any ink is collected (using the DesiredPacketDescription property), you have full control over which of the Tablet PC devices properties you want to receive.</span></span>

## <a name="extended-properties"></a><span data-ttu-id="944af-128">擴充屬性</span><span class="sxs-lookup"><span data-stu-id="944af-128">Extended Properties</span></span>

<span data-ttu-id="944af-129">擴充屬性提供一種機制，可將應用程式定義的資料附加至 [**筆跡**](inkdisp-class.md) 和其他物件。</span><span class="sxs-lookup"><span data-stu-id="944af-129">Extended properties provide a mechanism for attaching application-defined data to [**Ink**](inkdisp-class.md) and other objects.</span></span> <span data-ttu-id="944af-130">如需有關擴充屬性的詳細資訊，請參閱 [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) 集合。</span><span class="sxs-lookup"><span data-stu-id="944af-130">For more information about extended properties, see the [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) collection.</span></span>

## <a name="ink-rendering"></a><span data-ttu-id="944af-131">筆墨轉譯</span><span class="sxs-lookup"><span data-stu-id="944af-131">Ink Rendering</span></span>

<span data-ttu-id="944af-132">轉譯 [**器物件負責**](inkrenderer-class.md) 呈現 [**筆墨**](inkdisp-class.md)。</span><span class="sxs-lookup"><span data-stu-id="944af-132">The [**Renderer**](inkrenderer-class.md) object is responsible for rendering [**Ink**](inkdisp-class.md).</span></span> <span data-ttu-id="944af-133">由於有適當的 tablet 內容，轉譯 **器物件可以** 將筆墨空間座標組應到圖元、套用視圖轉換，以及在螢幕和印表機上顯示筆墨。</span><span class="sxs-lookup"><span data-stu-id="944af-133">Given an appropriate tablet context, the **Renderer** object can map ink space coordinates to pixels, apply view transforms, and display ink on screens and printers.</span></span> <span data-ttu-id="944af-134">[**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)和 [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)方法是用來呈現筆墨的主要方法。</span><span class="sxs-lookup"><span data-stu-id="944af-134">The [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) and [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) methods are the primary methods for rendering ink.</span></span> <span data-ttu-id="944af-135">如需在視窗中顯示筆墨的詳細資訊，請參閱轉譯 **器物件。**</span><span class="sxs-lookup"><span data-stu-id="944af-135">For more information about displaying ink in a window, see the **Renderer** object.</span></span>

## <a name="cusps"></a><span data-ttu-id="944af-136">Cusps</span><span class="sxs-lookup"><span data-stu-id="944af-136">Cusps</span></span>

<span data-ttu-id="944af-137">當畫筆降至繪圖介面時，通常會開始筆觸，並且在產生畫筆時結束。</span><span class="sxs-lookup"><span data-stu-id="944af-137">A stroke normally begins when the pen is lowered to the drawing surface and ends when the pen is raised.</span></span> <span data-ttu-id="944af-138">在筆劃內，方向的尖峰、角度和根式變更稱為 cusps。</span><span class="sxs-lookup"><span data-stu-id="944af-138">Within a stroke, the peaks, angles, and radical changes of direction are called cusps.</span></span> <span data-ttu-id="944af-139">筆劃的端點也會被視為 cusps。</span><span class="sxs-lookup"><span data-stu-id="944af-139">The endpoints of a stroke are also considered cusps.</span></span> <span data-ttu-id="944af-140">例如，大寫字母 "L" 有三個 cusps，一個在中間，一個在每一端。</span><span class="sxs-lookup"><span data-stu-id="944af-140">For example, the capital letter "L" has three cusps, one in the middle and one at each end.</span></span>

<span data-ttu-id="944af-141">輸入筆觸時，通常會使用貝塞爾 (或線條) 曲線，以平滑和呈現。</span><span class="sxs-lookup"><span data-stu-id="944af-141">As a stroke is entered, it is normally smoothed and rendered using a Bezier (or polyline) curve.</span></span> <span data-ttu-id="944af-142">貝茲曲線可能會將 cusps 變成小迴圈。</span><span class="sxs-lookup"><span data-stu-id="944af-142">Bezier curves may turn cusps into small loops.</span></span> <span data-ttu-id="944af-143">例如，草書信件 "i" 的尖峰可能會平滑化，使其類似于草書 "e"。</span><span class="sxs-lookup"><span data-stu-id="944af-143">For example, the peak of the cursive letter "i" might be smoothed to resemble the cursive "e".</span></span> <span data-ttu-id="944af-144">為了避免這種情況，Microsoft 轉譯器有以不同方式處理 cusps 的「預先貝塞爾」階段。</span><span class="sxs-lookup"><span data-stu-id="944af-144">To prevent this, Microsoft renderers have a "pre-Bezier" phase that handles the cusps differently.</span></span>

<span data-ttu-id="944af-145">Cusps 也可用來將 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件細分為可讀寫單位。</span><span class="sxs-lookup"><span data-stu-id="944af-145">Cusps can also be used to subdivide [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects into erasable units.</span></span> <span data-ttu-id="944af-146">例如，選取大寫 "L" 的垂直側邊可能表示只清除該端。</span><span class="sxs-lookup"><span data-stu-id="944af-146">For example, selecting the vertical side of a capital "L" could indicate erasing just that side.</span></span> <span data-ttu-id="944af-147">要清除之筆劃的部分將會是兩個 cusps 之間的部分。</span><span class="sxs-lookup"><span data-stu-id="944af-147">The part of the stroke to be erased would be the part between two cusps.</span></span>

 

 
