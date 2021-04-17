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
# <a name="basic-recognition-and-ink-analysis"></a>基本辨識和筆墨分析

本主題介紹筆墨分析 Api。

## <a name="simple-recognition"></a>簡單識別

筆墨分析 API 所公開的基本功能是存取指定筆跡的辨識結果。 這是簡單且簡單的方式，如下列範例程式碼所示。


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



辨識作業的結果只是表示手寫筆跡辨識值的字串值。 筆墨分析 API 會公開比辨識的字串更多的辨識功能，但這是最常見的作業。

## <a name="incremental-recognition"></a>遞增辨識

辨識程式需要一些時間才能完成，封鎖應用程式的 UI 執行緒來封鎖應用程式的存取。 因此，讓使用者以同步方式等待結果可能會很耗費成本，而令人沮喪。 許多 Tablet PC 應用程式都需要辨識多行筆墨，而且在背景執行緒上辨識筆劃的漸進式方法是最佳的策略。 漸進式方法（而非大量作業）的優點是，它允許在一段時間內進行筆劃的辨識，並在背景執行緒上分配工作，而不是在前景執行緒上同步處理。 為了支援累加式分析， [**InkAnalyzer**](inkanalyzer.md) 物件具有 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法，可處理應用程式背景執行緒的建立和管理。 **InkAnalyzer** 也會自動負責管理需要辨識的內容，以及已辨識的內容。

因此，有兩種機制可取得辨識結果：

-   [**分析**](iinkanalyzer-analyze.md)方法 (同步分析) ，最適用于：

    -   少量的筆跡。
    -   當需要結果之後，才能繼續執行應用程式中的下一個作業，例如顯示更正使用者介面時。

-   [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)方法 (非同步分析) ，最適用于：

    -   任意數量的筆墨。
    -   搭配計時器使用時大約每隔600毫秒。

> [!Note]  
> 目前的建議是600毫秒，但此時間可能會有變更等待進一步的測試。

 

若要使用 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 作業， [**InkCollector**](inkcollector-class.md) 物件 (或類似的物件或控制項（例如 [**RealTimeStylus**](realtimestylus-class.md) (RTS) 、 [**InkOverlay**](inkoverlay-class.md)或 Windows Presentation Foundation 中的 [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) ）) 管理筆墨筆劃的集合和轉譯。 如果 **InkCollector** 與筆墨分析 api 配對，應用程式可以通知 [**InkAnalyzer**](inkanalyzer.md) 有關新增至應用程式的每個新筆劃，藉以保留更新的辨識結果。 這可讓 **InkAnalyzer** 在背景執行緒上以累加方式辨識筆劃。

若要完成增量背景分析，應用程式必須執行三個步驟， (針對 managed 程式碼) 所示：

1. 只要引發 [**InkOverlay**](inkoverlay-class.md)物件的 [**stroke**](inkoverlay-stroke.md)事件，就將筆劃新增至 [**InkAnalyzer**](inkanalyzer.md) ：


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



2. 以設定的間隔叫用 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 作業。


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
> 注意：應用程式不應該只是在每個新的筆觸之後叫用背景分析作業。 如果背景作業已在執行中，這將會失敗 (傳回值 **false**) 。 這種行為的原因是限制背景執行緒和所需的對帳作業數目。

 

3. 接聽 [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) 事件 (managed 程式碼) 或 [**結果**](-ianalysisevents-results.md) 事件 (c + + 程式碼) ，以判斷背景進程已完成的時間：


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



現在已在背景執行緒上完成筆墨的處理，因此應用程式能夠在背景作業運作時接受對筆墨的變更。 如果我們使用同步執行緒，就不可能發生這種情況。 工作會在 UI 執行緒上執行，並封鎖變更的能力。 變更包括將更多筆墨新增至檔、刪除筆墨，或轉換現有筆墨的位置或外觀。 在背景作業期間發生的變更實際上可能會使結果無效。 例如，從 word 刪除筆劃會變更該單字的辨識值。 [**InkAnalyzer**](inkanalyzer.md) API 具有內建的對帳程式，可自動判斷背景作業的哪些部分會因為筆墨在分析時的變更而變成無效。

因為有三個因素，所以會完成自動對帳進程：

1.  [**DirtyRegion**](iinkanalyzer-getdirtyregion.md)屬性。

    -   每次應用程式新增 ([**AddStroke**](iinkanalyzer-addstroke.md)方法) 或移除 [**InkAnalyzer**](inkanalyzer.md)的筆觸) 的 ([**RemoveStroke**](iinkanalyzer-removestroke.md)方法時，就會捕捉筆觸的實體位置，並在下次叫用分析作業時， **InkAnalyzer** 確保分析筆劃或該筆劃所佔用的區域。
    -   每當應用程式修改現有的筆跡、變更位置，或變更筆墨的其他繪圖屬性時，變更的位置)  (可以加入至 [**InkAnalyzer**](inkanalyzer.md)的 [**DirtyRegion**](iinkanalyzer-getdirtyregion.md)屬性。 這可確保下次應用程式啟動分析作業時，系統會檢查這些區域是否有正確的結果。
    -   因此， [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) 屬性會在分析回合之間追蹤檔的哪些區域，以及要檢查哪些筆觸以找出正確的筆墨分析和辨識結果。

2.  有限的分析。

    -   每次應用程式叫用分析作業時， [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) 屬性會識別需要分析的筆劃。 這可讓分析作業將作業限制為僅限中途區域，並忽略所有其他區域，以優化重新分析筆墨所花費的時間量。
    -   [**InkAnalyzer**](inkanalyzer.md)不會完全忽略頁面上的所有其他區域，而是會檢查鄰近的區域，以判斷在中途區域中所做的變更是否會影響這些鄰近區域。 例如，在下列筆墨範例中，分析器會將 "：" 分類為 [**CoNtextNode**](icontextnode.md)類別的單一 **InkWord** 類型：

![手寫「是」](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

刪除 "s" 會導致中途區域 (標示紅色方塊) 。

![手寫 "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

分析之後，分析器會將 "I" 的分類變更為 **InkDrawing** 類型，即使它不在中途區域內也是一樣，因為沒有支援 "s" 筆觸，筆跡50/50 分析器的筆墨可能會將筆墨分類為繪圖或單字。

-   內部快取狀態。

    -   當應用程式叫用背景分析作業時， [**InkAnalyzer**](inkanalyzer.md) 會快取剪除資料的快照集。 藉由建立快照集， **InkAnalyzer** 可以針對應用程式所使用的資料，個別分析資料，或使用快照集做為比較點，判斷應用程式在背景分析時所做的變更。
    -   快取狀態和比較變更比保留一個主要原因所發生之所有變更的清單更好：資料 proxy。 這是本檔稍後所述的 advanced 案例，但它牽涉到應用程式只會在叫用的分析作業之前，以及在處理分析作業的結果之前，以目前的筆墨和非筆墨資料更新 [**InkAnalyzer**](inkanalyzer.md) 。

## <a name="simple-ink-analysis"></a>簡單筆墨分析

先前的兩個案例 (簡單的辨識和遞增辨識) 概述如何存取辨識值，但不會提及如何存取筆墨分析或分類結果。 [**InkAnalyzer**](inkanalyzer.md)的預設設定會執行筆墨分析演算法和辨識演算法。 此設定會產生最精確的結果，因為這兩種技術會一起運作以提高精確度。 也就是說，筆墨分析引擎可協助您將繪圖與書寫區分開，然後以水準平面的角度來正規化，也就是辨識引擎的最佳輸入平面。

若要存取筆墨分析結果，您的應用程式會使用 [**分析**](iinkanalyzer-analyze.md) 或 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法，完全如先前的兩個辨識案例所述。 沒有任何變更，因為呼叫這些方法時，已執行筆墨分析和辨識演算法。 但是，存取結果比讀取字串的值更複雜。 例如，下列程式碼範例會藉由在組成分類的筆劃群組周圍呈現矩形，來顯示所有 **InkWord** 區段和 **InkDrawing** 區段的群組和位置。

此範例只會使用表單的 **繪製** 事件，以在單字或繪圖周圍呈現彩色矩形。 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)方法會傳回物件的集合，這些物件只有在已執行分析作業且結果包含具有指定 [**CoNtextNode**](icontextnode.md)類型的分類時才存在。 如果檔中不存在所需類型的 **CoNtextNode** ，則會略過繪製矩形的步驟。

從 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法傳回的每個物件都會有與這類分類相關的屬性。 例如， **InkWordNode** 會參考組成檔中單一單字的所有筆劃，並參考該單字的可辨識字串。 **InkDrawingNode** 會參考組成檔中單一繪圖的所有筆劃，並參考該繪圖的圖形名稱。

[**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)方法非常類似于 [**DivisionResult：： ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype)方法，它會傳回撰寫或繪圖類型的 [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits)集合。


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



若要讓先前的程式碼範例進入觀點，請考慮下列筆墨範例：

![筆墨範例「這是一些筆墨」。 其下有圓圈](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

如果您呼叫 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法，並傳入 **InkWord** 的靜態欄位，分析器會傳回四個 **InkWordNode** 物件的集合：

![分析器的輸出：「這是一些筆墨」](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

如果您呼叫 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法，並傳入 **InkDrawing** 的靜態欄位，分析器會傳回一個 **InkDrawingNode** 物件的集合：

![顯示「oval」的影像，來自 inkdrawing 分析器的結果](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

在引發 **油漆** 事件之後，範例程式碼會在每個物件周圍呈現矩形：

![在物件和單字周圍呈現矩形的原始繪圖](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

這個範例只會在 [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) 方法上進行，但因為筆墨分析引擎可以偵測到一組更豐富的筆墨類型，所以此方法也會對應至筆墨分析引擎所偵測到的所有節點類型， (例如線條、段落和其他結構) 。

## <a name="using-ink-analysis-with-point-erase"></a>使用筆墨分析與點清除

您的應用程式必須在執行點清除時以更新筆劃的方式進行調整，以確保效能良好。 首先，在應用層，將現有筆劃的手寫筆點取代為新筆劃的手寫筆點，然後針對該筆劃呼叫 [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) ，並以筆劃的範圍更新中途區域。 這會導致 [**InkAnalyzer**](inkanalyzer.md) 在下一輪背景分析開始時，提取更新的筆觸資料。 下列範例會示範這項技術。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[筆墨分析總覽](ink-analysis-overview.md)
</dt> <dt>

[筆墨分析 API 使用方式](ink-analysis-api-usage.md)
</dt> </dl>

 

 
