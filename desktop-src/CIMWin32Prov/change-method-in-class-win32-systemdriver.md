---
description: 修改 Win32 \_ >systemdriver 服務。
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: 'Win32_SystemDriver 類別的 Change 方法 (Mbnapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468368"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="3d165-103">Win32 >systemdriver 類別的 Change 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3d165-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="3d165-104">**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ >systemdriver**](win32-systemdriver.md)服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="3d165-105">[**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)參數代表定義執行相依性的系統服務群組。</span><span class="sxs-lookup"><span data-stu-id="3d165-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="3d165-106">服務必須依照載入順序群組所指定的順序起始，因為服務彼此相依。</span><span class="sxs-lookup"><span data-stu-id="3d165-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="3d165-107">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="3d165-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="3d165-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3d165-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3d165-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3d165-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d165-110">語法</span><span class="sxs-lookup"><span data-stu-id="3d165-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="3d165-111">參數</span><span class="sxs-lookup"><span data-stu-id="3d165-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d165-112">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-113">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3d165-113">The display name of the service.</span></span> <span data-ttu-id="3d165-114">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="3d165-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="3d165-115">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="3d165-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="3d165-116">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3d165-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="3d165-117">條件約束：接受與 *Name* 參數相同的值。</span><span class="sxs-lookup"><span data-stu-id="3d165-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="3d165-118">範例： "Atdisk"</span><span class="sxs-lookup"><span data-stu-id="3d165-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="3d165-119">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-120">可執行檔的完整路徑，此檔案可執行服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="3d165-121">範例： *\\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="3d165-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="3d165-122">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-123">提供給呼叫它們之進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="3d165-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="3d165-124">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="3d165-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-125">核心驅動程式</span><span class="sxs-lookup"><span data-stu-id="3d165-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="3d165-126">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="3d165-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-127">檔案系統驅動程式</span><span class="sxs-lookup"><span data-stu-id="3d165-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="3d165-128">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="3d165-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-129">配接器</span><span class="sxs-lookup"><span data-stu-id="3d165-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="3d165-130">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="3d165-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-131">辨識器驅動程式</span><span class="sxs-lookup"><span data-stu-id="3d165-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="3d165-132">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="3d165-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-133">自有進程</span><span class="sxs-lookup"><span data-stu-id="3d165-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="3d165-134">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="3d165-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-135">共用進程</span><span class="sxs-lookup"><span data-stu-id="3d165-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="3d165-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="3d165-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="3d165-137">互動式進程</span><span class="sxs-lookup"><span data-stu-id="3d165-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d165-138">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-139">如果這項服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="3d165-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="3d165-140">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="3d165-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="3d165-141">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d165-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="3d165-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) </span><span class="sxs-lookup"><span data-stu-id="3d165-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3d165-143">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="3d165-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="3d165-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="3d165-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3d165-145">一般。</span><span class="sxs-lookup"><span data-stu-id="3d165-145">Normal.</span></span> <span data-ttu-id="3d165-146">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="3d165-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="3d165-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) </span><span class="sxs-lookup"><span data-stu-id="3d165-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3d165-148">系統會重新開機，並使用上一個良好的設定。</span><span class="sxs-lookup"><span data-stu-id="3d165-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3d165-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="3d165-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d165-150">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="3d165-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d165-151">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-152">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="3d165-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="3d165-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機啟動**</span><span class="sxs-lookup"><span data-stu-id="3d165-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-154">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d165-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="3d165-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機啟動**</span><span class="sxs-lookup"><span data-stu-id="3d165-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-156">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d165-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="3d165-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動**</span><span class="sxs-lookup"><span data-stu-id="3d165-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-158">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d165-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="3d165-159">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="3d165-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動**</span><span class="sxs-lookup"><span data-stu-id="3d165-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-161">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="3d165-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始**</span><span class="sxs-lookup"><span data-stu-id="3d165-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-163">當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員會啟動服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d165-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**</span><span class="sxs-lookup"><span data-stu-id="3d165-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="3d165-165">無法啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d165-166">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-167">值，如果 **為 True**，服務可以建立或與桌面上的視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="3d165-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="3d165-168">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-169">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3d165-169">The account name the service runs under.</span></span> <span data-ttu-id="3d165-170">根據服務類型而定，帳戶名稱可能採用 DomainName 使用者名稱或的形式 \\ 。 \\使用者。</span><span class="sxs-lookup"><span data-stu-id="3d165-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="3d165-171">當它執行時，會使用這兩種形式的其中一種來記錄服務進程。</span><span class="sxs-lookup"><span data-stu-id="3d165-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="3d165-172">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="3d165-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="3d165-173">如果指定了空字串，服務就會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="3d165-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="3d165-174">若是核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱，例如， \\ FileSystem \\ Rdr 或 \\ driver \\ Xns) ， (i/o) 系統用來載入設備磁碟機的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="3d165-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="3d165-175">如果指定 **Null** ，驅動程式會以預設物件名稱執行，系統會根據服務名稱（例如，DWDOM Admin）來建立 i/o 系統 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3d165-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="3d165-176">您也可以使用 (UPN) 格式的使用者主體名稱來指定 **StartName**，例如 *Username@DomainName* 。</span><span class="sxs-lookup"><span data-stu-id="3d165-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="3d165-177">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-178">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="3d165-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="3d165-179">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3d165-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="3d165-180">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="3d165-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="3d165-181">將服務從本機系統變更為網路，或從網路變更為本機系統時， *StartPassword* 必須是空字串 ( "" ) 而非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3d165-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="3d165-182">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-183">與其相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="3d165-183">The group name that it is associated with.</span></span> <span data-ttu-id="3d165-184">載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="3d165-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="3d165-185">如果指標為 **Null**，或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="3d165-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="3d165-186">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="3d165-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="3d165-187">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="3d165-188">系統登錄中的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="3d165-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="3d165-189">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="3d165-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="3d165-190">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-191">必須在此服務啟動之前啟動的載入順序群組清單。</span><span class="sxs-lookup"><span data-stu-id="3d165-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="3d165-192">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="3d165-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="3d165-193">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="3d165-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="3d165-194">組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (在 WinSvc .h 檔案中定義) 字元，以區別它們與服務名稱，因為服務和服務群組會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3d165-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="3d165-195">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="3d165-196">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d165-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d165-197">包含必須在此服務啟動之前啟動之服務名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="3d165-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="3d165-198">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="3d165-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="3d165-199">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="3d165-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="3d165-200">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="3d165-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d165-201">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d165-201">Return value</span></span>

<span data-ttu-id="3d165-202">如果已成功修改服務，則傳回零 (0) ，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="3d165-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3d165-203">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="3d165-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-204">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="3d165-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-205">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="3d165-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-206">正在執行 (3) 的 **相依服務**</span><span class="sxs-lookup"><span data-stu-id="3d165-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-207">**不正確服務控制** (4) </span><span class="sxs-lookup"><span data-stu-id="3d165-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-208">**服務無法接受 Control** (5) </span><span class="sxs-lookup"><span data-stu-id="3d165-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-209">**服務非** 使用中 (6) </span><span class="sxs-lookup"><span data-stu-id="3d165-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-210">**服務要求超時** (7) </span><span class="sxs-lookup"><span data-stu-id="3d165-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-211">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="3d165-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-212"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="3d165-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-213">**服務已** 在執行 (10) </span><span class="sxs-lookup"><span data-stu-id="3d165-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-214">**服務資料庫已鎖定** (11) </span><span class="sxs-lookup"><span data-stu-id="3d165-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-215">**服務相依性已刪除** (12) </span><span class="sxs-lookup"><span data-stu-id="3d165-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-216">**服務** 相依性失敗 (13) </span><span class="sxs-lookup"><span data-stu-id="3d165-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-217">**服務已停用** (14) </span><span class="sxs-lookup"><span data-stu-id="3d165-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-218">**服務登入失敗** (15) </span><span class="sxs-lookup"><span data-stu-id="3d165-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-219">已 **標示為要刪除的服務** (16) </span><span class="sxs-lookup"><span data-stu-id="3d165-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-220">**服務沒有線程** (17) </span><span class="sxs-lookup"><span data-stu-id="3d165-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-221">**狀態迴圈** 相依性 (18) </span><span class="sxs-lookup"><span data-stu-id="3d165-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-222">**狀態重複名稱** (19) </span><span class="sxs-lookup"><span data-stu-id="3d165-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-223">**狀態不正確名稱** (20) </span><span class="sxs-lookup"><span data-stu-id="3d165-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-224">**狀態不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="3d165-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-225">**狀態不正確服務帳戶** (22) </span><span class="sxs-lookup"><span data-stu-id="3d165-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-226">**狀態服務存在** (23) </span><span class="sxs-lookup"><span data-stu-id="3d165-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-227">**服務已暫停** (24) </span><span class="sxs-lookup"><span data-stu-id="3d165-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="3d165-228">**其他** (25 4294967295) </span><span class="sxs-lookup"><span data-stu-id="3d165-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3d165-229">備註</span><span class="sxs-lookup"><span data-stu-id="3d165-229">Remarks</span></span>

<span data-ttu-id="3d165-230">若要將服務從網路服務變更為本機系統，請使用下列值作為 *StartName* 和 *StartPassword* 參數：</span><span class="sxs-lookup"><span data-stu-id="3d165-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="3d165-231">若要將服務從本機系統服務變更為 network service，請針對 *StartName* 和 *StartPassword* 參數使用下列值：</span><span class="sxs-lookup"><span data-stu-id="3d165-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="3d165-232">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d165-232">Requirements</span></span>



| <span data-ttu-id="3d165-233">需求</span><span class="sxs-lookup"><span data-stu-id="3d165-233">Requirement</span></span> | <span data-ttu-id="3d165-234">值</span><span class="sxs-lookup"><span data-stu-id="3d165-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d165-235">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d165-235">Minimum supported client</span></span><br/> | <span data-ttu-id="3d165-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d165-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d165-237">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d165-237">Minimum supported server</span></span><br/> | <span data-ttu-id="3d165-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d165-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d165-239">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d165-239">Namespace</span></span><br/>                | <span data-ttu-id="3d165-240">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d165-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d165-241">標頭</span><span class="sxs-lookup"><span data-stu-id="3d165-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d165-242"><dt>Mbnapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d165-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="3d165-243">MOF</span><span class="sxs-lookup"><span data-stu-id="3d165-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d165-244"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d165-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d165-245">DLL</span><span class="sxs-lookup"><span data-stu-id="3d165-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d165-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d165-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d165-247">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d165-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d165-248">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d165-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3d165-249">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="3d165-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

