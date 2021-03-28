---
description: 本主題是可在自動播放 .inf 檔案中使用之專案的參考。 專案是由索引鍵和值所組成。
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: 自動播放 .inf 專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191186"
---
# <a name="autoruninf-entries"></a>自動播放 .inf 專案

本主題是可在自動播放 .inf 檔案中使用之專案的參考。 專案是由索引鍵和值所組成。

-   [\[自動運行機 \] 碼](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [圖示](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [shellexecute](#shellexecute)
    -   [殼](#autoruninf-entries)
    -   [shell \\ 動詞](#shellverb)
-   [\[內容 \] 金鑰](#content-keys)
-   [\[ExclusiveContentPaths 索引 \] 鍵](#exclusivecontentpaths-keys)
-   [\[IgnoreContentPaths 索引 \] 鍵](#ignorecontentpaths-keys)
-   [\[DeviceInstall 索引 \] 鍵](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[自動運行機 \] 碼

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [圖示](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [shellexecute](#shellexecute)
-   [殼](#autoruninf-entries)
-   [shell \\ 動詞](#shellverb)

### <a name="action"></a>動作

**動作** 專案會指定處理常式的 [自動播放] 對話方塊中所使用的文字，此處理程式代表媒體的 [自動執行] .inf 檔案中的 [open](#parameters)或 [shellexecute](#shellexecute)專案所指定的程式。 值可以是文字或以二進位格式儲存的資源。


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>參數

-   *ActionText*

    處理常式的 [自動播放] 對話方塊中所使用的文字，表示媒體的 [自動播放] 檔案中的 [open](#parameters) 或 [shellexecute](#shellexecute) 專案所指定的程式。

-   *filepath*

    字串，其中包含目錄的完整路徑，該目錄包含包含字串的二進位檔案。 如果未指定路徑，則檔案必須位於磁片磁碟機的根目錄中。

-   *filename*

    包含二進位檔案名稱的字串。

-   *Id*

    二進位檔案中的字串識別碼。

### <a name="remarks"></a>備註

**動作** 金鑰僅適用于 Windows XP Service Pack 2 (SP2) 或更新版本。 只有磁片磁碟機的磁片磁碟機卸載式 \_ 和磁片磁碟機 \_ 固定支援。 在卸載磁片磁碟機的情況下 \_ ，需要 **動作** 金鑰。 音訊 CD 或電影 DVD 的執行中 .inf 檔案中的 **動作** 命令會被忽略，而這些媒體會在 Windows XP Service Pack 1 (SP1) 和更早版本中繼續運作。

在 [自動播放] 對話方塊中顯示的字串，是藉由將 **動作** 專案中指定的文字與提供者的硬式編碼文字（由 Shell 所提供）結合在一起。 圖示旁邊會顯示 [圖示](#parameters) 。 此專案一律會顯示為 [自動播放] 對話方塊中的第一個選項，而且預設為選取。 如果使用者接受選項，則會啟動媒體的自動運行時檔案中的 [open](#parameters) 或 [shellexecute](#shellexecute) 專案所指定的應用程式。 在此情況下，[ **永遠執行選取的動作** ] 選項無法使用。

[動作](#parameters)和[圖示](#parameters)按鍵會定義使用者在 [自動播放] 對話方塊中看到的應用程式標記法。 它們應該以使用者可以輕鬆識別的方式來撰寫。 他們應該會指出要執行的應用程式、建立該應用程式的公司，以及任何相關聯的商標。

為了回溯相容性，對於磁片磁碟機類型的裝置而言， **動作** 專案是選擇性的 \_ 。 針對此類型，如果執行 .inf 檔案中沒有 **動作** 專案，則會在 [自動播放] 對話方塊中使用預設專案。

「 磁片磁碟機卸載」類型的裝置必須 \_ 要有動作專案，直到現在沒有支援 .inf 的支援。 如果沒有 **動作** 專案存在，則會顯示 [自動播放] 對話方塊，但沒有任何選項可啟動其他內容。

### <a name="customevent"></a>CustomEvent

**CustomEvent** 專案會指定自訂的自動播放內容事件。


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>參數

-   *CustomEventName*

    包含自動播放內容事件名稱的文字字串。 名稱不得超過100個英數位元。

### <a name="remarks"></a>備註

您可以在磁片區的 [自動播放] 檔案中包含自訂事件名稱。 當自動播放提示使用者將應用程式用於磁片區時，它只會顯示已針對指定的自訂事件名稱註冊的應用程式。 如需如何將應用程式註冊為自訂自動播放內容事件之處理常式的詳細資訊，請參閱 [使用自動播放自動啟動](/previous-versions/windows/apps/hh452731(v=win.10)) 或 [如何註冊事件處理常式](how-to-register-an-event-handler.md)。

下列範例會將 "MyContentOnArrival" 值指定為新的自動播放內容事件。


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

**圖示** 專案會指定代表 Windows 使用者介面中啟用自動啟用磁片磁碟機的圖示。


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>參數

-   *iconfilename*

    包含圖示資訊之 .ico、.bmp、.exe 或 .dll 檔案的名稱。 如果檔案包含一個以上的圖示，您也必須指定圖示的以零為基底的索引。

### <a name="remarks"></a>備註

圖示（連同標籤）表示 Windows 使用者介面中啟用自動啟動的磁片磁碟機。 例如，在 Windows 檔案總管中，磁片磁碟機是以這個圖示而非標準磁片磁碟機圖示來表示。 圖示的檔案必須與 [open](#parameters) 命令所指定的檔案位於相同的目錄中。

下列範例會指定 MyProg.exe 檔中的第二個圖示。


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

**標籤** 專案會指定文字標籤，表示 Windows 使用者介面中啟用自動啟用的磁片磁碟機。


```
label=LabelText
```



### <a name="parameters"></a>參數

-   *LabelText*

    包含標籤的文字字串。 它可以包含空格，而且不能超過32個字元。

> [!Note]  
> 您可以在 **LabelText** 參數中放入超過32個字元的值，而且不會收到任何錯誤訊息。 不過，系統只會顯示前32個字元。 第32之後的任何字元都會被截斷且不會顯示。 例如，如果 **LabelText** 如下所示：標籤 = 「此 CD 設計為終極音樂 cd」。 將會顯示下列「此 CD 設計成 ul」。

 

### <a name="remarks"></a>備註

標籤連同圖示，代表 Windows 使用者介面中啟用自動啟動的磁片磁碟機。

下列範例會將「我的磁片磁碟機標籤」值指定為磁片磁碟機的標籤。


```
label=My Drive Label
```



### <a name="open"></a>開啟

**開啟** 專案指定當使用者將光碟片插入磁片磁碟機時，自動啟動的應用程式路徑和檔案名。


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>參數

-   *exefile*

    插入光碟時執行之可執行檔的完整路徑。 如果只指定檔案名，它必須位於磁片磁碟機的根目錄中。 若要在子目錄中找出檔案，您必須指定路徑。 您也可以加入一或多個命令列參數，以傳遞至啟動應用程式。

### <a name="useautoplay"></a>UseAutoPlay

在 Windows XP 上， **UseAutoPlay** 專案指定應該使用自動播放，而不是自動播放。

在 Windows Vista （含）以後版本中，此專案會使用 [ **開啟** ] 或 [ **shellexecute** 專案]) ，從 [自動播放] 對話方塊中隱藏，導致任何針對自動執行 (指定的動作。 此專案對 Windows XP 之前的 Windows 版本沒有任何影響。

在 Windows 8 和更新版本上，指定值0將會停用此裝置的自動播放。

### <a name="parameters"></a>參數

若要使用此選項，請將 **UseAutoPlay** 的專案新增至執行 .inf 檔案，並將專案設定為等於1。 在 Windows 8 之前的 Windows 版本上，不支援其他的值。

在 Windows 8 和更新版本上，指定0的值以停用此裝置的自動播放。


```
UseAutoPlay=1
```



### <a name="remarks"></a>備註

目前， **UseAutoPlay** 僅適用于 Windows XP 或更新版本，且僅適用于 [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) 判斷為 **磁片磁碟機 \_ 光碟** 磁片磁碟機的磁片磁碟機。

使用 **UseAutoPlay** 時，windows XP 上的 **open** 或 **shellexecute** 專案所指定的任何動作都會被忽略，並在 Windows Vista 上的 [自動播放] 對話方塊中省略。

自動執行通常用來自動執行或載入插入的媒體上所含的某個內容，而 [自動播放] 則會顯示一個對話方塊，其中包含可能採取的相關動作清單，並可讓使用者選擇要採取的動作。 如需有關自動安裝和自動播放之間差異的詳細資訊，請參閱 [建立啟用自動啟動的 Cd-rom 應用程式](autoplay.md) ，並分別 [使用和設定自動播放](autoplay2k-using.md)。

### <a name="usage-example"></a>使用範例

CD 包含三個檔案：自動執行 .inf、Readme.txt 和 .wma。 視使用中的 Windows 版本和在 [自動執行] 中指定的選項而定，在插入光碟時，可以透過自動執行或自動播放來處理 CD (假設已為 CD 插入) 的磁片磁碟機啟用 [自動播放/自動播放]。

首先，請考慮具有下列內容的執行中 .inf 檔案，請注意未指定 **UseAutoPlay = 1** ：


```
[AutoRun]
shellexecute="Readme.txt"
```



插入此 CD 時，Shell 所採取的動作取決於使用中的 Windows 版本：

-   在 Windows XP 或更早版本上，此 CD 會在插入時由自動播放處理。 在此情況下，會讀取 **shellexecute** 專案，而且 Shell 會叫用與 .txt 檔案相關聯的檔案處理常式;這通常會在 [記事本] 中開啟 Readme.txt。
-   在 Windows Vista 中，具有 **shellexecute** 專案的自動播放 .inf 檔案，會將媒體識別為自動播放類型「軟體和遊戲」。 在此情況下，使用者會看到 [自動播放] 對話方塊，其中包含 **shellexecute** 專案所指定的動作 (在對話方塊中顯示為 [載入 Readme.txt]) ，以及與 [軟體和遊戲] 類型的媒體相關聯的預設動作。

若要指出應該使用 [自動播放]，而不是在 Windows XP 上執行，而且應該在 Windows Vista 上的 [自動播放] 對話方塊中隱藏 [自動執行 shellexecute] 專案指定的動作，請將 **UseAutoPlay** 插入至 [自動執行 .inf] 檔案，如下所示：


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



同樣地，當插入此 CD 時，Shell 所採取的動作會視使用中的 Windows 版本而定。

-   在 Windows XP 之前的 Windows 版本中，仍會使用自動執行，並執行 **shellexecute** 所指定的動作（如先前所述）。  (請注意，windows XP 之前的 Windows 版本只會提供自動執行時間。 ) 
-   在 Windows XP 上， **UseAutoPlay** 專案會導致自動播放用來取代自動播放。 在此情況下，自動播放會判斷媒體包含 Windows Media 音訊 ( .wma) 檔案，並將內容分類為「音樂檔案」。 使用者會看到 [自動播放] 對話方塊，其中包含「音樂檔案」自動播放媒體類型的已註冊處理常式。自動運行 shellexecute 專案會被忽略。

### <a name="shellexecute"></a>shellexecute

[版本5.0。](versions.md) **Shellexecute** 專案會指定自動執行將用來呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的應用程式或資料檔案。


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>參數

-   *filepath*

    字串，包含包含資料或可執行檔之目錄的完整路徑。 如果未指定路徑，則檔案必須位於磁片磁碟機的根目錄中。

-   *filename*

    字串，其中包含檔案的名稱。 如果是可執行檔，則會啟動它。 如果它是資料檔案，它必須是 [檔案類型](fa-file-types.md)的成員。 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 會啟動與檔案類型相關聯的預設命令。

-   *paramx*

    包含應傳遞給 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的任何其他參數。

### <a name="remarks"></a>備註

此專案類似于 [開啟](#parameters)，但它可讓您使用檔案 [關聯](fa-intro.md) 資訊來執行應用程式。

### <a name="shell"></a>殼層

**Shell** 專案會指定磁片磁碟機快捷方式功能表的預設命令。


```
shell=verb
```



### <a name="parameters"></a>參數

-   *動詞命令*

    對應至功能表命令的動詞命令。 動詞和其相關聯的功能表命令必須在具有 [shell \\ 動詞](#shellverb) 專案的 [自動播放] 檔案中定義。

### <a name="remarks"></a>備註

當使用者以滑鼠右鍵按一下磁片磁碟機圖示時，會出現快捷方式功能表。 如果有執行中的 .inf 檔案，則會從它取得預設快捷方式功能表命令。 當使用者按兩下磁片磁碟機的圖示時，也會執行此命令。

若要指定預設快捷方式功能表命令，請先使用 [shell \\ 動詞](#shellverb)來定義其動詞命令、命令字串和功能表文字。 然後使用 shell 將它設為預設快捷方式功能表命令。 否則，預設的功能表項目文字會是「自動播放」，這會啟動 [開啟](#parameters) 專案所指定的應用程式。

### <a name="shellverb"></a>shell \\ 動詞

**Shell \\ 動詞** 專案會將自訂命令新增至磁片磁碟機的快捷方式功能表。


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>參數

-   *動詞命令*

    功能表命令的動詞。 **Shell \\**_動詞_*_\\ 命令_* 專案會將動詞與可執行檔產生關聯。 動詞不能包含內嵌的空格。 依預設， *動詞* 是顯示在快捷方式功能表中的文字。

-   *Filename.exe*

    執行動作之應用程式的路徑和檔案名。

-   *MenuText*

    此參數會指定快捷方式功能表中顯示的文字。 如果省略，則會顯示 *動詞* 。 *MenuText* 可以是混合大小寫，而且可以包含空格。 您可以藉由在字母前面加上連字號 (&) ，來設定功能表項目的快速鍵。

### <a name="remarks"></a>備註

當使用者以滑鼠右鍵按一下磁片磁碟機圖示時，會出現快捷方式功能表。 將 **shell \\ 動詞** 命令新增至磁片磁碟機的 [自動播放] .inf 檔案，可讓您將命令新增到這個快捷方式功能表。

此專案有兩個部分，必須位於不同的行。 第一個部分是 **shell \\**_動詞_*_\\ 命令_*。 此為必要。 它會將名為 *動詞* 的字串與在命令執行時啟動的應用程式產生關聯。 第二個部分是 **shell \\**_動詞_ 專案。 此為選用項目。 您可以將它包含在快捷方式功能表中，以指定顯示的文字。

若要指定預設的快捷方式功能表命令，請使用 **shell \\ 動詞** 來定義動詞，並使其成為具有 [shell](#autoruninf-entries) 專案的預設命令。

下列範例自動執行 .inf 片段會將 *readit* 動詞與命令字串 "Notepad abc \\readme.txt" 產生關聯。 功能表文字是「自述我」，而「」是定義為專案的快速鍵。 當使用者選取此命令時， \\ 會使用 Microsoft 記事本開啟磁片磁碟機的 abcreadme.txt 檔。


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[內容 \] 金鑰

有三種檔案類型金鑰： **MusicFiles**、 **PictureFiles** 和 **VideoFiles**。

如果其中一項內容是透過不區分大小寫的值1、y、yes、t 或 true 來設定為 true，則不論媒體上是否存在該類型的內容，自動播放 UI 都會顯示與該內容類型相關聯的處理常式。

如果其中一項內容是透過不區分大小寫值0、n、否、f 或 false 的值設定為 false，則即使在媒體上偵測到該類型的內容，自動播放 UI 也不會顯示與該內容類型相關聯的處理常式。

使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放。 比方說，CD 可以歸類為只包含音樂內容，即使它也有圖片和影片，也會被視為具有混合的內容。

只有在 Windows Vista 和更新版本中才支援 [ **\[ 內容 \]** ] 區段。


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[ExclusiveContentPaths 索引 \] 鍵

本節所列的資料夾限制自動播放只搜尋這些資料夾及其內容的子資料夾。 您可以使用或不使用前置反斜線 () 來提供它們 \\ 。 在任一種情況下，都會從媒體的根目錄取得絕對路徑。 如果資料夾的名稱中有空格，請勿用引號括住，因為引號會以文字形式放在路徑的一部分。

使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放，並藉由將掃描限制在媒體的某些重要區域，縮短掃描時間。

以下是所有有效的路徑


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



只有在 Windows Vista 和更新版本下才支援 **\[ ExclusiveContentPaths \]** 區段。

## <a name="ignorecontentpaths-keys"></a>\[IgnoreContentPaths 索引 \] 鍵

在搜尋內容的媒體時，自動播放會忽略此區段中所列的資料夾及其子資料夾。 您可以使用或不使用前置反斜線 () 來提供它們 \\ 。 在任一種情況下，都會從媒體的根目錄取得絕對路徑。 如果資料夾的名稱中有空格，請勿用引號括住，因為引號會以文字形式放在路徑的一部分。

本節中的路徑優先于 **\[ ExclusiveContentPaths \]** 區段中的路徑。 如果 **\[ IgnoreContentPaths \]** 中提供的路徑是 **\[ ExclusiveContentPaths \]** 中指定之路徑的子資料夾，它仍會被忽略。

使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放，並藉由將掃描限制在媒體的某些重要區域，縮短掃描時間。

以下是所有有效的路徑


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



只有在 Windows Vista 和更新版本下才支援 **\[ IgnoreContentPaths \]** 區段。

## <a name="deviceinstall-keys"></a>\[DeviceInstall 索引 \] 鍵

### <a name="driverpath"></a>DriverPath

**DriverPath** 專案會指定要以遞迴方式搜尋驅動程式檔案的目錄。 此命令是在驅動程式安裝期間使用，不是自動執行操作的一部分。 只有在 Windows XP 下才支援 **\[ DeviceInstall \]** 區段。


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>參數

-   *directorypath*

    Windows 搜尋驅動程式檔案的目錄路徑，以及其所有子目錄。

### <a name="remarks"></a>備註

請勿在 *directorypath* 中使用磁碟機號，因為它們會從一部電腦變更為下一部電腦。

若要搜尋多個目錄，請在此範例中新增每個目錄的 **DriverPath** 專案。


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



如果 **\[ DeviceInstall \]** 區段中未提供任何 **DriverPath** 專案，或 **DriverPath** 專案沒有值，則會在搜尋驅動程式檔案期間略過該磁片磁碟機。

 

 
