---
description: BETest 是可測試 advanced backup 和 restore 作業的 VSS 要求者。
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: BETest 工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852652"
---
# <a name="betest-tool"></a><span data-ttu-id="661d7-103">BETest 工具</span><span class="sxs-lookup"><span data-stu-id="661d7-103">BETest Tool</span></span>

<span data-ttu-id="661d7-104">BETest 是可測試 advanced backup 和 restore 作業的 VSS 要求者。</span><span class="sxs-lookup"><span data-stu-id="661d7-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="661d7-105">此工具可用來測試應用程式使用複雜 VSS 功能的方式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="661d7-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="661d7-106">增量和差異備份</span><span class="sxs-lookup"><span data-stu-id="661d7-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="661d7-107">複雜還原選項，例如權威還原</span><span class="sxs-lookup"><span data-stu-id="661d7-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="661d7-108">向前復原選項</span><span class="sxs-lookup"><span data-stu-id="661d7-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="661d7-109">BETest 隨附于適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="661d7-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="661d7-110">VSS 7.2 SDK 包含的 BETest 版本只會在 Windows Server 2003 上執行。</span><span class="sxs-lookup"><span data-stu-id="661d7-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="661d7-111">本主題說明 BETest 的 Windows SDK 版本，而不是 VSS 7.2 SDK 中包含的 Windows Server 2003 版本。</span><span class="sxs-lookup"><span data-stu-id="661d7-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="661d7-112">如需下載 Windows SDK 和 VSS 7.2 SDK 的詳細資訊，請參閱 [磁碟區陰影複製服務](volume-shadow-copy-service-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="661d7-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="661d7-113">在 Windows SDK 安裝中，您可以在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 位 windows) 的 (和 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 位 windows) 的 (中找到 BETest 工具。</span><span class="sxs-lookup"><span data-stu-id="661d7-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="661d7-114">執行 BETest 工具</span><span class="sxs-lookup"><span data-stu-id="661d7-114">Running the BETest Tool</span></span>

<span data-ttu-id="661d7-115">若要從命令列執行 BETest 工具，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="661d7-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="661d7-116">**BETest** *命令列選項*</span><span class="sxs-lookup"><span data-stu-id="661d7-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="661d7-117">下列使用範例示範如何搭配使用 BETest 工具與 [Vss 測試編寫器工具](vss-test-writer-tool.md)，這是 vss 寫入器工具。</span><span class="sxs-lookup"><span data-stu-id="661d7-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="661d7-118">**BETest 工具使用範例**</span><span class="sxs-lookup"><span data-stu-id="661d7-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="661d7-119">建立名為 C： BETest 的測試目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="661d7-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="661d7-120">將下列檔案複製到此目錄中：</span><span class="sxs-lookup"><span data-stu-id="661d7-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="661d7-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="661d7-121">betest.exe</span></span>
    -   <span data-ttu-id="661d7-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="661d7-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="661d7-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="661d7-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="661d7-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="661d7-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="661d7-125">建立名為 C： TestPath 的目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="661d7-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="661d7-126">將部分測試資料檔案放在此目錄中。</span><span class="sxs-lookup"><span data-stu-id="661d7-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="661d7-127">建立名為 C： BackupDestination 的目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="661d7-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="661d7-128">將此目錄保留空白。</span><span class="sxs-lookup"><span data-stu-id="661d7-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="661d7-129">開啟兩個提高許可權的命令視窗，並將每個的工作目錄設定為 C： \\ BETest。</span><span class="sxs-lookup"><span data-stu-id="661d7-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="661d7-130">在第一個命令視窗中，啟動 [VSS 測試寫入器工具](vss-test-writer-tool.md) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="661d7-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="661d7-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="661d7-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="661d7-132">vswriterSample.xml 的檔案會設定 VSS 測試寫入器工具 (vswriter) 來報告 c： TestPath 目錄的內容，以 \\ 準備備份作業。</span><span class="sxs-lookup"><span data-stu-id="661d7-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="661d7-133">請注意，在偵測到來自要求者（例如 BETest）的活動之前，VSS 測試寫入器工具將不會產生輸出。</span><span class="sxs-lookup"><span data-stu-id="661d7-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="661d7-134">若要停止 VSS 測試編寫器工具，請按 CTRL + C。</span><span class="sxs-lookup"><span data-stu-id="661d7-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="661d7-135">在第二個命令視窗中，使用 BETest 工具來執行備份作業，如下所示：</span><span class="sxs-lookup"><span data-stu-id="661d7-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="661d7-136">**betest.exe/B/S backup.xml/D C： \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="661d7-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="661d7-137">BETest 會將檔從 C： \\ TestPath 目錄備份到 c： \\ BackupDestination 目錄。</span><span class="sxs-lookup"><span data-stu-id="661d7-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="661d7-138">它會將備份元件檔儲存至 C： \\ BETest \\backup.xml。</span><span class="sxs-lookup"><span data-stu-id="661d7-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="661d7-139">如果備份作業成功，請刪除 C： \\ TestPath 目錄的內容，並使用 BETest 工具來執行還原作業，如下所示：</span><span class="sxs-lookup"><span data-stu-id="661d7-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="661d7-140">**betest.exe/R/S backup.xml/D C： \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="661d7-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="661d7-141">BETest 工具 Command-Line 選項</span><span class="sxs-lookup"><span data-stu-id="661d7-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="661d7-142">BETest 工具會使用下列命令列選項來識別要執行的工作。</span><span class="sxs-lookup"><span data-stu-id="661d7-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="661d7-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="661d7-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-144">針對 Active Directory 或 Active Directory 應用程式模式執行授權還原作業。</span><span class="sxs-lookup"><span data-stu-id="661d7-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="661d7-145">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-146"><span id="_B"></span><span id="_b"></span>**後退**</span><span class="sxs-lookup"><span data-stu-id="661d7-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-147">執行備份操作，但不執行還原。</span><span class="sxs-lookup"><span data-stu-id="661d7-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="661d7-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-149">只執行備份完成作業。</span><span class="sxs-lookup"><span data-stu-id="661d7-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="661d7-150">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="661d7-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="661d7-152">此命令列選項僅提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="661d7-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="661d7-153">您應該改為使用 **/x** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="661d7-154">根據 *檔案名* 所指定的設定檔內容，選取要備份或還原的元件。</span><span class="sxs-lookup"><span data-stu-id="661d7-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="661d7-155">這個檔案必須只包含0到127範圍內的 ANSI 字元，而且必須大於 1 MB。</span><span class="sxs-lookup"><span data-stu-id="661d7-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="661d7-156">檔案中的每一行都必須使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="661d7-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="661d7-157">*WriterId* ： *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="661d7-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="661d7-158">其中 *WriterId* 是寫入器識別碼，而 *ComponentName* 是其中一個寫入器元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="661d7-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="661d7-159">寫入器識別碼和元件名稱必須以引號括住，而且在冒號 (： ) 之前和之後必須有空格。</span><span class="sxs-lookup"><span data-stu-id="661d7-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="661d7-160">如果指定了兩個以上的元件，則必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="661d7-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="661d7-161">例如：</span><span class="sxs-lookup"><span data-stu-id="661d7-161">For example:</span></span>

<span data-ttu-id="661d7-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="661d7-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="661d7-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *路徑*</span><span class="sxs-lookup"><span data-stu-id="661d7-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="661d7-164">儲存備份的檔案，或從 *Path* 指定的備份目錄還原這些檔案。</span><span class="sxs-lookup"><span data-stu-id="661d7-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="661d7-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-166">省略備份完成作業。</span><span class="sxs-lookup"><span data-stu-id="661d7-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="661d7-167">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="661d7-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-169">指定備份包含可開機的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="661d7-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="661d7-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-171">建立持續性陰影複製。</span><span class="sxs-lookup"><span data-stu-id="661d7-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="661d7-172">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="661d7-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="661d7-174">如果在 **/t** 命令列選項中指定的備份類型是 [增量] 或 [差異]，請將備份檔案設定為 [ *檔案名* ] 所指定的檔案，以用於先前的完整或增量備份。</span><span class="sxs-lookup"><span data-stu-id="661d7-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="661d7-175">**Windows Server 2003 和 WINDOWS XP：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="661d7-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-177">執行還原，但不執行備份。</span><span class="sxs-lookup"><span data-stu-id="661d7-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="661d7-178">必須與 **/s** 命令列選項一起使用。</span><span class="sxs-lookup"><span data-stu-id="661d7-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="661d7-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-180">建立可用於應用程式復原的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="661d7-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="661d7-181">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="661d7-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="661d7-183">如果是備份，請將備份檔案儲存至 *檔案名* 所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="661d7-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="661d7-184">如果只還原，則會從這個檔案載入備份檔案。</span><span class="sxs-lookup"><span data-stu-id="661d7-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="661d7-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-186">建立磁片區陰影複製，但不執行備份或還原。</span><span class="sxs-lookup"><span data-stu-id="661d7-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="661d7-187">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="661d7-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-189">發生第一個寫入器錯誤時停止 BETest。</span><span class="sxs-lookup"><span data-stu-id="661d7-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="661d7-190">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span><span class="sxs-lookup"><span data-stu-id="661d7-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="661d7-192">指定備份類型。</span><span class="sxs-lookup"><span data-stu-id="661d7-192">Specifies the backup type.</span></span> <span data-ttu-id="661d7-193">*BackupType* 可以是 FULL、LOG、COPY、增量或差異。</span><span class="sxs-lookup"><span data-stu-id="661d7-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="661d7-194">如需備份類型的詳細資訊，請參閱 [**VSS \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)。</span><span class="sxs-lookup"><span data-stu-id="661d7-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="661d7-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="661d7-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="661d7-196">產生可用於疑難排解的詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="661d7-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="661d7-197">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="661d7-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="661d7-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="661d7-199">根據 *Filename* 指定的 XML 設定檔內容，選取要備份或還原的元件。</span><span class="sxs-lookup"><span data-stu-id="661d7-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="661d7-200">這個檔案必須只包含0到127範圍內的 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="661d7-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="661d7-201">XML 檔案的格式是由 BETest.xml 檔案中的架構所定義。</span><span class="sxs-lookup"><span data-stu-id="661d7-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="661d7-202">如需範例設定檔，請參閱 BetestSample.xml。</span><span class="sxs-lookup"><span data-stu-id="661d7-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="661d7-203">這兩個檔案都在 vsstools 目錄中。</span><span class="sxs-lookup"><span data-stu-id="661d7-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="661d7-204">您可以在 Internet Explorer 中查看 BETest.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="661d7-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="661d7-205">開啟這個檔案之前，請確定 xdr-schema 與 BETest.xml 在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="661d7-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="661d7-206">Xdr-schema xsl 檔案包含轉譯指令，可讓 BETest.xml 檔案更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="661d7-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="661d7-207">**Windows Server 2003：** 不支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="661d7-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="661d7-208">範例 XML 設定檔： BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="661d7-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="661d7-209">下列範例設定檔 BetestSample.xml 可在 Vsstools 目錄中找到。</span><span class="sxs-lookup"><span data-stu-id="661d7-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="661d7-210">此簡單設定檔的範例會選取要備份或還原的一個元件。</span><span class="sxs-lookup"><span data-stu-id="661d7-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="661d7-211">範例 XML 設定檔： VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="661d7-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="661d7-212">下列範例設定檔 VswriterSample.xml 可在 Vsstools 目錄中找到。</span><span class="sxs-lookup"><span data-stu-id="661d7-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="661d7-213">此設定檔中的根項目命名為 TestWriter。</span><span class="sxs-lookup"><span data-stu-id="661d7-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="661d7-214">所有其他專案會排列在 TestWriter 元素之下。</span><span class="sxs-lookup"><span data-stu-id="661d7-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="661d7-215">與 TestWriter 相關聯的第一個屬性是 usage 屬性。</span><span class="sxs-lookup"><span data-stu-id="661d7-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="661d7-216">這個屬性會指定透過 [**IVssExamineWriterMetadata：： GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) 方法回報的使用類型。</span><span class="sxs-lookup"><span data-stu-id="661d7-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="661d7-217">此屬性的其中一個可能值為使用者 \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="661d7-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="661d7-218">第二個屬性是 deleteFiles 屬性。</span><span class="sxs-lookup"><span data-stu-id="661d7-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="661d7-219">這個屬性會在設定 [寫入器屬性](vss-test-writer-tool.md)中說明。</span><span class="sxs-lookup"><span data-stu-id="661d7-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="661d7-220">根項目的第一個子項目是 RestoreMethod 元素。</span><span class="sxs-lookup"><span data-stu-id="661d7-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="661d7-221">這個元素會指定下列專案：</span><span class="sxs-lookup"><span data-stu-id="661d7-221">This element specifies the following:</span></span>

-   <span data-ttu-id="661d7-222">在此情況下，restore 方法 (， \_ 如果 \_ 可以 \_ 取代則還原 \_) </span><span class="sxs-lookup"><span data-stu-id="661d7-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="661d7-223">寫入器是否需要還原事件 (在此情況下，一律) </span><span class="sxs-lookup"><span data-stu-id="661d7-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="661d7-224">還原寫入器之後是否需要重新開機 (在此案例中為否) </span><span class="sxs-lookup"><span data-stu-id="661d7-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="661d7-225">這個元素可以選擇性地指定替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="661d7-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="661d7-226"> (在此案例中，未指定替代位置 ) 。如需詳細資訊，請參閱 [指定替代位置](vss-test-writer-tool.md)對應。</span><span class="sxs-lookup"><span data-stu-id="661d7-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="661d7-227">第二個子項目是元件元素。</span><span class="sxs-lookup"><span data-stu-id="661d7-227">The second child element is a Component element.</span></span> <span data-ttu-id="661d7-228">此元素會導致寫入器將元件新增至其中繼資料。</span><span class="sxs-lookup"><span data-stu-id="661d7-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="661d7-229">元件專案包含屬性，用來描述元件和子項目，以描述元件的內容，如下所示：</span><span class="sxs-lookup"><span data-stu-id="661d7-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="661d7-230">componentType，指出這是否為檔案群組或資料庫 (在此案例中為檔案群組) </span><span class="sxs-lookup"><span data-stu-id="661d7-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="661d7-231">logicalPath 元件邏輯路徑的在此案例中，未指定任何 () </span><span class="sxs-lookup"><span data-stu-id="661d7-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="661d7-232">componentName：在此案例中為元件名稱 ("TestFiles" ) </span><span class="sxs-lookup"><span data-stu-id="661d7-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="661d7-233">可選取以指出可選取的備份狀態</span><span class="sxs-lookup"><span data-stu-id="661d7-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="661d7-234">Component 元素也有一個名為 ComponentFile 的子專案，可將檔案規格新增至此元件。</span><span class="sxs-lookup"><span data-stu-id="661d7-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="661d7-235"> (元件元素可以有任意數目的 ComponentFile 元素，可為每個元件指定。 ) 此 ComponentFile 元素具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="661d7-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="661d7-236">path = "c： \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="661d7-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="661d7-237">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="661d7-237">filespec="\*"</span></span>
-   <span data-ttu-id="661d7-238">遞迴 = "no"</span><span class="sxs-lookup"><span data-stu-id="661d7-238">recursive="no"</span></span>

 

 



