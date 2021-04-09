---
description: 建立由系統驅動程式管理的新服務。
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111648"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="2200b-103">Win32 >systemdriver 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2200b-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="2200b-104">**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立由系統驅動程式管理的新服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="2200b-105">*Win32 \_ LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。</span><span class="sxs-lookup"><span data-stu-id="2200b-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="2200b-106">服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。</span><span class="sxs-lookup"><span data-stu-id="2200b-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="2200b-107">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="2200b-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="2200b-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2200b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2200b-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2200b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2200b-110">語法</span><span class="sxs-lookup"><span data-stu-id="2200b-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="2200b-111">參數</span><span class="sxs-lookup"><span data-stu-id="2200b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2200b-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-113">要安裝至 **Create** 方法的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="2200b-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="2200b-114">字串長度上限為256個字元。</span><span class="sxs-lookup"><span data-stu-id="2200b-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="2200b-115">服務控制管理員資料庫會保留字元的大小寫，但服務名稱比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2200b-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="2200b-116">正斜線 (/) 和雙反斜線 (\\) 是不正確服務名稱字元。</span><span class="sxs-lookup"><span data-stu-id="2200b-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-117">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-118">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2200b-118">Display name of the service.</span></span> <span data-ttu-id="2200b-119">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="2200b-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="2200b-120">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="2200b-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="2200b-121">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2200b-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="2200b-122">條件約束：接受與 *Name* 參數相同的值。</span><span class="sxs-lookup"><span data-stu-id="2200b-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="2200b-123">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="2200b-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="2200b-124">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-125">可執行檔的完整路徑，該檔案可執行服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="2200b-126">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="2200b-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="2200b-127">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-128">提供給呼叫它們之進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="2200b-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="2200b-129">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="2200b-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-130">核心驅動程式</span><span class="sxs-lookup"><span data-stu-id="2200b-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="2200b-131">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="2200b-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-132">檔案系統驅動程式</span><span class="sxs-lookup"><span data-stu-id="2200b-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="2200b-133">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="2200b-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-134">配接器</span><span class="sxs-lookup"><span data-stu-id="2200b-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="2200b-135">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="2200b-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-136">辨識器驅動程式</span><span class="sxs-lookup"><span data-stu-id="2200b-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="2200b-137">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="2200b-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-138">自有進程</span><span class="sxs-lookup"><span data-stu-id="2200b-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="2200b-139">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="2200b-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-140">共用進程</span><span class="sxs-lookup"><span data-stu-id="2200b-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="2200b-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="2200b-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="2200b-142">互動式進程</span><span class="sxs-lookup"><span data-stu-id="2200b-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2200b-143">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-144">**建立** 方法無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="2200b-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="2200b-145">此值表示如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="2200b-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="2200b-146">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="2200b-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="2200b-147">0</span><span class="sxs-lookup"><span data-stu-id="2200b-147">0</span></span>
</dt> <dd>

<span data-ttu-id="2200b-148">拒絕</span><span class="sxs-lookup"><span data-stu-id="2200b-148">"Ignore"</span></span>

<span data-ttu-id="2200b-149">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="2200b-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-150">1</span><span class="sxs-lookup"><span data-stu-id="2200b-150">1</span></span>
</dt> <dd>

<span data-ttu-id="2200b-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="2200b-151">"Normal"</span></span>

<span data-ttu-id="2200b-152">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="2200b-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-153">2</span><span class="sxs-lookup"><span data-stu-id="2200b-153">2</span></span>
</dt> <dd>

<span data-ttu-id="2200b-154">嚴格</span><span class="sxs-lookup"><span data-stu-id="2200b-154">"Severe"</span></span>

<span data-ttu-id="2200b-155">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="2200b-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-156">3</span><span class="sxs-lookup"><span data-stu-id="2200b-156">3</span></span>
</dt> <dd>

<span data-ttu-id="2200b-157">必需</span><span class="sxs-lookup"><span data-stu-id="2200b-157">"Critical"</span></span>

<span data-ttu-id="2200b-158">系統嘗試以良好的設定開始。</span><span class="sxs-lookup"><span data-stu-id="2200b-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2200b-159">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-160">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="2200b-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="2200b-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**引導**</span><span class="sxs-lookup"><span data-stu-id="2200b-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="2200b-162">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2200b-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="2200b-163">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="2200b-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**系統**</span><span class="sxs-lookup"><span data-stu-id="2200b-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="2200b-165">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2200b-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="2200b-166">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="2200b-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動**</span><span class="sxs-lookup"><span data-stu-id="2200b-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="2200b-168">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="2200b-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動**</span><span class="sxs-lookup"><span data-stu-id="2200b-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="2200b-170">當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2200b-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**</span><span class="sxs-lookup"><span data-stu-id="2200b-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="2200b-172">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2200b-173">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-174">若 **為 true**，則服務可以建立或與桌面上的視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2200b-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-175">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-176">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2200b-176">Account name under which the service runs.</span></span> <span data-ttu-id="2200b-177">根據服務類型而定，帳戶名稱的格式可以是 DomainName \\ 使用者名稱或使用者主體名稱 (UPN) 格式 (Username@DomainName) 。</span><span class="sxs-lookup"><span data-stu-id="2200b-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="2200b-178">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="2200b-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="2200b-179">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2200b-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="2200b-180">如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="2200b-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="2200b-181">若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2200b-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="2200b-182">如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。</span><span class="sxs-lookup"><span data-stu-id="2200b-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="2200b-183">範例： DWDOM \\ 管理員</span><span class="sxs-lookup"><span data-stu-id="2200b-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="2200b-184">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-185">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="2200b-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="2200b-186">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2200b-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="2200b-187">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="2200b-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-188">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-189">與新服務相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="2200b-189">Group name associated with the new service.</span></span> <span data-ttu-id="2200b-190">載入順序群組包含于登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="2200b-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="2200b-191">如果指標為 **Null** 或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="2200b-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="2200b-192">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="2200b-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="2200b-193">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="2200b-194">登錄的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="2200b-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="2200b-195">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="2200b-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="2200b-196">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-197">必須在此服務之前啟動的載入順序群組陣列。</span><span class="sxs-lookup"><span data-stu-id="2200b-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="2200b-198">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="2200b-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="2200b-199">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="2200b-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="2200b-200">如果指標為 **Null** 或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="2200b-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="2200b-201">組名必須以 Winsvc 中定義的 **SC \_ 群組 \_ 識別碼** 作為前置詞， (在 .h 檔案中定義) 字元，以與服務名稱區別，因為服務和服務群組會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="2200b-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="2200b-202">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="2200b-203">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2200b-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2200b-204">陣列，包含在此服務啟動之前必須啟動之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2200b-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="2200b-205">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="2200b-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="2200b-206">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="2200b-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="2200b-207">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="2200b-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="2200b-208">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="2200b-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2200b-209">傳回值</span><span class="sxs-lookup"><span data-stu-id="2200b-209">Return value</span></span>

<span data-ttu-id="2200b-210">如果成功建立服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="2200b-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2200b-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="2200b-211">Requirements</span></span>



| <span data-ttu-id="2200b-212">需求</span><span class="sxs-lookup"><span data-stu-id="2200b-212">Requirement</span></span> | <span data-ttu-id="2200b-213">值</span><span class="sxs-lookup"><span data-stu-id="2200b-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2200b-214">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2200b-214">Minimum supported client</span></span><br/> | <span data-ttu-id="2200b-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2200b-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2200b-216">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2200b-216">Minimum supported server</span></span><br/> | <span data-ttu-id="2200b-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2200b-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2200b-218">命名空間</span><span class="sxs-lookup"><span data-stu-id="2200b-218">Namespace</span></span><br/>                | <span data-ttu-id="2200b-219">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2200b-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2200b-220">MOF</span><span class="sxs-lookup"><span data-stu-id="2200b-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2200b-221"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2200b-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2200b-222">DLL</span><span class="sxs-lookup"><span data-stu-id="2200b-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2200b-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2200b-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2200b-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2200b-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="2200b-225">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2200b-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2200b-226">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="2200b-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

