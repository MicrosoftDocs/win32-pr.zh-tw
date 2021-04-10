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
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="861d6-103">使用視覺效果樣式搭配自訂和 Owner-Drawn 控制項</span><span class="sxs-lookup"><span data-stu-id="861d6-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="861d6-104">本主題說明如何使用視覺化樣式 API，將視覺效果樣式套用至自訂控制項或主控描繪控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="861d6-105">使用視覺化樣式繪製控制項</span><span class="sxs-lookup"><span data-stu-id="861d6-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="861d6-106">回應主題變更</span><span class="sxs-lookup"><span data-stu-id="861d6-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="861d6-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="861d6-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="861d6-108">使用視覺化樣式繪製控制項</span><span class="sxs-lookup"><span data-stu-id="861d6-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="861d6-109">ComCtrl32.dll 第6版和更新版本支援視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="861d6-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="861d6-110">如果您的應用程式設定為使用 ComCtrl32.dll 6 版（含）以後版本，而且如果系統上有該版本，則會自動將目前的視覺效果樣式套用至應用程式中的所有通用控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="861d6-111">不過，目前的視覺效果樣式不會自動套用至自訂控制項或主控描繪控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="861d6-112">您的應用程式必須包含可檢查視覺效果樣式是否可用的程式碼，如果有的話，則會使用視覺化樣式 API 將目前選取的視覺化樣式套用至您的自訂和主控描繪控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="861d6-113">若要檢查視覺樣式是否可用，請呼叫 [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) 函數。</span><span class="sxs-lookup"><span data-stu-id="861d6-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="861d6-114">如果無法使用視覺化樣式，請使用 [回復程式碼] 來繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="861d6-115">如果有視覺化樣式，您可以使用視覺效果樣式的函式（例如 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ）來呈現您的控制項。</span><span class="sxs-lookup"><span data-stu-id="861d6-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="861d6-116">請注意， [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) 可讓您自訂文字的外觀，並在修改其他字型時保留主題字型的某些屬性。</span><span class="sxs-lookup"><span data-stu-id="861d6-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="861d6-117">**若要以目前的視覺效果樣式繪製控制項**</span><span class="sxs-lookup"><span data-stu-id="861d6-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="861d6-118">呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)，傳遞您要套用視覺化樣式之控制項的 *hwnd* ，以及描述控制項類型的類別清單。</span><span class="sxs-lookup"><span data-stu-id="861d6-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="861d6-119">這些類別定義于 Vssym32 中。</span><span class="sxs-lookup"><span data-stu-id="861d6-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="861d6-120">**OpenThemeData** 會傳回 HTHEME 控制碼，但如果視覺效果樣式管理員已停用，或目前的視覺化樣式未提供特定控制項的特定資訊，則此函數會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="861d6-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="861d6-121">如果傳回值為 **Null**，則使用非視覺化樣式的繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="861d6-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="861d6-122">若要繪製控制項背景，請呼叫 [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) 或 [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex)。</span><span class="sxs-lookup"><span data-stu-id="861d6-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="861d6-123">若要判斷內容矩形的位置，請呼叫 [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)。</span><span class="sxs-lookup"><span data-stu-id="861d6-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="861d6-124">若要轉譯文字，請使用 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) 或 [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex)，並以 [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)所傳回之矩形上的座標作為基礎。</span><span class="sxs-lookup"><span data-stu-id="861d6-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="861d6-125">這些函式可以在主題的字型中，針對指定的控制群組件和狀態，或目前在裝置內容中選取的字型（ (DC) ）來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="861d6-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="861d6-126">當您的控制項收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息時，請呼叫 [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) 來釋放您呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)時所傳回的主題控制碼。</span><span class="sxs-lookup"><span data-stu-id="861d6-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="861d6-127">下列範例程式碼示範在目前的視覺化樣式中繪製按鈕控制項的一種方式。</span><span class="sxs-lookup"><span data-stu-id="861d6-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


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





<span data-ttu-id="861d6-128">下列範例程式碼位於子類別化按鈕控制項的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息處理常式中。</span><span class="sxs-lookup"><span data-stu-id="861d6-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="861d6-129">控制項的文字是以視覺化樣式字型繪製，但是根據控制項的狀態，會以應用程式為依據來定義色彩。</span><span class="sxs-lookup"><span data-stu-id="861d6-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


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



<span data-ttu-id="861d6-130">您可以使用其他控制項的元件，並個別呈現每個元件。</span><span class="sxs-lookup"><span data-stu-id="861d6-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="861d6-131">例如，針對包含方格的行事曆控制項，您可以將方格所組成的每個正方形視為工具列按鈕，方法是取得主題控制碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="861d6-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="861d6-132">您可以針對指定的控制項多次呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) ，並使用適當的主題控制碼來繪製不同的部分，藉以混合和比對控制群組件。</span><span class="sxs-lookup"><span data-stu-id="861d6-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="861d6-133">不過，在某些視覺效果樣式中，某些部分可能與其他元件不相容。</span><span class="sxs-lookup"><span data-stu-id="861d6-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="861d6-134">以現用視覺化樣式呈現控制項的另一個方法是使用系統色彩。</span><span class="sxs-lookup"><span data-stu-id="861d6-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="861d6-135">例如，您可以使用系統色彩來設定呼叫 [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) 函式時的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="861d6-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="861d6-136">套用視覺化樣式檔案時，會設定大部分的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="861d6-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="861d6-137">回應主題變更</span><span class="sxs-lookup"><span data-stu-id="861d6-137">Responding to Theme Changes</span></span>

<span data-ttu-id="861d6-138">當您的控制項收到 [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) 訊息，且持有主題的全域控點時，它應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="861d6-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="861d6-139">呼叫 [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) 以關閉現有的主題控制碼。</span><span class="sxs-lookup"><span data-stu-id="861d6-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="861d6-140">呼叫 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 以取得新載入視覺效果樣式的主題控制碼。</span><span class="sxs-lookup"><span data-stu-id="861d6-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="861d6-141">下列範例說明這兩個呼叫。</span><span class="sxs-lookup"><span data-stu-id="861d6-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="861d6-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="861d6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="861d6-143">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="861d6-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="861d6-144">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="861d6-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 