---
description: 本主題介紹筆墨分析 Api。
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: 基本辨識和筆墨分析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386015"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="15c70-103">基本辨識和筆墨分析</span><span class="sxs-lookup"><span data-stu-id="15c70-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="15c70-104">本主題介紹筆墨分析 Api。</span><span class="sxs-lookup"><span data-stu-id="15c70-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="15c70-105">簡單識別</span><span class="sxs-lookup"><span data-stu-id="15c70-105">Simple Recognition</span></span>

<span data-ttu-id="15c70-106">筆墨分析 API 所公開的基本功能是存取指定筆跡的辨識結果。</span><span class="sxs-lookup"><span data-stu-id="15c70-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="15c70-107">這是簡單且簡單的方式，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="15c70-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="15c70-108">辨識作業的結果只是表示手寫筆跡辨識值的字串值。</span><span class="sxs-lookup"><span data-stu-id="15c70-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="15c70-109">筆墨分析 API 會公開比辨識的字串更多的辨識功能，但這是最常見的作業。</span><span class="sxs-lookup"><span data-stu-id="15c70-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="15c70-110">遞增辨識</span><span class="sxs-lookup"><span data-stu-id="15c70-110">Incremental Recognition</span></span>

<span data-ttu-id="15c70-111">辨識程式需要一些時間才能完成，封鎖應用程式的 UI 執行緒來封鎖應用程式的存取。</span><span class="sxs-lookup"><span data-stu-id="15c70-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="15c70-112">因此，讓使用者以同步方式等待結果可能會很耗費成本，而令人沮喪。</span><span class="sxs-lookup"><span data-stu-id="15c70-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="15c70-113">許多 Tablet PC 應用程式都需要辨識多行筆墨，而且在背景執行緒上辨識筆劃的漸進式方法是最佳的策略。</span><span class="sxs-lookup"><span data-stu-id="15c70-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="15c70-114">漸進式方法（而非大量作業）的優點是，它允許在一段時間內進行筆劃的辨識，並在背景執行緒上分配工作，而不是在前景執行緒上同步處理。</span><span class="sxs-lookup"><span data-stu-id="15c70-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="15c70-115">為了支援累加式分析， [**InkAnalyzer**](inkanalyzer.md) 物件具有 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法，可處理應用程式背景執行緒的建立和管理。</span><span class="sxs-lookup"><span data-stu-id="15c70-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="15c70-116">**InkAnalyzer** 也會自動負責管理需要辨識的內容，以及已辨識的內容。</span><span class="sxs-lookup"><span data-stu-id="15c70-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="15c70-117">因此，有兩種機制可取得辨識結果：</span><span class="sxs-lookup"><span data-stu-id="15c70-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="15c70-118">[**分析**](iinkanalyzer-analyze.md)方法 (同步分析) ，最適用于：</span><span class="sxs-lookup"><span data-stu-id="15c70-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="15c70-119">少量的筆跡。</span><span class="sxs-lookup"><span data-stu-id="15c70-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="15c70-120">當需要結果之後，才能繼續執行應用程式中的下一個作業，例如顯示更正使用者介面時。</span><span class="sxs-lookup"><span data-stu-id="15c70-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="15c70-121">[**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)方法 (非同步分析) ，最適用于：</span><span class="sxs-lookup"><span data-stu-id="15c70-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="15c70-122">任意數量的筆墨。</span><span class="sxs-lookup"><span data-stu-id="15c70-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="15c70-123">搭配計時器使用時大約每隔600毫秒。</span><span class="sxs-lookup"><span data-stu-id="15c70-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="15c70-124">目前的建議是600毫秒，但此時間可能會有變更等待進一步的測試。</span><span class="sxs-lookup"><span data-stu-id="15c70-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="15c70-125">若要使用 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 作業， [**InkCollector**](inkcollector-class.md) 物件 (或類似的物件或控制項（例如 [**RealTimeStylus**](realtimestylus-class.md) (RTS) 、 [**InkOverlay**](inkoverlay-class.md)或 Windows Presentation Foundation 中的 [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) ）) 管理筆墨筆劃的集合和轉譯。</span><span class="sxs-lookup"><span data-stu-id="15c70-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="15c70-126">如果 **InkCollector** 與筆墨分析 api 配對，應用程式可以通知 [**InkAnalyzer**](inkanalyzer.md) 有關新增至應用程式的每個新筆劃，藉以保留更新的辨識結果。</span><span class="sxs-lookup"><span data-stu-id="15c70-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="15c70-127">這可讓 **InkAnalyzer** 在背景執行緒上以累加方式辨識筆劃。</span><span class="sxs-lookup"><span data-stu-id="15c70-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="15c70-128">若要完成增量背景分析，應用程式必須執行三個步驟， (針對 managed 程式碼) 所示：</span><span class="sxs-lookup"><span data-stu-id="15c70-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="15c70-129">只要引發 [**InkOverlay**](inkoverlay-class.md)物件的 [**stroke**](inkoverlay-stroke.md)事件，就將筆劃新增至 [**InkAnalyzer**](inkanalyzer.md) ：</span><span class="sxs-lookup"><span data-stu-id="15c70-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="15c70-130">以設定的間隔叫用 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 作業。</span><span class="sxs-lookup"><span data-stu-id="15c70-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="15c70-131">注意：應用程式不應該只是在每個新的筆觸之後叫用背景分析作業。</span><span class="sxs-lookup"><span data-stu-id="15c70-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="15c70-132">如果背景作業已在執行中，這將會失敗 (傳回值 **false**) 。</span><span class="sxs-lookup"><span data-stu-id="15c70-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="15c70-133">這種行為的原因是限制背景執行緒和所需的對帳作業數目。</span><span class="sxs-lookup"><span data-stu-id="15c70-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="15c70-134">接聽 [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) 事件 (managed 程式碼) 或 [**結果**](-ianalysisevents-results.md) 事件 (c + + 程式碼) ，以判斷背景進程已完成的時間：</span><span class="sxs-lookup"><span data-stu-id="15c70-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="15c70-135">現在已在背景執行緒上完成筆墨的處理，因此應用程式能夠在背景作業運作時接受對筆墨的變更。</span><span class="sxs-lookup"><span data-stu-id="15c70-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="15c70-136">如果我們使用同步執行緒，就不可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="15c70-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="15c70-137">工作會在 UI 執行緒上執行，並封鎖變更的能力。</span><span class="sxs-lookup"><span data-stu-id="15c70-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="15c70-138">變更包括將更多筆墨新增至檔、刪除筆墨，或轉換現有筆墨的位置或外觀。</span><span class="sxs-lookup"><span data-stu-id="15c70-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="15c70-139">在背景作業期間發生的變更實際上可能會使結果無效。</span><span class="sxs-lookup"><span data-stu-id="15c70-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="15c70-140">例如，從 word 刪除筆劃會變更該單字的辨識值。</span><span class="sxs-lookup"><span data-stu-id="15c70-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="15c70-141">[**InkAnalyzer**](inkanalyzer.md) API 具有內建的對帳程式，可自動判斷背景作業的哪些部分會因為筆墨在分析時的變更而變成無效。</span><span class="sxs-lookup"><span data-stu-id="15c70-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="15c70-142">因為有三個因素，所以會完成自動對帳進程：</span><span class="sxs-lookup"><span data-stu-id="15c70-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="15c70-143">[**DirtyRegion**](iinkanalyzer-getdirtyregion.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="15c70-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="15c70-144">每次應用程式新增 ([**AddStroke**](iinkanalyzer-addstroke.md)方法) 或移除 [**InkAnalyzer**](inkanalyzer.md)的筆觸) 的 ([**RemoveStroke**](iinkanalyzer-removestroke.md)方法時，就會捕捉筆觸的實體位置，並在下次叫用分析作業時， **InkAnalyzer** 確保分析筆劃或該筆劃所佔用的區域。</span><span class="sxs-lookup"><span data-stu-id="15c70-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="15c70-145">每當應用程式修改現有的筆跡、變更位置，或變更筆墨的其他繪圖屬性時，變更的位置)  (可以加入至 [**InkAnalyzer**](inkanalyzer.md)的 [**DirtyRegion**](iinkanalyzer-getdirtyregion.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="15c70-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="15c70-146">這可確保下次應用程式啟動分析作業時，系統會檢查這些區域是否有正確的結果。</span><span class="sxs-lookup"><span data-stu-id="15c70-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="15c70-147">因此， [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) 屬性會在分析回合之間追蹤檔的哪些區域，以及要檢查哪些筆觸以找出正確的筆墨分析和辨識結果。</span><span class="sxs-lookup"><span data-stu-id="15c70-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="15c70-148">有限的分析。</span><span class="sxs-lookup"><span data-stu-id="15c70-148">Limited analysis.</span></span>

    -   <span data-ttu-id="15c70-149">每次應用程式叫用分析作業時， [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) 屬性會識別需要分析的筆劃。</span><span class="sxs-lookup"><span data-stu-id="15c70-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="15c70-150">這可讓分析作業將作業限制為僅限中途區域，並忽略所有其他區域，以優化重新分析筆墨所花費的時間量。</span><span class="sxs-lookup"><span data-stu-id="15c70-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="15c70-151">[**InkAnalyzer**](inkanalyzer.md)不會完全忽略頁面上的所有其他區域，而是會檢查鄰近的區域，以判斷在中途區域中所做的變更是否會影響這些鄰近區域。</span><span class="sxs-lookup"><span data-stu-id="15c70-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="15c70-152">例如，在下列筆墨範例中，分析器會將 "：" 分類為 [**CoNtextNode**](icontextnode.md)類別的單一 **InkWord** 類型：</span><span class="sxs-lookup"><span data-stu-id="15c70-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

![手寫「是」](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="15c70-154">刪除 "s" 會導致中途區域 (標示紅色方塊) 。</span><span class="sxs-lookup"><span data-stu-id="15c70-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

![手寫 "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="15c70-156">分析之後，分析器會將 "I" 的分類變更為 **InkDrawing** 類型，即使它不在中途區域內也是一樣，因為沒有支援 "s" 筆觸，筆跡50/50 分析器的筆墨可能會將筆墨分類為繪圖或單字。</span><span class="sxs-lookup"><span data-stu-id="15c70-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="15c70-157">內部快取狀態。</span><span class="sxs-lookup"><span data-stu-id="15c70-157">Internally cached state.</span></span>

    -   <span data-ttu-id="15c70-158">當應用程式叫用背景分析作業時， [**InkAnalyzer**](inkanalyzer.md) 會快取剪除資料的快照集。</span><span class="sxs-lookup"><span data-stu-id="15c70-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="15c70-159">藉由建立快照集， **InkAnalyzer** 可以針對應用程式所使用的資料，個別分析資料，或使用快照集做為比較點，判斷應用程式在背景分析時所做的變更。</span><span class="sxs-lookup"><span data-stu-id="15c70-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="15c70-160">快取狀態和比較變更比保留一個主要原因所發生之所有變更的清單更好：資料 proxy。</span><span class="sxs-lookup"><span data-stu-id="15c70-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="15c70-161">這是本檔稍後所述的 advanced 案例，但它牽涉到應用程式只會在叫用的分析作業之前，以及在處理分析作業的結果之前，以目前的筆墨和非筆墨資料更新 [**InkAnalyzer**](inkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="15c70-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="15c70-162">簡單筆墨分析</span><span class="sxs-lookup"><span data-stu-id="15c70-162">Simple Ink Analysis</span></span>

<span data-ttu-id="15c70-163">先前的兩個案例 (簡單的辨識和遞增辨識) 概述如何存取辨識值，但不會提及如何存取筆墨分析或分類結果。</span><span class="sxs-lookup"><span data-stu-id="15c70-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="15c70-164">[**InkAnalyzer**](inkanalyzer.md)的預設設定會執行筆墨分析演算法和辨識演算法。</span><span class="sxs-lookup"><span data-stu-id="15c70-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="15c70-165">此設定會產生最精確的結果，因為這兩種技術會一起運作以提高精確度。</span><span class="sxs-lookup"><span data-stu-id="15c70-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="15c70-166">也就是說，筆墨分析引擎可協助您將繪圖與書寫區分開，然後以水準平面的角度來正規化，也就是辨識引擎的最佳輸入平面。</span><span class="sxs-lookup"><span data-stu-id="15c70-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="15c70-167">若要存取筆墨分析結果，您的應用程式會使用 [**分析**](iinkanalyzer-analyze.md) 或 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法，完全如先前的兩個辨識案例所述。</span><span class="sxs-lookup"><span data-stu-id="15c70-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="15c70-168">沒有任何變更，因為呼叫這些方法時，已執行筆墨分析和辨識演算法。</span><span class="sxs-lookup"><span data-stu-id="15c70-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="15c70-169">但是，存取結果比讀取字串的值更複雜。</span><span class="sxs-lookup"><span data-stu-id="15c70-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="15c70-170">例如，下列程式碼範例會藉由在組成分類的筆劃群組周圍呈現矩形，來顯示所有 **InkWord** 區段和 **InkDrawing** 區段的群組和位置。</span><span class="sxs-lookup"><span data-stu-id="15c70-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="15c70-171">此範例只會使用表單的 **繪製** 事件，以在單字或繪圖周圍呈現彩色矩形。</span><span class="sxs-lookup"><span data-stu-id="15c70-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="15c70-172">[**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)方法會傳回物件的集合，這些物件只有在已執行分析作業且結果包含具有指定 [**CoNtextNode**](icontextnode.md)類型的分類時才存在。</span><span class="sxs-lookup"><span data-stu-id="15c70-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="15c70-173">如果檔中不存在所需類型的 **CoNtextNode** ，則會略過繪製矩形的步驟。</span><span class="sxs-lookup"><span data-stu-id="15c70-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="15c70-174">從 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法傳回的每個物件都會有與這類分類相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="15c70-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="15c70-175">例如， **InkWordNode** 會參考組成檔中單一單字的所有筆劃，並參考該單字的可辨識字串。</span><span class="sxs-lookup"><span data-stu-id="15c70-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="15c70-176">**InkDrawingNode** 會參考組成檔中單一繪圖的所有筆劃，並參考該繪圖的圖形名稱。</span><span class="sxs-lookup"><span data-stu-id="15c70-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="15c70-177">[**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)方法非常類似于 [**DivisionResult：： ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype)方法，它會傳回撰寫或繪圖類型的 [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits)集合。</span><span class="sxs-lookup"><span data-stu-id="15c70-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="15c70-178">若要讓先前的程式碼範例進入觀點，請考慮下列筆墨範例：</span><span class="sxs-lookup"><span data-stu-id="15c70-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![筆墨範例「這是一些筆墨」。](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="15c70-181">如果您呼叫 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法，並傳入 **InkWord** 的靜態欄位，分析器會傳回四個 **InkWordNode** 物件的集合：</span><span class="sxs-lookup"><span data-stu-id="15c70-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![分析器的輸出：「這是一些筆墨」](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="15c70-183">如果您呼叫 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法，並傳入 **InkDrawing** 的靜態欄位，分析器會傳回一個 **InkDrawingNode** 物件的集合：</span><span class="sxs-lookup"><span data-stu-id="15c70-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![顯示「oval」的影像，來自 inkdrawing 分析器的結果](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="15c70-185">在引發 **油漆** 事件之後，範例程式碼會在每個物件周圍呈現矩形：</span><span class="sxs-lookup"><span data-stu-id="15c70-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![在物件和單字周圍呈現矩形的原始繪圖](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="15c70-187">這個範例只會在 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法上進行，但因為筆墨分析引擎可以偵測到一組更豐富的筆墨類型，所以此方法也會對應至筆墨分析引擎所偵測到的所有節點類型， (例如線條、段落和其他結構) 。</span><span class="sxs-lookup"><span data-stu-id="15c70-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="15c70-188">使用筆墨分析與點清除</span><span class="sxs-lookup"><span data-stu-id="15c70-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="15c70-189">您的應用程式必須在執行點清除時以更新筆劃的方式進行調整，以確保效能良好。</span><span class="sxs-lookup"><span data-stu-id="15c70-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="15c70-190">首先，在應用層，將現有筆劃的手寫筆點取代為新筆劃的手寫筆點，然後針對該筆劃呼叫 [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) ，並以筆劃的範圍更新中途區域。</span><span class="sxs-lookup"><span data-stu-id="15c70-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="15c70-191">這會導致 [**InkAnalyzer**](inkanalyzer.md) 在下一輪背景分析開始時，提取更新的筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="15c70-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="15c70-192">下列範例會示範這項技術。</span><span class="sxs-lookup"><span data-stu-id="15c70-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="15c70-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="15c70-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c70-194">筆墨分析總覽</span><span class="sxs-lookup"><span data-stu-id="15c70-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="15c70-195">筆墨分析 API 使用方式</span><span class="sxs-lookup"><span data-stu-id="15c70-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
