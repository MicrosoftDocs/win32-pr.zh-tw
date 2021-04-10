---
description: 建立新的系統服務。
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: 'Win32_Service 類別的建立方法 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689196"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="cadc9-103">Win32_Service 類別的建立方法 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="cadc9-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cadc9-104">**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的系統服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="cadc9-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="cadc9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cadc9-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="cadc9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cadc9-107">語法</span><span class="sxs-lookup"><span data-stu-id="cadc9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="cadc9-108">參數</span><span class="sxs-lookup"><span data-stu-id="cadc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadc9-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-110">要安裝至 **Create** 方法的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="cadc9-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="cadc9-111">字串長度上限為256個字元。</span><span class="sxs-lookup"><span data-stu-id="cadc9-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="cadc9-112">服務控制管理員資料庫會保留字元的大小寫，但服務名稱比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cadc9-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="cadc9-113">正斜線 (/) 和雙反斜線 (\\) 是不正確服務名稱字元。</span><span class="sxs-lookup"><span data-stu-id="cadc9-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-114">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-115">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cadc9-115">Display name of the service.</span></span> <span data-ttu-id="cadc9-116">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="cadc9-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="cadc9-117">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="cadc9-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="cadc9-118">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cadc9-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="cadc9-119">條件約束：接受與 *Name* 參數相同的值。</span><span class="sxs-lookup"><span data-stu-id="cadc9-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="cadc9-120">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="cadc9-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-121">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-122">可執行檔的完整路徑，該檔案可執行服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="cadc9-123">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="cadc9-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-124">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-125">提供給呼叫它們的進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="cadc9-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="cadc9-126">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="cadc9-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-127">核心驅動程式</span><span class="sxs-lookup"><span data-stu-id="cadc9-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-128">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="cadc9-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-129">檔案系統驅動程式</span><span class="sxs-lookup"><span data-stu-id="cadc9-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-130">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="cadc9-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-131">配接器</span><span class="sxs-lookup"><span data-stu-id="cadc9-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-132">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="cadc9-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-133">辨識器驅動程式</span><span class="sxs-lookup"><span data-stu-id="cadc9-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-134">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="cadc9-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-135">自有進程</span><span class="sxs-lookup"><span data-stu-id="cadc9-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-136">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="cadc9-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-137">共用進程</span><span class="sxs-lookup"><span data-stu-id="cadc9-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="cadc9-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-139">互動式進程</span><span class="sxs-lookup"><span data-stu-id="cadc9-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cadc9-140">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-141">**建立** 方法無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="cadc9-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="cadc9-142">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="cadc9-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="cadc9-143">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="cadc9-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="cadc9-144">0</span><span class="sxs-lookup"><span data-stu-id="cadc9-144">0</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-145">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="cadc9-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-146">1</span><span class="sxs-lookup"><span data-stu-id="cadc9-146">1</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-147">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="cadc9-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-148">2</span><span class="sxs-lookup"><span data-stu-id="cadc9-148">2</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-149">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="cadc9-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-150">3</span><span class="sxs-lookup"><span data-stu-id="cadc9-150">3</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-151">系統嘗試以良好的設定開始。</span><span class="sxs-lookup"><span data-stu-id="cadc9-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cadc9-152">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-153">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="cadc9-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="cadc9-154">Boot</span><span class="sxs-lookup"><span data-stu-id="cadc9-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-155">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="cadc9-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="cadc9-156">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-157">系統</span><span class="sxs-lookup"><span data-stu-id="cadc9-157">System</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-158">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="cadc9-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="cadc9-159">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-160">自動</span><span class="sxs-lookup"><span data-stu-id="cadc9-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-161">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-162">手動</span><span class="sxs-lookup"><span data-stu-id="cadc9-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-163">當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="cadc9-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-165">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cadc9-166">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-167">若 **為 true**，則服務可以在桌面上建立 windows 或與其通訊。</span><span class="sxs-lookup"><span data-stu-id="cadc9-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-168">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-169">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cadc9-169">Account name under which the service runs.</span></span> <span data-ttu-id="cadc9-170">根據服務類型而定，帳戶名稱的格式可以是 DomainName \\ 使用者名稱或使用者主體名稱 (UPN) 格式 (Username@DomainName) 。</span><span class="sxs-lookup"><span data-stu-id="cadc9-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="cadc9-171">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="cadc9-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="cadc9-172">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="cadc9-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="cadc9-173">如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="cadc9-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="cadc9-174">若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) ，) 系統用來載入設備磁碟機的輸入和輸出 (i/o。</span><span class="sxs-lookup"><span data-stu-id="cadc9-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="cadc9-175">如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。</span><span class="sxs-lookup"><span data-stu-id="cadc9-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="cadc9-176">範例： DWDOM \\ Admin。</span><span class="sxs-lookup"><span data-stu-id="cadc9-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-177">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-178">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="cadc9-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="cadc9-179">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="cadc9-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="cadc9-180">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="cadc9-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-181">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-182">與新服務相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="cadc9-182">Group name associated with the new service.</span></span> <span data-ttu-id="cadc9-183">載入順序群組包含于登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="cadc9-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="cadc9-184">如果指標為 **Null** 或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="cadc9-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="cadc9-185">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="cadc9-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="cadc9-186">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="cadc9-187">登錄的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="cadc9-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="cadc9-188">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="cadc9-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-189">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-190">必須在此服務之前啟動的載入順序群組陣列。</span><span class="sxs-lookup"><span data-stu-id="cadc9-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="cadc9-191">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="cadc9-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="cadc9-192">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="cadc9-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="cadc9-193">如果指標為 **Null** 或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="cadc9-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="cadc9-194">組名必須以 Winsvc 中定義的 **SC \_ 群組 \_ 識別碼** 作為前置詞， (在 .h 檔案中定義) 字元，以與服務名稱區別，因為服務和服務群組會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="cadc9-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="cadc9-195">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-196">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cadc9-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-197">陣列，包含在此服務啟動之前必須啟動之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="cadc9-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="cadc9-198">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="cadc9-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="cadc9-199">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="cadc9-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="cadc9-200">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="cadc9-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="cadc9-201">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cadc9-202">傳回值</span><span class="sxs-lookup"><span data-stu-id="cadc9-202">Return value</span></span>

<span data-ttu-id="cadc9-203">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="cadc9-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="cadc9-204">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="cadc9-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cadc9-205">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="cadc9-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cadc9-206">**0**</span><span class="sxs-lookup"><span data-stu-id="cadc9-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-207">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="cadc9-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-208">**1**</span><span class="sxs-lookup"><span data-stu-id="cadc9-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-209">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="cadc9-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-210">**2**</span><span class="sxs-lookup"><span data-stu-id="cadc9-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-211">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="cadc9-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-212">**3**</span><span class="sxs-lookup"><span data-stu-id="cadc9-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-213">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="cadc9-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-214">**4**</span><span class="sxs-lookup"><span data-stu-id="cadc9-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-215">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="cadc9-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-216">**5**</span><span class="sxs-lookup"><span data-stu-id="cadc9-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-217">因為 [**Win32 \_ BaseService**](win32-baseservice.md)) 類別的服務 (**state** 屬性的狀態等於0、1或2，所以無法將要求的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-218">**6**</span><span class="sxs-lookup"><span data-stu-id="cadc9-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-219">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-220">**7**</span><span class="sxs-lookup"><span data-stu-id="cadc9-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-221">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="cadc9-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-222">**8**</span><span class="sxs-lookup"><span data-stu-id="cadc9-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-223">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cadc9-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-224">**9**</span><span class="sxs-lookup"><span data-stu-id="cadc9-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-225">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="cadc9-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-226">**10**</span><span class="sxs-lookup"><span data-stu-id="cadc9-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-227">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="cadc9-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-228">**11**</span><span class="sxs-lookup"><span data-stu-id="cadc9-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-229">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="cadc9-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-230">**12**</span><span class="sxs-lookup"><span data-stu-id="cadc9-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-231">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="cadc9-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-232">**13**</span><span class="sxs-lookup"><span data-stu-id="cadc9-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-233">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-234">**14**</span><span class="sxs-lookup"><span data-stu-id="cadc9-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-235">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-236">**15**</span><span class="sxs-lookup"><span data-stu-id="cadc9-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-237">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="cadc9-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-238">**16**</span><span class="sxs-lookup"><span data-stu-id="cadc9-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-239">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="cadc9-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-240">**17**</span><span class="sxs-lookup"><span data-stu-id="cadc9-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-241">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="cadc9-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-242">**達**</span><span class="sxs-lookup"><span data-stu-id="cadc9-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-243">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="cadc9-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-244">**診斷**</span><span class="sxs-lookup"><span data-stu-id="cadc9-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-245">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="cadc9-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-246">**20**</span><span class="sxs-lookup"><span data-stu-id="cadc9-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-247">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="cadc9-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-248">**21**</span><span class="sxs-lookup"><span data-stu-id="cadc9-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-249">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="cadc9-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-250">**22**</span><span class="sxs-lookup"><span data-stu-id="cadc9-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-251">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="cadc9-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-252">**23**</span><span class="sxs-lookup"><span data-stu-id="cadc9-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-253">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="cadc9-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cadc9-254">**24**</span><span class="sxs-lookup"><span data-stu-id="cadc9-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="cadc9-255">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="cadc9-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cadc9-256">備註</span><span class="sxs-lookup"><span data-stu-id="cadc9-256">Remarks</span></span>

<span data-ttu-id="cadc9-257">服務通常會以下列兩種方式之一進行安裝：作為作業系統安裝的一部分，或使用服務開發人員所提供的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="cadc9-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="cadc9-258">不過，某些服務（特別是在內部建立的服務）可能沒有安裝程式。</span><span class="sxs-lookup"><span data-stu-id="cadc9-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="cadc9-259">在這些情況下，您可以使用 **Create** 方法以程式設計方式安裝服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="cadc9-260">無論名稱為何，Create 方法都不會實際建立服務;它只會安裝現有的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="cadc9-261">若要使用此命令，您必須將服務可執行檔案複製到電腦，然後使用 [ **建立** ] 來安裝服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="cadc9-262">**Create** 方法類似于 [**變更**](change-method-in-class-win32-service.md)方法。</span><span class="sxs-lookup"><span data-stu-id="cadc9-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="cadc9-263">在這兩種情況下，服務的屬性都會作為參數傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="cadc9-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="cadc9-264">如同與 **變更** 方法搭配使用的參數，傳遞這些參數的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="cadc9-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="cadc9-265">*LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。</span><span class="sxs-lookup"><span data-stu-id="cadc9-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="cadc9-266">服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。</span><span class="sxs-lookup"><span data-stu-id="cadc9-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="cadc9-267">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="cadc9-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="cadc9-268">範例</span><span class="sxs-lookup"><span data-stu-id="cadc9-268">Examples</span></span>

<span data-ttu-id="cadc9-269">下列 VBScript 會安裝名為 DbService 的服務。</span><span class="sxs-lookup"><span data-stu-id="cadc9-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="cadc9-270">規格需求</span><span class="sxs-lookup"><span data-stu-id="cadc9-270">Requirements</span></span>



| <span data-ttu-id="cadc9-271">需求</span><span class="sxs-lookup"><span data-stu-id="cadc9-271">Requirement</span></span> | <span data-ttu-id="cadc9-272">值</span><span class="sxs-lookup"><span data-stu-id="cadc9-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cadc9-273">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cadc9-273">Minimum supported client</span></span><br/> | <span data-ttu-id="cadc9-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cadc9-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cadc9-275">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cadc9-275">Minimum supported server</span></span><br/> | <span data-ttu-id="cadc9-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cadc9-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cadc9-277">命名空間</span><span class="sxs-lookup"><span data-stu-id="cadc9-277">Namespace</span></span><br/>                | <span data-ttu-id="cadc9-278">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cadc9-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cadc9-279">MOF</span><span class="sxs-lookup"><span data-stu-id="cadc9-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cadc9-280"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cadc9-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cadc9-281">DLL</span><span class="sxs-lookup"><span data-stu-id="cadc9-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cadc9-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cadc9-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadc9-283">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cadc9-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="cadc9-284">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cadc9-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cadc9-285">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="cadc9-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="cadc9-286">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="cadc9-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

