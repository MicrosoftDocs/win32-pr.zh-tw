---
title: 遊戲開發人員的使用者帳戶控制
description: 本文描述的指導方針和最佳作法，可讓遊戲開發人員有效地使用 Windows Vista 中引進 (UAC) 安全性功能的使用者帳戶控制。
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14013a99926301d93a9b7b710af30f33f85b4fa1a48a60a6979c8a6868474e09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396522"
---
# <a name="user-account-control-for-game-developers"></a>遊戲開發人員的使用者帳戶控制

本文描述的指導方針和最佳作法，可讓遊戲開發人員有效地使用 Windows Vista 中引進 (UAC) 安全性功能的使用者帳戶控制。

-   [使用者帳戶控制的總覽](#overview-of-user-account-control)
-   [Windows Vista 中的使用者帳戶](#user-accounts-in-windows-vista)
-   [以標準使用者的方式存取檔案](#file-access-as-a-standard-user)
-   [以標準使用者的形式登錄存取](#registry-access-as-a-standard-user)
-   [權限提高](#privilege-elevation)
-   [CreateProcess () 的 UAC 含意 ](#uac-implications-with-createprocess)
-   [在應用程式資訊清單中設定執行層級](#setting-the-execution-level-in-the-application-manifest)
-   [在 Visual Studio 中內嵌資訊清單](#embedding-a-manifest-in-visual-studio)
-   [UAC 與舊版遊戲的相容性](#uac-compatibility-with-older-games)
-   [舊版案例和資訊清單](#legacy-scenarios-and-manifests)
-   [結論](#conclusion)
-   [進一步閱讀](#further-reading)

## <a name="overview-of-user-account-control"></a>使用者帳戶控制的總覽

使用者帳戶控制 (UAC) （在 Windows Vista 中引進）是一項安全性功能，其設計目的是要協助防止惡意攻擊者使用廣泛使用的應用程式中發現的弱點或 bug，來改變作業系統或其他已安裝的程式。 只要以標準使用者的身分執行大部分的程式和程式， (也稱為受限使用者、受限的使用者或 Least-Privileged 使用者) ，即使目前使用者的帳戶具有系統管理認證，也可以達成這個目的。 具有標準使用者權限的進程具有許多固有的限制，可防止它進行全系統的變更。

UAC 也負責處理權限提高，方法是使用在執行特定進程（指定為需要系統管理許可權）時所起始的對話型驗證配置。 權限提高可讓系統管理員以安全的許可權層級執行大部分的應用程式 (與任何其他標準使用者) 相同，但也允許需要系統管理許可權的進程和作業。 UAC 支援過度的驗證，讓系統管理員可以在標準使用者目前登入系統時，將較高的許可權授與程式。

UAC 功能預設為啟用。 雖然系統管理員可以停用 UAC 全系統，但是這樣做會有一些負面的後果。 首先，這會削弱所有系統管理帳戶的安全性，因為所有程式都是以系統管理認證執行，即使大部分的應用程式實際上並不需要它們。 停用 UAC 之後，在安全性中公開可攻擊弱點的標準使用者應用程式，可能會被用來竊取私人資訊、安裝 rootkit 或間諜軟體、損毀系統完整性，或在其他系統上裝載廢止的攻擊。 在啟用 UAC 的情況下，以標準使用者的形式執行大部分的軟體，可大幅限制這類 bug 可能造成的損害。 其次，關閉 UAC 會停用應用程式相容性的許多因應措施，讓真正的標準使用者能夠成功地執行廣泛的應用程式。 永遠不應建議停用 UAC 作為相容性因應措施。

請務必注意，應用程式應該盡可能只使用標準使用者權限。 雖然系統管理員可以輕鬆地提升進程的許可權，但在每次執行需要系統管理認證的應用程式時，提高許可權仍需要使用者互動和通知。 這項提高許可權也必須在程式啟動時完成，因此即使是單一作業，也需要系統管理認證，才能讓系統在應用程式的整個執行時間暴露在更高的風險。 標準使用者若沒有提高其許可權的能力，在家庭和企業設定中也很常見。 「以系統管理員身分執行」不是很好的相容性因應措施，會使使用者和系統暴露于更高的安全性風險，並且在許多情況下為使用者帶來挫折。

> [!Note]  
> Windows 7 也有 Windows Vista 中引進的使用者帳戶控制功能。 雖然使用各種系統功能的使用者經驗已透過使用者帳戶控制獲得改良，但對應用程式的影響基本上是相同的。 本文中的所有 Windows Vista 建議也適用于 Windows 7。 如需 Windows 7 的 UAC UI 變更的詳細資訊，請參閱[消費者介面-使用者帳戶控制對話方塊更新](../win7appqual/user-interface---user-account-control-dialog-updates.md)。

 

## <a name="user-accounts-in-windows-vista"></a>Windows Vista 中的使用者帳戶

WindowsVista 會將每位使用者分類成兩種使用者帳戶類型：系統管理員和標準使用者。

標準使用者帳戶類似于 Windows XP 中的有限使用者帳戶。 如同在 Windows XP 中，標準使用者無法寫入 [Program Files] 資料夾，無法寫入登錄的 HKEY \_ 本機 \_ 電腦部分，也無法執行修改系統的工作，例如安裝核心模式驅動程式或存取系統層級進程空間。

在 Windows XP 發行之後，系統管理員帳戶已大幅變更。 之前，由 Administrators 群組成員啟動的所有進程都具有系統管理許可權。 在啟用 UAC 的情況下，所有進程都會以標準使用者權限執行，除非系統管理員特別提高許可權。 這項差異讓系統管理員群組中的帳戶更安全，方法是降低大部分程式中可能發生的錯誤所造成的安全性風險。

在以標準使用者進程的形式執行時，所有應用程式（尤其是遊戲）都必須以有效率且負責任的方式運作。 所有需要系統管理許可權的作業都應在安裝時完成，或是由明確要求系統管理認證的輔助程式進行。 雖然許可權提升對於系統管理員群組的成員而言相當簡單，但標準使用者必須延遲給具有系統管理認證的使用者，才能實際輸入其密碼以提升許可權。 由於受家長監護保護的帳戶必須是標準使用者，因此對於使用 Windows Vista 的玩家來說，這是很常見的情況。

如果您的遊戲已經在使用有限使用者帳戶的 Windows XP 上工作，則在 Windows Vista 上的「移至使用者帳戶控制」應該相當簡單。 大部分的這類應用程式都可以正常運作，但強烈建議新增應用程式資訊清單。 在 [應用程式資訊清單中設定執行層級](#setting-the-execution-level-in-the-application-manifest)的本主題稍後會描述 (資訊清單。 ) 

## <a name="file-access-as-a-standard-user"></a>以標準使用者的方式存取檔案

最受標準使用者限制影響的遊戲層面是檔案系統組織和協助工具。 您永遠不應該假設您的遊戲可將檔案寫入您的遊戲安裝所在的資料夾。 例如，在 Windows Vista 中，使用者必須先提高使用者的許可權，應用程式才能寫入 [Program Files] 資料夾。 若要避免這種情況，您應該依照範圍和協助工具將遊戲的資料檔案分類，並使用 [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)函式，以及 Windows shell 所提供的 CSIDL 常數，以產生適當的檔案路徑。 CSIDL 常數對應至檔案系統中作業系統所使用的已知資料夾，並升級以分割全域和使用者特定的檔案。

如果應用程式沒有系統管理許可權，嘗試在未授與寫入權限給進程的資料夾下建立或寫入檔案或目錄，將會在 Windows Vista 失敗。 如果您的32位遊戲可執行檔是在舊版模式中執行，因為它並未宣告要求的執行層級，其寫入作業將會成功，但會受限於虛擬化，如本文稍後的「與舊版遊戲的 UAC 相容性」一節中所述。

**[表 1]。已知的資料夾**



| CSIDL 名稱             |  (Windows Vista 的一般路徑)                                                    | 標準使用者權限 | 系統管理員權限 | 存取範圍 | 描述                                                                                                                      | 範例                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ 個人        | C： \\ 使用者 \\ 使用者名稱 \\ 檔                                                | 讀取/寫入           | 讀取/寫入           | Per-User     | 讀取和修改的使用者特定遊戲檔案，可在遊戲內容之外操作。                          | 螢幕擷取畫面。 以副檔名關聯儲存遊戲檔案。 |
| CSIDL \_ 本機 \_ APPDATA  | C： \\ Users \\ 使用者名稱 \\ AppData \\ Local                                           | 讀取/寫入           | 讀取/寫入           | Per-User     | 使用者專屬的遊戲檔案，這些檔案只會在遊戲內容中讀取和修改，且僅供使用。                                 | 遊戲快取檔案。 播放機設定。                          |
| CSIDL \_ 一般 \_ APPDATA | C： \\ ProgramData                                                                | 如果擁有者，則為讀取/寫入  | 讀取/寫入           | 所有使用者    | 可由使用者建立，並由所有使用者讀取的遊戲檔案。 只有 (擁有者) 的檔案建立者才會授與寫入權限。 | 使用者設定檔                                                     |
| CSIDL \_ PROGRAM \_ FILES  | C： \\ Program Files<br/> 或<br/> C： \\ Program Files (x86)  <br/> | 唯讀            | 讀取/寫入           | 所有使用者    | 由所有使用者讀取的遊戲安裝程式所撰寫的靜態遊戲檔案。                                                    | 遊戲資產，例如材質和網格。                        |



 

您的遊戲通常會安裝在 CSIDL \_ PROGRAM FILES 常數所代表之資料夾下的資料夾中 \_ 。 不過，並不是永遠如此。 當您將路徑字串產生到安裝資料夾下的檔案或目錄時，您應該改為使用可執行檔的相對路徑。

您也應該避免對已知資料夾路徑進行硬式編碼的假設。 例如，在 Windows XP Professional 64 位版和 Windows Vista x64 上，程式檔案路徑是 C： \\ program files (x86) （適用于32位程式）和 C： \\ program files （適用于64位程式）。 這些已知的路徑會從 Windows XP 變更，使用者可以重新設定許多這些資料夾的位置，甚至在不同的磁片磁碟機上找到它們。 因此，請一律使用 CSIDL 常數來避免混淆和潛在問題。 Windows安裝程式會瞭解這些已知的資料夾位置，並且會在從 Windows XP 升級作業系統時移動資料;相反地，使用非標準位置或硬式編碼路徑，在作業系統升級之後可能會失敗。

請注意，CSIDL \_ PERSONAL AND CSIDL \_ LOCAL APPDATA 所指定之使用者特定資料夾之間的微妙可用性差異應提供給您 \_ 。 \_如果需要使用者與檔案互動，例如按兩下以在工具或應用程式中開啟檔案，並針對其他檔案使用 CSIDL 本機 APPDATA，則選取要用於寫入檔案的 CSIDL 常數的建議做法是使用 CSIDL PERSONAL \_ \_ 。 您的應用程式可以利用這兩個資料夾來儲存和組織使用者專屬的資料檔案，因為它們的存取範圍或許可權等級沒有任何差異。 請小心建立唯一可與其他應用程式不衝突的路徑名稱，但要將完整路徑中的字元數減少到最大路徑的值 \_ 260。

下列程式碼提供如何將檔案寫入已知資料夾的範例：

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>以標準使用者的形式登錄存取

標準使用者的登錄存取權會受到與檔案系統類似的方式。 允許標準使用者讀取登錄中所有金鑰的許可權;但是，寫入權限只會授與給 HKEY 的 \_ 目前 \_ 使用者 (HKCU) 子樹，而此子樹會在內部對應到使用者特定的子機碼 HKEY \_ 使用者 \\ 的安全識別碼 (SID) 的使用者。 需要寫入至 HKEY 目前使用者以外之任何登錄位置的應用 \_ 程式 \_ 需要系統管理許可權。

如果32位應用程式未在其資訊清單中包含要求的執行層級，則所有對 HKEY \_ 本機 \_ 電腦 \\ 軟體的寫入都會進行虛擬化，而寫入至 HKEY 目前使用者以外的其他位置 \_ 將會 \_ 失敗。

不建議將持續性資料儲存在登錄中，例如使用者的設定。 從遊戲儲存持續性資料的慣用方法，是藉由呼叫 [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 並取得 CSIDL 常數的值（如前一節所述），將資料寫入檔案系統。

## <a name="privilege-elevation"></a>權限提高

在 Windows Vista 中，任何需要系統管理許可權的應用程式都必須在其資訊清單中宣告系統管理執行層級的要求 (如下一節所述，在[應用程式資訊清單中設定執行層級](#setting-the-execution-level-in-the-application-manifest)) 。

如果是「提高許可權」，則是由 UAC 驅動的程式，可將進程升階為系統管理進程。 進程的許可權只能在建立時提高許可權。 一旦建立之後，進程將永遠不會升級為較高的許可權層級。 基於這個理由。 需要系統管理認證的作業應該隔離到個別的安裝程式和其他輔助程式。

當程式執行時，UAC 會在資訊清單中檢查要求的執行層級，如果需要較高的許可權，則會以兩個標準對話方塊的其中一個來提示目前的使用者：一個是標準使用者，另一個則是系統管理員。

如果目前的使用者是標準使用者，UAC 會提示使用者提供系統管理員的認證，然後才允許程式執行。

**圖1。提示標準使用者輸入系統管理帳戶的認證**

![提示標準使用者輸入系統管理帳戶的認證](images/uac-prompt-elevation.jpg)

如果目前的使用者是系統管理員，UAC 會提示使用者提供許可權，然後才允許程式執行。

**[圖 2]提示系統管理員授權電腦的變更**

![提示系統管理員授權電腦的變更](images/uac-prompt-authorization.jpg)

只有當標準使用者提供適當的系統管理認證或系統管理使用者提供通知時，應用程式才會被授與系統管理許可權;任何其他會導致應用程式終止。

請務必注意，具有較高許可權的進程會以系統管理使用者身分，在 UAC 提示字元中輸入認證，而不是以目前登入的標準使用者身分執行。 這類似于 Windows XP 中的 **RunAs** ，提高許可權的進程會在存取每位使用者的資料時取得系統管理員的資料夾和登錄機碼，而且提高許可權的進程所啟動的所有程式也會同時繼承系統管理許可權和使用者帳戶的位置。 系統管理員若系統管理員收到通知 (**繼續** 或 **取消**) ，這些位置將符合目前使用者的位置。 不過，一般情況下，需要提高許可權的進程不應對每個使用者資料執行操作。 請注意，這可能會大幅影響安裝程式的運作方式！ 如果安裝程式是以系統管理員身分執行，會寫入 HKCU 或使用者的設定檔，可能會很可能寫入錯誤的位置。 在第一次執行遊戲時，請考慮建立這些每個使用者的值。

## <a name="uac-implications-with-createprocess"></a>CreateProcess () 的 UAC 含意

UAC 提高許可權機制不會從 Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) () 函式的呼叫中叫用，以啟動可執行檔，其設定為需要比目前進程更高的執行層級。 因此，對 **CreateProcess** () 的呼叫將會失敗，並出現 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) () 傳回 \_ 所需的錯誤提高許可權 \_ 。 **CreateProcess** () 只有在被呼叫端的執行層級等於或小於呼叫端的執行層級時，才會成功。 必須產生提高許可權的進程必須使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) () 函式來完成，這會導致 UAC 提高許可權機制透過 shell 來觸發。

## <a name="setting-the-execution-level-in-the-application-manifest"></a>在應用程式資訊清單中設定執行層級

您可以藉由將擴充功能新增至應用程式資訊清單，宣告您的遊戲要求的執行層級。 下列 XML 程式碼顯示為應用程式設定執行層級所需的最基本設定：

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

在上述程式碼中，作業系統會收到通知，表示遊戲只需要下列標記的標準使用者許可權：

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

藉由明確地將並無 requestedexecutionlevel 設定為 "asInvoker"，此範例會判斷提示作業系統，讓遊戲在沒有系統管理許可權的情況下正常運作。 因此，UAC 會停用虛擬化，並使用與啟動程式相同的許可權來執行遊戲，這通常是標準的使用者權限，因為 Windows 檔案總管會以標準使用者的身份執行。

您可以藉由將 "asInvoker" 取代為 "requireAdministrator" 來建立下列標記，以通知遊戲需要提高系統管理許可權的許可權：

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

使用此設定時，作業系統會在每次執行遊戲時，使用其中一個標準 UAC 提高許可權對話方塊來提示目前的使用者。 強烈建議您不要讓任何遊戲都需要系統管理員許可權來執行，因為此對話方塊不僅會迅速變得很討厭，也會讓遊戲與家長監護不相容。 將這項需求新增至任何可執行檔之前，請先仔細考慮。

常見的誤解是，將會將並無 requestedexecutionlevel 設定為 "requireAdministrator" 的資訊清單，會略過提高許可權提示的需求。 不正確。 它只會防止作業系統猜測您的設定或更新應用程式是否需要系統管理許可權。 系統仍然會提示使用者授權提高許可權。

Windows 會在顯示 UAC 提示之前，檢查標示為提高許可權之任何應用程式的簽章。 標示為提高許可權的大型可執行檔需要較小的可執行檔檢查，而且比標記為 "asInvoker" 的可執行檔長。 自動解壓縮的設定可執行檔應該標示為 "asInvoker"，而任何需要標示為 "requireAdministrator" 的部分，都應該放在另一個協助程式可執行檔中。

在上述範例中所示的 uiAccess 屬性，對於遊戲來說應該一律為 FALSE。 這個屬性會指定使用者介面自動化用戶端是否可存取受保護的系統 UI，如果設定為 TRUE，則會有特殊的安全性含意。

## <a name="embedding-a-manifest-in-visual-studio"></a>在 Visual Studio 中內嵌資訊清單

從 VS2005 開始，先將資訊清單支援新增至 Visual Studio。 根據預設，內建于 Visual Studio 2005 (或更新版本) 的可執行檔，會在建立過程中內嵌自動產生的資訊清單。 自動產生之資訊清單的內容取決於您在 [專案屬性] 對話方塊中指定的特定專案設定。

Visual Studio 2005 自動產生的資訊清單不會包含區塊，因為沒有 <trustInfo> 任何方法可以在專案屬性中設定 UAC 執行層級。 新增這項資訊的慣用方法是讓 VS2005 合併使用者定義的資訊清單，其中包含 <trustInfo> 具有自動產生之資訊清單的區塊。 只要將 \* 資訊清單檔加入至包含上一節所列之 XML 的方案，就可以做到這一點。 當 Visual Studio 在您的方案中遇到資訊清單檔時，它會自動叫用資訊清單工具 (mt.exe) 將資訊清單檔與自動產生的檔案合併。

> [!Note]  
> 資訊清單工具中有一個 bug (mt.exe Visual Studio 2005 所提供的) 會導致合併和內嵌的資訊清單，當可執行檔在 SP3 之前的 Windows XP 上執行時，可能會造成問題。 Bug 是工具在區塊宣告時如何重新定義預設命名空間的結果 <trustInfo> 。 幸運的是，只要明確地在區塊中宣告不同的命名空間 <trustInfo> ，並將子節點的範圍設定為新的命名空間，就可以輕鬆地完全略過此問題。 上一節所提供的 XML 會示範此修正。

 

使用 Visual Studio 2005 中包含的 mt.exe 工具有一點要注意的是，它會在處理區塊時產生警告， <trustInfo> 因為工具不包含更新的架構來驗證 XML。 若要修正此警告，建議您取代 Visual Studio 2005 安裝目錄下的所有 mt.exe 檔案 () 有多個實例與最新 mt.exe 中提供的 Windows SDK。

從 Visual Studio 2008 開始，您現在可以在 [專案屬性] 對話方塊中指定應用程式的執行層級 ([圖 3]) ，或使用/MANIFESTUAC 連結器旗標。 設定這些選項會導致 Visual Studio 2008 自動產生，並將具有適當區塊的資訊清單內嵌 <trustInfo> 至可執行檔。

**圖3。在 Visual Studio 2008 中設定執行層級**

![在 visual studio 2008 中設定執行層級](images/setting-execution-level-in-vs2008.jpg)

在不含資訊清單支援的舊版 Visual Studio 中內嵌資訊清單仍有可能，但開發人員需要更多工作。 如需如何進行這項操作的範例，請檢查2008年3月版本之前的 DirectX SDK 中任何範例所包含的 Visual Studio 2003 專案。

## <a name="uac-compatibility-with-older-games"></a>UAC 與舊版遊戲的相容性

如果您的遊戲似乎要儲存並成功將檔案載入至 Program Files 目錄，但 Windows Vista 沒有任何檔的辨識項，則在資訊清單中未包含要求之執行層級的任何32位應用程式都會被視為繼承應用程式。 在 Windows Vista 之前，大部分的應用程式通常是由具有系統管理許可權的使用者執行。 因此，這些應用程式可以自由地讀取和寫入系統檔案與登錄機碼，而且許多開發人員都不會進行必要的變更，以便在 Windows XP 上的有限使用者帳戶上正常運作。 不過，在 Windows Vista 中，這些相同的應用程式現在會因為新的安全性模型中的存取權限不足而失敗，這會強制執行繼承應用程式的標準使用者執行。 為了減輕這個問題的影響，Windows Vista 也加入了虛擬化。 虛擬化可讓數以千計的繼承應用程式在 Windows Vista 上正常運作，而不需要讓這些應用程式擁有較高的許可權，就能在幾次的次要作業中順利完成。 發現，您的遊戲很可能是在舊版模式下執行，而且受限於虛擬化。

虛擬化會將區分系統的寫入 (以及後續的檔案或登錄作業，) 到目前使用者設定檔內的每個使用者位置，藉此影響檔案系統和登錄。 例如，如果應用程式嘗試寫入至下列檔案：

<dl> C： \\ Program Files \\ 公司名稱 \\ 標題 \\config.ini  
</dl>

寫入會自動重新導向至：

<dl> C： \\ Users \\ 使用者名稱 \\ AppData \\ Local \\ VirtualStore \\ Program Files \\ Company name \\ Title \\config.ini  
</dl>

同樣地，如果應用程式嘗試寫入登錄值（如下所示）：

<dl> HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 公司名稱 \\ 標題  
</dl>

它會改為重新導向至：

<dl> HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ 類別 \\ VirtualStore \\ 電腦 \\ 軟體 \\ 公司名稱 \\ 標題  
</dl>

受虛擬化影響的檔案和登錄機碼，只會透過以目前使用者的形式執行之虛擬化應用程式的檔案和登錄操作來存取。

不過，虛擬化有許多限制。 其中一種情況是，64位應用程式永遠不會在舊版模式中執行，以便在32位應用程式中受到虛擬化的相容性作業，在64位中將會失敗。 此外，如果以標準使用者身分執行的繼承應用程式嘗試將任何類型的可執行檔寫入至需要系統管理認證的位置，則不會進行虛擬化，而且寫入將會失敗。

**[圖 4]虛擬化流程**

![虛擬化流程](images/uac-virtualization-process.jpg)

當繼承應用程式在檔案系統或登錄中的系統相關位置上嘗試進行讀取作業時，會先搜尋虛擬位置。 如果找不到檔案或登錄機碼，則作業系統會存取預設的系統位置。

虛擬化將會從後續版本的 Windows 中移除，因此重要的是不要依賴這項功能。 相反地，您應該明確設定標準使用者或系統管理許可權的應用程式資訊清單，因為這樣會停用虛擬化。 虛擬化對終端使用者也而言並不明顯，所以即使虛擬化可能會允許您的應用程式執行，它也可以產生支援呼叫，並使這些客戶難以進行疑難排解。

請注意，如果停用 UAC，則也會停用虛擬化。 如果已停用虛擬化，標準使用者帳戶的行為就像 Windows XP 中的有限使用者帳戶一樣，而且繼承應用程式可能無法正常運作，以因應虛擬化而成功的標準使用者。

## <a name="legacy-scenarios-and-manifests"></a>舊版案例和資訊清單

在大部分的使用案例中，只要使用正確的 UAC 資訊清單元素標示 .exe，並確保應用程式能正常運作，因為標準使用者就足以滿足絕佳的 UAC 相容性。 大部分的玩家都是在啟用使用者帳戶控制的情況下執行 Windows Vista 或 Windows 7。 針對 Windows XP 和已停用「使用者帳戶控制」功能的 Windows Vista 或最為理想使用者，這些使用者通常會使用系統管理員帳戶來執行。 雖然這是較不安全的作業模式，但一般不會遇到任何額外的相容性問題，不過如前文所述，停用 UAC 也會停用虛擬化。

當程式在 UAC 資訊清單中標示為「requireAdministrator」時，有一個特殊案例值得注意。 在 Windows XP 上，以及已停用使用者帳戶控制的 Windows Vista 或 Windows 7 上，系統會忽略 UAC 資訊清單元素。 在此情況下，具有系統管理員帳戶的使用者一律會以完整系統管理員許可權執行所有程式，因此這些程式會如預期般運作。 Windows不過，在 Windows Vista 或 Windows 7 上執行的 XP 受限使用者與標準使用者，一律會以限制的許可權執行這些程式，而且所有的系統管理員層級作業都會失敗。 因此，建議將程式標示為「requiretAdministrator」，並 [**在啟動時將**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) 其標示為「」，並在傳回 FALSE 時顯示嚴重的錯誤訊息。 在上述的大部分案例中，這一律會成功，但是在這種罕見的情況下，可提供更好的使用者體驗和明確的錯誤訊息。

## <a name="conclusion"></a>結論

作為以 Windows 多使用者環境為目標的遊戲開發人員，您必須設計您的遊戲以有效率且負責任地操作。 您遊戲的主要可執行檔不應該相依于系統管理許可權。 這不僅可防止每次執行遊戲時提示提高許可權，也會對整體使用者體驗造成負面影響，但也可讓您的遊戲利用其他需要以標準使用者權限執行的功能，例如家長監護。

如果應用程式的設計是以標準使用者的認證來運作， (或舊版 Windows 下的有限使用者) 則不會受 UAC 影響，不會受到權限提高。 不過，它們應該包含資訊清單，並將其要求的執行層級設定為 "asInvoker"，以符合 Vista 的應用程式標準。

## <a name="further-reading"></a>深入閱讀

如需針對符合使用者帳戶控制規範的 Windows vista 設計應用程式的協助，請下載下列白皮書： [Windows Vista 應用程式開發需求的使用者帳戶控制相容性](/previous-versions/dotnet/articles/bb530410(v=msdn.10))。

這份白皮書提供有關設計流程的詳細步驟，以及程式碼範例、需求和最佳作法。 這份檔也會詳細說明 Windows Vista 中使用者體驗的技術更新和變更。

如需有關使用者帳戶控制的詳細資訊，請造訪 Windows Vista： [Microsoft TechNet](https://www.microsoft.com/technet/)上的[使用者帳戶控制](https://www.microsoft.com/technet/windowsvista/security/uac.mspx)。

另一項實用的資源是教授您的應用程式在2007年1月的[MSDN 雜誌](/archive/msdn-magazine/msdn-magazine-issues)中，[與 Windows Vista 使用者帳戶控制完美地播放](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)的文章。 本文討論應用程式相容性的一般問題，以及在 Windows Vista 上使用 Windows Installer 套件的優點和問題。

如需有關錯誤的詳細資訊以及 mt.exe 的修正程式，Visual Studio 2005 用來自動將資訊清單合併並內嵌到可執行檔的工具，請參閱[MSDN](/archive/blogs/)上 Chris Jackson 的 blog[中的探索資訊清單第2部分： Windows Vista 中的預設命名空間和 UAC 指令](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/)清單。

 

