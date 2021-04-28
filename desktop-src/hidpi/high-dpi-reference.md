---
title: 高 DPI 參考
description: 高 DPI 參考
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c10bcf5c5297b0adcfceef6853f2292c3fc8b98
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087796"
---
# <a name="high-dpi-reference"></a>高 DPI 參考

## <a name="functions"></a>函式



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **主題**                                                                                | **說明**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex)的變體，可傳回檔整為特定 DPI 的值。       |
| [**AreDpiAwarenessCoNtextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | 判斷兩個 [**DPI \_ 感知 \_ 內容**](dpi-awareness-context.md) 值是否相等。                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | 啟用自動調整指定最上層視窗的非工作區。                                                                               |
| [**GetAwarenessFromDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | 從 [**DPI \_ 感知 \_ 內容**](dpi-awareness-context.md)抓取 [**DPI \_ 感知**](/windows/desktop/api/windef/ne-windef-dpi_awareness)值                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | 查詢與監視器相關聯的 DPI 資訊。                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | 傳回系統 DPI。                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | 傳回指定之視窗的目前 DPI。                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | 抓取指定進程的 DPI 虛擬化模式。                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)的變體，可傳回檔整為特定 DPI 的值。         |
| [**GetThreadDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | 抓取目前線程的現用 DPI 感知內容。                                                                                                |
| [**GetWindowDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | 抓取視窗的 DPI 感知內容。                                                                                                                 |
| [**IsValidDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | 判斷 [**DPI \_ 感知 \_ 內容**](dpi-awareness-context.md) 是否有效，以及目前的系統是否支援。                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | 將視窗中的點從邏輯座標轉換為實體座標，而不考慮呼叫端的 DPI 感知。                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | 將視窗中的點從實體座標轉換為邏輯座標，不論呼叫端的 DPI 感知為何。                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | 設定目前進程的 DPI 虛擬化模式。                                                                                                         |
| [**SetThreadDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | 變更目前線程的現用 DPI 感知內容。                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)的變體，可傳回檔整為特定 DPI 的值。     |
| [**SetProcessDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | 設定目前進程的 DPI 感知內容。                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | 覆寫對話的預設個別監視器 DPI 縮放行為。                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | 抓取對話方塊的每個監視器 DPI 縮放行為。                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | 覆寫對話方塊中子視窗的預設個別監視器 DPI 縮放行為。                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | 在對話方塊中，抓取子視窗的任何每個監視器 DPI 縮放行為覆寫。                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | [OpenThemeData](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata)的變體，可開啟與特定 DPI 相關聯的主題控點。 |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | 抓取與給定進程相關聯的系統 DPI。                                                                                                         |
| [**GetDpiFromDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | 從給定的 [DPI \_ 感知 \_ 內容](dpi-awareness-context.md) 控制碼抓取 DPI。                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | 覆寫目前線程的預設 DPI 裝載行為。                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | 抓取目前線程的 DPI 裝載行為。                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | 抓取所指定視窗的 DPI 裝載行為。                                                                                                       |



 

## <a name="types"></a>類型



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **主題**                                                                  | **說明**                                                                        |
| [**DPI \_ 感知**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | 代表 DPI 座標虛擬化模式。                                        |
| [**DPI \_ 感知 \_ 內容**](dpi-awareness-context.md)                   | 代表 DPI 虛擬化模式和相關行為的 token。           |
| [**對話方塊 \_ 控制項 \_ DPI \_ 變更 \_ 行為**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | 描述對話方塊內子視窗的每個監視器 DPI 調整行為覆寫。 |
| [**對話方塊 \_ DPI \_ 變更 \_ 行為**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | 描述對話方塊的每個監視器 DPI 調整行為覆寫。                      |
| [**監視器 \_ DPI \_ 類型**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | 表示與監視器相關聯的 DPI 類型。                                  |
| [**進程 \_ DPI \_ 感知**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | 表示進程的 DPI 座標虛擬化模式。                        |
| [**DPI \_ 裝載 \_ 行為**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | 表示視窗的 DPI 裝載行為。                                      |



 

## <a name="messages"></a>訊息



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **主題**                                                          | **說明**                                                                                                                         |
| [**WM \_ DPICHANGED**](wm-dpichanged.md)                            | 通知最上層視窗其 DPI 已變更。                                                                                   |
| [**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md) | 通知子視窗與其包含的視窗相關聯的 DPI 已變更。 在父視窗收到通知之前傳遞。 |
| [**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)   | 通知子視窗與其包含的視窗相關聯的 DPI 已變更。 在父視窗收到通知之後傳遞。  |
| [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)                | 允許最上層視窗以 *非線性* 方式調整大小，以回應 DPI 變更。                                                           |



 

 

 
