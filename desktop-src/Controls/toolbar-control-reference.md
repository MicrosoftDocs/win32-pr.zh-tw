---
title: 工具列
description: 本章節包含與工具列控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd70f4e13d569930956a8b84e1010d99c1be434
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480934"
---
# <a name="toolbar"></a>工具列

本章節包含與工具列控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                   | 目錄                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於工具列控制項](toolbar-controls-overview.md) | 工具列是包含一或多個按鈕的控制項。 當使用者按下每個按鈕時，會將命令訊息傳送至父視窗。 通常，工具列中的按鈕對應於應用程式功能表中的項目，為使用者提供其他更直接的方式來存取應用程式的命令。<br/> |
| [使用工具列控制項](using-toolbar-controls.md)    | 本主題包含在應用程式中使用工具列控制項的執行詳細資料與範例程式碼。<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>函式




| 主題 | 目錄 | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>CreateMappedBitmap</strong></a> | 建立要在工具列中使用的點陣圖。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>CreateToolbarEx</strong></a> | 建立工具列視窗，並將指定的按鈕加入至工具列。<blockquote>[!Note]<br />此函式已被取代，因為它不支援工具列的所有功能。 請改用 <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> 。 如需範例，請參閱 <a href="using-toolbar-controls.md">使用工具列控制項</a>。</blockquote><br /><br /> | 




 

### <a name="messages"></a>訊息



| 主題                                                         | 目錄                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TB \_ ADDBITMAP**](tb-addbitmap.md)                         | 將一或多個影像新增至適用于工具列的按鈕影像清單。 <br/>                                                                                                               |
| [**TB \_ ADDBUTTONS**](tb-addbuttons.md)                       | 將一或多個按鈕加入至工具列。<br/>                                                                                                                                                       |
| [**TB \_ ADDSTRING**](tb-addstring.md)                         | 將新字串加入至工具列的字串集區。<br/>                                                                                                                                              |
| [**TB 自動 \_ 調整**](tb-autosize.md)                           | 使工具列調整大小。 <br/>                                                                                                                                                             |
| [**TB \_ BUTTONCOUNT**](tb-buttoncount.md)                     | 抓取工具列中目前的按鈕計數。 <br/>                                                                                                                                  |
| [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md)           | 指定 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的大小。 <br/>                                                                                                                           |
| [**TB \_ CHANGEBITMAP**](tb-changebitmap.md)                   | 變更工具列中按鈕的點陣圖。<br/>                                                                                                                                                |
| [**TB \_ CHECKBUTTON**](tb-checkbutton.md)                     | 檢查或取消核取工具列中的指定按鈕。<br/>                                                                                                                                              |
| [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md)               | 針對與指定的命令識別碼相關聯的按鈕，取得以零為基底的索引。 <br/>                                                                                             |
| [**TB \_ 自訂**](tb-customize.md)                         | 顯示 [ **自訂工具列** ] 對話方塊。<br/>                                                                                                                                               |
| [**TB \_ DELETEBUTTON**](tb-deletebutton.md)                   | 從工具列中刪除按鈕。 <br/>                                                                                                                                                          |
| [**TB \_ ENABLEBUTTON**](tb-enablebutton.md)                   | 在工具列中啟用或停用指定的按鈕。<br/>                                                                                                                                       |
| [**TB \_ GETANCHORHIGHLIGHT**](tb-getanchorhighlight.md)       | 抓取工具列的錨點醒目提示設定。 <br/>                                                                                                                                       |
| [**TB \_ GETBITMAP**](tb-getbitmap.md)                         | 抓取與工具列中的按鈕相關聯的點陣圖索引。 <br/>                                                                                                                    |
| [**TB \_ GETBITMAPFLAGS**](tb-getbitmapflags.md)               | 抓取描述要使用之點陣圖類型的旗標。<br/>                                                                                                                             |
| [**TB \_ GETBUTTON**](tb-getbutton.md)                         | 抓取工具列中指定之按鈕的相關資訊。<br/>                                                                                                                               |
| [**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)                 | 抓取工具列中按鈕的擴充資訊。 <br/>                                                                                                                                   |
| [**TB \_ GETBUTTONSIZE**](tb-getbuttonsize.md)                 | 抓取工具列按鈕目前的寬度和高度（以圖元為單位）。 <br/>                                                                                                                       |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)                 | 抓取工具列上按鈕的顯示文字。<br/>                                                                                                                                         |
| [**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)               | 從工具列控制項抓取色彩配置資訊。 <br/>                                                                                                                            |
| [**TB \_ GETDISABLEDIMAGELIST**](tb-getdisabledimagelist.md)   | 抓取工具列控制項用來顯示非作用中按鈕的影像清單。 <br/>                                                                                                           |
| [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)           | 抓取工具列控制項的延伸樣式。 <br/>                                                                                                                                        |
| [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md)             | 抓取工具列控制項用來顯示熱按鈕的影像清單。<br/>                                                                                                                 |
| [**TB \_ GETHOTITEM**](tb-gethotitem.md)                       | 抓取工具列中熱專案的索引。 <br/>                                                                                                                                           |
| [**TB \_ GETIDEALSIZE**](tb-getidealsize.md)                   | 取得工具列的理想大小。<br/>                                                                                                                                                          |
| [**TB \_ GETIMAGELIST**](tb-getimagelist.md)                   | 抓取工具列控制項用來顯示其預設狀態之按鈕的影像清單。 當按鈕未熱或停用時，工具列控制項會使用此影像清單來顯示按鈕。<br/> |
| [**TB \_ GETIMAGELISTCOUNT**](tb-getimagelistcount.md)         | 取得與工具列相關聯的影像清單數目。<br/>                                                                                                                                  |
| [**TB \_ GETINSERTMARK**](tb-getinsertmark.md)                 | 抓取工具列目前的插入標記。 <br/>                                                                                                                                       |
| [**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)       | 抓取用來繪製工具列之插入標記的色彩。 <br/>                                                                                                                        |
| [**TB \_ GETITEMDROPDOWNRECT**](tb-getitemdropdownrect.md)     | 取得具有樣式 [**BTNS \_ 下拉式清單**](toolbar-control-and-button-styles.md)的工具列專案之下拉式視窗的周框。<br/>                                  |
| [**TB \_ GETITEMRECT**](tb-getitemrect.md)                     | 抓取工具列中按鈕的周框。 <br/>                                                                                                                                  |
| [**TB \_ GETMAXSIZE**](tb-getmaxsize.md)                       | 抓取工具列中所有可見按鈕和分隔符號的總大小。 <br/>                                                                                                       |
| [**TB \_ GETMETRICS**](tb-getmetrics.md)                       | 抓取工具列控制項的度量。<br/>                                                                                                                                                  |
| [**TB \_ GETOBJECT**](tb-getobject.md)                         | 抓取工具列控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 。 <br/>                                                                                                                     |
| [**TB \_ GETPADDING**](tb-getpadding.md)                       | 抓取工具列控制項的邊框距離。 <br/>                                                                                                                                                |
| [**TB \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)     | 取得工具列控制項用來顯示處於已按下狀態之按鈕的影像清單。<br/>                                                                                                       |
| [**TB \_ GETRECT**](tb-getrect.md)                             | 抓取指定之工具列按鈕的周框。 <br/>                                                                                                                            |
| [**TB \_ GETROWS**](tb-getrows.md)                             | 使用 [**TBSTYLE \_ WRAPABLE**](toolbar-control-and-button-styles.md) 樣式來抓取工具列中的按鈕列數。 <br/>                                        |
| [**TB \_ >GETSTATE**](tb-getstate.md)                           | 抓取工具列中指定之按鈕的狀態相關資訊，例如是否已啟用、已按下或已核取。 <br/>                                                             |
| [**TB \_ GETSTRING**](tb-getstring.md)                         | 從工具列的字串集區抓取字串。<br/>                                                                                                                                             |
| [**TB \_ GETSTYLE**](tb-getstyle.md)                           | 抓取工具列控制項目前使用的樣式。 <br/>                                                                                                                                |
| [**TB \_ GETTEXTROWS**](tb-gettextrows.md)                     | 抓取工具列按鈕上可顯示的文字資料列數目上限。 <br/>                                                                                                        |
| [**TB \_ GETTOOLTIPS**](tb-gettooltips.md)                     | 抓取與工具列相關聯之工具提示控制項（如果有的話）的控制碼。 <br/>                                                                                                           |
| [**TB \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)           | 抓取控制項的 Unicode 字元格式旗標。 <br/>                                                                                                                                |
| [**TB \_ HASACCELERATOR**](tb-hasaccelerator.md)               | **適用于內部用途;不建議在應用程式中使用。**<br/> 抓取具有指定快速鍵的工具列按鈕計數。 <br/>                      |
| [**TB \_ HIDEBUTTON**](tb-hidebutton.md)                       | 在工具列中隱藏或顯示指定的按鈕。<br/>                                                                                                                                            |
| [**TB \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](tb-hittest.md)                             | 判中斷點位於工具列控制項中的位置。 <br/>                                                                                                                                         |
| [**TB \_ 不定**](tb-indeterminate.md)                 | 在工具列中設定或清除指定之按鈕的不定狀態。<br/>                                                                                                                 |
| [**TB \_ INSERTBUTTON**](tb-insertbutton.md)                   | 在工具列中插入按鈕。<br/>                                                                                                                                                               |
| [**TB \_ INSERTMARKHITTEST**](tb-insertmarkhittest.md)         | 抓取工具列中某個點的插入標記資訊。 <br/>                                                                                                                          |
| [**TB \_ ISBUTTONCHECKED**](tb-isbuttonchecked.md)             | 決定是否核取工具列中指定的按鈕。 <br/>                                                                                                                            |
| [**TB \_ ISBUTTONENABLED**](tb-isbuttonenabled.md)             | 判斷是否已啟用工具列中指定的按鈕。 <br/>                                                                                                                            |
| [**TB \_ ISBUTTONHIDDEN**](tb-isbuttonhidden.md)               | 決定是否隱藏工具列中指定的按鈕。 <br/>                                                                                                                             |
| [**TB \_ ISBUTTONHIGHLIGHTED**](tb-isbuttonhighlighted.md)     | 檢查工具列按鈕的醒目提示狀態。 <br/>                                                                                                                                             |
| [**TB \_ ISBUTTONINDETERMINATE**](tb-isbuttonindeterminate.md) | 判斷工具列中指定的按鈕是否不定。 <br/>                                                                                                                      |
| [**TB \_ ISBUTTONPRESSED**](tb-isbuttonpressed.md)             | 決定是否按下工具列中指定的按鈕。 <br/>                                                                                                                            |
| [**TB \_ LOADIMAGES**](tb-loadimages.md)                       | 將系統定義的按鈕影像載入工具列控制項的影像清單。<br/>                                                                                                                      |
| [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md)               | 判斷對應至指定快速鍵的按鈕識別碼。<br/>                                                                                                     |
| [**TB \_ MARKBUTTON**](tb-markbutton.md)                       | 在工具列控制項中設定指定按鈕的醒目提示狀態。<br/>                                                                                                                             |
| [**TB \_ MOVEBUTTON**](tb-movebutton.md)                       | 將按鈕從一個索引移至另一個索引。 <br/>                                                                                                                                                   |
| [**TB \_ PRESSBUTTON**](tb-pressbutton.md)                     | 在工具列中按下或放開指定的按鈕。<br/>                                                                                                                                       |
| [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md)                 | 以新的點陣圖取代現有的點陣圖。<br/>                                                                                                                                               |
| [**TB \_ SAVERESTORE**](tb-saverestore.md)                     | 傳送此訊息以起始儲存或還原工具列狀態。<br/>                                                                                                                           |
| [**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)       | 設定工具列的錨點醒目提示設定。 <br/>                                                                                                                                            |
| [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md)                 | 設定要新增至工具列之點陣圖影像的大小。 <br/>                                                                                                                             |
| [**TB \_ SETBOUNDINGSIZE**](tb-setboundingsize.md)             | **適用于內部用途;不建議在應用程式中使用。**<br/> 設定多欄工具列控制項的周框大小。 <br/>                                               |
| [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)                 | 設定工具列中現有按鈕的資訊。<br/>                                                                                                                                    |
| [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md)                 | 設定工具列上的按鈕大小。<br/>                                                                                                                                                       |
| [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md)               | 設定工具列控制項中的最小和最大按鈕寬度。<br/>                                                                                                                           |
| [**TB \_ SETCMDID**](tb-setcmdid.md)                           | 設定工具列按鈕的命令識別碼。 <br/>                                                                                                                                            |
| [**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)               | 設定工具列控制項的色彩配置資訊。 <br/>                                                                                                                                  |
| [**TB \_ SETDISABLEDIMAGELIST**](tb-setdisabledimagelist.md)   | 設定工具列控制項將用來顯示停用按鈕的影像清單。 <br/>                                                                                                          |
| [**TB \_ SETDRAWTEXTFLAGS**](tb-setdrawtextflags.md)           | 設定工具列的文字繪圖旗標。 <br/>                                                                                                                                                |
| [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)           | 設定工具列控制項的延伸樣式。 <br/>                                                                                                                                             |
| [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md)             | 設定工具列控制項將用來顯示熱按鈕的影像清單。<br/>                                                                                                                |
| [**TB \_ SETHOTITEM**](tb-sethotitem.md)                       | 設定工具列中的熱專案。<br/>                                                                                                                                                              |
| [**TB \_ SETHOTITEM2**](tb-sethotitem2.md)                     | 設定工具列中的熱專案。<br/>                                                                                                                                                              |
| [**TB \_ SETIMAGELIST**](tb-setimagelist.md)                   | 設定工具列用來顯示處於預設狀態之按鈕的影像清單。<br/>                                                                                                |
| [**TB \_ SETINDENT**](tb-setindent.md)                         | 設定工具列控制項中第一個按鈕的縮排。 <br/>                                                                                                                             |
| [**TB \_ SETINSERTMARK**](tb-setinsertmark.md)                 | 設定工具列的目前插入標記。 <br/>                                                                                                                                            |
| [**TB \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)       | 設定用來繪製工具列之插入標記的色彩。 <br/>                                                                                                                             |
| [**TB \_ SETLISTGAP**](tb-setlistgap.md)                       | 設定特定工具列上工具列按鈕之間的距離。<br/>                                                                                                                         |
| [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md)               | 設定工具列按鈕上顯示之文字資料列的最大數目。 <br/>                                                                                                                         |
| [**TB \_ SETMETRICS**](tb-setmetrics.md)                       | 設定工具列控制項的度量。<br/>                                                                                                                                                       |
| [**TB \_ SETPADDING**](tb-setpadding.md)                       | 設定工具列控制項的邊框距離。<br/>                                                                                                                                                      |
| [**TB \_ SETPARENT**](tb-setparent.md)                         | 設定工具列控制項傳送通知碼的視窗。 <br/>                                                                                                                      |
| [**TB \_ SETPRESSEDIMAGELIST**](tb-setpressedimagelist.md)     | 設定工具列用來顯示處於已按下狀態之按鈕的影像清單。<br/>                                                                                                    |
| [**TB \_ SETROWS**](tb-setrows.md)                             | 設定工具列中的按鈕列數。<br/>                                                                                                                                             |
| [**TB \_ SETSTATE**](tb-setstate.md)                           | 在工具列中設定指定之按鈕的狀態。<br/>                                                                                                                                        |
| [**TB \_ >SETSTYLE**](tb-setstyle.md)                           | 設定工具列控制項的樣式。 <br/>                                                                                                                                                       |
| [**TB \_ SETTOOLTIPS**](tb-settooltips.md)                     | 將工具提示控制項與工具列產生關聯。 <br/>                                                                                                                                                |
| [**TB \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)           | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/>    |
| [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)               | 設定工具列控制項的視覺化樣式。<br/>                                                                                                                                                  |
| [**TB \_ TRANSLATEACCELERATOR**](tb-translateaccelerator.md)   | 將鍵盤訊息傳遞至工具列。<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>通知



| 主題                                                            | 目錄                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ 字元 (工具列) ](nm-char-toolbar.md)                        | 當工具列收到 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                       |
| [NM \_ 按一下 (工具列) ](nm-click-toolbar.md)                      | 當使用者按一下具有滑鼠左鍵的專案時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                     |
| [NM \_ CUSTOMDRAW (工具列) ](nm-customdraw-toolbar.md)            | 由工具列傳送以通知其父視窗有關繪製作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                              |
| [NM \_ DBLCLK (工具列) ](nm-dblclk-toolbar.md)                    | 通知工具列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                             |
| [NM \_ KEYDOWN (工具列) ](nm-keydown-toolbar.md)                  | 當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                 |
| [NM \_ LDOWN](nm-ldown-toolbar.md)                                | 通知工具列的父視窗已按下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                        |
| [NM \_ RCLICK (工具列) ](nm-rclick-toolbar.md)                    | 當使用者按一下具有滑鼠右鍵的工具列時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                |
| [NM \_ RDBLCLK (工具列) ](nm-rdblclk-toolbar.md)                  | 通知控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                         |
| [NM \_ RELEASEDCAPTURE (工具列) ](nm-releasedcapture-toolbar-.md) | 通知工具列控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                               |
| [NM \_ TOOLTIPSCREATED (工具列) ](nm-tooltipscreated-toolbar-.md) | 通知工具列的父視窗，工具列已建立工具提示控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                    |
| [TBN \_ BEGINADJUST](tbn-beginadjust.md)                          | 通知工具列的父視窗，指出使用者已開始自訂工具列。 此訊息代碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                          |
| [TBN \_ BEGINDRAG](tbn-begindrag.md)                              | 通知工具列的父視窗，指出使用者已開始拖曳工具列中的按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                            |
| [TBN \_ CUSTHELP](tbn-custhelp.md)                                | 通知工具列的父視窗，指出使用者已在 [自訂工具列] 對話方塊中選擇 [說明] 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                       |
| [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md)                    | 工具列控制項在即將刪除按鈕時傳送。 <br/>                                                                                                                                                                                                                                                |
| [TBN \_ DRAGOUT](tbn-dragout.md)                                  | 當使用者按一下按鈕，然後將游標移出按鈕時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                     |
| [TBN \_ SYSTEM.WINDOWS.DRAGDROP.DRAGOVER>](tbn-dragover.md)                                | Ascertains 是否應針對要拖曳的按鈕傳送一則 [**TB \_ MARKBUTTON**](tb-markbutton.md) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                           |
| [TBN \_ 下拉式清單](tbn-dropdown.md)                                | 當使用者按一下下拉式按鈕時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                     |
| [TBN \_ DUPACCELERATOR](tbn-dupaccelerator.md)                    | Ascertains 快速鍵是否可用於兩個或多個作用中的工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                      |
| [TBN \_ ENDADJUST](tbn-endadjust.md)                              | 通知工具列的父視窗，指出使用者已停止自訂工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                   |
| [TBN \_ ENDDRAG](tbn-enddrag.md)                                  | 通知工具列的父視窗，指出使用者已停止拖曳工具列中的按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                        |
| [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)                      | 抓取工具列自訂資訊，並通知工具列的父視窗對工具列進行的任何變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                        |
| [TBN \_ GETDISPINFO](tbn-getdispinfo.md)                          | 抓取工具列專案的顯示資訊。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                                           |
| [TBN \_ GETINFOTIP](tbn-getinfotip.md)                            | 抓取工具列專案的資訊提示資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                                      |
| [TBN \_ GETOBJECT](tbn-getobject.md)                              | 由使用 [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) 樣式的工具列控制項所傳送，以在指標通過其按鈕時，要求放置目標物件。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/> |
| [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)                      | 當熱 (反白顯示) 專案變更時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                    |
| [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md)                      | 通知工具列的父視窗，自訂已開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                       |
| [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md)                    | 要求工具列中對應至指定之快速鍵字元的按鈕索引。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                  |
| [TBN \_ QUERYDELETE](tbn-querydelete.md)                          | 當使用者正在自訂工具列時，通知工具列的父視窗是否可從工具列中刪除按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                        |
| [TBN \_ QUERYINSERT](tbn-queryinsert.md)                          | 當使用者正在自訂工具列時，通知工具列的父視窗是否可將按鈕插入指定按鈕的左邊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                     |
| [TBN \_ 重設](tbn-reset.md)                                      | 通知工具列的父視窗，指出使用者已重設 [自訂工具列] 對話方塊的內容。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                          |
| [TBN \_ 還原](tbn-restore.md)                                  | 通知工具列的父視窗正在還原工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                 |
| [TBN \_ 儲存](tbn-save.md)                                        | 通知工具列的父視窗，工具列正在儲存中。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                    |
| [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md)                      | 通知工具列的父視窗，指出使用者已自訂工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                          |
| [TBN \_ WRAPACCELERATOR](tbn-wrapaccelerator.md)                  | 要求一或多個工具列中，對應至指定之快速鍵的按鈕索引。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                         |
| [TBN \_ WRAPHOTITEM](tbn-wraphotitem.md)                          | 通知應用程式有兩個或多個最忙碌專案即將變更的工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                |



 

### <a name="structures"></a>結構



| 主題                                      | 目錄                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORMAP**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | 包含 [**CreateMappedBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) 函數用來對應點陣圖色彩的資訊。 <br/>                                                                                                                                 |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | 包含工具列控制項所傳送的 [NM \_ CUSTOMDRAW](nm-customdraw-toolbar.md) 通知碼特定資訊。 <br/>                                                                                                                                |
| [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | 包含和接收工具列專案的顯示資訊。 此結構會與 [TBN \_ GETDISPINFO](tbn-getdispinfo.md) 通知程式碼搭配使用。 <br/>                                                                                                    |
| [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | 包含並接收工具列專案的資訊提示資訊。 此結構會與 [TBN \_ GETINFOTIP](tbn-getdispinfo.md) 通知程式碼搭配使用。 <br/>                                                                                                     |
| [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | 包含與 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知程式碼搭配使用的資訊。 <br/>                                                                                                                                                           |
| [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | 允許應用程式在儲存工具列狀態時，解壓縮在 [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) 中所放置的資訊。 當應用程式收到 [TBN \_ 還原](tbn-restore.md) 通知碼時，會將此結構傳遞給應用程式。<br/>             |
| [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | 當應用程式收到 [TBN \_ 儲存](tbn-save.md) 通知碼時，會將此結構傳遞給應用程式。 它包含目前儲存之按鈕的相關資訊。 應用程式可以修改成員的值以儲存其他資訊。 <br/> |
| [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | 包含用來處理工具列通知代碼的資訊。 此結構會取代 **TBNOTIFY** 結構。 <br/>                                                                                                                                      |
| [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | 將包含按鈕影像的點陣圖新增至工具列。<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | 包含工具列中按鈕的相關資訊。<br/>                                                                                                                                                                                                            |
| [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | 包含或接收工具列中特定按鈕的資訊。<br/>                                                                                                                                                                                         |
| [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | 包含工具列控制項中插入標記的資訊。 <br/>                                                                                                                                                                                            |
| [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | 定義用來壓縮或展開工具列專案之工具列的度量。<br/>                                                                                                                                                                            |
| [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | 搭配使用 [**TB 的 \_ REPLACEBITMAP**](tb-replacebitmap.md) 訊息，以將工具列點陣圖取代為另一個。<br/>                                                                                                                                              |
| [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | 指定登錄中 [**TB \_ SAVERESTORE**](tb-saverestore.md) 訊息儲存和抓取工具列狀態相關資訊的位置。 <br/>                                                                                           |



 

### <a name="constants"></a>常數




| 主題 | 目錄 | 
|-------|----------|
| <a href="toolbar-button-states.md">工具列按鈕狀態</a> | 此區段會列出工具列按鈕可以有的狀態。 <br /> | 
| <a href="toolbar-control-and-button-styles.md">Toolbar 控制項和按鈕樣式</a> | 下列視窗樣式是工具列特有的樣式。 當建立工具列時，它們會與其他視窗樣式合併。<br /><strong>注意</strong> 針對通用控制項 <a href="common-control-versions.md">版本 6.00</a>，如果 <a href="themes-overview.md">視覺效果樣式</a> 與工具列搭配使用，不論樣式設定為何，按鈕一律是透明的。 否則，透明行為是正常的，如使用 <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> 或 <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> 樣式所表示。<blockquote>[!Note]<br />Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 或更新版本中。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</blockquote><br /><br /> | 
| <a href="toolbar-extended-styles.md">工具列擴充樣式</a> | 本節列出工具列控制項支援的延伸樣式。<br /> | 
| <a href="toolbar-standard-button-image-index-values.md">工具列標準按鈕影像索引值</a> | 此區段會指定標準點陣圖內影像的索引值。<br /> | 




 

