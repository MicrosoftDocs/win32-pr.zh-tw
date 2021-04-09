---
title: Rich Edit
description: 本章節包含與 rich edit 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\richedit\richeditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fc87b75bcfad16770603150667b77605ee2c4b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933646"
---
# <a name="rich-edit"></a>Rich Edit

本章節包含與 rich edit 控制項搭配使用之程式設計項目的相關資訊。 Rich edit 控制項可讓使用者輸入、編輯、列印和儲存文字。 您可以將文字指派為字元和段落格式，也可以包含內嵌元件物件模型 (COM) 物件。

由於 rich edit 控制項支援幾乎所有與多行 [編輯控制項](edit-controls.md)搭配使用的訊息和通知程式碼，因此您可以輕鬆地變更已使用編輯控制項的應用程式，以使用 rich edit 控制項。

### <a name="overviews"></a>概觀



| 主題                                                    | 目錄                                                                                            |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [關於 Rich Edit 控制項](about-rich-edit-controls.md) | 本節介紹 rich edit 控制項。<br/>                                              |
| [使用 Rich Edit 控制項](using-rich-edit-controls.md) | 本章節包含的主題會示範如何建立和使用 rich edit 控制項。 <br/> |



 

### <a name="functions"></a>函式



| 主題                                            | 目錄                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)         | [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)函式是搭配 [**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)訊息使用的應用程式定義回呼函數。<br/>                                                                                                                                                   |
| [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)   | [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)函式是一種應用程式定義的回呼函式，搭配 [**Em \_ STREAMIN**](em-streamin.md)和 [**em \_ STREAMOUT**](em-streamout.md)訊息使用。 它是用來將資料流程傳入或流出 rich edit 控制項。 <br/>                                         |
| [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) | [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)函式是搭配 [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md)訊息使用的應用程式定義回呼函數。 它會決定文字分隔的字元索引，或字元類別，以及指定文字中字元的字元類別和文字分隔旗標。 <br/> |
| [*HyphenateProc*](/windows/desktop/api/Richedit/nf-richedit-hyphenateproc)             | [*HyphenateProc*](/windows/desktop/api/Richedit/nf-richedit-hyphenateproc)函式是搭配 [**EM \_ SETHYPHENATEINFO**](em-sethyphenateinfo.md)訊息使用的應用程式定義回呼函數。 它會決定如何在 Microsoft Rich Edit 控制項中完成斷字。<br/>                                                                                   |



 

### <a name="interfaces"></a>介面



| 主題                                                | 目錄                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)                 | [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)介面會公開 rich edit 控制項的 COM 功能。 您可以藉由傳送 [**EM \_ GETOLEINTERFACE**](em-getoleinterface.md) 訊息來取得介面。 <br/>                                                                                                                           |
| [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) | Rich text edit 控制項會使用 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 介面，從其用戶端抓取 OLE 相關的資訊。 Rich edit 控制項用戶端負責執行這個介面，並使用 [**EM \_ SETOLECALLBACK**](em-setolecallback.md) 訊息將它指派給控制項。<br/> |



 

### <a name="messages"></a>訊息



| 主題                                                       | 目錄                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EM \_ AUTOURLDETECT**](em-autourldetect.md)               | 啟用或停用 rich edit 控制項自動偵測 Url。 <br/>                                                                                                                                                                              |
| [**EM \_ CANPASTE**](em-canpaste.md)                         | 判斷 rich edit 控制項是否可以貼上指定的剪貼簿格式。<br/>                                                                                                                                                                        |
| [**EM \_ CANREDO**](em-canredo.md)                           | 判斷控制項重做佇列中是否有任何動作。 <br/>                                                                                                                                                                                  |
| [**EM \_ DISPLAYBAND**](em-displayband.md)                   | 顯示 rich edit 控制項的部分內容，如先前使用 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息針對裝置格式化的部分。<br/>                                                                                          |
| [**EM \_ EXGETSEL**](em-exgetsel.md)                         | 在 rich edit 控制項中，抓取選取範圍的開始和結束字元位置。<br/>                                                                                                                                                        |
| [**EM \_ EXLIMITTEXT**](em-exlimittext.md)                   | 將使用者可以輸入或貼上的文字數量上限設定為 rich edit 控制項。<br/>                                                                                                                                                        |
| [**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md)             | 判斷哪一行在 rich edit 控制項中包含指定的字元。<br/>                                                                                                                                                                        |
| [**EM \_ EXSETSEL**](em-exsetsel.md)                         | 在 Rich Edit 控制項中選取某個範圍的字元或 COM 物件。<br/>                                                                                                                                                                                  |
| [**EM \_ FINDTEXT**](em-findtext.md)                         | 在 rich edit 控制項中尋找文字。<br/>                                                                                                                                                                                                                |
| [**EM \_ FINDTEXTEX**](em-findtextex.md)                     | 在 rich edit 控制項中尋找文字。<br/>                                                                                                                                                                                                                |
| [**EM \_ FINDTEXTEXW**](em-findtextexw.md)                   | 在 rich edit 控制項中尋找 Unicode 文字。<br/>                                                                                                                                                                                                        |
| [**EM \_ FINDTEXTW**](em-findtextw.md)                       | 在 rich edit 控制項中尋找 Unicode 文字。<br/>                                                                                                                                                                                                        |
| [**EM \_ FINDWORDBREAK**](em-findwordbreak.md)               | 尋找指定字元位置之前或之後的下一個字組，或抓取位於該位置之字元的相關資訊。<br/>                                                                                                             |
| [**EM \_ FORMATRANGE**](em-formatrange.md)                   | 針對特定裝置格式化 rich edit 控制項中的文字範圍。<br/>                                                                                                                                                                                 |
| [**EM \_ GETAUTOURLDETECT**](em-getautourldetect.md)         | 指出是否已在 rich edit 控制項中開啟自動 URL 偵測。 <br/>                                                                                                                                                                      |
| [**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)             | 指出 rich edit 控制項中雙向選項的目前狀態。 <br/>                                                                                                                                                                   |
| [**EM \_ GETCHARFORMAT**](em-getcharformat.md)               | 判斷 rich edit 控制項中的字元格式。<br/>                                                                                                                                                                                           |
| [**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)             | 取得 Rich Edit 控制項的文字服務架構 (TSF) 模式偏差值。 <br/>                                                                                                                                                                     |
| [**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)         | 判斷 TSF 鍵盤為開啟或關閉。 <br/>                                                                                                                                                                                                    |
| [**EM \_ GETEDITSTYLE**](em-geteditstyle.md)                 | 抓取目前的編輯樣式旗標。<br/>                                                                                                                                                                                                               |
| [**EM \_ GETEVENTMASK**](em-geteventmask.md)                 | 抓取 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。<br/>                                                                                                           |
| [**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)         | 取得 Rich Edit 控制項的斷字資訊。 <br/>                                                                                                                                                                                          |
| [**EM \_ GETIMECOLOR**](em-getimecolor.md)                   | 抓取輸入方法編輯器 (IME) 組合色彩。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                         |
| [**EM \_ GETIMECOMPMODE**](em-getimecompmode.md)             | 取得 rich edit 控制項目前的 IME 模式。<br/>                                                                                                                                                                                                    |
| [**EM \_ GETIMECOMPTEXT**](em-getimecomptext.md)             | 取得 IME 組合文字。 <br/>                                                                                                                                                                                                                       |
| [**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)             | 取得 Rich Edit 控制項的 IME 模式偏差。 <br/>                                                                                                                                                                                                      |
| [**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)               | 抓取目前的 IME 選項。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                                                 |
| [**EM \_ GETIMEPROPERTY**](em-getimeproperty.md)             | 取得與目前輸入地區設定關聯之 IME 的屬性和功能。 <br/>                                                                                                                                                              |
| [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)             | 取得 rich edit 控制項的選項設定，用於輸入法和亞洲語言支援。 <br/>                                                                                                                                                                       |
| [**EM \_ GETOLEINTERFACE**](em-getoleinterface.md)           | 抓取 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 物件，用戶端可以使用此物件來存取 rich edit 控制項的 COM 功能。<br/>                                                                                                                     |
| [**EM \_ GETOPTIONS**](em-getoptions.md)                     | 抓取 rich edit 控制項選項。<br/>                                                                                                                                                                                                                  |
| [**EM \_ GETPAGEROTATE**](em-getpagerotate.md)               | 已取代。 取得 Rich Edit 控制項的文字版面配置。 <br/>                                                                                                                                                                                            |
| [**EM \_ GETPARAFORMAT**](em-getparaformat.md)               | 抓取 rich edit 控制項中目前選取範圍的段落格式。<br/>                                                                                                                                                                   |
| [**EM \_ GETPUNCTUATION**](em-getpunctuation.md)             | 取得 rich edit 控制項的目前標點符號字元。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                 |
| [**EM \_ GETREDONAME**](em-getredoname.md)                   | 在 rich edit 控制項的重做佇列中，抓取下一個動作的型別（如果有的話）。 <br/>                                                                                                                                                                |
| [**EM \_ GETSCROLLPOS**](em-getscrollpos.md)                 | 取得編輯控制項的目前滾動位置。 <br/>                                                                                                                                                                                             |
| [**EM \_ GETSELTEXT**](em-getseltext.md)                     | 抓取 rich edit 控制項中目前選取的文字。<br/>                                                                                                                                                                                         |
| [**EM \_ GETTEXTEX**](em-gettextex.md)                       | 取得任何您想要的特定程式碼基底中，來自 rich edit 控制項的所有文字。 <br/>                                                                                                                                                                |
| [**EM \_ GETTEXTLENGTHEX**](em-gettextlengthex.md)           | 以各種方式計算文字長度。 通常會在建立緩衝區之前呼叫，以接收控制項的文字。 <br/>                                                                                                                          |
| [**EM \_ GETTEXTMODE**](em-gettextmode.md)                   | 取得 rich edit 控制項的目前文字模式和復原層級。 <br/>                                                                                                                                                                                    |
| [**EM \_ GETTEXTRANGE**](em-gettextrange.md)                 | 從 rich edit 控制項抓取指定的字元範圍。<br/>                                                                                                                                                                                   |
| [**EM \_ GETTYPOGRAPHYOPTIONS**](em-gettypographyoptions.md) | 抓取 rich edit 控制項之印刷樣式選項的目前狀態。<br/>                                                                                                                                                                         |
| [**EM \_ GETUNDONAME**](em-getundoname.md)                   | Microsoft Rich Edit 2.0 和更新版本：抓取下一個復原動作的型別（如果有的話）。<br/> Microsoft Rich Edit 1.0：不支援此訊息。<br/>                                                                                             |
| [**EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md)     | 抓取目前註冊的延伸斷詞程式的位址。<br/>                                                                                                                                                                      |
| [**EM \_ GETWORDWRAPMODE**](em-getwordwrapmode.md)           | 取得 rich edit 控制項的目前文字換行和斷詞選項。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                       |
| [**EM \_ GETZOOM**](em-getzoom.md)                           | 取得目前的縮放比例，其一律介於1/64 到64之間。 <br/>                                                                                                                                                                                    |
| [**EM \_ HIDESELECTION**](em-hideselection.md)               | 隱藏或顯示在 rich edit 控制項中的選取專案。<br/>                                                                                                                                                                                                  |
| [**EM \_ ISIME**](em-isime.md)                               | 判斷目前的輸入地區設定是否為東亞地區設定。 <br/>                                                                                                                                                                                 |
| [**EM \_ PASTESPECIAL**](em-pastespecial.md)                 | 在 rich edit 控制項中貼上特定的剪貼簿格式。<br/>                                                                                                                                                                                            |
| [**EM \_ 漢字重帶**](em-reconversion.md)                 | 叫用輸入法的 [重組] 對話方塊。 <br/>                                                                                                                                                                                                             |
| [**EM \_ 重做**](em-redo.md)                                 | 重新執行控制項的重做佇列中的下一個動作。<br/>                                                                                                                                                                                                   |
| [**EM \_ REQUESTRESIZE**](em-requestresize.md)               | 強制 rich edit 控制項將 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知程式碼傳送至其父視窗。<br/>                                                                                                                               |
| [**EM \_ SELECTIONTYPE**](em-selectiontype.md)               | 判斷 rich edit 控制項的選取專案類型。<br/>                                                                                                                                                                                                |
| [**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)             | 在 rich edit 控制項中設定雙向選項的目前狀態。 <br/>                                                                                                                                                                        |
| [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md)               | 設定 rich edit 控制項的背景色彩。<br/>                                                                                                                                                                                                    |
| [**EM \_ SETCHARFORMAT**](em-setcharformat.md)               | 設定 rich edit 控制項中的字元格式。<br/>                                                                                                                                                                                                     |
| [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)             | 設定 Rich Edit 控制項的 TSF 模式偏差。 <br/>                                                                                                                                                                                                       |
| [**EM \_ SETCTFOPENSTATUS**](em-setctfopenstatus.md)         | 開啟或關閉 TSF 鍵盤。 <br/>                                                                                                                                                                                                                    |
| [**EM \_ SETEDITSTYLE**](em-seteditstyle.md)                 | 設定目前的編輯樣式旗標。 <br/>                                                                                                                                                                                                                   |
| [**EM \_ SETEVENTMASK**](em-seteventmask.md)                 | 設定 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。<br/>                                                                                                                |
| [**EM \_ SETFONTSIZE**](em-setfontsize.md)                   | 設定所選取文字的字型大小。 <br/>                                                                                                                                                                                                            |
| [**EM \_ SETHYPHENATEINFO**](em-sethyphenateinfo.md)         | 設定 Rich Edit 控制項進行斷字的方式。 <br/>                                                                                                                                                                                                   |
| [**EM \_ SETIMECOLOR**](em-setimecolor.md)                   | 設定 IME 組合色彩。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                                                    |
| [**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)             | 設定 Rich Edit 控制項的 IME 模式偏差。 <br/>                                                                                                                                                                                                      |
| [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)               | 設定 IME 選項。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                                                              |
| [**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)             | 在 rich edit 控制項中設定 IME 和亞洲語言支援的選項。 <br/>                                                                                                                                                                              |
| [**EM \_ SETOLECALLBACK**](em-setolecallback.md)             | 提供 rich edit 控制項的 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 物件，讓控制項用來從用戶端取得 OLE 相關的資源和資訊。<br/>                                                                          |
| [**EM \_ >SETOPTIONS**](em-setoptions.md)                     | 設定 rich edit 控制項的選項。<br/>                                                                                                                                                                                                             |
| [**EM \_ SETPAGEROTATE**](em-setpagerotate.md)               | 已取代。 設定 Rich Edit 控制項的文字版面配置。 <br/>                                                                                                                                                                                            |
| [**EM \_ SETPALETTE**](em-setpalette.md)                     | 變更 rich edit 用於其顯示視窗的調色板。 <br/>                                                                                                                                                                                      |
| [**EM \_ SETPARAFORMAT**](em-setparaformat.md)               | 設定 rich edit 控制項中目前選取範圍的段落格式。<br/>                                                                                                                                                                       |
| [**EM \_ SETPUNCTUATION**](em-setpunctuation.md)             | 設定 rich edit 控制項的標點符號字元。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                                           |
| [**EM \_ SETSCROLLPOS**](em-setscrollpos.md)                 | 告訴 rich edit 控制項滾動至特定點。<br/>                                                                                                                                                                                          |
| [**EM \_ SETTARGETDEVICE**](em-settargetdevice.md)           | 設定在 rich edit 控制項中，用於「您看到的內容」 (WYSIWYG) 格式的目標裝置和線條寬度。<br/>                                                                                                                            |
| [**EM \_ SETTEXTEX**](em-settextex.md)                       | 結合了 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 和 [**EM \_ REPLACESEL**](em-replacesel.md)的功能，並新增使用字碼頁設定文字的功能，以及使用 rtf 或純文字。<br/>                                         |
| [**EM \_ SETTEXTMODE**](em-settextmode.md)                   | 設定 rich edit 控制項的文字模式或復原層級。 如果控制項包含任何文字，則訊息會失敗。 <br/>                                                                                                                                         |
| [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) | 設定 rich edit 控制項之印刷樣式選項的目前狀態。 <br/>                                                                                                                                                                             |
| [**EM \_ SETUNDOLIMIT**](em-setundolimit.md)                 | 設定可儲存在復原佇列中的動作數目上限。 <br/>                                                                                                                                                                                |
| [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md)     | 設定延伸的斷詞程式。<br/>                                                                                                                                                                                                               |
| [**EM \_ SETWORDWRAPMODE**](em-setwordwrapmode.md)           | 設定 rich edit 控制項的自動換行和斷字選項。 此訊息僅適用于亞洲語言版本的作業系統。<br/>                                                                                        |
| [**EM \_ SETZOOM**](em-setzoom.md)                           | 在1/64 和64之間的任何位置設定縮放比例。 <br/>                                                                                                                                                                                                    |
| [**EM \_ SHOWSCROLLBAR**](em-showscrollbar.md)               | 顯示或隱藏文字主視窗中的其中一個捲軸。 <br/>                                                                                                                                                                                       |
| [**EM \_ STOPGROUPTYPING**](em-stopgrouptyping.md)           | 停止控制項，使其無法將其他輸入動作收集到目前的復原動作。 控制項會將下一個輸入動作（如果有的話）儲存至復原佇列中的新動作。 <br/>                                                                    |
| [**EM \_ STREAMIN**](em-streamin.md)                         | 以應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函式所提供的資料流程，取代 rich edit 控制項的內容。<br/>                                                                               |
| [**EM \_ STREAMOUT**](em-streamout.md)                       | 讓 rich edit 控制項將其內容傳遞至應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函數。 回呼函數接著可以將資料串流寫入檔案或它所選擇的任何其他位置。 <br/> |



 

### <a name="notifications"></a>通知



| 主題                                         | 目錄                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EN \_ ALIGNLTR](en-alignltr.md)               | 通知 rich edit 控制項的父視窗，段落方向已從左至右變更。 Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。<br/>                                                                  |
| [EN \_ ALIGNRTL](en-alignrtl.md)               | 通知 rich edit 控制項的父視窗，段落方向已從右至左變更。 Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。<br/>                                                                      |
| [EN \_ CORRECTTEXT](en-correcttext.md)         | 通知 rich edit 控制項的父視窗 SYV \_ 正確的手勢發生，讓父視窗有機會取消更正文字。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。 <br/>                          |
| [EN \_ DRAGDROPDONE](en-dragdropdone.md)       | 通知 rich edit 控制項的父視窗，拖放作業已完成。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                                                  |
| [EN \_ DROPFILES](en-dropfiles.md)             | 通知 rich edit 控制項的父視窗，使用者嘗試將檔案放入控制項。 Rich edit 控制項會在收到 [**wm \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles)訊息時，以 [**WM \_ 通知**](wm-notify.md)訊息的形式傳送此通知碼。<br/> |
| [EN \_ IMECHANGE](en-imechange.md)             | 通知 rich edit 控制項的父系，IME 轉換狀態已變更。 此訊息 *僅* 適用于亞洲語言版本的作業系統。 Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。<br/>  |
| [EN \_ 連結](en-link.md)                       | 當使用者按一下滑鼠或當滑鼠指標停留在具有 CFE 連結效果的文字上方時，通知 rich edit 控制項的父視窗 \_ 。 控制項的父視窗會透過 [**WM \_ 通知**](wm-notify.md) 訊息接收此通知碼。<br/>                    |
| [EN \_ LOWFIRTF](en-lowfirtf.md)               | 通知 rich edit 控制項的豐富編輯控制項父視窗，指出已收到不支援的 rtf 格式 (RTF) 關鍵字。 Rich Edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                          |
| [EN \_ MSGFILTER](en-msgfilter.md)             | 在控制項中通知 rich edit 控制項的鍵盤或滑鼠事件的父視窗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                                                     |
| [EN \_ OBJECTPOSITIONS](en-objectpositions.md) | 當控制項讀取物件時，通知 rich edit 控制項的父視窗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                                                               |
| [EN \_ OLEOPFAILED](en-oleopfailed.md)         | 通知 rich edit 控制項的父視窗，表示 COM 物件上的使用者動作失敗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                                                   |
| [\_受保護](en-protected.md)             | 通知 rich edit 控制項的父視窗，讓使用者採取動作來變更受保護的文字範圍。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                   |
| [EN \_ REQUESTRESIZE](en-requestresize.md)     | 通知 rich edit 控制項的父視窗，控制項的內容小於控制項的視窗大小。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                         |
| [EN \_ SAVECLIPBOARD](en-saveclipboard.md)     | 通知 rich edit 控制項的父視窗，指出控制項正在關閉，且剪貼簿包含資訊。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                            |
| [EN \_ SELCHANGE](en-selchange.md)             | 通知 rich edit 控制項的父視窗，指出目前的選取範圍已變更。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                                                                                          |
| [EN \_ STOPNOUNDO](en-stopnoundo.md)           | 通知 rich edit 控制項的父視窗，表示控制項無法配置足夠的記憶體來維持復原狀態。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。<br/>                          |



 

### <a name="structures"></a>結構



| 主題                                      | 目錄                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)         | 包含 rich edit 控制項的雙向資訊。 [**Em \_ GETBIDIOPTIONS**](em-getbidioptions.md)和 [**em \_ SETBIDIOPTIONS**](em-setbidioptions.md)訊息會使用此結構來取得和設定控制項的雙向資訊。<br/>                                                                                                                |
| [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)           | 包含 rich edit 控制項中的字元格式相關資訊。 <br/>                                                                                                                                                                                                                                                                                                            |
| [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)         | 包含 rich edit 控制項中的字元格式相關資訊。 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) 是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構的 Microsoft Rich Edit 2.0 延伸模組。 Microsoft Rich Edit 2.0 可讓您使用任一個結構搭配 [**em \_ GETCHARFORMAT**](em-getcharformat.md) 和 [**em \_ SETCHARFORMAT**](em-setcharformat.md) 訊息。 <br/> |
| [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)             | 指定 rich edit 控制項中的字元範圍。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)             | 包含組合字元串的色彩設定。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)           | 包含應用程式以 [**em \_ STREAMIN**](em-streamin.md) 或 [**em \_ STREAMOUT**](em-streamout.md) 訊息傳遞至 rich edit 控制項的資訊。 Rich edit 控制項會使用資訊將資料流程傳入或移出控制項。 <br/>                                                                                                              |
| [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)     | 包含要更正之所選取文字的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                                      |
| [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)         | 包含與 [En-us \_ DROPFILES](en-dropfiles.md) 通知碼相關聯的資訊。 Rich edit 控制項會在收到 [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) 訊息時傳送此通知碼。<br/>                                                                                                                                                                   |
| [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)                   | 包含來自 rich edit 控制項之 [En-us \_ 連結](en-link.md) 通知程式碼的相關資訊。 <br/>                                                                                                                                                                                                                                                                                  |
| [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)           | 在 Rich Edit 控制項中包含不支援的 RTF 關鍵字的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)     | 包含失敗作業的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)         | 包含與 [En-us \_ 受保護](en-protected.md) 的通知碼相關聯的資訊。 當使用者嘗試編輯受保護的文字時，rich edit 控制項會傳送這則通知。<br/>                                                                                                                                                                                             |
| [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) | 包含剪貼簿上物件和文字的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                       |
| [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)               | 包含 rich edit 控制項中搜尋作業的相關資訊。 此結構會搭配 [**EM \_ FINDTEXT**](em-findtext.md) 訊息使用。<br/>                                                                                                                                                                                                                                  |
| [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)           | 包含在 rich edit 控制項中要搜尋之文字的相關資訊。 此結構會搭配 [**EM \_ FINDTEXTEX**](em-findtextex.md) 訊息使用。<br/>                                                                                                                                                                                                                              |
| [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange)         | 包含 rich edit 控制項用來為特定裝置格式化輸出的資訊。 此結構會搭配 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息使用。<br/>                                                                                                                                                                                                 |
| [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)             | 包含從 rich edit 控制項取得文字之作業的相關資訊。 此結構會在 [**EM \_ GETTEXTEX**](em-gettextex.md)訊息的 **wParam** 中傳遞。<br/>                                                                                                                                                                                                      |
| [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) | 包含有關如何計算 rich edit 控制項文字長度的資訊。 此結構會在 [**EM \_ GETTEXTLENGTHEX**](em-gettextlengthex.md)訊息的 **wParam** 中傳遞。<br/>                                                                                                                                                                            |
| [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)     | 包含在 Rich Edit 控制項中斷字的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                                     |
| [**HYPHRESULT**](/windows/desktop/api/Richedit/ns-richedit-hyphresult)           | 包含 Rich Edit 控制項中斷字結果的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                       |
| [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)         | 包含 Rich Edit 控制項中組合文字的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                            |
| [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)             | 包含鍵盤或滑鼠事件的相關資訊。 Rich edit 控制項會將此結構傳送至其父視窗，做為 [EN \_ MSGFILTER](en-msgfilter.md) 通知程式碼的一部分，讓父系變更訊息或防止處理訊息。<br/>                                                                                                                |
| [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) | 包含物件位置資訊。 <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)           | 包含 rich edit 控制項中段落格式化屬性的相關資訊。 此結構會搭配 [**em \_ GETPARAFORMAT**](em-getparaformat.md) 和 [**em \_ SETPARAFORMAT**](em-setparaformat.md) 訊息使用。 <br/>                                                                                                                                                       |
| [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)         | 包含 rich edit 控制項中段落格式化屬性的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                 |
| [**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation)         | 包含 rich edit 控制項中所使用之標點符號的相關資訊。<br/>                                                                                                                                                                                                                                                                                                             |
| [**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)               | 包含物件的相關資訊。 <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)   | 包含識別貼上物件的顯示部分是否應以物件內容或代表物件的圖示為基礎的資訊。<br/>                                                                                                                                                                                                                  |
| [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)             | 包含 rich edit 控制項的要求大小。 Rich edit 控制項會將此結構傳送至其父視窗，作為 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知程式碼的一部分。<br/>                                                                                                                                                                                        |
| [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)             | 包含與 [En-us \_ SELCHANGE](en-selchange.md) 通知碼相關聯的資訊。 當目前的選取專案變更時，rich edit 控制項會將此通知傳送至其父視窗。<br/>                                                                                                                                                                                   |
| [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)             | 指定在設定文字) 時要使用的字碼頁 (、文字是否取代控制項中的所有文字，以及是否要保留復原狀態。<br/>                                                                                                                                                                                              |
| [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)             | 從 rich edit 控制項接收某範圍的文字。 此結構是由 [**EM \_ GETTEXTRANGE**](em-gettextrange.md) 訊息填入。 **LpstrText** 成員所指向的緩衝區必須夠大，才能接收所有字元和終止的 null 字元。<br/>                                                                                                     |



 

### <a name="constants"></a>常數



| 主題                                                                        | 目錄                                                                                                      |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Rich Edit 控制項事件遮罩旗標](rich-edit-control-event-mask-flags.md) | 事件遮罩會指定 rich edit 控制項傳送至其父視窗的通知碼。 <br/> |
| [Rich Edit 控制項樣式](rich-edit-control-styles.md)                     | 描述 rich edit 控制項特有的視窗樣式。 <br/>                                |



 

 

