---
description: 在匯出 CPlApplet 函式的 DLL 中所執行的主控台專案，其註冊需求與 .exe 檔不同。
title: 如何註冊 DLL 主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593188"
---
# <a name="how-to-register-dll-control-panel-items"></a>如何註冊 DLL 主控台專案

> [!Note]  
> 目前的執行指導方針指出新的主控台專案應該實作為 .exe 檔案，而不是 .cpl 檔。 下列資訊主要包含在舊版用途中。

 

在匯出 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式的 DLL 中所執行的主控台專案，其註冊需求與 .exe 檔不同。 從 Windows XP 中，新的主控台專案 dll 應該安裝在 [Program Files] 資料夾下相關聯的應用程式資料夾中。 不需要註冊儲存在 System32 目錄中且副檔名為 .cpl 的專案;它們會自動顯示在主控台中。 使用 **CPlApplet** 的所有其他主控台專案都必須以下列兩種方式之一進行註冊：

-   如果要將主控台專案提供給所有使用者使用，請在每一部電腦上註冊路徑，方法是將 **REG \_ EXPAND \_ SZ** 值新增至 **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **主控台** \\ **Cpls** 子機碼，並設定為 DLL 路徑。
-   如果主控台專案是以每個使用者為基礎，請使用 **HKEY \_ 目前 \_ 使用者** 做為根機碼，而不是 **HKEY \_ 本機 \_ 電腦**。

下列兩個範例會註冊 *MyCplApp* 主控台專案。 DLL 的名稱為 MyCpl.cpl，位於 *MyCorp \\ MyApp* 應用程式目錄中。 第一個範例說明每一電腦的註冊。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

將這項資訊新增至登錄，以註冊 .cpl 檔案的存在。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>步驟 2:

**Windows Vista 和更新版本：** 將此額外資訊新增至登錄，以提供主控台專案的 GUID。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

藉由產生可唯一識別主控台專案的 GUID，您可以將工作連結加入至主控台。 若沒有此 GUID，則無法將工作連結與主控台專案相關聯。 請參閱 [建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)。

### <a name="step-3"></a>步驟 3：

**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以建立專案的正式名稱。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

藉由新增正式名稱，使用者可以輸入，從命令列啟動主控台專案 `control.exe /name MyCorporation.MyCpl` 。 這也可以讓您稍後將 .cpl 檔案中的執行變更為 .exe 檔案，而不需要呼叫程式進行任何變更，因為它們可以繼續透過其正式名稱開啟專案。 如需標準名稱的詳細資訊，請參閱 [執行主控台專案](executing-control-panel-items.md)。

### <a name="step-4"></a>步驟 4：

**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以將主控台專案指派給一或多個類別。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP：** 將下列資訊新增至登錄，以將主控台專案指派給一或多個類別。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

此範例會將專案指派給類別3，也就是網路和網際網路。 若要將專案加入至多個類別，請以 \_ 逗號分隔的 REG SZ 值（例如 "3，8"）提供清單。 值可以是十進位或十六進位。 請注意，只有在 Windows XP Service Pack 2 (SP2) 和更新版本中，才能將專案加入至多個類別目錄的功能。 請參閱為所有可能的值 [指派主控台分類](assigning-control-panel-categories.md) 。

### <a name="step-5"></a>步驟 5：

**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以建立並指向 XML 檔案，以保存專案的工作連結。 此值必須是 REG \_ SZ 路徑（如下所示）或模組和資源識別碼 (例如 "C： \\ Program Files \\ MyCorp \\ MyApp \\MyApp.exe，-31" ) （如果它是內嵌的資源）。 應完整指定 XML 檔案的位置。 它不能使用環境變數，例如% ProgramFiles%。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

如需工作連結的詳細資訊，以及如何建立 XML 檔案來保存它們，請參閱 [建立主控台專案](creating-searchable-task-links.md)的可搜尋工作連結。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[如何註冊可執行檔主控台專案](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
