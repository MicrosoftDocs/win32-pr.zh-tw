---
title: 建立搜尋處理常式
description: Shell 支援數個搜尋公用程式，可讓使用者找出命名空間物件，例如檔案或印表機。 您可以建立自訂搜尋引擎，並藉由執行和註冊搜尋處理常式，讓使用者可以使用它。
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- 搜尋處理常式
- 註冊，搜尋處理常式
- 靜態搜尋處理常式
- 註冊、靜態搜尋處理常式
- 動態搜尋處理常式
- 註冊、動態搜尋處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315034"
---
# <a name="creating-search-handlers"></a>建立搜尋處理常式

\[只有在 Windows XP 或更早版本才支援這項功能。 請改用 Windows Search。\]

Shell 支援數個搜尋公用程式，可讓使用者找出命名空間物件，例如檔案或印表機。 您可以建立自訂搜尋引擎，並藉由執行和註冊 *搜尋處理常式*，讓使用者可以使用它。

[建立 shell](/windows/desktop/shell/handlers)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于搜尋處理常式特定的執行層面。

-   [搜尋處理常式的運作方式](#how-search-handlers-work)
-   [註冊搜尋處理常式](#registering-search-handlers)
    -   [註冊靜態搜尋處理常式](#registering-a-static-search-handler)
    -   [註冊動態搜尋處理常式](#registering-a-dynamic-search-handler)
-   [執行搜尋處理常式](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>搜尋處理常式的運作方式

使用者有兩種方式可以選取搜尋引擎。 第一種方式是從 [開始] 功能表。 在 Windows 2000 之前的系統上，選取 [**開始**] 功能表上的 [**尋找**] 命令會顯示可用搜尋引擎的子功能表。 在 Windows 2000 和更新版本中， **St** 的功能表的 [ **尋找** ] 命令會重新命名為 [搜尋]。 下圖顯示 Windows XP 系統上的 [ **搜尋** ] 按鈕。

![[開始] 功能表的 [搜尋] 子功能表](images/searchhandler1.jpg)

使用者也可以從 Windows 檔案總管啟動搜尋。 在 Windows 2000 之前的系統上，他們會按一下 [**工具**] 功能表上的 [**尋找**] 命令，顯示與 [**開始**] 功能表相關聯的功能表基本上是相同的功能表。 不過，Windows 2000 的 Windows 檔案總管會以非常不同的方式處理搜尋引擎。 工具列上現在有一個 [**搜尋**] 按鈕，而不是以 **工具** 功能表的子功能表來處理搜尋引擎。 按一下這個按鈕會開啟 Explorer 列的 [ **搜尋** ] 窗格。 下圖顯示 [ **搜尋檔案和資料夾** ] 搜尋窗格。

![windows explorer bar 的 [搜尋] 窗格](images/searchhandler2.jpg)

Windows 2000 和舊版系統如何管理影響執行和註冊的搜尋處理常式有一些差異。



| Windows 之前的2000                                                                                                                                                                                                       | Windows 2000 和更新版本                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 搜尋處理常式會實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)的類型。                                                                                                                     | 搜尋處理常式可以實作為快捷方式功能表處理常式，或是動態 HTML (DHTML) 檔。                                                                                                                                                                                                               |
| 搜尋處理常式可以是靜態或動態。 只有當使用者選取靜態處理常式時，才會載入靜態處理常式。 動態處理常式是由 Shell 在啟動時載入，而且在 Shell 結束之前不會終止。 | 實作為快捷方式功能表處理常式的處理常式可以是靜態或動態。 實作為 DHTML 檔案的處理常式必須是靜態的。                                                                                                                                                                           |
| 搜尋處理常式會顯示在 [**開始**] 功能表的 [**尋找**] 子功能表和 [Windows 檔案總管  **工具**] 功能表的 [**尋找**] 子功能表中。                                                                                  | 搜尋處理常式只會出現在 [**開始**] 功能表的 [**搜尋**] 子功能表上。 若要透過 Windows 檔案總管的功能表列提供自訂的搜尋窗格，您必須將它實作為 [帶區物件](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))。 然後，它會列在 [Windows 檔案總管  **View** ] 功能表的 [ **Explorer Bar** ] 子功能表上。 |



 

## <a name="registering-search-handlers"></a>註冊搜尋處理常式

搜尋處理常式會在檔案類型的 **FindExtensions** 子機碼下註冊。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

從此時開始，註冊程式取決於處理常式是靜態或動態。 如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](/windows/desktop/shell/handlers)程式。

### <a name="registering-a-static-search-handler"></a>註冊靜態搜尋處理常式

靜態搜尋處理常式只有在使用者啟動時才會載入。 這種方法最適合適用于較小且可快速載入的 Dll。 如果您使用 DHTML 來執行處理常式，它必須是靜態的。 若要註冊靜態延伸模組處理常式，請在 **FindExtensions** 子機碼的 **靜態** 子機碼下，建立名為的處理常式的子機碼。 系統不會使用該名稱，但它不能與 **FindExtensions** 子機碼下的其他搜尋處理常式名稱相同。

### <a name="shortcut-menu-based-search-handlers"></a>以快捷方式功能表為基礎的搜尋處理常式

如果您的處理常式是實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)，請將處理常式名稱子機碼的預設值設定為物件的類別識別碼， (CLSID) GUID。 在處理常式的名稱子機碼下，建立名為 **0** (零) 的子機碼，   並將其預設值設定為要顯示在 [**搜尋**] 或 [**尋找**] 子功能表中的字串。 您可以用一般方式啟用鍵盤快速鍵，方法是在快速鍵字元前面加上連字號 (&) 。 您可以在 [ **0** ] 子機碼底下建立 **DefaultIcon** 子機碼，以在功能表文字右邊顯示選擇性的小圖示。 將其預設值設定為字串，其中包含包含圖示之檔案的路徑，後面接著逗號，再接著圖示的以零為基底的索引。

下列範例會註冊 **MySearchEngine** 搜尋處理常式。 功能表文字是「我的搜尋引擎」，其中 M 指定為快速鍵。 此圖示為 C： \\ MyDir \\MySearch.dll，索引為2。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>以 DHTML 為基礎的搜尋處理常式

使用 Windows 2000，您也可以將搜尋處理常式實作為 DHTML 檔案。 其名稱會列在 [**開始**] 功能表的 [**搜尋**] 子功能表中。 當使用者選取該檔案時，它會啟動 Windows 檔案總管，並開啟搜尋檔的瀏覽器列。 您也可以指定要顯示在 Explorer 列右邊的 DHTML 檔案。 沒有任何方法可以從預設的 [搜尋] 窗格啟動不同的處理常式。 您可以直接從 Windows 檔案總管啟動搜尋引擎，但必須將它們實作為 [頻外物件](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))。

若要註冊以 DHTML 為基礎的搜尋處理常式，請將處理常式的名稱子機碼設定為 CLSID \_ ShellSearchExt (目前為 {169A0691-8DF9-11d1-A1C4-00C04FD75D13} ) 的字串格式，然後建立下列子機碼。

1.  在處理常式名稱子機碼底下建立 **0** (零) 子機碼，並將其預設值設定為功能表文字。
2.  若要在功能表文字旁邊顯示圖示，請在 **0** 底下建立 **DefaultIcon** 子機碼，並將其預設值設定為圖示的路徑和索引。
3.  在 **0** 底下建立 **SearchGUID** 子機碼。 將 GUID 指派給 DHTML 檔案，並將 **SearchGUID** 的預設值設定為其字串格式。 此 GUID 不需要在 **HKEY \_ 類別的 \_ 根目錄 \\ CLSID** 下註冊。
4.  在 **SearchGUID** 下建立 **Url** 子機碼。 將其預設值設定為將會出現在 Explorer 列中的 HTML 檔案的路徑。
5.  在 **SearchGUID** 下建立 **UrlNavNew** 子機碼。 將其預設值設定為顯示在 Explorer 列右邊的 HTML 檔案路徑。

下列範例會註冊實作為 DHTML 檔案的 **MySearchEngine** 搜尋處理常式。 功能表文字是「我的搜尋引擎」，其中 M 指定為快速鍵。 此圖示為 C： \\ MyDir \\MySearch.dll，索引為2。 Explorer 列的 DHTML 檔案是 C： \\ MyDir \\MySearch.htm，而顯示在 Explorer 列右邊的檔是 c： \\ MyDir \\MySearchPage.htm。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>註冊動態搜尋處理常式

如果您的處理常式實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)，您也可以將它註冊為動態處理常式。 在這種情況下，它會使用 Shell 載入，而且只會在 Shell 結束時終止。 當使用者啟動動態搜尋處理常式時，動態搜尋處理常式的回應速度會比靜態處理常式更快。 如果處理常式的 DLL 可能需要很長的時間載入，或可能經常呼叫，這個方法的效果最好。

動態搜尋處理常式會在 **FindExtensions** 子機碼下註冊。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

針對處理常式建立名為 **FindExtensions** 的子機碼，並將其預設值設定為處理常式的 CLSID GUID。 動態搜尋處理常式不支援功能表圖示。 下列範例會將 MySearchEngine 註冊為動態搜尋處理常式。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

與靜態搜尋處理常式不同的是，您不會在登錄中指定功能表文字。 載入處理常式時，Shell 會呼叫處理常式的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法，將專案加入至 [ **尋找** ] 或 [ **搜尋** ] 子功能表。

## <a name="implementing-search-handlers"></a>執行搜尋處理常式

搜尋處理常式可以實作為所有 Windows 版本的快捷方式功能表處理常式。 針對 Windows 2000，也可以將它們實作為 DHTML 檔案。

如需如何執行快捷方式功能表處理常式的一般討論，請參閱 [建立內容功能表處理常式](/windows/desktop/shell/context-menu-handlers)。 搜尋處理常式不同于標準快捷方式功能表處理常式，只是幾種方式。

若為靜態功能表處理常式，則會從登錄中的資訊建立 [ **尋找** ] 或 [ **搜尋** ] 子功能表。 您不需要讓處理常式加入功能表項目，因為一般的快捷方式功能表處理常式會這樣做。 Shell 會以下列方式管理靜態功能表處理常式。

-   當使用者啟動處理常式的功能表項目時，Shell 會載入處理常式的 DLL，並呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 來通知處理常式啟動搜尋引擎。 不會呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 和 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法。
-   呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)時，傳入的 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)結構的 **lpVerb** 成員會識別命令。 **LpVerb** 的低序位字組會設定為與命令子機碼名稱相等的數位。 因為這個子機碼通常會命名為 **0**，所以 **lpVerb** 通常會設定為零。 然後，處理常式應該啟動搜尋引擎。

動態搜尋處理常式的執行方式與一般快捷方式功能表處理常式的方式大致相同。 主要的例外狀況是在呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 時， *pidlFolder* 和 *lpdobj* 引數都會設定為 **Null**。

DHTML 搜尋處理常式會實作為一般 DHTML 檔案。 它們可以包含 Windows Internet Explorer 所支援的任何 HTML、DHTML 或腳本技術。

 

 