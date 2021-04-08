---
title: CGuiPaper 方法
description: CGuiPaper 的方法摘要如下所示。 這些方法全都在 GUIPAPER 中執行。Cpp。
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671671"
---
# <a name="cguipaper-methods"></a>CGuiPaper 方法

CGuiPaper 的方法摘要如下所示。 這些方法全都在 GUIPAPER 中執行。Cpp。



| 方法                                                         | 描述                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL Init (HINSTANCE hInst、HWND hWnd、TCHAR \* pszCmdLineFile) ; | 初始化 GuiPaper。 要求伺服器建立 COPaper 物件。                                                     |
| HRESULT DrawOn (void) ;                                          | 鎖定此用戶端專用繪圖的紙張。                                                                   |
| HRESULT DrawOff (void) ;                                         | 解除鎖定紙張以允許其他用戶端繪製。                                                                         |
| HRESULT ClearWin (void) ;                                        | 清除顯示視窗，但保留筆墨資料。                                                                           |
| HRESULT PaintWin (void) ;                                        | 清除視窗，並使用目前的筆墨資料重新繪製。                                                                     |
| HRESULT 清除 (void) ;                                           | 清除目前的繪圖內容，並清除顯示視窗。                                                             |
| HRESULT 調整大小 (WORD wWidth、WORD wHeight) ;                     | 調整顯示視窗的大小。                                                                                           |
| HRESULT InkWidth (SHORT nInkWidth) ;                             | 設定繪圖的目前筆墨寬度。                                                                                   |
| HRESULT InkColor (COLORREF crInkColor) ;                         | 設定繪圖的目前筆墨色彩。                                                                                   |
| HRESULT InkSaving (BOOL bInkSaving) ;                            | 開啟和關閉 COPaper 中的筆跡資料儲存。                                                                          |
| HRESULT InkStart (SHORT nX、SHORT nY) ;                          | 啟動筆墨繪圖順序。                                                                                          |
| HRESULT InkDraw (SHORT nX、SHORT nY) ;                           | 繪製筆墨順序資料。                                                                                              |
| HRESULT InkStop (SHORT nX、SHORT nY) ;                           | 停止筆墨繪圖順序。                                                                                           |
| HRESULT ConnectPaperSink (void) ;                                | 將用戶端 PaperSink 物件連接至伺服器 COPaper 來源。                                                    |
| HRESULT DisconnectPaperSink (void) ;                             | 中斷用戶端 PaperSink 物件與伺服器 COPaper 來源的連接。                                                |
| HRESULT Load (void) ;                                            | 從目前的複合檔案載入筆墨資料。                                                                            |
| HRESULT 儲存 (void) ;                                            | 將現有的筆跡資料儲存至目前的複合檔案。                                                                     |
| HRESULT AskSave (void) ;                                         | 檢查繪圖是否已變更。 如果是，則會顯示對話方塊，詢問使用者是否要儲存變更並適當地回應。 |
| HRESULT 開啟 (void) ;                                            | 顯示 Win32 通用對話方塊。 開啟現有的紙張資料複合檔案。                                               |
| HRESULT (void) ;                                          | 顯示 Win32 通用對話方塊。 將目前的檔資料儲存在重新命名的檔案中。                                              |
| COLORREF PickColor (void) ;                                      | 顯示 Win32 通用對話方塊。 要求使用者選擇 [新的畫筆色彩]。                                                      |



 

**Init** 方法會建立以伺服器為基礎的 COPaper 物件，並指派 CGuiPaper 的 m \_ pIPaper 成員。

**AskSave**、 **Open**、 **SaveAs** 和 **PickColor** 方法提供使用 Win32 通用對話方塊的熟悉 GUI 行為。 例如， **Open** 方法會使用 [Win32 Open file name] 對話方塊來要求使用者指定要開啟的檔案名。

本教學課程稍後將詳細說明「 **載入** 」和「 **儲存** 」方法。

**InkSaving**、 **InkStart**、 **InkDraw** 和 **InkStop** 是 **StoClien** 應用程式繪圖功能的集中方法。 **StoClien** 會使用這些 CGuiPaper 方法來捕捉、顯示和儲存互動式繪圖資料（在使用者控制項下出現）。 它們會執行將繪製影像繪製至用戶端視窗，以及將繪圖資料傳遞到伺服器中 COPaper 的雙重角色。 COPaper 會將繪圖資料轉譯為筆跡資料封包以進行儲存。

 

 




