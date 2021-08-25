---
description: 本主題說明在程式中使用程式庫時要考慮的一些事項。
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: 在您的程式中使用程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2c76c4ce8bf9114d7294b257c03bcc62adecc947a3d7e651d6f94fa8876d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821108"
---
# <a name="using-libraries-in-your-program"></a>在您的程式中使用程式庫

本主題說明在程式中使用程式庫時要考慮的一些事項。

本主題內容：

-   [程式庫程式設計總覽](#library-programming-overview)
-   [使用程式庫進行程式設計](#programming-with-libraries)
    -   [從已知資料夾移至程式庫](#moving-from-known-folders-to-libraries)
    -   [家庭和共用程式庫](#homegroup-and-shared-libraries)
-   [使用具有程式庫的通用檔案對話方塊](#using-a-common-file-dialog-box-with-libraries)
-   [從使用者介面啟用程式庫選擇](#enabling-library-selection-from-the-user-interface)
-   [存取程式中的程式庫內容](#accessing-library-content-in-a-program)
    -   [使用 IShellLibrary 介面存取程式庫內容](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [使用 Shell Api 存取程式庫內容](#accessing-library-content-with-the-shell-apis)
-   [在文件庫中儲存使用者內容](#saving-user-content-in-a-library)
-   [支援程式庫中的拖放作業](#supporting-drag-and-drop-operations-in-a-library)
-   [保持與程式庫同步](#keeping-in-sync-with-a-library)
    -   [大量更新](#bulk-update)
    -   [Shell API 通知](#shell-api-notification)
    -   [檔案系統 API 通知](#file-system-api-notification)
-   [相關主題](#related-topics)

## <a name="library-programming-overview"></a>程式庫程式設計總覽

程式庫可讓使用者以有意義的方式組織其檔案內容，而不受檔案系統組織的限制。 當您的程式支援程式庫時，可讓使用者以對他們有意義的方式來尋找其內容，同時呈現與 Windows 7 使用者體驗一致的使用者介面。 程式庫也可讓您的程式更容易找到儲存在不同資料夾或不同電腦上的檔案型內容。

本節中的主題描述如何將程式庫支援新增至您的程式，並利用程式庫所提供的新功能。 Windows 7 預設會提供這項支援。 如果您的程式不會修改目前使用的一般檔案對話方塊，則可能需要極少的額外程式設計來支援程式庫。

本節說明程式庫所提供的一些主要功能，以及如何在您的程式中支援這些功能。 透過這種資訊，您可以決定哪些功能會從您的程式提供最佳的使用者體驗。 如果您的程式自訂 [一般檔案] 對話方塊，本節中的資訊可協助您決定如何使用新的 [一般檔案] 對話方塊，在 Windows 7 中使用程式庫並提供對等功能。

## <a name="programming-with-libraries"></a>使用程式庫進行程式設計

Windows shell 程式設計模型會描述程式如何與 Windows Shell 程式設計物件互動。 雖然檔案系統物件（例如檔案和目錄）是由 Windows Shell 物件表示，但並非所有 Windows Shell 物件都是以檔案系統表示。 例如，程式庫是 Windows Shell 物件，這些物件沒有對等檔案系統。 在程式中使用 Windows shell 物件，可讓您的程式存取所有 Shell 物件，而不只是檔案系統物件。

為了獲得最佳結果，您的程式會使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 來與程式庫互動並存取其內容。 程式庫包含資料夾和檔案等檔案系統專案時，程式庫不是檔案系統專案。 因此，不能使用檔案系統 Api 來存取程式庫功能或程式庫內容。

如果您現有的程式目前使用許多檔案系統 Api，則您的程式仍可利用程式庫功能。 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)可提供程式庫中所找到專案的檔案系統參考，而這些檔案系統參考（例如檔案名和路徑）可以傳遞給現有程式中的現有檔案系統 api。

### <a name="moving-from-known-folders-to-libraries"></a>從已知資料夾移至程式庫

Windows 7 之前，通常會使用已知的資料夾（例如我的檔資料夾）作為 [檔案儲存] 或 [檔案開啟] 作業中的預設資料夾。 在 Windows 7 中，應該使用對應的程式庫，如此一來，使用者就會在您的程式中擁有與其他 Windows 7 程式（例如 Windows 檔案總管）相同的體驗。

如果您目前在程式中使用 Windows Shell API，新增程式庫支援很簡單。 例如，如果您目前呼叫 [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) 函式以取得我的檔資料夾的位置，則可以將我的檔已知資料夾的 [**KNOWNFOLDERID**](knownfolderid.md) 值取代為對應程式庫的 **KNOWNFOLDERID** 值。

下表顯示已知資料夾的 [**KNOWNFOLDERID**](knownfolderid.md)值與 Windows 7 中對應程式庫的 **KNOWNFOLDERID** 值之間的關聯性。 

| 已知的資料夾 KNOWNFOLDERID 值 | 程式庫 KNOWNFOLDERID 值 |
|-----------------------------------|------------------------------|
| FOLDERID \_ 檔               | FOLDERID \_ DocumentsLibrary   |
| FOLDERID \_ 圖片                | FOLDERID \_ PicturesLibrary    |
| FOLDERID \_ 音樂                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>家庭和共用程式庫

將程式庫支援新增至您的程式，將可支援在家庭集中共用程式庫。 此家庭群組是由其 [**KNOWNFOLDERID**](knownfolderid.md) 值 [**FOLDERID 的 \_ 家庭**](knownfolderid.md)工作識別。 您的程式可以在 [**IShellLibrary：： GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder)方法的呼叫中設定 [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype)值，以找出使用者的私用或共用預設儲存位置。

## <a name="using-a-common-file-dialog-box-with-libraries"></a>使用具有程式庫的通用檔案對話方塊

使用具有程式庫的通用檔案對話方塊已更新 [一般檔案] 對話方塊，以支援 Windows 7 中的程式庫。 下圖顯示 [一般檔案] 對話方塊在 Windows 7 中如何顯示給使用者。

![顯示文件庫的 [一般檔案] 對話方塊的螢幕擷取畫面](images/libraries-commonfiledialog.png)

在 Windows 7 中，如果您的程式目前顯示 [一般檔案] 對話方塊，而且沒有變更對話方塊範本或連結任何事件，它會自動顯示新的 Windows 7 版本的對話方塊。 具體來說，在呼叫一般檔案對話方塊函式時， [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpfnHook**、 **hInstance**、 **lpTemplatename** 成員都必須是 **Null** ，而且 **OFN \_ ENABLEHOOK** 和 **OFN \_ ENABLETEMPLATE** 旗標必須是純文字。

在 Windows 7 中， [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關的介面會取代舊版 Windows 中所使用的通用檔案對話方塊函式。 Windows 7 仍支援舊版的一般檔案對話方塊函式，但它們並不提供完整的 Windows 7 使用者體驗，也不支援程式庫。 **IFileDialog** 相關介面支援的一些新功能包括：

-   使用者可以存取 Windows 7 Windows 檔案總管所支援的檔案屬性，以搜尋並選取檔案。
-   程式可以使用 Shell 命名空間 API 中的介面和方法來處理專案。
-   此程式可以使用資料驅動自訂模型（而不是資源檔案驅動的自訂模型），將新的控制項加入至 [一般檔案] 對話方塊。

當下列情況時，您應該使用 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關的介面：

-   您必須在 Windows 7 中為程式自訂 [一般檔案] 對話方塊。 這可讓您的程式使用程式庫，並支援自訂對話方塊。
-   您希望使用者能夠從 [一般檔案] 對話方塊中選取多個檔案。 這可確保您取得所選物件的正確路徑，因為程式庫可以有儲存在不同資料夾中的內容。

如需有關 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)相關介面的詳細資訊，請參閱：

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>從使用者介面啟用程式庫選擇

如果您的程式允許使用者選取資料夾，例如匯入或匯出功能，則在 Windows 7 中，它應該也會允許使用者選取媒體櫃。 當系統提示您選取資料夾時， [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面和 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) 函數可讓使用者選取程式庫。 **IFileOpenDialog** 介面優先于 **SHBrowseForFolder** 函數，因為 **IFileOpenDialog** 支援 Windows 7 使用者介面。

若要允許使用者在使用 [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面時選取資料夾，請呼叫 >setoptions \_ 並設定 fos PICKFOLDERS 旗標，並確定 \_ 已清除 [fos FORCEFILESYSTEM] 旗標。


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



若要允許使用者在呼叫 SHBrowseForFolder 函數時選取資料夾，請在 [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) 結構的 ulFlags 成員中，設定 BIF \_ USENEWUI 旗標，並清除 BIF \_ RETURNONLYFSDIRS 旗標。


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>存取程式中的程式庫內容

若要存取程式庫的內容，您必須使用 Windows Shell API。 無法使用檔案系統 API 的功能來存取程式庫內容，因為程式庫不是檔案系統物件。 如果您的程式使用以檔案系統 API 為基礎的自訂檔案瀏覽器，它將無法流覽程式庫或存取程式庫內容。

本節說明如何存取程式庫內容，讓您可以選取更新程式以使用程式庫的最佳方式。

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>使用 IShellLibrary 介面存取程式庫內容

程式存取程式庫內容最簡單的方式是使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)。 如果您正在處理使用檔案系統 API 的程式， **Shell 程式庫 API** 可以傳回程式庫的檔系統資料夾，以將現有程式碼的變更降至最低。


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>使用 Shell Api 存取程式庫內容

由於程式庫物件是 shell 程式設計模型的一部分，因此可以與其他 Windows shell api 搭配使用。 例如，您可以在程式中使用 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 和 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面，以及相關的協助程式函式來存取程式庫的內容，方式就如同使用檔案系統 api 來列舉資料夾和資料夾內容以存取內容一樣。

Windows Shell api 支援兩種列舉模式來存取程式庫的內容：

-   **流覽列舉**

    流覽列舉是預設的列舉模式，會列舉程式庫資料夾的內容。 清除 SHCONTF \_ 導覽 \_ 列舉旗標以使用這個模式。

-   **導覽列舉**

    導覽列舉會列舉程式庫資料夾。 將 SHCONTF \_ 導覽 \_ 列舉旗標設定為使用這個模式。

如果您的程式使用自訂的樹狀目錄控制項來流覽使用者的資料夾，則在導覽列舉模式中列舉資料夾會提供程式庫資料夾的清單，這些資料夾與 Windows 檔案總管在 Windows 7 中列舉資料夾的方式一致。

如需如何在程式中使用這些功能的範例，請參閱 Windows SDK 中的 ShellStorage 範例。

## <a name="saving-user-content-in-a-library"></a>在文件庫中儲存使用者內容

您的程式可以將使用者內容儲存至文件庫，也可以儲存至文件庫中的資料夾。 同樣地，使用者可以儲存至文件庫中的特定資料夾，也可以儲存至程式庫。

每個程式庫都有一個指定為預設儲存位置的資料夾。 預設的儲存位置會在建立程式庫時定義;不過，使用者可以將預設儲存位置重新指派為文件庫中的任何資料夾。 使用者不需要設定預設的儲存位置，而是可以選擇進行變更。 如果使用者刪除目前設定為預設儲存位置的資料夾，程式庫會自動將程式庫中的下一個資料夾設定為預設儲存位置。

有數種方式可將使用者內容儲存至文件庫。

-   **Shell API**

    如果您使用 Shell 程式設計模型並將 Shell 專案（如 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)、IStorage 或 IStream 所代表）儲存至程式庫物件，則會自動將 shell 專案儲存在程式庫的預設儲存位置。

-   **檔案系統 API**

    如果您有現有的程式使用許多檔案系統 API 呼叫，您可以取得定義為程式庫預設儲存位置的資料夾路徑。 然後可以將資料夾路徑傳遞至檔案系統 API。

如需如何在程式中使用這些功能的範例，請參閱 Windows SDK 中的 ShellStorage 範例。

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>支援程式庫中的拖放作業

如果您的程式支援拖放動作，則應該更新這些動作，以支援正確的程式庫互動。 如果將檔案放入文件庫中，則應該將卸載的檔案儲存在預設儲存位置。 如果資料夾已放入程式庫，則應該將放置的資料夾新增為程式庫的新資料夾。 如果將檔案放入非預設儲存位置的現有資料夾，則應該將檔案新增至選取的資料夾。

如需如何為您的程式拖放功能新增程式庫支援的範例，請參閱 Windows SDK 中的 ShellLibraryCommandLine 範例。

## <a name="keeping-in-sync-with-a-library"></a>保持與程式庫同步

本主題說明程式如何將程式庫的內容保持在最新狀態。

### <a name="bulk-update"></a>大量更新

由於使用者可以在您的程式未執行時以互動方式修改程式庫的資料夾，因此，當程式開始探索並儲存程式庫的任何變更時，就應該呼叫 [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) 。 Shell API 提供 **SHResolveLibrary** 函式，可讓程式取得程式庫的目前內容，以及程式庫可能包含的任何資料夾的目前位置。

請注意， [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) 是封鎖函式，可能需要很長的時間才能傳回，取決於程式庫中的變更。 因此，它不應該從 UI 執行緒呼叫。

當程式已更新為最新狀態之後，即可註冊變更通知以維護目前的觀點。

### <a name="shell-api-notification"></a>Shell API 通知

Windows Shell API 提供 [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister)函式，這是在非服務進程收到程式庫變更通知的慣用方式。

若要使用 Windows Shell API 來偵測程式庫中專案的變更，請呼叫 [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister)註冊您的程式，以取得程式庫資料夾中專案變更的通知。 如果任何程式庫或只是在特定的媒體櫃中有變更，此函式就會通知您的程式。 當程式庫變更時，會立即傳送通知。

### <a name="file-system-api-notification"></a>檔案系統 API 通知

服務處理常式中必須使用檔案系統通知。

若要使用檔案系統 API 來偵測程式庫中專案的變更，請列舉程式庫中的資料夾，並針對每個要監視的資料夾呼叫 [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) 。 當受監視的資料夾變更時，您的程式會收到通知。 若要尋找資料夾中已變更之檔案的特定檔案，請呼叫 [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw)。 若要偵測程式庫描述檔案中的變更，請監視包含它的資料夾。 程式庫描述檔案可以在 FOLDERID 程式庫 [**資料夾 \_**](knownfolderid.md) 中找到。 不過，程式庫描述檔案不應該開啟或修改。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於程式庫](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shell 連結](./links.md)
</dt> <dt>

[已知的資料夾](known-folders.md)
</dt> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV 引數 \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
