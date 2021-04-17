---
title: 使用剪貼簿
description: 本節包含下列工作的程式碼範例
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- 剪貼簿，資料剪下
- 剪貼簿，複製資料
- 剪貼簿，貼上資料
- 剪貼簿，選取資料
- 剪貼簿、編輯功能表命令
- 剪貼簿，檢視器
- 剪貼簿，檢視器視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315460"
---
# <a name="using-the-clipboard"></a>使用剪貼簿

本節包含下列工作的程式碼範例：

-   [執行剪下、複製和貼上命令](#implementing-the-cut-copy-and-paste-commands)
    -   [選取資料](#selecting-data)
    -   [建立編輯功能表](#creating-an-edit-menu)
    -   [處理 WM \_ INITMENUPOPUP 訊息](#processing-the-wm_initmenupopup-message)
    -   [處理 WM \_ 命令訊息](#processing-the-wm_command-message)
    -   [將資訊複製到剪貼簿](#copying-information-to-the-clipboard)
    -   [從剪貼簿貼上資訊](#pasting-information-from-the-clipboard)
    -   [註冊剪貼簿格式](#registering-a-clipboard-format)
    -   [處理 WM \_ RENDERFORMAT 和 WM \_ RENDERALLFORMATS 訊息](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [處理 WM \_ DESTROYCLIPBOARD 訊息](#processing-the-wm_destroyclipboard-message)
    -   [使用 Owner-Display 剪貼簿格式](#using-the-owner-display-clipboard-format)
-   [監視剪貼簿內容](#monitoring-clipboard-contents)
-   [查詢剪貼簿序號](#querying-the-clipboard-sequence-number)
-   [建立剪貼簿格式接聽程式](#creating-a-clipboard-format-listener)
-   [建立剪貼簿檢視器視窗](#creating-a-clipboard-viewer-window)
-   [將視窗加入至剪貼簿檢視器鏈](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [處理 WM \_ CHANGECBCHAIN 訊息](#processing-the-wm_changecbchain-message)
    -   [從剪貼簿檢視器鏈中移除視窗](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [處理 WM \_ DRAWCLIPBOARD 訊息](#processing-the-wm_drawclipboard-message)
    -   [剪貼簿檢視器的範例](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>執行剪下、複製和貼上命令

本節說明如何在應用程式中執行標準 **剪** 下、 **複製** 和 **貼** 上命令。 本節中的範例會使用這些方法，使用已註冊的剪貼簿格式、 **cf \_ OWNERDISPLAY** 格式和 **cf \_ 文字** 格式，將資料放在剪貼簿上。 註冊的格式是用來表示矩形或橢圓形文字視窗，稱為標籤。

### <a name="selecting-data"></a>選取資料

在可以將資訊複製到剪貼簿之前，使用者必須選取要複製或剪下的特定資訊。 應用程式應該提供方法讓使用者選取檔中的資訊，並提供某種視覺回饋以表示選取的資料。

### <a name="creating-an-edit-menu"></a>建立編輯功能表

應用程式應該載入包含 [ **編輯** ] 功能表命令之標準鍵盤加速器的快速鍵對應表。 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)函式必須加入至應用程式的訊息迴圈，加速器才會生效。 如需鍵盤快速鍵盤的詳細資訊，請參閱 [鍵盤快捷](/windows/desktop/menurc/keyboard-accelerators)鍵。

### <a name="processing-the-wm_initmenupopup-message"></a>處理 WM \_ INITMENUPOPUP 訊息

並非所有的剪貼簿命令都可在任何指定時間提供給使用者使用。 應用程式應該處理 [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) 訊息，以啟用功能表項目來取得可用的命令，並停用無法使用的命令。

以下是名為 Label 的應用程式的 [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) 案例。


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



InitMenu 函數的定義如下。


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a>處理 WM \_ 命令訊息

若要處理功能表命令，請將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 案例新增至您應用程式的主視窗程式。 以下是標籤應用程式視窗程式的 **WM \_ 命令** 案例。


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



為了執行 **複製** 和 **剪** 下命令，視窗程式會呼叫應用程式定義的 EditCopy 函數。 如需詳細資訊，請參閱 [將資訊複製到剪貼](#copying-information-to-the-clipboard)簿。 為了執行 [ **貼** 上] 命令，視窗程式會呼叫應用程式定義的 EditPaste 函數。 如需 EditPaste 函數的詳細資訊，請參閱 [從剪貼簿貼上資訊](#pasting-information-from-the-clipboard)。

### <a name="copying-information-to-the-clipboard"></a>將資訊複製到剪貼簿

在 Label 應用程式中，應用程式定義的 EditCopy 函式會將目前的選取範圍複製到剪貼簿。 此函式會執行下列工作：

1.  藉由呼叫 [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) 函數來開啟剪貼簿。
2.  藉由呼叫 [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) 函數來清空剪貼簿。
3.  針對應用程式所提供的每個剪貼簿格式呼叫 [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) 函數一次。
4.  藉由呼叫 [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) 函數來關閉剪貼簿。

根據目前的選取範圍，EditCopy 函式會複製某範圍的文字，或複製代表整個標籤的應用程式定義結構。 結構稱為 LABELBOX，定義如下。


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



以下是 EditCopy 函數。


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a>從剪貼簿貼上資訊

在 Label 應用程式中，應用程式定義的 EditPaste 函式會貼上剪貼簿的內容。 此函式會執行下列工作：

1.  藉由呼叫 [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) 函數來開啟剪貼簿。
2.  判斷要抓取的可用剪貼簿格式。
3.  藉由呼叫 [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) 函數，以選取的格式抓取資料的控制碼。
4.  將資料的複本插入檔中。

    [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata)所傳回的控制碼仍由剪貼簿所擁有，因此應用程式不得釋出或保持鎖定。

5.  藉由呼叫 [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) 函數來關閉剪貼簿。

如果選取標籤並包含插入點，EditPaste 函式就會在插入點插入剪貼簿中的文字。 如果沒有選取專案，或選取標籤，則函式會使用剪貼簿上的應用程式定義 LABELBOX 結構來建立新的標籤。 LABELBOX 結構會使用已註冊的剪貼簿格式放置在剪貼簿上。

結構稱為 LABELBOX，定義如下。


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



以下是 EditPaste 函數。


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a>註冊剪貼簿格式

若要註冊剪貼簿格式，請將 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函式的呼叫新增至您應用程式的實例初始化函數，如下所示。


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>處理 WM \_ RENDERFORMAT 和 WM \_ RENDERALLFORMATS 訊息

如果視窗將 **Null** 控制碼傳遞至 [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) 函式，它必須處理 [**wm \_ RENDERFORMAT**](wm-renderformat.md) 和 [**wm \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息，以在要求時轉譯資料。

如果視窗延遲轉譯特定格式，而另一個應用程式要求該格式的資料，則會將 [**WM \_ RENDERFORMAT**](wm-renderformat.md) 訊息傳送至視窗。 此外，如果視窗延遲轉譯一或多個格式，而且這些格式的某些格式在視窗即將終結時仍會 unrendered，則會在其終結之前將 [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息傳送至視窗。

若要轉譯剪貼簿格式，視窗程式應該使用 [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata)函式，在剪貼簿上放置非 **Null** 的資料控制碼。 如果視窗程式正在轉譯格式以回應 [**WM \_ RENDERFORMAT**](wm-renderformat.md) 訊息，則在呼叫 **SetClipboardData** 之前，它不能開啟剪貼簿。 但是，如果它正在轉譯一或多個格式以回應 [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息，則必須開啟剪貼簿，並檢查視窗是否仍擁有剪貼簿，然後再呼叫 **SetClipboardData**，而且必須先關閉剪貼簿，然後再返回。

標籤應用程式會處理 [**wm \_ RENDERFORMAT**](wm-renderformat.md) 和 [**wm \_ RENDERALLFORMATS**](wm-renderallformats.md) 訊息，如下所示。


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



在這兩種情況下，視窗程式都會呼叫應用程式定義的 RenderFormat 函數，定義如下。

結構稱為 LABELBOX，定義如下。


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a>處理 WM \_ DESTROYCLIPBOARD 訊息

視窗可以處理 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息，以釋出任何設定的資源，以支援延遲的轉譯。 例如，Label 應用程式，將標籤複製到剪貼簿時，會配置本機記憶體物件。 然後，它會釋出這個物件以回應 **WM \_ DESTROYCLIPBOARD** 訊息，如下所示。


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>使用 Owner-Display 剪貼簿格式

如果視窗使用 **CF \_ OWNERDISPLAY** 剪貼簿格式將資訊放置在剪貼簿上，則必須執行下列動作：

-   處理 [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) 訊息。 當您必須重新繪製剪貼簿檢視器視窗的一部分時，此訊息會傳送給剪貼簿擁有者。

-   處理 [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) 訊息。 當剪貼簿檢視器視窗已調整大小或其內容已變更時，就會將此訊息傳送給剪貼簿擁有者。

    通常，視窗會藉由設定 [剪貼簿檢視器] 視窗的滾動位置和範圍，來回應此訊息。 針對此訊息的回應，標籤應用程式也會更新 [剪貼簿檢視器] 視窗的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構。

-   處理 [**wm \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) 和 [**wm \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) 訊息。 當剪貼簿檢視器視窗中發生捲軸事件時，這些訊息會傳送給剪貼簿擁有者。

-   處理 [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) 訊息。 [剪貼簿檢視器] 視窗會將此訊息傳送至應用程式，以取得擁有者顯示格式的名稱。

標籤應用程式的視窗程式會處理這些訊息，如下所示。


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a>監視剪貼簿內容

有三種方式可監視剪貼簿的變更。 最舊的方法是建立剪貼簿檢視器視窗。 Windows 2000 新增了查詢剪貼簿序號的能力，而 Windows Vista 也新增了剪貼簿格式接聽程式的支援。 支援剪貼簿檢視器視窗，以提供與舊版 Windows 的回溯相容性。 新程式應該使用剪貼簿格式接聽程式或剪貼簿序號。

## <a name="querying-the-clipboard-sequence-number"></a>查詢剪貼簿序號

每次剪貼簿的內容變更時，就會遞增稱為「剪貼簿」序號的32位值。 程式可以藉由呼叫 [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) 函式來取得目前的剪貼簿序號。 藉由比較傳回的值與前一次呼叫 **GetClipboardSequenceNumber** 所傳回的值，程式可以判斷剪貼簿內容是否已變更。 這個方法更適合用來根據目前剪貼簿內容快取結果的程式，並且需要知道計算是否仍然有效，再使用該快取的結果。 請注意，這不是通知方法，不應該用於輪詢迴圈中。 若要在剪貼簿內容變更時收到通知，請使用剪貼簿格式接聽程式或剪貼簿檢視器。

## <a name="creating-a-clipboard-format-listener"></a>建立剪貼簿格式接聽程式

剪貼簿格式接聽程式是已註冊的視窗，會在剪貼簿的內容變更時收到通知。 建議您不要建立剪貼簿檢視器視窗，因為如果程式無法適當地維護剪貼簿檢視器鏈，或剪貼簿檢視器鏈中的視窗停止回應訊息，則建議使用這個方法。

視窗會藉由呼叫 [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) 函式，將其註冊為剪貼簿格式接聽程式。 當剪貼簿的內容變更時，此視窗會張貼至 [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) 訊息。 註冊會維持有效，直到視窗透過呼叫 [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) 函式取消註冊本身為止。

## <a name="creating-a-clipboard-viewer-window"></a>建立剪貼簿檢視器視窗

[剪貼簿檢視器] 視窗會顯示剪貼簿的目前內容，並在剪貼簿內容變更時收到訊息。 若要建立剪貼簿檢視器視窗，您的應用程式必須執行下列動作：

-   將視窗加入至剪貼簿檢視器鏈。
-   處理 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息。
-   處理 [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 訊息。
-   在終結之前從剪貼簿檢視器中移除視窗。

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>將視窗加入至剪貼簿檢視器鏈

視窗會藉由呼叫 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函式，將本身新增至剪貼簿檢視器鏈。 傳回值是鏈中下一個視窗的控制碼。 視窗必須追蹤此值（例如，將它儲存在名為 *hwndNextViewer* 的靜態變數中）。

下列範例會將視窗新增到剪貼簿檢視器鏈，以回應 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息。


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



下列工作會顯示程式碼片段：

-   [處理 WM \_ CHANGECBCHAIN 訊息](/windows)
-   [從剪貼簿檢視器鏈中移除視窗](#removing-a-window-from-the-clipboard-viewer-chain)
-   [處理 WM \_ DRAWCLIPBOARD 訊息](/windows)
-   [剪貼簿檢視器的範例](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>處理 WM \_ CHANGECBCHAIN 訊息

當另一個視窗從剪貼簿檢視器鏈中移除時，[剪貼簿檢視器] 視窗會收到 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息。 如果要移除的視窗是鏈中的下一個視窗，則接收訊息的視窗必須將下一個視窗與鏈中斷連結。 否則，此訊息應該傳遞至鏈中的下一個視窗。

下列範例會顯示 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息的處理。


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>從剪貼簿檢視器鏈中移除視窗

為了從剪貼簿檢視器鏈中移除本身，視窗會呼叫 [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) 函數。 下列範例會從剪貼簿檢視器鏈中移除視窗，以回應 [**WM \_**](/windows/desktop/winmsg/wm-destroy) 終結訊息。


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>處理 WM \_ DRAWCLIPBOARD 訊息

[**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md)訊息會通知剪貼簿檢視器視窗，表示剪貼簿的內容已變更。 處理 **WM \_ DRAWCLIPBOARD** 訊息時，視窗應該執行下列作業：

1.  決定要顯示哪些可用的剪貼簿格式。
2.  取出剪貼簿資料，並將它顯示在視窗中。 或者，如果剪貼簿格式為 **CF \_ OWNERDISPLAY**，請將 [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) 訊息傳送給剪貼簿擁有者。
3.  將訊息傳送至剪貼簿檢視器鏈中的下一個視窗。

如需處理 [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 訊息的範例，請參閱 [剪貼簿檢視器範例](#example-of-a-clipboard-viewer)中的清單範例。

### <a name="example-of-a-clipboard-viewer"></a>剪貼簿檢視器的範例

下列範例顯示簡單的剪貼簿檢視器應用程式。


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 