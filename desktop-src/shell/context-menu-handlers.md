---
description: 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。 就像所有這類處理常式一樣，它們都是同進程元件物件模型， (COM) 物件實作為 Dll。
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: 建立快捷方式功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "103853192"
---
# <a name="creating-shortcut-menu-handlers"></a>建立快捷方式功能表處理常式

快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。 就像所有這類處理常式一樣，它們都是同進程元件物件模型， (COM) 物件實作為 Dll。

> [!Note]  
> 註冊在32位應用程式內容中運作的處理常式時，會有64位 Windows 的特殊考慮：當 Shell 動詞命令在32位應用程式的內容中叫用時，WOW64 子系統會將檔案系統存取重新導向至某些路徑。 如果您的 .exe 處理常式儲存在其中一個路徑中，就無法在此內容中存取。 因此，若要解決這個問題，請將 .exe 儲存在未重新導向的路徑中，或儲存啟動實際版本之 .exe 的存根版本。

 

本主題的組織方式如下：

-   [標準動詞](#canonical-verbs)
-   [擴充的動詞](#extended-verbs)
-   [使用靜態動詞自訂快捷方式功能表](#customizing-a-shortcut-menu-using-static-verbs)
    -   [使用 IDropTarget 介面啟用處理常式](#activating-your-handler-using-the-idroptarget-interface)
    -   [指定靜態動詞命令的位置和順序](#specifying-the-position-and-order-of-static-verbs)
    -   [將動詞放置於功能表頂端或底部](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [建立靜態串聯功能表](#creating-static-cascading-menus)
    -   [使用 Advanced Query 語法取得靜態動詞命令的動態行為](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [已淘汰：將動詞與動態資料交換命令建立關聯](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [完成動詞執行工作](#completing-verb-implementation-tasks)
    -   [自訂預先定義之 Shell 物件的快捷方式功能表](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [擴充新的子功能表](#extending-a-new-submenu)
    -   [隱藏動詞和控制可見度](#suppressing-verbs-and-controlling-visibility)
    -   [採用動詞選取模型](#employing-the-verb-selection-model)
    -   [使用專案屬性](#using-item-attributes)
    -   [透過 Desktop.ini為資料夾執行自訂動詞 ](#implementing-custom-verbs-for-folders-through-desktopini)
-   [相關主題](#related-topics)

## <a name="canonical-verbs"></a>標準動詞

應用程式通常負責為其定義的動詞提供當地語系化的顯示字串。 不過，為了提供某種程度的語言獨立性，系統會定義一組標準的常用動詞，稱為標準動詞。 標準動詞永遠不會向使用者顯示，而且可以搭配任何 UI 語言使用。 系統會使用標準名稱自動產生適當當地語系化的顯示字串。 例如，開啟動詞的顯示字串會設定為在英文系統上 **開啟** ，以及德文系統上的德文對等專案。



| 標準動詞 | Description                                                          |
|----------------|----------------------------------------------------------------------|
| 開啟           | 開啟檔案或資料夾。                                            |
| Opennew        | 在新視窗中開啟檔案或資料夾。                            |
| 列印          | 列印檔案。                                                     |
| Printto        | 允許使用者將檔案拖曳至印表機物件來列印該檔案。 |
| 探索        | 開啟 Windows 檔案總管，並選取資料夾。                     |
| 屬性     | 開啟物件的屬性工作表。                                   |



 

> [!Note]  
> **Printto** 動詞也是標準的，但永遠不會顯示。 它包含可讓使用者將檔案拖曳至印表機物件來列印該檔案。

 

快速鍵功能表處理常式可透過 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 搭配 **Gc \_ VERBW** 或 **gc \_ VERBA** 來提供自己的標準動詞。 系統會使用標準動詞作為第二個參數， (*lpOperation*) 傳遞至 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)，而是 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)。傳遞至 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)方法的 **lpVerb** 成員。

## <a name="extended-verbs"></a>擴充的動詞

當使用者以滑鼠右鍵按一下物件時，快捷方式功能表會顯示預設的動詞命令。 您可能想要在某些快捷方式功能表上新增和支援命令，而這些快捷方式功能表未顯示在每個快捷方式功能表上。 例如，您可能會有不常使用或適用于有經驗的使用者的命令。 基於這個理由，您也可以定義一或多個擴充動詞。 這些動詞命令類似于一般動詞，但會透過其註冊方式與一般動詞進行區別。 若要存取擴充的動詞，使用者必須在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件。 當使用者這樣做時，除了預設動詞以外，還會顯示擴充的動詞。

您可以使用登錄來定義一個或多個擴充動詞。 只有當使用者以滑鼠右鍵按一下物件，同步選取 SHIFT 鍵時，才會顯示相關聯的命令。 若要將動詞定義為擴充，請將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。 此值不應該有任何與其相關聯的資料。

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>使用靜態動詞自訂快捷方式功能表

[為快捷方式功能表選擇靜態或動態動詞命令](shortcut-choose-method.md)之後，您可以註冊檔案類型的靜態動詞命令，以擴充檔案類型的快捷方式功能表。 若要這樣做，請在與檔案類型相關聯的應用程式 ProgID 的子機碼底下，新增 **Shell** 子機碼。 （選擇性）您可以為檔案類型定義預設動詞，方法是將它設為 **Shell** 子機碼的預設值。

預設動詞會先顯示在快捷方式功能表上。 其目的是在呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函式時提供 Shell 所能使用的動詞命令，但不會指定任何動詞。 以這種方式使用 **ShellExecuteEx** 時，Shell 不一定會選取預設的動詞命令。

Shell 會依下列順序使用第一個可用的動詞：

1.  預設動詞
2.  如果指定了動詞順序，則為登錄中的第一個動詞
3.  **Open** 動詞
4.  **Open With** 動詞

如果未列出任何可用的動詞，作業就會失敗。

針對您想要在 Shell 子機碼下新增的每個動詞，各建立一個子機碼。 這些子機碼中的每個子機碼都必須將 **REG \_ SZ** 值設定為動詞的顯示字串， (當地語系化的字串) 。 針對每個動詞子機碼，建立命令子機碼，並將預設值設定為啟用專案的命令列。 針對標準動詞，例如 [ **開啟** ] 和 [ **列印**]，您可以省略顯示字串，因為系統會自動顯示適當的當地語系化字串。 針對 noncanonical 動詞，如果您省略顯示字串，則會顯示動詞字串。

在下列登錄範例中，請注意：

-   因為 **doit r** 不是標準動詞，所以會將顯示名稱指派給它，您可以按 D 鍵加以選取。
-   **Printto** 動詞未出現在快捷方式功能表上。 不過，它包含在登錄中可讓使用者藉由將檔案放在印表機圖示上來進行列印。
-   每個動詞都會顯示一個子機碼。 **%1** 代表檔案名和 **%2** 印表機的名稱。

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

下圖說明以上述登錄專案為依據的快捷方式功能表延伸。 此快捷方式功能表在其功能表上已 **開啟**、 **完成** 及 **列印** 動詞命令，並將 **其做** 為預設動詞。

![[做為預設動詞] 快捷方式功能表的螢幕擷取畫面](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>使用 IDropTarget 介面啟用處理常式

動態資料交換 (的 DDE) 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。 **IDropTarget** 更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟動。 如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。 此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。 這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。

如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。

### <a name="specifying-the-position-and-order-of-static-verbs"></a>指定靜態動詞命令的位置和順序

通常動詞命令會根據其列舉方式在快捷方式功能表上排序;列舉是根據關聯陣列的順序，接著是關聯陣列中專案的順序，如登錄的排序次序所定義。

您可以針對關聯專案指定 Shell 子機碼的預設值來排序動詞。 這個預設值可以包含單一專案，這會顯示在快捷方式功能表的頂端位置，或是以空格或逗號分隔的專案清單。 在後者的情況下，清單中的第一個專案是預設專案，而其他動詞會依照指定的順序顯示在其下方。

例如，下列登錄專案會依下列順序產生快捷方式功能表動詞：

1.  顯示
2.  小工具
3.  個人化

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

同樣地，下列登錄專案會依下列順序產生快捷方式功能表動詞：

1.  個人化
2.  小工具
3.  顯示

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>將動詞放置於功能表頂端或底部

下列登錄屬性可以用來將動詞放置在功能表的頂端或底部。 如果有多個動詞指定此屬性，則最後一個會取得優先順序：

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>建立靜態串聯功能表

在 Windows 7 （含）以後版本中，透過登錄設定支援串聯功能表的執行。 在 Windows 7 之前，只能透過 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面的執行來建立串聯功能表。 在 Windows 7 （含）以後版本中，您應該只在靜態方法不足時，才需要採用以 COM 程式碼為基礎的解決方案。

下列螢幕擷取畫面提供串聯功能表的範例。

![顯示級聯功能表範例的螢幕擷取畫面](images/file-assoc/filecascademenu2ndex.png)

在 Windows 7 和更新版本中，有三種方式可以建立串聯功能表：

-   [使用子命令登錄專案建立串聯式功能表](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [使用 IExplorerCommand 介面建立串聯式功能表](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>使用子命令登錄專案建立串聯式功能表

在 Windows 7 （含）以後版本中，您可以使用下列程式，使用子命令專案來建立串聯功能表。

**使用子命令專案建立串聯功能表**

1.  在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。 在此範例中，我們會為此子機碼命名為 *CascadeTest*。 請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。 在此範例中，我們將它指派為「測試 Cascade 功能表」。

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的子命令專案，這個專案是由分號所指派的動詞命令（以分號 demlimited），並以外觀順序顯示。 例如，我們在這裡指派了許多系統提供的動詞：

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  在自訂動詞命令的情況下，請使用任何靜態動詞實方法來加以執行，並在 **CommandStore** 子機碼底下列出它們，如下列虛構動詞 *VerbName* 的範例所示：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> 這個方法的優點是，自訂動詞命令可以註冊一次，並藉由列出子命令專案下的動詞名稱重複使用。 但是，應用程式需要有許可權才能修改 **HKEY \_ 本機 \_ 電腦** 下的登錄。

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表

在 Windows 7 和更新版本中，您可以使用 ExtendedSubCommandKey 專案來建立擴充的串聯功能表：串聯功能表中的串聯功能表。

下列螢幕擷取畫面是延伸串聯功能表的範例。

![顯示裝置的擴充串聯功能表的螢幕擷取畫面](images/file-assoc/extendedsubcommandskey.png)

由於 **HKEY \_ 類別 \_ 根目錄** 是 **HKEY \_ 目前 \_ 使用者** 和 **HKEY \_ 本機 \_ 電腦** 的組合，因此您可以在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼下註冊任何自訂動詞。 這麼做的主要優點是不需要提高許可權。 此外，其他檔案關聯也可以藉由指定相同的 ExtendedSubCommandsKey 子機碼，重複使用這整組動詞。 如果您不需要重複使用這組動詞，可以列出父系底下的動詞命令，但是確定父系的預設值是空的。

**使用 ExtendedSubCommandsKey 專案建立串聯功能表**

1.  在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。 在此範例中，我們會為此子機碼命名為 *CascadeTest2*。 請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。 在此範例中，我們將它指派為「測試 Cascade 功能表」。

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  在您所建立的 *CascadeTest* 子機碼底下，新增 **ExtendedSubCommandsKey** 子機碼，然後將 (**REG \_ SZ** 類型的檔子命令新增) ; 例如：

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    確定 [ *測試串聯功能表 2* ] 子機碼的預設值是空的，而且顯示為 [ **未設定) 的 (值**]。

4.  使用下列任何靜態動詞命令來填入 subverbs。 請注意，CommandFlags 子機碼代表 EXPCMDFLAGS 值。 如果您想要在 cascade 功能表項目之前或之後加入分隔符號，請使用 ECF \_ SEPARATORBEFORE (0x20) 或 ECF \_ SEPARATORAFTER (0x40) 。 如需這些 Windows 7 及更新版本旗標的說明，請參閱 [**IExplorerCommand：： GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags)。 ECF \_ SEPARATORBEFORE 僅適用于最上層的功能表項目。 MUIVerb 的類型為 **reg \_ SZ**，而 CommandFlags 的類型為 **reg \_ DWORD**。

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

下列螢幕擷取畫面是先前的登錄機碼專案範例的圖例。

![顯示顯示 [記事本] 和 [wordpad] 選項之級聯功能表範例的螢幕擷取畫面](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>使用 IExplorerCommand 介面建立串聯式功能表

將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。 這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。 在 Windows 7 （含）以後版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 來提供相同的動詞實行，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)一樣。

以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/filecascademenu.png)

下列螢幕擷取畫面說明 [ **裝置** ] 資料夾中串聯功能表的另一個執行。

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadedevices2.png)

> [!Note]  
> 因為 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 僅支援同進程啟用，所以建議您在需要于命令和快捷方式功能表之間共用執行的 Shell 資料來源使用。

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>使用 Advanced Query 語法取得靜態動詞命令的動態行為

Advanced Query 語法 (AQS) 可以表達要使用為其具現化動詞之專案的屬性進行評估的條件。 這個系統只適用于快速屬性。 這些是 Shell 資料來源回報的屬性，不會從 [**IShellFolder2：： GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)傳回 [* * * * SHCOLSTATE \_ 慢 *](/windows/win32/api/shtypes/ne-shtypes-shcolstate) * * *。

Windows 7 和更新版本支援可避免當地語系化組建問題的標準值。 當地語系化的組建需要下列標準語法，才能利用此 Windows 7 增強功能。

``` syntax
System.StructuredQueryType.Boolean#True
```

在下列範例登錄專案中：

-   **AppliesTo** 值會控制是否要顯示或隱藏動詞。
-   DefaultAppliesTo 值控制預設的動詞命令。
-   HasLUAShield 值會控制是否顯示使用者帳戶控制 (UAC) 盾牌。

在此範例中， **DefaultAppliesTo** 值會讓這個動詞成為其檔案名中有 "exampleText1" 這個字的任何檔案的預設值。 **AppliesTo** 值會啟用名稱中有 "exampleText1" 之任何檔案的動詞。 **HasLUAShield** 值會顯示名稱中有 "exampleText2" 的檔案盾牌。

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

新增 **命令** 子機碼和值：

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

在 Windows 7 登錄中，請參閱 **HKEY \_ 類別 \_ 根** \\ **磁片磁碟機** 作為使用下列方法的 bitlocker 動詞範例：

-   AppliesTo = BitlockerProtection： = 2
-   BitlockerRequiresAdmin： = StructuredQueryType。布林 \# 值 True

如需 AQS 的詳細資訊，請參閱 [Advanced Query 語法](../search/-search-3x-advancedquerysyntax.md)。

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>已淘汰：將動詞與動態資料交換命令建立關聯

DDE 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。 DDE 已被取代，因為它依賴廣播視窗訊息來探索 DDE 伺服器。 DDE 伺服器會停止回應廣播視窗訊息，因此會讓其他應用程式的 DDE 交談停止回應。 單一停滯的應用程式通常會在使用者的體驗中造成後續的停止回應。

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)方法更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟用。 如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。 此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。 這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。

如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。

## <a name="completing-verb-implementation-tasks"></a>完成動詞執行工作

下列用來執行動詞命令的工作，與靜態和動態動詞命令都有關。 如需動態動詞命令的詳細資訊，請參閱 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)。

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>自訂預先定義之 Shell 物件的快捷方式功能表

許多預先定義的 Shell 物件都具有可自訂的快捷方式功能表。 註冊命令的方式與註冊一般檔案類型的方式非常類似，但請使用預先定義的物件名稱做為檔案類型名稱。

預先定義的物件清單位於 [建立 Shell 延伸模組處理常式](handlers.md)的 *預先定義 Shell 物件* 區段中。 這些預先定義的 Shell 物件，其快捷方式功能表可透過在登錄中新增動詞來自訂，並在包含單字動詞的表格中標示。

### <a name="extending-a-new-submenu"></a>擴充新的子功能表

當使用者在 Windows 檔案總管中開啟 [檔案 **] 功能表時** ，其中一個顯示的命令是 [ **新增**]。 選取此命令會顯示子功能表。 依預設，子功能表包含兩個命令： **資料夾** 和 **快捷方式**，可讓使用者建立子資料夾和快捷方式。 您可以擴充此子功能表，以包含任何檔案類型的檔案建立命令。

若要將檔案建立命令新增至 **新** 的子功能表，您的應用程式檔必須有相關聯的檔案類型。 在檔案名下包含 **ShellNew** 子機碼。 選取 [檔案 **] 功能表的** [ **新** 命令] 時，Shell 會將檔案類型加入至 **新** 的子功能表。 命令的顯示字串是指派給程式 ProgID 的描述性字串。

若要指定檔案建立方法，請將一或多個資料值指派給 **ShellNew** 子機碼。 下表列出可用的值。



| ShellNew 子機碼值 | Description                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 命令               | 執行應用程式。 這個 **REG \_ SZ** 值會指定要執行之應用程式的路徑。 例如，您可以將它設定為啟動 wizard。                  |
| 資料                  | 建立包含指定資料的檔案。 這個 **REG \_ 二進位** 值會指定檔案的資料。 如果指定了 **NullFile** 或 **FileName** ，則會忽略 **資料**。 |
| FileName              | 建立檔案，該檔案為指定檔案的複本。 這個 **REG \_ SZ** 值會指定要複製之檔案的完整路徑。                                   |
| NullFile              | 建立空白檔案。 **NullFile** 尚未指派值。 如果指定 **NullFile** ，則會忽略 **資料** 和 **檔案名** 登錄值。                    |



 

下列登錄機碼範例和螢幕擷取畫面說明 myp-ms 檔案類型的 **新** 子功能表。 它有一個 **Myprogram.exe 應用程式** 命令。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

螢幕擷取畫面說明 **新** 的子功能表。 當使用者從 **新** 的子功能表選取 **myprogram.exe 應用程式** 時，Shell 會建立名為 **New myprogram.exe myp 的** 檔案，並將它傳遞至 **MyProgram.exe**。

![windows explorer 的螢幕擷取畫面，在 [新增] 子功能表上顯示新的 [myprogram.exe 應用程式] 命令](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>建立拖放處理常式

執行拖放處理常式的基本程式與傳統快捷方式功能表處理常式的基本程式相同。 不過，快捷方式功能表處理常式通常只會使用傳遞給處理常式之 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標，來將物件的名稱解壓縮。 拖放處理常式可以執行更複雜的資料處理程式來修改拖曳物件的行為。

當使用者以滑鼠右鍵按一下 Shell 物件來拖曳物件時，會在使用者嘗試卸載物件時顯示快捷方式功能表。 下列螢幕擷取畫面說明典型的拖放快捷方式功能表。

![拖放快捷方式功能表的螢幕擷取畫面](images/context-menu/context-dragdrop.png)

拖放處理常式是快捷方式功能表處理常式，可將專案加入這個快捷方式功能表。 拖放處理常式通常會在下列子機碼下註冊。

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

在名為的拖放處理常式的 **DragDropHandlers** 子機碼下新增子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串形式 (CLSID) GUID。 下列範例會啟用 **MyDD** 拖放處理常式。

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>隱藏動詞和控制可見度

您可以使用 Windows 原則設定來控制動詞可視性。 藉由將 **SuppressionPolicy** 值或 **SuppressionPolicyEx** GUID 值新增至動詞的登錄子機碼，就可以透過原則設定來隱藏動詞命令。 將 **SuppressionPolicy** 子機碼的值設定為原則識別碼。 如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。 如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。

### <a name="employing-the-verb-selection-model"></a>採用動詞選取模型

您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。 針對此動詞支援的三種情況，動詞都需要個別的登錄值。 動詞選取模型的可能值如下：

-   指定所有動詞的 MultiSelectModel 值。 如果未指定 MultiSelectModel 值，則會從您選擇的動詞執行類型推斷。 針對以 COM 為基礎的方法 (例如 DropTarget 和 ExecuteCommand) **播放** 程式，並假設為其他方法 **檔** 。
-   針對僅支援單一選取專案的動詞指定 **single** 。
-   針對支援任意數量專案的動詞指定 **播放** 程式。
-   針對每個專案建立最上層視窗的動詞命令指定 **檔** 。 這麼做會限制啟用的專案數目，如果使用者開啟太多視窗，則有助於避免系統資源不足。

當選取的專案數目不符合動詞選取模型，或大於下表所述的預設限制時，就無法顯示該動詞。



| 動詞執行的類型 | 文件 | 播放器    |
|-----------------------------|----------|-----------|
| 舊版                      | 15個專案 | 100專案 |
| COM                         | 15個專案 | 沒有限制  |



 

以下是使用 MultiSelectModel 值的範例登錄專案。

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>使用專案屬性

您可以測試專案之 Shell 屬性的 [**SFGAO**](sfgao.md) 旗標值，以判斷是否應啟用或停用動詞。

若要使用此屬性功能，請在下列動詞命令底下新增下列 **REG \_ DWORD** 值：

-   AttributeMask 值會指定要測試之遮罩的位值 [**SFGAO**](sfgao.md) 值。
-   AttributeValue 值會指定所測試之位的 [**SFGAO**](sfgao.md) 值。
-   ImpliedSelectionModel 為專案動詞指定零，或在背景快捷方式功能表上指定非零的動詞。

在下列範例登錄專案中，AttributeMask 會設定為 [**SFGAO \_ READONLY**](sfgao.md) (0x40000) 。

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>透過 Desktop.ini 為資料夾執行自訂動詞

在 Windows 7 和更新版本中，您可以透過 Desktop.ini 將動詞新增至資料夾。 如需 Desktop.ini 檔案的詳細資訊，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。

> [!Note]  
> Desktop.ini 的檔案應該一律標示為  +  **隱藏** 系統，使其不會顯示給使用者。

 

**若要透過 Desktop.ini 檔案新增資料夾的自訂動詞命令，請執行下列步驟：**

1.  建立標示為 **唯讀** 或 **系統** 的資料夾。
2.  建立包含的 Desktop.ini 檔案 \[ 。ShellClassInfo \] DirectoryClass = Folder ProgID。
3.  在登錄中，建立具有值 CanUseForDirectory 的 **HKEY \_ 類別 \_ 根** \\ **資料夾 ProgID** 。 CanUseForDirectory 值可避免誤用未設定為透過 Desktop.ini 為資料夾執行自訂動詞命令的 Progid。
4.  在 **資料夾** ProgID 子機碼底下新增動詞，例如：

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> 這些動詞命令可以是預設動詞，在此情況下，按兩下資料夾會啟動動詞。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速鍵功能表處理常式和多重選取動詞的最佳作法](verbs-best-practices.md)
</dt> <dt>

[為快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)
</dt> <dt>

[使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[動詞和檔案關聯](fa-verbs.md)
</dt> <dt>

[快速鍵功能表參考](context-menu-reference.md)
</dt> </dl>

 

 
