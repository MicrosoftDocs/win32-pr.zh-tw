---
title: 啟用及控制 DWM 組合
description: 桌面視窗管理員 (DWM) 撰寫 Api 提供數個函式，可用來設定及查詢 DWM 所使用的基本資訊。
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- 桌面視窗管理員 (DWM) ，組合
- DWM (桌面視窗管理員) ，組合
- 組合
- 桌面電腦群組合
- 著色
- 非用戶端區域呈現
- 桌面視窗管理員 (DWM) 、顏色標示
- DWM (桌面視窗管理員) 、顏色標示
- 桌面視窗管理員 (DWM) 、非用戶端區域呈現
- DWM (桌面視窗管理員) 、非用戶端區域呈現
- 桌面視窗管理員 (DWM) 、訊息
- DWM (桌面視窗管理員) ，訊息
- 傳訊
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: e8c5df1778436e2cfe23df85483453b01fb80884adc9a6d8ff34955deb3e0c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741578"
---
# <a name="enable-and-control-dwm-composition"></a>啟用及控制 DWM 組合

桌面視窗管理員 (DWM) 撰寫 Api 提供數個函式，可用來設定及查詢 DWM 所使用的基本資訊。 這些 Api 可讓您查詢及變更撰寫狀態。 此外，您可以針對不同的 DWM 視窗屬性，設定和查詢轉譯原則。

## <a name="retrieving-colorization-information"></a>正在抓取顏色標示資訊

視窗的非用戶端區域色彩是由目前的系統色彩主題所決定。 顏色標示值是透過 DWM Api 提供，可讓您的應用程式比對用戶端 UI 與系統色彩主題。

若要存取這個顏色標示值並監視色彩變更，請使用 [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) 函式和 [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) 訊息。

這個範例示範如何處理色彩變更的訊息，以及如何存取新的色彩。

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>控制非用戶端區域呈現

DWM 啟用的兩項視覺效果，是視窗的非用戶端區域的透明度，以及轉換效果。 您的應用程式可能必須基於樣式或相容性的理由，停用或重新啟用這些效果。 下列函式可用來管理透明度和轉換效果的行為。

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

若要取得應用程式視窗的目前非用戶端轉譯狀態，請呼叫 [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) ，並將 *dwAttribute* 設定為 [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)。 您可以從 [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)的檔中看到，當您將該旗標傳遞給 **DwmGetWindowAttribute** 時，所抓取的屬性值為 **BOOL** 類型。 不同的旗標會使 **DwmGetWindowAttribute** 傳回不同類型的值。 以下是程式碼範例。

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

下一個範例示範如何搭配使用 [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) 旗標與 **DwmGetWindowAttribute** ，以抓取視窗的擴充框架界限矩形。 該旗標的檔告訴我們，所抓取的屬性值是 **RECT** 型別。

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> 當您使用不同屬性的旗標呼叫 [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) 時，請遵循上面所示的相同程式設計模式。 [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)列舉主題指出每個旗標的資料列中，您應該在 **DwmGetWindowAttribute** 的 *pvAttribute* 參數中傳遞指標的數值型別。 *CbAttribute* 參數包含該物件的大小（以位元組為單位）。

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) 可讓您的應用程式設定非工作區呈現原則。 該函式也會決定您的應用程式應該如何處理 DWM 轉換效果。

下一個範例會停用非工作區呈現。 這會導致任何先前對 [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) 或 [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 的呼叫停用。

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

除了控制非工作區呈現之外， [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) 還可以控制 DWM 轉換效果。 您可以使用 **DWMWA \_ 轉換 \_ FORCEDISABLED** 做為 *dwAttribute* 參數來設定轉換行為。

## <a name="messages"></a>訊息

下列訊息提供 DWM 事件的通知。 這些訊息可以用來監視變更，例如撰寫狀態變更和系統色彩主題變更。

- [**WM \_ DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ DWMCOMPOSITIONCHANGED**](wm-dwmcompositionchanged.md)
- [**WM \_ DWMNCRENDERINGCHANGED**](wm-dwmncrenderingchanged.md)
- [**WM \_ DWMWINDOWMAXIMIZEDCHANGE**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows-7-and-earlier"></a>停用 DWM 組合 (Windows 7 及更早版本) 

> [!WARNING]
> 本節中的資訊僅適用于 Windows 7 和舊版系統。

因為 DWM 會使用圖形處理器 (GPU) 進行桌面撰寫，所以您的應用程式可能必須停用 DWM 以提供相容性。 完全控制桌面的應用程式（例如在全螢幕模式中執行的遊戲）必須判斷 DWM 是否已啟用，如果是，則會將它停用。 若要這樣做，需要兩個函數。

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

將 *fEnable* 設定為 **dwm \_ ec \_ DISABLECOMPOSITION** 的 [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)呼叫會停用 DWM 組合，直到呼叫進程關閉為止，或藉由呼叫 **DwmEnableComposition** （將 *fEnable* 設定為 **DWM \_ EC \_ ENABLECOMPOSITION**）來重新啟用組合。 當所有已停用組合的應用程式都已關閉，或藉由呼叫 **DwmEnableComposition** 手動重新啟用組合時，DWM 組合就會自動重新開機。

> [!NOTE]  
> 當應用程式嘗試直接繪製至主顯示器介面時，DWM 會自動停用組合。 在該應用程式放開主要裝置介面之前，將會停用組合。
