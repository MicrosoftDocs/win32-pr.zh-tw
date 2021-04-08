---
title: 如何執行追蹤工具提示
description: 追蹤工具提示會保持可見，直到應用程式明確關閉為止，並且可以動態地變更螢幕上的位置。 版本4.70 和更新版本的通用控制項都支援它們。
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021018"
---
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="47d29-104">如何執行追蹤工具提示</span><span class="sxs-lookup"><span data-stu-id="47d29-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="47d29-105">追蹤工具提示會保持可見，直到應用程式明確關閉為止，並且可以動態地變更螢幕上的位置。</span><span class="sxs-lookup"><span data-stu-id="47d29-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="47d29-106">[版本 4.70](common-control-versions.md)和更新版本的通用控制項都支援它們。</span><span class="sxs-lookup"><span data-stu-id="47d29-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="47d29-107">若要建立追蹤工具提示，請在傳送 \_ [**TTM \_ ADDTOOL**](ttm-addtool.md)訊息時，在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中包含 TTF TRACK 旗標。</span><span class="sxs-lookup"><span data-stu-id="47d29-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="47d29-108">您的應用程式必須以手動方式啟動 (顯示) ，並藉由傳送 [**TTM \_ TRACKACTI加值稅E**](ttm-trackactivate.md) 訊息來停用 (隱藏) 追蹤工具提示。</span><span class="sxs-lookup"><span data-stu-id="47d29-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="47d29-109">當追蹤工具提示為使用中時，您的應用程式必須將 [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) 訊息傳送至工具提示控制項，以指定工具提示的位置。</span><span class="sxs-lookup"><span data-stu-id="47d29-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="47d29-110">由於應用程式會處理工作（例如定位工具提示），因此追蹤工具提示不會使用 **TTF 子 \_ 類別** 旗標或 [**TTM \_ RELAYEVENT**](ttm-relayevent.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="47d29-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="47d29-111">[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)訊息會讓工具提示控制項使用兩個放置樣式的其中一個來顯示視窗：</span><span class="sxs-lookup"><span data-stu-id="47d29-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="47d29-112">根據預設，工具提示會顯示在控制項所選擇的位置中，對應工具的旁邊。</span><span class="sxs-lookup"><span data-stu-id="47d29-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="47d29-113">選擇的位置是相對於您使用此訊息所提供的座標。</span><span class="sxs-lookup"><span data-stu-id="47d29-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="47d29-114">如果您在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的成員中包含 **TTF \_ 絕對值**，則會在訊息中指定的圖元位置顯示工具提示。</span><span class="sxs-lookup"><span data-stu-id="47d29-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="47d29-115">在此情況下，控制項不會嘗試從您提供的座標變更工具提示視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="47d29-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="47d29-116">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="47d29-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="47d29-117">技術</span><span class="sxs-lookup"><span data-stu-id="47d29-117">Technologies</span></span>

-   [<span data-ttu-id="47d29-118">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="47d29-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="47d29-119">必要條件</span><span class="sxs-lookup"><span data-stu-id="47d29-119">Prerequisites</span></span>

-   <span data-ttu-id="47d29-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="47d29-120">C/C++</span></span>
-   <span data-ttu-id="47d29-121">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="47d29-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="47d29-122">指示</span><span class="sxs-lookup"><span data-stu-id="47d29-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="47d29-123">執行工具提示 In-Place</span><span class="sxs-lookup"><span data-stu-id="47d29-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="47d29-124">範例中所使用之 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **UFlags** 成員包含 **TTF \_ 絕對** 旗標。</span><span class="sxs-lookup"><span data-stu-id="47d29-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="47d29-125">如果沒有這個旗標，工具提示控制項會選擇要顯示工具提示的位置，而其相對於對話方塊的位置可能會隨著滑鼠指標移動而突然變更。</span><span class="sxs-lookup"><span data-stu-id="47d29-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="47d29-126">`g_toolItem` 是全域 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="47d29-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="47d29-127">下列範例示範如何建立追蹤工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="47d29-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="47d29-128">此範例會將主視窗的整個工作區指定為工具。</span><span class="sxs-lookup"><span data-stu-id="47d29-128">The example specifies the main window's entire client area as the tool.</span></span>


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a><span data-ttu-id="47d29-129">視窗程式執行</span><span class="sxs-lookup"><span data-stu-id="47d29-129">Window Procedure Implementation</span></span>

<span data-ttu-id="47d29-130">當滑鼠指標位於工作區時，工具提示會在作用中，並顯示游標座標，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="47d29-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![對話方塊的螢幕擷取畫面;工具提示會顯示滑鼠指標的 x 和 y 座標](images/tt-tracking.png)

<span data-ttu-id="47d29-132">下列範例程式碼來自對話方塊的視窗程式，此對話方塊會顯示在上述範例中建立的追蹤工具提示。</span><span class="sxs-lookup"><span data-stu-id="47d29-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="47d29-133">全域布林值變數 *g \_ TrackingMouse* 是用來判斷是否需要重新啟用工具提示和重設滑鼠追蹤，如此當滑鼠指標離開對話方塊的工作區時，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="47d29-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a><span data-ttu-id="47d29-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="47d29-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d29-135">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="47d29-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




