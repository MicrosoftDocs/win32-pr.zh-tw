---
title: 'Win32_Service 類別的變更方法 (Mbnapi)  (TerminalService) '
description: 修改 Win32 \_ TerminalService。
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- 變更方法遠端桌面服務
- 變更方法遠端桌面服務、Win32_Service 類別
- Win32_Service 類別遠端桌面服務，變更方法
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106995136"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="12b2b-106">Win32_Service 類別的 Change 方法 (Mbnapi) -TerminalService</span><span class="sxs-lookup"><span data-stu-id="12b2b-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="12b2b-107">**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ TerminalService**](win32-terminalservice.md)。</span><span class="sxs-lookup"><span data-stu-id="12b2b-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="12b2b-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="12b2b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="12b2b-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="12b2b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="12b2b-110">語法</span><span class="sxs-lookup"><span data-stu-id="12b2b-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="12b2b-111">參數</span><span class="sxs-lookup"><span data-stu-id="12b2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b2b-112">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-113">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="12b2b-113">The display name of the service.</span></span> <span data-ttu-id="12b2b-114">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="12b2b-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="12b2b-115">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="12b2b-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="12b2b-116">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="12b2b-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="12b2b-117">條件約束：接受與 **Name** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="12b2b-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="12b2b-118">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="12b2b-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-119">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-120">執行服務之可執行檔的完整路徑，例如「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="12b2b-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-121">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-122">提供給呼叫它們之進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="12b2b-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="12b2b-123">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="12b2b-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-124">核心驅動程式</span><span class="sxs-lookup"><span data-stu-id="12b2b-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-125">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="12b2b-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-126">檔案系統驅動程式</span><span class="sxs-lookup"><span data-stu-id="12b2b-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-127">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="12b2b-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-128">配接器</span><span class="sxs-lookup"><span data-stu-id="12b2b-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-129">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="12b2b-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-130">辨識器驅動程式</span><span class="sxs-lookup"><span data-stu-id="12b2b-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-131">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="12b2b-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-132">自有進程</span><span class="sxs-lookup"><span data-stu-id="12b2b-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-133">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="12b2b-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-134">共用進程</span><span class="sxs-lookup"><span data-stu-id="12b2b-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="12b2b-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-136">互動式進程</span><span class="sxs-lookup"><span data-stu-id="12b2b-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="12b2b-137">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-138">當此服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="12b2b-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="12b2b-139">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="12b2b-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="12b2b-140">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="12b2b-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="12b2b-141">0</span><span class="sxs-lookup"><span data-stu-id="12b2b-141">0</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-142">**Ignore**。</span><span class="sxs-lookup"><span data-stu-id="12b2b-142">**Ignore**.</span></span> <span data-ttu-id="12b2b-143">啟動會繼續。</span><span class="sxs-lookup"><span data-stu-id="12b2b-143">Startup continues.</span></span> <span data-ttu-id="12b2b-144">未向使用者提供服務失敗的通知。</span><span class="sxs-lookup"><span data-stu-id="12b2b-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-145">1</span><span class="sxs-lookup"><span data-stu-id="12b2b-145">1</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-146">**正常。**</span><span class="sxs-lookup"><span data-stu-id="12b2b-146">**Normal.**</span></span> <span data-ttu-id="12b2b-147">啟動會繼續。</span><span class="sxs-lookup"><span data-stu-id="12b2b-147">Startup continues.</span></span> <span data-ttu-id="12b2b-148">在使用者登入之前，使用者會收到通知：「在啟動期間，至少有一個服務或裝置失敗。」</span><span class="sxs-lookup"><span data-stu-id="12b2b-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-149">2</span><span class="sxs-lookup"><span data-stu-id="12b2b-149">2</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-150">**嚴重。**</span><span class="sxs-lookup"><span data-stu-id="12b2b-150">**Severe.**</span></span> <span data-ttu-id="12b2b-151">電腦嘗試以最後一個已知的正確設定重新開機。</span><span class="sxs-lookup"><span data-stu-id="12b2b-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="12b2b-152">如果服務再次失敗，則會繼續啟動，並將通知提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="12b2b-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-153">3</span><span class="sxs-lookup"><span data-stu-id="12b2b-153">3</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-154">**關鍵。**</span><span class="sxs-lookup"><span data-stu-id="12b2b-154">**Critical.**</span></span> <span data-ttu-id="12b2b-155">電腦嘗試以最後一個已知的正確設定重新開機。</span><span class="sxs-lookup"><span data-stu-id="12b2b-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="12b2b-156">如果服務再次失敗，啟動就會停止。</span><span class="sxs-lookup"><span data-stu-id="12b2b-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="12b2b-157">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-158">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="12b2b-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="12b2b-159">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="12b2b-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="12b2b-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**引導**</span><span class="sxs-lookup"><span data-stu-id="12b2b-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="12b2b-161">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="12b2b-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="12b2b-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**系統**</span><span class="sxs-lookup"><span data-stu-id="12b2b-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="12b2b-163">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="12b2b-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="12b2b-164">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="12b2b-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動**</span><span class="sxs-lookup"><span data-stu-id="12b2b-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="12b2b-166">服務控制管理員會在系統啟動期間自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="12b2b-167">自動啟動服務會在使用者登入電腦之前啟動，即使沒有任何使用者登入電腦，也會執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="12b2b-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動**</span><span class="sxs-lookup"><span data-stu-id="12b2b-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="12b2b-169">當進程呼叫 [**StartService**](win32-terminalservice-startservice.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="12b2b-170">雖然手動服務必須由使用者 (或腳本) 來明確啟動，但是即使使用者登出，還是會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="12b2b-171">手動服務通常稱為「隨選服務」。</span><span class="sxs-lookup"><span data-stu-id="12b2b-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12b2b-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**</span><span class="sxs-lookup"><span data-stu-id="12b2b-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="12b2b-173">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-173">Service that can no longer be started.</span></span> <span data-ttu-id="12b2b-174">若要啟動已停用的服務，您必須先將 [啟動] 選項變更為 [自動] 或 [手動]。</span><span class="sxs-lookup"><span data-stu-id="12b2b-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="12b2b-175">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-176">若 **為 True**，則服務可以建立或與桌面上的視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="12b2b-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-177">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-178">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="12b2b-178">Account name the service runs under.</span></span> <span data-ttu-id="12b2b-179">根據服務類型而定，帳戶名稱可能採用 DomainName 使用者名稱或的形式 \\ 。 \\使用者。</span><span class="sxs-lookup"><span data-stu-id="12b2b-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="12b2b-180">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="12b2b-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="12b2b-181">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="12b2b-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="12b2b-182">如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="12b2b-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="12b2b-183">若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="12b2b-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="12b2b-184">如果指定了 **Null** ，驅動程式就會根據服務名稱（例如 "DWDOM Admin"），以 i/o 系統建立的預設物件名稱執行 \\ 。</span><span class="sxs-lookup"><span data-stu-id="12b2b-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="12b2b-185">您也可以使用 (UPN) 格式的使用者主體名稱來指定 **StartName**，例如 *Username@DomainName* 。</span><span class="sxs-lookup"><span data-stu-id="12b2b-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-186">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-187">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="12b2b-188">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="12b2b-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="12b2b-189">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="12b2b-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="12b2b-190">將服務從本機系統變更為網路，或從網路變更為本機系統時， *StartPassword* 必須是空字串 ( "" ) 而非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="12b2b-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="12b2b-191">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-192">與其相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="12b2b-192">Group name that it is associated with.</span></span> <span data-ttu-id="12b2b-193">載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="12b2b-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="12b2b-194">如果指標為 **Null**，或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="12b2b-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="12b2b-195">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="12b2b-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="12b2b-196">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="12b2b-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="12b2b-197">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="12b2b-198">系統登錄中的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="12b2b-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="12b2b-199">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="12b2b-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-200">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-201">必須在此服務啟動之前啟動的載入順序群組清單。</span><span class="sxs-lookup"><span data-stu-id="12b2b-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="12b2b-202">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="12b2b-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="12b2b-203">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="12b2b-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="12b2b-204">組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (定義于 Winsvc .h 檔案) 字元中，以區別它們與服務名稱，因為服務和服務群組共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="12b2b-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="12b2b-205">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-206">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12b2b-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-207">包含必須在此服務啟動之前啟動之服務名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="12b2b-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="12b2b-208">陣列是雙重以 **Null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="12b2b-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="12b2b-209">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="12b2b-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="12b2b-210">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b2b-211">傳回值</span><span class="sxs-lookup"><span data-stu-id="12b2b-211">Return value</span></span>

<span data-ttu-id="12b2b-212">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="12b2b-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="12b2b-213">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="12b2b-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="12b2b-214">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="12b2b-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="12b2b-215">**0**</span><span class="sxs-lookup"><span data-stu-id="12b2b-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-216">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="12b2b-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-217">**1**</span><span class="sxs-lookup"><span data-stu-id="12b2b-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-218">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="12b2b-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-219">**2**</span><span class="sxs-lookup"><span data-stu-id="12b2b-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-220">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="12b2b-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-221">**3**</span><span class="sxs-lookup"><span data-stu-id="12b2b-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-222">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="12b2b-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-223">**4**</span><span class="sxs-lookup"><span data-stu-id="12b2b-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-224">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-225">**5**</span><span class="sxs-lookup"><span data-stu-id="12b2b-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-226">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="12b2b-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-227">**6**</span><span class="sxs-lookup"><span data-stu-id="12b2b-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-228">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-229">**7**</span><span class="sxs-lookup"><span data-stu-id="12b2b-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-230">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="12b2b-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-231">**8**</span><span class="sxs-lookup"><span data-stu-id="12b2b-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-232">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="12b2b-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-233">**9**</span><span class="sxs-lookup"><span data-stu-id="12b2b-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-234">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="12b2b-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-235">**10**</span><span class="sxs-lookup"><span data-stu-id="12b2b-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-236">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="12b2b-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-237">**11**</span><span class="sxs-lookup"><span data-stu-id="12b2b-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-238">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="12b2b-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-239">**12**</span><span class="sxs-lookup"><span data-stu-id="12b2b-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-240">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="12b2b-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-241">**13**</span><span class="sxs-lookup"><span data-stu-id="12b2b-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-242">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-243">**14**</span><span class="sxs-lookup"><span data-stu-id="12b2b-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-244">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-245">**15**</span><span class="sxs-lookup"><span data-stu-id="12b2b-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-246">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-247">**16**</span><span class="sxs-lookup"><span data-stu-id="12b2b-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-248">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="12b2b-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-249">**17**</span><span class="sxs-lookup"><span data-stu-id="12b2b-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-250">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="12b2b-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-251">**達**</span><span class="sxs-lookup"><span data-stu-id="12b2b-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-252">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="12b2b-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-253">**診斷**</span><span class="sxs-lookup"><span data-stu-id="12b2b-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-254">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-255">**20**</span><span class="sxs-lookup"><span data-stu-id="12b2b-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-256">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="12b2b-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-257">**21**</span><span class="sxs-lookup"><span data-stu-id="12b2b-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-258">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="12b2b-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-259">**22**</span><span class="sxs-lookup"><span data-stu-id="12b2b-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-260">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="12b2b-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-261">**23**</span><span class="sxs-lookup"><span data-stu-id="12b2b-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-262">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="12b2b-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="12b2b-263">**24**</span><span class="sxs-lookup"><span data-stu-id="12b2b-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="12b2b-264">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="12b2b-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12b2b-265">備註</span><span class="sxs-lookup"><span data-stu-id="12b2b-265">Remarks</span></span>

<span data-ttu-id="12b2b-266">當電腦啟動時，所有自動啟動的服務也會啟動。</span><span class="sxs-lookup"><span data-stu-id="12b2b-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="12b2b-267">有時候，其中一項服務可能無法與電腦一併啟動。</span><span class="sxs-lookup"><span data-stu-id="12b2b-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="12b2b-268">當服務在系統啟動期間失敗時，電腦會根據服務錯誤控制程式代碼的值採取動作。</span><span class="sxs-lookup"><span data-stu-id="12b2b-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="12b2b-269">大部分的服務都是使用一般的錯誤控制程式代碼安裝。</span><span class="sxs-lookup"><span data-stu-id="12b2b-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="12b2b-270">有些例外狀況（使用忽略錯誤碼來安裝）包括：</span><span class="sxs-lookup"><span data-stu-id="12b2b-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="12b2b-271">檔案複寫服務</span><span class="sxs-lookup"><span data-stu-id="12b2b-271">File Replication Service</span></span>
-   <span data-ttu-id="12b2b-272">智慧卡</span><span class="sxs-lookup"><span data-stu-id="12b2b-272">Smart Card</span></span>
-   <span data-ttu-id="12b2b-273">次要登入</span><span class="sxs-lookup"><span data-stu-id="12b2b-273">Secondary Logon</span></span>
-   <span data-ttu-id="12b2b-274">WMI</span><span class="sxs-lookup"><span data-stu-id="12b2b-274">WMI</span></span>

<span data-ttu-id="12b2b-275">若為使用忽略錯誤碼所安裝的服務，則不會向使用者提供服務失敗的通知。</span><span class="sxs-lookup"><span data-stu-id="12b2b-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="12b2b-276">如果您偏好無法啟動服務的螢幕通知，您可以使用 WMI 來變更錯誤控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="12b2b-277">錯誤控制代碼僅適用于電腦啟動;如果您在執行電腦之後停止然後嘗試重新開機服務，則不會使用錯誤控制代碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="12b2b-278">有時，您可能需要變更指定服務執行時所使用的帳戶。</span><span class="sxs-lookup"><span data-stu-id="12b2b-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="12b2b-279">例如，您可以在系統管理帳戶下執行服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="12b2b-280">因為這可能會產生安全性弱點，您可能會將服務切換為具有較少許可權的帳戶。</span><span class="sxs-lookup"><span data-stu-id="12b2b-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="12b2b-281">或者，您可能在即將刪除的帳戶下執行服務，或者您可能想要確保在所有伺服器上，某些服務會在特定帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="12b2b-282">您可以使用 [**Win32 \_ TerminalService**](win32-terminalservice.md)類別的 **Change** 方法，將服務設定為在指定的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="12b2b-283">選取帳戶時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="12b2b-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="12b2b-284">作為服務帳戶使用的帳戶必須具有以服務方式登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="12b2b-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="12b2b-285">您可以使用群組原則來授與此許可權。</span><span class="sxs-lookup"><span data-stu-id="12b2b-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="12b2b-286">作為服務帳戶使用的帳戶不應該是本機、網域或企業系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="12b2b-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="12b2b-287">服務的每個實例都應該在唯一的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="12b2b-288">這可提供額外的安全性，並可讓您進行個別服務實例的審核。</span><span class="sxs-lookup"><span data-stu-id="12b2b-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="12b2b-289">如果服務是互動式的，則服務必須在 LocalSystem 帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="12b2b-290">LocalSystem 是必要的，因為一次只有一個視窗工作站 (WinSta0) 可以是可見和互動式的。</span><span class="sxs-lookup"><span data-stu-id="12b2b-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="12b2b-291">如果服務是以 LocalSystem 以外的帳戶執行，則會在 0x03e7 $ \\ Default 視窗工作站中執行，這是不可見的視窗。</span><span class="sxs-lookup"><span data-stu-id="12b2b-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="12b2b-292">在此視窗工作站中執行的服務無法接收輸入或顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="12b2b-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="12b2b-293">當您將帳戶指派給服務時，SCM 需要該帳戶的正確密碼，才能進行指派。</span><span class="sxs-lookup"><span data-stu-id="12b2b-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="12b2b-294">如果您提供不正確的密碼，SCM 會拒絕該帳戶。</span><span class="sxs-lookup"><span data-stu-id="12b2b-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="12b2b-295">如果您使用 LocalSystem、LocalService 或 NetworkService 帳戶設定服務帳戶，則不需要提供帳戶密碼，因為這些帳戶沒有密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="12b2b-296">SCM 會將帳戶密碼儲存在服務資料庫中。</span><span class="sxs-lookup"><span data-stu-id="12b2b-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="12b2b-297">不過，在指派密碼之後，SCM 無法確保儲存在服務資料庫中的密碼和指派給使用者帳戶的密碼 Active Directory 繼續相符。</span><span class="sxs-lookup"><span data-stu-id="12b2b-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="12b2b-298">因此，可能會發生類似下列的情況：</span><span class="sxs-lookup"><span data-stu-id="12b2b-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="12b2b-299">.您可以設定在特定使用者帳戶下執行服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="12b2b-300">服務會使用目前的帳戶密碼在該帳戶下啟動。</span><span class="sxs-lookup"><span data-stu-id="12b2b-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="12b2b-301">您可以變更使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="12b2b-302">服務會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="12b2b-302">The service continues to run.</span></span> <span data-ttu-id="12b2b-303">但是，如果服務停止，您就無法將它重新開機，因為 SCM 會繼續使用舊的、不正確密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="12b2b-304">變更 Active Directory 中的密碼並不會變更儲存在服務資料庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="12b2b-305">如果您在一般使用者帳戶下執行服務，則每次使用者帳戶密碼變更時，都必須更新這些服務密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="12b2b-306">如果您不確定哪些服務是在該帳戶下執行，或是哪些電腦的服務是在該帳戶下執行，這可能特別耗時。</span><span class="sxs-lookup"><span data-stu-id="12b2b-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="12b2b-307">幸運的是，您可以使用 WMI 來檢查所有電腦上的服務帳戶，如有必要，也可以變更服務帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="12b2b-308">[**Win32 \_ LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup)參數代表定義執行相依性的一組系統服務。</span><span class="sxs-lookup"><span data-stu-id="12b2b-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="12b2b-309">服務必須依「載入順序」群組所指定的順序起始，因為服務會彼此相依。</span><span class="sxs-lookup"><span data-stu-id="12b2b-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="12b2b-310">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="12b2b-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="12b2b-311">若要將服務從網路服務變更為本機系統， *StartName* 和 *StartPassword* 參數應該具有下列值：</span><span class="sxs-lookup"><span data-stu-id="12b2b-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="12b2b-312">若要將服務從本機系統服務變更為網路， *StartName* 和 *StartPassword* 參數應該具有下列值：</span><span class="sxs-lookup"><span data-stu-id="12b2b-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="12b2b-313">範例</span><span class="sxs-lookup"><span data-stu-id="12b2b-313">Examples</span></span>

<span data-ttu-id="12b2b-314">下列 VBScript 會將服務的服務帳戶從指定的使用者帳戶，變更為 LocalSystem。</span><span class="sxs-lookup"><span data-stu-id="12b2b-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="12b2b-315">下列 VBScript 會變更在 Netsvc 下執行之所有腳本的服務帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="12b2b-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="12b2b-316">規格需求</span><span class="sxs-lookup"><span data-stu-id="12b2b-316">Requirements</span></span>



| <span data-ttu-id="12b2b-317">需求</span><span class="sxs-lookup"><span data-stu-id="12b2b-317">Requirement</span></span> | <span data-ttu-id="12b2b-318">值</span><span class="sxs-lookup"><span data-stu-id="12b2b-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12b2b-319">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12b2b-319">Minimum supported client</span></span><br/> | <span data-ttu-id="12b2b-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12b2b-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12b2b-321">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12b2b-321">Minimum supported server</span></span><br/> | <span data-ttu-id="12b2b-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12b2b-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12b2b-323">命名空間</span><span class="sxs-lookup"><span data-stu-id="12b2b-323">Namespace</span></span><br/>                | <span data-ttu-id="12b2b-324">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="12b2b-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="12b2b-325">標頭</span><span class="sxs-lookup"><span data-stu-id="12b2b-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="12b2b-326"><dt>Mbnapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="12b2b-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="12b2b-327">MOF</span><span class="sxs-lookup"><span data-stu-id="12b2b-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12b2b-328"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="12b2b-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="12b2b-329">DLL</span><span class="sxs-lookup"><span data-stu-id="12b2b-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12b2b-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12b2b-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12b2b-331">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12b2b-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b2b-332">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="12b2b-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="12b2b-333">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="12b2b-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="12b2b-334">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="12b2b-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="12b2b-335">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="12b2b-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

