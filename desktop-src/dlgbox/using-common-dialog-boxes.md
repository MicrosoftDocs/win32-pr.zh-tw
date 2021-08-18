---
title: 使用通用對話方塊
description: 本節涵蓋叫用通用對話方塊的工作。
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- 通用對話方塊程式庫、工作
- 通用對話方塊，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da09fcc99cdde617c3fbdaf34e4465d9a768b0073c5dbd6d461a19060ca92bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985298"
---
# <a name="using-common-dialog-boxes"></a>使用通用對話方塊

本節涵蓋的工作會叫用通用對話方塊：

-   [選擇色彩](#choosing-a-color)
-   [選擇字型](#choosing-a-font)
-   [開啟檔案](#opening-a-file)
-   [顯示 [列印] 對話方塊](#displaying-the-print-dialog-box)
-   [使用列印屬性工作表](#using-the-print-property-sheet)
-   [設定列印頁面](#setting-up-the-printed-page)
-   [尋找文字](#finding-text)

## <a name="choosing-a-color"></a>選擇色彩

本主題說明顯示 [ **色彩** ] 對話方塊的範例程式碼，讓使用者可以選取色彩。 範例程式碼會先初始化 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構，然後再呼叫 [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 函數來顯示對話方塊。 如果函式傳回 **TRUE**，表示使用者已選取色彩，範例程式碼會使用選取的色彩來建立新的實心筆刷。

這個範例會使用 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構來初始化對話方塊，如下所示：

-   使用值的靜態陣列指標，初始化 **lpCustColors** 成員。 陣列中的色彩一開始是黑色，但是靜態陣列會保留使用者所建立的自訂色彩，以進行後續的 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 呼叫。
-   設定 **CC \_ RGBINIT** 旗標，並初始化 **rgbResult** 成員，以指定對話方塊開啟時最初選取的色彩。 如果未指定，則初始選項為黑色。 此範例會使用 *rgbCurrent* 靜態變數，在 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))的呼叫之間保留選取的值。
-   設定 **CC \_ FULLOPEN** 旗標，因此一律會顯示對話方塊的自訂色彩延伸。


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>選擇字型

本主題說明顯示 [ **字型** ] 對話方塊的範例程式碼，讓使用者可以選擇字型的屬性。 範例程式碼會先初始化 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構，然後再呼叫 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函數來顯示對話方塊。

此範例會設定 **CF \_ SCREENFONTS** 旗標，以指定對話方塊只顯示幕幕字型。 它會設定 **CF \_ 效果** 旗標，以顯示可讓使用者選取刪除線、底線和色彩選項的控制項。

如果 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)傳回 **TRUE**，表示使用者按下 [**確定]** 按鈕， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構就會包含描述使用者所選取之字型和字型屬性的資訊，包括 **lpLogFont** 成員所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的成員。 **RgbColors** 成員包含選取的文字色彩。 範例程式碼會使用此資訊來設定與擁有者視窗相關聯之裝置內容的字型和文字色彩。


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>開啟檔案

> [!Note]  
> 從 Windows Vista 開始，一般的 [檔案] 對話方塊會在用來開啟檔案時由 [一般專案] 對話方塊取代。 建議您使用通用專案對話方塊 API，而不是一般檔案對話 API。 如需詳細資訊，請參閱 [一般專案對話方塊](/windows/win32/shell/common-file-dialog)。

 

本主題說明顯示 [ **開啟** ] 對話方塊的範例程式碼，讓使用者可以指定要開啟之檔案的磁片磁碟機、目錄和名稱。 範例程式碼會先初始化 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構，然後再呼叫 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 函數來顯示對話方塊。

在此範例中， **lpstrFilter** 成員是緩衝區的指標，此緩衝區會指定兩個檔案名篩選器，使用者可以選取這些篩選器來限制所顯示的檔案名。 緩衝區包含雙 null 結束的字串陣列，其中的每一對字串都會指定篩選。 **NFilterIndex** 成員會指定在建立對話方塊時使用第一個模式。

此範例會在 **旗標** 成員中設定 **OFN \_ PATHMUSTEXIST** 和 **OFN \_ FILEMUSTEXIST** 旗標。 這些旗標會在傳回之前，讓對話方塊確認使用者指定的路徑和檔案名確實存在。

如果使用者按一下 [**確定]** 按鈕，且指定的路徑和檔案名存在， [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)函式就會傳回 **TRUE** 。 在此情況下， **lpstrFile** 成員所指向的緩衝區會包含路徑和檔案名。 範例程式碼會在函式的呼叫中使用這項資訊來開啟檔案。

雖然此範例不會設定 **OFN \_ explorer** 旗標，但它仍會顯示預設的 [explorer 樣式 **開啟** ] 對話方塊。 但是，如果您想要提供攔截程式或自訂範本，而且您想要使用 Explorer 使用者介面，則必須設定 **OFN \_ Explorer** 旗標。

> [!Note]  
> 在 C 程式設計語言中，以引號括住的字串會以 null 終止。

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>顯示 [列印] 對話方塊

本主題描述的範例程式碼會顯示 [ **列印** ] 對話方塊，讓使用者可以選取列印檔案的選項。 範例程式碼會先初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構，然後再呼叫 [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數來顯示對話方塊。

這個範例會在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ RETURNDC** 旗 **標**。 這會導致 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 將裝置內容控制碼傳回至 **hDC** 成員中選取的印表機。 您可以使用此控制碼來呈現印表機上的輸出。

在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。 如果函式傳回 **TRUE**，這些成員會傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。 您可以使用這份資訊來準備要傳送到所選印表機的輸出。


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>使用列印屬性工作表

本主題說明顯示 **列印** 屬性工作表的範例程式碼，讓使用者可以選取列印檔案的選項。 範例程式碼會先初始化 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) 結構，然後再呼叫 [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數來顯示內容表。

範例程式碼會在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ RETURNDC** 旗 **標**。 這會導致 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式將裝置內容控制碼傳回至 **hDC** 成員中選取的印表機。

在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。 如果函式傳回 **S \_ OK**，這些成員會傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。 您可以使用這份資訊來準備要傳送到所選印表機的輸出。

完成列印工作之後，範例程式碼會釋出 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)、 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)和 [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) 緩衝區，然後呼叫 [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) 函數來刪除裝置內容。


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>設定列印頁面

本主題說明顯示 [版面 **設定** ] 對話方塊的範例程式碼，讓使用者可以選取列印頁面的屬性，例如紙張類型、紙張來源、頁面方向和頁面邊界。 範例程式碼會先初始化 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構，然後再呼叫 [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函數來顯示對話方塊。

此範例會在 **旗標** 成員中設定 **PSD \_ 邊界** 旗標，並使用 **rtMargin** 成員指定初始邊界值。 它會設定 **PSD \_ INTHOUSANDTHSOFINCHES** 旗標，以確保對話方塊會以一種英寸的萬分之一表示邊界維度。

在輸入時，範例程式碼會將 **hDevMode** 和 **hDevNames** 成員設為 **Null**。 如果函式傳回 **TRUE**，則函式會使用這些成員傳回 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的控制碼，其中包含使用者輸入以及印表機的相關資訊。 您可以使用這份資訊來準備要傳送到所選印表機的輸出。

下列範例也會啟用 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式，以自訂繪製範例頁面的內容。


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



下列範例顯示在範例頁面區域中繪製邊界矩形的範例 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式：


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>尋找文字

本主題描述顯示和管理 [ **尋找** ] 對話方塊的範例程式碼，讓使用者可以指定搜尋作業的參數。 此對話方塊會將訊息傳送至視窗程式，讓您可以執行搜尋作業。

顯示和管理 **取代** 對話方塊的程式碼很類似，不同之處在于它會使用 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函數來顯示對話方塊。 [ **取代** ] 對話方塊也會傳送訊息，以回應使用者按下 [ **取代** ] 和 [ **取代所有** ] 按鈕的動作。

若要使用 [ **尋找** 或 **取代** ] 對話方塊，您必須執行三個不同的工作：

1.  取得 [**FINDMSGSTRING**](findmsgstring.md) 註冊之訊息的訊息識別碼。
2.  顯示對話方塊。
3.  當對話方塊開啟時，處理 [**FINDMSGSTRING**](findmsgstring.md) 訊息。

當您初始化應用程式時，請呼叫 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得 [**FINDMSGSTRING**](findmsgstring.md) 已註冊訊息的訊息識別碼。


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



若要顯示 [ **尋找** ] 對話方塊，請先初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構，然後再呼叫 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 函數。 請注意， **FINDREPLACE** 結構和搜尋字串的緩衝區應該是全域或靜態變數，使其不會在對話方塊關閉之前移出範圍。 您必須設定 **hwndOwner** 成員，以指定接收已註冊之訊息的視窗。 建立對話方塊之後，您可以使用傳回的控制碼來移動或操作該對話方塊。


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



開啟對話方塊時，您的主要訊息迴圈必須包含 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函數的呼叫。 將控制碼傳遞至對話方塊，作為 **IsDialogMessage** 呼叫中的參數。 這樣可確保對話方塊正確處理鍵盤訊息。

若要監視從對話方塊傳送的訊息，您的視窗程式必須檢查 [**FINDMSGSTRING**](findmsgstring.md) 註冊的訊息，並處理在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構中傳遞的值，如下列範例所示。


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
