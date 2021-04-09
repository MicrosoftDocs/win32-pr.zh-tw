---
description: 建立新的服務。
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110601"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="f3778-103">Win32 BaseService 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f3778-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="f3778-104">**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="f3778-105">*LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。</span><span class="sxs-lookup"><span data-stu-id="f3778-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="f3778-106">服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。</span><span class="sxs-lookup"><span data-stu-id="f3778-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="f3778-107">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="f3778-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="f3778-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f3778-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f3778-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f3778-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3778-110">語法</span><span class="sxs-lookup"><span data-stu-id="f3778-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f3778-111">參數</span><span class="sxs-lookup"><span data-stu-id="f3778-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3778-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-113">要安裝至 **Create** 方法的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f3778-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="f3778-114">字串長度上限為256個字元。</span><span class="sxs-lookup"><span data-stu-id="f3778-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="f3778-115">服務控制管理員資料庫會保留字元的大小寫，但服務名稱比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f3778-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="f3778-116">正斜線 (/) 和雙反斜線 (\\) 是不正確服務名稱字元。</span><span class="sxs-lookup"><span data-stu-id="f3778-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-117">*DisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-118">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f3778-118">Display name of the service.</span></span> <span data-ttu-id="f3778-119">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="f3778-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="f3778-120">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="f3778-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="f3778-121">*DisplayName* 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f3778-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="f3778-122">條件約束：接受與 *Name* 參數相同的值。</span><span class="sxs-lookup"><span data-stu-id="f3778-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="f3778-123">範例： "Atdisk"。</span><span class="sxs-lookup"><span data-stu-id="f3778-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="f3778-124">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-125">可執行檔的完整路徑，該檔案可執行服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="f3778-126">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。</span><span class="sxs-lookup"><span data-stu-id="f3778-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="f3778-127">*ServiceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-128">提供給呼叫它們的進程的服務類型。</span><span class="sxs-lookup"><span data-stu-id="f3778-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="f3778-129">此值為點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f3778-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="f3778-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**核心驅動程式** (1) </span><span class="sxs-lookup"><span data-stu-id="f3778-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="f3778-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**檔案系統驅動程式** (2) </span><span class="sxs-lookup"><span data-stu-id="f3778-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="f3778-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**介面卡** (4) </span><span class="sxs-lookup"><span data-stu-id="f3778-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="f3778-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>辨識 **器驅動程式** (8) </span><span class="sxs-lookup"><span data-stu-id="f3778-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="f3778-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span> (16) 的 **進程**</span><span class="sxs-lookup"><span data-stu-id="f3778-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="f3778-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**共用進程** (32) </span><span class="sxs-lookup"><span data-stu-id="f3778-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="f3778-136">256</span><span class="sxs-lookup"><span data-stu-id="f3778-136">256</span></span>
</dt> <dd>

<span data-ttu-id="f3778-137">互動式進程</span><span class="sxs-lookup"><span data-stu-id="f3778-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f3778-138">*ErrorControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-139">**建立** 方法無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="f3778-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="f3778-140">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="f3778-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="f3778-141">系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3778-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="f3778-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) </span><span class="sxs-lookup"><span data-stu-id="f3778-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f3778-143">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="f3778-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="f3778-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="f3778-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f3778-145">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="f3778-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="f3778-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) </span><span class="sxs-lookup"><span data-stu-id="f3778-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f3778-147">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="f3778-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f3778-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="f3778-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3778-149">系統嘗試以良好的設定開始。</span><span class="sxs-lookup"><span data-stu-id="f3778-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f3778-150">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-151">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="f3778-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="f3778-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) </span><span class="sxs-lookup"><span data-stu-id="f3778-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="f3778-153">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f3778-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="f3778-154">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="f3778-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="f3778-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="f3778-156">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f3778-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f3778-157">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="f3778-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) </span><span class="sxs-lookup"><span data-stu-id="f3778-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="f3778-159">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="f3778-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) </span><span class="sxs-lookup"><span data-stu-id="f3778-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="f3778-161">當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3778-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="f3778-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="f3778-163">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f3778-164">*DesktopInteract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-165">若 **為 true**，則服務可以在桌面上建立 windows 或與其通訊。</span><span class="sxs-lookup"><span data-stu-id="f3778-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-166">*StartName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-167">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f3778-167">Account name under which the service runs.</span></span> <span data-ttu-id="f3778-168">根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username"。</span><span class="sxs-lookup"><span data-stu-id="f3778-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="f3778-169">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="f3778-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="f3778-170">如果帳戶屬於內建網域，則為」。 \\您可以指定使用者名稱」。</span><span class="sxs-lookup"><span data-stu-id="f3778-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="f3778-171">如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="f3778-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="f3778-172">若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f3778-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="f3778-173">如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。</span><span class="sxs-lookup"><span data-stu-id="f3778-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="f3778-174">範例： DWDOM \\ Admin。</span><span class="sxs-lookup"><span data-stu-id="f3778-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-175">*StartPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-176">*StartName* 參數所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3778-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="f3778-177">如果您不變更密碼，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f3778-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="f3778-178">如果此服務沒有密碼，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="f3778-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-179">*LoadOrderGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-180">與新服務相關聯的組名。</span><span class="sxs-lookup"><span data-stu-id="f3778-180">Group name associated with the new service.</span></span> <span data-ttu-id="f3778-181">載入順序群組包含于登錄中，並決定將服務載入作業系統的順序。</span><span class="sxs-lookup"><span data-stu-id="f3778-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="f3778-182">如果指標為 **Null** 或指向空字串，則服務不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="f3778-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="f3778-183">群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。</span><span class="sxs-lookup"><span data-stu-id="f3778-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="f3778-184">[載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="f3778-185">登錄的載入順序群組清單位於：</span><span class="sxs-lookup"><span data-stu-id="f3778-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="f3778-186">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="f3778-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="f3778-187">*LoadOrderGroupDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-188">必須在此服務之前啟動的載入順序群組陣列。</span><span class="sxs-lookup"><span data-stu-id="f3778-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="f3778-189">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="f3778-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f3778-190">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="f3778-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f3778-191">如果指標為 **Null** 或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="f3778-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f3778-192">組名必須以 \_ Winsvc 中定義的 SC 群組識別碼作為前置詞 \_ ， (在 .h 檔案中定義) 字元，以與服務名稱區別，因為服務和服務群組會共用相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f3778-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="f3778-193">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-194">*ServiceDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3778-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3778-195">陣列，包含在此服務啟動之前必須啟動之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3778-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="f3778-196">陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。</span><span class="sxs-lookup"><span data-stu-id="f3778-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f3778-197">在 Visual Basic 或腳本中，您可以傳遞 vbArray。</span><span class="sxs-lookup"><span data-stu-id="f3778-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f3778-198">如果指標為 **Null**，或指向空字串，則服務沒有相依性。</span><span class="sxs-lookup"><span data-stu-id="f3778-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f3778-199">服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3778-200">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3778-200">Return value</span></span>

<span data-ttu-id="f3778-201">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3778-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f3778-202">「成功」</span><span class="sxs-lookup"><span data-stu-id="f3778-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-203">0</span><span class="sxs-lookup"><span data-stu-id="f3778-203">0</span></span>

<span data-ttu-id="f3778-204">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="f3778-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-205">**不支援**</span><span class="sxs-lookup"><span data-stu-id="f3778-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-206">1</span><span class="sxs-lookup"><span data-stu-id="f3778-206">1</span></span>

<span data-ttu-id="f3778-207">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="f3778-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-208">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="f3778-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-209">2</span><span class="sxs-lookup"><span data-stu-id="f3778-209">2</span></span>

<span data-ttu-id="f3778-210">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="f3778-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-211">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="f3778-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-212">3</span><span class="sxs-lookup"><span data-stu-id="f3778-212">3</span></span>

<span data-ttu-id="f3778-213">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="f3778-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-214">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="f3778-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-215">4</span><span class="sxs-lookup"><span data-stu-id="f3778-215">4</span></span>

<span data-ttu-id="f3778-216">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3778-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-217">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="f3778-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-218">5</span><span class="sxs-lookup"><span data-stu-id="f3778-218">5</span></span>

<span data-ttu-id="f3778-219">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="f3778-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-220">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="f3778-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-221">6</span><span class="sxs-lookup"><span data-stu-id="f3778-221">6</span></span>

<span data-ttu-id="f3778-222">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-223">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="f3778-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-224">7</span><span class="sxs-lookup"><span data-stu-id="f3778-224">7</span></span>

<span data-ttu-id="f3778-225">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="f3778-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-226">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="f3778-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-227">8</span><span class="sxs-lookup"><span data-stu-id="f3778-227">8</span></span>

<span data-ttu-id="f3778-228">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="f3778-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-229">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="f3778-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-230">9</span><span class="sxs-lookup"><span data-stu-id="f3778-230">9</span></span>

<span data-ttu-id="f3778-231">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="f3778-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-232">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="f3778-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-233">10</span><span class="sxs-lookup"><span data-stu-id="f3778-233">10</span></span>

<span data-ttu-id="f3778-234">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="f3778-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-235">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="f3778-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-236">11</span><span class="sxs-lookup"><span data-stu-id="f3778-236">11</span></span>

<span data-ttu-id="f3778-237">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="f3778-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-238">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="f3778-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-239">12</span><span class="sxs-lookup"><span data-stu-id="f3778-239">12</span></span>

<span data-ttu-id="f3778-240">已經從系統中移除這個服務所依賴的相依性。</span><span class="sxs-lookup"><span data-stu-id="f3778-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-241">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="f3778-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-242">13</span><span class="sxs-lookup"><span data-stu-id="f3778-242">13</span></span>

<span data-ttu-id="f3778-243">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-244">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="f3778-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-245">14</span><span class="sxs-lookup"><span data-stu-id="f3778-245">14</span></span>

<span data-ttu-id="f3778-246">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="f3778-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-247">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="f3778-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-248">15</span><span class="sxs-lookup"><span data-stu-id="f3778-248">15</span></span>

<span data-ttu-id="f3778-249">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="f3778-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-250">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="f3778-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-251">16</span><span class="sxs-lookup"><span data-stu-id="f3778-251">16</span></span>

<span data-ttu-id="f3778-252">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="f3778-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-253">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="f3778-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-254">17</span><span class="sxs-lookup"><span data-stu-id="f3778-254">17</span></span>

<span data-ttu-id="f3778-255">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="f3778-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-256">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="f3778-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-257">18</span><span class="sxs-lookup"><span data-stu-id="f3778-257">18</span></span>

<span data-ttu-id="f3778-258">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="f3778-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-259">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="f3778-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-260">19</span><span class="sxs-lookup"><span data-stu-id="f3778-260">19</span></span>

<span data-ttu-id="f3778-261">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="f3778-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-262">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="f3778-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-263">20</span><span class="sxs-lookup"><span data-stu-id="f3778-263">20</span></span>

<span data-ttu-id="f3778-264">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="f3778-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-265">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="f3778-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-266">21</span><span class="sxs-lookup"><span data-stu-id="f3778-266">21</span></span>

<span data-ttu-id="f3778-267">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f3778-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-268">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="f3778-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-269">22</span><span class="sxs-lookup"><span data-stu-id="f3778-269">22</span></span>

<span data-ttu-id="f3778-270">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="f3778-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-271">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="f3778-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-272">23</span><span class="sxs-lookup"><span data-stu-id="f3778-272">23</span></span>

<span data-ttu-id="f3778-273">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="f3778-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-274">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="f3778-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-275">24</span><span class="sxs-lookup"><span data-stu-id="f3778-275">24</span></span>

<span data-ttu-id="f3778-276">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="f3778-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3778-277">**其他**</span><span class="sxs-lookup"><span data-stu-id="f3778-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f3778-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="f3778-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3778-279">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3778-279">Requirements</span></span>



| <span data-ttu-id="f3778-280">需求</span><span class="sxs-lookup"><span data-stu-id="f3778-280">Requirement</span></span> | <span data-ttu-id="f3778-281">值</span><span class="sxs-lookup"><span data-stu-id="f3778-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3778-282">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3778-282">Minimum supported client</span></span><br/> | <span data-ttu-id="f3778-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3778-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3778-284">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3778-284">Minimum supported server</span></span><br/> | <span data-ttu-id="f3778-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3778-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3778-286">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3778-286">Namespace</span></span><br/>                | <span data-ttu-id="f3778-287">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3778-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3778-288">MOF</span><span class="sxs-lookup"><span data-stu-id="f3778-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3778-289"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3778-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3778-290">DLL</span><span class="sxs-lookup"><span data-stu-id="f3778-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3778-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3778-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3778-292">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3778-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3778-293">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3778-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3778-294">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="f3778-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

