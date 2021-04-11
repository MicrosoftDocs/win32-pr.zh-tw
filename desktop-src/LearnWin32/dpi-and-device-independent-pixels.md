---
title: DPI 和 Device-Independent 圖元
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 深入瞭解： DPI 和 Device-Independent 圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852544"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI 和 Device-Independent 圖元

若要有效率地使用 Windows 圖形進行程式設計，您必須瞭解兩個相關概念：

-   每吋點數 (DPI)
-   與裝置無關的圖元 (Dip) 。

讓我們從 DPI 開始。 這將需要簡短繞道至印刷樣式。 在印刷樣式中，類型的大小是以稱為 *點* 的單位來測量。 一個點等於1/72 英寸。

<dl> 1 pt = 1/72 英寸  
</dl>

> [!Note]  
> 這是點的桌面發佈定義。 在過去，點的確切量值會不同。

 

例如，12點字型的設計目的是要容納在 1/6 " (12/72) 行文字中。 很明顯地，這並不表示字型中的每個字元都是「高度」1/6」。 事實上，某些字元的高度可能會高於1/6」。 例如，在許多字型中，字元Å的高度高於字型的名義高度。 若要正確地顯示，字型在文字之間需要一些額外的空間。 這個空間稱為「 *前置*」。

下圖顯示72點字型。 實線會在文字周圍顯示1個高度周框方塊。 虛線稱為 *基準*。 字型中的大部分字元都是在基準上的其餘部分。 字型的高度包括基準之上的部分 (*上升* 的) ，以及高於基準的部分 (*下降*) 。 在這裡顯示的字型中，上升是56點，下降則是16點。

![顯示72點字型的圖例。](images/graphics11.png)

不過，在電腦顯示時，測量文字大小會有問題，因為圖元的大小不是相同的。 圖元的大小取決於兩個因素：顯示解析度，以及監視的實體大小。 因此，實體英寸不是有用的量值，因為實體的圖元與圖元之間沒有固定的關聯性。 相反地，會以 *邏輯* 單元來測量字型。 72點字型的定義是一種邏輯英寸高度。 邏輯英寸接著會轉換成圖元。 多年來，Windows 使用了下列轉換：一個邏輯英寸等於96圖元。 使用此縮放比例，72點字型會轉譯為96圖元高。 12點字型的高度為16圖元。

<dl> 12點 = 12/72 邏輯英寸 = 1/6 邏輯英寸 = 96/6 圖元 = 16 圖元  
</dl>

此縮放比例描述為每英寸96點 (DPI) 。 「點」（term）是指從列印開始，其中會將筆墨的實體點放在紙張上。 對於電腦顯示而言，每個邏輯英寸應以96圖元為單位，但已停滯一詞。

因為實際的圖元大小有所差異，所以在一個監視器上可讀取的文字可能會在另一個監視器上太小。 此外，人們也會有不同的喜好設定，有些人偏好較大的文字。 基於這個理由，Windows 可讓使用者變更 DPI 設定。 例如，如果使用者將顯示器設定為 144 DPI，72-point 字型會是144圖元高。 標準 DPI 設定為 100% (96 DPI) 、125% (120 DPI) 和 150% (144 DPI) 。 使用者也可以套用自訂設定。 從 Windows 7 開始，DPI 是每個使用者的設定。

## <a name="dwm-scaling"></a>DWM 調整

如果程式不會考慮 DPI，則在高 DPI 設定上可能會有下列瑕疵：

-   裁剪的 UI 元素。
-   版面配置不正確。
-   圖元出點陣圖和圖示。
-   不正確的滑鼠座標，可能會影響點擊測試、拖放等等。

為了確保舊版程式在高 DPI 設定下運作，DWM 會執行有用的回復。 如果程式未標示為 DPI 感知，則 DWM 會調整整個 UI 以符合 DPI 設定。 例如，在 144 DPI，UI 是以150% 來調整，包括文字、圖形、控制項和視窗大小。 如果程式建立500×500視窗，此視窗實際上會顯示為750×750圖元，並據此調整視窗的內容。

此行為表示較舊的程式會在高 DPI 設定下「立即運作」。 不過，縮放比例也會產生稍微模糊的外觀，因為縮放是在視窗繪製之後套用。

## <a name="dpi-aware-applications"></a>DPI-Aware 應用程式

為了避免 DWM 調整，程式可以將本身標示為 DPI 感知。 這會告知 DWM 不要執行任何自動的 DPI 縮放比例。 所有新的應用程式都應該設計為 DPI 感知，因為 DPI 感知可改善較高 DPI 設定的 UI 外觀。

程式會透過應用程式資訊清單宣告本身的 DPI 感知。 *資訊清單* 只是描述 DLL 或應用程式的 XML 檔案。 資訊清單通常內嵌在可執行檔中，不過可以提供為個別的檔案。 資訊清單包含 DLL 相依性、要求的許可權層級，以及程式設計用途的 Windows 版本等資訊。

若要宣告您的程式為 DPI 感知，請在資訊清單中包含下列資訊。

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

此處所示的清單只是部分資訊清單，但 Visual Studio 連結器會自動為您產生資訊清單的其餘部分。 若要在專案中包含部分資訊清單，請在 Visual Studio 中執行下列步驟。

1.  在 [ **專案** ] 功能表上，按一下 [ **屬性**]。
2.  在左窗格中，依序展開 [設定 **屬性**]、[ **資訊清單工具**]，然後按一下 [ **輸入和輸出**]。
3.  在 [ **其他資訊清單** 檔案] 文字方塊中，輸入資訊清單檔案的名稱，然後按一下 **[確定]**。

將程式標示為 DPI 感知，就會告知 DWM 不要調整您的應用程式視窗。 現在，如果您建立500×500視窗，不論使用者的 DPI 設定為何，此視窗都會佔用500×500圖元。

## <a name="gdi-and-dpi"></a>GDI 和 DPI

GDI 繪圖是以圖元為單位。 這表示，如果您的程式標示為 DPI 感知，而且您要求 GDI 繪製200×100矩形，則產生的矩形將會是螢幕上的200圖元寬和100圖元高度。 不過，GDI 字型的大小會調整為目前的 DPI 設定。 換句話說，如果您建立72點字型，字型的大小會是96圖元（96 DPI），但144圖元為 144 DPI。 以下是使用 GDI 以 144 DPI 呈現的72點字型。

![顯示 gdi 中 DPI 字型縮放比例的圖表。](images/graphics12.png)

如果您的應用程式為 DPI 感知，而且您使用 GDI 進行繪製，請調整所有繪圖座標以符合 DPI。

## <a name="direct2d-and-dpi"></a>Direct2D 和 DPI

Direct2D 會自動執行調整以符合 DPI 設定。 在 Direct2D 中，座標是以與 *裝置無關的圖元為* 單位來測量， (dip) 。 DIP 定義為 *邏輯* 英寸的 1/計算1/96。 在 Direct2D 中，所有繪製作業都是在 Dip 中指定，然後調整為目前的 DPI 設定。



| DPI 設定 | DIP 大小    |
|-------------|-------------|
| 96          | 1 佹萺慒     |
| 120         | 1.25 圖元 |
| 144         | 1.5 圖元  |



 

例如，如果使用者的 DPI 設定為 144 DPI，而您要求 Direct2D 繪製200×100矩形，矩形將會是300×150實體圖元。 此外，DirectWrite 會以 Dip 量值來測量字型大小，而不是點。 若要建立12點字型，請指定 16 Dip (12 點 = 1/6 logical 英寸 = 96/6 Dip) 。 在螢幕上繪製文字時，Direct2D 會將 Dip 轉換為實體圖元。 此系統的優點是，不論目前的 DPI 設定為何，測量單位都一致以進行文字和繪圖。

有一點要注意：滑鼠和視窗座標仍然是以實體圖元為單位，而不是 Dip。 例如，如果您處理 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息，則會以實體圖元為單位提供滑鼠下位置。 若要在該位置繪製點，您必須將圖元座標轉換為 Dip。

## <a name="converting-physical-pixels-to-dips"></a>將實體圖元轉換成 Dip

從實體圖元轉換到 Dip 會使用下列公式。

<dl> Dip = 圖元/ (DPI/96.0)   
</dl>

若要取得 DPI 設定，請呼叫 [**ID2D1Factory：： GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法。 DPI 會以兩個浮點數（X 軸的值，一個是 y 軸）的形式傳回。 理論上，這些值可能會不同。 為每個軸計算個別的調整比例。


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



如果您不是使用 Direct2D，以下是取得 DPI 設定的替代方法：


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> 在 Windows 10 上，版本1903、  [**ID2D1Factory：： GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 已淘汰，建議為適用于 Windows Store 應用程式的 [**DisplayInformation：： LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) ，或適用于桌面應用程式的 [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) 。 如果您仍然想要使用它，請在 [**ID2D1Factory：： GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi)呼叫 [**#pragma 警告 (隱藏： 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) ，以隱藏編譯器錯誤訊息。 雖然不建議這麼做，但您可以使用 [**SetProcessDpiAwarenessCoNtext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext)，以程式設計的方式設定預設的 DPI 感知。 在您的進程中建立了一個 (HWND) 的視窗之後，就不再支援變更 DPI 感知模式。 如果您要以程式設計方式設定進程預設的 DPI 感知模式，您必須在建立任何 Hwnd 之前呼叫對應的 API。 如需詳細資訊，請參閱 [設定進程的預設 DPI 感知](../hidpi/setting-the-default-dpi-awareness-for-a-process.md)。

## <a name="resizing-the-render-target"></a>調整呈現目標的大小

如果視窗的大小變更，您必須調整轉譯目標的大小以符合。 在大多數情況下，您也需要更新配置並重新繪製視窗。 下列程式碼顯示這些步驟。


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



[**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)函式會取得工作區的新大小（以實體圖元為單位）， (不是 dip) 。 [**ID2D1HwndRenderTarget：： Resize**](../direct2d/id2d1hwndrendertarget-resize.md)方法會更新轉譯目標的大小，也會以圖元為單位來指定。 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)函式會藉由將整個工作區新增至視窗的更新區域，來強制重新繪製。  (在模組1中，請參閱 [繪製視窗](painting-the-window.md)。 ) 

當視窗增加或縮小時，您通常需要重新計算您繪製之物件的位置。 例如，在 circle 程式中，必須更新半徑和中心點：


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



[**ID2D1RenderTarget：： GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize)方法會以 dip 傳回轉譯目標的大小， (不是圖元) ，也就是計算版面配置的適當單位。 有一個密切相關的方法 [**ID2D1RenderTarget：： GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize)，會以實體圖元傳回大小。 針對 **HWND** 轉譯目標，此值會符合 [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)傳回的大小。 但是請記住，繪圖是以 Dip 而非圖元來執行。

## <a name="next"></a>下一個

[在 Direct2D 中使用色彩](using-color-in-direct2d.md)

 

 
