---
description: Windows XP 和 Windows Vista 中的 [開始] 功能表包含預設網際網路 (瀏覽器的保留位置) 和電子郵件 (的電子郵件) 用戶端，通常稱為「開始功能表網際網路應用程式」。
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: 如何使用 Windows 開始功能表註冊網際網路瀏覽器或電子郵件客戶程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa40a8775a60fbdd55ba33c2039065d744734a3331727a749b2c3a2e3d564be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046675"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>如何使用 Windows 開始功能表註冊網際網路瀏覽器或電子郵件客戶程式

> [!Note]  
> 本主題適用于 Windows XP、Windows Vista 和 Windows 7。

 

Windows XP 和 Windows Vista 中的 [開始] 功能表包含預設 **網際網路** (瀏覽器的保留位置) 和 **電子郵件 (的電子郵件**) 用戶端，通常稱為 *「開始功能表網際網路應用程式」*。 以 [開始] 功能表的形式註冊的應用程式，會在整個系統 (每部電腦) 。 在 Windows Vista 中，使用者可以使用 [**預設程式**] 功能來設定每位使用者的預設值。

當應用程式註冊為開始功能表網際網路應用程式時，Windows XP 和 Windows Vista 會在 [開始] 功能表上建立 **網際網路** 和 **電子郵件** 圖示。 按一下這些圖示會導致 [開始] 功能表檢查每位使用者的登錄子樹， (**HKEY \_ 目前的 \_ 使用者**) 。 如果找不到每個使用者的預設設定，[開始] 功能表會在 [ **HKEY \_ 本機 \_ 電腦**] 子樹中尋找每部電腦的預設子機碼。

> [!Note]  
> 預設安裝 Windows 不會註冊每位使用者的預設網際網路或電子郵件程式，只會註冊整個系統的預設值。 這會從舊版作業系統提供順暢的升級路徑，在此版本中， \_ \_ 用戶端註冊只支援 HKEY 本機電腦子樹。

 

本主題將討論下列專案：

-   [註冊 [開始] 功能表網際網路連結](#registering-for-the-start-menu-internet-link)
    -   [如何註冊為預設的網際網路用戶端](#how-to-register-as-the-default-internet-client)
-   [註冊 [開始] 功能表電子郵件連結](#registering-for-the-start-menu-email-link)
    -   [[開始] 功能表如何顯示預設電子郵件客戶](#how-the-start-menu-displays-the-default-email-client)
    -   [如何註冊為預設電子郵件客戶](#how-to-register-as-the-default-email-client)
-   [自訂內容功能表](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>註冊 [開始] 功能表網際網路連結

> [!Note]  
> 此註冊已于 Windows 7 淘汰，不再提供 [開始] 功能表的網際網路連結。 Windows 7 和更新版本中會忽略現有的註冊。 註冊為預設的 [開始] 功能表網際網路應用程式與註冊為預設網頁瀏覽器並不相同。 預設的網頁瀏覽器可用來從系統中的任何位置啟動任意 Url。 [開始] 功能表的網際網路應用程式只會控制當使用者按一下 [開始] 功能表上的網際網路圖示時所啟動的程式。

 

任何網頁瀏覽器應用程式都可以註冊，以 [開始] 功能表上的網際網路用戶端顯示。 此可見度會結合[適當的應用程式檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型註冊，並提供應用程式預設瀏覽器狀態。

在 [ **HKEY \_ 目前 \_ 使用者** ] 子樹中進行的註冊，其優先順序會高於在 **HKEY \_ 本機 \_ 電腦** 中所做的相對應註冊的主控台使用者。 針對系統上的新使用者，會使用儲存在 **HKEY \_ 本機 \_ 電腦** 中的設定。 從 Windows XP，[開始] 功能表的網際網路設定會保留在兩個登錄位置的預設專案中：

-   **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet**
-   **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet**

子機碼 **HKEY \_ 目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet** 描述當使用者按一下 [開始] 功能表上的 **網際網路** 圖示時，所啟動的網際網路瀏覽器。 如果該子機碼為空白或遺失，則 [開始] 功能表上的 **網際網路** 圖示會設定為儲存在第二個位置的系統預設值 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet** ，其中描述系統上安裝的所有網際網路瀏覽器應用程式。

當新的使用者登入系統時，[開始] 功能表會在 [ **\_ 本機 \_ 電腦** 軟體用戶端] StartMenuInternet 的子機碼中使用預設值， \\  \\  \\ 以顯示預設的網際網路用戶端，並在按一下該圖示時啟動已註冊的應用程式。

### <a name="how-to-register-as-the-default-internet-client"></a>如何註冊為預設的網際網路用戶端

在 [ **\_ 本機 \_ 電腦** 軟體用戶端 HKEY] 子機碼底下 \\  \\  \\ **StartMenuInternet** 可以有零個或多個子機碼，每個已註冊的網際網路瀏覽器應用程式一個 例如，假設系統可能會有這種安排：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

我們將會從虛構公司（稱為 Litware Inc.）示範具有假設瀏覽器的登錄專案。假設亮 View 的可執行檔名稱是 Litview.exe。 此時會出現 [亮視圖] 的註冊，如下所示：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

>localizedstring 資料是 REG \_ SZ 類型， \_ \_ 如果使用路徑變數（例如），則 reg EXPAND sz `%programfiles%` 。 >localizedstring 會提供可執行檔 (.exe) 或程式庫 (.dll) 檔的路徑。 請注意，路徑字串的開頭為 "at" 符號 ( @ ) 而且路徑周圍不需要任何引號，不論其內是否有空格。 十進位整數是字串資源的識別碼，包含在指定的 DLL 內，其值會顯示給使用者。 這可讓相同的註冊用於多個語言。 每種語言都提供不同的 ResourceDLL.dll。 這可讓系統根據目前選取的語言顯示正確的字串。

下列 reg \_ sz 或 REG \_ EXPAND \_ sz 值會通知 [開始] 功能表當使用者選取 [亮視圖] 作為 [開始] 功能表的網際網路瀏覽器時，所要顯示的預設圖示。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

下列登錄子機碼會指定當使用者按一下 [開始] 功能表上的 [網際網路] 功能表命令時要執行的命令列，並假設 [亮視圖] 是選取的 [開始] 功能表網際網路瀏覽器。 例如，此命令可能會使用使用者的首頁來開啟瀏覽器，或命令可能會啟動獨立軟體廠商 (ISV) 所覺得的入門使用者介面。 資料的類型是 REG \_ sz 或 reg \_ EXPAND \_ sz，但請注意，因為命令列路徑中有一個空格，可執行檔路徑會以引號括住。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

當使用者透過 [ [設定程式存取] 和 [電腦預設值 ](cpl-setprogramaccess.md) ] 來指定時 (SPAD) 應該使用亮 View 作為電腦層級的預設網頁瀏覽器，應用程式應該設定下列 REG \_ SZ 專案。 請注意，由於 SPAD 是以系統管理員許可權執行，因此允許存取此子機碼。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> 在 Windows Vista 中，使用者層級的預設網頁瀏覽器應該使用 [**預設程式**] 工具來設定，而不是 [ [SPAD](cpl-setprogramaccess.md)]。
> 
> **下列資訊僅適用于 Windows XP。**
> 
> 如果在 HKEY 本機電腦下註冊電腦層級的預設網頁瀏覽器 \_ \_ （如上所示），則應用程式應該刪除下列子機碼底下的預設專案：
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> 如果在 HKEY 本機電腦下註冊電腦層級的預設網頁瀏覽器 \_ \_ 失敗，應用程式應該 \_ 為「亮視圖」應用程式設定如下列範例所示的 REG SZ 資料：
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

更新適當的子機碼之後，應用程式會廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，並將其 *wParam* 參數設定為0，並將其 *lParam* 參數指向以 null 終止的字串 `"Software\Clients\StartMenuInternet"` 。 這會通知作業系統預設用戶端已變更。

針對預設的 [開始] 功能表網際網路瀏覽器設定這些子機碼，必須保持與舊版網頁瀏覽器的回溯相容性，而這些網頁瀏覽器不支援每一使用者的註冊。

## <a name="registering-for-the-start-menu-email-link"></a>註冊 [開始] 功能表電子郵件連結

> [!Note]  
> [開始] 功能表的電子郵件連結已從 Windows 7 移除。 不過，本章節中討論的這項註冊仍應針對其對指派預設 MAPI 用戶端的影響執行。

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>[開始] 功能表如何顯示預設電子郵件客戶

任何電子郵件應用程式都可以註冊，以在 [開始] 功能表上顯示為電子郵件客戶程式。 此可見度與適當的應用程式[檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型註冊結合，可提供應用程式預設的郵件狀態。

在 [ **HKEY \_ 目前 \_ 使用者** ] 子樹中進行的註冊，其優先順序會高於在 **HKEY \_ 本機 \_ 電腦** 中所做的相對應註冊的主控台使用者。 針對系統上的新使用者，會使用儲存在 **HKEY \_ 本機 \_ 電腦** 中的設定。 從 Windows XP，[開始] 功能表的電子郵件設定會保留在兩個登錄位置的預設專案中：

-   **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **郵件**
-   **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件**

子機碼 **HKEY \_ CURRENT \_ user** \\ **SOFTWARE** \\ **Clients** \\ **Mail** 描述當使用者按一下 [開始] 功能表上的 **電子郵件** 圖示時，所啟動的電子郵件客戶程式。

子 **機碼 HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 會描述安裝在系統上的電子郵件應用程式，以及預設的電子郵件應用程式。

如果 **HKEY \_ CURRENT \_ USER** \\ **software** \\ **用戶端** \\ **郵件** 為空白或遺失，則會使用 [ **HKEY \_ 本機 \_ 電腦** 軟體用戶端郵件] 中定義的預設值 \\  \\  \\ 來選取出現在 [開始] 功能表上的電子郵件應用程式。

當新的使用者登入系統時，[開始] 功能表會使用子機碼中 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 的預設值來顯示預設電子郵件客戶程式，並在按一下該圖示時啟動已註冊的應用程式。

### <a name="how-to-register-as-the-default-email-client"></a>如何註冊為預設電子郵件客戶

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 可以包含零或多個子機碼，每個已註冊的電子郵件應用程式都有一個。 例如，假設系統可能會定義下列子機碼：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

我們將示範名為 Litware Inc. Litware Inc. 之虛構公司的假設電子郵件客戶的登錄專案，其名為 "LitMail" 的虛構公司的電子郵件用戶端。 如同瀏覽器，內部名稱是用來做為子機碼名稱的唯一字串，但永遠不會向使用者顯示。

若要安裝 Lit Mail 電子郵件用戶端作為預設值，則會使用下列子機碼和其專案：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

>localizedstring 資料是 REG \_ SZ 類型， \_ \_ 如果使用路徑變數（例如），則 reg EXPAND sz `%programfiles%` 。 >localizedstring 會提供可執行檔 (.exe) 或程式庫 (.dll) 檔的路徑。 請注意，路徑字串的開頭為 "at" 符號 ( @ ) 而且路徑周圍不需要任何引號，不論其內是否有空格。 十進位整數是字串資源的識別碼，包含在指定的 DLL 內，其值會顯示給使用者。 這可讓相同的註冊用於多個語言。 每種語言都提供不同的 ResourceDLL.dll。 這可讓系統根據目前選取的語言顯示正確的字串。

更新適當的子機碼之後，應用程式會廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，並將其 *wParam* 參數設定為0，並將其 *lParam* 參數指向以 null 終止的字串 `"Software\Clients\Mail"` 。 這會通知作業系統預設用戶端已變更。

為了與不支援當地語系化字串的應用程式回溯相容，已安裝語言中的應用程式名稱也應該設定為子機碼的預設值。

下列 **reg \_ sz** 或 **REG \_ EXPAND \_ sz** 值會在使用者選取 Lit mail 做為 [開始] 功能表 mail 程式時，通知顯示預設圖示的 [開始] 功能表：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

下列專案會指定當使用者按一下 [開始] 功能表上的 [**電子郵件**] 功能表項目時要執行的命令列，並假設 [Lit mail] 是選取的 [開始] 功能表電子郵件程式。 如果使用者選取 [Windows Internet Explorer **工具**] 功能表中的 [**讀取電子郵件**]，也會執行此命令列。 資料的類型是 **REG \_ Sz** 或 **reg \_ EXPAND \_ sz**，但請注意，因為命令列路徑中有一個空格，可執行檔路徑會以引號括住。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

如果 (，而且只有在) *使用者* 將 [lit mail] 指定為預設 [開始] 功能表電子郵件應用程式時，則 lit mail 應用程式可能會將其內部名稱寫入至下列 **REG \_ SZ** 值：

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

如果 (，而且只有在) *使用者* 將 Lit mail 指定為全系統的預設電子郵件應用程式時，lit mail 應用程式可能會將其內部名稱寫入至下列指定的 **REG \_ SZ** 值。 請注意，這個子機碼的存取權可能會受到限制。 應用程式不應假設所有使用者都有變更全系統預設電子郵件應用程式的許可權。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

註冊為預設的 [開始] 功能表電子郵件應用程式，並不等同于註冊為系統預設電子郵件客戶程式或註冊的 *mailto* 處理常式。

-   當使用者按一下 Internet Explorer [**工具**] 功能表中的 [**讀取電子郵件**] 時，就會啟動系統預設電子郵件客戶程式。
-   當使用者按一下表單的 URL 時，即會啟動註冊的 *mailto* 處理常式 `mailto:someone@example.com` 。
-   當使用者按一下 [開始] 功能表上的 [**電子郵件**] 圖示時，就會啟動 [開始] 功能表電子郵件應用程式。

如果未指定預設的 [開始] 功能表電子郵件應用程式，[開始] 功能表的電子郵件圖示就會啟動系統預設的電子郵件客戶程式。

本主題並未涵蓋將應用程式註冊為預設 *mailto* 通訊協定處理常式的程式。 想要以這種方式註冊的應用程式應該繼續遵循本主題的現有規格。

## <a name="customizing-the-context-menu"></a>自訂內容功能表

應用程式可以自訂使用者從 **電子郵件** 中選取 **屬性** 時所顯示的屬性頁 (或 **網際網路**) 圖示的快捷方式功能表。 例如，Litware 電子郵件應用程式會新增下列 **REG \_ Sz** 或 **REG \_ EXPAND \_ sz** 資料，以顯示 **電子郵件** 圖示的自訂屬性工作表，而不是其預設屬性表。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

MUIVerb 資料項目是以 "at" 正負號 ( @ ) 開始，後面接著資源 DLL 的完整路徑、逗號、減號 ( ) ，然後是要顯示的十進位字串資源識別碼。 請注意，LitMail.exe 程式的路徑包含空格，因此路徑字串會放置在引號內。

應用程式也可以在內容功能表中新增其他命令。 例如，Litware 電子郵件應用程式會新增具有下列 **REG \_ SZ** 資料的 **find** 命令：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

**Shell** 下的子機碼名稱 (在此案例中，"find" ) 是任意的未當地語系化名稱。 同樣地，MUIVerb 的資料也會包含 "at" 符號 ( @ ) 作為第一個元素，後面接著資源 DLL 的路徑、逗號分隔字元，然後是小數點字串資源識別碼前面的減號。 例如，該字串資源可能是「開啟通訊錄」。 最後，請注意，命令列字串包含空格，因此會以引號括住。

 

 
