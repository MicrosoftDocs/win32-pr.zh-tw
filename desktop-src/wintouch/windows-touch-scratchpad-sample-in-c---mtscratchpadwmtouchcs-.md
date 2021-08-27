---
title: WindowsC (MTScratchpadWMTouchCS) 的觸控式範例
description: 'c # 中的 Windows Touch 便箋範例會示範如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。'
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows觸控、程式碼範例
- Windows觸控，範例程式碼
- Windows觸控、便箋簿範例
- 便箋範例
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 112f8446af4b845bfd36e4262a11da807535c93baaf6257a10a9a8d2b03374e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089841"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows觸控簿範例 (c # ) 

[c # 中的 Windows Touch 便箋範例會示範](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS)如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。 主要手指的追蹤（先放在數位板上）會以黑色繪製。 次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。 下圖顯示應用程式執行時的外觀。

![螢幕擷取畫面，顯示在螢幕上以紅色、綠色、藍色和紅色波浪線表示的 windows 觸控式攝影者範例](images/mtscratchpadwmtouchcs.png)

在此範例中，會建立可觸式表單來處理 [**WM_TOUCH**](wm-touchdown.md) 的訊息。 這種表單是繼承的，可啟用 [便箋] 應用程式上的 Windows Touch。 當 **WM_TOUCH** 訊息送至表單時，它們會被轉譯為點，並新增至筆劃的集合中。 筆觸集合會轉譯為繪圖物件。 下列程式碼顯示可觸式表單如何自行註冊處理 **WM_TOUCH** 訊息，以及它如何處理 **WM_TOUCH** 訊息。

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

下列程式碼說明如何解讀 Windows Touch 訊息，以及如何將資料加入至筆劃集合。

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

下列程式碼示範如何顯示筆觸集合。

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

下列程式碼示範個別筆劃物件如何以繪圖物件顯示本身。

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a>相關主題

[Windows Touch 的 () 的 c + + ](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md)、[多點觸控式的程式 (WM_TOUCH/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS)、[多點觸控式的便箋應用程式 (WM_TOUCH/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp)、 [Windows Touch 範例](windows-touch-samples.md)

