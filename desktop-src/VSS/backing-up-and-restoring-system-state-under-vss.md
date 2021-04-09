---
description: 請注意，本主題僅適用于 Windows Server 2003 R2 和 Windows Server 2003 Service Pack 1 (SP1) 。
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: 在 Windows Server 2003 R2 和 Windows Server 2003 SP1 中備份和還原系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945233"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a><span data-ttu-id="288ad-103">在 Windows Server 2003 R2 和 Windows Server 2003 SP1 中備份和還原系統狀態</span><span class="sxs-lookup"><span data-stu-id="288ad-103">Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1</span></span>

> [!Note]  
> <span data-ttu-id="288ad-104">本主題僅適用于 Windows Server 2003 R2 和 Windows Server 2003 Service Pack 1 (SP1) 。</span><span class="sxs-lookup"><span data-stu-id="288ad-104">This topic only applies to Windows Server 2003 R2 and Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="288ad-105">如需其他作業系統版本的詳細資訊，請參閱 [備份和還原系統狀態](locating-additional-system-files.md)。</span><span class="sxs-lookup"><span data-stu-id="288ad-105">For information about other operating system versions, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="288ad-106">Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="288ad-106">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="288ad-107">如需有關使用 Microsoft 提供的 Api 和程式來執行線上系統狀態還原的詳細資訊，請參閱 [MSDN 論壇中心](https://msdn.microsoft.com/community/default.aspx)提供的「社區資源」。</span><span class="sxs-lookup"><span data-stu-id="288ad-107">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

<span data-ttu-id="288ad-108">執行 VSS 備份或還原時，會將 Windows 系統狀態定義為數個主要作業系統元素及其檔案的集合。</span><span class="sxs-lookup"><span data-stu-id="288ad-108">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="288ad-109">這些元素應一律由備份和還原作業視為一個單位來處理。</span><span class="sxs-lookup"><span data-stu-id="288ad-109">These elements should always be treated by backup and restore operations as a unit.</span></span>

<span data-ttu-id="288ad-110">在 Windows Server 2003 R2 和 Windows Server 2003 （含 SP1）中，沒有任何 Windows API 設計來將這些物件視為一，因此建議要求者擁有自己的系統狀態物件，以便能夠以一致的方式處理這些元件。</span><span class="sxs-lookup"><span data-stu-id="288ad-110">In Windows Server 2003 R2 and Windows Server 2003 with SP1, there is no Windows API designed to treat these objects as one, so it is recommended that requesters have their own system state object so that they can process these components in a consistent manner.</span></span>

<span data-ttu-id="288ad-111">由於 VSS 是在 Windows 版本上執行，而 [*系統檔案保護*](vssgloss-s.md) (WFP) 保護系統狀態檔案免于損毀，因此需要特殊步驟來備份和還原系統狀態。</span><span class="sxs-lookup"><span data-stu-id="288ad-111">Because VSS runs on versions of Windows where [*System File Protection*](vssgloss-s.md) (WFP) protects system state files from corruption, special steps are needed to back up and restore system state.</span></span>

<span data-ttu-id="288ad-112">系統狀態包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="288ad-112">System state consists of the following:</span></span>

-   <span data-ttu-id="288ad-113">所有受 WFP 保護的檔案、開機檔案，包括 ntldr、ntdetect 和效能計數器設定</span><span class="sxs-lookup"><span data-stu-id="288ad-113">All files protected by WFP, boot files including ntldr, ntdetect, and performance counter configurations</span></span>
-   <span data-ttu-id="288ad-114">在網域控制站的系統上，Active Directory (ADSI)  () </span><span class="sxs-lookup"><span data-stu-id="288ad-114">The Active Directory (ADSI) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="288ad-115">系統磁碟區資料夾 (SYSVOL) ，檔案複寫服務會在網域控制站的系統上 (FRS)  () </span><span class="sxs-lookup"><span data-stu-id="288ad-115">The System Volume Folder (SYSVOL) that is replicated by the File Replication Service (FRS) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="288ad-116">提供憑證授權單位單位之系統上的憑證伺服器 () </span><span class="sxs-lookup"><span data-stu-id="288ad-116">Certificate server (on systems that provide Certification Authority)</span></span>
-   <span data-ttu-id="288ad-117">叢集資料庫 (在屬於 Windows 叢集節點的系統上) </span><span class="sxs-lookup"><span data-stu-id="288ad-117">Cluster database (on systems that are a node of a Windows cluster)</span></span>
-   <span data-ttu-id="288ad-118">註冊服務</span><span class="sxs-lookup"><span data-stu-id="288ad-118">Registry service</span></span>
-   <span data-ttu-id="288ad-119">COM + 類別註冊資料庫</span><span class="sxs-lookup"><span data-stu-id="288ad-119">COM+ class registration database</span></span>

<span data-ttu-id="288ad-120">系統狀態可以依任何順序進行備份。</span><span class="sxs-lookup"><span data-stu-id="288ad-120">The system state can be backed up in any order.</span></span>

<span data-ttu-id="288ad-121">不過，還原系統狀態應該會先取代開機檔案，然後將登錄的系統區段 (hive) 作為程式中的最後一個步驟，而且可能會依下列順序發生：</span><span class="sxs-lookup"><span data-stu-id="288ad-121">However, the restoration of the system state should replace boot files first and commit the system section (hive) of the registry as a final step in the process, and might occur in the following order:</span></span>

1.  <span data-ttu-id="288ad-122">還原開機檔案。</span><span class="sxs-lookup"><span data-stu-id="288ad-122">Restore the boot files.</span></span>
2.  <span data-ttu-id="288ad-123">COM + 類別註冊資料庫</span><span class="sxs-lookup"><span data-stu-id="288ad-123">COM+ class registration database</span></span>
3.  <span data-ttu-id="288ad-124">如有需要，請 (還原 SYSVOL、憑證伺服器和叢集資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="288ad-124">Restore SYSVOL, Certificate Server, and Cluster databases (if needed).</span></span>
4.  <span data-ttu-id="288ad-125">視需要) 還原 Active Directory (。</span><span class="sxs-lookup"><span data-stu-id="288ad-125">Restore Active Directory (if needed).</span></span>
5.  <span data-ttu-id="288ad-126">還原登錄。</span><span class="sxs-lookup"><span data-stu-id="288ad-126">Restore the registry.</span></span>

<span data-ttu-id="288ad-127">某些系統服務（例如憑證授權單位單位）有傳統的 VSS 寫入器，並遵循 VSS 備份和還原演算法。</span><span class="sxs-lookup"><span data-stu-id="288ad-127">Some system services, such as the Certification Authority, have conventional VSS writers and follow the VSS backup and restore algorithms.</span></span> <span data-ttu-id="288ad-128">其他專案（例如登錄）則需要自訂備份或還原作業;如需詳細資訊，請參閱 [自訂備份和還原](custom-backups-and-restores.md)。</span><span class="sxs-lookup"><span data-stu-id="288ad-128">Others, such as the registry, require custom backup or restore operations; for more information, see [Custom Backups and Restores](custom-backups-and-restores.md).</span></span>

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a><span data-ttu-id="288ad-129">開機和系統檔案的 VSS 備份和還原</span><span class="sxs-lookup"><span data-stu-id="288ad-129">VSS Backup and Restores of Boot and System Files</span></span>

<span data-ttu-id="288ad-130">開機和系統檔案只能以單一實體的形式來備份和還原。</span><span class="sxs-lookup"><span data-stu-id="288ad-130">The boot and system files should be backed up and restored only as a single entity.</span></span>

<span data-ttu-id="288ad-131">要求者可以安全地使用這些檔案的陰影複製版本，並確定系統磁碟區和開機裝置是 [*陰影複製*](vssgloss-s.md)的。</span><span class="sxs-lookup"><span data-stu-id="288ad-131">A requester can safely use shadow-copied versions of these files, and should be sure that the system volume and boot device are [*shadow copied*](vssgloss-s.md).</span></span>

<span data-ttu-id="288ad-132">系統和開機檔案包括：</span><span class="sxs-lookup"><span data-stu-id="288ad-132">The system and boot files include:</span></span>

-   <span data-ttu-id="288ad-133">核心開機檔案：</span><span class="sxs-lookup"><span data-stu-id="288ad-133">The core boot files:</span></span> <dl> <span data-ttu-id="288ad-134">NtLdr.exe</span><span class="sxs-lookup"><span data-stu-id="288ad-134">NtLdr.exe</span></span>  
    <span data-ttu-id="288ad-135">Boot.ini</span><span class="sxs-lookup"><span data-stu-id="288ad-135">Boot.ini</span></span>  
    <span data-ttu-id="288ad-136">NtDetect.com</span><span class="sxs-lookup"><span data-stu-id="288ad-136">NtDetect.com</span></span>  
    <span data-ttu-id="288ad-137">NtBootDD.sys (（如果有的話）) </span><span class="sxs-lookup"><span data-stu-id="288ad-137">NtBootDD.sys (if present)</span></span>  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> <span data-ttu-id="288ad-138">% SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span><span class="sxs-lookup"><span data-stu-id="288ad-138">%SystemRoot%\\System32\\CatRoot\\{F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span></span> </dl><span data-ttu-id="288ad-139">
-   所有受 [\*系統檔案保護*](vssgloss-s.md) 保護並由 [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) 列舉的檔案 (查看 -   效能計數器設定檔) 的 WFP 受保護檔案的 VSS 還原作業：</span><span class="sxs-lookup"><span data-stu-id="288ad-139">
-   All files protected by [\*System File Protection*](vssgloss-s.md) and enumerated by [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (see VSS Restore Operations of WFP Protected Files) -   The Performance Counter Configuration files:</span></span> <dl> <span data-ttu-id="288ad-140">% SystemRoot% \\ System32 效能 \\ ？00？。Dat</span><span class="sxs-lookup"><span data-stu-id="288ad-140">%SystemRoot%\\System32\\Perf?00?.dat</span></span>  
    <span data-ttu-id="288ad-141">% SystemRoot% \\ System32 效能 \\ ？00？。Bak</span><span class="sxs-lookup"><span data-stu-id="288ad-141">%SystemRoot%\\System32\\Perf?00?.bak</span></span> </dl><span data-ttu-id="288ad-142">
-   如果存在，則會在備份和還原作業中包含網際網路資訊伺服器 (IIS) 的中繼檔，因為它包含 Microsoft Exchange 和其他網路應用程式所使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="288ad-142">
-   If present, the Internet Information Server (IIS) metabase file should be included in backup and restore operations because it contains state that is used by Microsoft Exchange and other network applications.</span></span> <span data-ttu-id="288ad-143">這個檔案位於下列位置：</span><span class="sxs-lookup"><span data-stu-id="288ad-143">This file can be found at:</span></span> <dl> <span data-ttu-id="288ad-144">% SystemRoot% \\ System32 \\ InetSrv \\ 元資料庫. bin</span><span class="sxs-lookup"><span data-stu-id="288ad-144">%SystemRoot%\\System32\\InetSrv\\Metabase.bin</span></span> </dl><span data-ttu-id="288ad-145">
-   如果已備份 IIS 中繼檔，則可讓應用程式讀取特定加密專案的金鑰，應還原為系統狀態的一部分。</span><span class="sxs-lookup"><span data-stu-id="288ad-145">
-   If the IIS metabase file is backed up, keys to enable applications to read certain encrypted entries should be restored as part of the system state.</span></span> <span data-ttu-id="288ad-146">您可以在下列檔中找到這些檔案：</span><span class="sxs-lookup"><span data-stu-id="288ad-146">The files can be found under:</span></span> <dl> <span data-ttu-id="288ad-147">% SystemRoot% \\ System32 \\ Microsoft \\ 保護\\\*</span><span class="sxs-lookup"><span data-stu-id="288ad-147">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
    <span data-ttu-id="288ad-148">% AllUsersProfile% \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="288ad-148">%AllUsersProfile%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span> </dl><span data-ttu-id="288ad-149">
-備份開機和系統檔案時，您可能必須執行下列動作，以判斷 DOS 開機裝置： 1. 在 [ \*\*HKEY \_ 本機 \_ 電腦*\* \\ \*\*系統*\* \\ \*\*安裝*\* \\ \*\*SystemPartition\*\*] 下尋找系統磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="288ad-149">
-   When backing up boot and system files, it may become necessary to determine the DOS boot device by doing the following: 1.  Find the system partition under \*\*HKEY\_LOCAL\_MACHINE\*\*\\*\*System\*\*\\*\*Setup\*\*\\*\*SystemPartition\**.</span></span>
    <span data-ttu-id="288ad-150">2.  將系統根目錄環境變數 (% SystemRoot% ) 傳遞給掛接管理員，以取得 NT 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="288ad-150">2.  Pass the System Root environment variable (%SystemRoot%) to the mount manager to obtain the NT device name.</span></span>

## <a name="vss-restore-operations-of-wfp-protected-files"></a><span data-ttu-id="288ad-151">WFP 受保護檔案的 VSS 還原作業</span><span class="sxs-lookup"><span data-stu-id="288ad-151">VSS Restore Operations of WFP Protected Files</span></span>

<span data-ttu-id="288ad-152">WFP 服務是設計來防止系統檔案意外或分次取代。</span><span class="sxs-lookup"><span data-stu-id="288ad-152">The WFP service is designed to prevent accidental or piecemeal replacement of system files.</span></span> <span data-ttu-id="288ad-153">因此，必須採取特殊步驟來還原 WFP 資料。</span><span class="sxs-lookup"><span data-stu-id="288ad-153">Therefore, special steps need to be undertaken to restore WFP data.</span></span>

<span data-ttu-id="288ad-154">這表示當您定義寫入器元資料檔案時，WFP 寫入器應該 **\_ \_ \_ 在 \_ 重新開機** 還原方法時指定 VSS RME 還原。</span><span class="sxs-lookup"><span data-stu-id="288ad-154">The means the WFP writer should specify the **VSS\_RME\_RESTORE\_AT\_REBOOT** restore method when defining its Writer Metadata Document.</span></span> <span data-ttu-id="288ad-155">如果要求者判斷 WFP 寫入器無法指定此還原方法，它會指出寫入器錯誤。</span><span class="sxs-lookup"><span data-stu-id="288ad-155">If a requester determines that the WFP writer has failed to specify this restore method, it indicates a writer error.</span></span>

<span data-ttu-id="288ad-156">要求者應該在重新開機時，使用 Win32 函數 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa)搭配 **MOVEFILE \_ 延遲 \_ 直到 \_ 重新開機** 參數取代系統檔案，以 **\_ \_ \_ 在 \_ 重新開機時執行 VSS RME 還原** 的還原方法。</span><span class="sxs-lookup"><span data-stu-id="288ad-156">A requester should implement a restore method of **VSS\_RME\_RESTORE\_AT\_REBOOT** using the Win32 function [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) with the **MOVEFILE\_DELAY\_UNTIL\_REBOOT** parameter to replace system files.</span></span> <span data-ttu-id="288ad-157">還原的檔案不會複製到實際的系統檔案目錄中，直到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="288ad-157">The restored files are not copied into the actual system file directories until after system reboot.</span></span> <span data-ttu-id="288ad-158">只有當下列 **REG \_ WORD** 登錄專案的值設定為1時，才會覆寫受保護的系統檔案：</span><span class="sxs-lookup"><span data-stu-id="288ad-158">The overwriting of protected system files will occur only if the value of the following **REG\_WORD** registry entry is set to 1:</span></span>

<span data-ttu-id="288ad-159">**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **AllowProtectedRenames** = 1</span><span class="sxs-lookup"><span data-stu-id="288ad-159">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**AllowProtectedRenames** = 1</span></span>

<span data-ttu-id="288ad-160">必須先設定此值，才能透過 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) 取代受保護的檔案，並在重新開機之後刪除。</span><span class="sxs-lookup"><span data-stu-id="288ad-160">This value must be set before any boot where protected files are to be replaced via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and is deleted after reboot.</span></span>

<span data-ttu-id="288ad-161">您也應該使用開機磁碟區備份和還原來備份或還原系統 dllcache 目錄，並藉由檢查 **REG \_ EXPAND \_ SZ** 登錄專案來找到它：</span><span class="sxs-lookup"><span data-stu-id="288ad-161">The system dllcache directory should also be backed up or restored, with boot volume backup and restore, and is located by examining the **REG\_EXPAND\_SZ** registry entry:</span></span>

<span data-ttu-id="288ad-162">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**</span><span class="sxs-lookup"><span data-stu-id="288ad-162">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**SfcDllCache**</span></span><dl> <dt>

                  Data type
</dt> <dd>                  <span data-ttu-id="288ad-163">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="288ad-163">REG\_EXPAND\_SZ</span></span></dd> </dl>

<span data-ttu-id="288ad-164">系統 dllcache 目錄的內容會從命令提示字元使用系統檔案檢查程式 (SFC) 來重建：</span><span class="sxs-lookup"><span data-stu-id="288ad-164">The contents of the system dllcache directory are rebuilt by using the System File Checker (SFC) from the command prompt:</span></span>

-   <span data-ttu-id="288ad-165">**/SCANONCE** 選項會在下一次系統開機時掃描所有受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="288ad-165">The **/SCANONCE** option scans all protected files at the next system boot.</span></span>
-   <span data-ttu-id="288ad-166">**/SCANNOW** 選項會立即掃描所有受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="288ad-166">The **/SCANNOW** option scans all protected files immediately.</span></span>

<span data-ttu-id="288ad-167">系統將掃描所有受保護的檔案，並在目錄和 dllcache 位置中取代任何不正確版本。</span><span class="sxs-lookup"><span data-stu-id="288ad-167">All protected files will be scanned, and any versions that are not valid will be replaced in both the directory and dllcache location.</span></span>

<span data-ttu-id="288ad-168">有四個檔案是無法使用 WFP 檔案還原之 WFP 的一部分：</span><span class="sxs-lookup"><span data-stu-id="288ad-168">There are four files that are part of the WFP that cannot be restored with the WFP files:</span></span>

<dl> <span data-ttu-id="288ad-169">Ctl3dv2.dll</span><span class="sxs-lookup"><span data-stu-id="288ad-169">Ctl3dv2.dll</span></span>  
<span data-ttu-id="288ad-170">DtcSetup.exe</span><span class="sxs-lookup"><span data-stu-id="288ad-170">DtcSetup.exe</span></span>  
<span data-ttu-id="288ad-171">NtDll.dll</span><span class="sxs-lookup"><span data-stu-id="288ad-171">NtDll.dll</span></span>  
<span data-ttu-id="288ad-172">Smss.exe</span><span class="sxs-lookup"><span data-stu-id="288ad-172">Smss.exe</span></span>  
</dl>

<span data-ttu-id="288ad-173">這些檔案有助於還原 WFP 檔案，因此有迴圈的相依性。</span><span class="sxs-lookup"><span data-stu-id="288ad-173">These files help in the process of restoring the WFP files and as such there is a circular dependency.</span></span> <span data-ttu-id="288ad-174">目前沒有任何方法可以還原這些檔案，除非重新安裝 Windows。</span><span class="sxs-lookup"><span data-stu-id="288ad-174">Currently, there is no way to restore these files except to reinstall Windows.</span></span>

 

 
