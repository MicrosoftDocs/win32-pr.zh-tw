---
title: 滑鼠移動
description: 滑鼠移動
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106998557"
---
# <a name="mouse-movement"></a>滑鼠移動

當移動滑鼠時，Windows 會張貼 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。 根據預設， **WM \_ MOUSEMOVE** 會移至包含資料指標的視窗。 您可以藉由 *捕捉* 滑鼠（如下一節所述）來覆寫此行為。

[**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息包含的參數與滑鼠點擊的訊息相同。 *LParam* 的最低16位包含 x 座標，後面的16個位包含 y 座標。 使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，將座標從 *LPARAM* 解壓縮。 *WParam* 參數包含位 **or** of 旗標，表示另一個滑鼠按鍵的狀態以及 SHIFT 和 CTRL 鍵。 下列程式碼會從 *lParam* 取得滑鼠座標。


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



請記住，這些座標是以圖元為單位，而不是與裝置無關的圖元 (Dip) 。 稍後在本主題中，我們將探討在兩個單元之間轉換的程式碼。

如果資料指標的位置與視窗相對，則視窗也可以收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。 例如，如果游標位於視窗上，而使用者隱藏了視窗，即使滑鼠未移動，視窗仍會收到 **WM 的 \_ MOUSEMOVE** 訊息。 這種行為的結果之一，是在 **WM \_ MOUSEMOVE** 訊息之間的滑鼠座標可能不會變更。

## <a name="capturing-mouse-movement-outside-the-window"></a>在視窗外捕捉滑鼠移動

根據預設，如果滑鼠移動超過工作區邊緣，則視窗會停止接收 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。 但是針對某些作業，您可能需要在這個點之後追蹤滑鼠位置。 例如，繪圖程式可能會讓使用者將選取矩形拖曳到視窗邊緣以外的範圍，如下圖所示。

![滑鼠捕捉的圖例。](images/input01.png)

若要在視窗邊緣之後接收滑鼠移動訊息，請呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 函數。 呼叫此函式之後，只要使用者至少按住一個滑鼠按鍵，就會繼續收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，即使滑鼠移至視窗外也一樣。 [捕獲] 視窗必須是前景視窗，而且一次只能有一個視窗是 [捕獲] 視窗。 若要釋放滑鼠捕捉，請呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 函式。

您通常會以下列方式使用 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 和 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 。

1.  當使用者按下滑鼠左鍵時，請呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 來開始捕獲滑鼠。
2.  回應滑鼠移動的訊息。
3.  當使用者放開滑鼠左鍵時，請呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture)。

## <a name="example-drawing-circles"></a>範例：繪製圓形

讓我們藉由讓使用者使用滑鼠繪製圓形，來擴充 [模組 3](module-3---windows-graphics.md) 的圓形程式。 從 [Direct2D 圓形範例](direct2d-circle-sample.md) 程式開始。 我們將修改此範例中的程式碼，以新增簡單的繪圖。 首先，將新的成員變數新增至 `MainWindow` 類別。


```C++
    D2D1_POINT_2F           ptMouse;
```



當使用者拖曳滑鼠時，這個變數會儲存滑鼠下移的位置。 在此函式中 `MainWindow` ，初始化 *省略號* 和 *ptMouse* 變數。


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



移除方法的主體 `MainWindow::CalculateLayout` ; 此範例不需要它。


```C++
    void    CalculateLayout() { }
```



接下來，宣告左邊按鈕的訊息處理常式、向上左鍵和滑鼠移動訊息。


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



滑鼠座標是以實體圖元為單位，但 Direct2D 預期與裝置無關的圖元 (Dip) 。 若要正確處理高 DPI 設定，您必須將圖元座標轉譯為 Dip。 如需 DPI 的詳細討論，請參閱 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)。 下列程式碼顯示可將圖元轉換成 Dip 的 helper 類別。


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



`DPIScale::Initialize`在您建立 Direct2D factory 物件之後，于 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)處理常式中呼叫。


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



若要從滑鼠訊息的 Dip 中取得滑鼠座標，請執行下列動作：

1.  使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來取得圖元座標。 這些巨集定義于 WindowsX 中，因此請記得將該標頭包含在您的專案中。
2.  呼叫 `DPIScale::PixelsToDipsX` 並 `DPIScale::PixelsToDipsY` 將圖元轉換為 dip。

現在將訊息處理常式新增至您的視窗程式。


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



最後，執行訊息處理常式本身。

### <a name="left-button-down"></a>向下鍵向下按鈕

針對左側按鈕的訊息，請執行下列動作：

1.  呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 以開始捕獲滑鼠。
2.  將滑鼠按一下的位置儲存在 *ptMouse* 變數中。 這個位置會定義橢圓形周框方塊的左上角。
3.  重設橢圓形結構。
4.  呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)。 此函數會強制重新繪製視窗。


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>滑鼠移動

針對滑鼠移動訊息，檢查滑鼠左鍵是否已關閉。 如果是，請重新計算省略號，然後重新繪製視窗。 在 Direct2D 中，會以中心點和 x 和 y 半徑來定義橢圓形。 我們想要繪製一個橢圓形，使其符合滑鼠下點所定義的周框方塊 (*ptMouse*) 和目前的游標位置 (*x*， *y*) ，因此需要一點算術才能找出橢圓形的寬度、高度和位置。

下列程式碼會重新計算省略號，然後呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 來重新繪製視窗。

![顯示有 x 和 y 半徑之橢圓形的圖表。](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a>左方按鈕向上鍵

針對左側按鈕的訊息，只要呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 來釋放滑鼠捕捉。


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>下一個

[其他滑鼠操作](other-mouse-operations.md)

 

 