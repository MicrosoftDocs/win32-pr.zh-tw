---
title: 範例桌面應用程式的結構
description: 範例桌面應用程式的結構
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- 桌面應用程式、範例
- Windows Media 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- 範例，桌面應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fb377c1bb6ebf943721b55ec6175e65f70ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673612"
---
# <a name="structure-of-the-sample-desktop-application"></a>範例桌面應用程式的結構

範例桌面應用程式是由兩個主要部分所組成：

-   Wmdapp 專案包含大部分的類別，這些類別會顯示使用者介面、處理拖放，以及執行程式的所有必要功能。
-   Proghelp 專案是一個協助程式應用程式，其中包含不必要的類別，可處理狀態通知，以及從桌面手動將檔案傳送至應用程式。

只有當使用者選取 [**選項**] 功能表上的 [**使用作業介面**] 來處理手動檔案傳輸至裝置，並在下載進度表單中遞增狀態列時，此可執行檔才會使用 helper 專案。 應用程式的其餘部分會在 wmdapp 專案中處理。



| 類別                | 檔案                    | 描述                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp .cpp             | 處理使用者介面之父視窗的類別。 此檔案中的程式碼也會處理 CDevFiles 未處理的某些使用者輸入，例如在裝置上建立播放清單或專輯、刪除檔案，以及註冊功能表選項。                                                                                                                                                    |
| CDevices             | 裝置 .cpp             | 此類別會處理主要應用程式視窗的左窗格，其中會列出可用的裝置。 此類別會管理訊息迴圈，這會處理使用者輸入，例如選取裝置，並在裝置選取專案變更時通知 CDevFiles 窗格載入適當的檔案。                                                                              |
| CDevFiles            | Devfiles .cpp            | 此類別會處理主要應用程式視窗的右窗格，其中列出所選裝置上的檔案。 此類別會管理訊息迴圈，並處理使用者輸入，例如將檔案拖曳到裝置上，以及從裝置中刪除檔案。                                                                                                                          |
| CStatus              | 狀態 .cpp              | 在主視窗中處理底部狀態列的類別，其中會列出裝置和檔案的數目，以及所選裝置上的可用和已使用記憶體數量。                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr .cpp            | Windows Media 裝置管理員的最上層介面。 這個類別會處理驗證、抓取最上層的 **IWMDeviceManager** 介面，以及使用 **IWMDMNotification** 介面註冊通知。                                                                                                                                                                  |
| CProgress            | 進度 .cpp            | 主要應用程式專案中的類別，這個類別會建立和管理顯示事件進度的對話方塊。                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData .cpp            | 如果代表裝置上的檔案或資料夾，則為包裝函式 (類別（如果表示裝置上的檔案或資料夾）) 或裝置 (（如果代表裝置) ），以及物件的各種相關資訊（包括大小和屬性）。                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler .cpp | 藉由警示 CDevices 視窗來處理裝置抵達和移除通知。                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper .cpp      | 由 CDevFiles 在區域函式中建立，藉由執行 **IWMDMProgress** 來接收來自 Windows Media 裝置管理員的通知。 CProgress 類別會使用它來判斷進度列中的橫條數量，以及何時完成動作。 此類別定義為 COM 物件，此物件會公開 SDK 介面 **IWMDMProgress** 和自訂介面 IWMDMProgressHelper。 |
| COperationHelper     | Operationhelper .cpp     | 這個類別會實 **IWMDMOperation** 來處理手動傳輸檔案。 它是多執行緒的，可讓它以非同步方式發生，並定義為公開自訂介面 IWMDMOperationHelper 的 COM 物件，以具現化並初始化類別。 只有當使用者選取 [ **選項** ] 功能表中的 [使用作業介面] 時，才會使用這個類別。                            |



 

下列清單概述各種使用者動作所發生的基本步驟：

**啟動時**

啟動範例應用程式時，會發生下列主要步驟。

1.  全域 CWMDM 變數會具現化並經過驗證，並註冊以接收通知
2.  會具現化全域 CDevices，並呼叫 CDevices：： Create 來建立和填滿 [裝置] 窗格。
3.  會具現化全域 CDevFiles，並呼叫 CDevFiles：： Create 來建立 [檔案] 窗格， (在使用者選取裝置) 之前未填滿。
4.  會具現化全域 CStatus，並呼叫 CStatus：： Create 來具現化狀態列。
5.  \_OnViewRefresh 會列舉所有裝置，並將所有裝置初始化並新增 (CItemData) 至 CDevices，並更新狀態列以顯示裝置數目。
6.  CDevices：： AddItem 會將專案新增至代表裝置的 treeview，並以其本身的指標做為 TVITEM. lparam。 所有 CDevice (裝置) 和 CDevFiles (檔案) 物件都會儲存在適當視窗中 treeview 節點的這個成員。

**選取裝置時**

當使用者在應用程式視窗的左窗格中選取裝置時，會發生下列主要步驟。

1.  [CDevices] 視窗會先將一個 WM DRM UPDATEDEVICE 訊息的 click 和 post 張貼 \_ \_ 到本身。
2.  CDevices 會接收自己的訊息，並呼叫 UpdateSelection，告知 global CDevFiles 物件清除所有專案、列舉裝置中的所有最上層專案，並呼叫 CDevFiles：： AddItem 將每個專案新增至 [檔案] 窗格。
3.  最後，CDevices 會呼叫 CDevFiles：： UpdateStatusBar，以正確的裝置和檔案資訊來更新狀態列。

**建立播放清單時**

按一下 [ **容器** ] 功能表上的 [建立播放清單] 之後，應用程式會呼叫區域函式 \_ OnCreatePlaylist，它會執行下列動作：

1.  從全域 CDevFiles 變數取得選取專案的數目。
2.  呼叫區域函數 DlgNamePlaylist 開啟對話方塊，以取得播放清單的名稱。
3.  呼叫 CProgress：： Create 來建立顯示動作進度的對話方塊視窗，並在 CProgress 類別上設定參數，例如標題文字、範圍、目前的值等等。
4.  對 CDevFiles 樹狀檢視物件中所有選取的專案執行迴圈，並在樹狀檢視中要求與每個所選取檔案相關聯的 CItemData 物件，並使用每個檔案遞增進度對話方塊列。 這些檔案會新增至 [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) 介面的陣列。
5.  取得目前選取專案的控制碼，並針對 [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) 介面進行查詢，稍後將用來在裝置上建立新的播放清單。
6.  查詢選取的物件以進行 [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)，並呼叫 [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) 來建立新的 [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)介面。
7.  將 WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST 格式程式碼新增至新的 **IWMDMMetadata** 介面，然後藉由呼叫 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)並傳入中繼資料介面，在裝置上建立播放清單。 方法會捕獲裝置上新 **IWMDMStorage** 的指標。
8.  藉由查詢新的 [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)儲存體來填滿播放清單，並呼叫 [**IWMDMStorage4：： SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences)，並傳入步驟4中所收集 **IWMDMStorage** 指標的陣列。
9.  最後，建立新的 CItemData 物件以保存裝置上的新播放清單、使用新的存放裝置將它初始化，然後呼叫 CDevFiles：： AddItem 將其新增至 CDevFiles 窗格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**桌面應用程式範例**](sample-desktop-application.md)
</dt> </dl>

 

 




