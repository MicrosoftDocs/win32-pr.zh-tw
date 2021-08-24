---
description: 來源伺服器可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: 來源伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1938a617cd6c8f613df2a1113288a27f6593336f819cde2f5380a8420c329d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815508"
---
# <a name="source-server"></a>來源伺服器

來源伺服器可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。 由於模組的原始程式碼可能會在版本之間變更，而在一年的期間內，因此在建立問題的模組版本時，請務必查看原始程式碼是否存在。

來源伺服器會從原始檔控制抓取適當的檔案。 若要使用來源伺服器，應用程式必須已經過來源索引。

## <a name="source-indexing"></a>來源索引編制

來源索引系統是可執行檔和 Perl 腳本的集合。 Perl 腳本需要 Perl 5.6 或更新版本。

一般而言，建立應用程式之後，二進位檔會在建立程式期間編制來源索引。 來源伺服器所需的資訊會儲存在 PDB 檔案中。

來源伺服器目前隨附的腳本應與下列原始檔控制系統搭配使用。

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   CVS
-   Subversion

您也可以建立自訂腳本，為不同的原始檔控制系統建立程式碼的索引。

下表列出來源伺服器工具。



| 工具        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | 這個檔案是所有原始檔控制伺服器的主要清單。 每個專案都具有下列格式：*MYSERVER* = *serverinfo*<br/> 使用 Perforce 時，伺服器資訊是由伺服器的完整網路路徑所組成，後面接著冒號，後面接著它所使用的埠號碼。 例如：<br/> MYSERVER = machine.config：1666<br/> 您可以在執行偵錯工具的電腦上安裝這個檔案。 當來源伺服器啟動時，會查看 Srcsrv.ini 的值;這些值會覆寫 PDB 檔案中包含的資訊。 這可讓使用者將偵錯工具設定為在 debug time 使用替代的原始檔控制伺服器。<br/> 如需詳細資訊，請參閱隨來源伺服器工具一起安裝的範例 Srcsrv.ini。<br/> |
| Ssindex .cmd | 此腳本會建立簽入原始檔控制中的檔案清單，以及每個檔案的版本資訊。 它會在您建立應用程式時產生的 .pdb 檔案中儲存這項資訊的子集。 腳本會使用下列其中一個 Perl 模組來與原始檔控制互動： P4.pm (Perforce) 或 Vss.pm (Visual source 保管庫) 。如需詳細資訊，請使用-？執行腳本。 或-??  (詳細資訊說明) 選項或檢查腳本。<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | 此公用程式會列出在 .pdb 檔案中建立索引的所有檔案。 它會針對每個檔案列出檔案的完整路徑、原始檔控制伺服器和版本號碼。 您可以使用此資訊來取出檔案，而不需要使用來源伺服器。如需詳細資訊，請使用/？執行公用程式。 選項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | 索引腳本會使用此公用程式，將版本控制資訊插入目標 .pdb 檔案的 "srcsrv" 替代資料流程中。 它也可以從 .pdb 檔案讀取任何資料流程。 您可以使用此資訊來確認索引腳本是否正常運作。如需詳細資訊，請使用/？執行公用程式。 選項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>正在抓取來源檔案

DbgHelp API 可讓您透過 [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) 函數存取來源伺服器功能。 若要抓取要抓取之原始程式檔的名稱，請呼叫 [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) 或 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) 函數。

## <a name="using-source-server-with-a-debugger"></a>使用來源伺服器搭配偵錯工具

若要使用具有 WinDbg、KD、NTSD 或 CDB 的來源伺服器，請確定您已安裝最新版的偵錯工具，以供 Windows 套件 (6.3 版或更新版本) 。 然後，將 srv 包含 \* 在 srcpath 命令中，如下所示：

**\. srcpath srv \* ;**_c： \\ mysource_

請注意，此範例也包含傳統的來源路徑。 如果偵錯工具無法從來源伺服器取得檔案，則會搜尋指定的路徑。

如果來源檔案是由來源伺服器抓取，則在偵錯工具結束後，它會保留在硬碟上。 原始程式檔會儲存在本機的偵錯工具的 src 子目錄中，以便 Windows 安裝目錄。

## <a name="source-server-data-blocks"></a>來源伺服器資料區塊

來源伺服器依賴 PDB 檔案中的兩個數據區塊。

-   原始檔案清單。 建立模組會自動建立用來建立模組之原始程式檔的完整路徑清單。
-   資料區塊。 如先前所述對來源進行索引編制，會將替代資料流程新增至名為 "srcsrv" 的 PDB 檔案。 插入此資料的腳本取決於特定的組建進程和使用中的原始檔控制系統。

在語言規格第1版中，資料區塊分成三個區段： ini、變數和原始程式檔。 它有下列語法。

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

除了以百分比符號括住的文字 (% ) 之外，所有文字都會以字面方式解讀。 以百分比符號括住的文字會被視為要以遞迴方式解析的變數名稱，除非它是下列其中一項功能：

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>% fnvar% () 
</dt> <dd>

參數文字應以百分比符號括住，並視為要展開的變數。

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>% fnbksl% () 
</dt> <dd>

參數文字中 (/) 的所有正斜線都應取代為 () 的反斜線 \\ 。

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>% fnfile% () 
</dt> <dd>

參數文字中的所有路徑資訊都應該移除，只留下檔案名。

</dd> </dl>

Ini 區段包含描述需求的變數。 索引腳本可以將任意數目的變數加入此區段。 範例如下：

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>版本
</dt> <dd>

語言規格版本。 這是必要變數。

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

描述原始檔控制產品的字串。 這個變數是選擇性的。

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>DATETIME
</dt> <dd>

字串，表示 PDB 檔案的處理日期和時間。 這個變數是選擇性的。

</dd> </dl>

Variables 區段包含的變數，可描述如何從原始檔控制中解壓縮檔案。 它也可以用來將常用的文字定義為變數，以縮減資料區塊的大小。

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

說明如何建立解壓縮檔案的目標路徑。 這是必要的變數。

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

描述如何建立命令以從原始檔控制中解壓縮檔案。 這包括可執行檔及其命令列參數的名稱。 這是必要的變數。

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

字串，列出要在檔案解壓縮期間建立的環境變數。 以倒退鍵字元分隔多個專案 (\\ b) 。 這是選擇性變數。

</dd> </dl>

[來源檔案] 區段包含已編制索引之每個原始程式檔的專案。 每一行的內容都會轉譯為具有 VAR1、VAR2、VAR3 等名稱的變數，直到 VAR10 為止。 變數以星號分隔。 VAR1 必須指定來源檔案的完整路徑，如 PDB 檔案中的其他位置所列。 例如，下列程式程式碼：

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

解釋如下：

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

在此範例中，VAR4 是版本號碼。 不過，大部分的原始檔控制系統都支援以標記檔案的方式來還原指定組建的來源狀態。 因此，您可以另外使用組建的標籤。 您可以修改範例資料區塊，以包含如下所示的變數：

``` syntax
LABEL=BUILD47
```

然後，假設原始檔控制系統使用 at sign ( @ ) 來表示標籤，您可以修改 SRCSRVCMD 變數，如下所示：

**sd.exe-p% fnvar% (% var2% ) 列印-o% srcsrvtrg%-q% 倉庫%/%var3% @% label%**

## <a name="how-source-server-works"></a>來源伺服器的運作方式

來源伺服器用戶端會在 Symsrv.dll 中執行。 用戶端不會直接從 PDB 檔案解壓縮資訊;它會使用一個符號處理常式，例如在 Dbghelp.dll 中執行的處理常式。 它基本上是一個遞迴變數替代引擎，它會建立一個命令列，可用來從原始檔控制系統解壓縮適當的原始程式檔。 您的程式碼不應該直接呼叫 Symsrv.dll。 若要將它的功能整合到您的應用程式中，請使用 [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) 函數。

來源伺服器的第一個版本運作方式如下。 此行為在未來的版本中可能會變更。

-   用戶端會呼叫 **SrcSrvInit** 函式，並將目標路徑用作所有來源檔案提取的基底。 它會將此路徑儲存在 TARG 變數中。
-   用戶端會在載入模組 PDB 時從 PDB 解壓縮 Srcsrv 資料流程，並呼叫 **SrcSrvLoadModule** 函式將資料區塊傳遞給來源伺服器。
-   當 Dbghelp 抓取來源檔案時，用戶端會呼叫 **SrcSrvGetFile** 函式，以從原始檔控制中取出原始檔。
-   來源伺服器會搜尋資料區塊中的原始程式檔專案，以尋找符合所要求檔案的專案。 它會使用原始程式檔專案的內容，將 VAR1 填滿至 VAR *n* 。 接著，它會使用 VAR1 將 SRCSRVTRG 變數展開為 VAR *n*。 如果檔案已在這個位置中，它會將位置傳回給呼叫者。 否則，它會展開 SRCSRVCMD 變數，以建立從原始檔控制取出檔案並將它複製到目標位置所需的命令。 最後，它會執行此命令。

## <a name="creating-a-source-control-provider-module"></a>建立原始檔控制提供者模組

來源伺服器包含 Perforce 的提供者模組 (p4.pm) 和 Visual source 保管庫 (vss.pm) 。 若要建立您自己的提供者模組，您必須執行下列一組介面。

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module：： SimpleUsage ()**
</dt> <dd>

目的：將簡單的模組使用資訊顯示為 STDOUT。

參數：無

傳回值：無

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module：： VerboseUsage ()**
</dt> <dd>

目的：對 STDOUT 顯示深入的模組使用量資訊。

參數：無

傳回值：無

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module：： new (\@ CommandArguments)**
</dt> <dd>

目的：初始化提供者模組的實例。

參數： @ARGV SSIndex 未辨識為一般引數的所有引數。

傳回值：可在後續作業中使用的參考。

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref >GatherFileInformation ($SourcePath，$ServerHashReference)**
</dt> <dd>

目的：讓模組收集 $SourcePath 參數所指定之目錄的必要來源索引資訊。 模組不應該假設每個物件實例都只會呼叫這個專案一次，因為 SSIndex 可能會針對不同的路徑多次呼叫它。

參數： (1) 包含要編制索引之來源的本機目錄。  (2) 雜湊的參考，其中包含指定之 Srcsrv.ini 檔中的所有專案。

傳回值：無

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference、$FileEntry) = $objref->Microsoft.visualbasic.fileio.filesystem.getfileinfo ($LocalFile)**
</dt> <dd>

目的：提供從原始檔控制系統解壓縮單一特定檔案的必要資訊。

參數：完整檔案名

傳回值： (1) 解讀所傳回 $FileEntry 所需變數的雜湊參考。 SSIndex 會為單一 debug 檔案使用的每個來源檔案快取這些變數，以減少寫入來源索引資料流程的資訊量。  (2) 要寫入來源索引資料流程的檔案專案，以允許 SrcSrv.dll 從原始檔控制中解壓縮此檔案。 這一行的確切格式是由原始檔控制系統所特有。

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**
</dt> <dd>

目的：提供描述性字串來識別使用者的原始檔控制提供者。

參數：無

傳回值：原始檔控制系統的描述性名稱。

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**
</dt> <dd>

目的：讓原始檔控制提供者將原始檔控制特定變數加入至每個偵錯工具的來來源資料流。 範例模組會使用這個方法來撰寫必要的解壓縮 \_ CMD 和解壓縮 \_ 目標變數。

參數：無

傳回值：來來源資料流變數的專案清單。

</dd> </dl>

 

 




