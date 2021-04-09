---
title: 平面捲軸
description: Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683147"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="df844-103">平面捲軸</span><span class="sxs-lookup"><span data-stu-id="df844-103">Flat Scroll Bars</span></span>

<span data-ttu-id="df844-104">Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。</span><span class="sxs-lookup"><span data-stu-id="df844-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="df844-105">功能上，一般捲軸的行為就像標準捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="df844-106">不同之處在于，您可以自訂其外觀，以比標準捲軸更大的範圍。</span><span class="sxs-lookup"><span data-stu-id="df844-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="df844-107">下圖顯示包含平面捲軸的視窗。</span><span class="sxs-lookup"><span data-stu-id="df844-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![包含平面捲軸之視窗的螢幕擷取畫面](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="df844-109">Comctl32.dll 版本4.71 至5.82 支援平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="df844-110">Comctl32.dll 6.00 版和更新版本不支援一般捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="df844-111">使用平面捲軸</span><span class="sxs-lookup"><span data-stu-id="df844-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="df844-112">本節說明如何在您的應用程式中執行平面捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="df844-113">開始之前</span><span class="sxs-lookup"><span data-stu-id="df844-113">Before You Begin</span></span>

<span data-ttu-id="df844-114">若要使用一般捲軸函式，您必須在原始程式檔中包含 Commctrl，並連結至 Comctl32.dll。</span><span class="sxs-lookup"><span data-stu-id="df844-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="df844-115">將平面捲軸加入至視窗</span><span class="sxs-lookup"><span data-stu-id="df844-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="df844-116">若要將一般捲軸加入至視窗，請呼叫 [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)，並將控制碼傳遞至視窗。</span><span class="sxs-lookup"><span data-stu-id="df844-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="df844-117">您必須使用對等的 FlatSB XXX 函式，而不是使用標準捲軸函數來操作捲軸 \_ 。</span><span class="sxs-lookup"><span data-stu-id="df844-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="df844-118">有一些一般捲軸函式，可用於設定和取出捲軸資訊、範圍和位置。</span><span class="sxs-lookup"><span data-stu-id="df844-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="df844-119">如果您的視窗尚未初始化一般捲軸，則一般捲軸 API 會延後至對應的標準函式（如果使用的話）。</span><span class="sxs-lookup"><span data-stu-id="df844-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="df844-120">這可讓您開啟和關閉平面捲軸，而不需要撰寫條件式程式碼。</span><span class="sxs-lookup"><span data-stu-id="df844-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="df844-121">由於應用程式可能已為其平面捲軸設定自訂計量，因此系統計量變更時不會自動更新。</span><span class="sxs-lookup"><span data-stu-id="df844-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="df844-122">當系統捲軸計量變更時，會廣播 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息，並將其 *wParam* 設定為 [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。</span><span class="sxs-lookup"><span data-stu-id="df844-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="df844-123">若要將一般捲軸更新為新的系統計量，應用程式必須處理這個訊息，並明確地變更一般捲軸的度量相依屬性。</span><span class="sxs-lookup"><span data-stu-id="df844-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="df844-124">若要更新您的捲軸屬性，請使用 [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop)。</span><span class="sxs-lookup"><span data-stu-id="df844-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="df844-125">下列程式碼片段會將一般捲軸的度量相依屬性變更為目前的系統值。</span><span class="sxs-lookup"><span data-stu-id="df844-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="df844-126">強化平面捲軸</span><span class="sxs-lookup"><span data-stu-id="df844-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="df844-127">[**FlatSB \_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) 可讓您修改一般捲軸，以自訂視窗的外觀。</span><span class="sxs-lookup"><span data-stu-id="df844-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="df844-128">若為垂直捲動條，您可以變更橫條的寬度和方向箭號的高度。</span><span class="sxs-lookup"><span data-stu-id="df844-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="df844-129">針對水準捲軸，您可以變更橫條的高度和方向箭號的寬度。</span><span class="sxs-lookup"><span data-stu-id="df844-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="df844-130">您也可以變更水準和垂直捲動條的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="df844-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="df844-131">[**FlatSB \_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) 也可讓您自訂如何顯示一般捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="df844-132">藉由變更 WSB \_ \_ 屬性 VSTYLE 和 wsb \_ \_ 屬性 HSTYLE 屬性，您可以設定要使用的捲軸類型。</span><span class="sxs-lookup"><span data-stu-id="df844-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="df844-133">有三種樣式可供使用。</span><span class="sxs-lookup"><span data-stu-id="df844-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df844-134">FSB \_ 百科全書 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="df844-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="df844-135">標準的平面捲軸隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="df844-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="df844-136">當滑鼠移到方向按鈕或 thumb 上方時，捲軸的那個部分會顯示在3-d 中。</span><span class="sxs-lookup"><span data-stu-id="df844-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="df844-137">前端匯流排 \_ 平面 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="df844-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="df844-138">標準的平面捲軸隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="df844-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="df844-139">當滑鼠移到方向按鈕或 thumb 上方時，捲軸的那個部分會以反轉色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="df844-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="df844-140">FSB \_ 一般 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="df844-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="df844-141">隨即顯示一般的 nonflat 捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="df844-142">不會套用任何特殊的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="df844-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="df844-143">移除一般捲軸</span><span class="sxs-lookup"><span data-stu-id="df844-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="df844-144">如果您想要從視窗中移除一般捲軸，請呼叫 [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) 函式，並將控制碼傳遞至視窗。</span><span class="sxs-lookup"><span data-stu-id="df844-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="df844-145">此函數只會在執行時間從視窗中移除一般捲軸。</span><span class="sxs-lookup"><span data-stu-id="df844-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="df844-146">當您的視窗損毀時，您不需要呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="df844-146">You do not need to call this function when your window is destroyed.</span></span>

 

 