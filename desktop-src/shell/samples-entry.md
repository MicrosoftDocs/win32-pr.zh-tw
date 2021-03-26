---
description: 本節說明 Windows 軟體開發套件 (SDK 中包含的個別 Shell 範例) 以及大部分的情況下，可從 MSDN 程式碼庫下載。
title: Shell SDK 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: CFC388BE-5D74-440c-9C57-7EB853637712
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 61c043e83b5fd2f89e5cdd1e8c0acebeb5fb78d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973300"
---
# <a name="shell-samples"></a>Shell 範例

本節說明 [GitHub](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell)上提供的 Shell 範例。

| 主題           | 目錄                    |
|-------------|-----------------------|
| [Aero 精靈範例](samples-aerowizards.md)                                                                | 示範如何將 Wizard 97 軟體遷移至 Aero Wizard。    |
| [應用程式使用者模型識別碼 (AppUserModelID) 視窗屬性範例](samples-appusermodelidwindowproperty.md) | 示範如何透過 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性控制應用程式視窗的工作列群組行為。                   |
| [自動跳躍清單範例](samples-automaticjumplist.md)              | 示範如何將專案加入至應用程式的自動捷徑清單，包括在常見和最近類別的顯示之間切換。                                                                   |
| [變更通知監看員範例](samples-changenotifywatcher.md)                                               | 示範如何在 Windows 檔案總管命名空間中的資料夾或專案上接聽 Shell 變更通知。                                                                                                               |
| [一般檔案對話方塊模式範例](samples-commonfiledialogmodes.md)                                          | 示範如何使用不同模式的 [通用檔案] 對話方塊，在不關閉對話方塊的情況下，選取檔案、容器 (資料夾) 或檔案和資料夾 (購物籃模式) 。                                                  |
| [一般檔案對話方塊範例](samples-commonfiledialog.md)                                                     | 示範如何使用不同的一般檔案對話 Api 來建立自訂檔案開啟/儲存對話方塊。                                                                                                                         |
| [CreateProcess 動詞範例](samples-createprocessverb.md)                                                    | 示範如何使用 CreateProcess 方法來執行 Shell 動詞命令。                                                                                                                                                    |
| [自訂跳躍清單範例](samples-customjumplist.md)                                                         | 示範如何建立應用程式的自訂捷徑清單，包括新增自訂分類和工作。                                                                                                               |
| [拖放視覺效果範例](samples-dragdropvisuals.md)                                                   | 示範如何使用 Shell 的拖放服務，取得可針對目標和來源提供 Shell 拖放支援的呈現功能。                                                                     |
| [DropTarget 動詞範例](samples-droptargetverb.md)                                                          | 示範如何使用 DropTarget 方法來執行 Shell 動詞。                                                                                                                                                       |
| [執行命令動詞範例](samples-executecommandverb.md)                                                 | 示範如何使用 ExecuteCommand 方法來執行 Shell 動詞。                                                                                                                                                   |
| [在 Explorer 中執行範例](samples-execinexplorer.md)                                                      | 示範如何從 Windows 檔案總管進程呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 函數。                                                                                                                 |
| [Explorer 瀏覽器自訂內容範例](samples-explorerbrowsercustomcontents.md)                          | 示範如何為您的應用程式執行自訂的瀏覽器瀏覽器主。                                                                                                                                          |
| [Explorer 瀏覽器搜尋範例](samples-explorerbrowsersearch.md)                                           | 示範如何使用 Windows 檔案總管瀏覽器控制項，在應用程式中內嵌 Windows 檔案總管，以及如何使用記憶體中的搜尋資料夾來執行搜尋功能。                                           |
| [Explorer 命令動詞範例](samples-explorercommandverb.md)                                               | 示範如何使用 ExplorerCommand 和 ExplorerCommandState 方法來執行 Shell 動詞命令。                                                                                                                        |
| [Explorer 資料提供者範例](samples-explorerdataprovider.md)                                             | 示範如何在瀏覽器中執行 Shell 命名空間延伸模組，包括內容功能表行為和自訂工作。                                                                                                   |
| [檔案使用中範例](samples-fileinuse.md)                                                                | 示範如何自訂 [ **使用中** 的檔案] 對話方塊，以顯示應用程式中目前開啟之檔案的其他資訊和選項。                                                                |
| [檔案作業進度接收](samples-fileoperationprogresssink.md)                                         | 示範如何使用 [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) 介面方法來監視 [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) 介面動作的詳細資料。                      |
| [檔案作業範例](samples-fileoperations.md)                                                          | 示範如何複製、移動、刪除和重新命名檔案系統物件。                                                                                                                                                       |
| [家用群組範例](samples-homegroup.md)                                                                     | 示範如何判斷家庭操作人員的成員資格狀態、列舉 [ **家庭** 工作] Shell 資料夾中的最上層專案，以及啟動 [ **家庭共用嚮導]**。                                                          |
| [已知資料夾範例](samples-knownfolders.md)                                                              | 示範如何定義、註冊、列舉和尋找目前系統上所有已知資料夾的路徑。                                                                                                                |
| [命名空間樹狀目錄控制項範例](samples-namespacetreecontrol.md)                                             | 示範如何為應用程式執行自訂命名空間樹狀目錄控制項。                                                                                                                                             |
| [NonDefaultDropMenuVerb 範例](samples-nondefaultdropmenuverb.md)                                           | 示範如何延伸拖放快捷方式功能表 (有時也稱為內容功能表) 。                                                                                                                         |
| [NotificationIcon 範例](samples-notificationicon.md)                                                       | 示範如何使用 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 和 [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) api 來顯示通知圖示。                                                |
| [使用參數剖析範例](samples-parsingwithparameters.md)                                           | 示範如何利用 Shell 協助程式來利用 shell 程式設計模型，透過使用剖析名稱與專案互動。                                                                                     |
| [播放程式動詞命令範例](samples-playerverbsample.md)                                                            | 示範如何建立可在 Shell 專案和容器上操作的動詞，以播放專案或將專案加入至佇列。                                                                                                     |
| [播放清單建立者範例](samples-playlistcreator.md)                                                        | 示範如何建立在選取的 Shell 專案或容器上操作的動詞，以建立播放清單。                                                                                                                   |
| [配方預覽處理常式範例](samples-recipepreviewhandler.md)                                             | 示範如何撰寫用來在 Windows 檔案總管預覽窗格或其他預覽處理常式主機內顯示檔案預覽的處理常式。                                                                                   |
| [配方縮圖提供者範例](samples-recipethumbnailprovider.md)                                       | 示範如何依檔案類型建立縮圖處理常式，並延伸 Windows 檔案總管。                                                                                                                                     |
| [搜尋資料夾範例](samples-searchfolder.md)                                                              | 示範如何使用 Shell 程式設計模型，建立具有查詢準則約束的搜尋。                                                                                                                                 |
| [Shell 程式庫備份範例](samples-shelllibrarybackup.md)                                                 | 示範如何將程式庫列舉為容器。                                                                                                                                                                        |
| [Shell 程式庫命令列範例](samples-shelllibrarycommandline.md)                                      | 示範如何使用 [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 介面建立命令列應用程式，以提供程式設計的方式來檢查和操作程式庫和程式庫檔案。              |
| [Shell 儲存體範例](samples-shellstorage.md)                                                              | 示範如何在 Shell 容器中建立檔案和資料夾。 另外也會示範如何儲存至檔案對話方塊所傳回的 Shell 專案。                                                                             |
| [同步和共用動詞](samples-syncandshareverbs.md)                                                         | 示範如何註冊在 Windows 檔案總管命令列中擴充「同步處理」和「共用」動詞命令的動詞。                                                                                                            |
| [TabThumbnails 範例](samples-tabthumbnails.md)                                                             | 示範應用程式如何公開多個切換目標 (作為 taskband 上的索引標籤) ，以及如何提供縮圖。                                                                                           |
| [工作列週邊設備狀態範例](samples-taskbarperipheralstatus.md)                                       | 示範工作列圖示重迭和進度列。                                                                                                                                                                         |
| [工作列縮圖工具列範例](samples-taskbarthumbnailtoolbar.md)                                       | 示範縮圖工具列、內嵌于視窗縮圖預覽中的作用中工具列控制項，用來提供視窗的按鍵命令存取權，而不需要使用者還原或啟動應用程式的視窗。 |
| [使用影像 Factory 範例](samples-usingimagefactory.md)                                                   | 示範如何使用 [**IShellItemImageFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory) 介面取得專案的最佳可能影像。                                                                                    |
| [使用縮圖提供者範例](samples-usingthumbnailproviders.md)                                       | 示範如何使用 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 介面，從 Windows 縮圖快取系統中解壓縮專案的縮圖。                                                          |



 

 

 
