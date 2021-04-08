---
title: Active Directory 消費者和電腦屬性工作表
description: Active Directory 消費者和電腦 MMC 嵌入式管理單元是設計來顯示 Active Directory 伺服器中各種物件的屬性工作表。
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Active Directory 消費者和電腦屬性工作表廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681699"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Active Directory 消費者和電腦屬性工作表

Active Directory 消費者和電腦 MMC 嵌入式管理單元是設計來顯示 Active Directory 伺服器中各種物件的屬性工作表。 屬性工作表包含一或多個用來查看和修改物件資料的頁面。 不同的物件類型會顯示不同的頁面集合。 Active Directory 消費者和電腦 MMC 嵌入式管理單元也可讓協力廠商廠商將自訂頁面新增至特定物件類型的屬性工作表。 如需詳細資訊，請參閱搭配 [顯示規範使用的屬性頁](property-pages-for-use-with-display-specifiers.md)。

某些應用程式（Active Directory 消費者和電腦 MMC 嵌入式管理單元以外）必須為使用者提供 Active Directory 伺服器中物件的 [查看] 和 [編輯] 屬性的功能。 應用程式可執行自己的屬性工作表，但最好提供一致的使用者介面，以減少混淆和學習時間。 幸運的是，Active Directory 消費者和電腦 MMC 嵌入式管理單元可讓任何 OLE COM 應用程式顯示物件的屬性工作表，該物件等同于相同物件的 Active Directory 消費者和電腦 MMC 嵌入式管理單元所顯示的屬性工作表。

如需裝載 Active Directory 消費者和電腦屬性工作表的詳細資訊和程式碼範例，請參閱平臺軟體發展工具組 (SDK) 中的 PropSheetHost 範例。

## <a name="developer-audience"></a>開發人員讀者

本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。 目前，您無法使用 Visual Basic 來建立 Active Directory 的屬性工作表延伸模組。

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>裝載 Active Directory 消費者和電腦屬性工作表

**在 Active Directory 伺服器中顯示物件的屬性工作表**

1.  建立可以用來處理訊息的視窗。 這可以是現有的視窗或特殊用途的視窗。 這就是所謂的 *隱藏視窗*。
2.  建立衍生自 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)的 OLE COM 物件。 此資料物件必須支援下列資料格式：

    -   [**CFSTR \_DSOBJECTNAMES**](cfstr-dsobjectnames.md) 此資料格式包含可識別屬性工作表所適用之物件的 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 。 裝載屬性工作表時，下列清單會顯示 **DSOBJECTNAMES** 結構的更重要成員。

        **clsidNamespace** 保留。 如果您的應用程式在未來使用，請將此設定為您應用程式的 GUID。
        
        **aObjects** 包含 [**DSBOJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構的陣列。 每個 **DSBOJECT** 結構都代表單一目錄物件。 **CItems** 成員包含陣列中的元素數目。 只會使用這個陣列中的第一個物件。 系統會忽略其他物件。

    -   [**CFSTR \_DSDISPLAYSPECOPTIONS**](cfstr-ds-display-spec-options.md) 此資料格式包含 [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) 結構，其中包含屬性頁將使用的資料，例如從中載入屬性頁的位置、伺服器和要使用的認證等等。 下列清單中會顯示更重要的 **DSDISPLAYSPECOPTIONS** 成員。

        **offsetAttribPrefix** 屬性前置詞字串會決定取得屬性頁清單的位置。 這必須包含下列其中一個字串。

        

        | 屬性前置詞字串 | Description                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | 管理員<br/>      | 屬性頁是從 [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) 屬性載入的。<br/> |
        | shell<br/>      | 屬性頁是從 [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) 屬性載入的。<br/> |

        


    -   [**CFSTR \_DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) 此資料格式包含包含屬性工作表主機資料的 [**PROPSHEETCFG**](propsheetcfg.md) 結構。 裝載屬性工作表時， **PROPSHEETCFG** 結構中較大的成員會包含下列清單中所顯示的資料。

        **lNotifyHandle** 必須為零。
        **hwndParentSheet**  包含視窗的控制碼，可在其中一個頁面中的某個內容變更並套用時，接收 [**WM \_ ADSPROP \_ 通知 \_ 變更**](wm-adsprop-notify-change.md) 訊息。 如果不需要此訊息，則可以是 **Null** 。

        **hwndHidden** 包含視窗的控制碼，可接收 [**WM \_ dsa \_ 工作表 \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md) 和 [**WM \_ dsa \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md) 訊息。 將此設定為隱藏視窗的控制碼。

        **wParamSheetClose** 包含應用程式定義的識別碼，此識別碼會在「 [**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)」訊息的 *wParam* 中傳回。 如果此成員為零，則會將「 **WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知** 」訊息張貼至隱藏視窗。


3.  建立 [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) 物件的實例，並取得物件的 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。 您也可以複製 **CLSID \_ DsPropertyPages** 物件的行為。 如需詳細資訊，請參閱複製 CLSID \_ DsPropertyPages 物件的行為。
4.  藉由呼叫 [**IShellExtInit：： initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法來初始化 [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md)物件。 這個方法不會使用 *pidlFolder* 和 *hkeyProgID* 參數。 *Pdtobj* 參數是在步驟2中建立之資料物件的指標。 呼叫 **IShellExtInit：： Initialize** 方法時， **CLSID \_ DsPropertyPages** 物件將會儲存資料物件的參考。
5.  取得 [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md)物件的 [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)介面，然後呼叫 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法。 *LpfnAddPage* 參數是您必須執行的回呼函式的位址。 此函數的格式如下所示。 如果回呼函式宣告為 c + + 類別的成員，則回呼函數必須宣告為 **static**。 *LParam* 參數是應用程式定義的值，可用來識別實回呼函數的物件。 呼叫 **IShellPropSheetExt：： AddPages** 方法時， **CLSID \_ DsPropertyPages** 物件將會從資料物件取得資料，並列舉針對物件顯示規範所註冊的屬性頁。 **CLSID \_ DsPropertyPages** 物件接著會列舉屬性頁物件，並呼叫每個物件的 **IShellPropSheetExt：： AddPages** 方法。

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  每個由屬性頁物件新增的頁面都會導致呼叫回呼函式時，使用屬性頁的控制碼和應用程式定義的值。 您的回呼函數必須儲存每個傳遞的屬性頁控制碼。 當 [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) 物件的 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 方法傳回時，會透過您的回呼函式加入所有頁面。
7.  填入 [**PROPSHEETHEADER**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) 結構以顯示內容表。 **Phpage** 成員會收到回呼函數所收集之頁面控點陣列的指標。 **NPages** 成員會收到頁面控點陣列中的頁面數目。
8.  藉由呼叫 [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) 函數來顯示內容表。

如果任何頁面中的資料已變更，且按一下 [**確定]** 或 [套用]**按鈕，** 由 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndParentSheet** 成員所識別的視窗就會收到 [**WM \_ ADSPROP \_ 通知 \_ 變更**](wm-adsprop-notify-change.md)訊息。 這則訊息完全是通知，不需要採取任何特定動作。

當頁面關閉時， [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndHidden** 成員所識別的視窗將會收到 [**WM 的 \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)訊息。 這則訊息完全是通知，不需要執行特定動作。

在某些情況下，現有的屬性工作表將需要顯示次要屬性工作表。 例如，如果您顯示使用者物件的屬性工作表，並選取 [ **成員** ] 頁面，則會顯示使用者所屬群組的清單。 如果您按兩下清單中的其中一個群組，則會顯示該群組的屬性工作表。 主要屬性工作表不會單獨顯示次要工作表。 它會要求主機藉由將 [**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md)訊息傳送至 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndHidden** 成員所識別的視窗，來顯示次要工作表。 [ **WM \_ dsa \_ 工作表 \_ 建立 \_ 通知** 訊息] 的 *wParam* 是 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)結構的指標，其中包含次要屬性工作表及其代表物件的相關資訊。 為了回應這則訊息，屬性工作表主機必須以上述方式顯示次要屬性工作表。 處理 **WM \_ DSA \_ 工作表 \_ 建立 \_ 通知** 訊息之後，訊息接收者必須將 *wParam* 值傳遞給 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)函式，以釋放 **DSA \_ SEC \_ 頁面 \_ 資訊** 結構。

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>複製 CLSID DsPropertyPages 物件的行為 \_

**複製 CLSID \_ DsPropertyPages 物件的行為**

1.  列舉物件類別之顯示規範的 [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) 或 [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) 屬性中的值。 每個值都是一個字串，其中包含數位，後面接著逗號，接著是屬性頁延伸的類別識別碼的字串表示。 如需屬性頁的格式顯示規範值的詳細資訊，請參閱 [在顯示規範中註冊屬性頁 COM 物件](registering-the-property-page-com-object-in-a-display-specifier.md)。
2.  使用 [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)函式，將每個類別識別碼字串轉換成 **CLSID** 。
3.  依屬性值中每個類別識別碼字串前面的數位來排序擴充類別識別碼。 如果兩個數字相同，請依照從 Active Directory 伺服器取得屬性值的順序來排序類別識別碼。
4.  列舉擴充類別識別碼，建立每個延伸模組的實例。
5.  針對每個擴充功能，依照上面排序的順序，以裝載 Active Directory 消費者和電腦屬性工作表程式的步驟4中所述的相同資訊，呼叫延伸模組的 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 。
6.  針對每個擴充功能，依照以上排序的順序，以裝載 Active Directory 消費者和電腦屬性工作表程式的步驟5中所述的相同資訊，呼叫延伸模組的 [**IShellPropSheetExt：： AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 。

可能的話，請使用 [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) 物件來建立頁面，而不是手動執行。 **CLSID \_ DsPropertyPages** 已經過優化，而且會正確處理失敗的情況，例如，當目前的地區設定沒有可用的顯示規範時。 此外， **CLSID \_ DsPropertyPages** 物件可能會在未來變更，這表示您的屬性工作表可能不會完全符合 Active Directory 消費者和電腦 MMC 嵌入式管理單元所顯示的內容表。

## <a name="special-programming-elements"></a>特殊程式設計項目

目前，已發行的標頭檔中未定義下列程式設計項目。 若要使用這些專案，您必須以特定參考頁面中顯示的確切格式來定義它們。

-   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
-   [**PROPSHEETCFG**](propsheetcfg.md)
-   [**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md)
-   [**DSA \_ 秒 \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)

## <a name="example-code"></a>範例程式碼

下列 c + + 程式碼範例會示範定義這些專案的安全方式，即使這些專案是在未來已發行的標頭檔中定義，這些元素仍會繼續運作。


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

