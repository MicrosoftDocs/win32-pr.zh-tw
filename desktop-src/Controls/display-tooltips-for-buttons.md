---
title: 如何顯示按鈕的工具提示
description: 當您指定 TBSTYLE \_ 工具提示樣式時，工具列會建立和管理工具提示控制項。 工具提示控制項是隱藏的，只有在使用者將指標移到工具列按鈕上方，並將其保留大約一秒時才會出現。
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841991"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="891b3-104">如何顯示按鈕的工具提示</span><span class="sxs-lookup"><span data-stu-id="891b3-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="891b3-105">當您指定 [**TBSTYLE \_ 工具提示**](toolbar-control-and-button-styles.md) 樣式時，工具列會建立和管理工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="891b3-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="891b3-106">工具提示控制項是隱藏的，只有在使用者將指標移到工具列按鈕上方，並將其保留大約一秒時才會出現。</span><span class="sxs-lookup"><span data-stu-id="891b3-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="891b3-107">您的應用程式可以下列任何一種方式，將文字提供給工具提示控制項：</span><span class="sxs-lookup"><span data-stu-id="891b3-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="891b3-108">將工具提示文字設定為每個按鈕之 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iString** 成員。</span><span class="sxs-lookup"><span data-stu-id="891b3-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="891b3-109">您也必須傳送 [**TB 的 \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) 訊息，並將文字資料列的最大值設為0，讓文字不會顯示為按鈕標籤，而不會顯示為工具提示。</span><span class="sxs-lookup"><span data-stu-id="891b3-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="891b3-110">使用 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式建立工具列，然後設定 [**TBSTYLE \_ EX \_ MIXEDBUTTONS**](toolbar-extended-styles.md) 延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="891b3-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="891b3-111">標籤只會針對具有 [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) 樣式的按鈕顯示。</span><span class="sxs-lookup"><span data-stu-id="891b3-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="891b3-112">針對沒有此樣式的按鈕，會顯示包含按鈕文字的工具提示。</span><span class="sxs-lookup"><span data-stu-id="891b3-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="891b3-113">回應 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="891b3-114">回應 [TBN \_ GETINFOTIP](tbn-getinfotip.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="891b3-115">需要直接將訊息傳送至工具提示控制項的應用程式，可以使用 [**TB \_ GETTOOLTIPS**](tb-gettooltips.md) 訊息來取得控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="891b3-116">應用程式可以使用 [**TB \_ SETTOOLTIPS**](tb-settooltips.md) 訊息來取代工具列的工具提示控制項與另一個工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="891b3-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="891b3-117">提供工具提示文字最有彈性的方式，就是以 [**WM \_ 通知**](wm-notify.md)訊息的形式，回應工具列控制項傳送給其父系的 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)或 [TBN \_ GETINFOTIP](tbn-getinfotip.md)通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="891b3-118">針對 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)， *lParam* 參數包含 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構的指標 (也定義為 **LPTOOLTIPTEXT**) ，以指定需要解說文字之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="891b3-119">此識別碼位於 **NMTTDISPINFO idFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="891b3-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="891b3-120">應用程式可以將解說文字複製到結構中、指定包含解說文字之字串的位址，或指定字串資源的實例控制碼和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="891b3-121">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="891b3-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="891b3-122">技術</span><span class="sxs-lookup"><span data-stu-id="891b3-122">Technologies</span></span>

-   [<span data-ttu-id="891b3-123">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="891b3-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="891b3-124">必要條件</span><span class="sxs-lookup"><span data-stu-id="891b3-124">Prerequisites</span></span>

-   <span data-ttu-id="891b3-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="891b3-125">C/C++</span></span>
-   <span data-ttu-id="891b3-126">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="891b3-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="891b3-127">指示</span><span class="sxs-lookup"><span data-stu-id="891b3-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="891b3-128">顯示按鈕的工具提示</span><span class="sxs-lookup"><span data-stu-id="891b3-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="891b3-129">下列範例程式碼會藉由提供資源識別碼的文字來處理 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 工具提示通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="891b3-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="891b3-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="891b3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="891b3-131">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="891b3-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="891b3-132">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="891b3-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




