---
description: GetSystemMetrics 函式會傳回主要監視的值，但 SM \_ CXMAXTRACK 和 sm \_ CYMAXTRACK 除外，其指的是整個桌面。
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: 多個監視系統計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3143562116561bb220bc6f0b5ecfa4ad8f5103c3e4532cab639c4c2b37f59467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037706"
---
# <a name="multiple-monitor-system-metrics"></a>多個監視系統計量

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式會傳回主要監視的值，但 sm \_ CXMAXTRACK 和 sm \_ CYMAXTRACK 除外，其指的是整個桌面。 以下是所有設備磁碟機的計量： SM \_ CXCURSOR、sm \_ CYCURSOR、sm \_ CXICON、SMCYICON。 以下顯示功能對所有監視器都相同： LOGPIXELSX、LOGPIXELSY、DESTOPHORZRES、DESKTOPVERTRES。

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 也有僅參考多重監視系統的常數。 SM \_ XVIRTUALSCREEN 和 sm \_ YVIRTUALSCREEN 識別虛擬畫面的左上角、sm \_ CXVIRTUALSCREEN 和 SM \_ CYVIRTUALSCREEN 是虛擬螢幕的垂直和水準測量、sm \_ CMONITORS 是連接到桌面的監視器數目，而 sm SAMEDISPLAYFORMAT 則會 \_ 指出桌面上的所有監視器是否都有相同的色彩格式。

若要取得單一顯示器監視器或桌面上所有顯示監視器的相關資訊，請使用 EnumDisplayMonitors。 [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect)或 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect)所傳回之桌面視窗的矩形一律等於主要監視器的矩形，以與現有的應用程式相容。 因此，


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



將會是：


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



若要變更監視器的工作區域，請使用 [](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) SPI \_ SETWORKAREA 和 *pvParam* 指向所需監視器上的 [**RECT**](/previous-versions//dd162897(v=vs.85))結構來呼叫 SystemParametersInfo。 如果 *pvParam* 為 **Null**，則會修改主要監視器的工作區。 使用 SPI \_ GETWORKAREA 一律會傳回主要監視器的工作區。 若要取得主要監視器以外監視的工作區域，請呼叫 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)。

 

 
