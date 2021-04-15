---
description: 描述 Windows 協助工具功能、工具、檔和範例的最新創新和更新。
title: 適用于開發人員的 Windows 協助工具的新功能
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 44d8c453b09bc73e71006e132199c18b275860af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468528"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>適用于開發人員的新 Windows 協助工具功能、工具、檔和範例

Windows 平臺會以開發人員的新協助工具和自動化功能不斷更新。

在 Windows 10 上[安裝工具和 SDK](https://developer.microsoft.com/windows/downloads/#_blank) ，您就可以建立新的通用 Windows 應用程式，或探索如何在 Windows 上使用現有的應用程式程式碼。

如需可用來測試 Windows 和 web 應用程式之協助工具實作為最新工具的詳細資訊，請參閱 [測試協助工具](accessibility-testwithuia.md)。

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>Windows 10 2019 年5月更新 (1903 版的新功能) 

下列功能、工具、開發人員指引、範例和影片已提供給 [Windows 10 2019 年5月更新](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97)使用。

| 版本 | 平台 | 功能 | 描述 | 連結 |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | 消費者介面自動化支援 IAccessible2 | 消費者介面自動化用戶端現在可以順暢地存取 IAccessible2 提供者（例如 Chrome 瀏覽器）的資訊。 | n/a |
| 1903 | UWP | 捲軸可見度  | 當未進行互動時，捲軸會自動隱藏。 | [UISettings. AutoHideScrollBars 屬性](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | 消費者介面自動化支援結構化標記 | 預定（但不限於） MathML 剖析。 | n/a |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Windows 10 2018 年10月更新 (1809 版的新功能) 

下列功能、工具、開發人員指引、範例和影片已提供給 [Windows 10 2018 年10月更新](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97)使用。

| 版本 | 平台 | 功能 | 描述 | 連結 |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | 消費者介面自動化支援活動文字位置變更事件 | 消費者介面自動化提供者可以明確地設定文字範圍內的開始位置。 ) 用戶端的輔助技術 (接著可以將此位置傳達給使用者。 例如，如果使用者按一下相同頁面上錨點的連結 (書簽連結) ，則會提供新的位置給。 | [IUIAutomation6 介面](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | 消費者介面自動化支援事件聯合 | 藉由嘗試偵測、篩選和忽略重複的順序 MSAA 以及某些提供者所引發的 UIA TextChanged 事件，來改善效能。 | [IUIAutomation6 介面](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | 消費者介面自動化支援連接復原行為 | 如果提供者沒有回應) ，消費者介面自動化用戶端傳送給提供者的訊息會在兩秒內暫停 (。 這可減少延長超時的頻率，並使用事件和要求將沒有回應的提供者降至最低。 | [IUIAutomation6 介面](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | 增強的螢幕閱讀程式服務 | 用戶端知道有聲音的畫面讀取位置 (控制項或內容) 和閱讀模式。 | [ScreenReaderService 類別](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32、UWP | 消費者介面自動化支援對話方塊視窗 | 消費者介面自動化提供者可以明確地將 UIA 元素標示為對話方塊視窗。 ATs 通常會以不同的方式向使用者顯示對話方塊。  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[ContentDialog 類別](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | 文字大小調整  | 調整應用程式與網頁中的文字大小。 | [UISettings. TextScaleFactorChanged 事件](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[文字大小調整](/windows/uwp/design/input/text-scaling) |
