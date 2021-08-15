---
description: 使用預設程式來設定預設的使用者體驗。
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: 預設程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861355"
---
# <a name="default-programs"></a>預設程式

使用 **預設程式** 來設定預設的使用者體驗。 使用者可以從主控台或直接從 [**開始**] 功能表存取 **預設程式**。 [設定程式存取和電腦預設值 (SPAD)](cpl-setprogramaccess.md)工具（Windows XP 中的使用者主要預設體驗）現在是 **預設程式** 的一部分。

> [!IMPORTANT]
> 本主題不適用於 Windows 10。 預設檔案關聯在 Windows 10 中的運作方式有所變更。 如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。

 

當使用者使用 **預設程式** 設定程式預設值時，預設設定只會套用至該使用者，而不會套用到其他可能使用相同電腦的使用者。 **預設程式** 提供一組 (在 Windows 8) 中淘汰的 api，可讓獨立軟體廠商 (isv) 在預設系統中包含其程式或應用程式。 API 集也可協助 Isv 將其狀態更妥善地管理為預設值。

本主題的組織方式如下：

-   [預設程式及其相關的 API 集合簡介](#introduction-to-default-programs-and-its-related-api-set)
-   [註冊應用程式以搭配預設程式使用](#registering-an-application-for-use-with-default-programs)
    -   [Progid](#progids)
    -   [註冊子機碼和值描述](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [完整註冊範例](#full-registration-example)
-   [成為預設瀏覽器](#becoming-the-default-browser)
-   [預設程式 UI](#default-programs-ui)
-   [使用預設程式的最佳作法](#best-practices-for-using-default-programs)
    -   [在安裝期間](#during-installation)
    -   [安裝後](#after-installation)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>預設程式及其相關的 API 集合簡介

**預設程式** 主要是針對使用標準檔案類型的應用程式所設計，例如 .mp3 或 .jpg 檔案或標準通訊協定，例如 HTTP 或 mailto。 使用專屬通訊協定和檔案關聯的應用程式通常不會使用 **預設的程式** 功能。

針對 **預設程式** 功能註冊應用程式之後，您可以使用 API 集來使用下列選項和功能：

-   還原應用程式的所有已註冊的預設值。 Windows 8 已淘汰。
-   為應用程式還原單一已註冊的預設值。 Windows 8 已淘汰。
-   在單一呼叫中查詢特定預設值的擁有者，而不是搜尋登錄。 您可以查詢檔案關聯、通訊協定或 [ **開始** ] 功能表標準動詞命令的預設值。
-   針對特定應用程式啟動 UI，讓使用者可以在其中設定個別的預設值。
-   移除所有的每個使用者關聯。

**預設程式** 也提供 UI，可讓您註冊應用程式，以便為使用者提供其他資訊。 例如，數位簽署的應用程式可以包含製造商首頁的 URL。

使用相關聯的 API 集可協助應用程式在 Windows Vista 中引進 (UAC) 功能的使用者帳戶控制下正確運作。 在 UAC 下，系統管理員會以標準使用者的身分顯示系統，讓系統管理員通常無法寫入 **HKEY \_ 本機 \_ 電腦** 子樹。 這項限制是一種安全性功能，可防止進程成為系統管理員，而不需要系統管理員的知識。

使用者安裝程式通常是以提高許可權的進程執行。 不過，應用程式在安裝後於電腦層級修改預設關聯線為的嘗試會失敗。 相反地，預設值必須在每個使用者層級上註冊，如此可防止多個使用者覆寫彼此的預設值。

檔案和通訊協定關聯的階層式登錄結構，優先于電腦層級預設值的每個使用者預設值。 有些應用程式在其程式碼中包含的點，會在宣告 **HKEY \_ 本機 \_ 電腦** 中註冊的預設值時，暫時提升其許可權。 如果另一個應用程式已經註冊為每個使用者的預設值，則這些應用程式可能會遇到非預期的結果。 使用 **預設程式** 可避免這種混淆，並保證每個使用者層級的預期結果。

## <a name="registering-an-application-for-use-with-default-programs"></a>註冊應用程式以搭配預設程式使用

本節說明使用 **預設程式** 註冊應用程式所需的登錄子機碼和值。 其中包含完整的範例。

本節包含下列主題：

-   [Progid](#progids)
-   [註冊子機碼和值描述](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [完整註冊範例](#full-registration-example)

**預設程式** 會要求每個應用程式明確註冊檔案關聯、MIME 關聯，以及應將應用程式列為可能預設值的通訊協定。 您可以使用下列登錄專案來註冊關聯，稍後在本主題的註冊子機碼 [和值描述](#registration-subkey-and-value-descriptions)下會詳細說明：

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

下列範例會顯示虛構 Contoso 瀏覽器的登錄專案，稱為 WebBrowser：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>Progid

應用程式必須提供特定的 [ProgID](fa-progids.md)。 請務必包含通常寫入延伸模組之一般預設子機碼中的所有資訊。 例如，虛構的 Litware media player 會提供應用程式特定的 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **LitwarePlayer11.AssocFile.MP3** 子機碼。 該子機碼包含一般預設子 **機碼 HKEY \_ 本機 \_ 電腦** 軟體類別中的所有資訊 \\  \\  \\ **.mp3** 以及您想要應用程式註冊的任何其他資訊。 如此可確保當使用者將 .mp3 關聯還原至 Litware 播放程式時，Litware 播放程式的資訊不會完整，也不會被另一個應用程式覆寫。 如果預設子機碼是該資訊的唯一來源，則可能會發生 (覆寫。 ) 

當您將 ProgID 對應至副檔名或通訊協定時，應用程式可以對應到一或多個。 在 Contoso 範例中，ContosoHTML 會指向提供 .htm、.html、>.shtml、xht 和 xhtml 副檔名之 shellexecute 資訊的單一 ProgID。 因為每個通訊協定都有不同的 ProgID，所以當您使用通訊協定時，您可以讓每個通訊協定都有自己的執行字串。

當您的 MIME 類型可以內嵌在瀏覽器中時，MIME 型別的 ProgID 必須包含 **clsid** 子機碼，以使用對應應用程式 (clsid) 的類別識別碼。 此 clsid 用於查閱 mime 資料庫中儲存于 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **mime** \\ **資料庫** \\ **內容類型** 的 CLSID。 如果您的 MIME 類型不是要在瀏覽器中以內嵌方式來流覽，則可以省略此步驟。

### <a name="registration-subkey-and-value-descriptions"></a>註冊子機碼和值描述

本節說明使用 **預設程式** 來註冊應用程式時所使用的個別登錄子機碼和值，如先前所述。

### <a name="capabilities"></a>功能

[ **功能** ] 子機碼包含特定應用程式的所有 **預設程式** 資訊。 預留位置% ApplicationCapabilityPath% 指的是從 **HKEY \_ 目前 \_ 使用者** 或 **HKEY \_ 本機 \_ 電腦** 到應用程式 **功能** 子機碼的登錄路徑。 此子機碼包含下表所示的重要值。



| 值                  | 類型                       | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ sz 或 reg \_ EXPAND \_ SZ | **必要**。 若要讓使用者能夠做出明智的預設指派選項，應用程式必須提供描述應用程式功能的字串。 雖然先前的 Contoso 範例會將描述直接指派給 ApplicationDescription 值，但應用程式通常會提供描述做為內嵌于 .dll 檔案中的資源，以協助進行當地語系化。 如果未提供 ApplicationDescription，則應用程式不會出現在可能的預設程式的 UI 清單中。                                                            |
| ApplicationName        | REG \_ sz 或 reg \_ EXPAND \_ SZ | **選擇性。** 程式在 [預設程式] UI 中出現的名稱。 如果應用程式未提供此資料，則會在 UI 中使用與應用程式的第一個已註冊 ProgID 相關聯之可執行程式的名稱。 ApplicationName 必須一律符合在 [RegisteredApplications](#registeredapplications)中註冊的名稱。 如果您想要不同的應用程式類型（例如瀏覽器和電子郵件客戶程式）指向相同的可執行檔，但其顯示為不同的名稱，您可以使用 ApplicationName。<br/> |
| Hidden                 | REG \_ DWORD                 | **選擇性。** 將此值設定為1，以在 [ **設定您的預設程式** ] 對話方塊中的程式清單中隱藏應用程式。 如果這個值為0或不存在，則應用程式會在清單中正常顯示。                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

**FileAssociations** 子機碼包含應用程式所宣告的特定檔案關聯。 這些宣告會儲存為值，每個延伸模組都有一個值。 關聯會指向應用程式特定的 ProgID，而不是泛型 ProgID。 不過，並非所有關聯都必須指向相同的 ProgID。

### <a name="mimeassociations"></a>MIMEAssociations

**MIMEAssociations** 子機碼包含應用程式所宣告的特定 MIME 類型。 這些宣告會儲存為值，每個 MIME 類型都有一個值。 每個 MIME 類型的值名稱都必須完全符合 MIME 資料庫中所儲存的 MIME 名稱。 您也必須將應用程式特定的 ProgID 指派給此值，其中包含應用程式的對應 CLSID。

### <a name="startmenu"></a>Startmenu

**Startmenu** 子機碼與 [**開始**] 功能表中使用者可指派的 **網際網路** 和 **電子郵件** 專案相關聯。 應用程式必須個別註冊為這些專案的競爭者。 如需詳細資訊，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。

> [!Note]  
> 從 Windows 7 開始，[**開始**] 功能表中已不再有 **網際網路** 和 **電子郵件** 專案。 與 **電子郵件** 專案相關聯的登錄資料仍會用於預設的 MAPI 用戶端，但 Windows 完全不會使用與 **網際網路** 專案相關聯的登錄資料。

 

藉由將應用程式的 [ **開始** ] 功能表註冊與其 **預設程式** 註冊產生關聯，應用程式在 [ **設定關聯** ] UI 中會顯示為可能的預設值。 如果使用者選擇使用應用程式做為預設值，然後選擇還原所有的應用程式預設值，則會將應用程式還原至該使用者的 [ **開始** ] 功能表位置。 如需詳細資訊和圖例，請參閱本主題稍後的 [預設程式 UI](#default-programs-ui) 一節。

**Startmenu** 子機碼有兩個專案： [StartMenuInternet] 和 [Mail]，其對應于 [**開始**] 功能表中的標準 **網際網路** 和 **電子郵件** 位置。 應用程式會在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **客戶** 端 \\ **StartMenuInternet** 或 **HKEY \_ 本機 \_** 電腦軟體用戶端郵件 (] 下，指派等於應用程式登錄子機碼名稱的 StartMenuInternet 或 Mail 值， \\  \\  \\ 如) 的 [[註冊程式](reg-middleware-apps.md)] 中所述。

在 [**開始**] 功能表中的 **電子郵件** 標準位置案例中，它代表預設的 mapi 用戶端，因此假設能夠處理 MAPI 呼叫。 在 Windows 7 下，在 [**開始**] 功能表中已不再有 **電子郵件** 標準位置，這個子機碼會繼續用於預設的 MAPI 用戶端。 宣告郵件預設值的應用程式應該在下列子機碼下註冊為 MAPI 處理常式：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

如果郵件用戶端無法支援 MAPI，但仍想要爭用 [ **開始** ] 功能表 **電子郵件** 標準位置，它可以在下列子機碼底下註冊命令列：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

此外，在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** \\ *CanonicalName* ] 下，新增具有應用程式名稱的預設值。

這些專案可讓您從 [ **開始** ] 功能表的 **電子郵件** 位置啟動應用程式。 請注意，系統仍會對應用程式進行 MAPI 呼叫，並且會在先前的 MAPI 處理常式中執行，如果未設定 MAPI 處理常式，則會失敗。 如需詳細資訊，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。

### <a name="urlassociations"></a>UrlAssociations

**UrlAssociations** 子機碼包含應用程式所宣告的特定 URL 通訊協定。 這些宣告會儲存為值，每個通訊協定都有一個值。 每個通訊協定都必須指向應用程式特定的 ProgID，而不是一般 ProgID。 如 Contoso 範例中所述，您可以針對每個通訊協定使用不同的 ProgID，讓每個通訊協定都有自己的執行字串。

### <a name="registeredapplications"></a>RegisteredApplications

**RegisteredApplications** 的完整子機碼為：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **RegisteredApplications**

此子機碼為作業系統提供應用程式的 **預設程式** 資訊的登錄位置。 位置會儲存為值，其名稱必須與應用程式的名稱相符。

### <a name="full-registration-example"></a>完整註冊範例

此範例顯示用來註冊虛構 Litware 媒體播放機的子機碼和值。 此範例包含 ProgID 專案，以顯示其如何彼此搭配。

下列子機碼顯示 .mp3 MIME 類型的應用程式特定 ProgID：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

接下來是應用程式特定的 ProgID，會將 Litware 程式與 .mp3 副檔名產生關聯。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

下一個專案顯示 .mpeg MIME 類型和副檔名的合併 ProgID。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

下個專案會在 **預設程式** 中註冊 Litware 程式，並使用先前註冊的 progid

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

最後，此範例會註冊 Litware **預設程式** 註冊的位置。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>成為預設瀏覽器

瀏覽器註冊必須遵循本主題中所述的最佳做法。 當您安裝瀏覽器時，Windows 可以向使用者呈現系統通知，讓使用者可以選取瀏覽器做為系統預設值。 當符合下列條件時，就會顯示此通知：

-   瀏覽器的安裝程式會使用 **SHCNE \_ ASSOCCHANGED** 旗標來呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) ，告訴 Windows 已註冊新的通訊協定處理常式。
-   Windows 偵測到一或多個新的應用程式已註冊來處理 HTTP://和 HTTPs://通訊協定，且使用者尚未收到通知。 換句話說，使用者未看到下列其中一項：廣告應用程式的系統通知、包含應用程式的 OpenWith 飛出視窗，或應用程式的 [設定使用者預設值] (主控台) SUD] 頁面。

下列範例會顯示瀏覽器的安裝程式在寫入登錄機碼之後應該執行的建議註冊程式碼。

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 會先通知系統有新的關聯選項可供使用。 需要 **SHChangeNotify** 呼叫，才能確保系統預設值的正常運作。

然後， [**睡眠**](/windows/win32/api/synchapi/nf-synchapi-sleep) 語句可讓系統處理常式的時間處理通知。


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



如果使用者在未進行新的預設瀏覽器選取的情況下，關閉或忽略產生的通知或飛出視窗，預設瀏覽器會維持不變。 請注意，使用者也可以隨時透過其他機制變更預設瀏覽器，包括主控台中的設定使用者預設值。

## <a name="default-programs-ui"></a>預設程式 UI

本節中的圖例顯示使用者所見之 **預設程式** 的 UI。

下圖顯示主控台中的主要 **預設程式** 視窗。

![[預設程式] 專案頁面的螢幕擷取畫面](images/defaultprogramsmain.png)

當使用者選擇 [ **設定您的預設程式** ] 選項時，會出現下列視窗。 使用者可以使用此頁面，為所有檔案類型和通訊協定指派預設程式，此程式是可能的預設程式。 如下圖所示，所有 [已註冊](#registering-an-application-for-use-with-default-programs) 的程式和程式圖示都會出現在左側的 [ **程式** ] 方塊中。

![[設定您的預設程式] 頁面的螢幕擷取畫面](images/setyourdefaultprograms.png)

當使用者從清單中選取程式時，會顯示程式圖示和提供者。 如果 URL 內嵌在程式的數位簽署憑證中，程式也可以顯示 URL。 未經過數位簽署的程式無法顯示 URL。

程式在註冊期間提供的描述性文字也會顯示。 這是必要文字。 在 [描述] 方塊下方，指出目前已將程式指派給已註冊要處理之完整數位的預設數目。

若要將程式指派或還原為其註冊的所有檔案和通訊協定的預設值，使用者按一下 [ **將此程式設定為預設值** ]。

若要將個別的檔案類型和通訊協定指派給程式，使用者可以按一下 [ **選擇此程式的預設值** ] 選項，它會顯示程式視窗的 **設定關聯** ，如下圖所示。

> [!Note]  
> 建議您使用 [**IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)呼叫 **程式的設定關聯**。

 

![[設定關聯的程式] 頁面的螢幕擷取畫面](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>使用預設程式的最佳作法

本節提供在您註冊應用程式時使用 **預設程式** 的最佳做法指導方針。 它也提供建立應用程式的設計建議，以提供使用者最佳的 **預設程式** 功能。

### <a name="during-installation"></a>在安裝期間

除了通常會在 Windows XP 下練習的安裝程式之外，Windows Vista 或更新版本的應用程式必須向「**預設程式**」功能註冊，才能利用其功能。

在安裝期間，執行下列步驟順序。 步驟1-3 符合 Windows XP 中使用的步驟;步驟4是 Windows Vista 的新功能。

1.  安裝必要的二進位檔案。
2.  將 Progid 寫入 HKEY \_ 本機 \_ 電腦。 請注意，應用程式必須建立其關聯的應用程式特定 Progid。
3.  如先前 [註冊應用程式以搭配預設程式使用](#registering-an-application-for-use-with-default-programs)所述，使用 **預設程式** 來註冊應用程式。

### <a name="after-installation"></a>安裝後

本節討論應用程式提示應先對每個使用者呈現其預設選項。 它也會討論應用程式如何監視其狀態，以做為其可能的關聯和通訊協定的預設值。

### <a name="first-run-experiences"></a>首次執行體驗

當使用者第一次執行應用程式時，建議應用程式向使用者顯示通常包含這兩個選項的 UI：

-   接受預設的應用程式設定。 預設會選取這個選項。
-   自訂預設的應用程式設定。

在 Windows 8 之前，如果使用者接受預設設定，則您的應用程式會呼叫 [**IApplicationAssociationRegistration：： SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)，將安裝期間宣告的所有電腦層級關聯轉換成該使用者的每個使用者設定。

如果使用者決定自訂設定，您的應用程式就會呼叫 [**IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) 來顯示檔案關聯 UI。 下圖顯示虛構 Litware 媒體播放機的這個視窗。

![litware 的 [設定程式的關聯] 頁面的螢幕擷取畫面](images/setassociationsforaprogramforlitware.png)

[檔案關聯] 視窗會顯示應用程式註冊的預設值，也會顯示其他延伸模組和通訊協定的目前預設值。 當使用者完成自訂預設值之後，他們會按一下 [ **儲存** ] 按鈕來認可變更。 如果使用者按一下 [ **取消**]，視窗會關閉而不儲存變更。

您應該將此 UI 用於您的應用程式，而不是建立自己的應用程式。 如此一來，您就可以儲存先前開發檔案關聯 UI 所需的資源。 您也保證可以正確地儲存關聯。

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>設定應用程式以檢查它是否為預設值

> [!Note]  
> Windows 8 不再支援此功能。

 

應用程式通常會在執行時檢查它們是否設定為預設值。 藉由呼叫 [**IApplicationAssociationRegistration：： QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) 或 [**IApplicationAssociationRegistration：： QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)，設定您的應用程式來進行這項檢查。

如果應用程式判斷不是預設值，它可能會顯示 UI，詢問使用者是否要接受目前的情況，或將應用程式設為預設值。 一律在此 UI 中包含選取的核取方塊，並顯示不會再詢問的選項。

> [!Note]  
> 預設值應該是使用者導向的選項。 應用程式永遠不會在不詢問使用者的情況下回收預設值。

 

下圖顯示對話方塊範例。

![[範例] 對話方塊的螢幕擷取畫面](images/notthedefaultui.png)

## <a name="additional-resources"></a>其他資源

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案關聯的最佳作法](fa-best-practices.md)
</dt> <dt>

[檔案關聯範例案例](fa-sample-scenarios.md)
</dt> <dt>

[在 Windows Vista 和更新版本中管理預設應用程式的指導方針](vista-managing-defaults.md)
</dt> <dt>

[ (SPAD) 設定程式存取和電腦預設值 ](cpl-setprogramaccess.md)
</dt> </dl>

 

 
