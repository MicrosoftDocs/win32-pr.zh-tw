---
title: 範例轉譯程式碼
description: 範例轉譯程式碼
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- 視覺效果，範例程式碼
- 自訂視覺效果，範例程式碼
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- Render 函式，範例程式碼
- 範例、視覺效果的轉譯函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51265191ba7fd8b5eb9e4b1140990a7713eba08356d01c58097c727ec2fe533e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569784"
---
# <a name="sample-render-code"></a>範例轉譯程式碼

以下是一些範例程式碼，它會使用 **Render** 函式在畫面上繪製線條。 直線的高度是由波形值所定義。


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



轉譯函式是程式 **代碼的主要** 工作發生的位置。 每次 Windows Media Player 取得音訊的快照時，它就會呼叫這個函式，而您的程式碼將會執行。

此程式碼會執行下列工作。 如需有關特定功能的詳細資訊，請參閱 Microsoft Windows Platform SDK for 32 位 Windows。

## <a name="creating-objects"></a>建立物件

通常您會使用 Microsoft Windows 圖形化顯示介面隨附的繪圖函式 (GDI) 。 您必須建立畫筆來繪製線條和筆刷以填滿區域。

建立實心的黑色筆刷以填滿背景。

建立實心畫筆來繪製線條。 色彩會是即將顯示視覺效果的面板所定義的前景色彩。

## <a name="adding-the-object-to-the-dc"></a>將物件新增至 DC

您必須將畫筆新增至裝置內容 (DC) 。 DC 是儲存所有繪圖資料和物件的記憶體部分。 基本上，DC 是視窗流量管理員，可讓您以圖形方式追蹤所有內容。

您需要 *轉換* 您所建立的畫筆物件，並將它儲存為舊的畫筆。 針對所有新的畫筆使用此編碼技術。 這是32位程式設計所需的技術。

## <a name="filling-in-the-background"></a>填滿背景

您現在已準備好進行繪製。 **FillRect** 函式會填滿視窗的矩形，如 **Render** 函式的參數所定義。 矩形會填入黑色筆刷。

## <a name="getting-audio-data"></a>取得音訊資料

接下來，程式碼會從 Windows Media Player 取得一些音訊資料。 藉由使用波形陣列，您可以在拍攝快照集時取得音訊電源的目前值。 在此情況下，您會取得左方頻道的音訊資料。 陣列中的第一個值是音訊電源快照的第一個1024th。

這項資訊會用來顯示高度將符合音訊電源快照集的行。

## <a name="draw-the-line"></a>劃清底線

這一行是使用 **MoveToEx** 和 **LineTo** GDI 函數，從左至右繪製。

首先，將畫筆移至起始點。 在此情況下，會使用 x 和 y 來定義使用者將在螢幕上看到的由左至右和由上到下的值。 X 是由中國的矩形所定義，特別是由 prc >左方的值所定義。 Y 會定義為該時間的波形資料值。

然後，您可以在視窗的另一端繪製線條。 您用來繪製線條的點也會是 x，y 值。 X 是由中國的矩形所定義，但這次由 prc >右邊。 Y 仍然是由波形資料定義，而且與您開始的點相同，因為您是從左至右繪製一條直線。

## <a name="clean-up-everything"></a>清除所有專案

您必須刪除您所建立的物件。 具體來說，您必須刪除您所建立的任何筆刷和畫筆。 當您完成使用畫筆和筆刷時，最好先將它們刪除。

如果您未在完成 **轉譯函數的** 執行之前將其刪除，您的視覺效果會在一分鐘內損毀。 您必須保留畫筆和筆刷的計數，並終結每一個筆刷。 請特別小心，不要在程式碼迴圈內建立畫筆。

使用範例中提供的程式碼撰寫技術來終結畫筆和筆刷。

-   **重要** 摧毀您的畫筆和筆刷！

當您完成清除時，請務必返回 \_ [確定]，讓 Windows Media Player 知道您已完成繪製。 一旦完成，您的繪圖就會傳送至視窗，將會取得另一個快照集，然後轉譯會要求您的程式碼再次 **繪製，依此類推** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行轉譯**](implementing-render.md)
</dt> </dl>

 

 




