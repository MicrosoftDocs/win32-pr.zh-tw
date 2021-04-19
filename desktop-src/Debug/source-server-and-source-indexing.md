---
description: 來源伺服器可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: 來源伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991377"
---
# <a name="source-server"></a><span data-ttu-id="6fff3-103">來源伺服器</span><span class="sxs-lookup"><span data-stu-id="6fff3-103">Source Server</span></span>

<span data-ttu-id="6fff3-104">來源伺服器可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。</span><span class="sxs-lookup"><span data-stu-id="6fff3-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="6fff3-105">由於模組的原始程式碼可能會在版本之間變更，而在一年的期間內，因此在建立問題的模組版本時，請務必查看原始程式碼是否存在。</span><span class="sxs-lookup"><span data-stu-id="6fff3-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="6fff3-106">來源伺服器會從原始檔控制抓取適當的檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="6fff3-107">若要使用來源伺服器，應用程式必須已經過來源索引。</span><span class="sxs-lookup"><span data-stu-id="6fff3-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="6fff3-108">來源索引編制</span><span class="sxs-lookup"><span data-stu-id="6fff3-108">Source Indexing</span></span>

<span data-ttu-id="6fff3-109">來源索引系統是可執行檔和 Perl 腳本的集合。</span><span class="sxs-lookup"><span data-stu-id="6fff3-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="6fff3-110">Perl 腳本需要 Perl 5.6 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6fff3-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="6fff3-111">一般而言，建立應用程式之後，二進位檔會在建立程式期間編制來源索引。</span><span class="sxs-lookup"><span data-stu-id="6fff3-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="6fff3-112">來源伺服器所需的資訊會儲存在 PDB 檔案中。</span><span class="sxs-lookup"><span data-stu-id="6fff3-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="6fff3-113">來源伺服器目前隨附的腳本應與下列原始檔控制系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6fff3-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="6fff3-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="6fff3-114">Team Foundation Server</span></span>
-   <span data-ttu-id="6fff3-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="6fff3-115">Perforce</span></span>
-   <span data-ttu-id="6fff3-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="6fff3-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="6fff3-117">Cvs</span><span class="sxs-lookup"><span data-stu-id="6fff3-117">CVS</span></span>
-   <span data-ttu-id="6fff3-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="6fff3-118">Subversion</span></span>

<span data-ttu-id="6fff3-119">您也可以建立自訂腳本，為不同的原始檔控制系統建立程式碼的索引。</span><span class="sxs-lookup"><span data-stu-id="6fff3-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="6fff3-120">下表列出來源伺服器工具。</span><span class="sxs-lookup"><span data-stu-id="6fff3-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="6fff3-121">工具</span><span class="sxs-lookup"><span data-stu-id="6fff3-121">Tool</span></span>        | <span data-ttu-id="6fff3-122">描述</span><span class="sxs-lookup"><span data-stu-id="6fff3-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fff3-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="6fff3-123">Srcsrv.ini</span></span>  | <span data-ttu-id="6fff3-124">這個檔案是所有原始檔控制伺服器的主要清單。</span><span class="sxs-lookup"><span data-stu-id="6fff3-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="6fff3-125">每個專案都具有下列格式：*MYSERVER* = *serverinfo*</span><span class="sxs-lookup"><span data-stu-id="6fff3-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="6fff3-126">使用 Perforce 時，伺服器資訊是由伺服器的完整網路路徑所組成，後面接著冒號，後面接著它所使用的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="6fff3-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="6fff3-127">例如：</span><span class="sxs-lookup"><span data-stu-id="6fff3-127">For example:</span></span><br/> <span data-ttu-id="6fff3-128">MYSERVER = machine.config：1666</span><span class="sxs-lookup"><span data-stu-id="6fff3-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="6fff3-129">您可以在執行偵錯工具的電腦上安裝這個檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="6fff3-130">當來源伺服器啟動時，會查看 Srcsrv.ini 的值;這些值會覆寫 PDB 檔案中包含的資訊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="6fff3-131">這可讓使用者將偵錯工具設定為在 debug time 使用替代的原始檔控制伺服器。</span><span class="sxs-lookup"><span data-stu-id="6fff3-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="6fff3-132">如需詳細資訊，請參閱隨來源伺服器工具一起安裝的範例 Srcsrv.ini。</span><span class="sxs-lookup"><span data-stu-id="6fff3-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="6fff3-133">Ssindex .cmd</span><span class="sxs-lookup"><span data-stu-id="6fff3-133">Ssindex.cmd</span></span> | <span data-ttu-id="6fff3-134">此腳本會建立簽入原始檔控制中的檔案清單，以及每個檔案的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="6fff3-135">它會在您建立應用程式時產生的 .pdb 檔案中儲存這項資訊的子集。</span><span class="sxs-lookup"><span data-stu-id="6fff3-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="6fff3-136">腳本會使用下列其中一個 Perl 模組來與原始檔控制互動： P4.pm (Perforce) 或 Vss.pm (Visual Source Safe) 。如需詳細資訊，請使用-？執行腳本。</span><span class="sxs-lookup"><span data-stu-id="6fff3-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="6fff3-137">或-??</span><span class="sxs-lookup"><span data-stu-id="6fff3-137">or -??</span></span> <span data-ttu-id="6fff3-138"> (詳細資訊說明) 選項或檢查腳本。</span><span class="sxs-lookup"><span data-stu-id="6fff3-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6fff3-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="6fff3-139">Srctool.exe</span></span> | <span data-ttu-id="6fff3-140">此公用程式會列出在 .pdb 檔案中建立索引的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="6fff3-141">它會針對每個檔案列出檔案的完整路徑、原始檔控制伺服器和版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6fff3-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="6fff3-142">您可以使用此資訊來取出檔案，而不需要使用來源伺服器。如需詳細資訊，請使用/？執行公用程式。</span><span class="sxs-lookup"><span data-stu-id="6fff3-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="6fff3-143">選項。</span><span class="sxs-lookup"><span data-stu-id="6fff3-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6fff3-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="6fff3-144">Pdbstr.exe</span></span>  | <span data-ttu-id="6fff3-145">索引腳本會使用此公用程式，將版本控制資訊插入目標 .pdb 檔案的 "srcsrv" 替代資料流程中。</span><span class="sxs-lookup"><span data-stu-id="6fff3-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="6fff3-146">它也可以從 .pdb 檔案讀取任何資料流程。</span><span class="sxs-lookup"><span data-stu-id="6fff3-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="6fff3-147">您可以使用此資訊來確認索引腳本是否正常運作。如需詳細資訊，請使用/？執行公用程式。</span><span class="sxs-lookup"><span data-stu-id="6fff3-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="6fff3-148">選項。</span><span class="sxs-lookup"><span data-stu-id="6fff3-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="6fff3-149">正在抓取來源檔案</span><span class="sxs-lookup"><span data-stu-id="6fff3-149">Retrieving the Source File</span></span>

<span data-ttu-id="6fff3-150">DbgHelp API 可讓您透過 [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) 函數存取來源伺服器功能。</span><span class="sxs-lookup"><span data-stu-id="6fff3-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="6fff3-151">若要抓取要抓取之原始程式檔的名稱，請呼叫 [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) 或 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) 函數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="6fff3-152">使用來源伺服器搭配偵錯工具</span><span class="sxs-lookup"><span data-stu-id="6fff3-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="6fff3-153">若要使用具有 WinDbg、KD、NTSD 或 CDB 的來源伺服器，請確定您已安裝適用于 Windows 封裝 (6.3 版或更新版本的偵錯工具) 。</span><span class="sxs-lookup"><span data-stu-id="6fff3-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="6fff3-154">然後，將 srv 包含 \* 在 srcpath 命令中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6fff3-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="6fff3-155">**\. srcpath srv \* ;**_c： \\ mysource_</span><span class="sxs-lookup"><span data-stu-id="6fff3-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="6fff3-156">請注意，此範例也包含傳統的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="6fff3-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="6fff3-157">如果偵錯工具無法從來源伺服器取得檔案，則會搜尋指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="6fff3-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="6fff3-158">如果來源檔案是由來源伺服器抓取，則在偵錯工具結束後，它會保留在硬碟上。</span><span class="sxs-lookup"><span data-stu-id="6fff3-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="6fff3-159">原始程式檔會儲存在本機的偵錯工具的 src 子目錄中（適用于 Windows 安裝目錄）。</span><span class="sxs-lookup"><span data-stu-id="6fff3-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="6fff3-160">來源伺服器資料區塊</span><span class="sxs-lookup"><span data-stu-id="6fff3-160">Source Server Data Blocks</span></span>

<span data-ttu-id="6fff3-161">來源伺服器依賴 PDB 檔案中的兩個數據區塊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="6fff3-162">原始檔案清單。</span><span class="sxs-lookup"><span data-stu-id="6fff3-162">Source file list.</span></span> <span data-ttu-id="6fff3-163">建立模組會自動建立用來建立模組之原始程式檔的完整路徑清單。</span><span class="sxs-lookup"><span data-stu-id="6fff3-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="6fff3-164">資料區塊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-164">Data block.</span></span> <span data-ttu-id="6fff3-165">如先前所述對來源進行索引編制，會將替代資料流程新增至名為 "srcsrv" 的 PDB 檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="6fff3-166">插入此資料的腳本取決於特定的組建進程和使用中的原始檔控制系統。</span><span class="sxs-lookup"><span data-stu-id="6fff3-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="6fff3-167">在語言規格第1版中，資料區塊分成三個區段： ini、變數和原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="6fff3-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="6fff3-168">它有下列語法。</span><span class="sxs-lookup"><span data-stu-id="6fff3-168">It has the following syntax.</span></span>

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

<span data-ttu-id="6fff3-169">除了以百分比符號括住的文字 (% ) 之外，所有文字都會以字面方式解讀。</span><span class="sxs-lookup"><span data-stu-id="6fff3-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="6fff3-170">以百分比符號括住的文字會被視為要以遞迴方式解析的變數名稱，除非它是下列其中一項功能：</span><span class="sxs-lookup"><span data-stu-id="6fff3-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="6fff3-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>% fnvar% () </span><span class="sxs-lookup"><span data-stu-id="6fff3-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-172">參數文字應以百分比符號括住，並視為要展開的變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>% fnbksl% () </span><span class="sxs-lookup"><span data-stu-id="6fff3-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-174">參數文字中 (/) 的所有正斜線都應取代為 () 的反斜線 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6fff3-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>% fnfile% () </span><span class="sxs-lookup"><span data-stu-id="6fff3-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-176">參數文字中的所有路徑資訊都應該移除，只留下檔案名。</span><span class="sxs-lookup"><span data-stu-id="6fff3-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="6fff3-177">Ini 區段包含描述需求的變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="6fff3-178">索引腳本可以將任意數目的變數加入此區段。</span><span class="sxs-lookup"><span data-stu-id="6fff3-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="6fff3-179">範例如下：</span><span class="sxs-lookup"><span data-stu-id="6fff3-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="6fff3-180"><span id="VERSION"></span><span id="version"></span>版本</span><span class="sxs-lookup"><span data-stu-id="6fff3-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-181">語言規格版本。</span><span class="sxs-lookup"><span data-stu-id="6fff3-181">The language specification version.</span></span> <span data-ttu-id="6fff3-182">這是必要變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span><span class="sxs-lookup"><span data-stu-id="6fff3-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-184">描述原始檔控制產品的字串。</span><span class="sxs-lookup"><span data-stu-id="6fff3-184">A string that describes the source control product.</span></span> <span data-ttu-id="6fff3-185">這個變數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fff3-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-186"><span id="DATETIME"></span><span id="datetime"></span>Datetime</span><span class="sxs-lookup"><span data-stu-id="6fff3-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-187">字串，表示 PDB 檔案的處理日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6fff3-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="6fff3-188">這個變數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fff3-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="6fff3-189">Variables 區段包含的變數，可描述如何從原始檔控制中解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="6fff3-190">它也可以用來將常用的文字定義為變數，以縮減資料區塊的大小。</span><span class="sxs-lookup"><span data-stu-id="6fff3-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="6fff3-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span><span class="sxs-lookup"><span data-stu-id="6fff3-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-192">說明如何建立解壓縮檔案的目標路徑。</span><span class="sxs-lookup"><span data-stu-id="6fff3-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="6fff3-193">這是必要的變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span><span class="sxs-lookup"><span data-stu-id="6fff3-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-195">描述如何建立命令以從原始檔控制中解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="6fff3-196">這包括可執行檔及其命令列參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fff3-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="6fff3-197">這是必要的變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span><span class="sxs-lookup"><span data-stu-id="6fff3-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-199">字串，列出要在檔案解壓縮期間建立的環境變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="6fff3-200">以倒退鍵字元分隔多個專案 (\\ b) 。</span><span class="sxs-lookup"><span data-stu-id="6fff3-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="6fff3-201">這是選擇性變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="6fff3-202">[來源檔案] 區段包含已編制索引之每個原始程式檔的專案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="6fff3-203">每一行的內容都會轉譯為具有 VAR1、VAR2、VAR3 等名稱的變數，直到 VAR10 為止。</span><span class="sxs-lookup"><span data-stu-id="6fff3-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="6fff3-204">變數以星號分隔。</span><span class="sxs-lookup"><span data-stu-id="6fff3-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="6fff3-205">VAR1 必須指定來源檔案的完整路徑，如 PDB 檔案中的其他位置所列。</span><span class="sxs-lookup"><span data-stu-id="6fff3-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="6fff3-206">例如，下列程式程式碼：</span><span class="sxs-lookup"><span data-stu-id="6fff3-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="6fff3-207">解釋如下：</span><span class="sxs-lookup"><span data-stu-id="6fff3-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="6fff3-208">在此範例中，VAR4 是版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6fff3-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="6fff3-209">不過，大部分的原始檔控制系統都支援以標記檔案的方式來還原指定組建的來源狀態。</span><span class="sxs-lookup"><span data-stu-id="6fff3-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="6fff3-210">因此，您可以另外使用組建的標籤。</span><span class="sxs-lookup"><span data-stu-id="6fff3-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="6fff3-211">您可以修改範例資料區塊，以包含如下所示的變數：</span><span class="sxs-lookup"><span data-stu-id="6fff3-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="6fff3-212">然後，假設原始檔控制系統使用 at sign ( @ ) 來表示標籤，您可以修改 SRCSRVCMD 變數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6fff3-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="6fff3-213">**sd.exe-p% fnvar% (% var2% ) 列印-o% srcsrvtrg%-q% 倉庫%/%var3% @% label%**</span><span class="sxs-lookup"><span data-stu-id="6fff3-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="6fff3-214">來源伺服器的運作方式</span><span class="sxs-lookup"><span data-stu-id="6fff3-214">How Source Server Works</span></span>

<span data-ttu-id="6fff3-215">來源伺服器用戶端會在 Symsrv.dll 中執行。</span><span class="sxs-lookup"><span data-stu-id="6fff3-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="6fff3-216">用戶端不會直接從 PDB 檔案解壓縮資訊;它會使用一個符號處理常式，例如在 Dbghelp.dll 中執行的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6fff3-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="6fff3-217">它基本上是一個遞迴變數替代引擎，它會建立一個命令列，可用來從原始檔控制系統解壓縮適當的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="6fff3-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="6fff3-218">您的程式碼不應該直接呼叫 Symsrv.dll。</span><span class="sxs-lookup"><span data-stu-id="6fff3-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="6fff3-219">若要將它的功能整合到您的應用程式中，請使用 [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) 函數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="6fff3-220">來源伺服器的第一個版本運作方式如下。</span><span class="sxs-lookup"><span data-stu-id="6fff3-220">The first version of source server works as follows.</span></span> <span data-ttu-id="6fff3-221">此行為在未來的版本中可能會變更。</span><span class="sxs-lookup"><span data-stu-id="6fff3-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="6fff3-222">用戶端會呼叫 **SrcSrvInit** 函式，並將目標路徑用作所有來源檔案提取的基底。</span><span class="sxs-lookup"><span data-stu-id="6fff3-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="6fff3-223">它會將此路徑儲存在 TARG 變數中。</span><span class="sxs-lookup"><span data-stu-id="6fff3-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="6fff3-224">用戶端會在載入模組 PDB 時從 PDB 解壓縮 Srcsrv 資料流程，並呼叫 **SrcSrvLoadModule** 函式將資料區塊傳遞給來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="6fff3-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="6fff3-225">當 Dbghelp 抓取來源檔案時，用戶端會呼叫 **SrcSrvGetFile** 函式，以從原始檔控制中取出原始檔。</span><span class="sxs-lookup"><span data-stu-id="6fff3-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="6fff3-226">來源伺服器會搜尋資料區塊中的原始程式檔專案，以尋找符合所要求檔案的專案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="6fff3-227">它會使用原始程式檔專案的內容，將 VAR1 填滿至 VAR *n* 。</span><span class="sxs-lookup"><span data-stu-id="6fff3-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="6fff3-228">接著，它會使用 VAR1 將 SRCSRVTRG 變數展開為 VAR *n*。</span><span class="sxs-lookup"><span data-stu-id="6fff3-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="6fff3-229">如果檔案已在這個位置中，它會將位置傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="6fff3-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="6fff3-230">否則，它會展開 SRCSRVCMD 變數，以建立從原始檔控制取出檔案並將它複製到目標位置所需的命令。</span><span class="sxs-lookup"><span data-stu-id="6fff3-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="6fff3-231">最後，它會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="6fff3-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="6fff3-232">建立原始檔控制提供者模組</span><span class="sxs-lookup"><span data-stu-id="6fff3-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="6fff3-233">來源伺服器包含 Perforce 的提供者模組 (p4.pm) 和 Visual Source Safe (vss.pm) 。</span><span class="sxs-lookup"><span data-stu-id="6fff3-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="6fff3-234">若要建立您自己的提供者模組，您必須執行下列一組介面。</span><span class="sxs-lookup"><span data-stu-id="6fff3-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="6fff3-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module：： SimpleUsage ()**</span><span class="sxs-lookup"><span data-stu-id="6fff3-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-236">目的：將簡單的模組使用資訊顯示為 STDOUT。</span><span class="sxs-lookup"><span data-stu-id="6fff3-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="6fff3-237">參數：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-237">Parameters: None</span></span>

<span data-ttu-id="6fff3-238">傳回值：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module：： VerboseUsage ()**</span><span class="sxs-lookup"><span data-stu-id="6fff3-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-240">目的：對 STDOUT 顯示深入的模組使用量資訊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="6fff3-241">參數：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-241">Parameters: None</span></span>

<span data-ttu-id="6fff3-242">傳回值：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module：： new (\@ CommandArguments)**</span><span class="sxs-lookup"><span data-stu-id="6fff3-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-244">目的：初始化提供者模組的實例。</span><span class="sxs-lookup"><span data-stu-id="6fff3-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="6fff3-245">參數： @ARGV SSIndex 未辨識為一般引數的所有引數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="6fff3-246">傳回值：可在後續作業中使用的參考。</span><span class="sxs-lookup"><span data-stu-id="6fff3-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref >GatherFileInformation ($SourcePath，$ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="6fff3-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-248">目的：讓模組收集 $SourcePath 參數所指定之目錄的必要來源索引資訊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="6fff3-249">模組不應該假設每個物件實例都只會呼叫這個專案一次，因為 SSIndex 可能會針對不同的路徑多次呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6fff3-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="6fff3-250">參數： (1) 包含要編制索引之來源的本機目錄。</span><span class="sxs-lookup"><span data-stu-id="6fff3-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="6fff3-251"> (2) 雜湊的參考，其中包含指定之 Srcsrv.ini 檔中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="6fff3-252">傳回值：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference、$FileEntry) = $objref->Microsoft.visualbasic.fileio.filesystem.getfileinfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="6fff3-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-254">目的：提供從原始檔控制系統解壓縮單一特定檔案的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="6fff3-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="6fff3-255">參數：完整檔案名</span><span class="sxs-lookup"><span data-stu-id="6fff3-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="6fff3-256">傳回值： (1) 解讀所傳回 $FileEntry 所需變數的雜湊參考。</span><span class="sxs-lookup"><span data-stu-id="6fff3-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="6fff3-257">SSIndex 會為單一 debug 檔案使用的每個來源檔案快取這些變數，以減少寫入來源索引資料流程的資訊量。</span><span class="sxs-lookup"><span data-stu-id="6fff3-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="6fff3-258"> (2) 要寫入來源索引資料流程的檔案專案，以允許 SrcSrv.dll 從原始檔控制中解壓縮此檔案。</span><span class="sxs-lookup"><span data-stu-id="6fff3-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="6fff3-259">這一行的確切格式是由原始檔控制系統所特有。</span><span class="sxs-lookup"><span data-stu-id="6fff3-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="6fff3-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-261">目的：提供描述性字串來識別使用者的原始檔控制提供者。</span><span class="sxs-lookup"><span data-stu-id="6fff3-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="6fff3-262">參數：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-262">Parameters: None</span></span>

<span data-ttu-id="6fff3-263">傳回值：原始檔控制系統的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="6fff3-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="6fff3-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**</span><span class="sxs-lookup"><span data-stu-id="6fff3-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="6fff3-265">目的：讓原始檔控制提供者將原始檔控制特定變數加入至每個偵錯工具的來來源資料流。</span><span class="sxs-lookup"><span data-stu-id="6fff3-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="6fff3-266">範例模組會使用這個方法來撰寫必要的解壓縮 \_ CMD 和解壓縮 \_ 目標變數。</span><span class="sxs-lookup"><span data-stu-id="6fff3-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="6fff3-267">參數：無</span><span class="sxs-lookup"><span data-stu-id="6fff3-267">Parameters: None</span></span>

<span data-ttu-id="6fff3-268">傳回值：來來源資料流變數的專案清單。</span><span class="sxs-lookup"><span data-stu-id="6fff3-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




