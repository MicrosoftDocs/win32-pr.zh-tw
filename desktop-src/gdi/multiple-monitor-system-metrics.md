---
description: GetSystemMetrics 函式會傳回主要監視的值，但 SM \_ CXMAXTRACK 和 sm \_ CYMAXTRACK 除外，其指的是整個桌面。
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: 多個監視系統計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114640"
---
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="bc409-103">多個監視系統計量</span><span class="sxs-lookup"><span data-stu-id="bc409-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="bc409-104">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式會傳回主要監視的值，但 sm \_ CXMAXTRACK 和 sm \_ CYMAXTRACK 除外，其指的是整個桌面。</span><span class="sxs-lookup"><span data-stu-id="bc409-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="bc409-105">以下是所有設備磁碟機的計量： SM \_ CXCURSOR、sm \_ CYCURSOR、sm \_ CXICON、SMCYICON。</span><span class="sxs-lookup"><span data-stu-id="bc409-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="bc409-106">以下顯示功能對所有監視器都相同： LOGPIXELSX、LOGPIXELSY、DESTOPHORZRES、DESKTOPVERTRES。</span><span class="sxs-lookup"><span data-stu-id="bc409-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="bc409-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 也有僅參考多重監視系統的常數。</span><span class="sxs-lookup"><span data-stu-id="bc409-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="bc409-108">SM \_ XVIRTUALSCREEN 和 sm \_ YVIRTUALSCREEN 識別虛擬畫面的左上角、sm \_ CXVIRTUALSCREEN 和 SM \_ CYVIRTUALSCREEN 是虛擬螢幕的垂直和水準測量、sm \_ CMONITORS 是連接到桌面的監視器數目，而 sm SAMEDISPLAYFORMAT 則會 \_ 指出桌面上的所有監視器是否都有相同的色彩格式。</span><span class="sxs-lookup"><span data-stu-id="bc409-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="bc409-109">若要取得單一顯示器監視器或桌面上所有顯示監視器的相關資訊，請使用 EnumDisplayMonitors。</span><span class="sxs-lookup"><span data-stu-id="bc409-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="bc409-110">[**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect)或 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect)所傳回之桌面視窗的矩形一律等於主要監視器的矩形，以與現有的應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="bc409-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="bc409-111">因此，</span><span class="sxs-lookup"><span data-stu-id="bc409-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="bc409-112">將會是：</span><span class="sxs-lookup"><span data-stu-id="bc409-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="bc409-113">若要變更監視器的工作區域，請使用 [](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) SPI \_ SETWORKAREA 和 *pvParam* 指向所需監視器上的 [**RECT**](/previous-versions//dd162897(v=vs.85))結構來呼叫 SystemParametersInfo。</span><span class="sxs-lookup"><span data-stu-id="bc409-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="bc409-114">如果 *pvParam* 為 **Null**，則會修改主要監視器的工作區。</span><span class="sxs-lookup"><span data-stu-id="bc409-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="bc409-115">使用 SPI \_ GETWORKAREA 一律會傳回主要監視器的工作區。</span><span class="sxs-lookup"><span data-stu-id="bc409-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="bc409-116">若要取得主要監視器以外監視的工作區域，請呼叫 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)。</span><span class="sxs-lookup"><span data-stu-id="bc409-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
