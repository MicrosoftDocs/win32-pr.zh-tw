---
title: '協助工具工具-AccEvent (可存取的事件監看員) '
description: AccEvent (可存取的事件監看員) 可讓開發人員和測試人員驗證應用程式的 UI 元素是否會在 UI 變更時引發適當的 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 事件。
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2192bf6973444bf2bfc307ff4613d9d1c593d5a22f9800ecb61bc310b3a210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327798"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>協助工具工具-AccEvent (可存取的事件監看員) 

**AccEvent (可存取的事件** 監看員) 可讓開發人員和測試人員驗證應用程式的 ui 元素是否會在 ui 變更時引發適當的 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 事件。 當焦點變更時，或叫用、選取或變更狀態或屬性時，就會發生 UI 中的變更。

**AccEvent** 會隨 Windows 軟體開發套件 (SDK) 安裝。 它位於 \\ \\ < SDK 安裝路徑的 bin *版本* > \\ < *平臺*> 資料夾 (Accevent.exe) 。

> [!NOTE]
> **AccEvent** 是一種舊版工具。 建議您改為使用[協助工具 Insights](https://accessibilityinsights.io/) 。

## <a name="requirements"></a>規格需求

**AccEvent** 可以用來檢查沒有消費者介面自動化的系統上的協助工具資料，其原本是針對 Microsoft Active Accessibility 撰寫。 若要檢查消費者介面自動化，消費者介面自動化必須存在於系統上。 如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。

**AccEvent** 會安裝為 Windows SDK 的整體工具組的一部分，而不是以個別的 exe 下載方式來散發。 Windows SDK 包含本節中記載的所有協助工具相關工具。 [取得 Windows SDK。](https://developer.microsoft.com/) 如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) 

若要執行 **AccEvent**，請在 [ \\ bin \\ < *版本* 平臺>] 資料夾中尋找 AccEvent.exe， > \\ < 然後執行它 (您通常不需要以系統管理員身分執行) 。

## <a name="the-accessible-event-watcher-window"></a>可存取的事件監看員視窗

當您啟動 **AccEvent** 時，主視窗會隨即顯示。 [主要 **AccEvent** ] 視窗會顯示正在執行的應用程式所引發的消費者介面自動化或 Microsoft Active Accessibility 事件。 主視窗有下列主要部分：

- 標題列： 顯示目前的作業模式和狀態。
- 功能表列： 提供 **AccEvent** 功能的存取權。
- 資料檢視。 顯示每個事件的相關資訊，包括事件識別碼和引發事件之 UI 元素的選取屬性。

**AccEvent** 只能有圖形化使用者介面;此工具沒有任何命令列引數，但您可以使用其他工具將輸出記錄檔當作文字來處理。

下圖顯示主要 **AccEvent** 視窗。

![可存取的事件監看員工具的使用者介面](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>可存取的事件監看員工作

本節包含常用 **AccEvent** 工作的相關資訊。

### <a name="configuring-the-operating-mode"></a>設定操作模式

您可以使用 [ **模式]** 功能表來設定 **AccEvent** 作業模式，並選取控制工具行為的設定。 您可以選取下列選項。



| 選取此選項時 | **AccEvent**                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 永遠開啟頂端                | 顯示在畫面上任何其他使用者介面的上方。                                                                                                                                                                                    |
| UIA 事件                   | 顯示消費者介面自動化事件的相關資訊。                                                                                                                                                                                             |
| 內容) 中的 WinEvents (       | 顯示 Microsoft Active Accessibility 事件的相關資訊 (WinEvents) 傳遞給位於伺服器位址空間的攔截函式。 如需詳細資訊，請參閱內部內容攔截函 [式](in-context-hook-functions.md)。         |
| WinEvents (出內容)    | 顯示 (WinEvents) 傳遞給位於用戶端位址空間之攔截函式的 Microsoft Active Accessibility 事件的相關資訊。 如需詳細資訊，請參閱 [跨內容](out-of-context-hook-functions.md)攔截函式。 |
| 顯示反白顯示矩形     | 反白顯示引發所選事件之 UI 元素周圍的矩形。                                                                                                                                                                 |
| 顯示資訊工具提示     | 在工具提示中顯示事件資訊。                                                                                                                                                                                                        |
| 設定                     | 顯示 **UIA 事件設定** 或 **new-winevent 設定**] 對話方塊。                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>篩選消費者介面自動化事件

若要設定 **AccEvent** 視窗中顯示的消費者介面自動化事件和屬性，請按一下 [**模式]** 功能表，選取 [ **UIA 事件**]，然後選取 [**設定**]。 [ **UIA 事件設定**] 對話方塊隨即顯示。 您也可以使用此對話方塊來篩選事件。

**UIA 事件設定**] 對話方塊包含下列窗格：

- **全域活動**

    選取 [ **FocusChangedEvent** ] 核取方塊，以顯示有關全域焦點變更事件的資訊。

- **事件類型**

    選取您感興趣的事件。

- **範圍**

    選取您希望 **AccEvent** 接聽事件的 UI 元素。

- **包含事件來源**

    如果您要在 [**領域**] 窗格中選取之 UI 元素的直屬子項目看到事件，請選取 [**直屬子** 系]。 如果您想要查看所有子系專案的事件，請選取 [ **所有** 子系]。

- **報表屬性**

    選取您要在主視窗中的每個事件之後顯示的屬性。 如果已在 [**模式]** 功能表中選取 [**顯示資訊工具提示**]，則選取的屬性也會顯示在工具提示中。

### <a name="filtering-active-accessibility-events"></a>篩選 Active Accessibility 事件

若要設定 [ **AccEvent** ] 視窗中顯示的 Microsoft Active Accessibility 事件和屬性，請按一下 [**模式]** 功能表，選取 [**內容) 中** 的 [WinEvents] (或 [WinEvents] **(超出內容)**，然後選取 [**設定**]。 [ **new-winevent 設定**] 對話方塊隨即顯示。 您也可以使用此對話方塊來篩選事件。

[ **new-winevent 設定**] 對話方塊包含下列窗格：

- **物件**

    選取您希望 **AccEvent** 接聽事件的物件。 **AccEvent** 可以接聽源自 windows、游標或插入點的事件。 預設會選取 [**視窗]** 。

- **事件**

    選取您感興趣的事件。 預設會顯示所有事件。

- **事件資訊**

    選取您要在主視窗中的每個事件名稱之後顯示的資訊。

- **物件屬性**

    選取您要在主視窗中的每個事件之後顯示的屬性。 如果已在 [**模式]** 功能表中選取 [**顯示資訊工具提示**]，則選取的屬性也會顯示在工具提示中。 預設會選取 [**名稱**]、[**角色**] 和 [**狀態**]。

- **篩選**

    在 [篩選] 區段中選取其中一個選項按鈕，以篩選 [ **hwnd** ] 欄位中指定的視窗所引發的事件。 預設會選取 [ **不要篩選** ] 選項按鈕。

    - 選取 [ **排除** ] 選項按鈕，只顯示從指定視窗以外的物件所引發的事件。
    - 選取 [ **僅包含** ] 選項按鈕，並指定一或多個視窗控點，只顯示從這些視窗引發的事件。
    - 核取 [ **和** 子系] 核取方塊，以包含由指定之視窗的下階所引發的事件。

- **選項**

    接著，選取下列任何一個選項：

    

    | 選取此選項時                                  | **AccEvent**                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 使用 Invoke                                                    | 使用 [IDispatch：： Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 來取出物件屬性，而不是使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法。                               |
    | 即使未選取物件屬性，一律取得物件 ()      | 抓取與事件相關聯的物件，即使在 [物件屬性] 窗格中未選取任何專案。                                                                                        |
    | 除了選取的屬性外，還會顯示預設屬性 ()  | 顯示與事件相關聯之物件的預設屬性（如果有的話），以及 [物件屬性] 窗格中所選取的專案。                                                      |
    | 顯示隱藏/隱藏視窗的事件資訊       | 顯示所有物件的 [事件資訊] 窗格中選取的專案，包括隱藏或隱藏視窗中的專案。                                                                       |
    | 顯示隱藏/隱藏視窗的完整事件資訊  | 從 [事件資訊] 窗格中，顯示選取的專案，以及針對所有物件從 [物件屬性] 窗格中選取的 (或預設) 專案，包括隱藏或隱藏視窗中的物件。 |
    | DebugBreak 下一個事件                                      | 導致中斷點例外狀況發生在產生下一個 New-winevent 的進程中。 這會指示偵錯工具處理例外狀況。                                                        |

### <a name="using-the-event-menu"></a>使用事件功能表

使用 [ **事件** ] 功能表來執行下列工作：

| 選取此選項時 | **AccEvent**                                    |
|------------------------------|-------------------------------------------------------|
| 開始接聽              | 開始在資料檢視中顯示事件資訊。 |
| 停止接聽               | 停止顯示資料檢視中的事件資訊。  |
| 清除事件歷程記錄          | 清除資料檢視的內容。                 |
| 選取所有事件            | 選取資料檢視中列出的所有事件。           |
| 複製選取的事件         | 將選取的事件複製到剪貼簿。          |

### <a name="saving-active-accessibility-events"></a>正在儲存 Active Accessibility 事件

若要開始將事件儲存至文字檔，請開啟 **[檔案** ] 功能表，然後選取 [ **開始記錄至** 檔案]。 **AccEvent** 會開始將事件寫入至指定的檔案，直到您 **從 [檔案**] 功能表選取 [**停止記錄**]。 文字檔對於稍後進行疑難排解和檢查事件可能很有用。

## <a name="related-topics"></a>相關主題

- [協助工具事件監控程式](accessible-event-watcher.md)
- [測試控管](testing-tools.md)
- [UI 協助工具檢查程式](ui-accessibility-checker.md)
- [UI 自動化事件概觀](uiauto-eventsoverview.md)
- [使用者介面自動化確認](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)