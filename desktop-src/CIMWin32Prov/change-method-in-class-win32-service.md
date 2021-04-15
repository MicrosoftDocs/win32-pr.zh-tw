---
description: 修改 Win32 \_ 服務。
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: 'Win32_Service 類別的 Change 方法 (Mbnapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510642"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="23ef8-103">Win32_Service 類別的 Change 方法 (Mbnapi) </span><span class="sxs-lookup"><span data-stu-id="23ef8-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="23ef8-104">**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ 服務**](win32-service.md)。</span><span class="sxs-lookup"><span data-stu-id="23ef8-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="23ef8-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="23ef8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="23ef8-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="23ef8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="23ef8-107">語法</span><span class="sxs-lookup"><span data-stu-id="23ef8-107">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="23ef8-108">參數</span><span class="sxs-lookup"><span data-stu-id="23ef8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ef8-109">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-110">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="23ef8-110">The display name of the service.</span></span> <span data-ttu-id="23ef8-111">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="23ef8-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="23ef8-112">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="23ef8-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="23ef8-113">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="23ef8-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="23ef8-114">條件約束：接受與 **Name** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="23ef8-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="23ef8-115">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="23ef8-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-116">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-117">執行服務之可執行檔的完整路徑，例如「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="23ef8-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-118">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-119">提供給呼叫它們之進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="23ef8-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="23ef8-120">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="23ef8-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-121">核心驅動程式</span><span class="sxs-lookup"><span data-stu-id="23ef8-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-122">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="23ef8-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-123">檔案系統驅動程式</span><span class="sxs-lookup"><span data-stu-id="23ef8-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-124">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="23ef8-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-125">配接器</span><span class="sxs-lookup"><span data-stu-id="23ef8-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-126">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="23ef8-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-127">辨識器驅動程式</span><span class="sxs-lookup"><span data-stu-id="23ef8-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-128">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="23ef8-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-129">自有進程</span><span class="sxs-lookup"><span data-stu-id="23ef8-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-130">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="23ef8-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-131">共用進程</span><span class="sxs-lookup"><span data-stu-id="23ef8-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="23ef8-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-133">互動式進程</span><span class="sxs-lookup"><span data-stu-id="23ef8-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="23ef8-134">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-135">當此服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="23ef8-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="23ef8-136">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="23ef8-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="23ef8-137">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="23ef8-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="23ef8-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) </span><span class="sxs-lookup"><span data-stu-id="23ef8-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="23ef8-139">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="23ef8-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="23ef8-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="23ef8-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23ef8-141">一般。</span><span class="sxs-lookup"><span data-stu-id="23ef8-141">Normal.</span></span> <span data-ttu-id="23ef8-142">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="23ef8-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="23ef8-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) </span><span class="sxs-lookup"><span data-stu-id="23ef8-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23ef8-144">系統會重新開機，並使用上一個良好的設定。</span><span class="sxs-lookup"><span data-stu-id="23ef8-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="23ef8-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="23ef8-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23ef8-146">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="23ef8-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="23ef8-147">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-148">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="23ef8-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="23ef8-149">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="23ef8-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="23ef8-150">Boot</span><span class="sxs-lookup"><span data-stu-id="23ef8-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-151">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="23ef8-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="23ef8-152">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-153">系統</span><span class="sxs-lookup"><span data-stu-id="23ef8-153">System</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-154">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="23ef8-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="23ef8-155">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-156">自動</span><span class="sxs-lookup"><span data-stu-id="23ef8-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-157">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-158">手動</span><span class="sxs-lookup"><span data-stu-id="23ef8-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-159">當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-160">Disabled</span><span class="sxs-lookup"><span data-stu-id="23ef8-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-161">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="23ef8-162">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-163">若 **為 True**，則服務可以建立或與桌面上的視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="23ef8-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-164">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-165">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="23ef8-165">Account name the service runs under.</span></span> <span data-ttu-id="23ef8-166">根據服務類型而定，帳戶名稱可能採用 DomainName 使用者名稱或的形式 \\ 。 \\使用者。</span><span class="sxs-lookup"><span data-stu-id="23ef8-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="23ef8-167">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="23ef8-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="23ef8-168">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="23ef8-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="23ef8-169">如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="23ef8-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="23ef8-170">若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="23ef8-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="23ef8-171">如果指定了 **Null** ，驅動程式就會根據服務名稱（例如 "DWDOM Admin"），以 i/o 系統建立的預設物件名稱執行 \\ 。</span><span class="sxs-lookup"><span data-stu-id="23ef8-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="23ef8-172">您也可以使用 (UPN) 格式的使用者主體名稱來指定 **StartName**，例如 *Username@DomainName* 。</span><span class="sxs-lookup"><span data-stu-id="23ef8-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-173">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-174">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="23ef8-175">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="23ef8-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="23ef8-176">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="23ef8-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="23ef8-177">將服務從本機系統變更為網路，或從網路變更為本機系統時， *StartPassword* 必須是空字串 ( "" ) 而非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="23ef8-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="23ef8-178">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-179">與其相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="23ef8-179">Group name that it is associated with.</span></span> <span data-ttu-id="23ef8-180">載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="23ef8-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="23ef8-181">如果指標為 **Null**，或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="23ef8-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="23ef8-182">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="23ef8-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="23ef8-183">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="23ef8-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="23ef8-184">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="23ef8-185">系統登錄中的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="23ef8-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="23ef8-186">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="23ef8-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-187">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-188">必須在此服務啟動之前啟動的載入順序群組清單。</span><span class="sxs-lookup"><span data-stu-id="23ef8-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="23ef8-189">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="23ef8-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="23ef8-190">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="23ef8-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="23ef8-191">組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (定義于 Winsvc .h 檔案) 字元中，以區別它們與服務名稱，因為服務和服務群組共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="23ef8-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="23ef8-192">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-193">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23ef8-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-194">包含必須在此服務啟動之前啟動之服務名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="23ef8-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="23ef8-195">陣列是雙重以 **Null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="23ef8-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="23ef8-196">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="23ef8-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="23ef8-197">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ef8-198">傳回值</span><span class="sxs-lookup"><span data-stu-id="23ef8-198">Return value</span></span>

<span data-ttu-id="23ef8-199">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="23ef8-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="23ef8-200">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="23ef8-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="23ef8-201">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="23ef8-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="23ef8-202">「成功」</span><span class="sxs-lookup"><span data-stu-id="23ef8-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-203">0</span><span class="sxs-lookup"><span data-stu-id="23ef8-203">0</span></span>

<span data-ttu-id="23ef8-204">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="23ef8-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-205">**不支援**</span><span class="sxs-lookup"><span data-stu-id="23ef8-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-206">1</span><span class="sxs-lookup"><span data-stu-id="23ef8-206">1</span></span>

<span data-ttu-id="23ef8-207">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="23ef8-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-208">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="23ef8-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-209">2</span><span class="sxs-lookup"><span data-stu-id="23ef8-209">2</span></span>

<span data-ttu-id="23ef8-210">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="23ef8-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-211">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="23ef8-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-212">3</span><span class="sxs-lookup"><span data-stu-id="23ef8-212">3</span></span>

<span data-ttu-id="23ef8-213">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="23ef8-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-214">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="23ef8-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-215">4</span><span class="sxs-lookup"><span data-stu-id="23ef8-215">4</span></span>

<span data-ttu-id="23ef8-216">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-217">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="23ef8-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-218">5</span><span class="sxs-lookup"><span data-stu-id="23ef8-218">5</span></span>

<span data-ttu-id="23ef8-219">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="23ef8-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-220">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="23ef8-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-221">6</span><span class="sxs-lookup"><span data-stu-id="23ef8-221">6</span></span>

<span data-ttu-id="23ef8-222">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-223">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="23ef8-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-224">7</span><span class="sxs-lookup"><span data-stu-id="23ef8-224">7</span></span>

<span data-ttu-id="23ef8-225">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="23ef8-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-226">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="23ef8-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-227">8</span><span class="sxs-lookup"><span data-stu-id="23ef8-227">8</span></span>

<span data-ttu-id="23ef8-228">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="23ef8-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-229">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="23ef8-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-230">9</span><span class="sxs-lookup"><span data-stu-id="23ef8-230">9</span></span>

<span data-ttu-id="23ef8-231">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="23ef8-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-232">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="23ef8-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-233">10</span><span class="sxs-lookup"><span data-stu-id="23ef8-233">10</span></span>

<span data-ttu-id="23ef8-234">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="23ef8-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-235">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="23ef8-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-236">11</span><span class="sxs-lookup"><span data-stu-id="23ef8-236">11</span></span>

<span data-ttu-id="23ef8-237">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="23ef8-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-238">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="23ef8-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-239">12</span><span class="sxs-lookup"><span data-stu-id="23ef8-239">12</span></span>

<span data-ttu-id="23ef8-240">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="23ef8-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-241">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="23ef8-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-242">13</span><span class="sxs-lookup"><span data-stu-id="23ef8-242">13</span></span>

<span data-ttu-id="23ef8-243">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-244">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="23ef8-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-245">14</span><span class="sxs-lookup"><span data-stu-id="23ef8-245">14</span></span>

<span data-ttu-id="23ef8-246">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-247">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="23ef8-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-248">15</span><span class="sxs-lookup"><span data-stu-id="23ef8-248">15</span></span>

<span data-ttu-id="23ef8-249">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-250">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="23ef8-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-251">16</span><span class="sxs-lookup"><span data-stu-id="23ef8-251">16</span></span>

<span data-ttu-id="23ef8-252">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="23ef8-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-253">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="23ef8-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-254">17</span><span class="sxs-lookup"><span data-stu-id="23ef8-254">17</span></span>

<span data-ttu-id="23ef8-255">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="23ef8-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-256">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="23ef8-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-257">18</span><span class="sxs-lookup"><span data-stu-id="23ef8-257">18</span></span>

<span data-ttu-id="23ef8-258">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="23ef8-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-259">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="23ef8-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-260">19</span><span class="sxs-lookup"><span data-stu-id="23ef8-260">19</span></span>

<span data-ttu-id="23ef8-261">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-262">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="23ef8-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-263">20</span><span class="sxs-lookup"><span data-stu-id="23ef8-263">20</span></span>

<span data-ttu-id="23ef8-264">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="23ef8-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-265">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="23ef8-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-266">21</span><span class="sxs-lookup"><span data-stu-id="23ef8-266">21</span></span>

<span data-ttu-id="23ef8-267">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="23ef8-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-268">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="23ef8-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-269">22</span><span class="sxs-lookup"><span data-stu-id="23ef8-269">22</span></span>

<span data-ttu-id="23ef8-270">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="23ef8-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-271">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="23ef8-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-272">23</span><span class="sxs-lookup"><span data-stu-id="23ef8-272">23</span></span>

<span data-ttu-id="23ef8-273">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="23ef8-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-274">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="23ef8-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-275">24</span><span class="sxs-lookup"><span data-stu-id="23ef8-275">24</span></span>

<span data-ttu-id="23ef8-276">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="23ef8-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="23ef8-277">**其他**</span><span class="sxs-lookup"><span data-stu-id="23ef8-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="23ef8-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="23ef8-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23ef8-279">備註</span><span class="sxs-lookup"><span data-stu-id="23ef8-279">Remarks</span></span>

<span data-ttu-id="23ef8-280">當電腦啟動時，所有自動啟動的服務也會啟動。</span><span class="sxs-lookup"><span data-stu-id="23ef8-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="23ef8-281">有時候，其中一項服務可能無法與電腦一併啟動。</span><span class="sxs-lookup"><span data-stu-id="23ef8-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="23ef8-282">當服務在系統啟動期間失敗時，電腦會根據服務錯誤控制程式代碼的值採取動作。</span><span class="sxs-lookup"><span data-stu-id="23ef8-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="23ef8-283">大部分的服務都是使用一般的錯誤控制程式代碼安裝。</span><span class="sxs-lookup"><span data-stu-id="23ef8-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="23ef8-284">有些例外狀況（使用忽略錯誤碼來安裝）包括：</span><span class="sxs-lookup"><span data-stu-id="23ef8-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="23ef8-285">檔案複寫服務</span><span class="sxs-lookup"><span data-stu-id="23ef8-285">File Replication Service</span></span>
-   <span data-ttu-id="23ef8-286">智慧卡</span><span class="sxs-lookup"><span data-stu-id="23ef8-286">Smart Card</span></span>
-   <span data-ttu-id="23ef8-287">次要登入</span><span class="sxs-lookup"><span data-stu-id="23ef8-287">Secondary Logon</span></span>
-   <span data-ttu-id="23ef8-288">WMI</span><span class="sxs-lookup"><span data-stu-id="23ef8-288">WMI</span></span>

<span data-ttu-id="23ef8-289">若為使用忽略錯誤碼所安裝的服務，則不會向使用者提供服務失敗的通知。</span><span class="sxs-lookup"><span data-stu-id="23ef8-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="23ef8-290">如果您偏好無法啟動服務的螢幕通知，您可以使用 WMI 來變更錯誤控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="23ef8-291">錯誤控制代碼僅適用于電腦啟動;如果您在執行電腦之後停止然後嘗試重新開機服務，則不會使用錯誤控制代碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="23ef8-292">有時，您可能需要變更指定服務執行時所使用的帳戶。</span><span class="sxs-lookup"><span data-stu-id="23ef8-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="23ef8-293">例如，您可以在系統管理帳戶下執行服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="23ef8-294">因為這可能會產生安全性弱點，您可能會將服務切換為具有較少許可權的帳戶。</span><span class="sxs-lookup"><span data-stu-id="23ef8-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="23ef8-295">或者，您可能在即將刪除的帳戶下執行服務，或者您可能想要確保在所有伺服器上，某些服務會在特定帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="23ef8-296">您可以使用 [**Win32 \_ 服務**](win32-service.md)類別的 **Change** 方法，將服務設定為在指定的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="23ef8-297">選取帳戶時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="23ef8-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="23ef8-298">作為服務帳戶使用的帳戶必須具有以服務方式登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="23ef8-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="23ef8-299">您可以使用群組原則來授與此許可權。</span><span class="sxs-lookup"><span data-stu-id="23ef8-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="23ef8-300">作為服務帳戶使用的帳戶不應該是本機、網域或企業系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="23ef8-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="23ef8-301">服務的每個實例都應該在唯一的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="23ef8-302">這可提供額外的安全性，並可讓您進行個別服務實例的審核。</span><span class="sxs-lookup"><span data-stu-id="23ef8-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="23ef8-303">如果服務是互動式的，則服務必須在 LocalSystem 帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="23ef8-304">LocalSystem 是必要的，因為一次只有一個視窗工作站 (WinSta0) 可以是可見和互動式的。</span><span class="sxs-lookup"><span data-stu-id="23ef8-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="23ef8-305">如果服務是以 LocalSystem 以外的帳戶執行，則會在 0x03e7 $ \\ Default 視窗工作站中執行，這是不可見的視窗。</span><span class="sxs-lookup"><span data-stu-id="23ef8-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="23ef8-306">在此視窗工作站中執行的服務無法接收輸入或顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="23ef8-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="23ef8-307">當您將帳戶指派給服務時，SCM 需要該帳戶的正確密碼，才能進行指派。</span><span class="sxs-lookup"><span data-stu-id="23ef8-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="23ef8-308">如果您提供不正確的密碼，SCM 會拒絕該帳戶。</span><span class="sxs-lookup"><span data-stu-id="23ef8-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="23ef8-309">如果您使用 LocalSystem、LocalService 或 NetworkService 帳戶設定服務帳戶，則不需要提供帳戶密碼，因為這些帳戶沒有密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="23ef8-310">SCM 會將帳戶密碼儲存在服務資料庫中。</span><span class="sxs-lookup"><span data-stu-id="23ef8-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="23ef8-311">不過，在指派密碼之後，SCM 無法確保儲存在服務資料庫中的密碼和指派給使用者帳戶的密碼 Active Directory 繼續相符。</span><span class="sxs-lookup"><span data-stu-id="23ef8-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="23ef8-312">因此，可能會發生類似下列的情況：</span><span class="sxs-lookup"><span data-stu-id="23ef8-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="23ef8-313">您可以設定在特定使用者帳戶下執行服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="23ef8-314">服務會使用目前的帳戶密碼在該帳戶下啟動。</span><span class="sxs-lookup"><span data-stu-id="23ef8-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="23ef8-315">您可以變更使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="23ef8-316">服務會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="23ef8-316">The service continues to run.</span></span> <span data-ttu-id="23ef8-317">但是，如果服務停止，您就無法將它重新開機，因為 SCM 會繼續使用舊的、不正確密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="23ef8-318">變更 Active Directory 中的密碼並不會變更儲存在服務資料庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="23ef8-319">如果您在一般使用者帳戶下執行服務，則每次使用者帳戶密碼變更時，都必須更新這些服務密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="23ef8-320">如果您不確定哪些服務是在該帳戶下執行，或是哪些電腦的服務是在該帳戶下執行，這可能特別耗時。</span><span class="sxs-lookup"><span data-stu-id="23ef8-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="23ef8-321">幸運的是，您可以使用 WMI 來檢查所有電腦上的服務帳戶，如有必要，也可以變更服務帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="23ef8-322">[**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)參數代表定義執行相依性的一組系統服務。</span><span class="sxs-lookup"><span data-stu-id="23ef8-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="23ef8-323">服務必須依「載入順序」群組所指定的順序起始，因為服務會彼此相依。</span><span class="sxs-lookup"><span data-stu-id="23ef8-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="23ef8-324">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="23ef8-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="23ef8-325">若要將服務從網路服務變更為本機系統， *StartName* 和 *StartPassword* 參數應該具有下列值：</span><span class="sxs-lookup"><span data-stu-id="23ef8-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="23ef8-326">若要將服務從本機系統服務變更為網路， *StartName* 和 *StartPassword* 參數應該具有下列值：</span><span class="sxs-lookup"><span data-stu-id="23ef8-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="23ef8-327">範例</span><span class="sxs-lookup"><span data-stu-id="23ef8-327">Examples</span></span>

<span data-ttu-id="23ef8-328">下列 VBScript 會將服務的服務帳戶從指定的使用者帳戶，變更為 LocalSystem。</span><span class="sxs-lookup"><span data-stu-id="23ef8-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="23ef8-329">下列 VBScript 會變更在 Netsvc 下執行之所有腳本的服務帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="23ef8-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="23ef8-330">規格需求</span><span class="sxs-lookup"><span data-stu-id="23ef8-330">Requirements</span></span>



| <span data-ttu-id="23ef8-331">需求</span><span class="sxs-lookup"><span data-stu-id="23ef8-331">Requirement</span></span> | <span data-ttu-id="23ef8-332">值</span><span class="sxs-lookup"><span data-stu-id="23ef8-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23ef8-333">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23ef8-333">Minimum supported client</span></span><br/> | <span data-ttu-id="23ef8-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23ef8-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23ef8-335">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23ef8-335">Minimum supported server</span></span><br/> | <span data-ttu-id="23ef8-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23ef8-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23ef8-337">命名空間</span><span class="sxs-lookup"><span data-stu-id="23ef8-337">Namespace</span></span><br/>                | <span data-ttu-id="23ef8-338">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="23ef8-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23ef8-339">標頭</span><span class="sxs-lookup"><span data-stu-id="23ef8-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ef8-340"><dt>Mbnapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="23ef8-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="23ef8-341">MOF</span><span class="sxs-lookup"><span data-stu-id="23ef8-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23ef8-342"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="23ef8-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23ef8-343">DLL</span><span class="sxs-lookup"><span data-stu-id="23ef8-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23ef8-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23ef8-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ef8-345">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23ef8-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="23ef8-346">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23ef8-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="23ef8-347">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="23ef8-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="23ef8-348">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="23ef8-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

