---
description: 修改衍生自 Win32 BaseService 的服務物件 \_ 。
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: 'Win32_BaseService 類別的 Change 方法 (Mbnapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111112"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="9420c-103">Win32 BaseService 類別的 Change 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9420c-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="9420c-104">**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改衍生自 [**Win32 \_ BaseService**](win32-baseservice.md)的服務物件。</span><span class="sxs-lookup"><span data-stu-id="9420c-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="9420c-105">[**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)參數代表定義執行相依性的一組系統服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="9420c-106">服務必須依 Load Order 群組所指定的順序起始，因為服務會彼此相依。</span><span class="sxs-lookup"><span data-stu-id="9420c-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="9420c-107">這些相依服務需要 antecedent 服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="9420c-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="9420c-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="9420c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9420c-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="9420c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9420c-110">語法</span><span class="sxs-lookup"><span data-stu-id="9420c-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9420c-111">參數</span><span class="sxs-lookup"><span data-stu-id="9420c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9420c-112">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-113">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9420c-113">The display name for a service.</span></span> <span data-ttu-id="9420c-114">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="9420c-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="9420c-115">服務控制管理員中會保留名稱的大小寫。</span><span class="sxs-lookup"><span data-stu-id="9420c-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="9420c-116">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9420c-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="9420c-117">條件約束：接受與 *Name* 參數相同的值。</span><span class="sxs-lookup"><span data-stu-id="9420c-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="9420c-118">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="9420c-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="9420c-119">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-120">可執行檔的完整路徑，該檔案會執行服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="9420c-121">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="9420c-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="9420c-122">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-123">提供給呼叫它們的進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="9420c-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="9420c-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**核心驅動程式** (1) </span><span class="sxs-lookup"><span data-stu-id="9420c-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="9420c-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**檔案系統驅動程式** (2) </span><span class="sxs-lookup"><span data-stu-id="9420c-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="9420c-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**介面卡** (4) </span><span class="sxs-lookup"><span data-stu-id="9420c-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="9420c-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>辨識 **器驅動程式** (8) </span><span class="sxs-lookup"><span data-stu-id="9420c-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="9420c-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span> (16) 的 **進程**</span><span class="sxs-lookup"><span data-stu-id="9420c-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="9420c-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**共用進程** (32) </span><span class="sxs-lookup"><span data-stu-id="9420c-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9420c-130"> (256) </span><span class="sxs-lookup"><span data-stu-id="9420c-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="9420c-131">互動式進程</span><span class="sxs-lookup"><span data-stu-id="9420c-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9420c-132">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-133">如果此服務未在啟動時啟動，則為錯誤的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9420c-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="9420c-134">值指出發生失敗時，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="9420c-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="9420c-135">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="9420c-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="9420c-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) </span><span class="sxs-lookup"><span data-stu-id="9420c-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9420c-137">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="9420c-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="9420c-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="9420c-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9420c-139">一般。</span><span class="sxs-lookup"><span data-stu-id="9420c-139">Normal.</span></span> <span data-ttu-id="9420c-140">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="9420c-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="9420c-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) </span><span class="sxs-lookup"><span data-stu-id="9420c-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9420c-142">系統會重新開機，並使用上一個良好的設定。</span><span class="sxs-lookup"><span data-stu-id="9420c-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="9420c-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="9420c-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9420c-144">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="9420c-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9420c-145">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-146">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="9420c-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="9420c-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) </span><span class="sxs-lookup"><span data-stu-id="9420c-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="9420c-148">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="9420c-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="9420c-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="9420c-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="9420c-150">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="9420c-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="9420c-151">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="9420c-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) </span><span class="sxs-lookup"><span data-stu-id="9420c-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="9420c-153">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="9420c-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) </span><span class="sxs-lookup"><span data-stu-id="9420c-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="9420c-155">當進程呼叫 [**StartService**](startservice-method-in-class-win32-baseservice.md) 方法時，服務控制管理員會啟動服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9420c-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="9420c-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="9420c-157">無法啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9420c-158">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-159">若 **為 True**，則服務可以建立或與桌面上的視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9420c-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-160">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-161">服務執行所在的帳戶名稱，視服務類型而定。</span><span class="sxs-lookup"><span data-stu-id="9420c-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="9420c-162">帳戶名稱的格式可以是 DomainName \\ Username 或。 \\使用者。</span><span class="sxs-lookup"><span data-stu-id="9420c-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="9420c-163">當它執行時，會使用前兩種格式的其中一種來記錄服務處理常式。</span><span class="sxs-lookup"><span data-stu-id="9420c-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="9420c-164">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9420c-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="9420c-165">如果指定了空字串，服務就會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="9420c-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="9420c-166">若是核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱，例如， \\ FileSystem \\ Rdr 或 \\ driver \\ Xns，) 系統用來載入設備磁碟機的輸入和輸出 (i/o。</span><span class="sxs-lookup"><span data-stu-id="9420c-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="9420c-167">如果指定 **Null** ，驅動程式會以預設物件名稱執行，系統會根據服務名稱（例如，DWDOM Admin）來建立 i/o 系統 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9420c-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="9420c-168">您也可以使用 (UPN) 格式的使用者主體名稱來指定 **StartName**，例如 *Username@DomainName* 。</span><span class="sxs-lookup"><span data-stu-id="9420c-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-169">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-170">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="9420c-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="9420c-171">當您未變更密碼時，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9420c-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="9420c-172">如果服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="9420c-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="9420c-173">當您將服務從本機系統變更為網路或從網路變更為本機系統時， *StartPassword* 必須是空字串 ( "" ) 而非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9420c-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="9420c-174">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-175">與其相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="9420c-175">Group name that it is associated with.</span></span> <span data-ttu-id="9420c-176">載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="9420c-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="9420c-177">如果指標為 **Null** 或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="9420c-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="9420c-178">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="9420c-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="9420c-179">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="9420c-180">系統登錄中的載入順序群組清單位於 **HKEY \_ LOCAL \_ MACHINE** \\ **system** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**。</span><span class="sxs-lookup"><span data-stu-id="9420c-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-181">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-182">必須在此服務啟動之前啟動的載入順序群組清單。</span><span class="sxs-lookup"><span data-stu-id="9420c-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="9420c-183">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="9420c-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="9420c-184">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="9420c-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="9420c-185">組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (在 Winsvc .h 檔案中定義) 字元，以區別它們與服務名稱，因為服務和服務群組會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="9420c-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="9420c-186">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-187">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9420c-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9420c-188">包含必須在此服務啟動之前啟動之服務名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="9420c-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="9420c-189">陣列是雙重以 **null** 終止的。</span><span class="sxs-lookup"><span data-stu-id="9420c-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="9420c-190">如果指標為 **Null** 或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="9420c-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="9420c-191">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9420c-192">傳回值</span><span class="sxs-lookup"><span data-stu-id="9420c-192">Return value</span></span>

<span data-ttu-id="9420c-193">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="9420c-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9420c-194">「成功」</span><span class="sxs-lookup"><span data-stu-id="9420c-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-195">0</span><span class="sxs-lookup"><span data-stu-id="9420c-195">0</span></span>

<span data-ttu-id="9420c-196">已接受要求。</span><span class="sxs-lookup"><span data-stu-id="9420c-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-197">**不支援**</span><span class="sxs-lookup"><span data-stu-id="9420c-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-198">1</span><span class="sxs-lookup"><span data-stu-id="9420c-198">1</span></span>

<span data-ttu-id="9420c-199">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="9420c-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-200">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="9420c-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-201">2</span><span class="sxs-lookup"><span data-stu-id="9420c-201">2</span></span>

<span data-ttu-id="9420c-202">使用者沒有必要的存取權限。</span><span class="sxs-lookup"><span data-stu-id="9420c-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-203">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="9420c-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-204">3</span><span class="sxs-lookup"><span data-stu-id="9420c-204">3</span></span>

<span data-ttu-id="9420c-205">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="9420c-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-206">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="9420c-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-207">4</span><span class="sxs-lookup"><span data-stu-id="9420c-207">4</span></span>

<span data-ttu-id="9420c-208">要求的控制項程式碼無效，或是服務無法接受。</span><span class="sxs-lookup"><span data-stu-id="9420c-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-209">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="9420c-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-210">5</span><span class="sxs-lookup"><span data-stu-id="9420c-210">5</span></span>

<span data-ttu-id="9420c-211">由於 [**Win32 \_ BaseService**](win32-baseservice.md)物件中的 [**State**](win32-baseservice.md)屬性等於0、1或2，因此無法將要求的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-212">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="9420c-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-213">6</span><span class="sxs-lookup"><span data-stu-id="9420c-213">6</span></span>

<span data-ttu-id="9420c-214">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-215">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="9420c-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-216">7</span><span class="sxs-lookup"><span data-stu-id="9420c-216">7</span></span>

<span data-ttu-id="9420c-217">服務不會快速回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="9420c-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-218">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="9420c-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-219">8</span><span class="sxs-lookup"><span data-stu-id="9420c-219">8</span></span>

<span data-ttu-id="9420c-220">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="9420c-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-221">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="9420c-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-222">9</span><span class="sxs-lookup"><span data-stu-id="9420c-222">9</span></span>

<span data-ttu-id="9420c-223">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="9420c-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-224">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="9420c-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-225">10</span><span class="sxs-lookup"><span data-stu-id="9420c-225">10</span></span>

<span data-ttu-id="9420c-226">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="9420c-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-227">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="9420c-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-228">11</span><span class="sxs-lookup"><span data-stu-id="9420c-228">11</span></span>

<span data-ttu-id="9420c-229">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="9420c-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-230">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="9420c-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-231">12</span><span class="sxs-lookup"><span data-stu-id="9420c-231">12</span></span>

<span data-ttu-id="9420c-232">系統會從系統中移除這項服務所依賴的相依性。</span><span class="sxs-lookup"><span data-stu-id="9420c-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-233">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="9420c-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-234">13</span><span class="sxs-lookup"><span data-stu-id="9420c-234">13</span></span>

<span data-ttu-id="9420c-235">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-236">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="9420c-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-237">14</span><span class="sxs-lookup"><span data-stu-id="9420c-237">14</span></span>

<span data-ttu-id="9420c-238">系統會停用服務。</span><span class="sxs-lookup"><span data-stu-id="9420c-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-239">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="9420c-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-240">15</span><span class="sxs-lookup"><span data-stu-id="9420c-240">15</span></span>

<span data-ttu-id="9420c-241">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="9420c-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-242">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="9420c-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-243">16</span><span class="sxs-lookup"><span data-stu-id="9420c-243">16</span></span>

<span data-ttu-id="9420c-244">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="9420c-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-245">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="9420c-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-246">17</span><span class="sxs-lookup"><span data-stu-id="9420c-246">17</span></span>

<span data-ttu-id="9420c-247">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="9420c-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-248">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="9420c-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-249">18</span><span class="sxs-lookup"><span data-stu-id="9420c-249">18</span></span>

<span data-ttu-id="9420c-250">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="9420c-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-251">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="9420c-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-252">19</span><span class="sxs-lookup"><span data-stu-id="9420c-252">19</span></span>

<span data-ttu-id="9420c-253">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="9420c-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-254">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="9420c-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-255">20</span><span class="sxs-lookup"><span data-stu-id="9420c-255">20</span></span>

<span data-ttu-id="9420c-256">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="9420c-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-257">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="9420c-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-258">21</span><span class="sxs-lookup"><span data-stu-id="9420c-258">21</span></span>

<span data-ttu-id="9420c-259">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="9420c-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-260">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="9420c-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-261">22</span><span class="sxs-lookup"><span data-stu-id="9420c-261">22</span></span>

<span data-ttu-id="9420c-262">用來執行此服務的帳戶無效，或沒有執行此服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="9420c-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-263">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="9420c-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-264">23</span><span class="sxs-lookup"><span data-stu-id="9420c-264">23</span></span>

<span data-ttu-id="9420c-265">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9420c-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-266">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="9420c-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-267">24</span><span class="sxs-lookup"><span data-stu-id="9420c-267">24</span></span>

<span data-ttu-id="9420c-268">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="9420c-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="9420c-269">**其他**</span><span class="sxs-lookup"><span data-stu-id="9420c-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9420c-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="9420c-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9420c-271">備註</span><span class="sxs-lookup"><span data-stu-id="9420c-271">Remarks</span></span>

<span data-ttu-id="9420c-272">若要將服務從網路變更為本機系統，請使用下列值作為 *StartName* 和 *StartPassword* 參數：</span><span class="sxs-lookup"><span data-stu-id="9420c-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="9420c-273">若要將服務從本機系統變更為網路，請針對 *StartName* 和 *StartPassword* 參數使用下列值：</span><span class="sxs-lookup"><span data-stu-id="9420c-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="9420c-274">規格需求</span><span class="sxs-lookup"><span data-stu-id="9420c-274">Requirements</span></span>



| <span data-ttu-id="9420c-275">需求</span><span class="sxs-lookup"><span data-stu-id="9420c-275">Requirement</span></span> | <span data-ttu-id="9420c-276">值</span><span class="sxs-lookup"><span data-stu-id="9420c-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9420c-277">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9420c-277">Minimum supported client</span></span><br/> | <span data-ttu-id="9420c-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9420c-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9420c-279">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9420c-279">Minimum supported server</span></span><br/> | <span data-ttu-id="9420c-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9420c-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9420c-281">命名空間</span><span class="sxs-lookup"><span data-stu-id="9420c-281">Namespace</span></span><br/>                | <span data-ttu-id="9420c-282">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9420c-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9420c-283">標頭</span><span class="sxs-lookup"><span data-stu-id="9420c-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="9420c-284"><dt>Mbnapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9420c-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="9420c-285">MOF</span><span class="sxs-lookup"><span data-stu-id="9420c-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9420c-286"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9420c-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9420c-287">DLL</span><span class="sxs-lookup"><span data-stu-id="9420c-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9420c-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9420c-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9420c-289">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9420c-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="9420c-290">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9420c-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9420c-291">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="9420c-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

