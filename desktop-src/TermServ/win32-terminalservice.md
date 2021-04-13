---
title: Win32_TerminalService 類別
description: Win32 服務類別的子類別 \_ 。 Win32 \_ TerminalService 代表 win32 TerminalServiceToSetting 關聯的 Element 屬性 \_ 。
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService 類別遠端桌面服務
- Win32_TerminalService 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466725"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="16980-106">Win32 \_ TerminalService 類別</span><span class="sxs-lookup"><span data-stu-id="16980-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="16980-107">**Win32 \_ TerminalService** WMI 類別是 [**win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="16980-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="16980-108">**Win32 \_TerminalService** 代表 [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **Element** 屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="16980-109">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16980-110">語法</span><span class="sxs-lookup"><span data-stu-id="16980-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="16980-111">成員</span><span class="sxs-lookup"><span data-stu-id="16980-111">Members</span></span>

<span data-ttu-id="16980-112">**Win32 \_ TerminalService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16980-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="16980-113">方法</span><span class="sxs-lookup"><span data-stu-id="16980-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="16980-114">屬性</span><span class="sxs-lookup"><span data-stu-id="16980-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16980-115">方法</span><span class="sxs-lookup"><span data-stu-id="16980-115">Methods</span></span>

<span data-ttu-id="16980-116">**Win32 \_ TerminalService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="16980-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="16980-117">方法</span><span class="sxs-lookup"><span data-stu-id="16980-117">Method</span></span>                                                                       | <span data-ttu-id="16980-118">描述</span><span class="sxs-lookup"><span data-stu-id="16980-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16980-119">**變更**</span><span class="sxs-lookup"><span data-stu-id="16980-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="16980-120">修改服務。</span><span class="sxs-lookup"><span data-stu-id="16980-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="16980-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="16980-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="16980-122">修改服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="16980-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="16980-123">**建立**</span><span class="sxs-lookup"><span data-stu-id="16980-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="16980-124">建立新的服務。</span><span class="sxs-lookup"><span data-stu-id="16980-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="16980-125">**刪除**</span><span class="sxs-lookup"><span data-stu-id="16980-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="16980-126">刪除現有的服務。</span><span class="sxs-lookup"><span data-stu-id="16980-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="16980-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="16980-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="16980-128">傳回控制服務存取的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="16980-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="16980-129">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="16980-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="16980-130">要求服務將其狀態更新至 service manager。</span><span class="sxs-lookup"><span data-stu-id="16980-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="16980-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="16980-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="16980-132">嘗試將服務置於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="16980-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="16980-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="16980-134">嘗試將服務放在恢復狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="16980-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="16980-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="16980-136">寫入安全描述項的更新版本，以控制服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="16980-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="16980-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="16980-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="16980-138">嘗試將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="16980-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="16980-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="16980-140">將服務置於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="16980-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="16980-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="16980-142">嘗試將使用者定義的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="16980-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="16980-143">屬性</span><span class="sxs-lookup"><span data-stu-id="16980-143">Properties</span></span>

<span data-ttu-id="16980-144">**Win32 \_ TerminalService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16980-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="16980-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="16980-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16980-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「服務接受暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="16980-149">指出是否可以暫停服務。</span><span class="sxs-lookup"><span data-stu-id="16980-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="16980-150">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="16980-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-152">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="16980-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16980-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-154">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "服務接受停止" ) </span><span class="sxs-lookup"><span data-stu-id="16980-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="16980-155">指出是否可以停止服務。</span><span class="sxs-lookup"><span data-stu-id="16980-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="16980-156">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-157">**標題**</span><span class="sxs-lookup"><span data-stu-id="16980-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-160">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="16980-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="16980-161">服務的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="16980-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="16980-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="16980-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16980-163">**檢查站**</span><span class="sxs-lookup"><span data-stu-id="16980-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-166">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**service \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Check Point Count" ) </span><span class="sxs-lookup"><span data-stu-id="16980-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="16980-167">此值會在長時間啟動、停止、暫停或繼續作業期間，定期遞增以報告其進度。</span><span class="sxs-lookup"><span data-stu-id="16980-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="16980-168">例如，服務會在啟動時完成其初始化的每個步驟，以遞增此值。</span><span class="sxs-lookup"><span data-stu-id="16980-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="16980-169">在服務上叫用作業的使用者介面程式會使用這個值，在冗長的作業期間追蹤服務的進度。</span><span class="sxs-lookup"><span data-stu-id="16980-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="16980-170">此值無效，而且當服務沒有暫止的啟動、停止、暫停或繼續作業時，應該為零。</span><span class="sxs-lookup"><span data-stu-id="16980-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="16980-171">這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16980-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-175">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="16980-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-176">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="16980-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="16980-177">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="16980-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="16980-178">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="16980-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="16980-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16980-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-182">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 延遲 \_ 自動 \_ 啟動 \_ 資訊**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| FDelayedAutostart" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「延遲的自動啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="16980-183">若 **為 True**，則服務會在其他自動啟動服務啟動後加上短暫延遲之後啟動。</span><span class="sxs-lookup"><span data-stu-id="16980-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="16980-184">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="16980-185">這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-186">**說明**</span><span class="sxs-lookup"><span data-stu-id="16980-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-189">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="16980-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="16980-190">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="16980-190">Description of the object.</span></span>

<span data-ttu-id="16980-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="16980-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16980-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="16980-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-193">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="16980-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16980-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-195">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( [與桌面互動] ) </span><span class="sxs-lookup"><span data-stu-id="16980-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="16980-196">指出服務是否可以在桌面上建立或與 windows 通訊，進而以某種方式與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="16980-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="16980-197">互動式服務必須在本機系統帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="16980-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="16980-198">大部分的服務都不是互動式的;也就是說，它們不會以任何方式與使用者通訊。</span><span class="sxs-lookup"><span data-stu-id="16980-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="16980-199">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-200">**DisconnectedSessions**</span><span class="sxs-lookup"><span data-stu-id="16980-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16980-203">目前伺服器上已中斷連線的會話數目。</span><span class="sxs-lookup"><span data-stu-id="16980-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="16980-204">這些會話可能仍會主動耗用伺服器資源，但目前沒有與用戶端的網路連線。</span><span class="sxs-lookup"><span data-stu-id="16980-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="16980-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="16980-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-208">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Display Name" ) </span><span class="sxs-lookup"><span data-stu-id="16980-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-209">在 [服務] 嵌入式管理單元中所看到的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="16980-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="16980-210">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="16980-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="16980-211">請注意，儲存在登錄) 中的顯示名稱和服務名稱 (不一定相同。</span><span class="sxs-lookup"><span data-stu-id="16980-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="16980-212">例如，DHCP 用戶端服務的服務名稱是 Dhcp，而是顯示名稱 DHCP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="16980-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="16980-213">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="16980-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="16980-214">不過， [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="16980-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="16980-215">Constraint：接受與 [**Name**](/windows/desktop/CIMWin32Prov/win32-service) 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="16980-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="16980-216">範例： "Atdisk"</span><span class="sxs-lookup"><span data-stu-id="16980-216">Example: "Atdisk"</span></span>

<span data-ttu-id="16980-217">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="16980-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-221">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動失敗的嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="16980-222">當此服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="16980-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="16980-223">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="16980-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="16980-224">電腦系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="16980-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="16980-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) </span><span class="sxs-lookup"><span data-stu-id="16980-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="16980-226">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="16980-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="16980-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="16980-228">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="16980-228">User is notified.</span></span> <span data-ttu-id="16980-229">通常這會是顯示通知使用者問題的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="16980-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="16980-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="16980-231">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="16980-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="16980-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="16980-233">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="16980-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="16980-234">如果服務無法第二次啟動，則啟動會失敗。</span><span class="sxs-lookup"><span data-stu-id="16980-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16980-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="16980-236">錯誤的嚴重性未知。</span><span class="sxs-lookup"><span data-stu-id="16980-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="16980-237">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="16980-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-239">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-241">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="16980-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="16980-242">定義啟動或停止服務時所發生之錯誤的 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="16980-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="16980-243">這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 [**可見於 servicespecificexitcode**](/windows/desktop/CIMWin32Prov/win32-service) 屬性中取得。</span><span class="sxs-lookup"><span data-stu-id="16980-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="16980-244">服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="16980-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="16980-245">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="16980-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-247">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="16980-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16980-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-249">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="16980-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="16980-250">已安裝日期物件。</span><span class="sxs-lookup"><span data-stu-id="16980-250">Date object is installed.</span></span> <span data-ttu-id="16980-251">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="16980-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="16980-252">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="16980-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16980-253">**名稱**</span><span class="sxs-lookup"><span data-stu-id="16980-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-256">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16980-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="16980-257">提供受管理功能指示的服務的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="16980-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="16980-258">這項功能會在物件的 [**Description**](/windows/desktop/CIMWin32Prov/win32-service) 屬性中說明。</span><span class="sxs-lookup"><span data-stu-id="16980-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="16980-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="16980-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16980-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="16980-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-263">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Path Name" ) </span><span class="sxs-lookup"><span data-stu-id="16980-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-264">執行服務之服務二進位檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="16980-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="16980-265">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」</span><span class="sxs-lookup"><span data-stu-id="16980-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="16980-266">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-267">**進程**</span><span class="sxs-lookup"><span data-stu-id="16980-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-268">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-270">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態 \_ 進程**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "處理序識別碼" ) </span><span class="sxs-lookup"><span data-stu-id="16980-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="16980-271">服務的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="16980-271">Process identifier of the service.</span></span>

<span data-ttu-id="16980-272">範例：324</span><span class="sxs-lookup"><span data-stu-id="16980-272">Example: 324</span></span>

<span data-ttu-id="16980-273">這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-274">**可見於 servicespecificexitcode**</span><span class="sxs-lookup"><span data-stu-id="16980-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-275">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-277">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Server 特定結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="16980-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="16980-278">服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="16980-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="16980-279">結束代碼是由這個類別所代表的服務所定義。</span><span class="sxs-lookup"><span data-stu-id="16980-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="16980-280">只有當 [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) 屬性值為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="16980-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="16980-281">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="16980-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-283">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-285">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Service Type" ) </span><span class="sxs-lookup"><span data-stu-id="16980-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="16980-286">為呼叫處理序所提供的服務類型。</span><span class="sxs-lookup"><span data-stu-id="16980-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="16980-287">值如下：</span><span class="sxs-lookup"><span data-stu-id="16980-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="16980-288">**核心驅動程式** ( 「核心驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="16980-289">**檔案系統驅動程式** ( 「檔案系統驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="16980-290">**介面卡** ( 「介面卡」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="16980-291">辨識 **器驅動程式** ( 「辨識器驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="16980-292">**自己的進程** ( 「自己的進程」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="16980-293">**共用進程** ( 「共用進程」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="16980-294">**互動式進程** ( 「互動式進程」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="16980-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16980-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="16980-296">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-297">**已開始**</span><span class="sxs-lookup"><span data-stu-id="16980-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-298">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="16980-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16980-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-300">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="16980-301">指出服務是否已啟動。</span><span class="sxs-lookup"><span data-stu-id="16980-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="16980-302">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="16980-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-306">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="16980-307">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="16980-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="16980-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**開機** ( 「開機」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="16980-309">作業系統載入器啟動的設備磁碟機 (只對驅動程式服務) 有效。</span><span class="sxs-lookup"><span data-stu-id="16980-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="16980-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="16980-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="16980-311">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="16980-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="16980-312">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="16980-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="16980-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="16980-314">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="16980-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="16980-315">即使使用者沒有登入，也會啟動自動服務。</span><span class="sxs-lookup"><span data-stu-id="16980-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="16980-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="16980-317">當進程呼叫 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="16980-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="16980-318">除非使用者登入並啟動這些服務，否則這些服務將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="16980-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16980-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="16980-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="16980-320">在 StartMode 變更為 Auto 或 Manual 之前無法啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="16980-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="16980-321">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="16980-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-325">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "起始帳戶名稱" ) </span><span class="sxs-lookup"><span data-stu-id="16980-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-326">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="16980-326">Account name under which a service runs.</span></span> <span data-ttu-id="16980-327">根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username" 或 UPN 格式 ( " *Username@DomainName* " ) 。</span><span class="sxs-lookup"><span data-stu-id="16980-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="16980-328">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="16980-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="16980-329">如果帳戶屬於內建網域，則為 "。 \\您可以指定使用者名稱」。</span><span class="sxs-lookup"><span data-stu-id="16980-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="16980-330">若為核心或系統層級的驅動程式， [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) 會包含驅動程式物件名稱 (也就是「 \\ FileSystem \\ Rdr」或「 \\ 驅動程式 Xns」，這是 \\ i/o 系統用來載入設備磁碟機的 ) 。</span><span class="sxs-lookup"><span data-stu-id="16980-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="16980-331">此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。</span><span class="sxs-lookup"><span data-stu-id="16980-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="16980-332">範例： "DWDOM \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="16980-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="16980-333">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-334">**State**</span><span class="sxs-lookup"><span data-stu-id="16980-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-335">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-336">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="16980-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="16980-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "State" ) </span><span class="sxs-lookup"><span data-stu-id="16980-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="16980-338">基底服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-338">Current state of the base service.</span></span>

<span data-ttu-id="16980-339">值如下：</span><span class="sxs-lookup"><span data-stu-id="16980-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="16980-340">**停止** ( 「已停止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="16980-341">**開始暫** 止 ( 「開始暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="16980-342">**停止暫** 止 ( 「停止暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="16980-343">**正在** 執行 ( 「正在執行」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="16980-344">**繼續暫** 止 ( 「繼續暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="16980-345">**暫停暫** 止 ( 「暫停暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="16980-346">**暫停** ( 「已暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16980-347">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="16980-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16980-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="16980-349">**Windows Server 2008 和 Windows Vista：** 在 Windows 7 和 Windows Server 2008 R2 之前，此屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="16980-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="16980-350">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-351">**狀態**</span><span class="sxs-lookup"><span data-stu-id="16980-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-354">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="16980-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="16980-355">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-355">Current status of the object.</span></span> <span data-ttu-id="16980-356">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="16980-357">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="16980-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="16980-358">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="16980-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="16980-359">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="16980-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="16980-360">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="16980-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="16980-361">值如下：</span><span class="sxs-lookup"><span data-stu-id="16980-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="16980-362">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="16980-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="16980-363">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="16980-364">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16980-365">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="16980-366">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="16980-367">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="16980-368">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="16980-369">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="16980-370">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="16980-371">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="16980-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="16980-372">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="16980-373">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="16980-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16980-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="16980-375">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="16980-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16980-376">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16980-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-377">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-379">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)」。CreationClassName ") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="16980-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-380">裝載這項服務的系統類型名稱。</span><span class="sxs-lookup"><span data-stu-id="16980-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="16980-381">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="16980-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-383">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16980-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16980-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-385">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)」。Name ") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="16980-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="16980-386">裝載此服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="16980-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="16980-387">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="16980-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="16980-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-389">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-391">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "標記識別項" ) </span><span class="sxs-lookup"><span data-stu-id="16980-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="16980-392">群組中此服務的唯一標記值。</span><span class="sxs-lookup"><span data-stu-id="16980-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="16980-393">值為 0 (零) 表示服務沒有標記。</span><span class="sxs-lookup"><span data-stu-id="16980-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="16980-394">標記可以用來排序載入順序群組內的服務啟動，方法是在位於下列位置的登錄中指定標記順序向量：</span><span class="sxs-lookup"><span data-stu-id="16980-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="16980-395">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="16980-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="16980-396">標記只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務進行評估。</span><span class="sxs-lookup"><span data-stu-id="16980-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="16980-397">這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。</span><span class="sxs-lookup"><span data-stu-id="16980-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="16980-398">**TotalSessions**</span><span class="sxs-lookup"><span data-stu-id="16980-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-399">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16980-401">目前伺服器上的會話總數。</span><span class="sxs-lookup"><span data-stu-id="16980-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="16980-402">這包括已連線和已中斷連線的會話。</span><span class="sxs-lookup"><span data-stu-id="16980-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="16980-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="16980-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16980-404">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="16980-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16980-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16980-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16980-406">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「估計的等候時間」 ) </span><span class="sxs-lookup"><span data-stu-id="16980-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="16980-407">暫止的啟動、停止、暫停或繼續作業所需的預估時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="16980-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="16980-408">經過指定的時間之後，服務會使用遞增的 [**檢查點**](/windows/desktop/CIMWin32Prov/win32-service)值或 **CurrentState** 中的變更，對 **>setservicestatus** 方法進行下一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="16980-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="16980-409">如果 **WaitHint** 所指定的時間量，且 **檢查點** 尚未遞增，或 **CurrentState** 尚未變更，服務控制管理員或服務控制程式會假設發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="16980-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="16980-410">這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="16980-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16980-411">備註</span><span class="sxs-lookup"><span data-stu-id="16980-411">Remarks</span></span>

<span data-ttu-id="16980-412">由於 **win32 \_ TerminalService** 類別是 [**win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別的子類別，因此類別會繼承 **win32 \_ 服務** 的所有屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="16980-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="16980-413">[**Win32 \_TerminalServiceSetting**](win32-terminalservicesetting.md)會與 **win32 \_ TerminalService** 相關聯，作為 [**win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **設定** 屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="16980-414">[**Win32 \_TSSessionDirectory**](win32-tssessiondirectory.md)會與 **win32 \_ TerminalService** 相關聯，作為 [**win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)關聯的 **設定** 屬性。</span><span class="sxs-lookup"><span data-stu-id="16980-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="16980-415">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="16980-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="16980-416">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="16980-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="16980-417">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="16980-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="16980-418">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="16980-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="16980-419">規格需求</span><span class="sxs-lookup"><span data-stu-id="16980-419">Requirements</span></span>



| <span data-ttu-id="16980-420">需求</span><span class="sxs-lookup"><span data-stu-id="16980-420">Requirement</span></span> | <span data-ttu-id="16980-421">值</span><span class="sxs-lookup"><span data-stu-id="16980-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16980-422">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16980-422">Minimum supported client</span></span><br/> | <span data-ttu-id="16980-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16980-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16980-424">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16980-424">Minimum supported server</span></span><br/> | <span data-ttu-id="16980-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16980-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16980-426">命名空間</span><span class="sxs-lookup"><span data-stu-id="16980-426">Namespace</span></span><br/>                | <span data-ttu-id="16980-427">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="16980-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="16980-428">MOF</span><span class="sxs-lookup"><span data-stu-id="16980-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16980-429"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="16980-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="16980-430">DLL</span><span class="sxs-lookup"><span data-stu-id="16980-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16980-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16980-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16980-432">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16980-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16980-433">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="16980-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="16980-434">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="16980-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="16980-435">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="16980-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="16980-436">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="16980-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="16980-437">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="16980-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

