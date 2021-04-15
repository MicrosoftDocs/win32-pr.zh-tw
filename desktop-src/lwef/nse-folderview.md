---
title: 實作資料夾檢視
description: Windows Shell 會提供資料夾堆疊的預設執行，稱為 DefView，如此您就可以避免執行自己的命名空間延伸模組的大部分工作。
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- 資料夾檢視物件
- IShellView
- IShellBrowser，資料夾檢視物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/11/2020
ms.locfileid: "104383153"
---
# <a name="implementing-a-folder-view"></a>實作資料夾檢視

Windows Shell 會提供資料夾堆疊的預設執行，稱為 DefView，如此您就可以避免執行自己的命名空間延伸模組的大部分工作。 由於某些視圖功能無法透過自訂視圖來達成，因此通常建議使用預設的系統資料夾 view 物件來取代自訂視圖。 如需詳細資訊，請參閱 [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview)。 本主題的其餘部分將討論如何執行無法支援較新的視圖功能的自訂資料夾檢視。

不同于樹狀檢視，Windows 檔案總管不會管理資料夾檢視的內容。 資料夾檢視視窗會改為裝載資料夾物件所提供的子視窗。 資料夾物件負責建立資料夾 view 物件，以在子視窗中顯示資料夾的內容。

執行資料夾檢視物件的關鍵是 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面。 Windows 檔案總管會使用這個介面與資料夾 view 物件進行通訊。 在顯示資料夾視圖之前，Windows 檔案總管會呼叫資料夾物件的 [**IShellFolder：： CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) 方法，並將 *RIID* 設定為 IID \_ IShellView。 建立資料夾 view 物件，並傳回其 **IShellView** 介面。 資料夾 view 物件接著必須建立資料夾檢視視窗的子視窗，並使用子視窗來顯示資料夾內容的相關資訊。

除了控制資料的顯示方式，擴充功能也可以自訂 Windows 檔案總管的一些功能。 例如，延伸模組可以將專案加入至工具列或功能表列，或在狀態列上顯示資訊。

-   [資料夾 View 物件](#the-folder-view-object)
-   [正在初始化資料夾 View 物件](#initializing-the-folder-view-object)
-   [顯示資料夾視圖](#displaying-the-folder-view)
-   [執行 IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [[重新整理]](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [使用 IShellBrowser 與 Windows 檔案總管通訊](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [修改 Windows 檔案總管的功能表列](#modifying-the-windows-explorer-menu-bar)
    -   [修改 Windows 檔案總管的工具列](#modifying-the-windows-explorer-toolbar)
    -   [修改 Windows 檔案總管狀態列](#modifying-the-windows-explorer-status-bar)
    -   [儲存視圖特定資訊](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>資料夾 View 物件

資料夾檢視物件是 (COM) 物件的元件物件模型，此物件會公開 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面。 此物件負責：

-   建立資料夾檢視視窗的子視窗，並使用它來顯示資料夾的內容。
-   處理與 Windows 檔案總管的通訊。
-   將資料夾特定的命令新增至 Windows 檔案總管功能表列和工具列，並在選取這些命令時進行處理。
-   管理使用者與資料夾檢視視窗的互動，例如顯示快捷方式功能表或處理拖放作業。

本檔討論前三個主題。 因為與資料夾檢視互動的使用者會在子視窗內進行，所以您的資料夾 view 物件會負責處理它，就像在任何其他視窗中一樣。

Windows 檔案總管藉由呼叫您的資料夾物件的 [**IShellFolder：： CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) ，並將 *RIID* 設定為 IID IShellView，要求資料夾 view 物件 \_ 。 建立資料夾檢視的程式如下：

1.  您的資料夾物件會建立資料夾 view 物件的新實例，並傳回其 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面的指標。
2.  Windows 檔案總管藉由呼叫 [**IShellView：： CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) 方法，初始化資料夾 view 物件。 建立資料夾檢視視窗的子視窗，並將其控制碼傳回 Windows 檔案總管。
3.  資料夾 view 物件使用 Windows 檔案總管 [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) 介面來自訂 Windows 檔案總管工具列、功能表列和狀態列。
4.  資料夾 view 物件會在子視窗中顯示資料夾的內容。
5.  資料夾檢視物件會處理使用者與資料夾檢視的互動，以及任何資料夾特定的工具列或功能表列專案。

## <a name="initializing-the-folder-view-object"></a>正在初始化資料夾 View 物件

Windows 檔案總管藉由呼叫 [**IShellView：： CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) 方法，初始化資料夾 view 物件。 方法的參數會為資料夾 view 物件提供建立子視窗所需的資訊，以用來顯示資料夾的內容：

-   上一個資料夾檢視物件之 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面的指標。 這個參數可以設定為 **Null**。
-   包含前一個資料夾檢視設定的 [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) 結構。
-   Windows 檔案總管 [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) 介面的指標。
-   具有資料夾檢視視窗維度的 [矩形](/previous-versions//ms536136(v=vs.85)) 結構。

[**IShellView：： CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow)方法是在終結先前的資料夾 view 物件之前呼叫。 因此， [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面指標可讓您與上一個資料夾 view 物件進行通訊。 如果先前的資料夾屬於您的延伸模組，並使用相同的顯示配置，這個介面主要很有用。 若是如此，您可以與先前的資料夾 view 物件進行通訊，以做為交換私用設定的目的。

判斷 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 指標是否屬於您延伸模組的簡單方式，就是讓所有資料夾 view 物件都公開私用介面。 呼叫 [IShellView：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 要求私用介面，並檢查傳回值，判斷資料夾 view 物件是否為您的資料夾。 然後，您可以在該介面上使用私用方法來交換資訊。

[**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings)結構包含上一個資料夾檢視的顯示設定。 主要設定是觀看模式：大型圖示、小圖示、清單或詳細資料。 另外還有一個旗標，其中包含各種顯示選項的設定，例如，視圖是否應靠左對齊。 您的資料夾顯示應該盡可能將這些設定放在可能的範圍內，讓使用者在從一個資料夾移到另一個資料夾時擁有一致的體驗。 您應該儲存此結構，並在設定變更時加以更新。 Windows 檔案總管會呼叫 [**IShellView：： GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) 來取得此結構的最新值，然後再開啟下一個資料夾檢視。

[**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)介面是由 Windows 檔案總管所公開。 此介面是 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 的隨附物件，可讓資料夾檢視物件與 Windows 檔案總管進行通訊。 沒有其他方法可取得此介面指標，因此您的資料夾 view 物件應該儲存它以供稍後使用。 尤其是，您必須呼叫 [IShellBrowser：： GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) ，以抓取您將用來建立子視窗的父資料夾檢視視窗。 請注意，IShellBrowser：： GetWindow 方法不包含在 **IShellBrowser** 檔中，因為它是從 [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow)繼承的。 儲存介面指標之後，請記得呼叫 [IShellBrowser：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 來遞增介面的參考計數。 當您不再需要介面時，請呼叫 [IShellBrowser：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。

若要建立子視窗：

1.  檢查 [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) 和 [RECT](/previous-versions//ms536136(v=vs.85)) 結構。
2.  如有需要，請從上一個資料夾 view 物件取得私用設定。
3.  呼叫 [IShellBrowser：： GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) ，以抓取父資料夾的視圖視窗。
4.  建立在上一個步驟中取得之資料夾檢視視窗的子系，並將其傳回 Windows 檔案總管。

## <a name="displaying-the-folder-view"></a>顯示資料夾視圖

當您建立子視窗，並將它傳回 Windows 檔案總管之後，您就可以顯示資料夾的內容。 一般情況下，延伸模組會顯示其資訊，方法是讓子視窗主 [控制項成為清單視圖控制項](../controls/list-view-control-reference.md) 或 **WebBrowser 控制項**。 清單視圖控制項可讓您複寫 Windows 檔案總管的 [傳統視圖](web-view.md)。 WebBrowser 控制項可讓您使用動態 HTML (DHTML) 檔來顯示您的資訊，就像 Windows 檔案總管 Web 視圖一樣。 如需詳細資訊，請參閱這些控制項的檔。

資料夾檢視視窗一律存在，即使沒有焦點也一樣。 因此，您應該為子視窗維持三種狀態：

-   以焦點啟用。 資料夾檢視已建立並具有焦點。 設定適合焦點狀態的功能表列或工具列專案。
-   啟用但不包含焦點。 資料夾檢視已建立且為使用中狀態，但沒有焦點。 設定適用于 nonfocused 狀態的功能表列或工具列專案。 省略套用至資料夾檢視內專案選取專案的任何專案。
-   關閉。 資料夾檢視即將損毀。 移除所有資料夾特定的功能表項目。

Windows 檔案總管藉由呼叫 [**IShellView：： UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate)，在視窗狀態變更時通知資料夾 view 物件。 接著，當使用者藉由呼叫 [**IShellBrowser：： OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive)來啟動資料夾檢視視窗時，資料夾 view 物件應該會通知 Windows 檔案總管。 如需此介面的進一步討論，請參閱 [使用 IShellBrowser 與 Windows 檔案總管進行通訊](#using-ishellbrowser-to-communicate-with-windows-explorer)。

當資料夾檢視為使用中狀態時，您需要處理屬於子視窗的任何 Windows 訊息，例如 [WM \_ 大小](../winmsg/wm-size.md)。 您的視窗程式也會收到您已新增至 Windows 檔案總管功能表列或工具列之任何專案的 [WM \_ 命令](../menurc/wm-command.md) 訊息。

建立資料夾檢視之後，Windows 檔案總管會呼叫資料夾 view 物件的 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面，將各種資訊傳遞給它。 您的物件必須據以修改其顯示。 當資料夾檢視即將終結時，Windows 檔案總管藉由呼叫 [**IShellView：:D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) 方法來通知資料夾 view 物件。

## <a name="implementing-ishellview"></a>執行 IShellView

建立資料夾物件之後，Windows 檔案總管會呼叫各種 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 方法來要求資訊，或將 Windows 檔案總管狀態的變更通知物件。 本節概述如何執行這些 **IShellView** 方法。 其餘的方法會用於更特製化的用途，例如 [檔案開啟一般] 對話方塊。 如需詳細資訊，請參閱 **IShellView** 檔。

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

當使用者從 Windows 檔案總管 [**工具**] 功能表選取 [**資料夾選項**] 時，會顯示可讓使用者修改資料夾選項的屬性工作表。 Windows 檔案總管會呼叫您的資料夾 view 物件的 [**IShellView：： AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) 方法，讓您可以在此屬性工作表中加入頁面。

Windows 檔案總管會在 [**IShellView：： AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages)的 *lpfn* 參數中傳遞 [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage)回呼函數的指標。 呼叫 [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 來建立頁面，然後呼叫 AddPropSheetPageProc，將它加入至屬性工作表。 如需如何處理屬性工作表的進一步討論，請參閱 [屬性工作表](../controls/property-sheets.md)。

### <a name="getcurrentinfo"></a>GetCurrentInfo

當使用者從某個資料夾切換到另一個資料夾時，Windows 檔案總管嘗試維護類似的資料夾檢視。 比方說，如果前一個資料夾檢視顯示大型圖示，則下一個資料夾應該也是。 當 Windows 檔案總管呼叫 [**IShellView：： CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) 來初始化您的資料夾 view 物件時，方法會收到 [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) 結構。 此結構包含的資訊可讓您將資料夾檢視顯示為與上一個資料夾檢視一致。

為了協助確保下一個視圖與目前的視圖一致，請儲存 [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) 結構。 如果視圖變更（例如，從大到小的圖示），請據以更新結構。 切換視圖之前，Windows 檔案總管會呼叫 [**IShellView：： GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) 來要求目前的 **FOLDERSETTINGS** 值，將其傳遞至下一個資料夾 view 物件。

### <a name="refresh"></a>重新整理

使用者 **可以從 [** **view** ] 功能表中選取 [重新整理] 或按 F5 鍵，以確保資料夾檢視反映資料夾的目前狀態。 當使用者這樣做時，Windows 檔案總管會呼叫 [**IShellView：： Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) 方法。 您的資料夾 view 物件應該立即更新資料夾檢視顯示。

### <a name="saveviewstate"></a>SaveViewState

Windows 檔案總管會呼叫 [**IShellView：： SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) 方法，以提示您的資料夾 view 物件儲存其檢視狀態。 然後，您可以在下一次查看資料夾時復原狀態。 儲存檢視狀態的慣用方式是呼叫 [**IShellBrowser：： GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) 方法。 這個方法會傳回一個 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 介面，您的資料夾 view 物件可以使用它來儲存其狀態。 當您建立另一個資料夾檢視時，您可以呼叫相同的 **IShellBrowser：： GetViewStateStream** 方法來取得 IStream 指標，讓您能夠讀取先前資料夾檢視所儲存的設定。

### <a name="translateacelerator"></a>TranslateAcelerator

當使用者按下快速鍵時，Windows 檔案總管藉由呼叫 [**IShellView：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator)，將訊息傳遞至資料夾 view 物件。 傳回 \_ FALSE，使 Windows 檔案總管處理訊息。 如果您的資料夾 view 物件已處理訊息，請返回 \_ [確定]。

當資料夾檢視視窗具有焦點時，Windows 檔案總管會先呼叫 [**IShellView：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) ，然後再處理訊息。 因為大部分的訊息通常會與 Windows 檔案總管的功能表列或工具列命令相關聯，所以您的資料夾 view 物件通常會傳回 \_ FALSE。 然後 Windows 檔案總管可以正常地處理訊息。 \_只有當訊息是資料夾特定的，而且您不想 Windows 檔案總管進行任何進一步的處理時，才會傳回 [確定]。 如果資料夾檢視沒有焦點，Windows 檔案總管先處理訊息。 只有在未處理訊息時，它才會呼叫 [**IShellBrowser：： TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) 。

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>使用 IShellBrowser 與 Windows 檔案總管通訊

資料夾檢視物件會使用 [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) 介面來與 Windows 檔案總管進行通訊，以因應各種用途，包括：

-   [修改 Windows 檔案總管的功能表列](#modifying-the-windows-explorer-menu-bar)
-   [修改 Windows 檔案總管的工具列](#modifying-the-windows-explorer-toolbar)
-   [修改 Windows 檔案總管狀態列](#modifying-the-windows-explorer-status-bar)
-   [儲存視圖特定資訊](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>修改 Windows 檔案總管的功能表列

Windows 檔案總管的功能表列可讓使用者啟動各種不同的命令。 依預設，功能表列只支援特定于 Windows 檔案總管的命令。 相關的 [WM \_ 命令](../menurc/wm-command.md) 訊息會由 Windows 檔案總管處理，而不會傳遞至您的資料夾 view 物件。 不過，您可以使用 [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)修改功能表列，以包含一或多個資料夾特定的功能表項目。 Windows 檔案總管將這些專案的相關聯的 WM \_ 命令訊息傳遞至您資料夾物件的視窗程式進行處理。 您也可以移除或停用任何未套用至應用程式的標準命令。

資料夾檢視物件通常會在第一次顯示資料夾視圖之前修改功能表列。 當資料夾檢視損毀時，他們必須將功能表列傳回其原始狀態。 您也可能需要在每次資料夾檢視獲得或失去焦點時，修改功能表列。

因為 Windows 檔案總管會在每次資料夾檢視視窗的狀態變更時呼叫 [**IShellView：： UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) ，所以通常會在該方法的執行中包含功能表列修改。 修改 Windows 檔案總管功能表列的基本程式如下：

1.  呼叫 [CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) 來建立功能表控制碼。
2.  藉由呼叫 [**IShellBrowser：： InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb)，將該功能表控制碼傳遞至 Windows 檔案總管。 Windows 檔案總管將會填入其功能表資訊。
3.  視需要修改功能表。
4.  呼叫 [**IShellBrowser：： SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) ，讓 Windows 檔案總管顯示修改過的功能表列。

Windows 檔案總管在功能表列上有六個快顯功能表。 如同所有的 OLE 容器，[Windows 檔案總管] 功能表分為六個群組： [檔案]、[編輯]、[容器]、[物件]、[視窗] 和 [說明]。 下表列出 Windows 檔案總管快顯功能表與其相關聯的群組，以及功能表識別碼。



| 快顯功能表 | 識別碼                     | Group     |
|-------------|------------------------|-----------|
| 檔案        | FCIDM \_ 功能表 \_ 檔      | 檔案      |
| 編輯        | FCIDM \_ 功能表 \_ 編輯      | 檔案      |
| 檢視        | FCIDM \_ 功能表 \_ 視圖      | 容器 |
| 我的最愛   | FCIDM 功能表我的最愛 \_ \_ | 容器 |
| 工具       | FCIDM \_ 功能表 \_ 工具     | 容器 |
| Help        | FCIDM \_ 功能表 \_ 說明      | 時間範圍    |



 

當您藉由呼叫 [**IShellBrowser：： InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb)，將功能表控制碼傳遞至 Windows 檔案總管時，您也必須將指標傳遞至其成員已初始化為零的 [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) 結構。

當 [**IShellBrowser：： InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) 傳回時，Windows 檔案總管會新增其功能表項目。 然後，您可以將傳回的功能表控制碼與標準的 Windows 功能表功能搭配使用，例如 [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) 至：

-   將專案新增至 Windows 檔案總管快顯功能表。
-   修改或刪除 Windows 檔案總管快顯功能表中的現有專案。
-   加入新的快顯功能表。

使用表格中所列的識別碼來識別各種 Windows 檔案總管快顯功能表。

> [!Note]  
> 為了避免與 Windows 檔案總管的命令識別碼發生衝突，您新增的任何功能表項目的識別碼都必須介於 FCIDM \_ SHVIEWFIRST 和 FCIDM \_ SHVIEWLAST 之間。 這兩個值是在 Shlobj.h 中定義。

 

當您完成修改功能表之後，請呼叫 [**IShellBrowser：： SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) 讓 Windows 檔案總管顯示新的功能表列。

一開始顯示資料夾視圖之後，Windows 檔案總管每次資料夾檢視獲得或失去焦點時，就會呼叫 [**IShellView：： UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) 。 如果您有任何與資料夾檢視狀態相關的功能表項目，您應該在每次狀態變更時，據以修改功能表。 比方說，您可能有一個功能表項目，它會作用於使用者所選取的資料夾檢視中的專案。 當資料夾檢視失去焦點時，您應該停用或移除這個功能表項目。

當 Windows 檔案總管呼叫 [**IShellView：： UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) 指出正在停用資料夾檢視時，請呼叫 [**IShellBrowser：： RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb)，將功能表列還原為其原始狀態。

### <a name="modifying-the-windows-explorer-toolbar"></a>修改 Windows 檔案總管的工具列

除了修改 Windows 檔案總管的功能表列，您也可以將按鈕加入至工具列。 在功能表列中，修改工具列通常是 [**IShellView：： UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) 執行的一部分。 將按鈕新增至 Windows 檔案總管工具列的程式如下：

1.  將按鈕的點陣圖新增至工具列的影像清單。
2.  定義按鈕的文字字串。
3.  將按鈕加入至工具列。

若要將點陣圖新增至工具列的影像清單，請藉由呼叫 [**IShellBrowser：： SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg)，將一個 [ [TB] \_ ADDBITMAP](../controls/tb-addbitmap.md)訊息傳送給工具列。 若要指定工具列控制項，請將方法的 *id* 參數設定為 **FCW \_ 工具列**。 將 *wParam* 設定為點陣圖中的按鈕影像數目，並 *lParam* 至 [TBADDBITMAP](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) 結構的位址。 映射索引會在 *pret* 參數中傳回。

有兩種方式可以定義按鈕的字串：

-   將字串指派給按鈕 [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton)結構的 **iString** 成員。
-   呼叫 [**IShellBrowser：： SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) ，將 [ \_ ADDSTRING](../controls/tb-addstring.md) 訊息傳送至工具列控制項。 *WParam* 參數應設為零，並將 *lParam* 參數設定為字串。 字串索引會在 *pret* 參數中傳回。

若要將按鈕加入至工具列，請填入 [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) 結構，並將它傳遞至 [**IShellBrowser：： SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems)。 如同功能表，您的命令識別碼必須落在 FCIDM \_ SHVIEWFIRST 和 FCIDM \_ SHVIEWLAST 之間。 工具列接著會將按鈕附加至現有按鈕的右邊。

例如，下列程式碼片段會將一個標準按鈕新增至 [Windows 檔案總管] 工具列，其中包含 [.IDB MYBUTTON] 的命令識別碼 \_ 。


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



如需如何處理工具列控制項的進一步討論，請參閱 [工具列控制項](../controls/toolbar-control-reference.md)。

### <a name="modifying-the-windows-explorer-status-bar"></a>修改 Windows 檔案總管狀態列

您可以使用 Windows 檔案總管狀態列來顯示各種有用的資訊。 有兩種方式可以使用狀態列：

-   使用 [**IShellBrowser：： SetStatusTextSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) 在狀態列上顯示文字字串。
-   將訊息直接傳送至具有 [**IShellBrowser：： SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg)的狀態列控制項。

第一個方法很簡單，但也足以滿足許多用途。 為了提供更大的彈性，您可以呼叫 [**IShellBrowser：： SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) ，並將 *id* 參數設定為 **FCW \_ status**，將訊息直接傳送至狀態列控制項。 如需狀態列控制項的進一步討論，請參閱 [狀態列](../controls/status-bars.md)。

### <a name="storing-view-specific-information"></a>儲存視圖特定資訊

當某個視圖即將終結時，儲存資訊（例如，視圖的狀態或設定）通常會很有用。 Windows 檔案總管會提示您藉由呼叫 [**IShellView：： SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate)來執行這項工作。 儲存視圖特定資訊的慣用方式是呼叫 [**IShellBrowser：： GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream)。 這個方法會提供您可用來儲存資訊的 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 介面。 您可以自由使用任何適合的資料格式。

 

 
