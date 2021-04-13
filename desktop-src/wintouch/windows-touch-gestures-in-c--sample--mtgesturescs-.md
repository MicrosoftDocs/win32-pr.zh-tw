---
title: 'C 範例中的 Windows Touch 手勢 (MTGesturesCS) '
description: 本節說明 C \ 中的 Windows Touch 手勢範例。
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，手勢
- Windows Touch、手勢範例
- 手勢範例
- 手勢，範例程式碼
- 手勢，程式碼範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374422"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="2490d-110">C # 範例中的 Windows Touch 手勢 (MTGesturesCS) </span><span class="sxs-lookup"><span data-stu-id="2490d-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="2490d-111">本節說明 c # 中的 Windows Touch 手勢範例。</span><span class="sxs-lookup"><span data-stu-id="2490d-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="2490d-112">此 Windows Touch 手勢範例示範如何使用手勢訊息，藉由處理 [**WM_GESTURE**](wm-gesture.md) 訊息，來轉譯、旋轉和調整圖形裝置介面 (GDI) 所轉譯的方塊。</span><span class="sxs-lookup"><span data-stu-id="2490d-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="2490d-113">下列螢幕擷取畫面顯示範例在執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="2490d-113">The following screen shot shows how the sample looks when it is running.</span></span>

![螢幕擷取畫面，顯示 c 中的 windows 觸控手勢（當其正在執行時），並在畫面上以黑色空心矩形為中心](images/mtgesturescs.png)

<span data-ttu-id="2490d-115">在此範例中，會將手勢訊息傳遞至手勢引擎，然後呼叫繪圖物件上的方法，以轉譯、旋轉和縮放具有處理這些命令之方法的物件。</span><span class="sxs-lookup"><span data-stu-id="2490d-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="2490d-116">若要在 c # 中這麼做，會建立特殊形式 TouchableForm 來處理手勢訊息。</span><span class="sxs-lookup"><span data-stu-id="2490d-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="2490d-117">然後，此表單會使用訊息來變更繪圖物件（DrawingObject），以變更物件在油漆方法中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="2490d-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="2490d-118">若要協助示範範例的運作方式，請考慮使用平移命令轉譯轉譯方塊的步驟。</span><span class="sxs-lookup"><span data-stu-id="2490d-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="2490d-119">使用者執行平移手勢，此動作會產生具有手勢識別碼 GID_PAN 的 [**WM_GESTURE**](wm-gesture.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2490d-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="2490d-120">TouchableForm 會處理此訊息並更新繪圖物件的位置，然後物件會轉譯成本身的轉譯。</span><span class="sxs-lookup"><span data-stu-id="2490d-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="2490d-121">下列程式碼示範軌跡處理常式如何從 [**WM_GESTURE**](wm-gesture.md) 訊息抓取參數，然後透過呼叫繪圖物件的 move 方法，在轉譯的方塊上執行轉譯。</span><span class="sxs-lookup"><span data-stu-id="2490d-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

<span data-ttu-id="2490d-122">下列程式碼顯示繪圖物件的 move 方法如何更新內部位置變數。</span><span class="sxs-lookup"><span data-stu-id="2490d-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="2490d-123">下列程式碼顯示如何在繪圖物件的 paint 方法中使用位置。</span><span class="sxs-lookup"><span data-stu-id="2490d-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

<span data-ttu-id="2490d-124">平移手勢將會轉譯已轉譯的繪圖方塊。</span><span class="sxs-lookup"><span data-stu-id="2490d-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2490d-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="2490d-125">Related topics</span></span>

<span data-ttu-id="2490d-126">[多點觸控手勢應用程式 (c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)、 [多點觸控手勢應用程式 (c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp)、 [Windows Touch 範例](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="2490d-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
