---
description: 本主題討論應用程式如何公開啟用特定案例所需的相關資訊。
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: 應用程式註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac1c72614ce3241cbac6b880b0d9f5f84f9fbf85c8ee022d83574df6d86e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224940"
---
# <a name="application-registration"></a>應用程式註冊

本主題討論應用程式如何公開啟用特定案例所需的相關資訊。 這包括找出應用程式所需的資訊、應用程式支援的動詞，以及應用程式可以處理的檔案類型。

本主題的組織方式如下：

-   [尋找應用程式可執行檔](#finding-an-application-executable)
-   [註冊應用程式](#registering-applications)
    -   [使用應用程式路徑子機碼](#using-the-app-paths-subkey)
    -   [使用應用程式子機碼](#using-the-applications-subkey)
-   [註冊動詞和其他檔案關聯資訊](#registering-verbs-and-other-file-association-information)
-   [註冊認知型別](#registering-a-perceived-type)
-   [相關主題](#related-topics)

> [!Note]  
> 您也可以在 [設定程式存取和電腦預設值] (SPAD) 中註冊應用程式，並將您的預設程式 (SYDP) 控制台應用程式。 如需 SPAD 和 SYDP 應用程式註冊的相關資訊，請參閱檔案 [關聯和預設程式的指導方針](appguide-fa-defpro.md)，以及 [設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md)。

 

## <a name="finding-an-application-executable"></a>尋找應用程式可執行檔

使用 *lpFile* 參數中的可執行檔名稱呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)函式時，函式會尋找檔案的數個位置。 建議您在 **應用程式路徑** 登錄子機碼中註冊您的應用程式。 這麼做可避免應用程式需要修改系統 PATH 環境變數。

檔案會在下列位置中尋找：

-   目前的工作目錄。
-   **Windows** 目錄僅 (不會) 搜尋任何子目錄。
-   **Windows \\ System32** 目錄。
-   PATH 環境變數中所列的目錄。
-   建議： **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑**

## <a name="registering-applications"></a>註冊應用程式

應用程式 **路徑** 和 **應用程式** 登錄子機碼都是用來代表應用程式註冊和控制系統的行為。 [ **應用程式路徑** ] 子機碼是慣用的位置。

### <a name="using-the-app-paths-subkey"></a>使用應用程式路徑子機碼

在 Windows 7 和更新版本中，強烈建議您安裝每位使用者的應用程式，而不是每部電腦的應用程式。 針對每位使用者安裝的應用程式，可以在 **HKEY \_ 目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑** 下註冊。 針對電腦的所有使用者所安裝的應用程式，都可以在 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑** 中進行註冊。

在 **應用程式路徑** 下找到的專案主要用於下列用途：

-   將應用程式的可執行檔名稱對應至該檔案的完整路徑。
-   在每個應用程式上，以每個進程為基礎，將資訊預先暫止至 PATH 環境變數。

如果 **應用程式路徑** 的子機碼名稱與檔案名相符，則 Shell 會執行兩個動作：

-    (預設) 專案會用來做為檔案的完整路徑。
-   該子機碼的路徑專案會預先暫止至該進程的 PATH 環境變數。 如果這不是必要的，則可以省略路徑值。

可能要注意的問題包括：

-   Shell 會將命令列的長度限制為最大 \_ 路徑 \* 2 個字元。 如果有許多檔案列為登錄專案或其路徑很長，則清單稍後的檔案名可能會在截斷命令列時遺失。
-   有些應用程式不接受命令列中的多個檔案名。
-   某些接受多個檔案名的應用程式無法辨識 Shell 提供這些名稱的格式。 Shell 將參數清單提供為加上引號的字串，但有些應用程式可能需要不含引號的字串。
-   並非所有可拖曳的專案都是檔案系統的一部分;例如，印表機。 這些專案沒有標準的 Win32 路徑，所以沒有任何方法可提供有意義的 *lpParameters* 值給 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。

使用 DropTarget 專案可避免這些潛在問題，方法是提供所有剪貼簿格式的存取權，包括長檔案清單的 [CFSTR \_ SHELLIDLIST](clipboard.md) (，以及) 非檔案系統物件) 和 [CFSTR \_ FILECONTENTS](clipboard.md) (。

**使用應用程式路徑子機碼註冊及控制應用程式的行為**：

1.  將名稱與可執行檔相同的子機碼新增至 [ **應用程式路徑** ] 子機碼，如下列登錄專案所示。

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  請參閱下表，以取得 **應用程式路徑** 子機碼專案的詳細資料。 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>登錄項目</th>
    <th>詳細資料</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>(預設值)</td>
    <td>是應用程式的完整路徑。  (預設) 專案中提供的應用程式名稱，可以使用或不使用其 .exe 延伸模組來陳述。 如有必要， <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 函式會在搜尋 <strong>應用程式路徑</strong> 子機碼時新增擴充功能。 專案屬於 <strong>REG_SZ</strong> 類型。</td>
    </tr>
    <tr class="even">
    <td>DontUseDesktopChangeRouter</td>
    <td>偵錯工具應用程式必須有這項功能，以避免在處理 Windows 檔案總管進程時發生檔案對話方塊鎖死。 但是，設定 DontUseDesktopChangeRouter 專案會產生稍微不有效率的變更通知處理。 專案屬於 <strong>REG_DWORD</strong> 類型，而值為0x1。</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>是)  (CLSID 的類別識別碼。 DropTarget 專案包含物件的 CLSID (通常是本機伺服器，而不是執行 <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>的同進程伺服器) 。 根據預設，當放置目標是可執行檔，且未提供任何 DropTarget 值時，Shell 會將已卸載的檔案清單轉換成命令列參數，並透過<em>lpParameters</em>將其傳遞至<a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 。</td>
    </tr>
    <tr class="even">
    <td>路徑</td>
    <td>藉由呼叫 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>來啟動應用程式時，以分號分隔的目錄清單格式提供字串 (，) 附加至 PATH 環境變數。 它是 .exe 的完整路徑。 這是 <strong>REG_SZ</strong>。 在<strong>Windows 7 和更新版本</strong>中，類型可以<strong>REG_EXPAND_SZ</strong>，而且通常<strong>REG_EXPAND_SZ</strong> % ProgramFiles%。
    <blockquote>
    [!Note]<br />
除了 Shell 辨識的 (預設) 、路徑和 DropTarget 專案之外，應用程式也可以將自訂值新增至其可執行檔的 <strong>應用程式路徑</strong> 子機碼。 我們鼓勵應用程式開發人員使用應用程式 <strong>路徑</strong> 子機碼，以提供應用程式特定路徑，而不是將新增至全域系統路徑。
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>建立字串，其中包含指定之索引鍵的 URL 通訊協定配置。 這可包含多個登錄值，以指出支援的配置。 此字串的格式如下 <strong>scheme1： scheme2</strong>。 如果這份清單不是空的，則會將 <strong>file：</strong> 新增至字串。 定義 <em>SupportedProtocols</em> 時，會隱含地支援此通訊協定。 <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>指出您的應用程式可以接受 URL (而不是在命令列上) 的檔案名。 可以直接從網際網路開啟檔的應用程式（例如網頁瀏覽器和媒體播放機）應該設定此專案。 <br/> 當 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 函式啟動應用程式，且未設定 UseUrl = 1 值時， <strong>ShellExecuteEx</strong> 會將檔下載至本機檔案，並在本機複本上叫用處理程式。<br/> 例如，如果應用程式具有這個專案集，且使用者以滑鼠右鍵按一下儲存在 web 伺服器上的檔案，則會提供開啟的動詞。 如果沒有，使用者將必須下載檔案並開啟本機複本。 <br/> UseUrl 專案屬於 <strong>REG_DWORD</strong> 類型，而值為0x1。<br/> 在 Windows Vista （含）以前版本中，此專案指出當透過 ShellExecuteEx 呼叫時，應將 URL 傳遞至應用程式以及本機檔案名。 在 Windows 7 中，它表示應用程式可以瞭解任何傳遞給它的 HTTP 或 HTTPs url，也不需要提供快取檔案名稱。 此登錄機碼與 <em>SupportedProtocols</em> 索引鍵相關聯。<br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>使用應用程式子機碼

透過在 **HKEY \_ 類別的 \_ 根** 應用程式下包含登錄專案ApplicationName.exe子機碼 \\  \\  ，應用程式可以提供下表所示的應用程式特定資訊。



| 登錄項目                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| shell \\ 動詞                      | 提供從 OpenWith 呼叫應用程式的動詞方法。 如果沒有在這裡指定動詞定義，系統會假設應用程式支援 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)，並在命令列上傳遞檔案名。 此功能適用于所有動詞方法，包括 DropTarget、ExecuteCommand 和動態資料交換 (DDE) 。                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | 讓應用程式提供特定圖示來代表應用程式，而不是儲存在 .exe 檔案中的第一個圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | 提供一種方式，讓您取得可當地語系化的應用程式名稱，而不只是顯示的版本資訊，可能無法當地語系化。 關聯查詢 [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) 會讀取這個登錄專案值，並切換回使用版本資訊中的 FileDescription 名稱。 如果遺漏該名稱，關聯查詢會預設為檔案的顯示名稱。 應用程式應該使用 **ASSOCSTR \_ FRIENDLYAPPNAME** 來取得此資訊，以取得正確的行為。                                                                                                                                                                        |
| SupportedTypes                   | 列出應用程式所支援的檔案類型。 這樣做可讓應用程式列在 [ **開啟檔案** ] 對話方塊的 [cascade] 功能表中。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | 指出未指定任何應用程式來開啟此檔案類型。 請注意，如果已依檔案類型設定應用程式的 OpenWithProgIDs 子機碼，而且 ProgID 子機碼本身也沒有 NoOpenWith 專案，則該應用程式將會出現在建議或可用的應用程式清單中，即使已指定 NoOpenWith 專案也一樣。 如需詳細資訊，請參閱如何 [在 [開啟方式] 對話方塊中加入應用程式](how-to-include-an-application-on-the-open-with-dialog-box.md) ，以及 [如何從 [開啟檔案] 對話方塊中排除應用程式](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)。<br/> |
| IsHostApp                        | 指出程式是一種主機進程，例如 Rundll32.exe 或 Dllhost.exe，而且不應該被視為 [ **開始** ] 功能表釘選，或包含在最常使用的 (MFU) 清單中。 當使用包含非 null 引數清單的快捷方式啟動，或 [ (AppUserModelIDs) 的明確應用程式使用者模型識別碼 ](appids.md)啟動時，可以將該程式釘選 () 的快捷方式。 這類快速鍵是要包含在 最常使用清單中的候選項目。                                                                                                                                                                                                                                                  |
| NoStartPage                      | 指出應該從 [ **開始** ] 功能表排除應用程式可執行檔和快捷方式，並將其釘選或包含在 最常使用清單中。 此專案通常用來排除系統工具、安裝程式和 uninstallers，以及讀我檔案。                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | 如果沒有此應用程式的可釘選快捷方式，而不是第一次遇到的視窗圖示，則會讓工作列使用這個可執行檔的預設圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | 指定用來覆寫工作列圖示的圖示。 視窗圖示通常用於工作列。 設定 TaskbarGroupIcon 專案時，系統會改為使用應用程式 .exe 中的圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>範例

透過 **HKEY \_ 類別 \_ 根** \\ **應用程式** \\ *ApplicationName.exe* 子機碼的一些應用程式註冊範例如下所示。 所有登錄專案值都是 **reg \_ sz** 型別，但 **DefaultIcon** 是 **reg \_ EXPAND \_ sz** 型別。

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>註冊動詞和其他檔案關聯資訊

在 **HKEY \_ 類別 \_ 根** SystemFileAssociations 下註冊的子機碼， \\ 可讓 Shell 定義檔案類型之屬性的預設行為，並啟用共用檔案關聯。 當使用者變更檔案類型的預設應用程式時，新的預設應用程式的 ProgID 具有提供動詞和其他關聯資訊的優先順序。 此優先順序是因為它是關聯陣列中的第一個專案。 如果預設程式已變更，則無法再使用先前 ProgID 下的資訊。

若要主動處理變更為預設程式的結果，您可以使用 **HKEY \_ 類別 \_ 根** \\ **SystemFileAssociations** 來註冊動詞和其他關聯資訊。 因為它們在關聯陣列中的 ProgID 之後的位置，所以這些註冊的優先順序較低。 即使使用者變更預設程式，並提供位置來註冊將永遠可供特定檔案類型使用的次要動詞命令，這些 SystemFileAssociationsregistrations 仍是穩定的。 如需登錄範例，請參閱本主題稍後的 [註冊認知型](#registering-a-perceived-type) 別。

下列登錄範例顯示當使用者在主控台中執行 **預設程式** 專案時所發生的情況，以將 .mp3 檔案的預設值變更為 App2ProgID。 變更預設值之後，Verb1 就無法再使用，Verb2 會成為預設值。

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>註冊認知型別

已知類型的登錄值會定義為 **HKEY \_ 類別 \_ 根** SystemFileAssociations 登錄子機碼的子機碼 \\  。 例如，認知的型別 **文字** 會註冊如下：

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

在檔案類型的子機碼中包含 PerceivedType 值，即表示檔案類型的可感知類型。 PerceivedType 值會設定為在 **HKEY \_ 類別 \_ 根** SystemFileAssociations 登錄子機碼下註冊的認知型別名稱 \\  ，如先前的登錄範例所示。 例如，若要將 .cpp 檔案宣告為「文字」類型，請新增下列登錄專案：

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

