---
description: 本主題說明如何在 Windows 登錄中註冊程式，作為下列其中一種用戶端類型：瀏覽器、電子郵件、媒體播放、立即訊息或適用于 JAVA 的虛擬機器。
title: 使用用戶端類型註冊程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470416"
---
# <a name="registering-programs-with-client-types"></a>使用用戶端類型註冊程式

本主題說明如何在 Windows 登錄中註冊程式，作為下列其中一種用戶端類型：瀏覽器、電子郵件、媒體播放、立即訊息或適用于 JAVA 的虛擬機器。

> [!Note]  
> 這項資訊適用于下列作業系統：
> 
> -   Windows 2000 Service Pack 3 (SP3) 
> -   Windows 2000 Service Pack 4 (SP4) 
> -   WindowsXP Service Pack 1 (SP1) 
> -   WindowsXP Service Pack 2 (SP2) 
> -   WindowsXP Service Pack 3 (SP3) 
> -   Windows Server 2003
> -   Windows Vista
> -   WindowsVista Service Pack 1 (SP1) 
> -   Windows 8

 

本主題包含下列各節。

-   [所有用戶端類型的一般註冊元素](#common-registration-elements-for-all-client-types)
    -   [選取正式名稱](#selecting-a-canonical-name)
    -   [註冊程式的顯示名稱](#registering-a-programs-display-name)
    -   [註冊程式的圖示](#registering-a-programs-icon)
    -   [註冊開啟的動詞](#registering-an-open-verb)
    -   [註冊安裝資訊](#registering-installation-information)
-   [特定用戶端類型的註冊元素](#registration-elements-for-specific-client-types)
    -   [開始功能表註冊](#start-menu-registration)
    -   [郵件用戶端註冊](#mail-client-registration)
-   [完成範例註冊](#complete-sample-registrations)
    -   [範例瀏覽器](#a-sample-browser)
    -   [範例郵件瀏覽器](#a-sample-mail-browser)
    -   [範例媒體播放機](#a-sample-media-player)
    -   [範例即時 Messenger 程式](#a-sample-instant-messenger-program)
    -   [適用于 JAVA 的虛擬機器範例](#a-sample-virtual-machine-for-java)
-   [相關主題](#related-topics)

本主題會擴充現有的檔，將程式註冊為特定的用戶端類型。 如需該檔的連結，請參閱相關主題一節。

## <a name="common-registration-elements-for-all-client-types"></a>所有用戶端類型的一般註冊元素

將程式註冊為用戶端類型時，無論用戶端類型為何，大部分的登錄專案都相同。 不過，某些登錄專案是用戶端類型專屬的，而且這些專案會在 [ [特定用戶端類型的註冊元素](#registration-elements-for-specific-client-types) ] 區段中注明。

本節將討論下列主題：

-   [選取正式名稱](#selecting-a-canonical-name)
-   [註冊程式的顯示名稱](#registering-a-programs-display-name)
-   [註冊程式的圖示](#registering-a-programs-icon)
-   [註冊開啟的動詞](#registering-an-open-verb)
-   [註冊安裝資訊](#registering-installation-information)

> [!Note]  
> 在本主題中，以斜體指定的子機碼名稱是使用者定義子機碼名稱或一組可能值的預留位置。 [完整範例註冊](#complete-sample-registrations)一節中提供了完整的範例名稱範例。

 

所有用戶端類型註冊資訊都會儲存在下列子機碼底下：

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* 是下列其中一個子機碼名稱：

-   瀏覽器的 StartMenuInternet () 
-   電子郵件) 的郵件 (
-   媒體播放) 媒體 (
-   立即訊息) 的 IM (
-   適用于 JAVA) 的虛擬機器 JAVAVM (

在本主題中，您將會看到名為 "Litware Inc." 的虛構電腦程式的參考，其中包含名為 Litview.exe 的可執行檔。 這項假設性的程式是為了方便說明，可交換為立即 messenger、瀏覽器或其他類型的用戶端程式。

### <a name="selecting-a-canonical-name"></a>選取正式名稱

廠商必須選擇程式的 *標準名稱* 。 標準名稱永遠不會向使用者顯示，因此不需要當地語系化。 其唯一目的是提供可用來識別程式的唯一字串。 它通常會與程式的英文名稱相同，但這只是一種慣例。

針對瀏覽器以外的用戶端類型，標準名稱可以是任何字串。 選擇一個不太可能由另一個廠商使用的唯一名稱。

針對瀏覽器用戶端，正式名稱必須是相關聯可執行檔的名稱（包括副檔名）;例如，"Litview.exe"。

以下是標準名稱的一些範例。

-   Iexplore.exe (瀏覽器) 
-   Windows郵件 (電子郵件) 
-   Windows Media Player (媒體) 
-   WindowsMessenger (立即訊息) 

建立子機碼以註冊正式名稱，如下所示。 子機碼的名稱是標準名稱。 與該程式註冊相關的所有資訊都會存在於此子機碼底下。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>註冊程式的顯示名稱

註冊的下一步是指定程式的顯示名稱。 它會以標準名稱索引鍵的形式提供值，如下所示。 請再次注意， *CanonicalName* 和 *ClientTypeName* 不是索引鍵的實際名稱，而是只有真正名稱的預留位置，例如 *亮視圖*。

> [!Note]  
> 從 Windows 8，用來註冊[設定程式存取和電腦預設值的名稱 (SPAD) ](cpl-setprogramaccess.md)和[預設程式](default-programs.md)應該相符，才能讓 SPAD 變更觸發預設程式註冊。

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

**>Localizedstring** 值是 REG \_ SZ 字串，其中包含 "at" 符號 ( @ ) 、.dll 或 .exe 檔案的完整路徑、逗號、減號和十進位整數。 十進位整數是字串資源的識別碼（包含在 .dll 或 .exe 檔案中），其值會以此用戶端的名稱顯示給使用者。 請注意，即使檔案路徑包含空格，也不需要加上引號。

以這種方式註冊顯示名稱字串，可讓相同的註冊用於多種語言。 每個語言安裝都會提供不同的資源檔，並以相同的資源識別碼儲存顯示名稱。

下列範例顯示虛構的「立即查看」立即訊息程式的註冊。 因為這是立即訊息程式，所以在此案例中， *CanonicalName* 子機碼 (在 **IM** 子機 *碼下)* 。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

請注意，使用 (預設) 專案做為用戶端顯示名稱的次要宣告。 如果 **>localizedstring** 不存在，則會改用 (預設) 值。 這適用于所有用戶端類型 (的網際網路瀏覽器、電子郵件瀏覽器、即時 messengers 和媒體播放機) 。 為了與 [Internet Explorer 用戶端](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))登錄配置相容，電子郵件程式應將 *CanonicalName* 子機碼 (預設) 值設定為目前安裝之語言的用戶端顯示名稱。

### <a name="registering-a-programs-icon"></a>註冊程式的圖示

> [!Note]  
> 本節不適用於 Windows 2000。

 

依預設，Windows XP 和 Windows Vista [**開始**] 功能表的上方區段包含 **網際網路** 和 **電子郵件** 圖示。 Windows 7 和更新版本中不會有這些圖示。 針對瀏覽器和電子郵件客戶程式，將程式指派為其用戶端類型的預設值時，會針對這些 [ **開始** ] 功能表項目顯示該程式的註冊圖示。

瀏覽器和電子郵件客戶程式都必須註冊程式的圖示。 註冊適用于 JAVA 用戶端類型的媒體播放、立即訊息或虛擬機器的圖示是選擇性的，而這些用戶端類型的註冊圖示目前未由 Windows 使用，且不會顯示在 Windows XP 或 Windows Vista [**開始**] 功能表的上半部區段中。

若要註冊用戶端程式的圖示，請新增具有預設值的 **DefaultIcon** 子機碼，如下所示。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

**FilePath** 值是包含圖示之檔案的完整路徑。 即使此路徑包含空格，也不需要引號。

**>Iconindex** 值的解釋如下：

-   如果 **>iconindex** 是正數，則會使用數位作為儲存在檔案中之以 *零為基* 底之圖示陣列的索引。 例如，如果 **>iconindex** 是1，則會從檔案載入第二個圖示。
-   如果 **>iconindex** 為負數，則會使用 **>iconindex** 的絕對值作為資源識別碼 (而不是圖示的索引) 。 例如，如果 **>iconindex** 為-3，則會從檔案載入其資源識別碼為3的圖示。

下列範例示範如何註冊假設性的視圖瀏覽器。 Litview.exe 檔案中儲存的第二個圖示會用來做為預設值。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>註冊開啟的動詞

> [!Note]  
> 本節不適用於 Windows 2000。 下列步驟僅適用于瀏覽器和電子郵件客戶程式。

 

假設使用者已選取您的程式做為預設網際網路或電子郵件程式。 該使用者在 Windows XP 或 Windows Vista [**開始**] 功能表中按一下 [**網際網路**] 或 [**電子郵件**] 圖示，以開啟程式。 此時會執行已註冊的命令列，如下所示。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

命令列必須指定檔案的完整絕對路徑，後面接著選擇性的命令列選項。 如果專案類型是 REG \_ EXPAND \_ SZ，則環境變數可以在路徑中使用。 適當地使用引號，以確保命令列中的空格不會誤解。 命令列應該以適當的預設值執行程式。 瀏覽器通常預設為使用者的首頁。 電子郵件程式通常會開啟使用者的 **收件** 匣。

下列範例會示範如何註冊 `open` 假想亮 View 瀏覽器的動詞。 它不會指定任何命令列選項。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

請注意，在此值中，引號是放在路徑周圍，因為它包含內嵌的空格。 省略這些引號可能會導致命令列被誤解。

### <a name="registering-installation-information"></a>註冊安裝資訊

> [!Note]  
> 本節不適用於 Windows Server 2003。

 

-   [重新安裝命令](#the-reinstall-command)
-   [隱藏圖示命令](#the-hide-icons-command)
-   [顯示圖示命令](#the-show-icons-command)
-   [組程式設定](#group-program-configuration)
-   [瀏覽器註冊範例](#browser-registration-example)

使用者選取個別電腦預設程式的功能，如下表所示進行命名和存取。  (Windows Vista 引進了一項新功能，請 **設定您的預設程式，讓** 使用者可以設定每位使用者的預設值。 ) 




| 作業系統 | 標題 | 存取位置 | 
|------------------|-------|-----------------|
| Windows 7 | 設定程式存取和電腦預設值 | <ul><li><strong>開始</strong> 功能表 <strong>預設程式</strong> 選項</li><li><strong>預設程式</strong> 主控台專案</li></ul> | 
| Windows Vista | 設定程式存取和電腦預設值 | <ul><li><strong>開始</strong> 功能表 <strong>預設程式</strong> 選項</li><li><strong>預設程式</strong> 主控台專案</li></ul> | 
| Windows XP SP2 | 設定程式存取和預設值 | <ul><li><strong>開始</strong> 功能表</li><li><strong>新增或移除程式</strong> 主控台專案</li></ul> | 
| Windows XP SP1 | 設定程式 | <ul><li><strong>新增或移除程式</strong> 主控台專案</li></ul> | 




 

為了簡單起見，本主題使用功能的 Windows 7 標題。 所有版本的功能也就一般稱為 SPAD。

> [!Note]  
> 如果您正在執行 Windows 2000 或 Windows xp，則必須至少安裝 Windows 2000 SP3 或 Windows XP SP1，才能看到 [**設定程式存取和預設值**] 頁面。 在 Windows Vista 和更新版本中，存取 [**設定程式存取和電腦預設值**] 頁面需要系統管理員許可權。 基於這個理由，我們鼓勵開發人員註冊您的 [預設程式](default-programs.md) 主控台專案，讓任何使用者都能管理應用程式預設值。

 

下列登錄樹狀目錄顯示必須在程式的 **InstallInfo** 機碼中註冊的各種資訊，程式才會出現在 [ **設定程式存取和電腦預設值** ] 頁面上，以作為其用戶端類型的選項。 下列各節將詳細討論這些值。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

命令列必須指定檔案的完整絕對路徑，後面接著選擇性的命令列選項。 適當地使用引號，以確保命令列中的空格不會誤解。

### <a name="the-reinstall-command"></a>重新安裝命令

當使用者使用 [ **設定程式存取和電腦預設值** ] 頁面來選取您的程式做為其用戶端類型的預設值時，會執行 ReinstallCommand 值中宣告的重新安裝命令列。 在 Windows Vista 和更新版本中，存取此頁面需要系統管理員許可權層級。 在 Windows 8 中，如果您已針對 [**設定程式存取] 和 [電腦預設值**] 和 [**預設程式**] 使用相同的名稱來註冊應用程式，則會對目前的使用者套用該應用程式的 **預設程式** 中指定的預設值，以及執行重新安裝命令。

重新安裝命令列所啟動的程式必須將應用程式與應用程式可處理[的一組完整檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型產生關聯。 所有應用程式都必須在重新安裝命令中建立處理常式功能。 應用程式可以使用重新安裝命令來註冊功能，並選擇性地建立預設狀態。 當應用程式選擇在重新安裝命令中同時執行功能和預設處理常式狀態時，它也應該恢復任何所需的可見連結或快捷方式。 大部分應用程式選擇的可見進入點會列在 [隱藏圖示命令](#the-hide-icons-command)中。

> [!Note]  
> 強烈建議應用程式在重新安裝命令中執行處理功能。

 

重新安裝程式完成後，重新安裝命令列所啟動的程式應該會結束。 它不應該啟動對應的程式;它應該只會註冊預設值。 例如，瀏覽器的重新安裝命令不應開啟使用者的首頁。

> [!Note]  
> 針對 Windows XP 和 Windows Vista 中的瀏覽器和電子郵件客戶程式，在重新安裝命令中選擇建立處理功能和預設狀態的應用程式，應該在 [開始] 功能表頂端註冊對應的圖示。 如需其他資訊，請參閱 [開始功能表註冊](#start-menu-registration) 。

 

### <a name="the-hide-icons-command"></a>隱藏圖示命令

當使用者在 [**設定程式存取和電腦預設值**] 頁面中清除 [**啟用對這個程式的存取**] 方塊時，會執行在 HideIconsCommand 值中宣告的命令列。 此命令列必須隱藏在使用者介面中顯示的所有程式存取點。 特定的指導方針是移除下列位置的快捷方式和圖示：

-   桌面圖示
-   [開始] 功能表連結，包括 **Startup** 群組
-   快速啟動 bar 連結
-   [通知] 區域
-   快顯功能表
-   資料夾工作區

此命令列也必須防止自動叫用程式，例如 **執行** 登錄機碼中指定的程式。 建議廠商在應用程式的隱藏存取回呼中實施這些指導方針。

隱藏圖示時，您不需要放棄註冊 (應用程式功能) 檔案類型。 您也不需要為檔案和通訊協定類型放棄應用程式的預設狀態。 當 UI 中遇到這些類型時，這樣做可能會導致不良的使用者體驗。

成功隱藏圖示之後，您必須將 IconsVisible 登錄值更新為0，如下所示：

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

IconsVisible 專案的類型為 **REG \_ DWORD**。

### <a name="an-alternate-hide-icons-method-in-spad"></a>SPAD 中的替代隱藏圖示方法

針對某些繼承應用程式，隱藏存取的完整執行可能不實用。 另一種可達到相同效果的方法是卸載應用程式。 下一節顯示範例行為和範例程式碼來執行此替代方案。 一般而言，獨立軟體廠商 (Isv) 應避免此替代方案，因為它將會：

-   從系統完全卸載應用程式。
-   移除先前選取的預設值。
-   不要讓 UI 選項重新安裝應用程式。
-   讓 [啟用存取] 功能不再可用，因為卸載會從 SPAD 完全移除應用程式。

建議的使用者體驗如下所示：

-   當使用者在 SPAD 中取消核取 [ **啟用此程式存取** ] 方塊時，會顯示下列 UI。

    ![關於隱藏程式存取權的對話方塊](images/hideaccessvista.png)

-   當使用者選取 **[確定]** 時，主控台專案的 [ **程式和功能** ] 隨即啟動，讓使用者可以卸載應用程式。
-   WindowsXP 使用者應該會看到此對話方塊。

    ![對等的 windows xp 對話方塊](images/hideaccessxp.png)

-   當 Windows XP 使用者選取 **[確定]** 時，會啟動 [**新增或移除程式**] 主控台專案，讓使用者可以卸載應用程式。

下列程式碼會為隱藏存取功能提供可重複使用的執行方式，如上面所述。 它可用於 Windows XP、Windows Vista 和 Windows 7。


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>顯示圖示命令

當使用者在 [**設定程式存取和電腦預設值**] 頁面中檢查 [**啟用存取此程式**] 方塊時，會執行在 ShowIconsCommand 專案中宣告的命令列。 此命令列可還原程式的存取點，包括 [ **開始** ] 功能表、桌面上和 [ **啟動** ] 群組中的存取點，以及一般自動叫用，例如在 [ **執行** ] 登錄機碼中指定的存取點。 對大部分應用程式感興趣的可見存取點會列在 [隱藏圖示命令](#the-hide-icons-command)中。 應用程式不應變更每個使用者預設值;這項變更應該由使用者透過 **預設程式** 來完成。

成功顯示圖示之後，您必須將 IconsVisible 登錄值更新為1，如下所示：

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

請注意，如果您已使用 HideIconsCommand 專案提示卸載應用程式，ShowIconsCommand 專案就不會使用。 它應該從登錄中移除，並在卸載過程中移除其餘的應用程式資訊。

### <a name="group-program-configuration"></a>組程式設定

> [!Note]  
> 本節不適用於 Windows 2000。

 

在系統準備過程中，OEM 可以建立針對 JAVA 用戶端程式隱藏 Microsoft 瀏覽器、電子郵件、媒體播放、立即訊息或虛擬機器存取點的設定，並指定自己的預設程式。 Oem 可以設定下列登錄值，讓使用者隨時都能將電腦重設為此預設設定。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

如果設定這些金鑰，使用者就可以在 [**設定程式存取和電腦預設值**] 頁面上，選取 [**電腦製造商**] 選項來還原 OEM 設定。 如果未設定這些金鑰，則不會顯示 [ **電腦製造商** ] 選項。

**OEMShowIcons** 專案（如果有的話）會設定指定用戶端的圖示顯示狀態（如果使用者選取 **電腦製造商** 的話）。 值為1會顯示圖示，值為0則不會顯示圖示。 如果 **OEMShowIcons** 不存在，則選取 [ **電腦製造商** ] 並不會影響圖示顯示設定。 **OEMShowIcons** 的類型為 **REG \_ DWORD**。

如果出現並設定為1， **OEMDefault** 專案就會建立指定之型別的預設用戶端的 OEM 喜好設定。 只有一個特定類型的用戶端可以標記為 OEM 預設值。 如果有多個用戶端的註冊包含 **OEMDefault** 專案，則會忽略所有專案，而且目前的用戶端會繼續作為預設用戶端使用。 如果 **OEMDefault** 專案不存在或存在，而且設定為0，則在使用者選取 **電腦製造商** 時，不會將該特定用戶端當做預設用戶端使用。 **OEMDefault** 的類型為 **REG \_ DWORD**。

除了將電腦重設為 OEM 所建立之預設設定的選項之外，使用者還有其他三個設定選項：

-   將電腦設定為 Microsoft Windows 設定。 在此情況下，[ **設定程式存取和電腦預設值** ] 頁面可讓您存取在相關產品類別中註冊之電腦上的所有 microsoft 和非 microsoft 軟體。 系統會將 Microsoft Windows 程式選取為每個類別的預設選項。
-   將其電腦設定為非 Microsoft 設定。 此設定會隱藏存取點 (例如 [**開始**] 功能表) ，以 Windows Internet Explorer、Windows Media Player、Windows Messenger 和 Microsoft Outlook Express。 它可讓您存取電腦上的非 Microsoft 軟體。 此外，如果類別中有非 Microsoft 程式，則會設定為該類別的預設值。 如果類別中有一個以上的非 Microsoft 程式，系統會要求使用者選擇應使用哪一個非 Microsoft 程式做為預設。
-   建立自訂設定。 使用者可以自行選擇是否要啟用或移除存取權，並在適當的情況下混用 Microsoft 與非 Microsoft 程式。 使用者會依類別目錄來建立預設選項。

使用者隨時都可以隨時變更這些選項。

### <a name="browser-registration-example"></a>瀏覽器註冊範例

下列範例顯示虛構亮 View 瀏覽器的完整 **InstallInfo** 註冊。 在此情況下，命令列參數可讓 Litview.exe 檔案執行每個值所需的任何動作。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

請注意，引號是放在路徑周圍，因為它們包含內嵌的空格。

## <a name="registration-elements-for-specific-client-types"></a>特定用戶端類型的註冊元素

您也可以在本主題結尾的相關主題一節所列的資源中找到下列資訊。

-   [開始功能表註冊](#start-menu-registration)
-   [郵件用戶端註冊](#mail-client-registration)

### <a name="start-menu-registration"></a>開始功能表註冊

在 Windows XP 中，應用程式通常會在全電腦 (**HKEY \_ 本機 \_ 電腦** 上註冊預設值，) 而不是使用者 (**HKEY \_ 目前 \_ 使用者**) 範圍。 有了 Windows Vista 的使用者帳戶控制 (UAC) ，在 [**開始**] 功能表中宣告 **網際網路** 和 **電子郵件** 位置的應用程式，必須在正確的執行內容中執行重新安裝命令。

> [!Note]  
> 從 Windows 7 起，已移除 [開始] 功能表的 **電子郵件** 連結。 不過，本節所討論的註冊仍應執行，因為它會指派預設的 MAPI 用戶端。

 

Windows XP、Windows Vista 或 Windows 7 的受限使用者無法存取 SPAD。 基於這個理由，我們鼓勵開發人員註冊您的 **預設程式** 主控台專案，讓任何使用者都可以管理每個使用者的應用程式預設值。

在 SPAD 中所做的選擇只會影響個別電腦的設定。

設定登錄值，如下所示。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **下列資訊僅適用于 Windows XP。**
> 
> 如果在 HKEY 本機電腦下註冊電腦層級的預設值 \_ \_ （如上所示），則應用程式應該刪除下列子機碼底下指派給預設專案的值：
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> 如果在 HKEY 本機電腦下註冊電腦層級的預設值（如上 \_ \_ 所示）失敗，通常是因為使用者沒有子機碼的寫入權限，應用程式應該設定下列值：
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> 這只會為目前的使用者註冊標準名稱，而不會為所有使用者註冊。

 

更新登錄機碼之後，程式應該使用 **wParam** = 0 廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md)訊息，並將 **lParam** 指向以 null 終止的字串 "Software \\ Clients \\ **ClientTypeName**"，以通知作業系統預設用戶端已變更。

### <a name="mail-client-registration"></a>郵件用戶端註冊

若為郵件用戶端，程式必須在 **HKEY \_ 類別的 \_ 根** mailto 金鑰下註冊設定，才能 \\ 服務使用此通訊協定的 url `mailto` 。 設定可在下列機碼底下鏡像這些設定的值和索引鍵。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

此登錄階層會取代 `mailto` 在 **HKEY \_ 類別 \_ 根目錄** \\ **mailto** 找到的現有登錄階層。 階層保持不變，只有位置已變更。 此階層的格式記載于 MSDN 上的 [非同步插即用通訊協定總覽和教學](/previous-versions//aa767913(v=vs.85))課程。 一般來說， `mailto` 通訊協定會註冊到程式，而不是非同步通訊協定，在這種情況下，會套用將 [應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) 的檔。

下列範例會顯示註冊 `mailto` `mailto` 至程式之處理常式的註冊區段。

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

EditFlags 登錄值記錄在標題為「定義檔案類型屬性」一節的 [檔案類型](fa-file-types.md) 中。

## <a name="complete-sample-registrations"></a>完成範例註冊

下列範例是為了顯示各種用戶端類型的完整註冊需求而提供。

-   [範例瀏覽器](#a-sample-browser)
-   [範例郵件瀏覽器](#a-sample-mail-browser)
-   [範例媒體播放機](#a-sample-media-player)
-   [範例即時 Messenger 程式](#a-sample-instant-messenger-program)
-   [適用于 JAVA 的虛擬機器範例](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>範例瀏覽器

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>範例郵件瀏覽器

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>範例媒體播放機

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>範例即時 Messenger 程式

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>適用于 JAVA 的虛擬機器範例

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*此處所描述的範例公司、組織、產品、功能變數名稱、電子郵件地址、標誌、人員、地點及事件均屬虛構。任何真實的公司、組織、產品、功能變數名稱、電子郵件地址、標誌、人員、地點或事件，都不會有任何關聯。*

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預設程式](default-programs.md)
</dt> <dt>

[如何使用 Windows 開始功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)
</dt> <dt>

[Internet Explorer 用戶端登錄配置 (請參閱「用戶端登錄機碼定義」一節) ](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[非同步插即用通訊協定的總覽和教學課程](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
