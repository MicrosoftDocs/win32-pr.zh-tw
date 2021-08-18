---
title: 繪製視窗
description: 您已建立您的視窗。 現在您想要在其中顯示某個東西。 在 Windows 術語中，這稱為繪製視窗。 為了混合使用，視窗是空白畫布，等候您填滿。
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: 93d0cb0234975b61ee7ffc05a680b5e1e6b1e01b9d4de7235fc4239ec5573f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896998"
---
# <a name="painting-the-window"></a>繪製視窗

您已建立您的視窗。 現在您想要在其中顯示某個東西。 在 Windows 術語中，這稱為繪製視窗。 為了混合使用，視窗是空白畫布，等候您填滿。

有時候您的程式會起始繪製，以更新視窗的外觀。 在其他情況下，作業系統會通知您必須重新繪製視窗的一部分。 發生這種情況時，作業系統會傳送 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息給視窗。 必須繪製之視窗的部分稱為「 *更新區域*」。

第一次顯示視窗時，必須繪製視窗的整個工作區。 因此，當您顯示視窗時，一律會收到至少一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息。

![顯示視窗更新區域的圖例](images/painting01.png)

您只需負責繪製工作區。 周圍的框架（包括標題列）會自動由作業系統繪製。 在您完成工作區的繪製之後，請清除更新區域，這會告知作業系統不需要傳送另一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，直到發生變更為止。

現在假設使用者移動另一個視窗，使其遮蔽視窗的一部分。 當遮蔽部分再次變成可見時，該部分會新增至更新區域，而您的視窗會收到另一個 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息。

![圖例顯示當兩個 windows 重迭時，更新區域的變更方式](images/painting02.png)

如果使用者將視窗伸展，更新區域也會變更。 在下圖中，使用者將視窗向右延伸。 視窗右邊的新公開區域會新增至更新區域：

![圖例顯示調整大小視窗時更新區域的變更方式](images/painting03.png)

在我們的第一個範例程式中，繪製常式非常簡單。 它只會以純色填滿整個工作區。 同樣地，此範例也足以示範一些重要的概念。

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

藉由呼叫 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 函數來啟動繪製作業。 此函式會在 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構中填入重新繪製要求的資訊。 目前的更新區域是在 **PAINTSTRUCT** 的 **rcPaint** 成員中提供。 此更新區域的定義是相對於工作區：

![顯示工作區來源的圖例](images/painting04.png)

在您的繪圖程式碼中，您有兩個基本選項：

- 無論更新區域的大小為何，小畫家整個工作區。 任何落在更新區域以外的地方都會裁剪。 也就是說，作業系統會忽略它。
- 藉由只繪製更新區域內視窗的部分來優化。

如果您一律繪製整個工作區，則程式碼會比較簡單。 但是，如果您有複雜的繪製邏輯，則略過更新區域以外的區域可能更有效率。

下列程式程式碼使用系統定義的視窗背景色彩 (**色彩 \_ 視窗**) ，以單一色彩填滿更新區域。 **色彩 \_ 視窗** 所指出的實際色彩取決於使用者目前的色彩配置。

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

在此範例中， [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) 的詳細資料並不重要，但第二個參數會提供矩形的座標來填滿。 在此情況下，我們會將整個更新區域傳入 ([**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)) 的 **rcPaint** 成員。 在第一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息上，必須繪製整個工作區，因此 **rcPaint** 將包含整個工作區。 在後續的 **WM \_ 油漆** 訊息上， **rcPaint** 可能會包含較小的矩形。

[**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect)函式是圖形裝置介面 (GDI) 的一部分，而這種的驅動 Windows 圖形很長一段時間。 在 Windows 7 中，Microsoft 引進了新的圖形引擎（名為 Direct2D），可支援高效能圖形作業，例如硬體加速。 Direct2D 也可透過適用于[Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-overview.md)，以及透過 Windows Server 2008 的平臺更新 Windows Server 2008 來 Windows Vista。 仍完全支援 (GDI。 ) 

完成繪製之後，請呼叫 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 函數。 此函式會清除更新區域，以通知 Windows 視窗已完成繪圖本身。

## <a name="next"></a>下一個

[關閉視窗](closing-the-window.md)