---
description: 登錄中的硬式編碼字串儲存體是預先 Windows Vista 當地語系化模型的一部分。
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: 使用登錄字串重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bac55f59bd414002f5dcc0ce3611102a4effd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887403"
---
# <a name="using-registry-string-redirection"></a>使用登錄字串重新導向

登錄中的硬式編碼字串儲存體是預先 Windows Vista 當地語系化模型的一部分。 MUI 不支援此功能。 在目前的模型中，作業系統的使用者介面會在語言中立的基底之上，以特定語言的資源檔執行。 作業系統的元件會以非語言相關的方式使用登錄。

MUI 只會使用基底語言資源檔中的 Win32 PE 資源所定義的重新導向登錄字串。 重新導向是個別定義，例如在 .inf 檔案中。 這種類型的儲存體可讓資源載入器在資源模組載入期間自動選取正確的語言資源。

> [!Note]  
> 本主題僅適用于 Win32 PE 資源。 如果使用非 Win32 PE 資源，您必須提供自訂的登錄字串重新導向（如有需要）。

 

## <a name="create-a-language-neutral-resource"></a>建立 Language-Neutral 資源

在 Windows Vista 和更新版本上執行的 MUI 應用程式會使用中性語言的字串資源，以允許存取儲存在字串資源資料表中的特定語言字串。 從登錄中讀取這些值的應用程式程式碼會在 [尋找重新導向字串](locating-redirected-strings.md)的 [載入 Language-Neutral 登錄值] 區段中描述。

語言中立登錄值的資料格式為 " `@<PE-path>,-<stringID>[;<comment>]` "，其中：

-   *PE 路徑* 指定可執行檔的路徑。 您可以使用環境變數（例如% ProgramFiles%）來指定路徑，以支援部署。 進行字串參考的替代方法是省略檔案路徑資訊。 在此情況下，您的應用程式必須有一些方法（例如，另一個登錄值），才能傳達自己的安裝目錄。
-   *stringid 指定* 會指定相關字串資源的數值資源識別碼，其執行方式就像任何其他可當地語系化的字串資源。
-   *批註* 會指定選擇性的資訊來進行偵錯工具或登錄值的可讀性。 登錄 API 函數會在載入字串時忽略批註。

> [!Note]  
> 登錄值的資料不會明確參考特定語言的資源檔。 根據目前的使用者介面語言喜好設定，在執行時間決定正確的檔案。

 

輸入的登錄值不會有 "，" 和 "-" 之間的空格。 正確的登錄值為：

`shell32.dll,-22912`

不正確的登錄值為：

`shell32.dll, -22912`

Windows Vista 的範例是具有下列資料的登錄值：

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>建立快捷方式字串的資源

當 MUI 應用程式在 shell 使用者介面中顯示其名稱時，會顯示應用程式圖示的提示字元字串。 針對每個支援的語言，您應該建立應用程式顯示名稱和相關聯的提示字元字串的字串資源。 當資源就緒時，您的應用程式可以使用在 [尋找重新導向字串](locating-redirected-strings.md)的登錄區段中，使用 Shell API 中所述的字串來載入快速鍵字串。

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>準備使用 Windows Installer 建立之快捷方式的資源

如果您使用 Windows Installer (MSI) 建立快捷方式，則字串資源會包含快捷方式顯示名稱和描述。 在 [MSI 快速鍵資料表](../msi/shortcut-table.md)中，資源 DLL 會在適當的資料行中參考，而快速鍵顯示名稱和描述的資源識別碼則會用於對應的資源識別碼資料行。

為了讓應用程式快捷方式可與 MUI 資源技術正常搭配運作，請在準備快速鍵字串時記住下列幾點：

-   請使用環境變數或相對路徑來註冊 DLL。 您可以指定 @% systemroot% \\ system32shell32.dll，只要登錄 \\ 字串類型為 REG \_ EXPAND SZ 即可 \_ 。 Shell32.dll 中「文字檔」的字串資源識別碼為12345。
-   請勿在 "，" 和 "-" 符號前後使用空格。 正確的範例是 "shell32.dll，-22912"。
-   請勿使用簡短的檔案名。 此類型的名稱不適用於資源載入器。

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>使用 INF 格式準備快速鍵的資源

如果您使用 INF 檔案格式來建立快捷方式字串，資源檔應該進行下列登錄設定。 這些指示假設您使用的是安裝程式 API 的 ProfileItems 語法。

1.  使用路徑和資源識別碼，將 [提示] 值變更為指向 [字串重新導向參考]。
2.  在 ProfileItems 安裝區段底下新增值 DisplayResource。

下列範例顯示如何將計算機應用程式新增至 [ **開始** ] 功能表：


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



使用 INF 將專案（例如存取群組資料夾）新增至 [ **開始** ] 功能表時，請使用如下所示的語法。 此語法假設 \[ \] 從安裝程式使用 StartMenuItems 支援，類似于 Syssetup 中使用的語法。


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



將 *[值]* 提示字元設定為字串參考 " `@<path>,-resID` "。

顯示名稱取決於 *resDLL* 和 *resID* 值。 *ResID* 值會指定與非語言相關檔案相關聯之字串資源的資源識別碼。 *ResDLL* 值指定非語言相關檔案的路徑。

## <a name="create-resources-for-friendly-document-type-names"></a>建立易記檔案類型名稱的資源

您必須將應用程式的易記名稱和提示字元字串作為字串資源來執行。 若要允許易記的檔案類型名稱回應使用者介面語言，應用程式必須在檔案類型的程式識別碼機碼下，使用 FriendlyTypeName 值來註冊名稱。 應該保留程式識別碼金鑰的預設值，以維持回溯相容性。 如需從應用程式存取名稱的詳細資訊，請參閱 [尋找重新導向字串](locating-redirected-strings.md)之登錄區段中的查詢易記檔案類型名稱。

特定工作牽涉到下列步驟：

1.  將易記名稱和提示字串實作為特定語言的字串資源。
2.  在 [檔案類型] 登錄機碼底下新增 FriendlyTypeName 值。 值的資料會在模式 "" 之後 `@<path>,-<resID>` ，其中 *path* 表示可執行檔，而 *resID* 是與該可執行檔相關聯之可當地語系化字串資源的資源識別碼。
3.  根據 "" 格式指定提示登錄值 `@<path>,-<resID>` 。

下列範例顯示 .txt 檔的登錄設定：


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>提供 Shell 動詞動作字串的資源

特定動詞的動作字串（例如「開啟」和「編輯」）會顯示在使用者以滑鼠右鍵按一下 Windows 檔案總管中的檔案時顯示的快顯功能表中。 您的應用程式不需要指定常用 shell 動詞命令的字串，因為 shell 針對這些動詞電腦有其具有 MUI 功能的預設值。 不過，您應該為代表不尋常動詞的字串提供可當地語系化的字串資源。

在預先 Windows XP 作業系統上，會使用下列語法來轉譯登錄中 shell 動詞命令的字串，其中 *verb* 會指定實際的動詞名稱：


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



以下為範例：


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



在 Windows XP 和更新版本上，您可以使用一層間接取值來讓動作字串相依于使用者介面語言。 這些作業系統支援 MUIVerb 值來定義與 MUI 相容的字串。 以下是非常見動詞命令的登錄專案範例：


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



您的 MUI 應用程式也應該能夠將舊的預設值註冊為可當地語系化的字串，如下所示：


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> 不建議您註冊舊的預設值，因為它需要 Windows XP 和更新版本上的不同安裝程式，而不是舊版作業系統上所使用的安裝程式。

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>建立動詞、通訊協定和 AuxUserType 字串的資源

您應該為動詞、Protocol 和 AuxUserType 字串建立可當地語系化的字串資源。 使用下列登錄設定：


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



針對 >localizedstring 指定的值只會包含或取代您的 *動詞* 值（而不是兩個旗標值）。

以下是可協助您確保正確登錄設定的摘要：

-   如果 CLSID 有 HKCR \\ clsid \\ {clsid} 的 [插入] 索引 \\ 鍵，請使用 HKCR \\ CLSID \\ {clsid} >LOCALIZEDSTRING \\ 來定義預設的 clsid 值。
-   如果 CLSID 在 HKCR clsid {clsid} 動詞下有一或多個子機碼 \\ \\ \\ ，請使用 HKCR \\ CLSID \\ {clsid} \\ 動詞 \\ xxx \\ >localizedstring 來定義每個個別的動詞字串。
-   如果 CLSID 在 HKCR {progid} protocol Stdfileediting 動詞下有一或多個子機碼 \\ \\ \\ \\ ，請使用 HKCR \\ {progid} \\ protocol \\ Stdfileediting \\ Verb \\ xxx >localizedstring \\ 來定義每個個別的動詞字串。
-   如果 CLSID 在 HKCR clsid {clsid} AuxUserType 下有一或多個列出的 AuxUserType 子機碼 \\ \\ \\ ，請使用 HKCR \\ CLSID \\ {clsid} \\ AuxUserType \\ xxx \\ >localizedstring 來定義每個 AuxUserType 專案。

## <a name="create-a-resource-for-the-uninstall-program"></a>建立卸載程式的資源

若要註冊應用程式的卸載程式，您可以在登錄機碼 HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ uninstall 下，于應用程式的唯一識別碼子機碼中建立登錄值。 要設定的值包括： DisplayName、DisplayVersion、Publisher、ProductID、RegOwner、RegCompany、UrlInfoAbout、HelpTelephone、HelpLink、InstallLocation、InstallSource、InstallDate、Contact、comment、DisplayIcon、Readme、UrlUpdateInfo。

> [!Note]  
> 若要啟用每個值的 MUI 技術，您可以在值名稱中附加「 \_ 當地語系化」。

 

需要作業系統元件才能針對 \_ 以 MUI 為特定的方式當地語系化的 DisplayName 提供值。 假設識別碼是1245，您應該將顯示名稱放在 DLL 中，例如 Res.dll，作為字串資源。 然後，應用程式可以將顯示名稱註冊為 \_ 使用 "@ \\res.DLL，-1245" 值當地語系化的 DisplayName。 所有其他的登錄設定都應該保持不變，包括 DisplayName 的原始值。

## <a name="create-resources-for-sound-events"></a>建立音效事件的資源

Windows 將某些事件與音效檔產生關聯，例如新的郵件通知事件或重大電池警示事件。 事件名稱必須由使用者介面顯示，且必須支援全球化。 因此，您應該針對每個事件描述的描述，執行可當地語系化的字串資源。 針對每個事件名稱新增一個新的登錄值，以及硬式編碼的預設值。

執行下列動作來啟用音效事件：

1.  將描述實作為可當地語系化的字串資源。
2.  除了硬式編碼的預設值外，還會為顯示名稱加入新的登錄值。 相關聯的登錄配置如下所示：


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



如果 shell 找不到或無法取出 DispFileName 的值，則會使用預設描述。

## <a name="create-resources-for-keyboard-layout-strings"></a>建立鍵盤配置字串的資源

如果您的應用程式會執行鍵盤配置，則需要可當地語系化的字串資源作為螢幕顯示配置的名稱，例如，在鍵盤配置的清單中。 每個鍵盤配置都有一個登錄機碼，位於 HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ 鍵盤版面配置。

該索引鍵的值包括版面配置文字、可供回溯相容的人們看得懂的名稱，以及版面配置顯示名稱。 針對版面配置顯示名稱提供的資料應該是 "" 格式的字串參考 `@<path>,-resID` ，參考與鍵盤配置相關聯的可當地語系化字串資源。

以下是西班牙文 (西班牙) 鍵盤配置的登錄設定範例：

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>代表 OLE 插入物件的通用對話方塊字串

您可以將 OLE 可插入物件的顯示名稱，作為與執行該物件之程式碼相關聯的可當地語系化字串資源。 [ [OLE 插入物件] 對話方塊](/cpp/mfc/reference/coleinsertdialog-class)會從登錄機碼 HKCR \\ CLSID \\ {*&lt; GUID &gt;*} 取得顯示名稱，其中 *GUID* 會識別可插入之 OLE 物件的類別識別碼。 WindowsVista 和更新版本會以可當地語系化的方式來執行這種類型的物件，並使用符合 MUI 規範的顯示名稱來自訂使用者介面語言。 相反地，預先 Windows Vista 作業系統會使用對應的登錄機碼的預設值來執行這種類型物件的顯示名稱。 此名稱通常是英文 (美國) 名稱或系統預設 UI 語言中的名稱。

> [!Note]  
> 並非所有對應到登錄機碼子機碼的物件都是可插入的。

 

HKCR \\ CLSID \\ {*&lt; &gt; GUID*} 金鑰的預設值應該保留人們可讀取的名稱，以提供回溯相容性。 不過，它也應該以 "" 格式來定義 >localizedstring 值， `@<path>,-ResID` 其中路徑會識別執行物件的可執行檔。 ResID 值會為顯示名稱指定可當地語系化字串的資源識別碼。

例如，可插入媒體剪輯物件的註冊腳本包含下列幾行：


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



第一行提供回溯相容性，方法是將簡單的文字字串放在登錄中作為預設的顯示名稱。 第二行提供 MUI 相容顯示名稱的存取權。 指出儲存在 Mplay32.exe 中的字串識別碼。 Mplay32.exe 中識別碼為9217的字串可以與任意數目語言的字串資源值產生關聯。 其英文 (美國) 名稱是「媒體剪輯」。

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>建立 Microsoft Management Console Snap-Ins 的字串資源

您應該為您的 MUI 應用程式所使用的每個 Microsoft Management Console (MMC) 嵌入式管理單元建立可當地語系化的字串資源。 因為嵌入式管理單元是主控台的一部分，所以它具有使用者介面，且必須經過全球化才能以多種語言運作。

大部分的情況下，MMC 嵌入式管理單元會引發與 MUI 應用程式本身相同的全球化和當地語系化問題。 MMC 嵌入式管理單元必須反映其在登錄中的名稱以供顯示。 登錄專案應該包含可當地語系化字串資源的間接參考，以及回溯相容性的常值字串。

每個 MMC 嵌入式管理單元都有一個登錄機碼，位於 HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MMC \\ 嵌入式管理單元。 該索引鍵的值會 NameString，指定可讀的名稱以提供回溯相容性，而 NameStringIndirect 則指定可當地語系化字串資源的間接參考。 針對 NameStringIndirect，您應該提供 "" 格式的字串參考 `@<path>,-resID` ，代表可當地語系化的字串資源。

例如，您可能會為 Mymmc.dll 進行下列設定，其中12345是對應字串資源的識別碼，其中包含嵌入式管理單元的可當地語系化名稱：


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



某些嵌入式管理單元會註冊 MMC 不會從登錄讀取的其他登錄字串值。 如需有關使用這些值的詳細資訊，請參閱註冊 Microsoft Management Console Snap-In 在 [尋找重新導向的字串](locating-redirected-strings.md)時無法從登錄讀取的字串。

## <a name="create-string-resources-for-a-windows-service"></a>建立 Windows 服務的字串資源

雖然 Windows 服務通常沒有任何使用者介面，但它必須顯示符合 mui 規範的名稱，而且通常會提供符合 mui 規範的語言特定描述。 描述 Windows 服務的登錄機碼只支援服務名稱的 DisplayName 值和服務描述的描述值。

從應用程式進行 Windows 服務的設定，如在[尋找重新導向的字串](locating-redirected-strings.md)中從登錄設定 Windows 服務的顯示名稱和描述所述。 如果您的應用程式未設定服務使用者介面的登錄值，則登錄中的值仍會設定為 [英文]，即使使用者介面是另一種語言。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[準備資源](preparing-resources.md)
</dt> <dt>

[尋找重新導向的字串](locating-redirected-strings.md)
</dt> </dl>

 

 
