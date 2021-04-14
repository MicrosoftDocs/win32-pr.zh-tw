---
description: VShadow 是一種命令列工具，可讓您用來建立和管理磁片區陰影複製。
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: VShadow 工具和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469100"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="a0dcc-103">VShadow 工具和範例</span><span class="sxs-lookup"><span data-stu-id="a0dcc-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="a0dcc-104">VShadow 是一種命令列工具，可讓您用來建立和管理磁片區陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-105">VShadow 隨附于適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="a0dcc-106">VSS 7.2 SDK 包含的 VShadow 版本只會在 Windows Server 2003 上執行。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="a0dcc-107">如需下載 Windows SDK 和 VSS 7.2 SDK 的詳細資訊，請參閱 [磁碟區陰影複製服務](volume-shadow-copy-service-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="a0dcc-108">VShadow 工具會使用命令列選項和選擇性旗標來識別要執行的工作。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="a0dcc-109">使用時若沒有任何命令列選項，VShadow 命令會建立新的陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="a0dcc-110">VShadow 命令會執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="a0dcc-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="a0dcc-111">建立陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="a0dcc-112">匯入陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="a0dcc-113">查詢陰影複製屬性</span><span class="sxs-lookup"><span data-stu-id="a0dcc-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="a0dcc-114">刪除陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="a0dcc-115">中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="a0dcc-116">使用 BreakSnapshotSetEx 方法中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="a0dcc-117">在本機公開陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="a0dcc-118">遠端公開陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="a0dcc-119">列出寫入器狀態和中繼資料</span><span class="sxs-lookup"><span data-stu-id="a0dcc-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="a0dcc-120">執行還原作業</span><span class="sxs-lookup"><span data-stu-id="a0dcc-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="a0dcc-121">還原為先前的陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="a0dcc-122">重新同步處理 Lun</span><span class="sxs-lookup"><span data-stu-id="a0dcc-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="a0dcc-123">建立陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="a0dcc-124">**vshadow** \[OptionalFlags \] *VolumeList*</span><span class="sxs-lookup"><span data-stu-id="a0dcc-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="a0dcc-125">此命令會建立新的陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="a0dcc-126">*VolumeList* 是磁片區名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="a0dcc-127">VShadow 會為清單中的每個磁片區建立一個陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="a0dcc-128">您可以選擇性地以反斜線 () 來終止磁片區名稱 \\ 。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="a0dcc-129">例如，C：和 C： \\ 都是有效的磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="a0dcc-130">您也可以指定裝載的資料夾 (例如，C： \\ DirectoryName) 或磁片區 GUID 名稱 (例如 \\ \\ ？ \\磁片區 {edbed95e-7e8d-11d8-9d01-505054503030} ) 。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="a0dcc-131">*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0dcc-132">選擇性旗標值</span><span class="sxs-lookup"><span data-stu-id="a0dcc-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="a0dcc-133">Description</span><span class="sxs-lookup"><span data-stu-id="a0dcc-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0dcc-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-135">此選擇性旗標指定差異硬體陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="a0dcc-136">此旗標和 <strong>-ap</strong> 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-137">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-139">此選擇性旗標指定了 plex 硬體陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="a0dcc-140">此旗標和 <strong>-ad</strong> 旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-141">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-bc =</strong><em>File</em><strong>.xml</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-143">這個選擇性旗標會指定不可傳送的陰影複製，並將備份元件檔儲存到指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="a0dcc-144">此檔案可用於後續的還原作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="a0dcc-145">此旗標和 <strong>-t</strong> 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-146">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>命令</em></span><span class="sxs-lookup"><span data-stu-id="a0dcc-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="a0dcc-148">這個選擇性旗標會在建立陰影複製之後，但在 VShadow 工具結束之前，執行命令或腳本。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="a0dcc-149"><em>命令</em> 可以指定可執行檔 shell 命令或 CMD 檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="a0dcc-150">如果指定了 shell 命令，就不能指定任何命令參數。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-151">為了安全起見，並讓執行保持簡單， <strong>-exec</strong> 選擇性旗標不會接受將參數傳遞給命令或腳本。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="a0dcc-152">傳遞至 <strong>-exec</strong> 選擇性旗標的整個字串會被視為單一的 CMD 或 EXE 檔案。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="a0dcc-153">如需這項限制的詳細資訊，請參閱 VShadow 原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-155">這個選擇性旗標會指定只有在可以還原所有磁片簽章時，才會完成陰影複製作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-156">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-157"><strong>Windows Server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-159">此選擇性旗標指定當陰影複製集中斷時，應該從電腦遮罩陰影複製 Lun。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-160">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-161"><strong>Windows Server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-163">這個選擇性旗標會指定不含自動復原的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="a0dcc-164">如需此選項的詳細資訊，請參閱 <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> 列舉之 VSS_VOLSNAP_ATTR_NO_AUTORECOVERY 旗標的檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-166">這個選擇性旗標指定不應復原磁碟簽章。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-167">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-168"><strong>Windows Server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-170">這個選擇性旗標會指定陰影複製，而不涉及寫入器。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="a0dcc-171">如需不含寫入器參與之陰影複製的詳細資訊，請參閱 <a href="shadow-copy-creation-details.md">陰影複製建立詳細資料</a>。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="a0dcc-172">此旗標和 <strong>-wi-fi</strong> 和 <strong>-wx</strong> 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-174">這個選擇性旗標會指定 <a href="vssgloss-p.md"><em>持續性陰影複製</em></a>。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-175">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-177">此選擇性旗標指定當陰影複製集中斷時，應該將陰影複製 Lun 設為讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-178">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-179"><strong>Windows Server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-181">這個選擇性旗標會指定 <a href="vssgloss-c.md"><em>用戶端可存取的陰影複製</em></a>。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-182">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em></em><strong>.cmd</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-184">這個選擇性旗標會產生 CMD 檔案，其中包含與建立的陰影複製相關的環境變數，例如陰影複製識別碼和陰影複製集識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>.xml</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-186">這個選擇性旗標會指定可轉移的陰影複製，並將備份元件檔儲存到 <em>File.xml</em> 參數所指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="a0dcc-187">此檔案可用於後續的匯入和/或還原作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="a0dcc-188">此旗標和 <strong>-bc</strong> 旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="a0dcc-189"><strong>Windows server 2003、Standard edition 和 Windows server 2003、Web edition：</strong> 不支援可轉移的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="a0dcc-190">所有版本的 Windows Server 2003 Service Pack 1 (SP1) 支援可轉移的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-192">這個選擇性旗標會指定在建立陰影複製時應該強制執行 TxF 復原。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-193">只有在 Windows server 作業系統上才支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-追蹤</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-195">這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-197">此選擇性旗標會在結束之前，讓 VShadow 工具等候使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi-fi =</strong><em>寫入器</em></span><span class="sxs-lookup"><span data-stu-id="a0dcc-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="a0dcc-199">這個選擇性旗標會驗證指定的寫入器或元件是否包含在陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="a0dcc-200"><em>寫入器</em> 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="a0dcc-201">此旗標和 <strong>-nw</strong> 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dcc-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx =</strong><em>Writer</em></span><span class="sxs-lookup"><span data-stu-id="a0dcc-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="a0dcc-203">這個選擇性旗標會驗證指定的寫入器或元件是否已從陰影複製中排除。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="a0dcc-204"><em>寫入器</em> 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="a0dcc-205">此旗標和 <strong>-nw</strong> 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="a0dcc-206">匯入陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="a0dcc-207">**vshadow** \[OptionalFlags \] **-i =**_File_*_.xml_*</span><span class="sxs-lookup"><span data-stu-id="a0dcc-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="a0dcc-208">**-I** 命令列選項會匯入可轉移的陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-209">只有在 Windows server 作業系統上才支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="a0dcc-210">*File.xml* 檔必須是以 **-t** 或 **-bc** 選擇性旗標建立之可轉移陰影複製集的備份元件檔檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="a0dcc-211">如果是以 **-p** 選擇性旗標建立的陰影複製集，則為 [*持續陰影複製*](vssgloss-p.md)。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="a0dcc-212">如果可轉移的陰影複製集為非持續性，則會在執行陰影複製建立命令時短暫出現，並在命令傳回時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="a0dcc-213">您只能在建立陰影複製時匯入非持續性陰影複製，方法是使用 **-exec** 選擇性旗標建立陰影複製集，以執行 **呼叫 VShadow 的** CMD 檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="a0dcc-214">**-I** 命令列選項不能與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="a0dcc-215">*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="a0dcc-216">選擇性旗標值</span><span class="sxs-lookup"><span data-stu-id="a0dcc-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="a0dcc-217">Description</span><span class="sxs-lookup"><span data-stu-id="a0dcc-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dcc-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_命令_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="a0dcc-219">這個選擇性旗標會在匯入陰影複製之後，但在 VShadow 工具結束之前，執行命令或腳本。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="a0dcc-220">*命令* 可以指定可執行檔 shell 命令或 CMD 檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="a0dcc-221">如果指定了 shell 命令，就不能指定任何命令參數。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="a0dcc-222"><span id="-tracing"></span><span id="-TRACING"></span>**-追蹤**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="a0dcc-223">這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="a0dcc-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="a0dcc-225">此選擇性旗標會在結束之前，讓 VShadow 工具等候使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="a0dcc-226">查詢陰影複製屬性</span><span class="sxs-lookup"><span data-stu-id="a0dcc-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="a0dcc-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-227">**vshadow** **-q**</span></span>

<span data-ttu-id="a0dcc-228">**vshadow** **-qx =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="a0dcc-229">**vshadow** **-s =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="a0dcc-230">**-Q** 命令列選項會列出電腦上所有陰影複製的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="a0dcc-231">**-Qx** 命令列選項會列出陰影複製集中所有陰影複製的屬性，其識別碼是由 *ShadowCopySetId* 所指定。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="a0dcc-232">**-S** 命令列選項會列出 *SHADOWCOPYID* 指定其識別碼的陰影複製屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="a0dcc-233">這些命令列選項使用 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) 和 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) 的組合來取得指定陰影複製集的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="a0dcc-234">**-Q**、 **-qx** 和 **-s** 命令列選項都是互斥的，且無法與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="a0dcc-235">刪除陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="a0dcc-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-236">**vshadow** **-da**</span></span>

<span data-ttu-id="a0dcc-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-237">**vshadow** **-do**</span></span>

<span data-ttu-id="a0dcc-238">**vshadow** **-dx =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="a0dcc-239">**vshadow** **-ds =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="a0dcc-240">**-Da** 命令會刪除電腦上的所有陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-241">**-Da** 命令列選項需要使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="a0dcc-242">**-Do** 命令列選項會刪除電腦上最舊的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="a0dcc-243">**-Dx** 命令列選項會刪除陰影複製集中的所有陰影複製，其識別碼是由 *ShadowCopySetId* 所指定。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="a0dcc-244">**-Ds** 命令列選項會刪除 *SHADOWCOPYID* 指定其識別碼的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="a0dcc-245">這些命令列選項僅適用于持續性 [*陰影複製*](vssgloss-p.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="a0dcc-246">非持續性陰影複製不需要明確刪除，因為它們會在 VShadow 建立命令結束時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="a0dcc-247">**-Da**、 **-do**、 **-dx** 和 **-ds** 命令列選項都是互斥的，且無法與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="a0dcc-248">中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="a0dcc-249">**vshadow** **-b =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="a0dcc-250">**vshadow** **-bw =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="a0dcc-251">**-B =**_ShadowCopySetId_ 命令列選項會將陰影複製集中的每個陰影複製轉換成獨立唯讀磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="a0dcc-252">**-Bw =**_ShadowCopySetId_ 命令列選項會將陰影複製集中的每個陰影複製轉換成獨立的可寫入磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-253">只有在 Windows server 作業系統上才支援 **-b** 和 **-bw** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="a0dcc-254">如需有關中斷陰影複製集的詳細資訊，請參閱 [中斷陰影](breaking-shadow-copies.md)複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="a0dcc-255">陰影複製組中斷之後，陰影複製組和個別的陰影複製就不存在，而且無法使用 VSS 命令來管理。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="a0dcc-256">如果是使用 **-p** 選擇性旗標建立陰影複製集，則其為持續性。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="a0dcc-257">如果可轉移的陰影複製集為非持續性，則會在執行陰影複製建立命令時短暫出現，並在命令傳回時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="a0dcc-258">您只能在建立陰影複製時中斷非持續性陰影複製集，方法是使用 **-exec** 選擇性旗標建立陰影複製集，以執行呼叫 **vshadow** **-b** 或 **vshadow** **bw** 的 CMD 檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="a0dcc-259">**-B** 和 **-bw** 命令列選項互斥，而且無法與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="a0dcc-260">使用 BreakSnapshotSetEx 方法中斷陰影複製集</span><span class="sxs-lookup"><span data-stu-id="a0dcc-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="a0dcc-261">**vshadow** **-bex**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="a0dcc-262">**-Bex** 命令列選項會根據選擇性 **遮罩**、 **-rw**、 **-forcerevert** 和 **-norevert** 旗標所指定的選項來中斷陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="a0dcc-263">此命令列選項類似于 **-b** 和 **-bw** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="a0dcc-264">**-Bex** 命令列選項會使用 [**IVssBackupComponentsEx2：： BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)方法，而 **-b** 和 **-bw** 命令列選項則使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)方法。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="a0dcc-265">如需有關中斷陰影複製集的詳細資訊，請參閱 [中斷陰影](breaking-shadow-copies.md)複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-266">只有在 Windows server 作業系統上才支援 **-bex** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="a0dcc-267">**vshadow** **-bex** **-mask**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="a0dcc-268">**遮罩** 旗標指定將從主機遮罩陰影複製 LUN。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="a0dcc-269">如果指定 **-mask** 旗標，則無法指定 **-rw**、 **-forcerevert** 和 **-norevert** 旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="a0dcc-270">**vshadow** **-bex** **-rw**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="a0dcc-271">**-Rw** 旗標指定將陰影複製 LUN 公開給主機，作為讀取/寫入磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="a0dcc-272">**vshadow** **-bex** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="a0dcc-273">**-Forcerevert** 旗標會指定所有陰影複製 lun 的磁片識別碼都會還原為原始 lun 的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="a0dcc-274">但是，如果有任何原始 Lun 存在於系統上，此作業將會失敗，而且不會還原任何識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="a0dcc-275">此旗標和 **-norevert** 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="a0dcc-276">**vshadow** **-bex** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="a0dcc-277">**-Norevert** 旗標指定不會還原任何陰影複製 LUN 磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="a0dcc-278">此旗標和 **-forcerevert** 旗標互斥。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="a0dcc-279">在本機公開陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="a0dcc-280">**vshadow** **-el =**_ShadowCopyId_*_、_*_LocalEmptyDirectory_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="a0dcc-281">**vshadow** **-el =**_ShadowCopyId_*_、_*_UnusedDriveLetter_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="a0dcc-282">**-El** 命令列選項會將掛接的資料夾或磁碟機號指派給持續性陰影複製。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="a0dcc-283">請注意，除非您後續呼叫 **vshadow** **-bw** 來中斷陰影複製集，否則磁片區內容將維持唯讀狀態。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-284">無法在本機公開非持續性陰影複製和 [*用戶端可存取的陰影複製*](vssgloss-c.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="a0dcc-285">例如，如果 {edbed95e-7e8d-11d8-9d01-505054503030} 是現有持續性陰影複製的 GUID，而 X：是未使用的磁碟機號，則下列命令會在 X 下公開陰影複製：</span><span class="sxs-lookup"><span data-stu-id="a0dcc-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="a0dcc-286">**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}，x：**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="a0dcc-287">下列範例示範如何在裝載的資料夾 C： ShadowCopies June23 下公開相同的陰影 \\ 複製 \\ ：</span><span class="sxs-lookup"><span data-stu-id="a0dcc-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="a0dcc-288">**mkdir c： \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="a0dcc-289">**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}，c： \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="a0dcc-290">**-El** 命令列選項不能與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="a0dcc-291">遠端公開陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="a0dcc-292">**vshadow** **-er =**_ShadowCopyId_*_，_*_UnusedShareName_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="a0dcc-293">**vshadow** **-er =**_ShadowCopyId_*_、_*_UnusedShareName_*_、_*_PathFromRootOnShadow_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="a0dcc-294">**-Er** 命令列選項會將唯讀共用名稱指派給根目錄 (或從陰影複製) 子目錄。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="a0dcc-295">請注意，除非您後續呼叫 **vshadow** **-bw** 來中斷陰影複製集，否則共用內容將維持唯讀狀態。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-296">[*用戶端可存取的陰影複製*](vssgloss-c.md) 無法從遠端公開。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="a0dcc-297">例如，如果 {edbed95e-7e8d-11d8-9d01-505054503030} 是現有持續性陰影複製的 GUID，而共用 \_ 123 是未使用的共用名稱，則下列命令會公開共用123底下的陰影複製 \_ ：</span><span class="sxs-lookup"><span data-stu-id="a0dcc-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="a0dcc-298">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}，共用 \_ 123**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="a0dcc-299">下列範例示範如何只在相同的共用下，公開名稱為 "Folder1 \\ Folder2" ) 的子樹 (的相同陰影複製：</span><span class="sxs-lookup"><span data-stu-id="a0dcc-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="a0dcc-300">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}，Share \_ 123，Folder1 \\ Folder2**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="a0dcc-301">**-Er** 命令列選項不能與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="a0dcc-302">列出寫入器狀態和中繼資料</span><span class="sxs-lookup"><span data-stu-id="a0dcc-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="a0dcc-303">**vshadow** **-ws**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="a0dcc-304">**vshadow** **-wm**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="a0dcc-305">**vshadow** **-wm2-downloadbtn**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="a0dcc-306">**vshadow** **-wm3**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="a0dcc-307">**-Ws** 命令列選項會列舉目前正在電腦上執行的 VSS 寫入器，並說明其狀態。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="a0dcc-308">此命令相當於 [Vssadmin list 寫入](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 器命令。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="a0dcc-309">有六個可能的狀態值：穩定、失敗、未知、等待凍結、凍結，以及等待完成。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="a0dcc-310">**-Wm** 命令列選項會列出寫入器中繼資料的摘要，包括受影響的磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="a0dcc-311">**-Wm2-downloadbtn** 命令列選項會列出所有寫入器中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="a0dcc-312">**-Wm3** 命令列選項會以原始 XML 格式列出所有寫入器中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="a0dcc-313">**Windows Vista 和 Windows Server 2003：** 不支援 **-wm3** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="a0dcc-314">您可以使用這項資訊來判斷要包含在磁片區陰影複製集中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-315">如果寫入器狀態為穩定或等候完成，寫入器可視為處於穩定狀態，可供下一次備份之用。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="a0dcc-316">**-Ws**、 **-wm**、 **-wm2-downloadbtn** 和 **-wm3** 命令列選項都是互斥的，且無法與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="a0dcc-317">執行還原作業</span><span class="sxs-lookup"><span data-stu-id="a0dcc-317">Performing Restore Operations</span></span>

<span data-ttu-id="a0dcc-318">**vshadow** \[OptionalFlags \] **-r =**_File_*_.xml_*</span><span class="sxs-lookup"><span data-stu-id="a0dcc-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="a0dcc-319">**vshadow** \[OptionalFlags \] **-rs =**_File_*_.xml_*</span><span class="sxs-lookup"><span data-stu-id="a0dcc-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="a0dcc-320">**-R** 命令列選項會執行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="a0dcc-321">**-Rs** 命令列選項會執行模擬的還原作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="a0dcc-322">*File.xml* 檔案必須是使用 **-t** 或 **-bc** 選擇性旗標所建立的陰影複製集的備份元件檔檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="a0dcc-323">**-R** 和 **-rs** 命令列選項互斥，而且無法與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="a0dcc-324">*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="a0dcc-325">選擇性旗標值</span><span class="sxs-lookup"><span data-stu-id="a0dcc-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="a0dcc-326">Description</span><span class="sxs-lookup"><span data-stu-id="a0dcc-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dcc-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi-fi =**_寫入器_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="a0dcc-328">這個選擇性旗標會驗證指定的寫入器或元件是否包含在還原中。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="a0dcc-329">*寫入器* 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="a0dcc-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx =**_Writer_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="a0dcc-331">這個選擇性旗標會驗證指定的寫入器或元件是否排除在還原之外。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="a0dcc-332">*寫入器* 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="a0dcc-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_命令_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="a0dcc-334">這個選擇性旗標會在傳送至寫入器的還原前和還原後事件之間執行命令或腳本。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="a0dcc-335">*命令* 可以指定可執行檔 shell 命令或 CMD 檔。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="a0dcc-336">如果指定了 shell 命令，就不能指定任何命令參數。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="a0dcc-337"><span id="-tracing"></span><span id="-TRACING"></span>**-追蹤**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="a0dcc-338">這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="a0dcc-339">還原為先前的陰影複製</span><span class="sxs-lookup"><span data-stu-id="a0dcc-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="a0dcc-340">**vshadow** **-revert =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="a0dcc-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-341">只有在 Windows server 作業系統上才支援此命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="a0dcc-342">**Windows server 2008 和 Windows server 2003：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="a0dcc-343">**-Revert** 命令列選項會將磁片區還原為先前的陰影複製，其識別碼是由 *ShadowCopyId* 所指定。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="a0dcc-344">**-Revert** 命令列選項不能與其他命令列選項結合。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="a0dcc-345">重新同步處理 Lun</span><span class="sxs-lookup"><span data-stu-id="a0dcc-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="a0dcc-346">**vshadow** **-addresync =**_ShadowCopyId_ **-resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="a0dcc-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="a0dcc-347">**vshadow** **-addresync =**_ShadowCopyId_*_，_* *TargetVolumeDriveLetter* **-resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="a0dcc-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="a0dcc-348">**-Addresync** 命令列選項會指定要包含在 LUN 重新同步作業中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="a0dcc-349">*ShadowCopyId* 參數會指定陰影複製的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="a0dcc-350">選擇性的 *TargetVolumeDriveLetter* 參數會指定要複製陰影複製磁片區內容的目的地磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="a0dcc-351">**-Resync** 命令列選項會起始 LUN 重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="a0dcc-352">作業完成之後，每個目標 LUN 的簽章應與目標磁片區 LUN 的簽章相同。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="a0dcc-353">*BCDFileName* 參數會指定包含備份元件檔的 XML 檔案名。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="a0dcc-354">只有在 Windows server 作業系統上才支援 **-addresync** 和 **-resync** 命令列選項。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="a0dcc-355">**Windows server 2008 和 Windows server 2003：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="a0dcc-356">*OptionalResyncFlags* 是下表中選擇性旗標值的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0dcc-357">選擇性旗標值</span><span class="sxs-lookup"><span data-stu-id="a0dcc-357">Optional flag value</span></span></th>
<th><span data-ttu-id="a0dcc-358">Description</span><span class="sxs-lookup"><span data-stu-id="a0dcc-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0dcc-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-360">此選擇性旗標指定在作業完成之後，每個目標 LUN 的簽章應與用來建立陰影複製的原始 LUN 相同，而不是目標磁片區 LUN。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-361">只有在 Windows server 作業系統上才支援 <strong>-revertsig</strong> 旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-362"><strong>Windows server 2008 和 Windows server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dcc-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="a0dcc-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="a0dcc-364">此選擇性旗標指定 VSS 服務不應該檢查 LUN 重新同步作業將覆寫的未選取磁片區。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dcc-365">只有在 Windows server 作業系統上才支援 <strong>-novolcheck</strong> 旗標。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a0dcc-366"><strong>Windows server 2008 和 Windows server 2003：</strong> 不支援。</span><span class="sxs-lookup"><span data-stu-id="a0dcc-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
