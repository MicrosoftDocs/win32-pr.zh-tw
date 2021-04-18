---
title: 放大 API 總覽
description: 本主題說明放大 API，並說明如何在應用程式中使用它。
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- 放大
- 螢幕縮放比例的應用程式
- 放大
- 自訂影像處理
- Magnification.dll
- 建立放大鏡控制項
- 選擇性放大
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966042"
---
# <a name="magnification-api-overview"></a>放大 API 總覽

放大 API 可讓輔助技術廠商開發在 Microsoft Windows 上執行的螢幕縮放應用程式。 本主題說明放大 API，並說明如何在應用程式中使用它。 它包含下列區段：

- [快速入門](#getting-started)
- [基本概念](#basic-concepts)
  - [放大鏡的類型](#types-of-magnifiers)
  - [放大因數](#magnification-factor)
  - [色彩效果](#color-effects)
  - [來源矩形](#source-rectangle)
  - [篩選清單](#filter-list)
  - [輸入轉換](#input-transform)
  - [系統資料指標](#system-cursor)
- [初始化放大鏡執行時間程式庫](#initializing-the-magnifier-run-time-library)
- [使用 Full-Screen 放大鏡](#using-the-full-screen-magnifier)
- [使用放大鏡控制項](#using-the-magnifier-control)
  - [建立放大鏡控制項](#creating-the-magnifier-control)
  - [初始化控制項](#initializing-the-control)
  - [設定來源矩形](#setting-the-source-rectangle)
  - [套用色彩效果](#applying-color-effects)
  - [選擇性放大](#selective-magnification)
- [相關主題](#related-topics)

## <a name="getting-started"></a>開始使用

Windows Vista 和更新版本的作業系統支援放大 API 的原始版本。 在 Windows 8 和更新版本上，API 支援其他功能，包括全螢幕縮放比例，以及設定放大的系統游標可見度。

放大 API 的支援是由 Magnification.dll 提供。 若要編譯您的應用程式，請包含放大和連結至放大程式庫。

> [!Note]  
> 在 WOW64 下不支援放大 API;也就是說，32位的放大鏡應用程式將無法在64位 Windows 上正確執行。

## <a name="basic-concepts"></a>基本概念

本節說明放大 API 所依據的基本概念。 其中包含下列部分：

- [放大鏡的類型](#types-of-magnifiers)
- [放大因數](#magnification-factor)
- [色彩效果](#color-effects)
- [來源矩形](#source-rectangle)
- [篩選清單](#filter-list)
- [輸入轉換](#input-transform)
- [系統資料指標](#system-cursor)

### <a name="types-of-magnifiers"></a>放大鏡的類型

此 API 支援兩種類型的放大鏡，也就是 *全螢幕放大鏡* 和 *放大鏡控制項*。 全螢幕放大鏡會放大整個畫面的內容，而放大鏡控制項會放大螢幕上特定區域的內容，並在視窗中顯示內容。 針對這兩種放大鏡，影像和文字都會放大，而且兩者都可讓您控制縮放量。 您也可以將色彩效果套用至放大的螢幕內容，以便更輕鬆地查看具有色彩缺陷的人員，或需要色彩有更多或更少對比的人員。

> [!Important]  
> 放大鏡控制項 API 適用于 Windows Vista 和更新版本的作業系統，而全螢幕放大鏡 API 僅適用于 Windows 8 和更新版本的作業系統。

### <a name="magnification-factor"></a>放大因數

全螢幕放大鏡和放大鏡控制項都套用縮放轉換來放大螢幕內容。 調整規模轉換所套用的放大量稱為「 *縮放比例因數*」。 它是以浮點數表示，其中1.0 對應到無縮放比例，而較大的值則會產生相對應的放大量。 例如，值為1.5 時，會放大螢幕內容50%。 小於1.0 的放大因數無效。

### <a name="color-effects"></a>色彩效果

色彩效果的達成方式是將5到5的色彩轉換矩陣套用至放大螢幕內容的色彩。 矩陣會決定內容之紅色、藍色、綠色和 Alpha 元件的濃度。 如需詳細資訊，請參閱在 Windows GDI + 檔中 [使用色彩矩陣轉換單一色彩](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) 。

### <a name="source-rectangle"></a>來源矩形

全螢幕放大鏡會將縮放轉換和色彩轉換套用至整個畫面。 另一方面，放大鏡控制項會將螢幕的區域（稱為 *來源矩形*）複製到螢幕點陣圖。 接下來，控制項會將縮放轉換和色彩轉換（如果有的話）套用至非螢幕點陣圖。 最後，控制項會在 [放大鏡控制] 視窗中顯示縮放和色彩轉換的點陣圖。

### <a name="filter-list"></a>篩選清單

根據預設，「放大鏡」控制項會放大指定來源矩形中的所有視窗。 不過，藉由提供視窗控制碼的 *篩選清單* ，您可以控制哪些視窗包含在放大的內容中，而不是。 如需詳細資訊，請參閱 [選擇性放大](#selective-magnification)。

全螢幕放大鏡不支援篩選清單;它一律會放大螢幕上的所有視窗。

### <a name="input-transform"></a>輸入轉換

一般來說，使用者畫筆或觸控輸入的放大螢幕內容會「隱藏」。 例如，如果使用者按下控制項的放大影像，則系統不一定會將輸入傳遞給控制項。 相反地，如果有任何) 位於 unmagnified 桌面上的點擊螢幕座標，系統就會將輸入傳遞到 (的任何專案。 [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)函式可讓您指定 *輸入轉換*，將放大螢幕內容的座標空間對應到實際的 (unmagnified) 螢幕座標空間。 這可讓系統將在放大螢幕內容中輸入的畫筆或觸控輸入，傳遞至畫面上正確的 UI 元素。

> [!Note]  
> 呼叫進程必須具有 UIAccess 許可權才能設定輸入轉換。 如需詳細資訊，請參閱 [消費者介面自動化安全性考慮](../uiauto-securityoverview.md) 和 [/MANIFESTUAC (在資訊清單) 中內嵌 UAC 資訊 ](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest)。

### <a name="system-cursor"></a>系統資料指標

[**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)函數可讓您顯示或隱藏系統資料指標。 如果您在全螢幕放大鏡為使用中時顯示系統游標，系統游標一律會與其余的螢幕內容一同放大。 如果您在全螢幕放大鏡處於作用中狀態時隱藏系統游標，則完全不會顯示系統游標。

使用 [放大鏡] 控制項， [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) 函式會顯示或隱藏 unmagnified 系統資料指標，但不會影響放大的系統資料指標。 放大的系統游標可見度取決於放大鏡控制項是否有 [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) 樣式。 如果有此樣式，則每當系統游標進入來源矩形時，[放大鏡] 控制項就會顯示放大的系統游標以及放大的螢幕內容。

## <a name="initializing-the-magnifier-run-time-library"></a>初始化放大鏡執行時間程式庫

您必須藉由呼叫 [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) 函式來建立並初始化放大鏡執行時間物件，才能呼叫任何其他放大鏡 API 函式。 同樣地，在您完成使用放大鏡 API 之後，請呼叫 [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) 函式來終結放大鏡執行時間物件，並釋放相關聯的系統資源。

## <a name="using-the-full-screen-magnifier"></a>使用 Full-Screen 放大鏡

若要使用全螢幕放大鏡，請呼叫 [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) 函式。 *MagLevel* 參數會指定放大因數。 *XOffset* 和 *yOffset* 參數指定放大的螢幕內容相對於螢幕的放置方式。

螢幕內容放大時，會變得大於螢幕本身。 部分內容會延伸到超出螢幕邊緣，並對使用者變得看不見。 [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)函式的 *xOffset* 和 *yOffset* 參數會決定螢幕上會顯示放大螢幕內容的哪一部分。 參數會一起指定 unmagnified 螢幕內容中某個點的座標。 當內容放大時，會將指定的點放置在螢幕的左上角。

下列範例會設定全螢幕放大鏡的縮放因數，並將放大的螢幕內容置中放在螢幕的中央。

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

您可以使用 [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) 函式，藉由設定應用程式定義的色彩轉換矩陣，將色彩效果套用至全螢幕內容。 例如，下列範例會設定將色彩轉換成灰階的色彩轉換矩陣。

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

您可以藉由呼叫 [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) 函式來取得目前的放大因數和位移值。 您可以藉由呼叫 [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) 函數來取出目前的色彩轉換矩陣。

## <a name="using-the-magnifier-control"></a>使用放大鏡控制項

放大鏡控制項會放大螢幕上特定區域的內容，並在視窗中顯示內容。 本節說明如何使用 [放大鏡] 控制項。 其中包含下列部分：

- [建立放大鏡控制項](#creating-the-magnifier-control)
- [初始化控制項](#initializing-the-control)
- [設定來源矩形](#setting-the-source-rectangle)
- [套用色彩效果](#applying-color-effects)
- [選擇性放大](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>建立放大鏡控制項

放大鏡控制項必須裝載在使用 [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) 擴充樣式建立的視窗中。 建立主視窗之後，呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 以設定主機視窗的不透明度。 主機視窗通常會設定為完全不透明，以防止顯示基礎螢幕內容。 下列範例示範如何將主機視窗設定為完全不透明：

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

如果您將 [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) 樣式套用至主機視窗，則會將滑鼠點擊動作傳遞至滑鼠游標位置的主機視窗後方的任何物件。 請注意，因為主視窗不會處理滑鼠點擊，使用者將無法使用滑鼠移動或調整縮放視窗的大小。

[放大鏡] 控制項視窗的視窗類別必須是 **WC_MAGNIFIER**。 如果您套用 [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) 樣式，[放大鏡] 控制項就會在放大的螢幕內容中包含系統游標，而且游標會與螢幕內容一起放大。

建立 [放大鏡] 控制項之後，請保留視窗控制碼，讓您可以將它傳遞至其他函式。

下列範例顯示如何建立放大鏡控制項。

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>初始化控制項

建立 [放大鏡] 控制項之後，您必須呼叫 [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) 函數來指定放大因數。 這只是指定矩陣

 (*n*、0.0、0.0) 

 (0.0、 *n*、0.0) 

 (0.0、0.0、1.0) 

其中 *n* 為放大因數。

下列範例顯示如何設定 [放大鏡] 控制項的放大因數。

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>設定來源矩形

當使用者將滑鼠游標移到螢幕周圍時，您的應用程式會呼叫 [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) 函式，以指定要放大的基礎螢幕部分。

下列範例函式會根據滑鼠位置和放大鏡視窗的尺寸除以放大因數) 來計算來源矩形的位置和維度 (，並據此設定來源矩形。 函式也會將主機視窗的工作區放在滑鼠位置。 此函式會依間隔呼叫，以更新放大視窗。

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>套用色彩效果

具有 [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) 樣式的放大鏡控制項會套用內建的色彩轉換矩陣，以反轉放大螢幕內容的色彩。 下圖顯示具有 **MS_INVERTCOLORS** 樣式的 [放大鏡] 控制項中的螢幕內容。

![具有反轉色彩之放大內容的螢幕擷取畫面](images/color-inversion.png)

[**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)函式可讓您設定應用程式定義的色彩轉換矩陣，以套用其他色彩效果。 例如，下列函式會設定將色彩轉換成灰階的色彩轉換矩陣。


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

如需色彩轉換如何運作的詳細資訊，請參閱在 GDI + 檔中 [使用色彩矩陣轉換單一色彩](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) 。

### <a name="selective-magnification"></a>選擇性放大

根據預設，縮放比例會套用至縮放視窗本身以外的所有視窗。 若要指定要放大的視窗，請呼叫 [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) 函數。 這個方法會採用要放大的 windows 清單，或是要從縮放比例排除的 windows 清單。

## <a name="related-topics"></a>相關主題

[放大 API](entry-magapi-sdk.md)