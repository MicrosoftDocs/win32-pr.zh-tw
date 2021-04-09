---
description: SymStore (symstore.exe) 是用來建立符號存放區的工具。 它包含在適用于 Windows 的偵錯工具套件中。
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: 使用 SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110709"
---
# <a name="using-symstore"></a>使用 SymStore

SymStore (symstore.exe) 是用來建立符號存放區的工具。 它包含在 [適用于 Windows 的偵錯工具](https://www.microsoft.com/?ref=go) 套件中。

SymStore 會以一種格式來儲存符號，讓偵錯工具能夠根據) 的 (的格式來查閱符號，以及的 .pdb 或可執行檔的簽章和 age (來查閱符號，) 。 符號存放區優於傳統符號儲存格式的優點在於，所有符號都可以儲存或在相同的伺服器上加以參考，而且偵錯工具也不需要事先知道哪個產品包含對應的符號。

請注意，多個版本的 .pdb 符號檔 (例如，公用和私用版本) 無法儲存在相同的伺服器上，因為它們各包含相同的簽章和存留期。

## <a name="symstore-transactions"></a>SymStore 交易

每次呼叫 SymStore 都會記錄為一筆交易。 交易類型有兩種：新增和刪除。

建立符號存放區時，會在伺服器的根目錄下建立名為 "000admin" 的目錄。 000admin 目錄包含每個交易的一個檔案，以及記錄檔 Server.txt 和 History.txt。 Server.txt 檔案包含目前在伺服器上的所有交易清單。 History.txt 檔案包含所有交易的時間歷程記錄。

每次 SymStore 儲存或移除符號檔案時，就會建立新的交易編號。 然後，會在000admin 中建立檔案，其名稱為此交易編號。 此檔案包含在此交易期間加入至符號存放區的所有檔案或指標的清單。 如果刪除交易，SymStore 會讀取其交易檔，以判斷應該刪除的檔案和指標。

[ **加入** ] **和 [** 刪除] 選項會指定是否要執行新增或刪除交易。 包含 **/p** 選項與 add 作業，可指定要加入指標;省略 **/p** 選項會指定要新增實際的符號檔。

您也可以在兩個不同的階段建立符號存放區。 在第一個階段中，您會使用 SymStore 搭配 **/x** 選項來建立索引檔。 在第二個階段中，您會使用 SymStore 搭配 **/y** 選項，從索引檔案中的資訊建立實際的檔案或指標存放區。

基於各種原因，這可能是很有用的技巧。 比方說，這可讓您輕鬆地重新建立符號存放區（只要索引檔仍然存在的話）。 或可能是包含符號檔的電腦，與將在其中建立符號存放區的電腦網路連接速度很慢。 在此情況下，您可以在與符號檔案相同的電腦上建立索引檔案，將索引檔案傳送至第二部電腦，然後在第二部電腦上建立存放區。

如需所有 SymStore 參數的完整清單，請參閱 [SymStore Command-Line 選項](symstore-command-line-options.md)。

> [!Note]  
> SymStore 不支援來自多個使用者的同時交易。 建議將一個使用者指定為符號存放區的「系統管理員」，並負責所有的「 **新增** 」和「 **del** 」交易。

 

## <a name="transaction-examples"></a>交易範例

以下兩個範例 SymStore 將 Windows Server 2003 組建3790的符號指標新增至 \\ \\ >sampledir \\ symsrv：

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

在下列範例中，SymStore 會將 largeapp >appserver bin 中應用程式專案的實際符號檔加入 \\ \\ \\ \\ \\ \\ testdir \\ symsrv：

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

以下是使用索引檔案的範例。 首先，SymStore 會根據 \\ \\ largeapp \\ >appserver \\ bin 中的符號檔集合來建立索引檔案 \\ 。 在此情況下，會將索引檔案放在第三部電腦上， \\ \\ hubserver \\ hubshare。 您可以使用 **/g** 選項來指定檔案前置詞 " \\ \\ largeapp \\ >appserver" 未來可能會變更：

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

現在假設您將所有符號檔移出電腦 \\ \\ largeapp \\ >appserver，並將它們放在 \\ \\ myarchive \\ >appserver 上。 然後，您可以從 [索引檔 hubserver hubshare] 建立符號存放區本身myindex.txt 如下所示 \\ \\ \\ \\ ：

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

最後，以下是 SymStore 刪除先前交易所加入之檔案的範例。 請參閱下一節，以取得如何判斷交易識別碼的說明 (在此案例中為 0000000096) 。

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>壓縮檔案

SymStore 可以透過兩種不同的方式用於壓縮檔案。

1.  使用 SymStore 搭配 **/p** 選項來儲存符號檔的指標。 SymStore 完成後，壓縮指標所參考的檔案。
2.  使用 SymStore 搭配 **/x** 選項來建立索引檔。 SymStore 完成後，壓縮索引檔中所列的檔案。 然後搭配使用 SymStore 與 **/y** 選項 (，如果您想要的話， **/p** 選項) 將檔案或指標儲存至符號存放區中的檔案。  (SymStore 不需要解壓縮檔案，就能執行此作業。 ) 

當需要時，您的符號伺服器將負責解壓縮檔案。

如果您使用 SymSrv 作為符號伺服器，則應該使用隨 Microsoft Windows 軟體開發套件 (SDK) 散發的 compress.exe 工具來執行任何壓縮。 壓縮檔案副檔名中的最後一個字元應該有底線 (例如， \_ module2 \_) 。 如需詳細資訊，請參閱 [使用 SymSrv](using-symsrv.md)。

## <a name="the-servertxt-and-historytxt-files"></a>server.txt 和 history.txt 檔案

當新增交易時，會將數個資訊專案新增至 server.txt，並 history.txt 供未來查閱功能使用。 以下是 server.txt 中的程式程式碼範例，以及新增交易的 history.txt：

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

這是以逗號分隔的行。 這些欄位的定義如下。



| 欄位      | 描述                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | SymStore 所建立的交易識別碼。                                      |
| add        | 交易的類型。 這個欄位可以是 [ **新增** ] 或 [ **del**]。                   |
| ptr        | 是否已加入檔案或指標。 這個欄位 **可以是 [檔案] 或 [** **ptr**]。 |
| 10/09/99   | 交易發生的日期。                                                     |
| 00:08:32   | 交易開始的時間。                                                      |
| Windows XP | 產品。                                                                            |
| x86 頻率    |  (選用) 的版本。                                                                 |
| 新增來源 | 批註 (選擇性)                                                                   |
| 未使用     |  (保留供稍後使用。 )                                                            |



 

以下是事務檔0000000096中的一些範例。 每一行都會記錄目錄，以及已新增至目錄的檔案或指標的位置。

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

如果您使用 **del** 交易來復原原始的 **加入** 交易，這些行會從 server.txt 中移除，並將下列程式程式碼新增至 history.txt：

``` syntax
0000000105,del,0000000096
```

刪除交易的欄位定義如下。



| 欄位      | 描述                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | SymStore 所建立的交易識別碼。                    |
| del        | 交易的類型。 這個欄位可以是 [ **新增** ] 或 [ **del**]。 |
| 0000000096 | 已刪除的交易。                                     |



 

## <a name="symbol-storage-format"></a>符號儲存格式

SymStore 使用檔案系統本身做為資料庫。 它會根據符號檔案時間戳記、簽章、存留期和其他資料等專案，建立一個大型目錄樹狀目錄名稱。

例如，在將數個不同的 acpi 檔加入至伺服器之後，目錄看起來可能如下所示：

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

在此範例中，適用于 acpi 符號檔的查閱路徑可能看起來像這樣： \\ \\ mybuilds \\ symsrv \\ acpi \\ 37cdb03962040。

查閱目錄內可能會有三個檔案：

1.  如果已儲存檔案，則會在該處存在 acpi。
2.  如果指標已儲存，則名為 file 的檔案會存在，而且會包含實際符號檔的路徑。
3.  稱為 refs 的檔案，其中包含所有目前的 acpi 的位置清單，此時間戳記與目前新增至符號存放區的影像大小。

顯示 \\ \\ mybuilds symsrv acpi 的目錄 \\ 清單 \\ 。 dbg \\ 37cdb03962040 提供下列各項：

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

檔案。 ptr 包含文字字串 " \\ \\ mybuilds \\ 符號 \\ x86 \\ 2128 .chk \\ 符號 \\ sys \\ acpi"。 由於這個目錄中沒有名為 acpi 的檔案，偵錯工具會嘗試在 \\ \\ mybuilds 符號 x86 2128 中尋找檔案 \\ \\ \\ 。 .chk \\ 符號 \\ sys \\ acpi

Refs 的內容僅供 SymStore 使用，而不是由偵錯工具使用。 此檔案包含在此目錄中發生之所有交易的記錄。 Refs 的範例行可能是：

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

這會顯示 \\ \\ mybuilds \\ 符號 x86 2128 的指標。 \\ \\ \\ \\ \\ 已使用交易 "0000000026" 加入了 sys acpi。

某些符號檔會透過各種產品或組建或特定產品保持不變。 其中一個範例是 file msvcrt.lib .pdb。 執行 \\ \\ mybuilds symsrv 的目錄 \\ \\ msvcrt.lib 會顯示只有兩個版本的 msvcrt.lib 已新增至符號伺服器：

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

但是，執行 \\ \\ mybuilds \\ symsrv \\ msvcrt.lib 目錄時， \\ 會顯示 refs 中有幾個指標。

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

\\ \\ Mybuilds \\ symsrv \\ msvcrt.lib .pdb \\ 37a8f40e2 \\ refs 的內容如下：

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

這會顯示 msvcrt.lib 儲存在 \\ \\ mybuilds \\ symsrv 上的多個符號組建中使用了相同的 .pdb。

以下是包含混合檔案和指標新增的目錄範例：

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

在此情況下，refs 會有下列內容：

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

因此，交易43、44和45會將相同的檔案加入至伺服器，並將交易46和47加入指標。 如果刪除交易43、44和45，則會從目錄中刪除 dbghelp 檔案。 目錄接著會有下列內容：

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

現在是檔案。 ptr 包含 " \\ \\ sampledir2 \\ bin \\ 符號 \\ retail \\ dll \\ dbghelp"，以及 refs contains

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

只要 refs 中的最後一個專案是指標，檔案就會存在，而且會包含關聯檔案的路徑。 每當 refs 中的最後一個專案是檔案時，就不會有任何檔案。 ptr 會存在於此目錄中。 因此，在 refs 中移除最後一個專案的任何刪除作業，可能會導致建立、刪除或變更檔案的 ptr。

 

 



