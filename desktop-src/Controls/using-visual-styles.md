---
title: 使用視覺效果樣式搭配自訂和 Owner-Drawn 控制項
description: 本主題說明如何使用視覺化樣式 API，將視覺效果樣式套用至自訂控制項或主控描繪控制項。
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093395"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>使用視覺效果樣式搭配自訂和 Owner-Drawn 控制項

本主題說明如何使用視覺化樣式 API，將視覺效果樣式套用至自訂控制項或主控描繪控制項。

-   [使用視覺化樣式繪製控制項](#drawing-controls-with-visual-styles)
-   [回應主題變更](#responding-to-theme-changes)
-   [相關主題](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>使用視覺化樣式繪製控制項

ComCtrl32.dll 第6版和更新版本支援視覺效果樣式。 如果您的應用程式設定為使用 ComCtrl32.dll 6 版（含）以後版本，而且如果系統上有該版本，則會自動將目前的視覺效果樣式套用至應用程式中的所有通用控制項。 不過，目前的視覺效果樣式不會自動套用至自訂控制項或主控描繪控制項。 您的應用程式必須包含可檢查視覺效果樣式是否可用的程式碼，如果有的話，則會使用視覺化樣式 API 將目前選取的視覺化樣式套用至您的自訂和主控描繪控制項。

若要檢查視覺樣式是否可用，請呼叫 [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) 函數。 如果無法使用視覺化樣式，請使用 [回復程式碼] 來繪製控制項。

如果有視覺化樣式，您可以使用視覺效果樣式的函式（例如 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ）來呈現您的控制項。 請注意， [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) 可讓您自訂文字的外觀，並在修改其他字型時保留主題字型的某些屬性。

**若要以目前的視覺效果樣式繪製控制項**

1.  呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)，傳遞您要套用視覺化樣式之控制項的 *hwnd* ，以及描述控制項類型的類別清單。 這些類別定義于 Vssym32 中。 **OpenThemeData** 會傳回 HTHEME 控制碼，但如果視覺效果樣式管理員已停用，或目前的視覺化樣式未提供特定控制項的特定資訊，則此函數會傳回 **Null**。 如果傳回值為 **Null**，則使用非視覺化樣式的繪圖函數。
2.  若要繪製控制項背景，請呼叫 [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) 或 [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex)。
3.  若要判斷內容矩形的位置，請呼叫 [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)。
4.  若要轉譯文字，請使用 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) 或 [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex)，並以 [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)所傳回之矩形上的座標作為基礎。 這些函式可以在主題的字型中，針對指定的控制群組件和狀態，或目前在裝置內容中選取的字型（ (DC) ）來呈現文字。
5.  當您的控制項收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息時，請呼叫 [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) 來釋放您呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)時所傳回的主題控制碼。

下列範例程式碼示範在目前的視覺化樣式中繪製按鈕控制項的一種方式。


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





下列範例程式碼位於子類別化按鈕控制項的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息處理常式中。 控制項的文字是以視覺化樣式字型繪製，但是根據控制項的狀態，會以應用程式為依據來定義色彩。


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



您可以使用其他控制項的元件，並個別呈現每個元件。 例如，針對包含方格的行事曆控制項，您可以將方格所組成的每個正方形視為工具列按鈕，方法是取得主題控制碼，如下所示：


```C++
OpenThemeData(hwnd, L"Toolbar");
```



您可以針對指定的控制項多次呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) ，並使用適當的主題控制碼來繪製不同的部分，藉以混合和比對控制群組件。 不過，在某些視覺效果樣式中，某些部分可能與其他元件不相容。

以現用視覺化樣式呈現控制項的另一個方法是使用系統色彩。 例如，您可以使用系統色彩來設定呼叫 [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) 函式時的文字色彩。 套用視覺化樣式檔案時，會設定大部分的系統色彩。

## <a name="responding-to-theme-changes"></a>回應主題變更

當您的控制項收到 [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) 訊息，且持有主題的全域控點時，它應該執行下列作業：

-   呼叫 [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) 以關閉現有的主題控制碼。
-   呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 以取得新載入視覺效果樣式的主題控制碼。

下列範例說明這兩個呼叫。


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用視覺化樣式](cookbook-overview.md)
</dt> <dt>

[視覺化樣式](themes-overview.md)
</dt> </dl>

 

 