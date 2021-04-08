---
description: Windows 檔案總管透過登錄機碼專案來控制通訊協定處理常式的搜尋連接器建立。 透過登錄，實施者和協力廠商可讓新的和舊版通訊協定處理常式參與 Windows 7 搜尋。
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: 建立通訊協定處理常式的搜尋連接器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112481"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>建立通訊協定處理常式的搜尋連接器

Windows 檔案總管透過登錄機碼專案來控制通訊協定處理常式的搜尋連接器建立。 透過登錄，實施者和協力廠商可讓新的和舊版通訊協定處理常式參與 Windows 7 搜尋。

本主題的組織方式如下：

-   [關於 Windows 7 中通訊協定處理常式的搜尋連接器](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [啟用通訊協定處理常式以參與搜尋](#enabling-protocol-handlers-to-participate-in-search)
    -   [停用通訊協定處理常式搜尋連接器建立](#disabling-protocol-handler-search-connector-creation)
    -   [自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [使用登錄字串重新導向](#using-registry-string-redirection)
    -   [還原已刪除的通訊協定處理常式搜尋連接器](#restoring-a-deleted-protocol-handler-search-connector)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>關於 Windows 7 中通訊協定處理常式的搜尋連接器

在 Windows 7 中，搜尋 [ **開始** ] 功能表或 Windows 檔案總管只包含索引位置中的檔案，以及非檔案系統專案，例如遠端資料存放區或具有搜尋連接器的通訊協定處理常式專案。 除了在 [ **開始** ] 功能表和 Shell 搜尋範圍中包含通訊協定處理常式專案之外，搜尋連接器還可讓 [ **開始** ] 功能表在 [ **開始** ] 功能表結果中將通訊協定處理常式專案群組在一起，得到的好處是使用者可以按一下群組標頭，並只從通訊協定處理常式來查看結果。 或者，使用者可以流覽至 [ **搜尋** ] 資料夾，開啟搜尋連接器檔案，然後執行僅包含與該搜尋連接器相關聯之特定通訊協定處理常式中專案的搜尋。

當使用者第一次啟動註冊通訊協定處理常式的應用程式時，Windows 檔案總管會針對使用者 **搜尋** 資料夾中的通訊協定處理常式產生搜尋連接器檔案 (. searchConnector-ms) 。 具有通訊協定處理常式的應用程式可以選擇停用此行為，或自訂通訊協定處理常式搜尋連接器的名稱和描述。

> [!Note]  
> 使用者 **搜尋** 資料夾的位置是% userprofile% \\ 搜尋或 FOLDERID \_ SavedSearches。 FOLDERID SavedSearches 的 GUID \_ 是 {7d1d3a04-debb-4115-95cf-2f29da2920da}。

 

Windows 檔案總管會透過下列各節所述的登錄機碼專案，控制通訊協定處理常式的搜尋連接器建立：

-   [啟用通訊協定處理常式以參與搜尋](#enabling-protocol-handlers-to-participate-in-search)
-   [停用通訊協定處理常式搜尋連接器建立](#disabling-protocol-handler-search-connector-creation)
-   [自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [還原已刪除的通訊協定處理常式搜尋連接器](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> 沒有以程式設計方式為通訊協定處理常式建立搜尋連接器。 它們必須透過登錄設定。

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>啟用通訊協定處理常式以參與搜尋

下表列出登錄機碼及其可能的值。 通訊協定處理常式可以填入部分或所有登錄機碼 <protocol> ，其中以其通訊協定的實際名稱（例如 MAPI、檔案或 csc）取代。



| 登錄機碼                                                                                                                 | 可能的值 (s)                                                                                                                      | 類型       | 註解                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 版本                     | 預設)  (不存在。 否則為1或更大。                                                                               | REG \_ DWORD | 此值可用來偵測已處理之搜尋根的位置範本註冊變更。 如果不存在，請使用0做為預設值。 或者，將版本遞增以通知 Windows 檔案總管因為已安裝較新版本的通訊協定處理常式，所以應重新產生搜尋連接器。 |
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors | 預設)  (不存在。 否則設定為1。                                                                                         | REG \_ DWORD | 如果不存在，請在 [搜尋] 資料夾中建立 searchconnector （ms）檔案。 如果是1，則標示為已處理且不執行任何動作。                                                                                                                                                                                                                                   |
| HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ 描述        | 可當地語系化的字串，其中包含搜尋連接器的描述。                                                              | REG \_ SZ    | 選擇性。 它會用在 searchconnector-ms 檔案的 Description 元素中。                                                                                                                                                                                                                                                                          |
| HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ 名稱               | 用來命名搜尋連接器的當地語系化字串。 用來作為 searchconnector-ms 檔案的名稱。                                    | REG \_ SZ    | 每個位置都必須有唯一的名稱。 如果沒有這個值，就會使用通訊協定處理常式 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 所提供的顯示名稱。                                                                                                                             |
| HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ FolderType         | GUID，可識別要套用至搜尋連接器的 [FOLDERTYPEID](../shell/foldertypeid.md) 。 | REG \_ SZ    | 選擇性。 用於 searchconnector-ms 檔案的 folderType 元素，以指出應該使用哪些範本來顯示結果。 例如，FOLDERTYPEID Documents 的 GUID 值 \_ 。                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>停用通訊協定處理常式搜尋連接器建立

如果您的應用程式透過通訊協定處理常式公開專案以用於應用程式本身，而您不想透過 [ **開始** ] 功能表中的 Shell (公開專案，並 Windows 檔案總管搜尋) ，則需要停用您的通訊協定處理常式建立搜尋連接器。

若要停用搜尋連接器建立，請將 DoNotCreateSearchConnectors 設定為 0x00000001 (1) ，如下列登錄機碼範例所示。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

如果 DoNotCreateSearchConnectors 設定為1，則建議您在通訊協定處理常式公開的每個專案上公開 [OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) 屬性，並將這個屬性的值設為 **TRUE**。 這樣做會讓通訊協定處理常式專案無法出現在 [開始 **] 功能表檔案** 群組之下。

如果 DoNotCreateSearchConnectors 存在且設定為零，則 Windows 檔案總管會為通訊協定處理常式建立搜尋連接器，並在 [ **開始** ] 功能表中傳回通訊協定處理常式專案，並 Windows 檔案總管搜尋。

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType

搜尋連接器名稱不僅會用來識別 [ **搜尋** ] 資料夾中的搜尋連接器，而是用來做為 [ **開始** ] 功能表搜尋結果的群組標頭。 因此，請務必提供搜尋連接器的描述性名稱。 如果登錄機碼中未提供名稱，根據預設，Windows 檔案總管會使用 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 為通訊協定處理常式的搜尋根目錄和空白描述所提供的名稱。 您可以透過登錄機碼專案覆寫預設名稱，而不需要重新命名 IShellFolder 介面。 雖然它看起來不像搜尋連接器名稱，您也可以提供自己的描述來覆寫搜尋連接器的描述。

若要覆寫預設名稱或描述，請設定下列登錄範例所示的專案。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

此外，FolderType 專案可以設定為其中一個 [FOLDERTYPEID](../shell/foldertypeid.md) guid。 值應該是實際的 GUID，而不是其名稱。 例如，{94d6ddcc-4a68-4175-a374-bd584a510b78}，而不是 FOLDERTYPEID \_ 音樂。 FOLDERTYPEID 的 GUID 可以在 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)的 Shlguid .h 標頭檔中取得。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>使用登錄字串重新導向

您可以使用重新 [導向的字串](../intl/using-registry-string-redirection.md) ，以確保您為搜尋連接器提供的名稱可以當地語系化。 您可以為名稱和描述登錄機碼包含可當地語系化的字串，而不是在登錄中輸入實際的字串。

若要針對名稱或描述值包含可當地語系化的字串，請設定下列登錄機碼範例所示的值。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

可當地語系化的字串採用下列格式：

-   @dllname.dll、-resourceID、where：
    -   @dllname.dll 這是包含字串資源之 DLL 的路徑。
    -   resourceID 是字串資源的整數資源識別碼

[SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)函式中描述間接字串的格式，以及附加版本修飾詞的間接字串。

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>還原已刪除的通訊協定處理常式搜尋連接器

由於搜尋連接器是使用者電腦上的檔案，因此可能會被錯誤地刪除。 若要還原所有已刪除的通訊協定處理常式搜尋連接器，請還原預設程式庫。 若要這麼做，請開啟 Windows 檔案總管，以滑鼠右鍵按一下 [連結 **庫** ] 資料夾，然後選取 [ **還原預設程式庫**]。

![顯示 [還原預設程式庫] 功能表選項的螢幕擷取畫面](images/libraries.png)

## <a name="additional-resources"></a>其他資源

-   [IShellItem：： GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[瞭解通訊協定處理常式](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[通知索引變更](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[新增圖示和快顯功能表](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
