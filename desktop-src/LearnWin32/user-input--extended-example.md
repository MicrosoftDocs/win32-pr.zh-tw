---
標題：使用者輸入擴充的範例描述：使用者輸入：擴充的範例 assetid： A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms。主題：文章 ms. 日期：05/31/2018
---

# <a name="user-input-extended-example"></a>使用者輸入：擴充的範例

讓我們結合已瞭解的使用者輸入內容，以建立簡單的繪圖程式。 以下是程式的螢幕擷取畫面：

![繪圖程式的螢幕擷取畫面](images/input03.png)

使用者可以使用數種不同的色彩來繪製省略號，然後選取、移動或刪除省略號。 為了讓 UI 保持簡單，程式不會讓使用者選取橢圓形色彩。 相反地，程式會自動迴圈顯示預先定義的色彩清單。 程式不支援省略號以外的任何圖形。 很明顯地，此計畫不會贏得任何對圖形軟體的獎勵。 不過，它仍然是從中學習的實用範例。 您可以從 [簡單的繪圖範例](simple-drawing-sample.md)下載完整的原始程式碼。 本節只會討論一些重點。

省略號是在程式中以包含橢圓形資料 ([**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) 和 color ([**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) 的結構來表示。 結構也會定義兩個方法：用來繪製橢圓形的方法，以及用來執行點擊測試的方法。


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



程式會使用相同的純色筆刷來繪製每個橢圓形的填滿和外框，並視需要變更色彩。 在 Direct2D 中，變更單色筆刷的色彩是有效率的作業。 因此，單色筆刷物件支援 [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) 方法。

省略號會儲存在 STL **清單** 容器中：


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **共用的 \_ ptr** 是在 TR1 中新增至 c + +，並在 c + + 0x 中正規化的智慧型指標類別。 Visual Studio 2010 新增對 **共用 \_ pt** r 和其他 C + + 0x 功能的支援。 如需詳細資訊，請參閱 *MSDN 雜誌* [Visual Studio 2010 中的探索新的 c + + 和 MFC 功能](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010)。  (此資源可能無法在某些語言及國家/地區使用。 ) 

 

此程式有三種模式：

-   繪圖模式。 使用者可以繪製新的省略號。
-   選取模式。 使用者可以選取省略號。
-   拖曳模式。 使用者可以拖曳選取的橢圓形。

使用者可以使用 [快速鍵對應表](accelerator-tables.md)中所述的相同鍵盤快速鍵，在繪製模式與選取模式之間切換。 在選取模式中，如果使用者按一下橢圓形，程式就會切換至拖曳模式。 當使用者放開滑鼠按鍵時，就會切換回選取模式。 目前的選取專案會儲存為省略號清單中的反覆運算器。 Helper 方法 `MainWindow::Selection` 會傳回所選橢圓形的指標，如果沒有選取範圍，則會傳回值 **nullptr** 。


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



下表摘要說明在三種模式中的滑鼠輸入效果。



| 滑鼠輸入      | 繪圖模式                                          | 選取模式                                                                                                                               | 拖曳模式                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| 向下鍵向下按鈕 | 設定滑鼠捕捉並開始繪製新的橢圓形。 | 釋放目前的選取範圍並執行點擊測試。 如果叫用省略號，請捕捉游標、選取省略號，然後切換至拖曳模式。 | 不進行動作。                 |
| 滑鼠移動       | 如果左按鈕已關閉，則調整橢圓形的大小。    | 不進行動作。                                                                                                                                   | 移動選取的橢圓形。 |
| 左方按鈕向上鍵   | 停止繪圖橢圓形。                          | 不進行動作。                                                                                                                                   | 切換至選取模式。  |



 

類別中的下列方法會 `MainWindow` 處理 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息。


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



滑鼠座標會以圖元傳遞給這個方法，然後轉換為 Dip。 請務必不要混淆這兩個單元。 例如， [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) 函式使用圖元，但繪製和點擊測試使用 dip。 一般規則是 windows 或滑鼠輸入的相關函式使用圖元，而 Direct2D 和 DirectWrite 則使用 Dip。 一律以高 DPI 設定測試程式，並記得將您的程式標示為 DPI 感知。 如需詳細資訊，請參閱 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)。

以下是處理 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息的程式碼。


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



先前的 [範例：繪製圓形](mouse-movement.md)中會說明調整橢圓形大小的邏輯。 也請注意 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)的呼叫。 這可確保重新繪製視窗。 下列程式碼會處理 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息。


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



如您所見，滑鼠輸入的訊息處理常式全都有分支程式碼，視目前的模式而定。 這是這個相當簡單程式的可接受設計。 但是，如果加入新的模式，它可能很快就會變得太複雜。 針對較大的程式， (MVC) 架構的模型視圖控制器可能是更好的設計。 在這種架構中，負責處理使用者輸入的 *控制器* 會與 *模型* 分開，以管理應用程式資料。

當程式切換模式時，游標會變更以將意見反應提供給使用者。


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



最後，請記得在視窗收到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息時設定游標：


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>總結

在本課程模組中，您已瞭解如何處理滑鼠和鍵盤輸入;如何定義鍵盤快速鍵;以及如何更新游標影像，以反映程式的目前狀態。

 

 
