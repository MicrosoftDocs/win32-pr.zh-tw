---
title: 資料指標
description: 本節討論資料指標，這是螢幕上的位置是由指標裝置（例如滑鼠、畫筆或軌跡球）控制的小型圖片。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- 資源，資料指標
- 資料指標，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7be5b8e213dd1911d2227a3dce4b61078ab1a22711d4e765525c7fbd5bd08d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712608"
---
# <a name="cursors"></a>資料指標

游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。 在此總覽的其餘部分，「滑鼠」一詞是指任何指標裝置。

當使用者移動滑鼠時，系統會據以移動游標。 資料指標函數可讓應用程式建立、載入、顯示、動畫、移動、限制和終結資料指標。

### <a name="in-this-section"></a>本節內容



| 名稱                                     | 描述                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [關於資料指標](about-cursors.md)       | 討論標準資料指標。<br/>                    |
| [使用資料指標](using-cursors.md)       | 討論如何執行與資料指標相關的工作。<br/> |
| [資料指標參考](cursor-reference.md) | 包含 API 參考。<br/>                        |



 

### <a name="cursor-functions"></a>資料指標函數



| 名稱                                                 | 描述                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | 將游標範圍設為螢幕上的矩形區域。 如果後續的游標位置 (由 [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) 函式所設定，或滑鼠) 位於矩形外，系統會自動調整位置，以將游標放在矩形區域內。 <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | 複製指定的資料指標。 <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | 建立具有指定大小、位模式和作用點的資料指標。 <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | 終結資料指標，並釋出資料指標所佔用的任何記憶體。 請勿使用這個函數來終結共用資料指標。<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | 抓取游標所限制之矩形區域的螢幕座標。 <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | 抓取目前資料指標的控制碼。 <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | 抓取全域資料指標的相關資訊。<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | 以螢幕座標抓取游標的位置。<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | 抓取資料指標在實體座標中的位置。<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | 從可執行檔載入指定的資料指標資源， (.EXE) 與應用程式實例相關聯的檔案。<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | 根據檔案中包含的資料來建立資料指標。 <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | 設定資料指標圖形。 <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | 將游標移至指定的螢幕座標。 如果新座標不在最新的 [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) 函式呼叫所設定的螢幕矩形內，系統會自動調整座標，讓游標停留在矩形內。 <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | 設定資料指標在實體座標中的位置。<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | 讓應用程式自訂系統資料指標。 它會將 *id* 參數所指定的系統資料指標內容取代為 *hcur* 參數所指定之資料指標的內容，然後終結 *hcur*。 <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | 顯示或隱藏游標。 <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>資料指標通知



| 名稱                                  | 描述                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ SETCURSOR**](wm-setcursor.md) | 如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。 <br/> |



 

### <a name="cursor-structures"></a>資料指標結構



| 名稱                             | 描述                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | 包含全域資料指標資訊。<br/> |



 

 

 





