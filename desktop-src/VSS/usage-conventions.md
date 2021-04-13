---
description: 開發您自己的 VSS 應用程式時，您應該觀察下列指導方針和限制。
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: VSS 應用程式相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318408"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="e826a-103">VSS 應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="e826a-103">VSS Application Compatibility</span></span>

<span data-ttu-id="e826a-104">開發您自己的 VSS 應用程式時，您應該觀察下列指導方針和限制。</span><span class="sxs-lookup"><span data-stu-id="e826a-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="e826a-105">您可能會發現，您可以參考 Microsoft Windows 軟體開發套件 (SDK) 中提供的 VSS 要求者、提供者和寫入器的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="e826a-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="e826a-106">Windows SDK 僅適用于 Windows Vista 和更新版本的 Windows 作業系統版本，可用於開發 VSS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e826a-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="e826a-107">它無法用來開發 Windows Server 2003 R2、Windows Server 2003 或 Windows XP 的 VSS 要求者、提供者或寫入器。</span><span class="sxs-lookup"><span data-stu-id="e826a-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="e826a-108">**Windows server 2003 R2、Windows server 2003 和 WINDOWS XP：** 您可以從磁碟區陰影複製服務 7.2 SDK 取得 VSS，以供下載 [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) 。</span><span class="sxs-lookup"><span data-stu-id="e826a-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="e826a-109">請注意，Win2003 Obj 目錄下目錄中的64位 vssapi .lib 檔案 \\ 可用於64位版本的 Windows server 2003 R2、Windows server 2003 和 WINDOWS XP。</span><span class="sxs-lookup"><span data-stu-id="e826a-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="e826a-110">此 SDK 也提供 VSS 要求者、提供者和寫入器的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="e826a-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="e826a-111">編譯 VSS 應用程式</span><span class="sxs-lookup"><span data-stu-id="e826a-111">Compiling VSS Applications</span></span>

<span data-ttu-id="e826a-112">開發要求者時，例如備份應用程式：</span><span class="sxs-lookup"><span data-stu-id="e826a-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="e826a-113">包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="e826a-113">Include the following headers:</span></span> <dl> <span data-ttu-id="e826a-114">Vss。h</span><span class="sxs-lookup"><span data-stu-id="e826a-114">Vss.h</span></span>  
    <span data-ttu-id="e826a-115">VsWriter。h</span><span class="sxs-lookup"><span data-stu-id="e826a-115">VsWriter.h</span></span>  
    <span data-ttu-id="e826a-116">VsBackup。h</span><span class="sxs-lookup"><span data-stu-id="e826a-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="e826a-117">VssApi .Lib</span><span class="sxs-lookup"><span data-stu-id="e826a-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="e826a-118">開發寫入器時：</span><span class="sxs-lookup"><span data-stu-id="e826a-118">When developing a writer:</span></span>

-   <span data-ttu-id="e826a-119">包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="e826a-119">Include the following headers:</span></span> <dl> <span data-ttu-id="e826a-120">Vss。h</span><span class="sxs-lookup"><span data-stu-id="e826a-120">Vss.h</span></span>  
    <span data-ttu-id="e826a-121">VsWriter。h</span><span class="sxs-lookup"><span data-stu-id="e826a-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="e826a-122">VssApi .lib</span><span class="sxs-lookup"><span data-stu-id="e826a-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="e826a-123">支援的設定和限制</span><span class="sxs-lookup"><span data-stu-id="e826a-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="e826a-124">下列清單說明支援的設定和限制：</span><span class="sxs-lookup"><span data-stu-id="e826a-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="e826a-125">從 Windows XP 開始的 Windows 作業系統版本會提供並支援 VSS。</span><span class="sxs-lookup"><span data-stu-id="e826a-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="e826a-126">下表摘要說明 Windows 版本之間的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="e826a-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="e826a-127">請注意，如果 VSS 應用程式「已針對」指定的 Windows 版本進行編譯，這表示應用程式是使用該版本專用的標頭檔和程式庫進行編譯。</span><span class="sxs-lookup"><span data-stu-id="e826a-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="e826a-128">硬體提供者只會在 Windows server 作業系統版本上執行。</span><span class="sxs-lookup"><span data-stu-id="e826a-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="e826a-129">它們不會在 Windows 用戶端作業系統版本上執行。</span><span class="sxs-lookup"><span data-stu-id="e826a-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="e826a-130">在下表中，Windows Server 2008 （含 Service Pack 2 (SP2) 應視為與 Windows Server 2008 相同。</span><span class="sxs-lookup"><span data-stu-id="e826a-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="e826a-131">如需 Windows Server 2008 （含 SP2）的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=178730> 。</span><span class="sxs-lookup"><span data-stu-id="e826a-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="e826a-132">Windows Server 2003 R2 應視為與 Windows Server 2003 相同。</span><span class="sxs-lookup"><span data-stu-id="e826a-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="e826a-133">如果針對 Windows Server 2003 或更新版本編譯 VSS 應用程式，它也會在較新版本的 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="e826a-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e826a-134">為其編譯的 VSS 要求者、寫入器和提供者</span><span class="sxs-lookup"><span data-stu-id="e826a-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="e826a-135">將執行于</span><span class="sxs-lookup"><span data-stu-id="e826a-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e826a-136">Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 和 Windows Vista (64 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="e826a-137">Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 和 Windows Vista (64 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e826a-138">Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 和 Windows Vista (32 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="e826a-139">Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 和 Windows Vista (32 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e826a-140">Windows Server 2003 (64 位元)</span><span class="sxs-lookup"><span data-stu-id="e826a-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="e826a-141">Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 、Windows Vista (64 位) ，以及 Windows Server 2003 (64 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e826a-142">Windows Server 2003 (32 位元)</span><span class="sxs-lookup"><span data-stu-id="e826a-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="e826a-143">Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 、Windows Vista (32 位) ，以及 Windows Server 2003 (32 位) </span><span class="sxs-lookup"><span data-stu-id="e826a-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="e826a-144">要求者也會在 Windows Server 2003 (64 位) 上執行。</span><span class="sxs-lookup"><span data-stu-id="e826a-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e826a-145">Windows XP 64 位版本</span><span class="sxs-lookup"><span data-stu-id="e826a-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="e826a-146">Windows Server 2003 (64 位) 和 Windows XP 64 位版本</span><span class="sxs-lookup"><span data-stu-id="e826a-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e826a-147">Windows XP (32 位元)</span><span class="sxs-lookup"><span data-stu-id="e826a-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="e826a-148">Windows XP (32 位元)</span><span class="sxs-lookup"><span data-stu-id="e826a-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="e826a-149">編譯 VSS 要求者、寫入器或提供者</span><span class="sxs-lookup"><span data-stu-id="e826a-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="e826a-150">使用</span><span class="sxs-lookup"><span data-stu-id="e826a-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e826a-151">Windows Server 2008 R2 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="e826a-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="e826a-152">Windows 7 (的 Windows SDK 可從 [Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)取得。 ) </span><span class="sxs-lookup"><span data-stu-id="e826a-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="e826a-153">Windows Server 2008 或 Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e826a-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="e826a-154">Windows SDK Windows Server 2008 (可從 [Windows SDK 開發人員中心](https://msdn.microsoft.com/windows/bb980924.aspx)取得。 ) </span><span class="sxs-lookup"><span data-stu-id="e826a-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="e826a-155">Windows Server 2003 R2、Windows Server 2003 或 Windows XP</span><span class="sxs-lookup"><span data-stu-id="e826a-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="e826a-156">磁碟區陰影複製服務 7.2 SDK</span><span class="sxs-lookup"><span data-stu-id="e826a-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="e826a-157">所有32位 VSS 應用程式 (要求者、提供者和寫入器) 必須以原生32位或64位應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="e826a-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="e826a-158">不支援在 WOW64 下執行它們。</span><span class="sxs-lookup"><span data-stu-id="e826a-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="e826a-159">**Windows Server 2003 和 WINDOWS XP：** 支援在 WOW64 下執行32位 VSS 要求者，但不支援系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="e826a-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="e826a-160">不支援在 WOW64 下執行32位 VSS 提供者和寫入器。</span><span class="sxs-lookup"><span data-stu-id="e826a-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="e826a-161">在 Windows Vista 和後續版本中，已移除在 WOW64 下執行32位要求者的支援。</span><span class="sxs-lookup"><span data-stu-id="e826a-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="e826a-162">在 Windows Server 2003 R2 或 Windows Server 2003 上建立的陰影複製，無法在執行 Windows Server 2008 R2 或 Windows Server 2008 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="e826a-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="e826a-163">在 Windows Server 2008 R2 或 Windows Server 2008 上建立的陰影複製無法在執行 Windows Server 2003 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="e826a-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="e826a-164">不過，在 Windows Server 2008 上建立的陰影複製可以在執行 Windows Server 2008 R2 的電腦上使用，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="e826a-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="e826a-165">若要支援陰影複製，執行 VSS 的系統必須至少有一個 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="e826a-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="e826a-166">此檔案系統將裝載陰影複製的「差異區域」。</span><span class="sxs-lookup"><span data-stu-id="e826a-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="e826a-167">如需詳細資訊，請參閱 [系統提供者](providers.md)。</span><span class="sxs-lookup"><span data-stu-id="e826a-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="e826a-168">假設有一個 NTFS 檔案系統，並提供適當的內容選擇 (請參閱 [陰影複製內容](shadow-copy-context-configurations.md) 設定) ，任何支援的本機檔案系統都可進行陰影複製。</span><span class="sxs-lookup"><span data-stu-id="e826a-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="e826a-169">您只能針對本機掛接的檔案系統製作陰影複製。</span><span class="sxs-lookup"><span data-stu-id="e826a-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="e826a-170">裝載遠端共用和其他跨掛接檔案系統的系統無法進行陰影複製。</span><span class="sxs-lookup"><span data-stu-id="e826a-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="e826a-171">這些檔案系統只能由提供檔案系統的系統進行陰影複製。</span><span class="sxs-lookup"><span data-stu-id="e826a-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="e826a-172">寫入器和要求者只能指定本機資源。</span><span class="sxs-lookup"><span data-stu-id="e826a-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="e826a-173">本機資源是一組檔案，其絕對路徑開頭為磁碟機號，而磁碟機號無法與遠端共用上掛接的資料夾相關聯。</span><span class="sxs-lookup"><span data-stu-id="e826a-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="e826a-174">每個磁片區的軟體陰影複製數目上限為512。</span><span class="sxs-lookup"><span data-stu-id="e826a-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="e826a-175">不過，根據預設，您只能維護 64 個「共用資料夾陰影複製」功能所使用的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="e826a-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="e826a-176">若要變更共用資料夾陰影複製功能的限制，請使用 [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e826a-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="e826a-177">備份元件基礎結構不支援將叢集資源備份為寫入器元件。</span><span class="sxs-lookup"><span data-stu-id="e826a-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="e826a-178">若要備份叢集資源，應用程式應該假設路徑是指定特定叢集節點的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="e826a-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="e826a-179">Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="e826a-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="e826a-180">備份和復原系統狀態時，建議的策略是除了系統狀態寫入器所列舉的檔案之外，還會備份和復原系統和開機磁碟區。</span><span class="sxs-lookup"><span data-stu-id="e826a-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="e826a-181">系統狀態寫入器是將 [ [**vss \_ 使用 \_ 類型**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) ] 屬性設為 [vss \_ BOOTABLESYSTEMSTATE] 或 [ \_ vss SYSTEMSERVICE] 的寫入器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e826a-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
