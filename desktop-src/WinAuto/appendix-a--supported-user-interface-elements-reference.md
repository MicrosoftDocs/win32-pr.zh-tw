---
title: 附錄 A 支援的消費者介面元素參考
description: 本附錄包含 Windows 95、Windows 98、Microsoft Windows NT、Windows 2000、Windows XP 和 Windows 2000 Server Microsoft Active Accessibility 公開的系統提供 UI 元素的相關資訊。
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e434eec9a480f46bb352dbd5b523b8b5c9cde6624c9d94372703d054e945bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994368"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>附錄 A：支援的消費者介面元素參考

本附錄包含 Windows 95、Windows 98、Microsoft Windows NT、Windows 2000、Windows XP 和 Windows 2000 Server Microsoft Active Accessibility 公開的系統提供 UI 元素的相關資訊。 這項支援可讓用戶端公用程式取得未執行 Microsoft Active Accessibility 之應用程式中系統提供的 UI 元素的相關資訊。

Oleacc.dll 支援 User32.dll、Comctl32.dll 和 Windows UI 元素中定義的控制項。 具體而言，它支援下列類型的 UI 元素， (Windows 類別名稱) 列出。



| Windows 類別名稱                   | UI 元素類型                                         | WindowsVista 更新                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | 清單方塊                                              | 無                                                                                                                                                                                                                 |
| Button                               | 按鈕、選項按鈕、複選按鈕、群組方塊 | 分割按鈕可以有零個或多個子系。                                                                                                                                                                        |
| 靜態                               | 標籤                                                  | 無                                                                                                                                                                                                                 |
| 編輯                                 | 文字方塊                                              | 無                                                                                                                                                                                                                 |
| ComboBox                             | 下拉式方塊、下拉式清單                            | 無                                                                                                                                                                                                                 |
| ScrollBar                            | 捲軸                                             | [**活動 \_物件 \_ CONTENTSCROLLED**](event-constants.md) 是具有滾動功能但不包含標準捲軸作為控制項一部分之控制項的新事件。 |
| \#32768                              | 使用者功能表                                              | 無                                                                                                                                                                                                                 |
| \#32770                              | 使用者對話方塊                                       | 無                                                                                                                                                                                                                 |
| \#32771                              | Alt-tab 視窗                                          | 僅適用于傳統模式。                                                                                                                                                                                      |
| msctls \_ statusbar32                  | 狀態列                                             | 無                                                                                                                                                                                                                 |
| msctls \_ progress32                   | 進度列                                           | Microsoft Active Accessibility 或 Microsoft 消費者介面自動化屬性不會公開進度列的新色彩選項。                                                                                         |
| msctls \_ hotkey32                     | 快速鍵控制項                                        | 無                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars、滑杆                                      | 無                                                                                                                                                                                                                 |
| msctls \_ updown32                     | 上下調整控制項                                | 無                                                                                                                                                                                                                 |
| SysAnimate32                         | 動畫控制項                                       | 無                                                                                                                                                                                                                 |
| SysTabControl32                      | 索引標籤控制項                                             | 無                                                                                                                                                                                                                 |
| SysHeader32                          | 清單視圖標頭                                       | 無                                                                                                                                                                                                                 |
| SysListView32                        | 清單視圖控制項                                      | 無                                                                                                                                                                                                                 |
| SysTreeView32                        | 樹狀檢視控制項                                      | 無                                                                                                                                                                                                                 |
| SysDateTimePick32 (第5版和第6版)  | 日期和/或時間選擇器                                 | 在 Windows Vista 中，此控制項的第6版具有原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)執行。                                                                                                           |
| SysIPAddress32                       | IP 位址控制項                                     | 無                                                                                                                                                                                                                 |
| 工具提示 \_ class32                    | 提示                                                | 無                                                                                                                                                                                                                 |
| ToolbarWindow32                      | 工具列                                                | 無                                                                                                                                                                                                                 |
| RICHEDIT、RichEdit20A、RichEdit20W   | 文字欄位                                             | 無                                                                                                                                                                                                                 |
| SysMonthCal32 (第5版和第6版)      | 月曆                                          | 在 Windows Vista 中，此控制項的第6版具有原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)執行。                                                                                                           |



 

雖然對系統提供的 UI 元素有一些支援是由 Microsoft Windows NT 4.0 （含 service pack 4）上的 Microsoft Active Accessibility 所提供，但這項支援受限。

本附錄列出 Microsoft Active Accessibility 針對每個 UI 元素所支援的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法。 在適用的情況下，檔也會列出 UI 元素觸發的 [WinEvents](winevents-infrastructure.md) ，並包含有關所支援屬性和方法的其他資訊。 它也包含物件角色及其支援的 **IAccessible** 方法和屬性的相關資訊。

這些詳細資料可協助用戶端開發人員避免對不支援的屬性和方法進行不必要的呼叫。 這種資訊也可讓伺服器開發人員知道自訂控制項應支援哪些屬性和方法，以及哪些 WinEvents 的控制項應該會觸發。

使用本附錄中的資訊做為指南。 強烈建議您使用 Microsoft Active Accessibility 工具來確認 UI 元素或物件角色的預期行為。

如需詳細資訊，請參閱下列主題：

-   [Active Accessibility 如何公開消費者介面元素](how-active-accessibility-exposes-user-interface-elements.md)
-   [消費者介面元素參考](user-interface-element-reference.md)

 

 




