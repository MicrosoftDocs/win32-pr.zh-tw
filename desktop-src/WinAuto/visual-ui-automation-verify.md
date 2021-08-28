---
title: Visual 消費者介面自動化驗證
description: visual 消費者介面自動化確認 (的 visual UIA 確認) 是 Windows \ 32;UIA 測試程式庫的 GUI 驅動程式，專為手動測試使用者介面自動化所設計。
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e8c6118914c791e04226dfa11d2c3bd9548368
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466845"
---
# <a name="visual-ui-automation-verify"></a>Visual 消費者介面自動化驗證

visual 消費者介面自動化確認 (的 visual UIA 確認) 是 UIA 測試程式庫的 Windows GUI 驅動程式，專為手動測試使用者介面自動化所設計。 它提供 UIA 測試程式庫功能的介面，可消除命令列工具的編碼額外負荷。

-   [功能表命令](#menu-commands)
-   [功能窗格](#functional-panes)
    -   [自動化元素樹狀結構窗格](#automation-elements-tree-pane)
    -   [測試窗格](#tests-pane)
    -   [顯示結果窗格](#test-results-pane)
    -   [屬性窗格](#properties-pane)

Visual UIA Verify 僅支援 UIA Verify XML 記錄器 (WUIALoggerXml.dll) 原生。 使用者可選取的 XML 轉換會併入 Visual UIA 的 [驗證] 中，以在 **測試結果** 窗格中呈現 XML 記錄器報表的各種不同的觀點。

根據預設，Visual UIA Verify 會載入隨附于消費者介面自動化原始版本的消費者介面自動化用戶端提供者。 您可以在 VisualUIVerifyNative.exe 的命令列選項中新增 **/NOCLIENTSIDEPROVIDER** ，以選擇不要載入此提供者。

下列螢幕擷取畫面顯示 Visual UIA Verify 使用者介面的主要功能區域。

![visual uia 的主要功能區域驗證使用者介面](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>功能表命令

下表描述 [Visual UIA 驗證] 功能表中的命令。




| 功能表 | 命令 | 描述 | 
|------|---------|-------------|
| <strong>檔案</strong> | <strong>結束</strong> | Exit Visual UIA Verify。 | 
| <strong>檢視</strong> | <strong>反白顯示</strong> | 在 [ <strong>自動化元素] 樹狀目錄</strong> 窗格中，反白顯示所選取專案的周框。 可用選項如下。<ul><li><strong>矩形</strong>—純紅線。</li><li><strong>淡化矩形</strong>—在幾秒鐘後消失的純紅線。</li><li><strong>放射線和矩形</strong>—具有額外藍色醒目提示的純紅線，可從周框矩形的每個角落中放射。</li><li><strong>無</strong>-沒有可見的醒目提示。</li></ul> | 
| <strong>Automation 元素樹狀結構</strong>$ {REMOVE} $<br /> | <strong>重新整理選取的元素</strong> | 重新整理 [ <strong>自動化元素] 樹狀目錄</strong> 窗格中選取之專案的子系。 專案清單是靜態的，而且不會在元素樹狀結構變更時自動重新整理 () 。 | 
| <strong>導覽</strong> | 在元素樹狀結構中流覽至下列其中一個專案。<ul><li><strong>父系</strong>：移至父元素。</li><li><strong>第一個子</strong>系—移至第一個子項目。</li><li><strong>下一個同級</strong>-移至第一個同級元素。</li><li><strong>上一個同級</strong>：移至上一個同級元素。</li><li><strong>最後一個子</strong>系-移至最後一個子項目。</li></ul> | 
| <strong>Mode</strong>$ {REMOVE} $<br /> | <strong>Always On Top</strong> | [視覺效果 UIA 驗證] 視窗會保持在桌面 z 順序的頂端。 | 
| <strong>停留模式 (使用 Ctrl) </strong> | 按下 Ctrl 鍵時，會將滑鼠游標下的元素識別為感興趣的元素。 [ <strong>自動化專案] 樹狀結構</strong> 窗格會重新整理，並反白顯示專案清單中的對應專案。 | 
| <strong>焦點追蹤</strong> | 當焦點變更時，會將具有焦點的專案識別為感興趣的元素。 [ <strong>自動化專案] 樹狀結構</strong> 窗格會重新整理，並反白顯示專案清單中的對應專案。 | 
| <strong>測試</strong>$ {REMOVE} $<br /> | <strong>左移</strong> | 將一個節點移至 [ <strong>測試</strong> ] 樹狀結構中。 | 
| <strong>向上</strong> | 在 <strong>測試</strong> 樹狀結構中向上移動一個節點。 | 
| <strong>往下移</strong> | 在 <strong>測試</strong> 樹狀結構中向下移動一個節點。 | 
| <strong>移至右方</strong> | 在 [ <strong>測試</strong> ] 樹狀結構中，直接移動一個節點。 | 
| <strong>在選取的元素上執行選取的測試 (s) </strong> | 從選取專案上的 [ <strong>測試</strong> ] 樹狀結構執行選取的測試。 | 
| <strong>篩選已知問題</strong> | 篩選來自測試結果的已知消費者介面自動化錯誤。 | 
| <strong>說明</strong> | <strong>關於 Visual 消費者介面自動化驗證</strong> | 顯示 Visual UIA Verify 的軟體版本和著作權資訊。 | 




 

## <a name="functional-panes"></a>功能窗格

本章節描述 Visual UIA Verify 使用者介面中的功能窗格。

-   [自動化元素樹狀結構窗格](#automation-elements-tree-pane)
-   [測試窗格](#tests-pane)
-   [顯示結果窗格](#test-results-pane)
-   [屬性窗格](#properties-pane)

### <a name="automation-elements-tree-pane"></a>自動化元素樹狀結構窗格

[ **自動化專案] 樹狀目錄** 窗格包含可供測試之 Automation 元素物件的階層式快照集。 樹狀結構中的最上層元素代表桌面。

此視圖是在 Visual UIA Verify 開始時編譯的靜態集合。 若要重新整理所選節點的視圖，請使用 [重新整理 **選取** 專案] 功能表命令或工具列按鈕。

下列螢幕擷取畫面顯示 [ **自動化元素] 樹狀結構** 窗格。

![visual uia 的自動化元素樹狀結構窗格確認](images/automation-elements-tree-pane.png)

[ **自動化元素] 樹狀結構** 中的 [無法使用] () 節點，表示專案是消費者介面自動化原始視圖的成員，但不符合要被視為內容檢視器或控制項視圖成員的條件。 不過，您仍然可以從 Visual 消費者介面自動化 Verify 測試專案。 如需詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。

可從 [ **自動化元素] 樹狀** 工具列使用的命令包括：

-   重新 **整理：重新** 整理選取的節點及其子系。 除非已選取根節點，否則這個命令不會重新整理整個元素樹狀結構。
-   **父 (Ctrl + Shift + F6)**-移至目前節點的父代。
-   **第一個子 (Ctrl + Shift + F7)**-移至目前節點的第一個子系。
-   **下一個同級 (Ctrl + Shift + F8)**-移至目前節點的下一個同級子系。
-   **上一個同級 (Ctrl + Shift + F9)**-移至目前節點的上一個同級。
-   **最後一個子 (Ctrl + Shift + F10)**-移至目前節點的最後一個子系。
-   **焦點追蹤**：根據焦點追蹤，開啟或關閉節點選取。

### <a name="tests-pane"></a>測試窗格

[ **測試** ] 窗格包含依測試類型組織 (**Automation 元素**、 **控制項** 和 **模式**) 的消費者介面自動化測試清單，以及 (**組建驗證**、優先順序 **0**、優先順序 **1**、 **優先順序 2** 和 **優先順序 3**) 。 這份清單是根據 [ **自動化元素] 樹狀目錄** 窗格中選取之專案的控制項類型所產生。 如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。

下列螢幕擷取畫面顯示 [ **測試** ] 窗格。

![測試窗格](images/test-pane.png)

可從 [ **測試** ] 工具列使用的命令包括：

-   **顯示**-指定要顯示的消費者介面自動化測試;也就是說，會顯示所有測試，或只顯示 [ **Automation 元素] 樹狀結構** 中選取之專案的控制項類型所適用的測試 (預設) 。
-   **類型**-指定要顯示的測試類型： **Automation 元素**、 **模式** 或 **控制項**。
-   **優先順序**：指定要顯示的測試優先順序： **組建驗證**、 **優先順序 0**、 **優先順序 1**、 **優先順序 2** 或 **優先權 3**。
-   往 **左**-移至目前節點的父代。
-   **上一步-移** 至目前節點的上一個同級。
-   **下一步-移** 至目前節點的下一個同級。
-   **移** 至目前節點的第一個子系。
-   **執行選取的測試 (s)**：在 [ **Automation 元素] 樹狀結構** 中選取的元素上執行測試。

### <a name="test-results-pane"></a>顯示結果窗格

**測試結果** 窗格包含 Visual UIA 驗證記錄功能。 下列螢幕擷取畫面顯示 **測試結果** 窗格。

![測試結果窗格](images/test-results-pane.png)

可從 [ **測試結果** ] 工具列使用的命令包括：

-   **上一頁**：報表查看歷程記錄中的上一頁。
-   **向前**：在報表查看歷程記錄中向前復原頁面。
-   **整體**：顯示測試結果的摘要， (**通過**、**失敗及未****預期的錯誤**) 。 測試結果會連結到 [ **所有結果** ] 視圖。 **整體** 的命令會顯示如下的表格。

    ![整體測試結果資料表](images/overall-test-results.png)

-   **所有結果**-顯示每個測試結果的詳細記錄，如下表所示。

    ![從所有結果檢視記錄結果詳細資料的範例](images/all-results-log.png)

    [ **全部結果** ] 資料表中的測試名稱會連結到元素的測試案例描述，如下表所示。

    ![測試案例詳細資料](images/test-case-detail.png)

-   **完整記錄**：顯示每個測試結果詳細記錄的替代視圖，如下列螢幕擷取畫面所示。

    ![測試案例詳細資料的替代視圖](images/alt-view-of-test-case-detail.png)

-   **Xml**：顯示 xml 記錄器所產生的原始 xml。
-   **快速尋找**： **測試結果** 窗格中的目前視圖的簡單文字搜尋。
-   **在新視窗中開啟**-在 Internet Explorer 的新實例中開啟目前的視圖。

### <a name="properties-pane"></a>屬性窗格

[ **屬性** ] 窗格包含依屬性類型組織的消費者介面自動化屬性和屬性值的清單： **一般協助工具**、 **識別**、 **模式** (控制項模式) 、 **狀態** 和 **可見度**。 屬性值會根據 [ **自動化元素] 樹狀目錄** 窗格中選取之物件的控制項類型，動態填入。 下列螢幕擷取畫面顯示 [ **屬性** ] 窗格。

![屬性窗格](images/properties-pane.png)

如果選取的控制項支援特定的控制項模式，則 Visual UIA Verify 會提供呼叫該控制項模式所支援之方法的能力。 例如， [window 控制項類型](uiauto-supportwindowcontroltype.md)支援 [視窗控制項模式](uiauto-implementingwindow.md)，其具有可從 [**屬性**] 窗格中叫用的 [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close)方法，如下列螢幕擷取畫面所示。 如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。

![從 [屬性] 窗格叫用之視窗控制項模式的關閉方法](images/close-invoked-from-properties-pane.png)

可從 [ **屬性** ] 工具列使用的命令包括：

-   重新 **整理：重新** 整理 [**屬性**] 樹狀目錄。
-   **全部展開**：展開 **屬性** 樹狀結構中的所有節點。

 

 




