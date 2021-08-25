---
description: 此範例說明在給定螢幕位置的情況下，用來尋找筆墨的兩種方法。
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: 筆墨點擊測試範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995bd6f14b4a0a014452ae9392fa744ab93f01f9047c79e5dc30652c243473db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713078"
---
# <a name="ink-hit-test-sample"></a>筆墨點擊測試範例

此範例說明在給定螢幕位置的情況下，用來尋找筆墨的兩種方法。

此範例使用下列功能：

-   使用筆墨收集器
-   執行點擊測試
-   找出最接近的點

## <a name="accessing-the-ink-api"></a>存取筆墨 API

首先，參考位於 Windows Vista 或 Windows XP Tablet pc Edition 軟體發展工具組 (SDK) 的 Tablet pc 類別。


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>處理表單載入和小畫家事件

表單的 Load 事件處理常式：

-   建立表單的 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件（ic）。
-   將 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件的 [CollectionMode](/previous-versions/ms836497(v=msdn.10)) 屬性設定為忽略手勢。
-   啟用 [InkCollector](/previous-versions/ms583683(v=vs.100))。
-   將 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件的 [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) 屬性設定為 **TRUE**。


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



表單的小畫家事件處理常式會檢查應用程式模式：

-   在 System.windows.media.visualtreehelper.hittest 模式中，它會繪製圍繞游標的圓形。 現用畫筆是在應用程式的 handleHitTest 方法中設定。
-   在 NearestPoint 模式中，它會在游標和最接近資料指標的點之間繪製紅線。 最接近的點會在應用程式的 handleNearestPoint 方法中計算。


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



此範例具有非常簡單的重新繪製演算法。 當其 [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) 屬性設定為 **TRUE** 時，筆墨收集器會在重繪表單時自行重新繪製。 為了簡化重新繪製表單的工作，應用程式會追蹤一個周框方塊（invalidateRect 成員變數），以瞭解加入繪圖的區域，這會在每次重繪表單時失效。

## <a name="handling-menu-events"></a>處理功能表事件

Exit 命令會在結束應用程式之前停用 [InkCollector](/previous-versions/ms583683(v=vs.100)) 。

筆墨命令會更新應用程式模式和功能表狀態、啟用筆墨收集器，並讓先前繪製的表單區域失效。

點擊測試和最接近的點命令都會變更游標、更新應用程式模式和功能表狀態、停用筆墨收集器，並讓先前繪製的表單區域失效。

清楚！ 命令會停用[InkCollector](/previous-versions/ms583683(v=vs.100)) ，同時以新的[筆墨](/previous-versions/ms571716(v=vs.100))物件取代 InkCollector 物件的[筆墨](/previous-versions/ms836505(v=msdn.10))屬性、產生筆墨命令事件，然後強制重新整理控制項。

## <a name="handling-mouse-events"></a>處理滑鼠事件

[MouseMove](/previous-versions/ms567617(v=vs.100))事件處理常式會檢查應用程式模式：

-   在筆墨模式中，它不會執行任何動作，讓筆墨收集器可以正常地收集筆跡。
-   在 System.windows.media.visualtreehelper.hittest 模式中，它會將事件引數傳送至應用程式的 handleHitTest 方法。
-   在 NearestPoint 模式中，它會將事件引數傳送至應用程式的 handleNearestPoint 方法。

## <a name="performing-a-hit-test"></a>執行點擊測試

應用程式的 handleHitTest 方法會建立兩個點、游標位置和點 HitSize 距離游標的距離，然後將這兩個點從圖元轉換成筆墨空間座標。


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



然後， [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件會使用 [system.windows.media.visualtreehelper.hittest () ](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來尋找 pt3 內的任何筆觸。X-pt2。資料指標的 X 筆墨空間單位，pt2。


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



HandleHitTest 方法接著會根據是否找到筆劃來設定畫筆色彩、使 invalidateRect 區域失效、計算點擊測試圓形繪製所在的新區域，然後使新區域失效。

## <a name="locating-the-nearest-point"></a>找出最接近的點

應用程式的 handleNearestPoint 方法會建立兩個兩個點，兩者都等於游標的位置，其中一個點 pt，會轉換成筆墨空間，並用於[InkCollector](/previous-versions/ms583683(v=vs.100))[筆墨](/previous-versions/ms836505(v=msdn.10))物件的 NearestPoint 方法呼叫中。 NearestPoint 方法會傳回最接近該點的 [Stroke](/previous-versions/ms827842(v=msdn.10)) 物件，並設定浮點索引輸出參數。


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



如果沒有任何筆觸，NearestPoint 方法會傳回 **Null**，而資料指標位置會當做最接近的點使用。 否則，會計算對應至浮點數索引之筆劃上的位置。

最接近的點座標接著會轉換成從筆墨空間算出的圖元，handleNearestPoint 方法接著會使 invalidateRect 區域失效、計算新的區域，該行指向最接近的點，並使新的區域失效。

## <a name="closing-the-form"></a>關閉表單

表單的 Dispose 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。

 

 
