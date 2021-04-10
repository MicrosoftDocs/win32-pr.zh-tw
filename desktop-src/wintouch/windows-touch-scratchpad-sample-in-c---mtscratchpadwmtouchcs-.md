---
title: 'C (MTScratchpadWMTouchCS 中的 Windows Touch 範例簿範例) '
description: 'C # 中的 Windows Touch 便箋範例會示範如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。'
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，範例簿範例
- 便箋範例
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 2d91c08c55f0d5b29a170a3a01c6ee882fad765f
ms.sourcegitcommit: c7fa8fc137714433c8d18b1bf71e9cf0b5bf5e80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/25/2020
ms.locfileid: "104024211"
---
# <a name="windows-touch-scratchpad-sample-c"></a><span data-ttu-id="02949-107">Windows Touch (的 c # 範例 ) </span><span class="sxs-lookup"><span data-stu-id="02949-107">Windows Touch Scratchpad Sample (C#)</span></span>

<span data-ttu-id="02949-108">[C # 中的 Windows Touch 便箋範例會示範](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS)如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。</span><span class="sxs-lookup"><span data-stu-id="02949-108">The [Windows Touch Scratchpad sample in C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="02949-109">主要手指的追蹤（先放在數位板上）會以黑色繪製。</span><span class="sxs-lookup"><span data-stu-id="02949-109">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="02949-110">次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。</span><span class="sxs-lookup"><span data-stu-id="02949-110">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="02949-111">下圖顯示應用程式執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="02949-111">The following image shows how the application could look when it runs.</span></span>

![螢幕擷取畫面，顯示在螢幕上以紅色、綠色、藍色和紅色波浪線表示的 windows 觸控式攝影者範例](images/mtscratchpadwmtouchcs.png)

<span data-ttu-id="02949-113">在此範例中，會建立可觸式表單來處理 [**WM_TOUCH**](wm-touchdown.md) 的訊息。</span><span class="sxs-lookup"><span data-stu-id="02949-113">For this sample, a touchable form is created to handle [**WM_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="02949-114">這種表單是繼承的，可啟用 [便箋] 應用程式上的 Windows Touch。</span><span class="sxs-lookup"><span data-stu-id="02949-114">This form is inherited to enable Windows Touch on the scratchpad application.</span></span> <span data-ttu-id="02949-115">當 **WM_TOUCH** 訊息送至表單時，它們會被轉譯為點，並新增至筆劃的集合中。</span><span class="sxs-lookup"><span data-stu-id="02949-115">When the **WM_TOUCH** messages come to the form, they are interpreted into points and are added to the collection of strokes.</span></span> <span data-ttu-id="02949-116">筆觸集合會轉譯為繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="02949-116">The strokes collection is rendered to the Graphics object.</span></span> <span data-ttu-id="02949-117">下列程式碼顯示可觸式表單如何自行註冊處理 **WM_TOUCH** 訊息，以及它如何處理 **WM_TOUCH** 訊息。</span><span class="sxs-lookup"><span data-stu-id="02949-117">The following code shows how the touchable form registers itself for handling **WM_TOUCH** messages, and how it handles **WM_TOUCH** messages.</span></span>

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

<span data-ttu-id="02949-118">下列程式碼說明如何解讀 Windows Touch 訊息，以及如何將資料加入至筆劃集合。</span><span class="sxs-lookup"><span data-stu-id="02949-118">The following code shows how the Windows Touch message is interpreted and the data is added to stroke collections.</span></span>

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

<span data-ttu-id="02949-119">下列程式碼示範如何顯示筆觸集合。</span><span class="sxs-lookup"><span data-stu-id="02949-119">The following code shows how a stroke collection is displayed.</span></span>

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

<span data-ttu-id="02949-120">下列程式碼示範個別筆劃物件如何以繪圖物件顯示本身。</span><span class="sxs-lookup"><span data-stu-id="02949-120">The following code shows how the individual stroke objects display themselves with a Graphics object.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="02949-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="02949-121">Related topics</span></span>

<span data-ttu-id="02949-122">[Windows Touch 的 () 的 c + + ](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md)、 [多點觸控式的程式 (WM_TOUCH/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS)、 [多點觸控式的便箋應用程式 (WM_TOUCH/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp)、 [Windows Touch 範例](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="02949-122">[Windows Touch Scratchpad Sample (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

