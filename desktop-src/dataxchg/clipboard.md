---
title: 剪貼簿
description: 剪貼簿是一組可讓應用程式傳輸資料的函式和訊息。
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\clipboard.htm
keywords:
- 剪貼簿，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62be59ad369b85b6c9f8b4fb46f793ee68b7081d4c190b85a35a8bacea7b4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128600"
---
# <a name="clipboard"></a>剪貼簿

*剪貼* 簿是一組可讓應用程式傳輸資料的函式和訊息。 由於所有應用程式都有存取剪貼簿的許可權，因此可以輕鬆地在應用程式之間或應用程式內傳輸資料。

本總覽不說明如何複製和貼上連結或內嵌的物件。 如需這些主題的詳細資訊，請參閱元件物件模型 (COM) 檔集。

### <a name="in-this-section"></a>本節內容



| 名稱                                                          | 描述                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於剪貼簿](about-the-clipboard.md)<br/>     | 討論剪貼簿。<br/>                                                                                                                                                                                                                                 |
| [剪貼簿格式](clipboard-formats.md)<br/>         | 討論剪貼簿格式。 視窗可以在剪貼簿上放置一個以上的物件，每個物件都代表不同剪貼簿格式的相同資訊。 使用者不需要留意剪貼簿上物件所使用的剪貼簿格式。<br/> |
| [剪貼簿作業](clipboard-operations.md)<br/>   | 討論剪貼簿作業。 當您剪下、複製或貼上資料時，視窗應該使用剪貼簿。 視窗會將資料放在剪貼簿上，以進行剪下和複製作業，並從剪貼簿取得貼上作業的資料。<br/>                  |
| [HTML 剪貼簿格式](html-clipboard-format.md)<br/> | 討論 HTML 剪貼簿格式。<br/>                                                                                                                                                                                                                     |
| [使用剪貼簿](using-the-clipboard.md)<br/>     | [剪貼簿檢視器] 視窗會顯示剪貼簿的目前內容，並在剪貼簿內容變更時收到訊息。<br/>                                                                                                                       |
| [剪貼簿參考](clipboard-reference.md)<br/>     | 包含 API 參考。<br/>                                                                                                                                                                                                                              |



 

### <a name="clipboard-functions"></a>剪貼簿函數



| 名稱                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)<br/>       | 將指定的視窗置於系統維護的剪貼簿格式接聽程式清單中。<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain)<br/>                   | 從剪貼簿檢視器鏈中移除指定的視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)<br/>                               | 關閉剪貼簿。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats)<br/>                 | 抓取目前剪貼簿上的不同資料格式數目。 <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)<br/>                               | 清空剪貼簿，並釋放剪貼簿中的資料控制碼。 然後，此函式會將剪貼簿的擁有權指派給目前開啟 [剪貼簿] 的視窗。 <br/>                                                                                                                                                                                                                                                                                    |
| [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats)<br/>                   | 列舉剪貼簿目前可用的資料格式。 <br/> 剪貼簿資料格式會儲存在已排序的清單中。 若要執行剪貼簿資料格式的列舉，您需要對 [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) 函數進行一連串的呼叫。 針對每個呼叫， *format* 參數會指定可用的剪貼簿格式，而函數會傳回下一個可用的剪貼簿格式。 <br/>                         |
| [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata)<br/>                           | 以指定的格式抓取剪貼簿中的資料。 剪貼簿必須先前已開啟。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)<br/>               | 從剪貼簿中，以指定的註冊格式名稱抓取。 函數會將名稱複製到指定的緩衝區。 <br/>                                                                                                                                                                                                                                                                                                                                |
| [**GetClipboardOwner**](/windows/desktop/api/Winuser/nf-winuser-getclipboardowner)<br/>                         | 抓取剪貼簿目前擁有者的視窗控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)<br/>       | 抓取目前視窗工作站的剪貼簿序號。 <br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer)<br/>                       | 抓取剪貼簿檢視器鏈中第一個視窗的控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow)<br/>               | 抓取目前開啟剪貼簿的視窗控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat)<br/>       | 抓取指定清單中第一個可用的剪貼簿格式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**GetUpdatedClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-getupdatedclipboardformats)<br/>       | 抓取目前支援的剪貼簿格式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)<br/>       | 判斷剪貼簿是否包含指定格式的資料。 <br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)<br/>                                 | 開啟剪貼簿進行檢查，並防止其他應用程式修改剪貼簿內容。 <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)<br/>             | 註冊新的剪貼簿格式。 這種格式可以用來做為有效的剪貼簿格式。 <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)<br/> | 從系統維護的剪貼簿格式接聽程式清單中移除指定的視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)<br/>                           | 以指定的剪貼簿格式將資料放在剪貼簿上。 視窗必須是目前的剪貼簿擁有者，而且應用程式必須呼叫 [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) 函數。  (回應 [**WM \_ RENDERFORMAT**](wm-renderformat.md)訊息時，剪貼簿擁有者在呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)之前，不能呼叫 **OpenClipboard** 。 ) <br/> |
| [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)<br/>                       | 將指定的視窗加入至剪貼簿檢視器的鏈。 每當剪貼簿的內容變更時，剪貼簿檢視器視窗就會收到 [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 訊息。 <br/>                                                                                                                                                                                                                                                           |



 

### <a name="clipboard-messages"></a>剪貼簿訊息



| 名稱                                     | 描述                                                                                                                                                                                                                                                             |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 清除**](wm-clear.md)<br/> | 傳送至編輯控制項或下拉式方塊來刪除 (清除：從編輯控制項) 目前的選取專案（如果有的話）。 <br/>                                                                                                                                                |
| [**WM \_ 複製**](wm-copy.md)<br/>   | 傳送至編輯控制項或下拉式方塊，以 [**CF \_ 文字**](standard-clipboard-formats.md) 格式將目前的選取範圍複製到剪貼簿。 <br/>                                                                                                       |
| [**WM \_ 剪下**](wm-cut.md)<br/>     | 傳送至編輯控制項或下拉式方塊，以刪除 (剪下) 目前的選取專案（如果有的話），並將已刪除的文字複製到 [**CF \_ 文字**](standard-clipboard-formats.md) 格式的剪貼簿。 <br/>                                        |
| [**WM \_ 貼上**](wm-paste.md)<br/> | 傳送至編輯控制項或下拉式方塊，將剪貼簿目前的內容複寫到目前插入號位置的編輯控制項。 只有當剪貼簿包含 [**CF \_ 文字**](standard-clipboard-formats.md) 格式的資料時，才會插入資料。 <br/> |



 

### <a name="clipboard-notifications"></a>剪貼簿通知



| 名稱                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md)<br/>   | 由剪貼簿檢視器視窗傳送給剪貼簿擁有者，以要求 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 剪貼簿格式的名稱。 <br/>                                                                                                                                                                                                                                 |
| [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)<br/>       | 從鏈中移除視窗時，傳送至剪貼簿檢視器鏈中的第一個視窗。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md)<br/>   | 當剪貼簿的內容變更時傳送。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md)<br/> | 當 [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) 函式的呼叫清空剪貼簿時，傳送給剪貼簿擁有者。 <br/>                                                                                                                                                                                                                                                                                    |
| [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md)<br/>       | 當剪貼簿的內容變更時，傳送至剪貼簿檢視器鏈中的第一個視窗。 這可讓剪貼簿檢視器視窗顯示剪貼簿的新內容。 <br/>                                                                                                                                                                                                                      |
| [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md)<br/> | 由剪貼簿檢視器視窗傳送給剪貼簿擁有者。 當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而且在剪貼簿檢視器的水準捲軸中發生事件時，就會發生這種情況。 擁有者應該滾動剪貼簿影像，並更新捲軸值。 <br/>                                                             |
| [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md)<br/>     | 當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區需要重新繪製時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。 <br/>                                                                                                                                                                    |
| [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)<br/> | 如果剪貼簿擁有者有延遲轉譯一或多個剪貼簿格式，則會在終結之前傳送給剪貼簿擁有者。 若要讓剪貼簿的內容仍然可供其他應用程式使用，剪貼簿擁有者必須以它能夠產生的所有格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) 函式將資料放在剪貼簿上。 <br/> |
| [**WM \_ RENDERFORMAT**](wm-renderformat.md)<br/>         | 如果已延遲轉譯特定的剪貼簿格式，且應用程式已要求該格式的資料，則傳送給剪貼簿擁有者。 剪貼簿擁有者必須以指定的格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) 函式將其放在剪貼簿上。 <br/>                                                                                              |
| [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md)<br/>       | 當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區已變更時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。 <br/>                                                                                                                                                                    |
| [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md)<br/> | 當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，並在剪貼簿檢視器的垂直捲動條中發生事件時，將剪貼簿檢視器視窗傳送給剪貼簿擁有者。 擁有者應該滾動剪貼簿影像，並更新捲軸值。 <br/>                                                                            |



 

### <a name="structures"></a>結構



| 名稱                                            | 描述                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)<br/> | 定義用來透過剪貼簿交換中繼檔資料的中繼檔圖片格式。 <br/> |



 

 

 





