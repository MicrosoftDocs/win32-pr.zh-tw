---
description: 示範如何註冊為同步根提供者，並將雲端存放裝置提供者整合至流覽窗格的根層級。
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: 整合雲端存放裝置提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21fdc5abfbf9881bfe23b00a924fce989aec7c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564631"
---
# <a name="integrate-a-cloud-storage-provider"></a>整合雲端存放裝置提供者

當您有雲端存放裝置提供者時，您必須採取幾個步驟，才能為使用者提供一致且慣用的體驗。 這兩個專案會註冊為同步根提供者，並將您的應用程式整合到流覽窗格的根層級中。

> [!IMPORTANT]
> 從 Windows 10 開始，才支援整合雲端存放裝置提供者。

 

第一件事是註冊為同步根提供者。 這可讓 Windows Shell 知道您的應用程式，而且您的應用程式會負責同步處理根的檔案。 這也可讓其他應用程式知道您要同步處理這些檔案，讓它們能夠適當地回應。 然後，其他應用程式就可以使用 [**StorageFile**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) 來取得應用程式的 [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) 和 [**Id**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) 。

為了註冊為同步根提供者，您必須建立多個登錄專案。 在提供索引鍵/值組的清單之前，以下是一些您應該以自己的應用程式資料取代的預留位置。

-   *\[ 儲存提供者 \] 識別碼*：雲端儲存體提供者的名稱。 無論您的應用程式版本為何，此名稱都應該一致。 這是 OneDrive 的範例。
-   *\[ Windows sid \]*：識別使用者的唯一 Windows sid。 如果您的應用程式在單一電腦上支援多個使用者的多個安裝，則需要此部分。
-   *\[ 帳戶識別碼 \]*：此使用者目前帳戶的服務提供者識別碼。 有些提供者需要能夠為使用者提供多個同步處理根。 其中一個範例是工作和個人帳戶。 *帳戶識別碼* 可讓您為一位使用者註冊多個帳戶。 如果您的提供者支援每位使用者多個同步處理根，則需要此部分。

這些預留位置會合並在一起，以形成同步根識別碼。您必須將 **！** 形成同步根識別碼時，每個預留位置之間的字元。以下是需要建立的機碼值組。

-   **HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ DisplayNameResource_* ：指向 Windows Shell 或其他應用程式可以為您的同步根目錄取得使用者易記名稱的資源。
-   **HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ IconResource_* ：指向 Windows Shell 或其他應用程式可以為您的同步根目錄取得圖示的資源。
-   **HKLM \\軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\** _\[ 儲存提供者 \] 識別碼_*_！_*_\[ Windows SID \]_ *_！_*_\[ 帳戶識別碼 \]_ *_\\ UserSyncRoots \\_* _\[ Windows SID \]_ ：同步根目錄所在磁片上的位置。

除了註冊為同步根提供者之外，您也希望使用者能夠輕鬆存取您提供的資料。 檔案總管命名空間的設計目的，是為了提供可輕鬆存取的方法。 建立提供者的命名空間延伸模組並將其併入檔案總管視窗中，可讓使用者與服務的根層級互動，就像是與其他檔案總管專案搭配使用一樣。 本主題說明如何擴充檔案總管命名空間，讓您的提供者會出現在流覽窗格中的根層級。

檔案總管視窗的導覽窗格是顯示在左側視窗的部分。 在下圖中，您可以看到此使用者的命名空間結構。 流覽窗格中的根層級包括 **OneDrive**、這部 **電腦** 和 **網路** 的物件。 遵循這些步驟會將您的延伸模組加入至相同的層級。

![瀏覽窗格](images/navigationpane.png)

若要將擴充功能新增至流覽窗格，您必須先具備下列各項，才能編輯登錄：

-   檔系統資料夾，其中包含要向使用者顯示的資料。

-   將出現在流覽窗格中的雲端服務名稱。 如果您的服務支援多個帳戶，這也可以是實例的名稱。

-   應用程式的可識別圖示。

-   應用程式的 CLSID。 為您的應用程式產生 CLSID 的其中一種方式是使用 Uuidgen.exe。 如需 CLSID 的詳細資訊，請參閱 [Clsid 金鑰](../com/clsid-key-hklm.md) 。

下列步驟會修改登錄，以便在檔案總管命名空間中取得必要的資訊。 特定步驟會執行三項工作。

-   在登錄中為您的 CLSID 建立機碼，其中包含您的延伸模組名稱和圖示值，以及定義其行為的其他資訊。

-   將您的延伸模組設定為整合到適當位置的流覽窗格中，並具有適當的可見度。

-   設定您的延伸模組，使其在導覽窗格中具有元素的預期行為。

這些指示特別使用 **reg.exe** 命令，不過您可以使用任何您選擇的登錄編輯工具。 您甚至可以將這些步驟整合到以程式設計方式更新登錄的安裝程式。

## <a name="instructions"></a>指示

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>步驟1：加入您的 CLSID 並命名您的延伸模組

在 [HKEY 目前使用者] 下，將您的擴充功能名稱新增至登錄 \_ \_ 。 您也將新增此延伸模組的唯一識別碼。 每位使用者可以加入多個擴充功能，但在此情況下，每個延伸模組都需要唯一的名稱和識別碼。 在這些步驟的其餘部分中，此名稱和識別碼必須保持一致。 在此範例中，名稱是 *MyCloudStorageApp*。

> [!IMPORTANT]
> 在這些步驟中 (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) 提供的識別碼，只是作為範例使用。 您必須將此變更為您的唯一 CLSID。

 

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d "MyCloudStorageApp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>步驟2：設定圖示的影像

提供要顯示在導覽窗格中的圖示路徑。 在下列範例中， *1043* 是指指定之 DLL 中圖示的資源識別碼。

> [!IMPORTANT]
> 您必須更新映射路徑。 它應該指向您的應用程式安裝映射的一般路徑。

 

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t REG \_ EXPAND \_ SZ/d%% SystemRoot%% \\ system32 \\imageres.dll，-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>步驟3：將您的擴充功能新增至流覽窗格並讓它顯示

將此值設定為0x1 表示延伸模組應固定。 這可確保預設會對使用者顯示。 使用者的預設設定是只有釘選的專案會顯示在流覽窗格中。 使用者可以在流覽窗格中按一下滑鼠右鍵，然後選取 [ **顯示所有資料夾**] 來變更該設定。 如果您不想要釘選您的延伸模組，您可以將此值設定為0x0。 這不會移除您的延伸模組，只會防止預設顯示給使用者。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/v SYSTEM. IsPinnedToNameSpaceTree/t REG \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>步驟4：在流覽窗格中設定延伸模組的位置

這一點很重要，因為這是為了確保流覽窗格能為使用者提供一致的體驗。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/V SortOrderIndex/t REG \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>步驟5：提供裝載您延伸模組的 dll。

使用 shell32.dll 模擬預設的 windows 資料夾。 只有當您有特定原因要進行變更時，才需要變更，並熟悉命名空間延伸模組。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32/ve/t REG \_ EXPAND \_ SZ/d%% systemroot%% \\ system32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>步驟6：定義實例物件

指出您的命名空間延伸模組應如檔案總管中的其他檔案資料夾結構一樣運作。 如需 shell 實例物件的詳細資訊，請參閱 [使用 Shell 實例物件建立 Shell 延伸](/previous-versions/ms997573(v=msdn.10))模組。

**reg add HKCU \\ Software \\ 類別 \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance/v clsid/T REG \_ SZ/d {0E5AAE11-A475-4c5b-AB00-C66DE400274E}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>步驟7：提供目的檔案夾的檔案系統屬性

這是必要的，以確保檔案總管為使用者提供一致且預期的體驗。 此命令會設定 **檔 \_ 屬性 \_ 目錄** 和 **檔 \_ 屬性 \_ READONLY**，兩者都是 [**檔案屬性常數**](../fileio/file-attribute-constants.md)。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ INSTANCE \\ InitPropertyBag/v Attributes/t REG \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>步驟8：設定同步根的路徑

設定同步根的路徑。

**reg add HKCU \\ Software \\ 類別 \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ 實例 \\ InitPropertyBag/v TargetFolderPath/t REG \_ EXPAND \_ SZ/d%% USERPROFILE%% \\ MyCloudStorageApp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>步驟9：設定適當的 shell 旗標

設定將命名空間延伸模組釘選到檔案總管樹狀結構所需的一些旗標。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v FolderValueFlags/t REG \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>步驟10：設定適當的旗標，以控制您的 shell 行為

設定適當的 [**SFGAO**](sfgao.md) 旗標。 相關的旗標為 SFGAO \_ CANCOPY、SFGAO \_ CANLINK、SFGAO \_ STORAGE、SFGAO \_ HASPROPSHEET、SFGAO \_ STORAGEANCESTOR、SFGAO \_ FILESYSANCESTOR、SFGAO \_ FOLDER、SFGAO \_ FILESYSTEM 和 SFGAO \_ HASSUBFOLDER。

**reg add HKCU \\ Software \\ class \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v Attributes/t REG \_ DWORD/d 0xF080004D/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>步驟11：在命名空間根目錄中註冊您的延伸模組

將命名空間延伸模組設定為 [桌面] 資料夾的子系。

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d MyCloudStorageApp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>步驟12：從桌面上隱藏您的延伸模組

您的延伸模組必須只出現在檔案總管的導覽窗格上。 命名空間延伸模組的運作方式不像一般快捷方式。 因此，您不應該使用這個方法來建立桌面快捷方式。

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/t REG \_ DWORD/d 0x1/f**

 

 
