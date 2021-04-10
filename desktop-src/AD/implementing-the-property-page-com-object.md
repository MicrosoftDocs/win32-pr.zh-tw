---
title: 執行屬性頁 COM 物件
description: 屬性工作表延伸是實作為同進程伺服器的 COM 物件。
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- 執行屬性頁 COM 物件
- 屬性頁 COM 物件，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55962002ca059ad6e9c137925d1ba21ba9adc513
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842071"
---
# <a name="implementing-the-property-page-com-object"></a>執行屬性頁 COM 物件

屬性工作表延伸是實作為同進程伺服器的 COM 物件。 屬性工作表延伸模組必須執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面。 當使用者顯示類別物件的屬性工作表時，會將屬性工作表延伸具現化，該類別的屬性工作表延伸已在類別的顯示規範中註冊。

-   [執行 IShellExtInit](#implementing-ishellextinit)
-   [執行 IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [將延伸模組物件傳遞給屬性頁](#passing-the-extension-object-to-the-property-page)
-   [使用通知物件](#working-with-the-notification-object)
-   [其他](#miscellaneous)
-   [多重選取屬性工作表](#multiple-selection-property-sheets)
-   [Windows Server 2003 的新](#new-with-windows-server-2003)
-   [相關主題](#related-topics)

## <a name="implementing-ishellextinit"></a>執行 IShellExtInit

在屬性工作表延伸 COM 物件具現化之後，會呼叫 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 方法。 **IShellExtInit：： Initialize** 會提供具有 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 物件的屬性工作表延伸，其包含與屬性工作表所套用的目錄物件有關的資料。

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)包含 [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format)格式的資料。 **CFSTR \_ DSOBJECTNAMES** 資料格式是包含 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)結構的 **HGLOBAL** 。 **DSOBJECTNAMES** 結構包含屬性工作表延伸模組所套用的目錄物件資料。

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)也包含 [**CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項**](cfstr-ds-display-spec-options.md)格式的資料。 **CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項** 資料格式是包含 [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)結構的 **HGLOBAL** 。 **DSDISPLAYSPECOPTIONS** 包含延伸模組所使用的設定資料。

如果從 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)傳回 **S \_ OK** 以外的任何值，就不會顯示內容表。

不會使用 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 *pidlFolder* 和 *hkeyProgID* 參數。

擴充功能可以藉由遞增 **IDataObject** 的參考計數來儲存 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標。 此介面必須在不再需要時釋放。

## <a name="implementing-ishellpropsheetext"></a>執行 IShellPropSheetExt

[**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)傳回之後，會呼叫 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法。 屬性工作表延伸模組必須在此方法期間加入頁面。 藉由填滿 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) 結構，然後將此結構傳遞至 [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式，即可建立屬性頁。 然後藉由呼叫 *lpfnAddPage* 參數中傳遞給 **IShellPropSheetExt：： AddPages** 的回呼函式，將屬性頁加入至屬性工作表。

如果從 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)傳回 **S \_ [確定]** 以外的任何值，則不會顯示內容表。

如果不需要屬性工作表延伸模組將任何頁面加入至屬性工作表，它就不應該在 *lpfnAddPage* 參數中呼叫傳遞給 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)的回呼函數。

未使用 [**IShellPropSheetExt：： ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) 方法。

## <a name="passing-the-extension-object-to-the-property-page"></a>將延伸模組物件傳遞給屬性頁

屬性工作表延伸物件是獨立于屬性頁的。 在許多情況下，最好能夠從屬性頁使用擴充物件或其他物件。 若要這樣做，請將 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2)結構的 **lParam** 成員設定為物件指標。 然後，屬性頁面會在處理 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) 訊息時，取得此值。 在屬性頁中， **WM \_ INITDIALOG** 訊息的 *lParam* 參數是 **PROPSHEETPAGE** 結構的指標。 將 **WM \_ INITDIALOG** 訊息的 *lParam* 轉換為 **PROPSHEETPAGE** 指標，然後取得 **PROPSHEETPAGE** 結構的 **lParam** 成員，以抓取物件指標。

下列 c + + 程式碼範例示範如何將物件傳遞給屬性頁。


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



請注意，在呼叫 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 之後，屬性工作表會釋出屬性工作表延伸物件，而且永遠不會再使用它。 這表示會在顯示內容頁之前刪除擴充物件。 當頁面嘗試存取物件指標時，記憶體將會釋出，且指標無效。 若要更正這個錯誤，請在加入頁面時遞增擴充物件的參考計數，然後在屬性頁對話方塊終結時釋放物件。 這會造成另一個問題，因為在第一次顯示頁面之前，不會建立 [屬性頁] 對話方塊。 如果使用者從未選取 [延伸] 頁面，則永遠不會建立和終結頁面。 這會導致擴充物件永遠無法釋出，因此會發生記憶體流失。 若要避免這種情況，請執行屬性頁回呼函數。 若要這樣做，請 **將 \_ PSP USECALLBACK** 旗標加入至 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2)結構的 **dwFlags** 成員，然後將 **PROPSHEETPAGE** 結構的 **pfnCallback** 成員設定為所實 [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)函數的位址。 當 **PropSheetPageProc** 函式收到 **PSPCB \_ 發行** 通知時， **PropSheetPageProc** 的 *ppsp* 參數會包含 **PROPSHEETPAGE** 結構的指標。 **PROPSHEETPAGE** 結構的 **lParam** 成員包含可用於釋放物件的延伸模組指標。

下列 c + + 程式碼範例示範如何釋放擴充物件。


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>使用通知物件

由於屬性工作表延伸頁面會顯示在延伸模組未知元件所建立的屬性工作表中，因此必須使用「管理員」來處理延伸模組頁面與屬性工作表之間的資料傳輸。 此「管理員」稱為通知物件。 通知物件在個別頁面與屬性工作表之間會以仲裁者的形式運作。

當屬性工作表延伸模組物件初始化時，擴充功能必須藉由呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)來建立通知物件，並傳遞從 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)取得的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)和目錄物件名稱。 不需要遞增 **IDataObject** 介面的參考計數，因為 **ADsPropCreateNotifyObj** 函數所建立的通知物件將會執行這項作業。 應儲存 **ADsPropCreateNotifyObj** 提供的通知物件控制碼，以供稍後使用。 **ADsPropCreateNotifyObj** 可以在 **IShellExtInit：： Initialize** 或 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)期間呼叫。 當屬性工作表擴充功能關閉時，它必須將 [**WM \_ ADSPROP \_ 通知 \_**](wm-adsprop-notify-exit.md) 結束訊息傳送給通知物件。 這會導致通知物件自行終結。 當 [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 函式收到 **PSPCB \_ 發行** 通知時，最好這麼做。

除了呼叫 [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)所提供的 [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format)剪貼簿格式之外，屬性工作表延伸模組也可以取得資料。 使用 **ADsPropGetInitInfo** 的優點之一，就是它會提供用來以程式設計方式處理目錄物件的 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 物件。

> [!Note]  
> 不同于大部分的 COM 方法與函數， [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) 不會遞增 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 物件的參考計數。 除非先手動遞增參考計數，否則不得釋放 **IDirectoryObject** 。

 

當您第一次建立屬性頁時，擴充功能應該使用頁面的視窗控制碼呼叫 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) ，以向通知物件註冊頁面。

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) 是一個公用程式函式，可讓屬性工作表延伸模組用來判斷是否可以寫入屬性。

## <a name="miscellaneous"></a>其他

屬性頁的控制碼會傳遞至頁面對話方塊程式。 屬性工作表是屬性頁的直接父系，因此可以藉由呼叫 [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) 函數與屬性頁控制碼來取得屬性工作表的控制碼。

當延伸模組頁面的內容變更時，擴充功能應該使用 [**PropSheet \_ 已變更**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) 宏來通知屬性工作表變更。 屬性工作表接著會啟用 [套用] 按鈕。

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection 屬性工作表

使用 Windows Server 2003 和更新版本的作業系統時，Active Directory 的管理 MMC 嵌入式管理單元，可支援多個目錄物件的屬性工作表延伸模組。 當您一次查看一個以上的專案的屬性時，就會顯示這些屬性工作表。 單一選取屬性工作表延伸和多重選取屬性工作表延伸模組之間的主要差異在於 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)中的 [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format)剪貼簿格式所提供的 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)結構將會包含一個以上的 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)結構。

建立通知物件時，多重選取屬性工作表延伸模組必須傳遞嵌入式管理單元所提供的唯一名稱，而不是延伸模組所建立的名稱。 若要取得唯一的名稱，請從 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)取得的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)要求 [**CFSTR \_ DS \_ MULTISELECTPROPPAGE**](cfstr-ds-multiselectproppage.md)剪貼簿格式。 這項資料是包含以 null 終止之 Unicode 字串的 **HGLOBAL** ，此字串是唯一的名稱。 然後，這個唯一名稱會傳遞至 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) 函式以建立通知物件。 [範例程式碼](example-code-for-implementation-of-the-property-sheet-com-object.md)中的 **CreateADsNotificationObject** 範例函式會示範如何正確地執行此作業，以及與不支援多重選取屬性工作表的舊版嵌入式管理單元相容。

針對多重選取的屬性工作表，系統只會系結至 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 陣列中的第一個物件。 因此， [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) 只會針對陣列中的第一個物件提供 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 和可寫入屬性。 陣列中的其他物件不會系結至。

在 [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) 屬性下註冊了多重選取的屬性工作表延伸。

## <a name="new-with-windows-server-2003"></a>Windows Server 2003 的新

以下是 Windows Server 2003 的新功能。

如果屬性頁遇到錯誤，則可以使用適當的錯誤資料來呼叫 [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) 。 **ADsPropSendErrorMessage** 會將所有錯誤訊息儲存在佇列中。 下次呼叫 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) 時，就會顯示這些訊息。 當 **ADsPropShowErrorDialog** 傳回時，會刪除已排入佇列的訊息。

Windows Server 2003 引進 [**ADsPropSetHwndWithTitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) 函式。 此函式類似于 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)，但包含頁面標題。 這會啟用 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) 所顯示的錯誤對話方塊，以提供更多有用的資料給使用者。 如果屬性工作表擴充功能使用 **ADsPropShowErrorDialog** 函式，則此延伸模組應使用 **ADsPropSetHwndWithTitle** 而不是 **ADsPropSetHwnd**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性工作表 COM 物件的執行範例程式碼](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 