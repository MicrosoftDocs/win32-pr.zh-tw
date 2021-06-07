---
title: 用於備份和還原的登錄機碼和值
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 深入瞭解：備份和還原的登錄機碼和值
keywords:
- 備份備份，登錄機碼
- 登錄機碼備份
- CustomPerformanceSettings 備份
- DisableMonitoring 備份
- FilesNotToBackup 備份
- FilesNotToSnapshot 備份
- KeysNotToRestore 備份
- LastInstance 備份
- LastRestoreId 備份
- MaxShadowCopies 備份
- MinDiffAreaFileSize 備份
- OverallPerformanceSetting 備份
- SYSVOL 備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7058378561072bdc0f51abb455c098a22a9ad5e
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386787"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a><span data-ttu-id="d7438-116">用於備份和還原的登錄機碼和值</span><span class="sxs-lookup"><span data-stu-id="d7438-116">Registry Keys and Values for Backup and Restore</span></span>

<span data-ttu-id="d7438-117">要求或執行備份和還原作業的應用程式，應該使用下列登錄機碼和值彼此通訊，或透過 [磁碟區陰影複製服務 (VSS) ](/windows/desktop/VSS/volume-shadow-copy-service-portal) 和 Windows 備份等功能進行通訊：</span><span class="sxs-lookup"><span data-stu-id="d7438-117">Applications that request or perform backup and restore operations should use the following registry keys and values to communicate with each other or with features such as the [Volume Shadow Copy Service (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) and Windows Backup:</span></span>

-   [<span data-ttu-id="d7438-118">CustomPerformanceSettings</span><span class="sxs-lookup"><span data-stu-id="d7438-118">CustomPerformanceSettings</span></span>](#customperformancesettings)
-   [<span data-ttu-id="d7438-119">DisableMonitoring</span><span class="sxs-lookup"><span data-stu-id="d7438-119">DisableMonitoring</span></span>](#disablemonitoring)
-   [<span data-ttu-id="d7438-120">FilesNotToBackup</span><span class="sxs-lookup"><span data-stu-id="d7438-120">FilesNotToBackup</span></span>](#filesnottobackup)
-   [<span data-ttu-id="d7438-121">FilesNotToSnapshot</span><span class="sxs-lookup"><span data-stu-id="d7438-121">FilesNotToSnapshot</span></span>](#filesnottosnapshot)
-   [<span data-ttu-id="d7438-122">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="d7438-122">IdleTimeout</span></span>](#idletimeout)
-   [<span data-ttu-id="d7438-123">KeysNotToRestore</span><span class="sxs-lookup"><span data-stu-id="d7438-123">KeysNotToRestore</span></span>](#keysnottorestore)
-   [<span data-ttu-id="d7438-124">LastInstance</span><span class="sxs-lookup"><span data-stu-id="d7438-124">LastInstance</span></span>](#lastinstance)
-   [<span data-ttu-id="d7438-125">LastRestoreId</span><span class="sxs-lookup"><span data-stu-id="d7438-125">LastRestoreId</span></span>](#lastrestoreid)
-   [<span data-ttu-id="d7438-126">MaxShadowCopies</span><span class="sxs-lookup"><span data-stu-id="d7438-126">MaxShadowCopies</span></span>](#maxshadowcopies)
-   [<span data-ttu-id="d7438-127">MinDiffAreaFileSize</span><span class="sxs-lookup"><span data-stu-id="d7438-127">MinDiffAreaFileSize</span></span>](#mindiffareafilesize)
-   [<span data-ttu-id="d7438-128">OverallPerformanceSetting 和 CustomPerformanceSettings</span><span class="sxs-lookup"><span data-stu-id="d7438-128">OverallPerformanceSetting and CustomPerformanceSettings</span></span>](#overallperformancesetting-and-customperformancesettings)
-   [<span data-ttu-id="d7438-129">SYSVOL</span><span class="sxs-lookup"><span data-stu-id="d7438-129">SYSVOL</span></span>](#sysvol)

## <a name="customperformancesettings"></a><span data-ttu-id="d7438-130">CustomPerformanceSettings</span><span class="sxs-lookup"><span data-stu-id="d7438-130">CustomPerformanceSettings</span></span>

<span data-ttu-id="d7438-131">請參閱 [OverallPerformanceSetting 和 CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)。</span><span class="sxs-lookup"><span data-stu-id="d7438-131">See [OverallPerformanceSetting and CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings).</span></span>

## <a name="disablemonitoring"></a><span data-ttu-id="d7438-132">DisableMonitoring</span><span class="sxs-lookup"><span data-stu-id="d7438-132">DisableMonitoring</span></span>

<span data-ttu-id="d7438-133">從 Windows 7 開始，在 Windows 用戶端平臺上，如果使用者尚未這麼做，系統會自動提示使用者設定 Windows 備份功能。</span><span class="sxs-lookup"><span data-stu-id="d7438-133">On Windows client platforms beginning with Windows 7, users are automatically prompted to configure the Windows Backup feature if they have not already done so.</span></span> <span data-ttu-id="d7438-134">這些通知會在電腦啟動時顯示，在安裝作業系統之後的七天開始。</span><span class="sxs-lookup"><span data-stu-id="d7438-134">These notifications appear at computer startup time, beginning seven days after the operating system is installed.</span></span> <span data-ttu-id="d7438-135">它們也會在使用者插入硬碟時出現;在此情況下，通知會立即顯示。</span><span class="sxs-lookup"><span data-stu-id="d7438-135">They also appear when the user plugs in a hard disk drive; in this case, the notifications appear immediately.</span></span>

<span data-ttu-id="d7438-136">協力廠商備份應用程式的 Oem 和開發人員可以使用 **DisableMonitoring** 登錄值來關閉這些自動通知。</span><span class="sxs-lookup"><span data-stu-id="d7438-136">OEMs and developers of third-party backup applications can use the **DisableMonitoring** registry value to turn off these automatic notifications.</span></span>

<span data-ttu-id="d7438-137">根據預設，這個值並不存在，因此必須在下列登錄機碼底下建立：</span><span class="sxs-lookup"><span data-stu-id="d7438-137">This value does not exist by default, so it must be created under the following registry key:</span></span>

<span data-ttu-id="d7438-138">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**</span><span class="sxs-lookup"><span data-stu-id="d7438-138">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsBackup**</span></span>

<span data-ttu-id="d7438-139">**DisableMonitoring** 登錄值的資料類型為 REG \_ DWORD，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d7438-139">The **DisableMonitoring** registry value has the data type REG\_DWORD and is interpreted as follows:</span></span>

-   <span data-ttu-id="d7438-140">如果值的資料設定為1，而且使用者尚未設定 Windows 備份功能，則會關閉自動通知。</span><span class="sxs-lookup"><span data-stu-id="d7438-140">If the value's data is set to 1 and if users have not already configured the Windows Backup feature, the automatic notifications are turned off.</span></span> <span data-ttu-id="d7438-141">如果 [行動中心] 已有自動通知，設定此登錄值會導致在下列早上的10:00 移除通知。</span><span class="sxs-lookup"><span data-stu-id="d7438-141">If an automatic notification is already present in Action Center, setting this registry value causes the notification to be removed at 10:00 the following morning.</span></span>
-   <span data-ttu-id="d7438-142">如果值不存在，如果未設定其資料，或其資料設定為零，則不會關閉自動通知。</span><span class="sxs-lookup"><span data-stu-id="d7438-142">If the value does not exist, if its data is not set, or if its data is set to zero, the automatic notifications are not turned off.</span></span>

<span data-ttu-id="d7438-143">**Windows Vista 和 WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-143">**Windows Vista and Windows XP:** This registry value is not supported.</span></span>

## <a name="filesnottobackup"></a><span data-ttu-id="d7438-144">FilesNotToBackup</span><span class="sxs-lookup"><span data-stu-id="d7438-144">FilesNotToBackup</span></span>

<span data-ttu-id="d7438-145">**FilesNotToBackup** 登錄機碼會指定備份應用程式不應備份或還原的檔案和目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="d7438-145">The **FilesNotToBackup** registry key specifies the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="d7438-146">此機碼中的每個專案都是 \_ 使用 \_ 下列格式的 REG 多重 SZ 字串：</span><span class="sxs-lookup"><span data-stu-id="d7438-146">Each of the entries in this key is a REG\_MULTI\_SZ string in the following format:</span></span>

<span data-ttu-id="d7438-147">\[*磁片磁碟機* \] \[ \] 路徑 \\*檔案名* \[/s\]</span><span class="sxs-lookup"><span data-stu-id="d7438-147">\[*Drive*\]\[*Path*\]\\*FileName* \[/s\]</span></span>

-   <span data-ttu-id="d7438-148">*磁片* 磁碟機指定磁片磁碟機，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d7438-148">*Drive* specifies the drive and is optional.</span></span> <span data-ttu-id="d7438-149">例如，c：</span><span class="sxs-lookup"><span data-stu-id="d7438-149">For example, c:.</span></span> <span data-ttu-id="d7438-150">若要指定所有磁片磁碟機，請使用反斜線 (\\) ; 不需要任何磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="d7438-150">To specify all drives, use a backslash (\\); no drive letters are needed.</span></span>
-   <span data-ttu-id="d7438-151">*路徑* 指定路徑，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d7438-151">*Path* specifies the path and is optional.</span></span> <span data-ttu-id="d7438-152">它不能包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d7438-152">It cannot contain wildcard characters.</span></span>
-   <span data-ttu-id="d7438-153">*FileName* 會指定檔案或目錄，而且是必要的。</span><span class="sxs-lookup"><span data-stu-id="d7438-153">*FileName* specifies the file or directory and is required.</span></span> <span data-ttu-id="d7438-154">它可以包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d7438-154">It can contain wildcard characters.</span></span>
-   <span data-ttu-id="d7438-155">/s 指定要包含指定路徑的所有子目錄。</span><span class="sxs-lookup"><span data-stu-id="d7438-155">/s specifies that all subdirectories of the specified path are to be included.</span></span>
-   <span data-ttu-id="d7438-156">像是% Systemroot% 的環境變數可以替代整個字串的所有或部分。</span><span class="sxs-lookup"><span data-stu-id="d7438-156">Environment variables such as %Systemroot% can be substituted for all or part of the entire string.</span></span>

<span data-ttu-id="d7438-157">下表顯示一些一般專案。</span><span class="sxs-lookup"><span data-stu-id="d7438-157">The following table shows some typical entries.</span></span>

| <span data-ttu-id="d7438-158">專案名稱</span><span class="sxs-lookup"><span data-stu-id="d7438-158">Entry name</span></span>                             | <span data-ttu-id="d7438-159">預設值</span><span class="sxs-lookup"><span data-stu-id="d7438-159">Default value</span></span>                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7438-160">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="d7438-160">Internet Explorer</span></span>                      | <span data-ttu-id="d7438-161">暫存檔案</span><span class="sxs-lookup"><span data-stu-id="d7438-161">Temporary Files</span></span>                                                                           |
| <span data-ttu-id="d7438-162">記憶體分頁檔案</span><span class="sxs-lookup"><span data-stu-id="d7438-162">Memory Page File</span></span>                       | <span data-ttu-id="d7438-163">\\Pagefile.sys</span><span class="sxs-lookup"><span data-stu-id="d7438-163">\\Pagefile.sys</span></span>                                                                            |
| <span data-ttu-id="d7438-164">MS 分散式交易協調器</span><span class="sxs-lookup"><span data-stu-id="d7438-164">MS Distributed Transaction Coordinator</span></span> | <span data-ttu-id="d7438-165">C： \\ Windows \\ system32 \\ msdtc msdtc \\ 。記錄檔 C： \\ Windows \\ system32 \\ MSDtc \\ 追蹤 \\ dtctrace .log</span><span class="sxs-lookup"><span data-stu-id="d7438-165">C:\\Windows\\system32\\MSDtc\\MSDTC.LOG C:\\Windows\\system32\\MSDtc\\trace\\dtctrace.log</span></span> |
| <span data-ttu-id="d7438-166">離線檔案快取</span><span class="sxs-lookup"><span data-stu-id="d7438-166">Offline Files Cache</span></span>                    | <span data-ttu-id="d7438-167">% Systemroot% \\ CSC \\ \* /s</span><span class="sxs-lookup"><span data-stu-id="d7438-167">%Systemroot%\\CSC\\\* /s</span></span>                                                                  |
| <span data-ttu-id="d7438-168">電源管理</span><span class="sxs-lookup"><span data-stu-id="d7438-168">Power Management</span></span>                       | <span data-ttu-id="d7438-169">\\hiberfil.sys</span><span class="sxs-lookup"><span data-stu-id="d7438-169">\\hiberfil.sys</span></span>                                                                            |
| <span data-ttu-id="d7438-170">儲存單一版本</span><span class="sxs-lookup"><span data-stu-id="d7438-170">Single Instance Storage</span></span>                | <span data-ttu-id="d7438-171">\\SIS 一般存放區 \\ \* 。 \* /s</span><span class="sxs-lookup"><span data-stu-id="d7438-171">\\SIS Common Store\\\*.\* /s</span></span>                                                              |
| <span data-ttu-id="d7438-172">暫存檔案</span><span class="sxs-lookup"><span data-stu-id="d7438-172">Temporary Files</span></span>                        | <span data-ttu-id="d7438-173">% TEMP% \\ \* /s</span><span class="sxs-lookup"><span data-stu-id="d7438-173">%TEMP%\\\* /s</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="d7438-174">執行磁片區層級備份的應用程式通常會在區塊層級複製整個磁片區，因此在備份時無法接受 **FilesNotToBackup** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-174">Applications that perform volume-level backups generally do so by copying the entire volume at the block level, so they cannot honor the **FilesNotToBackup** registry key at backup time.</span></span> <span data-ttu-id="d7438-175">相反地，他們會等待還原時間，以刪除不會備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7438-175">Instead, they wait until restore time to delete the files that were not to be backed up.</span></span> <span data-ttu-id="d7438-176">在大部分的情況下，這是合理的策略。</span><span class="sxs-lookup"><span data-stu-id="d7438-176">In most cases, this is a reasonable strategy.</span></span> <span data-ttu-id="d7438-177">不過，在單一實例儲存體檔案的情況下，不能在還原時刪除 SIS 一般存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="d7438-177">However, in the case of Single Instance Storage files, the SIS Common Store files must not be deleted at restore time.</span></span>

 

<span data-ttu-id="d7438-178">針對區塊層級磁片區備份，Windows Server Backup 和 Windows Wbadmin 公用程式會在還原時刪除適當的檔案，以接受 **FilesNotToBackup** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-178">For block-level volume backups, Windows Server Backup and the Windows Wbadmin utility honor the **FilesNotToBackup** registry key by deleting the appropriate files at restore time.</span></span> <span data-ttu-id="d7438-179">系統還原和系統狀態備份不接受 **FilesNotToBackup** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-179">System Restore and System State Backup do not honor the **FilesNotToBackup** registry key.</span></span>

<span data-ttu-id="d7438-180">**WINDOWS XP：** 系統還原接受 **FilesNotToBackup** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-180">**Windows XP:** System Restore honors the **FilesNotToBackup** registry key.</span></span>

## <a name="filesnottosnapshot"></a><span data-ttu-id="d7438-181">FilesNotToSnapshot</span><span class="sxs-lookup"><span data-stu-id="d7438-181">FilesNotToSnapshot</span></span>

<span data-ttu-id="d7438-182">VSS 支援 **FilesNotToSnapshot** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-182">VSS supports the **FilesNotToSnapshot** registry key.</span></span> <span data-ttu-id="d7438-183">應用程式和服務可以使用此金鑰來指定要從新建立的陰影複製中刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7438-183">Applications and services can use this key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="d7438-184">如需詳細資訊，請參閱 [從陰影複製中排除](/windows/desktop/VSS/excluding-files-from-shadow-copies)檔案。</span><span class="sxs-lookup"><span data-stu-id="d7438-184">For more information, see [Excluding Files from Shadow Copies](/windows/desktop/VSS/excluding-files-from-shadow-copies).</span></span>

<span data-ttu-id="d7438-185">**Windows Server 2003 和 WINDOWS XP：** 不支援此登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-185">**Windows Server 2003 and Windows XP:** This registry key is not supported.</span></span>

<span data-ttu-id="d7438-186">針對區塊層級磁片區備份，Windows Server Backup 會在還原時刪除適當的檔案，以接受 **FilesNotToSnapshot** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-186">For block-level volume backups, Windows Server Backup honors the **FilesNotToSnapshot** registry key by deleting the appropriate files at restore time.</span></span>

## <a name="idletimeout"></a><span data-ttu-id="d7438-187">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="d7438-187">IdleTimeout</span></span>

<span data-ttu-id="d7438-188">**IdleTimeout** 登錄值會指定 VSS 服務閒置時的等候時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7438-188">The **IdleTimeout** registry value specifies the amount of time, in seconds, that the VSS service will wait when it is idle.</span></span> <span data-ttu-id="d7438-189">如果達到此超時值且沒有可執行檔工作，則 VSS 服務將會關閉。</span><span class="sxs-lookup"><span data-stu-id="d7438-189">If this timeout value is reached and there are no tasks for it to perform, the VSS service will shut down.</span></span>

<span data-ttu-id="d7438-190">您可以在下列登錄機碼下找到這個登錄值：</span><span class="sxs-lookup"><span data-stu-id="d7438-190">This registry value can be found under the following registry key:</span></span>

<span data-ttu-id="d7438-191">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **VSS** \\ **設定**</span><span class="sxs-lookup"><span data-stu-id="d7438-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**VSS**\\**Settings**</span></span>

<span data-ttu-id="d7438-192">如果此登錄值不存在：</span><span class="sxs-lookup"><span data-stu-id="d7438-192">If this registry value does not exist:</span></span>

-   <span data-ttu-id="d7438-193">使用的實際超時值為180秒 (3 分鐘) 預設為3分鐘。</span><span class="sxs-lookup"><span data-stu-id="d7438-193">The actual timeout value that is used is 180 seconds (3 minutes) by default.</span></span>
-   <span data-ttu-id="d7438-194">您可以建立具有名稱 **IdleTimeout** 和類型 DWORD 的值，並將它設定為所需的值。</span><span class="sxs-lookup"><span data-stu-id="d7438-194">You can create a value with the name **IdleTimeout** and the type DWORD and set it to the desired value.</span></span>

<span data-ttu-id="d7438-195">如果此登錄值設定為0秒：</span><span class="sxs-lookup"><span data-stu-id="d7438-195">If this registry value is set to 0 seconds:</span></span>

-   <span data-ttu-id="d7438-196">使用的實際超時值為180秒 (3 分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="d7438-196">The actual timeout value that is used is 180 seconds (3 minutes).</span></span>

<span data-ttu-id="d7438-197">如果您設定此登錄值：</span><span class="sxs-lookup"><span data-stu-id="d7438-197">If you set this registry value:</span></span>

-   <span data-ttu-id="d7438-198">VSS 會使用您設定的超時值。</span><span class="sxs-lookup"><span data-stu-id="d7438-198">VSS uses the timeout value that you set.</span></span>
-   <span data-ttu-id="d7438-199">您可以指定介於1到 FFFFFFFF 秒之間的任何值。</span><span class="sxs-lookup"><span data-stu-id="d7438-199">You can specify any value between 1 and FFFFFFFF seconds.</span></span> <span data-ttu-id="d7438-200">不過，建議您選擇介於1到180秒之間的值。</span><span class="sxs-lookup"><span data-stu-id="d7438-200">However, it is recommended that you choose a value between 1 and 180 seconds.</span></span>

<span data-ttu-id="d7438-201">**Windows Server 2003 和 WINDOWS XP：** 不支援此登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-201">**Windows Server 2003 and Windows XP:** This registry key is not supported.</span></span>

## <a name="keysnottorestore"></a><span data-ttu-id="d7438-202">KeysNotToRestore</span><span class="sxs-lookup"><span data-stu-id="d7438-202">KeysNotToRestore</span></span>

<span data-ttu-id="d7438-203">**KeysNotToRestore** 登錄機碼會指定備份應用程式不應還原的登錄子機碼和值的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7438-203">The **KeysNotToRestore** registry key specifies the names of the registry subkeys and values that backup applications should not restore.</span></span> <span data-ttu-id="d7438-204">如需詳細資訊，請參閱 [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="d7438-204">For more information, see [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)).</span></span> <span data-ttu-id="d7438-205">不需要接受 **KeysNotToRestore** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-205">It is not necessary to honor the **KeysNotToRestore** registry key.</span></span>

<span data-ttu-id="d7438-206">**Windows Server 2003 和 WINDOWS XP：** 您必須接受 **KeysNotToRestore** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-206">**Windows Server 2003 and Windows XP:** You must honor the **KeysNotToRestore** registry key.</span></span>

<span data-ttu-id="d7438-207">針對區塊層級磁片區備份，Windows Server Backup 會在還原時刪除適當的檔案，以接受 **KeysNotToRestore** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-207">For block-level volume backups, Windows Server Backup honors the **KeysNotToRestore** registry key by deleting the appropriate files at restore time.</span></span>

<span data-ttu-id="d7438-208">系統狀態備份會接受 **KeysNotToRestore** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d7438-208">System State Backup honors the **KeysNotToRestore** registry key.</span></span>

## <a name="lastinstance"></a><span data-ttu-id="d7438-209">LastInstance</span><span class="sxs-lookup"><span data-stu-id="d7438-209">LastInstance</span></span>

<span data-ttu-id="d7438-210">**LastInstance** 登錄值表示已執行裸機還原作業，而磁片區已被覆寫但未格式化。</span><span class="sxs-lookup"><span data-stu-id="d7438-210">The **LastInstance** registry value indicates that a bare-metal restore operation has been performed and that the volumes have been overwritten but not formatted.</span></span> <span data-ttu-id="d7438-211">如需詳細資訊，請參閱 [使用 VSS 自動化系統復原進行](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery)嚴重損壞修復。</span><span class="sxs-lookup"><span data-stu-id="d7438-211">For more information, see [Using VSS Automated System Recovery for Disaster Recovery](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).</span></span>

<span data-ttu-id="d7438-212">**Windows Server 2003 和 WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-212">**Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

## <a name="lastrestoreid"></a><span data-ttu-id="d7438-213">LastRestoreId</span><span class="sxs-lookup"><span data-stu-id="d7438-213">LastRestoreId</span></span>

<span data-ttu-id="d7438-214">當備份應用程式執行系統狀態還原時，它必須藉由設定 **LastRestoreId** 登錄值來指出它已完成。</span><span class="sxs-lookup"><span data-stu-id="d7438-214">When a backup application performs a system state restore, it must indicate that it has done so by setting the **LastRestoreId** registry value.</span></span> <span data-ttu-id="d7438-215">在此情況下，「系統狀態還原」指的是選擇性還原作業系統二進位檔和驅動程式的任何還原。</span><span class="sxs-lookup"><span data-stu-id="d7438-215">"System state restore" in this case refers to any restore that selectively restores operating system binaries and drivers.</span></span>

<span data-ttu-id="d7438-216">如果整個開機和系統磁碟區是在磁片區層級還原，則不能設定這個值。</span><span class="sxs-lookup"><span data-stu-id="d7438-216">If the entire boot and system volume are restored at the volume level, this value must not be set.</span></span>

<span data-ttu-id="d7438-217">如果 **LastRestoreId** 登錄值不存在，則備份應用程式應該在下列登錄機碼底下建立它：</span><span class="sxs-lookup"><span data-stu-id="d7438-217">If the **LastRestoreId** registry value does not exist, the backup application should create it under the following registry key:</span></span>

<span data-ttu-id="d7438-218">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **BackupRestore** \\ **SystemStateRestore**</span><span class="sxs-lookup"><span data-stu-id="d7438-218">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**BackupRestore**\\**SystemStateRestore**</span></span>

<span data-ttu-id="d7438-219">建立名稱為 **LastRestoreId** 且類型為 REG SZ 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7438-219">Create a value with the name **LastRestoreId** and type REG\_SZ.</span></span> <span data-ttu-id="d7438-220">此值應該是唯一的不透明值，例如 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7438-220">The value should be a unique opaque value such as a GUID.</span></span>

<span data-ttu-id="d7438-221">每當執行新的系統狀態還原時，備份應用程式應變更 **LastRestoreId** 值的資料。</span><span class="sxs-lookup"><span data-stu-id="d7438-221">Whenever a new system state restore is performed, the backup application should change the data of the **LastRestoreId** value.</span></span>

<span data-ttu-id="d7438-222">其他需要監視系統狀態還原的應用程式應該儲存此登錄值的資料。</span><span class="sxs-lookup"><span data-stu-id="d7438-222">Other applications that need to monitor system state restores should store the data of this registry value.</span></span> <span data-ttu-id="d7438-223">這項資料可以與 **LastRestoreId** 登錄值的目前資料進行比較，以判斷是否已執行新的系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="d7438-223">This data can be compared against the current data of the **LastRestoreId** registry value to determine whether a new system state restore has been performed.</span></span>

<span data-ttu-id="d7438-224">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 之前，不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-224">**Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="maxshadowcopies"></a><span data-ttu-id="d7438-225">MaxShadowCopies</span><span class="sxs-lookup"><span data-stu-id="d7438-225">MaxShadowCopies</span></span>

<span data-ttu-id="d7438-226">**MaxShadowCopies** 登錄值會指定可儲存在電腦每個磁片區上的 [*用戶端可存取陰影複製*](/windows/desktop/VSS/vssgloss-c)的最大數目。</span><span class="sxs-lookup"><span data-stu-id="d7438-226">The **MaxShadowCopies** registry value specifies the maximum number of [*client-accessible shadow copies*](/windows/desktop/VSS/vssgloss-c) that can be stored on each volume of the computer.</span></span> <span data-ttu-id="d7438-227">用戶端可存取的陰影複製是一種陰影複製，使用 [**\_ vss \_ 快照集 \_ 內容**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context)列舉的 **vss \_ CTX \_ 用戶端 \_ 可存取** 值建立。</span><span class="sxs-lookup"><span data-stu-id="d7438-227">A client-accessible shadow copy is a shadow copy that is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="d7438-228">共用資料夾陰影複製會使用用戶端可存取的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="d7438-228">Client-accessible shadow copies are used by Shadow Copies for Shared Folders.</span></span> <span data-ttu-id="d7438-229">如需陰影複製的詳細資訊，請參閱 [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) 檔集。</span><span class="sxs-lookup"><span data-stu-id="d7438-229">For more information about shadow copies, see the [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) documentation.</span></span>

<span data-ttu-id="d7438-230">如果 **MaxShadowCopies** 登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它：</span><span class="sxs-lookup"><span data-stu-id="d7438-230">If the **MaxShadowCopies** registry value does not exist, the backup application can create it under the following registry key:</span></span>

<span data-ttu-id="d7438-231">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **VSS** \\ **設定**</span><span class="sxs-lookup"><span data-stu-id="d7438-231">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**VSS**\\**Settings**</span></span>

<span data-ttu-id="d7438-232">建立名稱為 **MaxShadowCopies** 和類型為 DWORD 的值。</span><span class="sxs-lookup"><span data-stu-id="d7438-232">Create a value with the name **MaxShadowCopies** and type DWORD.</span></span> <span data-ttu-id="d7438-233">此值的預設資料為64。</span><span class="sxs-lookup"><span data-stu-id="d7438-233">The default data for this value is 64.</span></span> <span data-ttu-id="d7438-234">最小值為1。</span><span class="sxs-lookup"><span data-stu-id="d7438-234">The minimum is 1.</span></span> <span data-ttu-id="d7438-235">最大值為512。</span><span class="sxs-lookup"><span data-stu-id="d7438-235">The maximum is 512.</span></span>

> [!Note]  
> <span data-ttu-id="d7438-236">若是其他類型的陰影複製，則沒有對應至 **MaxShadowCopies** 的登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-236">For other types of shadow copies, there is no registry value that corresponds to **MaxShadowCopies**.</span></span> <span data-ttu-id="d7438-237">每個磁片區的陰影複製數目上限為512。</span><span class="sxs-lookup"><span data-stu-id="d7438-237">The maximum number of shadow copies is 512 per volume.</span></span>

 

<span data-ttu-id="d7438-238">**注意**  Windows Server 2003 或更新版本支援 **MaxShadowCopies** 設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-238">**Note**  The **MaxShadowCopies** setting is supported on Windows Server 2003 or later.</span></span>

<span data-ttu-id="d7438-239">**Windows Server 2003：** 在叢集伺服器上， **MaxShadowCopies** 登錄值的資料可能需要設定為較低的數位。</span><span class="sxs-lookup"><span data-stu-id="d7438-239">**Windows Server 2003:** On cluster servers, **MaxShadowCopies** registry value's data may need to be set to a lower number.</span></span> <span data-ttu-id="d7438-240">For more information, see "When you use the Volume Shadow Copy Service on Windows Server 2003-based computers that run many I/O operations, disk volumes take longer to go online" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058).</span><span class="sxs-lookup"><span data-stu-id="d7438-240">For more information, see "When you use the Volume Shadow Copy Service on Windows Server 2003-based computers that run many I/O operations, disk volumes take longer to go online" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058).</span></span>

<span data-ttu-id="d7438-241">**WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-241">**Windows XP:** This registry value is not supported.</span></span>

## <a name="mindiffareafilesize"></a><span data-ttu-id="d7438-242">MinDiffAreaFileSize</span><span class="sxs-lookup"><span data-stu-id="d7438-242">MinDiffAreaFileSize</span></span>

<span data-ttu-id="d7438-243">[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) 會配置陰影複製存放區域 (或「差異區域」 ) 來儲存陰影複製的資料。</span><span class="sxs-lookup"><span data-stu-id="d7438-243">[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) allocates a shadow copy storage area (or "diff area") to store data for shadow copies.</span></span> <span data-ttu-id="d7438-244">陰影複製存放區域的大小下限是可使用 **MinDiffAreaFileSize** 登錄值指定的每部電腦設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-244">The minimum size of the shadow copy storage area is a per-computer setting that can be specified by using the **MinDiffAreaFileSize** registry value.</span></span>

<span data-ttu-id="d7438-245">如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的大小下限為 32 mb，適用于小於 500 mb 的磁片區，以及大於 500 mb 的磁片區的 320 mb。</span><span class="sxs-lookup"><span data-stu-id="d7438-245">If the **MinDiffAreaFileSize** registry value is not set, the minimum size of the shadow copy storage area is 32 MB for volumes that are smaller than 500 MB and 320 MB for volumes that are larger than 500 MB.</span></span>

<span data-ttu-id="d7438-246">**Windows server 2008、Windows server 2003 SP1 和 Windows Vista：** 如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的最小大小為 300 MB。</span><span class="sxs-lookup"><span data-stu-id="d7438-246">**Windows Server 2008, Windows Server 2003 with SP1 and Windows Vista:** If the **MinDiffAreaFileSize** registry value is not set, the shadow copy storage area has a minimum size of 300 MB.</span></span> <span data-ttu-id="d7438-247">如果已設定 **MinDiffAreaFileSize** 登錄值，其資料必須介於 300 mb 到 3000 mb (3 GB) ，而且必須是 300 MB 的倍數。</span><span class="sxs-lookup"><span data-stu-id="d7438-247">If the **MinDiffAreaFileSize** registry value is set, its data must be between 300 MB and 3000 MB (3 GB), and it must be a multiple of 300 MB.</span></span>

<span data-ttu-id="d7438-248">**Windows Server 2003：** 如果未設定 **MinDiffAreaFileSize** 登錄值，陰影複製存放區域的大小下限為 100 MB。</span><span class="sxs-lookup"><span data-stu-id="d7438-248">**Windows Server 2003:** If the **MinDiffAreaFileSize** registry value is not set, the minimum size of the shadow copy storage area is 100 MB.</span></span>

<span data-ttu-id="d7438-249">**WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-249">**Windows XP:** This registry value is not supported.</span></span>

<span data-ttu-id="d7438-250">如果 **MinDiffAreaFileSize** 登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它：</span><span class="sxs-lookup"><span data-stu-id="d7438-250">If the **MinDiffAreaFileSize** registry value does not exist, the backup application can create it under the following registry key:</span></span>

<span data-ttu-id="d7438-251">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**</span><span class="sxs-lookup"><span data-stu-id="d7438-251">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**VolSnap**</span></span>

<span data-ttu-id="d7438-252">建立名稱為 **MinDiffAreaFileSize** 的值，並輸入 REG \_ DWORD。</span><span class="sxs-lookup"><span data-stu-id="d7438-252">Create a value with the name **MinDiffAreaFileSize** and type REG\_DWORD.</span></span> <span data-ttu-id="d7438-253">此索引鍵的資料會以 mb 為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="d7438-253">The data for this key is specified in megabytes.</span></span> <span data-ttu-id="d7438-254">320等於 320 MB，而3200等於 3.2 GB。</span><span class="sxs-lookup"><span data-stu-id="d7438-254">320 is equal to 320 MB, and 3200 is equal to 3.2 GB.</span></span> <span data-ttu-id="d7438-255">您應該指定一個數位，其為32的倍數。</span><span class="sxs-lookup"><span data-stu-id="d7438-255">You should specify a number that is a multiple of 32.</span></span> <span data-ttu-id="d7438-256">如果您指定的值不是32的倍數，則會使用32的下一個倍數。</span><span class="sxs-lookup"><span data-stu-id="d7438-256">If you specify a value that is not a multiple of 32, the next multiple of 32 will be used.</span></span>

<span data-ttu-id="d7438-257">如果 **MinDiffAreaFileSize** 登錄值指定的大小下限大於陰影複製存放區的大小上限，則陰影複製可能無法正確運作。</span><span class="sxs-lookup"><span data-stu-id="d7438-257">Shadow copies might not function correctly if the **MinDiffAreaFileSize** registry value specifies a minimum size that is larger than the maximum size of the shadow copy storage area.</span></span> <span data-ttu-id="d7438-258">若要指定陰影複製存放區的大小上限，請使用 [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add Shadowstorage 或 vssadmin resize shadowstorage 命令。</span><span class="sxs-lookup"><span data-stu-id="d7438-258">To specify the maximum size of the shadow copy storage area, use the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add shadowstorage or the Vssadmin resize shadowstorage command.</span></span> <span data-ttu-id="d7438-259">若要查看目前的大小上限，請使用 [Vssadmin list shadowstorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 命令。</span><span class="sxs-lookup"><span data-stu-id="d7438-259">To see the current maximum size, use the [Vssadmin list shadowstorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="d7438-260">如果您未設定大小上限，則可以使用的空間量沒有限制。</span><span class="sxs-lookup"><span data-stu-id="d7438-260">If you have not set a maximum size, there is no limit to the amount of space that can be used.</span></span>

## <a name="overallperformancesetting-and-customperformancesettings"></a><span data-ttu-id="d7438-261">OverallPerformanceSetting 和 CustomPerformanceSettings</span><span class="sxs-lookup"><span data-stu-id="d7438-261">OverallPerformanceSetting and CustomPerformanceSettings</span></span>

<span data-ttu-id="d7438-262">**OverallPerformanceSetting** 和 **CustomPerformanceSettings** 登錄值是用來指定 Windows Server Backup 的效能設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-262">The **OverallPerformanceSetting** and **CustomPerformanceSettings** registry values are used to specify performance settings for Windows Server Backup.</span></span> <span data-ttu-id="d7438-263">只有在 Windows server 作業系統上才支援這些登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-263">These registry values are supported only on Windows server operating systems.</span></span>

<span data-ttu-id="d7438-264">**Windows Server 2003：** 不支援這些登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-264">**Windows Server 2003:** These registry values are not supported.</span></span>

<span data-ttu-id="d7438-265">如果這些登錄值不存在，則備份應用程式可以在下列登錄機碼底下建立它們：</span><span class="sxs-lookup"><span data-stu-id="d7438-265">If these registry values do not exist, the backup application can create them under the following registry key:</span></span>

<span data-ttu-id="d7438-266">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **windows** \\ **CurrentVersion** \\ **windows 區塊層級備份**</span><span class="sxs-lookup"><span data-stu-id="d7438-266">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Windows Block Level Backup**</span></span>

<span data-ttu-id="d7438-267">若要指定所有磁片區的效能設定，請建立名稱為 **OverallPerformanceSetting** 的值，並輸入 REG \_ DWORD。</span><span class="sxs-lookup"><span data-stu-id="d7438-267">To specify performances settings for all volumes, create a value with the name **OverallPerformanceSetting** and type REG\_DWORD.</span></span> <span data-ttu-id="d7438-268">值的資料應該設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d7438-268">The value's data should be set to one of the following values.</span></span>

| <span data-ttu-id="d7438-269">值</span><span class="sxs-lookup"><span data-stu-id="d7438-269">Value</span></span> | <span data-ttu-id="d7438-270">意義</span><span class="sxs-lookup"><span data-stu-id="d7438-270">Meaning</span></span>                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7438-271">1</span><span class="sxs-lookup"><span data-stu-id="d7438-271">1</span></span>     | <span data-ttu-id="d7438-272">一般備份效能 (使用完整備份) 。</span><span class="sxs-lookup"><span data-stu-id="d7438-272">Normal backup performance (by using full backups).</span></span> <span data-ttu-id="d7438-273">這項設定會對應到 [ [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))] 中所述的一般備份效能設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-273">This setting corresponds to the Normal backup performance setting described in [Optimizing Backup and Server Performance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).</span></span>            |
| <span data-ttu-id="d7438-274">2</span><span class="sxs-lookup"><span data-stu-id="d7438-274">2</span></span>     | <span data-ttu-id="d7438-275">使用增量備份) 來加快備份效能 (。</span><span class="sxs-lookup"><span data-stu-id="d7438-275">Faster backup performance (by using incremental backups).</span></span> <span data-ttu-id="d7438-276">這項設定會對應到 [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))中所述的更快備份效能設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-276">This setting corresponds to the Faster backup performance setting described in [Optimizing Backup and Server Performance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).</span></span>     |
| <span data-ttu-id="d7438-277">3</span><span class="sxs-lookup"><span data-stu-id="d7438-277">3</span></span>     | <span data-ttu-id="d7438-278">藉由指定每個磁片區) 的效能設定，可 (自訂備份效能。</span><span class="sxs-lookup"><span data-stu-id="d7438-278">Custom backup performance (by specifying a performance setting for each volume).</span></span> <span data-ttu-id="d7438-279">這項設定會對應到 [ [優化備份和伺服器效能](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))] 中所述的自訂設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-279">This setting corresponds to the Custom setting described in [Optimizing Backup and Server Performance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).</span></span> |



 

<span data-ttu-id="d7438-280">如果您將 **OverallPerformanceSetting** 設定為3，您也必須個別指定每個磁片區的效能設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-280">If you set **OverallPerformanceSetting** to 3, you must also specify performances settings for each volume individually.</span></span> <span data-ttu-id="d7438-281">若要這樣做，請建立名稱為 **CustomPerformanceSettings** 且類型為 REG \_ 多重 \_ SZ 的值。</span><span class="sxs-lookup"><span data-stu-id="d7438-281">To do this, create a value with the name **CustomPerformanceSettings** and type REG\_MULTI\_SZ.</span></span> <span data-ttu-id="d7438-282">此值的資料應設定如下：</span><span class="sxs-lookup"><span data-stu-id="d7438-282">This value's data should be set as follows:</span></span>

-   <span data-ttu-id="d7438-283">REG 多重 SZ 字串中的每個字串都 \_ \_ 包含磁片區的設定。</span><span class="sxs-lookup"><span data-stu-id="d7438-283">Each string in the REG\_MULTI\_SZ sequence of strings contains the setting for a volume.</span></span>
-   <span data-ttu-id="d7438-284">每個字串都包含一個磁片區 GUID，後面接著一個逗號，後面接著一個 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="d7438-284">Each string consists of a volume GUID, followed by a comma, followed by a DWORD value.</span></span>
-   <span data-ttu-id="d7438-285">每個 DWORD 值都可以是 1 (完整備份) 或 2 (增量備份) 。</span><span class="sxs-lookup"><span data-stu-id="d7438-285">Each of the DWORD values is either 1 (full backup) or 2 (incremental backup).</span></span>

<span data-ttu-id="d7438-286">例如，假設電腦有兩個磁片區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d7438-286">For example, suppose the computer has two volumes as follows:</span></span>

-   <span data-ttu-id="d7438-287">這兩個磁片區為 C： \\ 和 D： \\ 。</span><span class="sxs-lookup"><span data-stu-id="d7438-287">The two volumes are C:\\ and D:\\.</span></span>
-   <span data-ttu-id="d7438-288">磁片區 C：的 GUID \\ 是 07c473ca4-2df8-11de-9d80-806e6f6e6963，而磁片區 D：的 guid \\ 是 0ac22ea6c-712f-11de-adb0-00215a67606e。</span><span class="sxs-lookup"><span data-stu-id="d7438-288">The GUID for volume C:\\ is 07c473ca4-2df8-11de-9d80-806e6f6e6963, and the GUID for volume D:\\ is 0ac22ea6c-712f-11de-adb0-00215a67606e.</span></span>
-   <span data-ttu-id="d7438-289">您想要指定磁片區 C 的一般備份 perfornance： \\ 磁片區 D：的備份效能更快 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d7438-289">You want to specify normal backup perfornance for volume C:\\ and faster backup performance for volume D:\\.</span></span>

<span data-ttu-id="d7438-290">若要這樣做，您可以將 **OverallPerformanceSetting** 設定為3，並將 **CustomPerformanceSettings** 設定為 "07c473ca4-2df8-11de-9d80-806e6f6e6963，1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e，2"。</span><span class="sxs-lookup"><span data-stu-id="d7438-290">To do this, you would set **OverallPerformanceSetting** to 3 and **CustomPerformanceSettings** to "07c473ca4-2df8-11de-9d80-806e6f6e6963,1\\00ac22ea6c-712f-11de-adb0-00215a67606e,2".</span></span>

<span data-ttu-id="d7438-291">如果您將 **OverallPerformanceSetting** 設定為1或2，則會忽略 **CustomPerformanceSettings** 值中的資料。</span><span class="sxs-lookup"><span data-stu-id="d7438-291">If you set **OverallPerformanceSetting** to 1 or 2, the data in the **CustomPerformanceSettings** value is ignored.</span></span>

## <a name="sysvol"></a><span data-ttu-id="d7438-292">SYSVOL</span><span class="sxs-lookup"><span data-stu-id="d7438-292">SYSVOL</span></span>

<span data-ttu-id="d7438-293">**SYSVOL** 登錄值是一種方式，可通知分散式檔案系統複寫 (DFSR) 服務，表示已起始系統狀態還原作業。</span><span class="sxs-lookup"><span data-stu-id="d7438-293">The **SYSVOL** registry value is a way to notify the Distributed File System Replication (DFSR) service that a system state restore operation has been initiated.</span></span> <span data-ttu-id="d7438-294">任何執行 SYSVOL 系統狀態還原的備份應用程式，都應該使用此值來指出還原作業是否為授權或非授權。</span><span class="sxs-lookup"><span data-stu-id="d7438-294">Any backup application that performs system state restore of SYSVOL should use this value to indicate whether the restore operation is authoritative or nonauthoritative.</span></span> <span data-ttu-id="d7438-295">DFSR 服務會讀取這個值。</span><span class="sxs-lookup"><span data-stu-id="d7438-295">This value is read by the DFSR service.</span></span> <span data-ttu-id="d7438-296">如果未設定此值，則預設會執行 nonauthoritatively 的 SYSVOL 還原。</span><span class="sxs-lookup"><span data-stu-id="d7438-296">If this value is not set, the SYSVOL restore is performed nonauthoritatively by default.</span></span>

<span data-ttu-id="d7438-297">如果 **SYSVOL** 登錄值不存在，則備份應用程式應該在下列登錄機碼底下建立它：</span><span class="sxs-lookup"><span data-stu-id="d7438-297">If the **SYSVOL** registry value does not exist, the backup application should create it under the following registry key:</span></span>

<span data-ttu-id="d7438-298">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **還原**</span><span class="sxs-lookup"><span data-stu-id="d7438-298">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**DFSR**\\**Restore**</span></span>

<span data-ttu-id="d7438-299">建立名稱為 **SYSVOL** 的值，並輸入 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="d7438-299">Create a value with the name **SYSVOL** and type REG\_SZ.</span></span> <span data-ttu-id="d7438-300">根據系統管理員的要求，值的資料應該設定為「授權」或「非授權」。</span><span class="sxs-lookup"><span data-stu-id="d7438-300">The value's data should be set to either "authoritative" or "non-authoritative" based on the system administrator's request.</span></span>

<span data-ttu-id="d7438-301">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="d7438-301">**Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

 

 
