---
title: 通用對話方塊程式庫
description: 本節討論通用對話方塊程式庫。 通用對話方塊程式庫包含一組用來執行一般工作的對話方塊，例如開啟檔案和列印檔案。
ms.assetid: 28573019-f0bd-4a8e-a1a1-48559f658a81
keywords:
- 通用對話方塊程式庫
- 通用對話方塊
- 預先定義的對話方塊
- 對話方塊、通用對話方塊程式庫
- 開啟對話方塊
- '[另存新檔] 對話方塊'
- 尋找對話方塊
- 取代對話方塊
- 列印對話方塊
- '[列印設定] 對話方塊'
- '[列印屬性工作表] 對話方塊'
- 版面設定對話方塊
- '[色彩] 對話方塊'
- 字型對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1500112af60862f093fedf32f56efba66c6fb0d3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549683"
---
# <a name="common-dialog-box-library"></a>通用對話方塊程式庫

通用對話方塊程式庫包含一組用來執行一般應用程式工作的對話方塊，例如開啟檔案、選擇色彩值，以及列印檔案。 一般對話方塊可讓您對應用程式的使用者介面執行一致的方法。 這可減少使用者針對您的應用程式學慣用戶介面行為所花費的工作量。

本章節描述包含 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊的通用對話方塊;[ **尋找** 和 **取代** 編輯] 對話方塊; **列印**、 **列印設定**、 **列印屬性工作表** 和版面 **設定** 列印對話方塊;和 [ **色彩** ] 和 [ **字型** ] 對話方塊。

> [!Note]  
> 從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。

 

### <a name="in-this-section"></a>本節內容



| 名稱                                                                                 | 描述                                                                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [一般對話方塊類型](dialog-box-types.md)                                      | 討論不同的對話方塊。<br/>                                                      |
| [通用對話方塊初始化旗標](common-dialog-box-initialization-flags.md) | 討論如何使用旗標來修改通用對話方塊的行為和外觀。<br/> |
| [自訂通用對話方塊](customizing-common-dialog-boxes.md)               | 討論如何使用通用對話方塊。<br/>                                                  |
| [使用通用對話方塊](using-common-dialog-boxes.md)                           | 涵蓋叫用通用對話方塊的工作。<br/>                                              |
| [通用對話方塊參考](common-dialog-box-reference.md)                       | 包含 API 參考。<br/>                                                                |



 

### <a name="functions"></a>函式



| 名稱                                                 | 描述                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                       | 接收適用于 [ **色彩** ] 對話方塊之預設對話方塊程式的訊息或通知。 這是應用程式定義的或程式庫定義的回呼函式，可搭配 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 函式使用。<br/>                                                                                                           |
| [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                       | 接收適用于 [ **字型** ] 對話方塊之預設對話方塊程式的訊息或通知。 這是應用程式定義的或程式庫定義的回呼程式，可搭配 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式使用。<br/>                                                                                                             |
| [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))                   | 建立可讓使用者選取色彩的 [ **色彩** ] 對話方塊。<br/>                                                                                                                                                                                                                                                                                        |
| [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)                     | 建立可讓使用者選擇邏輯字型屬性的 [ **字型** ] 對話方塊。 這些屬性包括字型系列和相關聯的字型樣式、點大小、效果 (底線、刪除線和文字色彩) ，以及腳本 (或字元集) 。<br/>                                                                                                  |
| [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) | 傳回通用對話方塊錯誤碼。 此程式碼表示執行其中一個常見對話方塊函式時，最新的錯誤。<br/>                                                                                                                                                                                                     |
| [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)                         | 建立系統定義的無模式 [ **尋找** ] 對話方塊，可讓使用者指定要搜尋的字串，以及搜尋檔中的文字時要使用的選項。<br/>                                                                                                                                                                                              |
| [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                       | 接收訊息或通知，其適用于 [ **尋找** 或 **取代** ] 對話方塊的預設對話方塊程式。 這是應用程式定義的或程式庫定義的回呼函式，可搭配 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 或 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函數使用。<br/>                                                             |
| [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)                 | 抓取指定檔案的名稱。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)           | 建立 [ **開啟** ] 對話方塊，讓使用者指定要開啟之檔案或檔案集合的磁片磁碟機、目錄和名稱。<br/>                                                                                                                                                                                                                                |
| [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)           | 建立可讓使用者指定要儲存的磁片磁碟機、目錄和檔案名的 [ **儲存** ] 對話方塊。<br/>                                                                                                                                                                                                                                                     |
| [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                     | 接收從對話方塊傳送的通知訊息。 函式也會接收您藉由指定子對話方塊範本所定義的任何其他控制項的訊息。 這是應用程式定義的或程式庫定義的回呼函式，可搭配 Explorer 樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊使用。<br/>                               |
| [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))  | 接收適用于對話方塊程式的訊息或通知。 這是應用程式定義的或程式庫定義的回呼函式，可搭配 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊使用。<br/>                                                                                                                                                     |
| [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)                 | 接收訊息，讓您在 [版面 **設定** ] 對話方塊中自訂範例頁面的繪圖。 這是與 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函數搭配使用的應用程式定義或程式庫定義的回呼函式。<br/>                                                                                                                    |
| [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))                 | 建立 [版面 **設定** ] 對話方塊，可讓使用者指定列印頁面的屬性。 這些屬性包括紙張大小和來源、 (縱向或橫向) 的頁面方向，以及頁面邊界的寬度。<br/>                                                                                                                    |
| [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                 | 接收適用于 [版面設定] 對話方塊之預設對話方塊 **程式** 的訊息或通知。 這是與 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))函數搭配使用的應用程式定義或程式庫定義的回呼函式。<br/>                                                                                                              |
| [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))                         | 顯示 [[列印] 對話方塊](print-dialog-box.md)。 [ **列印** ] 對話方塊可讓使用者指定特定列印工作的屬性。<br/>                                                                                                                                                                                                             |
| [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))                     | 顯示 **列印** 屬性工作表，可讓使用者指定特定列印工作的屬性。**列印** 屬性工作表具有 **[一般** ] 頁面，其中包含與 [ **列印** ] 對話方塊類似的控制項。 屬性工作表也可以有其他的應用程式特定和驅動程式特定的屬性頁，以及 **一般** 頁面。<br/> |
| [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                 | 接收適用于 [ **列印** ] 對話方塊之預設對話方塊程式的訊息或通知。 這是應用程式定義的或程式庫定義的回呼函式，可搭配 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式使用。<br/>                                                                                                                 |
| [**Replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)                   | 建立系統定義的非強制回應對話方塊，讓使用者指定要搜尋的字串和取代字串，以及控制尋找和取代作業的選項。<br/>                                                                                                                                                                        |
| [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)                 | 搭配 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式使用的應用程式定義或程式庫定義的回呼函數。 攔截程式會接收適用于 [ **列印設定** ] 對話方塊之預設對話方塊程式的訊息或通知。<br/>                                                                                                        |



 

### <a name="interfaces"></a>介面



| 名稱                                                 | 描述                                                                                                                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) | 提供可讓應用程式在顯示 [列印屬性工作表](print-property-sheet.md)時，從 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式接收通知和訊息的方法。<br/> |
| [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) | 提供的方法，可讓使用 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式的應用程式取得目前所選印表機的相關資訊。<br/>                                                 |



 

### <a name="messages"></a>訊息



| 名稱                                                           | 描述                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)                    | 在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中，抓取所選取檔案的路徑和檔案名。 您必須使用 OFN EXPLORER 旗標建立對話方塊 \_ ; 否則，訊息會失敗。<br/>                                                  |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md)            | 抓取對應于目前開啟之 [Explorer 樣式 **開啟** ] 或 [ **另存** 新檔] 對話方塊之資料夾的專案識別碼清單位址。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/> |
| [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md)                | 抓取 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中目前開啟之資料夾或目錄的路徑。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/>                                      |
| [**CDM \_ GETSPEC**](cdm-getspec.md)                            | 抓取檔案名 (不包含在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中目前選取之檔案的路徑) 。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/>                    |
| [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md)                    | 在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中隱藏指定的控制項。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/>                                                                        |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)              | 在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中，設定指定之控制項的文字。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/>                                                            |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)                        | 設定 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的預設副檔名。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。<br/>                                                              |
| [**SETRGBSTRING**](setrgbstring.md)                           | [ **色彩** ] 對話方塊（ [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)）的 [攔截程式] 可以將已註冊的 [**SETRGBSTRING**](setrgbstring.md) 訊息傳送至對話方塊，以設定目前的色彩選取範圍。 <br/>                                                        |
| [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) | 應用程式會將 [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) 訊息傳送至 [ **字型** ] 對話方塊，以取得使用者目前字型選取專案的相關資訊。 <br/>                                                                      |
| [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)     | 應用程式會將 [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) 訊息傳送至 [ **字型** ] 對話方塊，以設定對話方塊的顯示選項。<br/>                                                                                              |
| [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md) | 應用程式會將 [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md) 訊息傳送至 [ **字型** ] 對話方塊，以設定目前的邏輯字型資訊。 <br/>                                                                                           |



 

### <a name="notifications"></a>通知



| 名稱                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDN \_ FILEOK**](cdn-fileok.md)                        | 當使用者指定檔案名，並按一下 [**確定**] 按鈕時，由 Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送。 <br/>                                                                                                                                                                                                                                                                                   |
| [**CDN \_ FOLDERCHANGE**](cdn-folderchange.md)            | 開啟新資料夾時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。 <br/>                                                                                                                                                                                                                                                                                                                        |
| [**CDN \_ 說明**](cdn-help.md)                            | 當使用者按一下 [說明 **] 按鈕時，由** Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送。 <br/>                                                                                                                                                                                                                                                                                                           |
| [**CDN \_ INCLUDEITEM**](cdn-includeitem.md)              | 由 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送，以判斷對話方塊是否應在 shell 資料夾的專案清單中顯示專案。 當使用者開啟資料夾時，對話方塊會為資料夾中的每個專案傳送 [**CDN \_ INCLUDEITEM**](cdn-includeitem.md) 通知。 只有在建立對話方塊時設定了 **OFN \_ ENABLEINCLUDENOTIFY** 旗標，對話方塊才會傳送此通知。 <br/> |
| [**CDN \_ INITDONE**](cdn-initdone.md)                    | 當系統完成對話方塊中的控制項排列時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。 系統會移動標準控制項，以騰出空間給子對話方塊的控制項。 <br/>                                                                                                                                                                                |
| [**CDN \_ SELCHANGE**](cdn-selchange.md)                  | 當清單方塊中顯示目前開啟的資料夾或目錄的內容時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊所傳送。 <br/>                                                                                                                                                                                                                                  |
| [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)        | 當使用者按一下 [**確定]** 按鈕時，由 Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送，表示選取的檔案發生網路共用違規。 <br/>                                                                                                                                                                                                                                                |
| [**CDN \_ TYPECHANGE**](cdn-typechange.md)                | 當使用者從 [檔案類型] 下拉式方塊中選取新的檔案類型時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。 <br/>                                                                                                                                                                                                                                                                                |
| [**COLOROKSTRING**](colorokstring.md)                   | 當使用者選取色彩，然後按一下 [**確定]** 按鈕時，[**色彩**] 對話方塊會將已註冊的 [**COLOROKSTRING**](colorokstring.md)訊息傳送至您的掛勾程式 [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)。 攔截程式可以接受色彩，並允許對話方塊關閉或拒絕色彩，然後強制對話方塊保持開啟狀態。 <br/>                                                           |
| [**FILEOKSTRING**](fileokstring.md)                     | 當使用者指定檔案名，然後按一下 [**確定]** 按鈕時，[**開啟**] 或 [**另存** 新檔] 對話方塊會將已註冊的 [**FILEOKSTRING**](fileokstring.md)訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)。 攔截程式可以接受檔案名，並允許對話方塊關閉或拒絕檔案名，並強制對話方塊維持開啟狀態。 <br/>                              |
| [**FINDMSGSTRING**](findmsgstring.md)                   | 當使用者按一下 [**尋找下一個**]、[**取代**] 或 [**全部取代**] 按鈕，或關閉對話方塊時，[**尋找** 或 **取代**] 對話方塊會將 [**FINDMSGSTRING**](findmsgstring.md)註冊的訊息傳送至其擁有者視窗的視窗程式。 <br/>                                                                                                                                                   |
| [**HELPMSGSTRING**](helpmsgstring.md)                   | 當使用者按一下 [說明 **] 按鈕時**，通用的對話方塊會將已註冊的 [**HELPMSGSTRING**](helpmsgstring.md)訊息傳送至其擁有者視窗的視窗程式。<br/>                                                                                                                                                                                                                                     |
| [**LBSELCHSTRING**](lbselchstring.md)                   | [ **開啟** ] 或 [ **另存** 新檔] 對話方塊會在對話方塊的任何清單方塊或下拉式方塊中選取的專案變更時，將已註冊的 [**LBSELCHSTRING**](lbselchstring.md) 訊息傳送至您的勾點程式。<br/>                                                                                                                                                                                            |
| [**SHAREVISTRING**](sharevistring.md)                   | [ **開啟** ] 或 [ **另存** 新檔] 對話方塊會將已註冊的 [**SHAREVISTRING**](sharevistring.md) 訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)，如果當使用者按一下 [ **確定]** 按鈕時，所選取的檔案發生共用違規。<br/>                                                                                                                                                   |
| [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)     | 通知 [版面設定] 對話方塊 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)的攔截 **程式**，對話方塊即將繪製範例頁面的信封戳記矩形。 <br/>                                                                                                                                                                                                                          |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | 在 [版面設定] 對話方塊中，通知範例頁面矩形座標的 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點 **程式** 。 當此對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。<br/>                                                                                                                                                                      |
| [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)   | 通知 **頁面設定** 對話方塊 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)的攔截程式，對話方塊即將在範例頁面的邊界矩形內繪製希臘文文字。 <br/>                                                                                                                                                                                                                |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | 通知 **頁面設定** 對話方塊（ [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)）的攔截程式，對話方塊即將繪製範例頁面的邊界矩形。 <br/>                                                                                                                                                                                                                                  |
| [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)   | 通知範例頁面中邊界矩形座標的 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點程式。 當 [版面 **設定** ] 對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。<br/>                                                                                                                                                                            |
| [**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)     | 通知 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點程式，[版面 **設定** ] 對話方塊即將繪製範例頁面的內容。 攔截程式可以使用此訊息來執行與繪製範例頁面內容相關的初始化工作。<br/>                                                                                                                                 |
| [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md) | 通知 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)**頁面設定** 對話方塊的攔截程式，此對話方塊即將繪製信封範例頁面的傳回位址部分。 <br/>                                                                                                                                                                                                                    |



 

### <a name="structures"></a>結構



| 名稱                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)            | 包含 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 函數用來初始化 [ **色彩** ] 對話方塊的資訊。 使用者關閉對話方塊之後，系統會傳回使用者在此結構中選取專案的相關資訊。 <br/>                                                                                                                                                                                                                  |
| [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)              | 包含 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函數用來初始化 **字型** 對話方塊的資訊。 使用者關閉對話方塊之後，系統會傳回使用者在此結構中選取專案的相關資訊。 <br/>                                                                                                                                                                                                                |
| [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)                  | 包含可識別印表機之驅動程式、裝置和輸出埠名稱的字串。 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))和 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))函數會使用這些字串來初始化系統定義的 [[列印屬性工作表](print-property-sheet.md)] 或 [[列印] 對話方塊](print-dialog-box.md)。 當使用者關閉屬性工作表或對話方塊時，就會在此結構中傳回所選印表機的相關資訊。 <br/> |
| [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)            | 包含 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 和 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函數用來初始化 [ **尋找** 和 **取代** ] 對話方塊的資訊。 [**FINDMSGSTRING**](findmsgstring.md)註冊的訊息會使用此結構，將使用者的搜尋或取代輸入傳遞至 [**尋找** 或 **取代**] 對話方塊的 [主控視窗] 視窗。<br/>                                                                                 |
| [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)                  | 針對 [**開啟**] 或 [**另存** 新檔] 對話方塊，包含傳送至 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)攔截程式之 [**WM \_ 通知**](../controls/wm-notify.md)訊息的相關資訊。 **WM \_ 通知** 訊息的 *LParam* 參數是指向 [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。 <br/>                                                                                                                                                    |
| [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)              | 包含 [**CDN \_ INCLUDEITEM**](cdn-includeitem.md) 通知訊息的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)          | 包含 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 和 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) 函數用來初始化 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的資訊。 使用者關閉對話方塊之後，系統會傳回使用者在此結構中選取專案的相關資訊。<br/>                                                                                                                                          |
| [**OPENFILENAME \_ NT4**](/windows/win32/api/commdlg/ns-commdlg-openfilename_nt4a) | 和[](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) \_ WIN32 \_ WINNT 設定為0x0400 的 OPENFILENAME 相同。 <br/>                                                                                                                                                                                                                                                                                                                                                              |
| [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)          | 包含 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函數用來初始化 [版面 **設定** ] 對話方塊的資訊。 使用者關閉對話方塊之後，系統會傳回這個結構中使用者定義頁面參數的相關資訊。 <br/>                                                                                                                                                                                               |
| [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)                  | 包含 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數用來初始化 [ [列印] 對話方塊](print-dialog-box.md)的資訊。 在使用者關閉對話方塊之後，系統會使用此結構來傳回使用者選取專案的相關資訊。<br/>                                                                                                                                                                                           |
| [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)              | 包含 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數用來初始化 [列印屬性工作表](print-property-sheet.md)的資訊。 在使用者關閉屬性工作表之後，系統會使用此結構來傳回使用者選取專案的相關資訊。<br/>                                                                                                                                                                           |
| [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange)      | 指定列印工作中的頁面範圍。 列印工作可以有一個以上的頁面範圍。 呼叫 [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式時，會在 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構中提供這項資訊。<br/>                                                                                                                                                                                                               |



 

