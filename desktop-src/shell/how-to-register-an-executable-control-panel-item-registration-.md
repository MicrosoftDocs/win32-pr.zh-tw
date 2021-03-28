---
description: 針對實作為 .exe 檔的主控台專案，不需要特殊的匯出或訊息處理。 您可以將任何 .exe 檔案註冊為命令物件，以在主控台資料夾中顯示進入點。
title: 如何註冊可執行檔主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026732"
---
# <a name="how-to-register-executable-control-panel-items"></a>如何註冊可執行檔主控台專案

針對實作為 .exe 檔的主控台專案，不需要特殊的匯出或訊息處理。 您可以將任何 .exe 檔案註冊為命令物件，以在主控台資料夾中顯示進入點。

這裡使用範例來示範註冊需求。 此範例示範如何將稱為「 **我的設定** 」主控台專案註冊為命令物件，使其出現在 [主控台] 視窗中。 當命令執行時，[ **我的設定** ] 視窗也會出現 `MyApp.exe /settings` 。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

產生主控台專案的 GUID。 GUID 可唯一識別主控台專案。 在此範例中， `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` 是主控台專案的 GUID。

### <a name="step-2"></a>步驟 2:

使用 GUID 做為名稱，將子機碼新增到登錄中，如下所示。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

預設專案的資料只是主控台專案的 REG \_ SZ 名稱。 預設專案有助於識別 GUID 專案，但它是選擇性的。

### <a name="step-3"></a>步驟 3：

使用 GUID 做為名稱，將子機碼和其專案新增到登錄中，如下所示。

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Default**。 REG \_ SZ。 主控台專案的顯示名稱。
-   **>localizedstring**。 選擇性。 REG \_ sz 或 reg \_ 展開 \_ SZ。 主控台專案之當地語系化名稱的模組名稱和字串資料表識別碼。 格式為 "at" 符號 ( @ ) 後面接著包含多語系消費者介面 (MUI) 字串資料表的 .exe 或 .dll 的名稱。 環境變數可以用來取代路徑的一部分。 路徑和檔案名後面會接著逗號 (、) 和連字號 ( ) ，後面接著字串表中的識別碼。

    如果模組沒有字串資料表，則此專案可以是顯示名稱字串。 如果您只使用顯示名稱字串，而不是字串資料表，則名稱不會調整為目前的顯示語言。

-   提示。 REG \_ sz 或 reg \_ 展開 \_ SZ。 主控台專案的描述。 這項資訊會顯示在滑鼠停留在專案的圖示上時所顯示的資訊提示中。 語法與用於 >localizedstring 的語法相同，包括只提供字串而非字串資料表參考的選項。
-   **** System.servicemodel。 REG \_ SZ。 專案的正式名稱。 Form 的命令 `control.exe /name System.ApplicationName` 會開啟此專案，例如 `control.exe /name MyCorporation.MySettings` 。 如需使用 Control.exe 的詳細資訊，請參閱 [執行主控台專案](executing-control-panel-items.md) 。
-   **控制台類別**。 REG \_ SZ。 值，宣告出現專案的主控台類別目錄。 多個類別會以逗號分隔。 在上述範例的案例中，專案會指定 [我的 **設定** ] 專案應該出現在 [ **外觀] 和 [個人** 化] 和 [ **程式** ] 類別中。 請參閱 [指派主控台類別](assigning-control-panel-categories.md) 以取得可能的類別值。
-   **System.software.tasksfileurl**。 REG \_ sz 或 reg \_ 展開 \_ SZ。 定義工作 [連結](creating-searchable-task-links.md)之 XML 檔案的路徑。 這可以是直接檔案路徑（如範例所示），或指定為模組名稱和資源識別碼（例如 "% ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe，-31"）的內嵌資源。

### <a name="step-4"></a>步驟 4：

在相同的 GUID 子機碼下，將下列子機碼新增至登錄，以提供檔案的路徑，該檔案包含圖示和該檔案中映射的資源識別碼。

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

請注意，雖然語法類似于稍早所討論的 >localizedstring 和提示專案，但不會使用 ' @ ' 字元做為 REG sz 中的前置詞， \_ 或 reg \_ EXPAND \_ 指定路徑的專案。

### <a name="step-5"></a>步驟 5：

將下列資訊新增至登錄，以提供使用者開啟主控台時由系統呼叫的命令。

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[如何註冊 DLL 主控台專案](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



