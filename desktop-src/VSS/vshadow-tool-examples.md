---
description: 深入瞭解： VShadow 工具範例
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: VShadow 工具範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690463"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="00360-103">VShadow 工具範例</span><span class="sxs-lookup"><span data-stu-id="00360-103">VShadow Tool Examples</span></span>

<span data-ttu-id="00360-104">下列範例示範如何使用 VShadow 工具來執行最常見的工作：</span><span class="sxs-lookup"><span data-stu-id="00360-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="00360-105">從 CMD 腳本存取陰影複製屬性</span><span class="sxs-lookup"><span data-stu-id="00360-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="00360-106">存取非持續性陰影複製</span><span class="sxs-lookup"><span data-stu-id="00360-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="00360-107">從陰影複製複製檔案</span><span class="sxs-lookup"><span data-stu-id="00360-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="00360-108">列舉陰影複製裝置上的所有檔案</span><span class="sxs-lookup"><span data-stu-id="00360-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="00360-109">匯入可轉移的陰影複製</span><span class="sxs-lookup"><span data-stu-id="00360-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="00360-110">包含寫入器或元件</span><span class="sxs-lookup"><span data-stu-id="00360-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="00360-111">排除寫入器或元件</span><span class="sxs-lookup"><span data-stu-id="00360-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="00360-112">使用 BreakSnapshotSetEx 方法的中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="00360-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="00360-113">如需命令列選項及其用法的完整清單，請參閱 [VShadow 工具和範例](vshadow-tool-and-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="00360-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="00360-114">從 CMD 腳本存取陰影複製屬性</span><span class="sxs-lookup"><span data-stu-id="00360-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="00360-115">如果您在建立陰影複製時使用 **-script** 選擇性旗標，VShadow 會建立 CMD 腳本檔案，其中包含與新建立的陰影複製相關的環境變數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="00360-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="00360-116">陰影複製集識別碼，儲存在% VSHADOW \_ set \_ id% 環境變數中</span><span class="sxs-lookup"><span data-stu-id="00360-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="00360-117">陰影複製識別碼，儲存在格式為% VSHADOW \_ ID NNN% 的變數中 \_ \*\*，其中 *NNN* 代表 VSHADOW 命令列中來源磁片區的索引</span><span class="sxs-lookup"><span data-stu-id="00360-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="00360-118">陰影複製裝置名稱，儲存在表單% VSHADOW \_ 裝置 NNN% 的變數中 \_ \*\*，其中 *NNN* 是 VSHADOW 命令列中來源磁片區的索引</span><span class="sxs-lookup"><span data-stu-id="00360-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="00360-119">您可以使用產生的 CMD 檔案，對陰影複製執行有限的管理作業。</span><span class="sxs-lookup"><span data-stu-id="00360-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="00360-120">[**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)寫入器事件會在執行 **-exec** 腳本之後傳送。</span><span class="sxs-lookup"><span data-stu-id="00360-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="00360-121">VSS 會呼叫 **>ivssbackupcomponents：： BackupComplete** 方法，以向寫入器告知備份已完成，而寫入器可能會在此時截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="00360-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="00360-122">因此，請務必確認陰影/備份確實已完成。</span><span class="sxs-lookup"><span data-stu-id="00360-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="00360-123">如果備份失敗，您可以在執行的腳本/命令中傳回非零的結束代碼，以取消建立進程。</span><span class="sxs-lookup"><span data-stu-id="00360-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="00360-124"> (在 [Windows 命令列參考](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))中參閱結束命令的檔。 ) 如果自訂命令傳回非零結束代碼，則會取消陰影複製建立，且不會呼叫 **>ivssbackupcomponents：： BackupComplete** 。</span><span class="sxs-lookup"><span data-stu-id="00360-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="00360-125">下列範例顯示如何從命令列建立持續性陰影複製，並使用 CMD 腳本來公開它。</span><span class="sxs-lookup"><span data-stu-id="00360-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="00360-126">**vshadow-p-nw-script = SETVAR1 .cmd c：**</span><span class="sxs-lookup"><span data-stu-id="00360-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="00360-127">**呼叫 SETVAR1 .cmd**</span><span class="sxs-lookup"><span data-stu-id="00360-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="00360-128">**C： \\>vshadow-el =% vshadow \_ ID \_ 1%，c： \\ directory1**</span><span class="sxs-lookup"><span data-stu-id="00360-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="00360-129">存取非持續性陰影複製</span><span class="sxs-lookup"><span data-stu-id="00360-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="00360-130">在此情況下，非持續性陰影複製會在建立它們的程式 (時自動刪除，VShadow) 結束。</span><span class="sxs-lookup"><span data-stu-id="00360-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="00360-131">若要存取這些陰影複製的內容，VShadow 可以讓您在建立陰影複製之後，但在 VShadow 程式結束之前執行腳本。</span><span class="sxs-lookup"><span data-stu-id="00360-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="00360-132">下列範例顯示如何使用-exec 命令列選項來執行名為 "enum" 的腳本：</span><span class="sxs-lookup"><span data-stu-id="00360-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="00360-133">**vshadow-nw-exec = enum c：**</span><span class="sxs-lookup"><span data-stu-id="00360-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="00360-134">在執行的腳本中，您也可以在這個自訂命令中執行產生的 SETVAR 腳本。</span><span class="sxs-lookup"><span data-stu-id="00360-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="00360-135">這可讓腳本直接存取陰影複製的內容。</span><span class="sxs-lookup"><span data-stu-id="00360-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="00360-136">請記住，您可以從 VSHADOW \_ 裝置 NNN 環境變數中取出陰影裝置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="00360-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="00360-137">以下是範例列舉 .cmd 腳本：</span><span class="sxs-lookup"><span data-stu-id="00360-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="00360-138">以下是用來執行列舉 .cmd 腳本的命令列：</span><span class="sxs-lookup"><span data-stu-id="00360-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="00360-139">**vshadow-nw-exec = c： \\ enum。 cmd-script = setvar1 .cmd c：**</span><span class="sxs-lookup"><span data-stu-id="00360-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="00360-140">從陰影複製複製檔案</span><span class="sxs-lookup"><span data-stu-id="00360-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="00360-141">下列範例顯示如何從陰影複製複製檔案。</span><span class="sxs-lookup"><span data-stu-id="00360-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="00360-142">**dir > c： \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="00360-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="00360-143">**vshadow-p-nw-script = SETVAR1 .cmd c：**</span><span class="sxs-lookup"><span data-stu-id="00360-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="00360-144">**呼叫 SETVAR1 .cmd**</span><span class="sxs-lookup"><span data-stu-id="00360-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="00360-145">**複製% VSHADOW \_ DEVICE \_ 1% \\somefile.txt c： \\ somefile.txt 之 \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="00360-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="00360-146">列舉陰影複製裝置上的所有檔案</span><span class="sxs-lookup"><span data-stu-id="00360-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="00360-147">下列範例顯示如何從批次檔列舉陰影複製裝置上的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="00360-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="00360-148">**dir > c： \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="00360-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="00360-149">**vshadow-p-nw-script = SETVAR1 .cmd c：**</span><span class="sxs-lookup"><span data-stu-id="00360-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="00360-150">**呼叫 SETVAR1 .cmd**</span><span class="sxs-lookup"><span data-stu-id="00360-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="00360-151">**若為/R% VSHADOW \_ 裝置 \_ 1%%% \\ i in (\*) 進行 @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="00360-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="00360-152">匯入可轉移的陰影複製</span><span class="sxs-lookup"><span data-stu-id="00360-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="00360-153">若要在一部電腦上建立可轉移的陰影複製，並將其匯入到另一部電腦上，您必須有兩部透過 SAN 設定連接 (的電腦) 至支援 VSS 硬體陰影複製的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="00360-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="00360-154">每部電腦上都必須安裝 VSS 硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="00360-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="00360-155">下列範例顯示如何建立和匯入陰影複製。</span><span class="sxs-lookup"><span data-stu-id="00360-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="00360-156">在命令提示字元下輸入下列命令，在電腦 A 上建立陰影複製集 (生產伺服器) ：</span><span class="sxs-lookup"><span data-stu-id="00360-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="00360-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="00360-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="00360-158">這不會公開電腦 A 上的任何陰影複製裝置。</span><span class="sxs-lookup"><span data-stu-id="00360-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="00360-159">將備份元件檔 (bc1.xml) 從電腦 A 複製到電腦 B。</span><span class="sxs-lookup"><span data-stu-id="00360-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="00360-160">輸入下列命令，以匯入電腦 B 上的陰影集合：</span><span class="sxs-lookup"><span data-stu-id="00360-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="00360-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="00360-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="00360-162">（選擇性）您可以將這些陰影複製公開為磁碟機號或裝載的資料夾。</span><span class="sxs-lookup"><span data-stu-id="00360-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="00360-163">此外，您可能會中斷陰影組，使新的陰影複製磁片區可讀寫。</span><span class="sxs-lookup"><span data-stu-id="00360-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="00360-164">若要將陰影集管理程式自動化，您可以使用 **-script** 命令列選項來產生包含陰影複製識別碼的 CMD 腳本。</span><span class="sxs-lookup"><span data-stu-id="00360-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="00360-165">然後，您可以將產生的腳本連同備份元件複製到另一部電腦上。</span><span class="sxs-lookup"><span data-stu-id="00360-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="00360-166">下列範例示範如何使用 CMD 腳本建立、公開及中斷可轉移的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="00360-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="00360-167">從命令列 (生產伺服器) 建立電腦 A 上的陰影複製集，如下所示：</span><span class="sxs-lookup"><span data-stu-id="00360-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="00360-168">**vshadow-p-t =bc1.xml-script = sc1 .cmd**</span><span class="sxs-lookup"><span data-stu-id="00360-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="00360-169">指定 **-script** 選項以產生包含適當環境變數定義的腳本。</span><span class="sxs-lookup"><span data-stu-id="00360-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="00360-170">請注意，這不會公開電腦 A 上的任何陰影複製裝置。</span><span class="sxs-lookup"><span data-stu-id="00360-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="00360-171">將備份元件檔 (bc1.xml) 和產生的腳本 (sc1 從電腦 A) 到電腦 B。</span><span class="sxs-lookup"><span data-stu-id="00360-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="00360-172">輸入下列命令，以匯入電腦 B 上的陰影集合：</span><span class="sxs-lookup"><span data-stu-id="00360-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="00360-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="00360-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="00360-174">這會顯示電腦 B 上所建立的裝置。</span><span class="sxs-lookup"><span data-stu-id="00360-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="00360-175">執行產生的腳本，藉由在命令提示字元中輸入檔案名來設定陰影複製集的環境變數，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="00360-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="00360-176">**sc1 .cmd**</span><span class="sxs-lookup"><span data-stu-id="00360-176">**sc1.cmd**</span></span>

    <span data-ttu-id="00360-177">這會設定相關的環境變數，如從 CMD 腳本存取陰影複製屬性中所述。</span><span class="sxs-lookup"><span data-stu-id="00360-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="00360-178">輸入下列命令，以公開電腦 B 上的陰影複製：</span><span class="sxs-lookup"><span data-stu-id="00360-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="00360-179">**rmdir/s c： \\ 裝入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="00360-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="00360-180">**mkdir c： \\ 裝入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="00360-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="00360-181">**vshadow – el =% VSHADOW \_ ID \_ 1%，c： \\ 裝入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="00360-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="00360-182">這會呈現電腦 B 上所建立的陰影複製裝置。</span><span class="sxs-lookup"><span data-stu-id="00360-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="00360-183">輸入下列命令，以中斷陰影複製集，使磁片區可供寫入：**C： \\>vshadow – bw =% vshadow \_ set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="00360-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="00360-184">請注意，您也可以匯入非持續性的可轉移陰影複製，但在 **vshadow** **-i** 進程結束時，會自動將其刪除。</span><span class="sxs-lookup"><span data-stu-id="00360-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="00360-185">若要在刪除陰影複製之前將其匯入，您必須使用「存取永久性陰影複製」中所述的 **-exec** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="00360-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="00360-186">包含寫入器或元件</span><span class="sxs-lookup"><span data-stu-id="00360-186">Including Writers or Components</span></span>

<span data-ttu-id="00360-187">依預設，所有寫入器都會參與陰影複製的建立。</span><span class="sxs-lookup"><span data-stu-id="00360-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="00360-188">若要判斷哪些寫入器和元件將包含在陰影複製集中，請使用 **-wm** 或 **-wm2-downloadbtn** 命令列選項，如 [清單寫入器狀態和中繼資料](vshadow-tool-and-sample.md)所述。</span><span class="sxs-lookup"><span data-stu-id="00360-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="00360-189">若要確認是否包含所有寫入器的元件，請使用下列任何格式的 **-wi-fi** 選擇性旗標：</span><span class="sxs-lookup"><span data-stu-id="00360-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="00360-190">**vshadow** **-wi-fi** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="00360-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="00360-191">**vshadow** **-wi-fi** \*\*\*\*「_寫入器名稱字串_*__* 」</span><span class="sxs-lookup"><span data-stu-id="00360-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="00360-192">**vshadow** **-wi-fi** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="00360-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="00360-193">**vshadow** **-wi-fi** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="00360-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="00360-194">若要確認是否包含特定的元件，請使用下列任何格式的 **-wi-fi** 選擇性旗標：</span><span class="sxs-lookup"><span data-stu-id="00360-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="00360-195">**vshadow** **-wi-fi** \*WriterName ***： \\** _LogicalPath_* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="00360-196">**vshadow** **-wi-fi** **"**_Writer Name String_*_"： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="00360-197">**vshadow** **-wi-fi** **{**_WriterID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="00360-198">**vshadow** **-wi-fi** **{**_InstanceID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="00360-199">下列範例示範如何使用 **-wi-fi** 選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="00360-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="00360-200">指定 *WriterName*： \\ *LogicalPath* \\ *ComponentName*：</span><span class="sxs-lookup"><span data-stu-id="00360-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="00360-201">**vshadow-wi-fi = "Registry Writer： \\ registry"**</span><span class="sxs-lookup"><span data-stu-id="00360-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="00360-202">指定 {*WriterID*}：</span><span class="sxs-lookup"><span data-stu-id="00360-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="00360-203">**vshadow-wi-fi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="00360-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="00360-204">指定一個以上的寫入器或元件：</span><span class="sxs-lookup"><span data-stu-id="00360-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="00360-205">**vshadow-wi-fi = "Registry Writer： \\ registry"-wi-fi = "COM + REGDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="00360-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="00360-206">排除寫入器或元件</span><span class="sxs-lookup"><span data-stu-id="00360-206">Excluding Writers or Components</span></span>

<span data-ttu-id="00360-207">若要排除所有寫入器，請在建立陰影複製時使用 **-nw** 選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="00360-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="00360-208">若要排除所有寫入器的元件，請使用下列任何格式的 **-wx** 選擇性旗標：</span><span class="sxs-lookup"><span data-stu-id="00360-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="00360-209">**vshadow** **-wx** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="00360-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="00360-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span><span class="sxs-lookup"><span data-stu-id="00360-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="00360-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="00360-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="00360-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="00360-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="00360-213">若要排除特定的元件，請使用下列任何一種格式的 **-wx** 選擇性旗標：</span><span class="sxs-lookup"><span data-stu-id="00360-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="00360-214">**vshadow** **-wx** \*WriterName ***： \\** _LogicalPath_* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="00360-215">**vshadow** **-wx** **"**_Writer Name String_*_"： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="00360-216">**vshadow** **-wx** **{**_WriterID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="00360-217">**vshadow** **-wx** **{**_InstanceID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="00360-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="00360-218">下列範例示範如何使用 **-wx** 選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="00360-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="00360-219">指定 *WriterName*： \\ *LogicalPath* \\ *ComponentName*：</span><span class="sxs-lookup"><span data-stu-id="00360-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="00360-220">**vshadow-wx = "Registry Writer： \\ registry"**</span><span class="sxs-lookup"><span data-stu-id="00360-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="00360-221">指定 {*WriterID*}：</span><span class="sxs-lookup"><span data-stu-id="00360-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="00360-222">**vshadow-wx = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="00360-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="00360-223">指定一個以上的寫入器或元件：</span><span class="sxs-lookup"><span data-stu-id="00360-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="00360-224">**vshadow-wx = "Registry Writer： \\ registry"-wx = "COM + REGDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="00360-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="00360-225">使用 BreakSnapshotSetEx 方法的中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="00360-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="00360-226">下列範例示範如何使用 **-bex** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="00360-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="00360-227">指定陰影複製 LUN 將會從主機遮罩：</span><span class="sxs-lookup"><span data-stu-id="00360-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="00360-228">**vshadow** **-bex** **-mask**</span><span class="sxs-lookup"><span data-stu-id="00360-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="00360-229">指定將陰影複製 LUN 公開給主機作為讀取/寫入磁片區：</span><span class="sxs-lookup"><span data-stu-id="00360-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="00360-230">**vshadow** **-bex** **-rw**</span><span class="sxs-lookup"><span data-stu-id="00360-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="00360-231">指定陰影複製 LUN 會以讀取/寫入磁片區的形式公開給主機，而且陰影複製 Lun 上的磁片簽章都不會還原為原始 Lun 的磁片簽章：</span><span class="sxs-lookup"><span data-stu-id="00360-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="00360-232">**vshadow** **-bex** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="00360-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
