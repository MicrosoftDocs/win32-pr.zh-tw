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
# <a name="using-symstore"></a><span data-ttu-id="b659b-104">使用 SymStore</span><span class="sxs-lookup"><span data-stu-id="b659b-104">Using SymStore</span></span>

<span data-ttu-id="b659b-105">SymStore (symstore.exe) 是用來建立符號存放區的工具。</span><span class="sxs-lookup"><span data-stu-id="b659b-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="b659b-106">它包含在 [適用于 Windows 的偵錯工具](https://www.microsoft.com/?ref=go) 套件中。</span><span class="sxs-lookup"><span data-stu-id="b659b-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="b659b-107">SymStore 會以一種格式來儲存符號，讓偵錯工具能夠根據) 的 (的格式來查閱符號，以及的 .pdb 或可執行檔的簽章和 age (來查閱符號，) 。</span><span class="sxs-lookup"><span data-stu-id="b659b-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="b659b-108">符號存放區優於傳統符號儲存格式的優點在於，所有符號都可以儲存或在相同的伺服器上加以參考，而且偵錯工具也不需要事先知道哪個產品包含對應的符號。</span><span class="sxs-lookup"><span data-stu-id="b659b-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="b659b-109">請注意，多個版本的 .pdb 符號檔 (例如，公用和私用版本) 無法儲存在相同的伺服器上，因為它們各包含相同的簽章和存留期。</span><span class="sxs-lookup"><span data-stu-id="b659b-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="b659b-110">SymStore 交易</span><span class="sxs-lookup"><span data-stu-id="b659b-110">SymStore Transactions</span></span>

<span data-ttu-id="b659b-111">每次呼叫 SymStore 都會記錄為一筆交易。</span><span class="sxs-lookup"><span data-stu-id="b659b-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="b659b-112">交易類型有兩種：新增和刪除。</span><span class="sxs-lookup"><span data-stu-id="b659b-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="b659b-113">建立符號存放區時，會在伺服器的根目錄下建立名為 "000admin" 的目錄。</span><span class="sxs-lookup"><span data-stu-id="b659b-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="b659b-114">000admin 目錄包含每個交易的一個檔案，以及記錄檔 Server.txt 和 History.txt。</span><span class="sxs-lookup"><span data-stu-id="b659b-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="b659b-115">Server.txt 檔案包含目前在伺服器上的所有交易清單。</span><span class="sxs-lookup"><span data-stu-id="b659b-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="b659b-116">History.txt 檔案包含所有交易的時間歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="b659b-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="b659b-117">每次 SymStore 儲存或移除符號檔案時，就會建立新的交易編號。</span><span class="sxs-lookup"><span data-stu-id="b659b-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="b659b-118">然後，會在000admin 中建立檔案，其名稱為此交易編號。</span><span class="sxs-lookup"><span data-stu-id="b659b-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="b659b-119">此檔案包含在此交易期間加入至符號存放區的所有檔案或指標的清單。</span><span class="sxs-lookup"><span data-stu-id="b659b-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="b659b-120">如果刪除交易，SymStore 會讀取其交易檔，以判斷應該刪除的檔案和指標。</span><span class="sxs-lookup"><span data-stu-id="b659b-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="b659b-121">[ **加入** ] **和 [** 刪除] 選項會指定是否要執行新增或刪除交易。</span><span class="sxs-lookup"><span data-stu-id="b659b-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="b659b-122">包含 **/p** 選項與 add 作業，可指定要加入指標;省略 **/p** 選項會指定要新增實際的符號檔。</span><span class="sxs-lookup"><span data-stu-id="b659b-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="b659b-123">您也可以在兩個不同的階段建立符號存放區。</span><span class="sxs-lookup"><span data-stu-id="b659b-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="b659b-124">在第一個階段中，您會使用 SymStore 搭配 **/x** 選項來建立索引檔。</span><span class="sxs-lookup"><span data-stu-id="b659b-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="b659b-125">在第二個階段中，您會使用 SymStore 搭配 **/y** 選項，從索引檔案中的資訊建立實際的檔案或指標存放區。</span><span class="sxs-lookup"><span data-stu-id="b659b-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="b659b-126">基於各種原因，這可能是很有用的技巧。</span><span class="sxs-lookup"><span data-stu-id="b659b-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="b659b-127">比方說，這可讓您輕鬆地重新建立符號存放區（只要索引檔仍然存在的話）。</span><span class="sxs-lookup"><span data-stu-id="b659b-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="b659b-128">或可能是包含符號檔的電腦，與將在其中建立符號存放區的電腦網路連接速度很慢。</span><span class="sxs-lookup"><span data-stu-id="b659b-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="b659b-129">在此情況下，您可以在與符號檔案相同的電腦上建立索引檔案，將索引檔案傳送至第二部電腦，然後在第二部電腦上建立存放區。</span><span class="sxs-lookup"><span data-stu-id="b659b-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="b659b-130">如需所有 SymStore 參數的完整清單，請參閱 [SymStore Command-Line 選項](symstore-command-line-options.md)。</span><span class="sxs-lookup"><span data-stu-id="b659b-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="b659b-131">SymStore 不支援來自多個使用者的同時交易。</span><span class="sxs-lookup"><span data-stu-id="b659b-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="b659b-132">建議將一個使用者指定為符號存放區的「系統管理員」，並負責所有的「 **新增** 」和「 **del** 」交易。</span><span class="sxs-lookup"><span data-stu-id="b659b-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="b659b-133">交易範例</span><span class="sxs-lookup"><span data-stu-id="b659b-133">Transaction Examples</span></span>

<span data-ttu-id="b659b-134">以下兩個範例 SymStore 將 Windows Server 2003 組建3790的符號指標新增至 \\ \\ >sampledir \\ symsrv：</span><span class="sxs-lookup"><span data-stu-id="b659b-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="b659b-135">在下列範例中，SymStore 會將 largeapp >appserver bin 中應用程式專案的實際符號檔加入 \\ \\ \\ \\ \\ \\ testdir \\ symsrv：</span><span class="sxs-lookup"><span data-stu-id="b659b-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="b659b-136">以下是使用索引檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="b659b-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="b659b-137">首先，SymStore 會根據 \\ \\ largeapp \\ >appserver \\ bin 中的符號檔集合來建立索引檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b659b-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="b659b-138">在此情況下，會將索引檔案放在第三部電腦上， \\ \\ hubserver \\ hubshare。</span><span class="sxs-lookup"><span data-stu-id="b659b-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="b659b-139">您可以使用 **/g** 選項來指定檔案前置詞 " \\ \\ largeapp \\ >appserver" 未來可能會變更：</span><span class="sxs-lookup"><span data-stu-id="b659b-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="b659b-140">現在假設您將所有符號檔移出電腦 \\ \\ largeapp \\ >appserver，並將它們放在 \\ \\ myarchive \\ >appserver 上。</span><span class="sxs-lookup"><span data-stu-id="b659b-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="b659b-141">然後，您可以從 [索引檔 hubserver hubshare] 建立符號存放區本身myindex.txt 如下所示 \\ \\ \\ \\ ：</span><span class="sxs-lookup"><span data-stu-id="b659b-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="b659b-142">最後，以下是 SymStore 刪除先前交易所加入之檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="b659b-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="b659b-143">請參閱下一節，以取得如何判斷交易識別碼的說明 (在此案例中為 0000000096) 。</span><span class="sxs-lookup"><span data-stu-id="b659b-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="b659b-144">壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="b659b-144">Compressed Files</span></span>

<span data-ttu-id="b659b-145">SymStore 可以透過兩種不同的方式用於壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="b659b-146">使用 SymStore 搭配 **/p** 選項來儲存符號檔的指標。</span><span class="sxs-lookup"><span data-stu-id="b659b-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="b659b-147">SymStore 完成後，壓縮指標所參考的檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="b659b-148">使用 SymStore 搭配 **/x** 選項來建立索引檔。</span><span class="sxs-lookup"><span data-stu-id="b659b-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="b659b-149">SymStore 完成後，壓縮索引檔中所列的檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="b659b-150">然後搭配使用 SymStore 與 **/y** 選項 (，如果您想要的話， **/p** 選項) 將檔案或指標儲存至符號存放區中的檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="b659b-151"> (SymStore 不需要解壓縮檔案，就能執行此作業。 ) </span><span class="sxs-lookup"><span data-stu-id="b659b-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="b659b-152">當需要時，您的符號伺服器將負責解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="b659b-153">如果您使用 SymSrv 作為符號伺服器，則應該使用隨 Microsoft Windows 軟體開發套件 (SDK) 散發的 compress.exe 工具來執行任何壓縮。</span><span class="sxs-lookup"><span data-stu-id="b659b-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b659b-154">壓縮檔案副檔名中的最後一個字元應該有底線 (例如， \_ module2 \_) 。</span><span class="sxs-lookup"><span data-stu-id="b659b-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="b659b-155">如需詳細資訊，請參閱 [使用 SymSrv](using-symsrv.md)。</span><span class="sxs-lookup"><span data-stu-id="b659b-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="b659b-156">server.txt 和 history.txt 檔案</span><span class="sxs-lookup"><span data-stu-id="b659b-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="b659b-157">當新增交易時，會將數個資訊專案新增至 server.txt，並 history.txt 供未來查閱功能使用。</span><span class="sxs-lookup"><span data-stu-id="b659b-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="b659b-158">以下是 server.txt 中的程式程式碼範例，以及新增交易的 history.txt：</span><span class="sxs-lookup"><span data-stu-id="b659b-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="b659b-159">這是以逗號分隔的行。</span><span class="sxs-lookup"><span data-stu-id="b659b-159">This is a comma-separated line.</span></span> <span data-ttu-id="b659b-160">這些欄位的定義如下。</span><span class="sxs-lookup"><span data-stu-id="b659b-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="b659b-161">欄位</span><span class="sxs-lookup"><span data-stu-id="b659b-161">Field</span></span>      | <span data-ttu-id="b659b-162">描述</span><span class="sxs-lookup"><span data-stu-id="b659b-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b659b-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="b659b-163">0000000096</span></span> | <span data-ttu-id="b659b-164">SymStore 所建立的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="b659b-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="b659b-165">add</span><span class="sxs-lookup"><span data-stu-id="b659b-165">add</span></span>        | <span data-ttu-id="b659b-166">交易的類型。</span><span class="sxs-lookup"><span data-stu-id="b659b-166">Type of transaction.</span></span> <span data-ttu-id="b659b-167">這個欄位可以是 [ **新增** ] 或 [ **del**]。</span><span class="sxs-lookup"><span data-stu-id="b659b-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="b659b-168">ptr</span><span class="sxs-lookup"><span data-stu-id="b659b-168">ptr</span></span>        | <span data-ttu-id="b659b-169">是否已加入檔案或指標。</span><span class="sxs-lookup"><span data-stu-id="b659b-169">Whether files or pointers were added.</span></span> <span data-ttu-id="b659b-170">這個欄位 **可以是 [檔案] 或 [** **ptr**]。</span><span class="sxs-lookup"><span data-stu-id="b659b-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="b659b-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="b659b-171">10/09/99</span></span>   | <span data-ttu-id="b659b-172">交易發生的日期。</span><span class="sxs-lookup"><span data-stu-id="b659b-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="b659b-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="b659b-173">00:08:32</span></span>   | <span data-ttu-id="b659b-174">交易開始的時間。</span><span class="sxs-lookup"><span data-stu-id="b659b-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="b659b-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b659b-175">Windows XP</span></span> | <span data-ttu-id="b659b-176">產品。</span><span class="sxs-lookup"><span data-stu-id="b659b-176">Product.</span></span>                                                                            |
| <span data-ttu-id="b659b-177">x86 頻率</span><span class="sxs-lookup"><span data-stu-id="b659b-177">x86 fre</span></span>    | <span data-ttu-id="b659b-178"> (選用) 的版本。</span><span class="sxs-lookup"><span data-stu-id="b659b-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="b659b-179">新增來源</span><span class="sxs-lookup"><span data-stu-id="b659b-179">Added from</span></span> | <span data-ttu-id="b659b-180">批註 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="b659b-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="b659b-181">未使用</span><span class="sxs-lookup"><span data-stu-id="b659b-181">Unused</span></span>     | <span data-ttu-id="b659b-182"> (保留供稍後使用。 ) </span><span class="sxs-lookup"><span data-stu-id="b659b-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="b659b-183">以下是事務檔0000000096中的一些範例。</span><span class="sxs-lookup"><span data-stu-id="b659b-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="b659b-184">每一行都會記錄目錄，以及已新增至目錄的檔案或指標的位置。</span><span class="sxs-lookup"><span data-stu-id="b659b-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="b659b-185">如果您使用 **del** 交易來復原原始的 **加入** 交易，這些行會從 server.txt 中移除，並將下列程式程式碼新增至 history.txt：</span><span class="sxs-lookup"><span data-stu-id="b659b-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="b659b-186">刪除交易的欄位定義如下。</span><span class="sxs-lookup"><span data-stu-id="b659b-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="b659b-187">欄位</span><span class="sxs-lookup"><span data-stu-id="b659b-187">Field</span></span>      | <span data-ttu-id="b659b-188">描述</span><span class="sxs-lookup"><span data-stu-id="b659b-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="b659b-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="b659b-189">0000000105</span></span> | <span data-ttu-id="b659b-190">SymStore 所建立的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="b659b-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="b659b-191">del</span><span class="sxs-lookup"><span data-stu-id="b659b-191">del</span></span>        | <span data-ttu-id="b659b-192">交易的類型。</span><span class="sxs-lookup"><span data-stu-id="b659b-192">Type of transaction.</span></span> <span data-ttu-id="b659b-193">這個欄位可以是 [ **新增** ] 或 [ **del**]。</span><span class="sxs-lookup"><span data-stu-id="b659b-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="b659b-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="b659b-194">0000000096</span></span> | <span data-ttu-id="b659b-195">已刪除的交易。</span><span class="sxs-lookup"><span data-stu-id="b659b-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="b659b-196">符號儲存格式</span><span class="sxs-lookup"><span data-stu-id="b659b-196">Symbol Storage Format</span></span>

<span data-ttu-id="b659b-197">SymStore 使用檔案系統本身做為資料庫。</span><span class="sxs-lookup"><span data-stu-id="b659b-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="b659b-198">它會根據符號檔案時間戳記、簽章、存留期和其他資料等專案，建立一個大型目錄樹狀目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="b659b-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="b659b-199">例如，在將數個不同的 acpi 檔加入至伺服器之後，目錄看起來可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="b659b-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

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

<span data-ttu-id="b659b-200">在此範例中，適用于 acpi 符號檔的查閱路徑可能看起來像這樣： \\ \\ mybuilds \\ symsrv \\ acpi \\ 37cdb03962040。</span><span class="sxs-lookup"><span data-stu-id="b659b-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="b659b-201">查閱目錄內可能會有三個檔案：</span><span class="sxs-lookup"><span data-stu-id="b659b-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="b659b-202">如果已儲存檔案，則會在該處存在 acpi。</span><span class="sxs-lookup"><span data-stu-id="b659b-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="b659b-203">如果指標已儲存，則名為 file 的檔案會存在，而且會包含實際符號檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b659b-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="b659b-204">稱為 refs 的檔案，其中包含所有目前的 acpi 的位置清單，此時間戳記與目前新增至符號存放區的影像大小。</span><span class="sxs-lookup"><span data-stu-id="b659b-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="b659b-205">顯示 \\ \\ mybuilds symsrv acpi 的目錄 \\ 清單 \\ 。 dbg \\ 37cdb03962040 提供下列各項：</span><span class="sxs-lookup"><span data-stu-id="b659b-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="b659b-206">檔案。 ptr 包含文字字串 " \\ \\ mybuilds \\ 符號 \\ x86 \\ 2128 .chk \\ 符號 \\ sys \\ acpi"。</span><span class="sxs-lookup"><span data-stu-id="b659b-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="b659b-207">由於這個目錄中沒有名為 acpi 的檔案，偵錯工具會嘗試在 \\ \\ mybuilds 符號 x86 2128 中尋找檔案 \\ \\ \\ 。 .chk \\ 符號 \\ sys \\ acpi</span><span class="sxs-lookup"><span data-stu-id="b659b-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="b659b-208">Refs 的內容僅供 SymStore 使用，而不是由偵錯工具使用。</span><span class="sxs-lookup"><span data-stu-id="b659b-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="b659b-209">此檔案包含在此目錄中發生之所有交易的記錄。</span><span class="sxs-lookup"><span data-stu-id="b659b-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="b659b-210">Refs 的範例行可能是：</span><span class="sxs-lookup"><span data-stu-id="b659b-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="b659b-211">這會顯示 \\ \\ mybuilds \\ 符號 x86 2128 的指標。 \\ \\ \\ \\ \\ 已使用交易 "0000000026" 加入了 sys acpi。</span><span class="sxs-lookup"><span data-stu-id="b659b-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="b659b-212">某些符號檔會透過各種產品或組建或特定產品保持不變。</span><span class="sxs-lookup"><span data-stu-id="b659b-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="b659b-213">其中一個範例是 file msvcrt.lib .pdb。</span><span class="sxs-lookup"><span data-stu-id="b659b-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="b659b-214">執行 \\ \\ mybuilds symsrv 的目錄 \\ \\ msvcrt.lib 會顯示只有兩個版本的 msvcrt.lib 已新增至符號伺服器：</span><span class="sxs-lookup"><span data-stu-id="b659b-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="b659b-215">但是，執行 \\ \\ mybuilds \\ symsrv \\ msvcrt.lib 目錄時， \\ 會顯示 refs 中有幾個指標。</span><span class="sxs-lookup"><span data-stu-id="b659b-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="b659b-216">\\ \\ Mybuilds \\ symsrv \\ msvcrt.lib .pdb \\ 37a8f40e2 \\ refs 的內容如下：</span><span class="sxs-lookup"><span data-stu-id="b659b-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

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

<span data-ttu-id="b659b-217">這會顯示 msvcrt.lib 儲存在 \\ \\ mybuilds \\ symsrv 上的多個符號組建中使用了相同的 .pdb。</span><span class="sxs-lookup"><span data-stu-id="b659b-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="b659b-218">以下是包含混合檔案和指標新增的目錄範例：</span><span class="sxs-lookup"><span data-stu-id="b659b-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="b659b-219">在此情況下，refs 會有下列內容：</span><span class="sxs-lookup"><span data-stu-id="b659b-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="b659b-220">因此，交易43、44和45會將相同的檔案加入至伺服器，並將交易46和47加入指標。</span><span class="sxs-lookup"><span data-stu-id="b659b-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="b659b-221">如果刪除交易43、44和45，則會從目錄中刪除 dbghelp 檔案。</span><span class="sxs-lookup"><span data-stu-id="b659b-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="b659b-222">目錄接著會有下列內容：</span><span class="sxs-lookup"><span data-stu-id="b659b-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="b659b-223">現在是檔案。 ptr 包含 " \\ \\ sampledir2 \\ bin \\ 符號 \\ retail \\ dll \\ dbghelp"，以及 refs contains</span><span class="sxs-lookup"><span data-stu-id="b659b-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="b659b-224">只要 refs 中的最後一個專案是指標，檔案就會存在，而且會包含關聯檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b659b-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="b659b-225">每當 refs 中的最後一個專案是檔案時，就不會有任何檔案。 ptr 會存在於此目錄中。</span><span class="sxs-lookup"><span data-stu-id="b659b-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="b659b-226">因此，在 refs 中移除最後一個專案的任何刪除作業，可能會導致建立、刪除或變更檔案的 ptr。</span><span class="sxs-lookup"><span data-stu-id="b659b-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



