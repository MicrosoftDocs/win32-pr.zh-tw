---
title: 如何自訂工具列
description: 大部分的 Windows 應用程式都使用工具列控制項，讓使用者能夠輕鬆存取程式功能。
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104023192"
---
# <a name="how-to-customize-toolbars"></a>如何自訂工具列

大部分的 Windows 應用程式都使用工具列控制項，讓使用者能夠輕鬆存取程式功能。 不過，靜態工具列有一些缺點，例如，沒有足夠的空間可有效顯示所有可用的工具。 解決此問題的方法是讓應用程式的工具列成為使用者可自訂的。 然後，使用者可以選擇只顯示所需的工具，並以適合其個人工作型態的方式來組織它們。

> [!Note]  
> 對話方塊中的工具列無法自訂。

 

若要啟用自訂，請在建立工具列控制項時，加入 [**CCS 可 \_ 調整**](common-control-styles.md) 的通用控制項樣式旗標。 自訂的基本方法有兩種：

-   [自訂] 對話方塊。 這個系統提供的對話方塊是最簡單的方法。 它可為使用者提供圖形化使用者介面，讓他們可以新增、刪除或移動圖示。
-   拖放工具。 執行拖放功能，可讓使用者將工具移至工具列上的另一個位置，或將其拖曳至工具列上以將其刪除。 它為使用者提供快速且輕鬆的方式來組織其工具列，但不允許他們新增工具。

您可以根據應用程式的需求，執行任一種方法或兩者。 這兩種自訂方法都不會提供內建機制（例如 [取消] 或 [復原] 按鈕），讓工具列回到先前的狀態。 您必須明確地使用工具列控制項 API 來儲存工具列的 precustomization 狀態。 如有必要，您可以在稍後使用此儲存的資訊，將工具列還原為其原始狀態。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="customization-dialog-box"></a>自訂對話方塊

[自訂] 對話方塊是由工具列控制項提供，可讓使用者以簡單的方式加入、移動或移除工具。 使用者可以按兩下工具列來啟動它。 應用程式可以藉由傳送一個 [**TB \_ 自訂**](tb-customize.md) 訊息的工具列控制項，以程式設計方式啟動 [自訂] 對話方塊。

下圖顯示 [工具列自訂] 對話方塊的範例。

![具有三個專案工具列之視窗的螢幕擷取畫面，以及一個對話方塊，其中包含 [可用] 和 [目前] 工具列按鈕的清單](images/tb-customdlg.png)

右邊清單方塊中的工具是目前在工具列上的工具。 一開始，此清單將包含您在建立工具列時所指定的工具。 左邊的清單方塊包含可新增至工具列的工具。 您的應用程式會負責將清單填入 (除了分隔符號之外，它會自動) 。

Toolbar 控制項會透過傳送 [TBN \_ BEGINADJUST](tbn-beginadjust.md) 通知碼，後面接著 [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) 通知碼的父視窗，來通知您的應用程式正在啟動自訂對話方塊。 在大多數情況下，應用程式不需要回應這些通知代碼。 但是，如果您不想要 [自訂工具列] 對話方塊顯示 [說明] 按鈕，請藉由傳回 TBNRF HIDEHELP 來處理 TBN \_ INITCUSTOMIZE \_ 。

工具列控制項接著會依下列順序傳送三系列通知碼，以收集初始化對話方塊所需的資訊：

-   工具列上的每個按鈕的 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 通知碼，以決定可以插入按鈕的位置。 傳回 **FALSE** 以防止在通知訊息中指定的按鈕左邊插入按鈕。 如果您對所有 TBN \_ QUERYINSERT 通知碼傳回 FALSE，則不會顯示此對話方塊。
-   [TBN 會 \_ QUERYDELETE](tbn-querydelete.md)目前在工具列上的每個工具的通知碼。 如果可以移除工具，則傳回 **TRUE** ，否則傳回 **FALSE** 。
-   一系列的 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 通知程式碼，用來填入可用按鈕的清單。 若要將按鈕加入至清單，請填入以通知碼傳遞的 [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) 結構，並傳回 **TRUE**。 當您沒有其他工具可新增時，會傳回 **FALSE**。 請注意，您可以傳回工具列上已有按鈕的資訊;這些按鈕將不會新增至清單。

接著會顯示對話方塊，而且使用者可以開始自訂工具列。

當對話方塊開啟時，您的應用程式可以根據使用者的動作收到各種通知碼：

-   [TBN \_QUERYINSERT](tbn-queryinsert.md)。 使用者已變更工具列上的工具位置或新增工具。 傳回 **FALSE** 以防止工具插入至該位置。
-   [TBN \_DELETINGBUTTON](tbn-deletingbutton.md)。 使用者即將從工具列移除工具。
-   [TBN \_CUSTHELP](tbn-custhelp.md)。 使用者按一下 [說明] 按鈕。
-   [TBN \_TOOLBARCHANGE](tbn-toolbarchange.md)。 使用者已新增、移動或移除工具。
-   [TBN \_重設](tbn-reset.md)。 使用者按一下 [重設] 按鈕。

終結對話方塊之後，您的應用程式將會收到 [TBN \_ ENDADJUST](tbn-endadjust.md) 通知碼。

下列程式碼範例示範一個方法來執行工具列自訂。


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>拖放工具

使用者也可以按下 SHIFT 鍵，然後將按鈕拖曳到另一個位置，來重新排列工具列上的按鈕。 拖放進程會由工具列控制項自動處理。 它會在拖曳時顯示按鈕的准刪除影像，並在卸載後重新排列工具列。 使用者無法以這種方式加入按鈕，但可以藉由將按鈕放在工具列上來刪除按鈕。

雖然工具列控制項通常會自動執行此作業，但它也會將您的應用程式傳送至兩個通知碼： [TBN \_ QUERYDELETE](tbn-querydelete.md) 和 [TBN \_ QUERYINSERT](tbn-queryinsert.md)。 若要控制拖放程式，請依照下列方式處理這些通知碼：

-   [TBN \_ QUERYDELETE](tbn-querydelete.md)通知碼會在使用者嘗試移動按鈕時立即傳送，然後才會顯示 [准刪除] 按鈕。 傳回 **FALSE** 以防止移動按鈕。 如果您傳回 **TRUE**，則使用者將可以移動工具或將它刪除，方法是將它放在工具列上。 如果工具可以移動，就可以將它刪除。 不過，如果使用者移除工具，工具列控制項會將 [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) 通知程式碼傳送給您的應用程式，此時您可以選擇在其原始位置重新插入按鈕，藉此取消刪除。
-   當使用者嘗試在工具列上放置按鈕時，會傳送 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 通知碼。 若要防止將移動的按鈕放在通知中所指定按鈕的左邊，請傳回 **FALSE**。 如果使用者將工具從工具列卸載，則不會傳送此通知碼。

如果使用者嘗試拖曳按鈕，但未按下 SHIFT 鍵，工具列控制項將不會處理拖放作業。 不過，它會將 [TBN \_ BEGINDRAG](tbn-begindrag.md) 通知程式碼傳送給您的應用程式，以指示開始拖曳作業，並使用 [TBN \_ ENDDRAG](tbn-enddrag.md) 通知碼來指出結尾。 如果您想要啟用這種形式的拖放，您的應用程式必須處理這些通知代碼、提供必要的使用者介面，以及修改工具列以反映任何變更。

### <a name="saving-and-restoring-toolbars"></a>儲存和還原工具列

在自訂工具列的過程中，您的應用程式可能需要儲存資訊，讓您可以將工具列還原為其原始狀態。 若要起始儲存或還原工具列狀態，請將 *lParam* 設定為 **TRUE** 的 [**\_ SAVERESTORE**](tb-saverestore.md)訊息傳送給 toolbar 控制項。 此訊息的 *lParam* 值會指定您是否要要求儲存或還原作業。 傳送訊息之後，有兩種方式可以處理儲存/還原作業：

-   使用通用控制項 [4.72 版](common-control-versions.md) 和更舊版本，您必須執行 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 處理常式。 工具列控制項會傳送此通知碼，以要求每個按鈕還原時的相關資訊。
-   5.80 版包含儲存/還原選項。 在程式開始時，您的應用程式會在儲存或還原每個按鈕時收到 [TBN \_ 儲存](tbn-save.md) 或 [TBN \_ 還原](tbn-restore.md) 通知碼。 若要使用此選項，您必須執行通知處理常式，以提供成功儲存或還原工具列狀態所需的點陣圖和狀態資訊。

工具列狀態會儲存在資料流程中，其中包含與應用程式定義資料區塊相關聯的 Shell 定義資料區塊。 每個按鈕都會儲存每個類型的一個資料區塊，以及一個選擇性的全域資料區塊，應用程式可以在資料流程的開頭放置這些資料。 在儲存程式期間，您的 [TBN \_ 儲存](tbn-save.md) 處理常式會將應用程式定義的區塊新增至資料流程。 在還原過程中， [TBN \_ 還原](tbn-restore.md) 處理常式會讀取每個區塊，並為 Shell 提供重建工具列所需的資訊。

### <a name="how-to-handle-a-tbn_save-notification"></a>如何處理 TBN \_ 儲存通知

第一個 [TBN \_ 儲存](tbn-save.md) 通知程式碼會在儲存程式的開頭傳送。 儲存任何按鈕之前， [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) 結構的成員設定如下表所示。



| 成員       | 設定                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Shell 定義資料所需的記憶體數量。                                                                                                                                                                                                                                                                                                |
| **cButtons** | 按鈕的數目。                                                                                                                                                                                                                                                                                                                             |
| **.Pdata**    | 應用程式定義資料所需的記憶體計算量。 一般而言，您會包含一些全域資料，再加上每個按鈕的資料。 將該值新增至 **cbData** ，並將足夠的記憶體配置給 **.pdata** ，以將其全部保存。                                                                                                                      |
| **pCurrent** | 資料流程中第一個未使用的位元組。 如果您不需要全域工具列資訊，請設定 **pCurrent**  =  **.pdata** ，使它指向資料流程的開頭。 如果您確實需要全域工具列資訊，請將它儲存在 **.pdata**，然後將 **pCurrent** 設定為數據串流未使用部分的開頭，然後再返回。 |



 

如果您想要新增一些全域工具列資訊，請將它放在資料流程的開頭。 前進 **pCurrent** 至全域資料的結尾，使其指向資料流程未使用部分的開頭，然後傳回。

傳回之後，Shell 會開始儲存按鈕資訊。 它會在 **pCurrent** 的第一個按鈕新增 Shell 定義的資料，然後將 **pCurrent** 前進到未使用部分的開頭。

儲存每個按鈕之後，會傳送 [TBN \_ 儲存](tbn-save.md) 通知碼，而且會傳回 [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) ，並將這些成員設定如下。



| 成員                       | 設定                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | 按鈕編號的以零為起始的索引。                                                                                                                                                                                                                           |
| **pCurrent**                 | 資料流程中第一個未使用之位元組的指標。 如果您想要儲存按鈕的其他相關資訊，請將它儲存在 **pCurrent** 所指向的位置，並更新 **pCurrent** 以指向該資料串流的第一個未使用部分。 |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | 描述正在儲存之按鈕的 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構。                                                                                                                                                                              |



 

當您收到通知碼時，您應該從 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)中解壓縮任何您需要的按鈕特定資訊。 請記住，當您新增按鈕時，可以使用 **TBBUTTON** 的 **dwData** 成員來保存應用程式特定資料。 將您的資料載入資料流程的 **pCurrent**。 將 **pCurrent** 向前移至資料的結尾，再次指向資料流程未使用部分的開頭，然後返回。

Shell 接著移至 [下一步] 按鈕，將其資訊新增至 [ **.pdata**]、[前進 **pCurrent**]、[載入 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)]，然後傳送另一個 [TBN \_ 儲存](tbn-save.md) 通知碼。 此程式會繼續進行，直到儲存所有按鈕為止。

### <a name="restoring-saved-toolbars"></a>還原已儲存的工具列

還原程式基本上會反轉儲存流程。 一開始，您的應用程式將會收到 [TBN \_ 還原](tbn-restore.md)通知碼，其中 [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)結構的 **iItem** 成員會設定為–1。 **CbData** 成員會設定為 **.pdata** 的大小，而 **cButtons** 會設定為按鈕數目。

您的通知處理常式應該將在儲存期間放置於 **.pdata** 開頭的全域資訊解壓縮，並將 **PCurrent** 前進到 Shell 定義資料的第一個區塊的開頭。 將 **cBytesPerRecord** 設定為您用來儲存按鈕資料的資料區塊大小。 將 **cButtons** 設定為按鈕數目，然後傳回。

下一個 [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) 是第一個按鈕。 **PCurrent** 成員指向第一個按鈕資料區塊的開頭，而 **iItem** 則設定為按鈕索引。 將該資料解壓縮，並繼續 **pCurrent**。 將資料載入 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)中，然後傳回。 若要從還原的工具列省略按鈕，請將 **TBBUTTON** 的 **idCommand** 成員設定為零。 Shell 會針對其餘按鈕重複此程式。 除了 [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) 和 **NMTBRESTORE** 訊息以外，您也可以使用像是 [TBN \_ RESET](tbn-reset.md) 的訊息來儲存和還原工具列。

下列程式碼範例會先儲存工具列再進行自訂，並在應用程式收到 [TBN \_ 重設](tbn-reset.md) 訊息時加以還原。


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具列控制項](using-toolbar-controls.md)
</dt> <dt>

[**工具列標準按鈕影像索引值**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




