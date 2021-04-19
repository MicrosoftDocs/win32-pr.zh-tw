---
description: Winmgmt 是在 &0034 下執行的 SVCHOST 進程內的 WMI 服務 \# ;LocalSystem&\# 0034; 帳戶。
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982714"
---
# <a name="winmgmt"></a><span data-ttu-id="e8cad-103">winmgmt</span><span class="sxs-lookup"><span data-stu-id="e8cad-103">winmgmt</span></span>

<span data-ttu-id="e8cad-104">Winmgmt 是在「LocalSystem」帳戶下執行的 SVCHOST 進程內的 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="e8cad-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="e8cad-105">在所有情況下，WMI 服務會在第一個管理應用程式或腳本要求與 WMI 命名空間的連接時自動啟動。</span><span class="sxs-lookup"><span data-stu-id="e8cad-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="e8cad-106">如需詳細資訊，請參閱[啟動和停止 WMI 服務](starting-and-stopping-the-wmi-service.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8cad-107">WMI 是 Windows 作業系統的核心元件，可讓開發人員和 IT 系統管理員撰寫腳本和應用程式，以將某些工作自動化。</span><span class="sxs-lookup"><span data-stu-id="e8cad-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="e8cad-108">Winmgmt.exe 是允許 WMI 在本機電腦上執行的服務。</span><span class="sxs-lookup"><span data-stu-id="e8cad-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="e8cad-109">如需使用 WMI 的詳細資訊，請參閱 [使用 wmi](using-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="e8cad-110">如果您收到有關 winmgmt.exe 的錯誤訊息，請參閱 [WMI 疑難排解](wmi-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="e8cad-111">如需 Winmgmt.exe 的詳細資訊，請參閱 [使用 WMI 管理工具](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="e8cad-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="e8cad-112">從命令提示字元執行時，WMI 服務會有下列參數。</span><span class="sxs-lookup"><span data-stu-id="e8cad-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="e8cad-113">交換器</span><span class="sxs-lookup"><span data-stu-id="e8cad-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="e8cad-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="e8cad-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cad-115">導致 WMI 將存放庫備份至指定的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e8cad-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="e8cad-116">*Filename* 引數應該包含檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e8cad-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="e8cad-117">此程式需要儲存機制的寫入鎖定，如此一來，儲存機制的寫入作業才會暫止，直到備份程式完成為止。</span><span class="sxs-lookup"><span data-stu-id="e8cad-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="e8cad-118">如果您未指定檔案的路徑，它會放在% Windir% \\ System32 目錄中。</span><span class="sxs-lookup"><span data-stu-id="e8cad-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="e8cad-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cad-120">從指定的備份檔案手動還原 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="e8cad-121">*Filename* 引數應該包含備份檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e8cad-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="e8cad-122">若要執行還原作業，WMI 會儲存現有的存放庫，以在作業失敗時回寫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="e8cad-123">然後，系統會從 *filename* 引數中指定的備份檔案還原存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="e8cad-124">如果無法取得存放庫的獨佔存取權，現有的用戶端就會從 WMI 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="e8cad-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="e8cad-125">*旗* 標引數必須是 1 (強制中斷使用者連線，並還原) 或 0 (預設還原（如果沒有任何使用者連接) 並指定還原模式）。</span><span class="sxs-lookup"><span data-stu-id="e8cad-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<winmgmt-服務-處理序識別碼>*</span><span class="sxs-lookup"><span data-stu-id="e8cad-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cad-127">使用 WMI 註冊電腦的效能程式庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="e8cad-128">WMI PID 是 WMI 服務的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8cad-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="e8cad-129">只有在效能監視類別未傳回可靠的結果時才需要。</span><span class="sxs-lookup"><span data-stu-id="e8cad-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="e8cad-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="e8cad-131">將 Winmgmt 服務移至具有固定 DCOM 端點的獨立 Svchost 進程。</span><span class="sxs-lookup"><span data-stu-id="e8cad-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="e8cad-132">預設端點為「ncacn \_ ip \_ 0.24158」。</span><span class="sxs-lookup"><span data-stu-id="e8cad-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="e8cad-133">不過，您可以藉由執行 Dcomcnfg.exe 來變更端點。</span><span class="sxs-lookup"><span data-stu-id="e8cad-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="e8cad-134">如需設定 WMI 固定通訊埠的詳細資訊，請參閱 [設定 wmi 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="e8cad-135">*層級* 引數是 Svchost 進程的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="e8cad-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="e8cad-136">WMI 通常會作為共用服務主機的一部分來執行，而且您無法單獨增加 WMI 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="e8cad-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="e8cad-137">如果未指定 *層級* ，預設值為 4 (**RPC \_ C \_ 驗證 \_ level \_ PKT** 或 **WbemAuthenticationLevelPkt**) 。</span><span class="sxs-lookup"><span data-stu-id="e8cad-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="e8cad-138">您可以藉由將驗證等級提高為封包隱私權 (**RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** 或 **WbemAuthenticationLevelPktPrivacy**) ，更安全地執行 WMI。</span><span class="sxs-lookup"><span data-stu-id="e8cad-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="e8cad-139">Visual Basic 和腳本的驗證層級會在 [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)中說明。</span><span class="sxs-lookup"><span data-stu-id="e8cad-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="e8cad-140">若為 c + +，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="e8cad-141">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="e8cad-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="e8cad-143">將 Winmgmt 服務移至共用的 Svchost 進程。</span><span class="sxs-lookup"><span data-stu-id="e8cad-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="e8cad-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cad-145">在 WMI 儲存機制上執行一致性檢查。</span><span class="sxs-lookup"><span data-stu-id="e8cad-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="e8cad-146">當您新增沒有引數的 **/verifyrepository** 參數時 *<path>* ，系統就會驗證 WMI 目前使用的即時存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="e8cad-147">當您指定 *path* 引數時，您可以驗證儲存機制的任何儲存複本。</span><span class="sxs-lookup"><span data-stu-id="e8cad-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="e8cad-148">在此情況下，path 引數應該包含已儲存存放庫複本的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e8cad-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="e8cad-149">儲存的存放庫應該是整個存放庫資料夾的複本。</span><span class="sxs-lookup"><span data-stu-id="e8cad-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="e8cad-150">如需有關此命令所傳回錯誤的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="e8cad-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="e8cad-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="e8cad-152">在 WMI 存放庫上執行一致性檢查，如果偵測到不一致的情況，則重建存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="e8cad-153">不一致存放庫的內容會合並到重建的儲存機制中（如果可以讀取）。</span><span class="sxs-lookup"><span data-stu-id="e8cad-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="e8cad-154">搶救作業一律適用于 WMI 服務目前使用的存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="e8cad-155">如需有關此命令所傳回錯誤的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="e8cad-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="e8cad-156">包含 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器語句的% MOF 檔案會還原至存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="e8cad-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="e8cad-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="e8cad-158">第一次安裝作業系統時，系統會將存放庫重設為初始狀態。</span><span class="sxs-lookup"><span data-stu-id="e8cad-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="e8cad-159">包含 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器語句的 MOF 檔案會還原至存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8cad-160">備註</span><span class="sxs-lookup"><span data-stu-id="e8cad-160">Remarks</span></span>

<span data-ttu-id="e8cad-161">此工具位於% Windir% \\ System32 \\ wbem 目錄中。</span><span class="sxs-lookup"><span data-stu-id="e8cad-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="e8cad-162">如需可用參數的清單，請 `WinMgmt /?` 在命令提示字元中輸入。</span><span class="sxs-lookup"><span data-stu-id="e8cad-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="e8cad-163">WMI 存放庫（也稱為 CIM 存放庫）不只是單一檔案，而是存放庫資料夾中的檔案集合，可一起做為資料庫。</span><span class="sxs-lookup"><span data-stu-id="e8cad-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="e8cad-164">當您使用 **/backup** 參數來備份儲存機制時，產生的備份會是單一壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="e8cad-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="e8cad-165">如果驗證作業指出存放庫的狀態不一致，WMI 會傳回錯誤 **\_ 內部 \_ 資料庫 \_ 損毀** (net helpmsg 1358) 。</span><span class="sxs-lookup"><span data-stu-id="e8cad-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="e8cad-166">此錯誤可以從執行存放庫驗證的任何命令傳回，例如 **/verifyrepository** 或 **/salvagerepository**。</span><span class="sxs-lookup"><span data-stu-id="e8cad-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="e8cad-167">如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。</span><span class="sxs-lookup"><span data-stu-id="e8cad-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="e8cad-168">失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8cad-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="e8cad-169">在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e8cad-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="e8cad-170">如需問題來源的詳細資訊，請下載並執行 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) 診斷命令列工具。</span><span class="sxs-lookup"><span data-stu-id="e8cad-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="e8cad-171">這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。</span><span class="sxs-lookup"><span data-stu-id="e8cad-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="e8cad-172">報表也會協助 Microsoft 支援服務協助您。</span><span class="sxs-lookup"><span data-stu-id="e8cad-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="e8cad-173">您可以下載 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)。</span><span class="sxs-lookup"><span data-stu-id="e8cad-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8cad-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8cad-174">Requirements</span></span>



| <span data-ttu-id="e8cad-175">需求</span><span class="sxs-lookup"><span data-stu-id="e8cad-175">Requirement</span></span> | <span data-ttu-id="e8cad-176">值</span><span class="sxs-lookup"><span data-stu-id="e8cad-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e8cad-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8cad-177">Minimum supported client</span></span><br/> | <span data-ttu-id="e8cad-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8cad-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e8cad-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8cad-179">Minimum supported server</span></span><br/> | <span data-ttu-id="e8cad-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8cad-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8cad-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8cad-181">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8cad-182">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="e8cad-182">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="e8cad-183">從 Vista 開始從遠端連線至 WMI</span><span class="sxs-lookup"><span data-stu-id="e8cad-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

