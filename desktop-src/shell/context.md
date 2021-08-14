---
description: 以滑鼠右鍵按一下物件，通常會顯示快捷方式功能表。 此功能表包含使用者可選取的命令清單，可在物件上執行各種動作。 本節是檔案系統物件的快捷方式功能表簡介。
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: 擴充快速鍵功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460645"
---
# <a name="extending-shortcut-menus"></a>擴充快速鍵功能表

以滑鼠右鍵按一下物件，通常會顯示 *快捷方式功能表*。 此功能表包含使用者可選取的命令清單，可在物件上執行各種動作。 本節是檔案系統物件的快捷方式功能表簡介。

-   [檔案系統物件的快捷方式功能表](#shortcut-menus-for-file-system-objects)
-   [快速鍵功能表動詞](#shortcut-menu-verbs)
    -   [標準動詞](#canonical-verbs)
    -   [擴充的動詞](#extended-verbs)
-   [擴充檔案類型的快捷方式功能表](#extending-the-shortcut-menu-for-a-file-type)
-   [擴充預先定義之 Shell 物件的快捷方式功能表](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [註冊應用程式以處理任意檔案類型](#registering-an-application-to-handle-arbitrary-file-types)
-   [擴充新的子功能表](#extending-the-new-submenu)

其他資訊可在這裡取得：

-   [如何定義擴充動詞](how-to-define-extended-verbs.md)
-   [如何建立動詞與 DDE 命令的關聯](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>檔案系統物件的快捷方式功能表

當使用者以滑鼠右鍵按一下顯示在 Windows 檔案總管或桌面上的物件（例如檔案）時，會出現快捷方式功能表，其中包含命令清單。 然後，使用者可以藉由選取適當的命令，在檔案上執行動作，例如開啟或刪除檔案。

因為快捷方式功能表通常用於檔案管理，所以 Shell 會提供一組預設的命令，例如剪下和複製，並顯示在任何檔案的快捷方式功能表上。 請注意，雖然 [開啟檔案] 是預設的命令，但是不會針對某些標準檔案類型（例如 .wav）顯示。 下列範例我的檔目錄的圖例，也用來作為 [自訂圖示](icon.md)的範例，會顯示以滑鼠右鍵按一下 MyDocs4.xyz 所顯示的預設快捷方式功能表。

![檔案系統物件的預設快捷方式功能表的螢幕擷取畫面](images/context1.jpg)

MyDocs4.xyz 顯示預設快捷方式功能表的原因是它不是已註冊 [檔案類型](fa-file-types.md)的成員。 另一方面，.txt 是已註冊的檔案類型。 如果您以滑鼠右鍵按一下其中一個 .txt 檔案，則會改為在上方區段中看到有另外兩個命令的快捷方式功能表： [ **開啟** ] 和 [ **列印**]。

![檔案系統物件的自訂快捷方式功能表的螢幕擷取畫面](images/context2.jpg)

註冊檔案類型之後，您可以使用其他命令來擴充其快捷方式功能表。 當以滑鼠右鍵按一下該類型的任何檔案時，它們會顯示在預設的命令上方。 雖然以這種方式新增的大部分命令都是常見的命令（例如 [ **列印** ] 或 [ **開啟**]），但您可以隨意新增任何使用者可能覺得有用的命令。

擴充檔案類型的快捷方式功能表所需的所有專案，都是為每個命令建立一個登錄專案。 更複雜的方法是執行 *快捷方式功能表處理常式*，它可讓您依檔案逐一擴充檔案類型的快捷方式功能表。 如需詳細資訊，請參閱 [建立快顯功能表處理常式](context-menu-handlers.md)。

## <a name="shortcut-menu-verbs"></a>快速鍵功能表動詞

快速鍵功能表上的每個命令都是由其 *動詞* 命令在登錄中識別。 這些動詞與 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 在以程式設計方式啟動應用程式時所使用的相同。 如需有關使用 **ShellExecuteEx** 的詳細資訊，請參閱 [啟動應用程式](launch.md)的討論。

動詞是簡單的文字字串，可供 Shell 用來識別相關聯的命令。 每個動詞命令都對應至用來在主控台視窗或批次 (.bat) 檔中啟動命令的 *命令字串* 。 例如， **open** 動詞通常會啟動程式來開啟檔案。 它的命令字串通常看起來像這樣：

``` syntax
"My Program.exe" "%1"
```

"%1" 是檔案名所提供之命令列參數的標準預留位置。 例如，它可以指定要顯示在索引標籤式視圖中的特定頁面。

> [!Note]  
> 如果命令字串的任何元素包含或可能包含空格，則必須以引號括住。 否則，如果元素包含空格，將無法正確剖析。 比方說，「我的 Program.exe」會正確啟動應用程式。 如果您使用我的 Program.exe，系統會嘗試以 "Program.exe" 作為第一個命令列引數來啟動 "My"。 您應該一律使用引號，其中包含引數（例如 "%1"），並由 Shell 擴充為字串，因為您無法確定字串不會包含空格。

 

動詞也可以有相關聯的 *顯示字串* ，這會顯示在快捷方式功能表上，而不是動詞字串本身。 例如， **openas** 的顯示字串會以開啟。 如同一般的功能表字串，在顯示字串中包含 & 符號 (&) ，可讓您選擇鍵盤的命令。

### <a name="canonical-verbs"></a>標準動詞

一般情況下，應用程式會負責為其定義的動詞提供當地語系化的顯示字串。 不過，為了提供某種程度的語言獨立性，系統會定義一組標準的常用動詞，稱為標準 *動詞*。 標準動詞可以搭配任何語言使用，系統會自動產生適當當地語系化的顯示字串。 比方說， **開啟** 動詞的顯示字串將設定為在英文系統上開啟，並且在德文系統上Öffnen。

標準動詞包括：



| 值      | 描述                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| 開啟       | 開啟檔案或資料夾。                                                                   |
| opennew    | 在新視窗中開啟檔案或資料夾。                                                   |
| print      | 列印檔案。                                                                            |
| 探索    | 開啟 Windows 檔案總管，並選取資料夾。                                            |
| 尋找       | 開啟 [ **Windows Search** ] 對話方塊，並將資料夾設定為預設搜尋位置。 |
| openas     | 開啟 [ **開啟方式** ] 對話方塊。                                                         |
| properties | 開啟物件的屬性工作表。                                                          |



 

Printto 動詞也是標準的，但永遠不會顯示。 它可讓使用者將檔案拖曳至印表機物件來列印該檔案。

### <a name="extended-verbs"></a>擴充的動詞

當使用者以滑鼠右鍵按一下物件時，快捷方式功能表會包含所有一般動詞。 不過，可能會有您想要支援但未顯示在每個快捷方式功能表上的命令。 例如，您可能會有不常使用或適用于有經驗的使用者的命令。 基於這個理由，您也可以定義一或多個 *擴充動詞*。 這些動詞也是字元字串，類似于一般動詞。 它們是以其註冊方式與一般動詞的區別。 若要存取與擴充動詞相關聯的命令，使用者必須在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件。 擴充的動詞將會連同一般動詞一起顯示。

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>擴充檔案類型的快捷方式功能表

擴充檔案類型之快捷方式功能表最簡單的方式就是使用登錄。 若要這樣做，請在與 [檔案類型](fa-file-types.md)相關聯的應用程式 ProgID 的索引鍵下方新增 **Shell** 子機碼。 （選擇性）您可以為檔案類型定義 *預設動詞* ，方法是將它設為 **Shell** 子機碼的預設值。

預設動詞會先顯示在快捷方式功能表上。 其目的是在呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 時，提供 Shell 所能使用的動詞，但未指定任何動詞。 以這種方式使用 **ShellExecuteEx** 時，Shell 不一定會選取預設的動詞命令。 針對 shell [5.0 版](versions.md)和更新版本，在 Windows 2000 和更新版本的系統上找到，shell 會使用下列清單中第一個可用的動詞命令。 如果沒有可用的，則作業會失敗。

-   Open 動詞
-   預設動詞
-   登錄中的第一個動詞
-   Openwith 動詞

若為 [5.0 版](versions.md)之前的 Shell 版本，請省略第三個專案。

在 **Shell** 子機碼底下，為您要新增的每個動詞建立一個子機碼。 這些子機碼的每一個都會將 **REG \_ SZ** 值設定為動詞的顯示字串。 您可以省略標準動詞的顯示字串，因為系統會自動顯示適當的當地語系化字串。 如果您省略 noncanonical 動詞的顯示字串，將會顯示動詞字串。 針對每個動詞子機碼，建立 **命令** 子機碼，並將預設值設定為命令字串。

下圖顯示在 [檔案類型](fa-file-types.md) 中使用之 myp 檔案類型與 [自訂圖示](icon.md)的快捷方式功能表。 它現在會在其快捷方式功能表上提供開啟、doit r、列印和 printto 動詞，並以 doit r 作為預設動詞。 快捷方式功能表如下所示。

![自訂快捷方式功能表的螢幕擷取畫面](images/context3.jpg)

用來擴充上圖所示之快捷方式功能表的登錄專案如下：

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

雖然 **Open With** 命令高於第一個分隔符號，但它會由系統自動建立，且不需要登錄專案。 系統會自動建立標準動詞開啟和列印的顯示名稱。 因為 doit r 不是標準的動詞命令，所以會將顯示名稱指派為「&這麼做」，只要按 D 鍵就可以選取它。 Printto 動詞命令不會出現在快捷方式功能表上，但包含它可讓使用者藉由將檔案放在印表機圖示上來列印檔案。 在此範例中，%1 代表檔案名和 %2 印表機名稱。

藉由將 SuppressionPolicy 值新增至動詞鍵，即可透過原則設定來隱藏動詞。 將 SuppressionPolicy 的值設定為原則識別碼。 如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。 如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>擴充預先定義之 Shell 物件的快捷方式功能表

許多預先定義的 Shell 物件都有可延伸的快捷方式功能表。 註冊命令的方式與註冊一般檔案類型的方式非常類似，但請使用預先定義的物件名稱做為檔案類型名稱。

預先定義的物件清單可以在 [建立 Shell 延伸模組處理常式](handlers.md)的 *預先定義 shell 物件* 區段中找到。 這些預先定義的 Shell 物件，其快捷方式功能表可透過在登錄中新增動詞來加以擴充，並以 "Verb" 這個字標示在資料表中。

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>註冊應用程式以處理任意檔案類型

本檔的前面幾節已經討論過如何定義特定檔案類型的快捷方式功能表項目。 此外，定義快捷方式功能表可讓您指定相關聯的應用程式如何開啟檔案類型的成員。 不過，如 [檔案類型](fa-file-types.md)中所述，當使用者嘗試使用您的應用程式開啟您未與應用程式建立關聯的檔案類型時，應用程式也可以註冊個別的預設程式。 本主題會在此討論，因為您註冊的預設程式與註冊快捷方式功能表項目的方式大致相同。

預設程式有兩個基本用途。 其中一個方法是指定應該如何叫用應用程式，以開啟任意檔案類型。 比方說，您可以使用命令列旗標來指出正在開啟未知的檔案類型。 另一個用途是定義檔案類型的各種特性，例如快捷方式功能表項目和圖示。 如果使用者將您的應用程式與其他檔案類型產生關聯，則該類型會具有這些特性。 如果其他檔案類型先前與另一個應用程式相關聯，這些特性將會取代原始的。

若要註冊預設程式，請將您為應用程式 ProgID 建立的登錄機碼放在 **HKEY \_ 類別 \_ 根** 應用程式的應用程式子機碼下 \\ ****。 您也可以包含 FriendlyAppName 值，為系統提供易記的應用程式名稱。 應用程式的易記名稱也可以從它的可執行檔中解壓縮，但只有在 FriendlyAppName 值不存在時。 下列登錄片段顯示 MyProgram.exe 的範例預設程式，可定義易記名稱和數個快捷方式功能表項目。 命令字串包含/a 旗標，以通知應用程式它正在開啟任意檔案類型。 如果您包含 **DefaultIcon** 子機碼，您應該使用一般圖示。

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>擴充新的子功能表

當使用者在 Windows 檔案總管中開啟 [檔案 **] 功能表時**，第一個命令是 [**新增**]。 選取此命令會顯示子功能表。 依預設，它包含兩個命令、 **資料夾** 和 **快捷方式**，可讓使用者建立子資料夾和快捷方式。 您可以擴充此子功能表，以包含任何檔案類型的檔案建立命令。

若要將檔案建立命令新增至 **新** 的子功能表，您的應用程式檔必須有相關聯的 [檔案類型](fa-file-types.md) 。 在副檔名的機碼底下包含 **ShellNew** 子機碼。 選取 [檔案] 功能表的 [**新** 命令] 時，Shell 會將它新增至 **新** 的 **子功能表。** 命令的顯示字串將會是指派給程式 ProgID 的描述性字串。

將一或多個資料值指派給 **ShellNew** 子機碼，以指定檔案建立方法。 可用的值如下。



| 值    | 描述                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 命令  | 執行應用程式。 這是 **REG \_ SZ** 值，可指定要執行之應用程式的路徑。 例如，您可以將它設定為啟動 wizard。 |
| 資料     | 建立包含指定資料的檔案。 資料是具有檔案資料的 **REG \_ 二進位** 值。 如果指定了 NullFile 或 FileName，則會忽略資料。  |
| FileName | 建立檔案，該檔案為指定檔案的複本。 FileName 是 **REG \_ SZ** 值，設定為要複製之檔案的完整路徑。                 |
| NullFile | 建立空白檔案。 未將值指派給 NullFile。 如果指定 NullFile，則會忽略資料和檔案名的值。                                  |



 

下圖顯示在 [檔案類型](fa-file-types.md)中用來做為範例的 myp 檔案類型的 **新** 子功能表，以及 [自訂圖示](icon.md)。 它現在有一個命令 **Myprogram.exe 應用程式**。 當使用者從 **新** 的子功能表選取 **myprogram.exe 應用程式** 時，Shell 會建立名為 "New myprogram.exe Application. myp" 的檔案，並將它傳遞給 MyProgram.exe。

![自訂 [新增] 功能表的螢幕擷取畫面](images/context5.png)

登錄專案現在如下所示：

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



