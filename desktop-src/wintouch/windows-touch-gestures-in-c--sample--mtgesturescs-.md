---
title: 'WindowsC 範例中的觸控手勢 (MTGesturesCS) '
description: 本節說明 C \ 中的 Windows Touch 手勢範例。
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows觸控、程式碼範例
- Windows觸控，範例程式碼
- Windows觸控、手勢
- Windows觸控、手勢範例
- 手勢範例
- 手勢，範例程式碼
- 手勢，程式碼範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089900"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>WindowsC # 範例中的觸控手勢 (MTGesturesCS) 

本節說明 c # 中的 Windows Touch 手勢範例。

此 Windows Touch 手勢範例示範如何使用手勢訊息，藉由處理 [**WM_GESTURE**](wm-gesture.md)訊息，來轉譯、旋轉和調整圖形裝置介面 (GDI) 所轉譯的方塊。 下列螢幕擷取畫面顯示範例在執行時的外觀。

![螢幕擷取畫面，顯示 c 中的 windows 觸控手勢（當其正在執行時），並在畫面上以黑色空心矩形為中心](images/mtgesturescs.png)

在此範例中，會將手勢訊息傳遞至手勢引擎，然後呼叫繪圖物件上的方法，以轉譯、旋轉和縮放具有處理這些命令之方法的物件。 若要在 c # 中這麼做，會建立特殊形式 TouchableForm 來處理手勢訊息。 然後，此表單會使用訊息來變更繪圖物件（DrawingObject），以變更物件在小畫家方法中的呈現方式。

若要協助示範範例的運作方式，請考慮使用平移命令轉譯轉譯方塊的步驟。 使用者執行平移手勢，此動作會產生具有手勢識別碼 GID_PAN 的 [**WM_GESTURE**](wm-gesture.md) 訊息。 TouchableForm 會處理此訊息並更新繪圖物件的位置，然後物件會轉譯成本身的轉譯。

下列程式碼示範軌跡處理常式如何從 [**WM_GESTURE**](wm-gesture.md) 訊息抓取參數，然後透過呼叫繪圖物件的 move 方法，在轉譯的方塊上執行轉譯。

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

下列程式碼顯示繪圖物件的 move 方法如何更新內部位置變數。

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

下列程式碼顯示如何在繪圖物件的 paint 方法中使用位置。

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

平移手勢將會轉譯已轉譯的繪圖方塊。

## <a name="related-topics"></a>相關主題

[多點觸控手勢應用程式 (c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)、[多點觸控手勢應用程式 (c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp)、 [Windows Touch 範例](windows-touch-samples.md)
