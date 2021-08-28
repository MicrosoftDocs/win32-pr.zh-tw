---
title: 使用 Least-Privileged 使用者帳戶的遊戲
description: 本文說明遊戲開發人員如何撰寫 Microsoft Windows 的遊戲，以搭配最低許可權的使用者帳戶 (，也稱為受限使用者帳戶) 。
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db15302eb856aaeb05c68fae4746110dd42cb4a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887390"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>使用 Least-Privileged 使用者帳戶的遊戲

本文說明遊戲開發人員如何撰寫 Microsoft Windows 的遊戲，以搭配最低許可權的使用者帳戶 (，也稱為受限使用者帳戶) 。

-   [簡介](#introduction)
-   [Least-Privileged 使用者帳戶的檔案存取](#file-access-for-least-privileged-user-accounts)
    -   [案例1：使用者不需要查看或變更的檔案](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [案例2：需要由使用者查看或變更的檔案](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Least-Privileged 使用者帳戶的登錄存取權](#registry-access-for-least-privileged-user-accounts)
-   [使用 Least-Privileged 使用者帳戶進行修補](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>簡介

Windows 使用帳戶管理其使用者。 現今，在家裡有超過80% 的電腦使用者與其他家庭成員共用電腦。 當多個使用者共用 Windows 的電腦時，會建立多個使用者帳戶，而每個使用者會以個別帳戶登入，以存取電腦。 有了安全性的增強功能，就能讓使用者以最低許可權的使用者帳戶操作電腦，也就是不具有系統完整控制權的有限使用者帳戶。 系統管理員帳戶通常不受限制地存取電腦的每個部分。 這可能會影響以 Windows 為基礎的遊戲如何運作。

針對撰寫遊戲的遊戲開發人員，有額外的權益可使用最低許可權的使用者帳戶。 在 Windows Vista 和更新版本中，系統會強制執行最低許可權的使用者帳戶，這表示系統上的每個帳戶（本機系統管理員除外）都是最低許可權的使用者帳戶。 這會影響不遵循指導方針 (繼承應用程式) 在 Windows Vista 和更新版本上執行的遊戲。 例如，當應用程式嘗試寫入至沒有許可權的資料夾或登錄值時，會將檔案寫入重新導向至使用者的虛擬檔案存放區。 此虛擬檔案存放區將位於使用者具有寫入權限的資料夾中。 這種行為看起來可能不像寫入嘗試失敗的情況，不過，建立虛擬檔案的應用程式可能會讓使用者混淆，因為檔案不會寫入至使用者預期的位置。 比方說，將高分數檔案寫入與可執行檔資料夾相同資料夾的遊戲，會改為將這些檔案寫入虛擬化資料夾。 因此，一位使用者無法看到由另一位使用者所達成的高分數，因為每位使用者都有個別的虛擬化檔案存放區。

遵循本文指導方針的遊戲將會以最低許可權的使用者帳戶執行，因此會維持與 Windows Vista 和更新版本的相容性。

## <a name="file-access-for-least-privileged-user-accounts"></a>Least-Privileged 使用者帳戶的檔案存取

Windows 支援兩種檔案系統： FAT32 和 NTFS。 FAT32 是僅為了回溯相容性所支援的舊版檔案系統;NTFS 支援功能強大且功能更強大的檔案許可權。 使用 ntfs 正在進行擴充，因為零售商正在將 Windows 預先安裝在 NTFS 磁碟分割的硬碟上的新電腦。 在 NTFS 型的 Windows XP 系統上，具有最低許可權使用者帳戶的使用者只會有數個資料夾的有限存取權。 不過，它們會在以 FAT32 為基礎的 Windows XP 系統上具有完整的存取權。

下表列出這些資料夾及其許可權的預設位置。



| 路徑                                               | 資料夾內容              | 讀取 | 寫入 | 建立/刪除 |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| &lt;磁片磁碟機 &gt; ： \\ Windows                            | Windows 作業系統 | X    |       |               |
| &lt;磁片磁碟機 &gt; ： \\ Program Files                      | 可執行檔應用程式檔 | X    |       |               |
| &lt;磁片磁碟機 &gt; ： \\ 檔和設定使用者 \\ 名稱\* | 每個使用者的檔案            | X    | X     | X             |
| &lt;磁片磁碟機 &gt; ： \\ 檔和設定 \\ 所有使用者  | 所有使用者檔案               | X    | X     | X             |



 

\* Username 是使用者的登入名稱。

在最低許可權的使用者帳戶中，您可以讀取、寫入、建立和刪除資料夾中的檔案： [檔] 和 [設定使用者名稱] 或 [檔]， \\ 並設定 \\ 所有使用者。

這表示，您不應該將 [儲存遊戲] 放置在 [ \\ Program Files] 中，改為移至我的檔的子資料夾中 \\ 。 此外，您不應該將暫存的應用程式資料放在 \\ 程式檔或 \\ 我的檔中，而是放置在 [應用程式資料] 資料夾中， (CSIDL \_ 本機 \_ APPDATA) 。

更具體來說，每個遊戲應該處理的案例有兩種：

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>案例1：使用者不需要查看或變更的檔案

典型的範例是遊戲的設定檔、暫存檔案和遊戲快取檔案。 這些檔案通常會保留在應用程式資料夾中。 若要取得此資料夾路徑，請[](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)使用 CSIDL \_ APPDATA 或 CSIDL LOCAL APPDATA 呼叫 SHGetFolderPath 函式， \_ \_ 如下列程式碼範例所示。

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

本機和漫遊應用程式資料檔案夾之間的差異在於，在 Windows 2000 和 Windows XP 上，在登入/登出過程中，漫遊內容會複製到伺服器，而本機內容則不會。 在大部分的遊戲中，本機應用程式資料就已足夠。

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>案例2：需要由使用者查看或變更的檔案

典型的範例是使用者儲存的遊戲檔案。 將檔案儲存在使用者的 [檔] 資料夾中，讓使用者可以輕鬆看見檔案。 應用程式會藉由呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 與 CSIDL PERSONAL 來取得使用者的檔資料夾路徑 \_ ，如下列程式碼範例所示：

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

有時候，遊戲可能需要儲存所有使用者要查看和使用的檔案。 其中一個範例是高分數記錄，其中所有使用者都會寫入相同的記錄檔，如此一來，就會為每位使用者維持全系統的高度分數，而不是個別的高度分數。 其他範例包括下載的地圖、任務和遊戲修改。 如果共用這些共用，則只有一位使用者必須下載它們，而不是每位使用者。 在此案例中，請使用 [共用設定檔] 資料夾底下的 [檔] 資料夾，如下列程式碼所示。

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Least-Privileged 使用者帳戶的登錄存取權

應用程式通常會使用 Windows 登錄來儲存資訊。 類似于檔案存取，系統管理員和最低許可權的使用者帳戶沒有登錄的相同許可權。 針對最低許可權的使用者帳戶，整個 HKEY \_ 本機 \_ 電腦節點是唯讀的。 例如，遊戲可以讀取預設的設定資訊，但可能不會將任何新資訊寫入此節點。 因此，以最低許可權的使用者模式執行的遊戲必須寫入登錄，才能使用 [HKEY 目前的使用者] \_ \_ 節點來儲存每個使用者的資訊，如下列程式碼所示。

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

值得注意的是，在安裝期間，應該將登錄資訊寫入 HKEY \_ 本機 \_ 電腦，而不是 HKEY \_ 目前的 \_ 使用者。 這是因為執行安裝的人員通常是系統管理員，而且可能不是使用程式的唯一人員。 在這種情況下，寫入 HKEY \_ 目前 \_ 的使用者會讓其他使用者無法使用該資訊。 這通常不是問題，因為在安裝期間寫入登錄的資訊是套用至程式每個使用者的設定和預設設定。

卸載遊戲時，必須進行額外的工作，才能移除遊戲已寫入登錄的每個值。 因為卸載程式是由一位人員（通常是系統管理員）執行，所以直接刪除 HKEY 本機電腦中的相關資訊， \_ \_ 而 HKEY \_ 目前的 \_ 使用者將不會移除其他使用者的值。 移除登錄中每個使用者資訊的其中一種方式，是列舉 HKEY \_ USERS 登錄 hive 根目錄。 HKEY USERS 下的每個子機碼都會 \_ 對應到 \_ \_ 系統上特定使用者的 HKEY 目前使用者 hive。 藉由列舉 HKEY \_ 使用者並移除每個子機碼下的遊戲特定資訊，卸載程式可以確保不會留下任何資訊。

## <a name="patching-with-least-privileged-user-accounts"></a>使用 Least-Privileged 使用者帳戶進行修補

修補遊戲牽涉到更新遊戲的檔案。 因此，它通常需要對遊戲的程式資料夾進行寫入存取。 修補遊戲是由系統管理員完成的簡單程式，因為他們對遊戲的程式資料夾有不受限制的存取權。 相反地，基於存取限制，通常很難在不可能的情況下，為最低許可權的使用者修補遊戲。 現在， [Windows Installer](/windows/desktop/Msi/windows-installer-portal)已增強，可讓最低許可權的使用者帳戶進行修補。 為了充分利用這項功能，我們鼓勵遊戲利用 Windows Installer 進行安裝和修補。

從 Windows Installer 3.0 開始，在符合特定條件時，應用程式修補程式可由最低許可權使用者套用。 這些條件包括：

-   應用程式是使用 Windows Installer 3.0 安裝的。
-   應用程式原本是依電腦安裝。
-   應用程式是從卸載式媒體（例如 CD-ROM 或數位攝影機）安裝 (DVD) 。
-   修補程式是由原始安裝程式套件所識別的憑證進行數位簽署， (.msi 檔) 。
-   修補程式可以針對數位簽章進行驗證。
-   原始安裝程式套件尚未停用最低許可權的使用者帳戶修補。
-   系統管理員未透過系統原則停用最低許可權的使用者帳戶修補。

一般來說，最低許可權的使用者無法修改遊戲的程式檔。 不過，當符合上述條件且已啟用 LUA 修補時，Windows Installer 可以更新遊戲的檔案，讓使用者取得最新的版本。

> [!Note]  
> 本文所包含的資訊與發行前版本的軟體產品相關，可能會在第一次商業發行之前大幅修改。 因此，在第一次正式發行時，資訊可能無法正確描述或反映軟體產品。 本文僅供參考之用，Microsoft 對於本文或其中包含的資訊不提供任何明示或默示的擔保。

 

 

 
