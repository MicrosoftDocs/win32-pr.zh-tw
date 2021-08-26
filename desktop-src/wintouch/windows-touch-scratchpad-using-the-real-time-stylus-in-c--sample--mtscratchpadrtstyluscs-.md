---
title: 'Windows使用 Real-Time 手寫筆範例 (c # ) 的觸控式便箋'
description: 複習 Windows Touch 的 (MTScratchpadRTStylus) 範例，其中會示範如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows觸控、程式碼範例
- Windows觸控，範例程式碼
- Windows觸控、便箋簿範例
- 便箋範例
- Windows觸控、即時手寫筆 (RTS) 物件
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055841"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows使用 Real-Time 手寫筆範例 (c # ) 的觸控式便箋

Windows Touch 的便箋範例 ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) 會示範如何使用 Windows Touch 訊息來繪製觸控點至視窗的追蹤。 主要手指的追蹤（先放在數位板上）會以黑色繪製。 次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。 下列螢幕擷取畫面顯示應用程式在執行時的外觀。

![螢幕擷取畫面，顯示 windows 觸控式攝影的範例，使用 c 中的即時手寫筆範例，並在螢幕上使用黑色和紅色波浪線](images/mtscratchpadrtstyluscs.png)

在此範例中，會建立 Real-Time 的手寫筆 (RTS) 物件，並啟用多個連絡人點的支援。 DynamicRenderer 外掛程式會新增至 RTS 以呈現內容。 外掛程式（EventHandlerPlugIn）的執行是追蹤手指的數目，以及變更動態轉譯器繪製的色彩。 使用 RTS 外掛程式堆疊中的這兩個外掛程式時，Windows Touch 的便箋會將主要連絡人轉譯為黑色，而其餘的連絡人會以各種不同的色彩呈現。

下列程式碼顯示 EventHandlerPlugIn 如何遞增和遞減連絡人數目的計數，並設定動態轉譯器的色彩。

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

下列程式碼說明如何使用多個接觸點支援來建立 RTS。

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

在 DynamicRenderer 物件的色彩變更並繪製筆觸之後，呼叫 DynamicRenderer：： Refresh 將會出現新的筆劃。 下列程式碼顯示如何在 OnPaintHandler 方法中執行這項作業。

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a>相關主題

[多點觸控式的程式簿應用程式 (rts/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)、多點觸控式的[程式 (RTS/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)、 [Windows Touch 範例](windows-touch-samples.md)
