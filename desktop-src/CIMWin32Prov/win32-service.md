---
description: 代表執行 Windows 的電腦系統上的服務。
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025841"
---
# <a name="win32_service-class"></a><span data-ttu-id="4f4fc-103">Win32 \_ 服務類別</span><span class="sxs-lookup"><span data-stu-id="4f4fc-103">Win32\_Service class</span></span>

<span data-ttu-id="4f4fc-104">**Win32 \_ 服務** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="4f4fc-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4f4fc-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="4f4fc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="4f4fc-108">成員</span><span class="sxs-lookup"><span data-stu-id="4f4fc-108">Members</span></span>

<span data-ttu-id="4f4fc-109">**Win32 \_ 服務** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f4fc-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="4f4fc-110">方法</span><span class="sxs-lookup"><span data-stu-id="4f4fc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f4fc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4f4fc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f4fc-112">方法</span><span class="sxs-lookup"><span data-stu-id="4f4fc-112">Methods</span></span>

<span data-ttu-id="4f4fc-113">**Win32 \_ 服務** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="4f4fc-114">方法</span><span class="sxs-lookup"><span data-stu-id="4f4fc-114">Method</span></span>                                                                               | <span data-ttu-id="4f4fc-115">描述</span><span class="sxs-lookup"><span data-stu-id="4f4fc-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f4fc-116">**變更**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="4f4fc-117">修改服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="4f4fc-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="4f4fc-119">修改服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="4f4fc-120">**建立**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="4f4fc-121">建立新的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="4f4fc-122">**刪除**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="4f4fc-123">刪除現有的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="4f4fc-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="4f4fc-125">傳回控制服務存取的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="4f4fc-126">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="4f4fc-127">要求服務將其狀態更新至 service manager。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="4f4fc-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="4f4fc-129">嘗試將服務置於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="4f4fc-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="4f4fc-131">嘗試將服務放在恢復狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="4f4fc-132">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="4f4fc-133">寫入安全描述項的更新版本，以控制服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="4f4fc-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="4f4fc-135">嘗試將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="4f4fc-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="4f4fc-137">將服務置於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="4f4fc-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="4f4fc-139">嘗試將使用者定義的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="4f4fc-140">屬性</span><span class="sxs-lookup"><span data-stu-id="4f4fc-140">Properties</span></span>

<span data-ttu-id="4f4fc-141">**Win32 \_ 服務** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f4fc-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-145">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「服務接受暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-146">指出是否可以暫停服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="4f4fc-147">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-149">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-151">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "服務接受停止" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-152">指出是否可以停止服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="4f4fc-153">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-154">**標題**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-157">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-158">服務的簡短描述—單行字串。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="4f4fc-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-160">**檢查站**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-163">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**service \_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Check Point Count" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-164">此值會在長時間啟動、停止、暫停或繼續作業期間，定期遞增以報告其進度。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="4f4fc-165">例如，服務會在啟動時完成其初始化的每個步驟，以遞增此值。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="4f4fc-166">在服務上叫用作業的使用者介面程式會使用這個值，在冗長的作業期間追蹤服務的進度。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="4f4fc-167">此值無效，而且當服務沒有暫止的啟動、停止、暫停或繼續作業時，應該為零。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-171">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-172">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4f4fc-173">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4f4fc-174">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-176">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-178">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 延遲 \_ 自動 \_ 啟動 \_ 資訊**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| FDelayedAutostart" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「延遲的自動啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-179">若 **為 True**，則服務會在其他自動啟動服務啟動後加上短暫延遲之後啟動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="4f4fc-180">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-181">**說明**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-184">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-185">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-185">Description of the object.</span></span>

<span data-ttu-id="4f4fc-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-188">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-190">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( [與桌面互動] ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-191">指出服務是否可以在桌面上建立或與 windows 通訊，進而以某種方式與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="4f4fc-192">互動式服務必須在本機系統帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="4f4fc-193">大部分的服務都不是互動式的;也就是說，它們不會以任何方式與使用者通訊。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="4f4fc-194">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Display Name" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-199">在 [服務] 嵌入式管理單元中所看到的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="4f4fc-200">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4f4fc-201">請注意，儲存在登錄) 中的顯示名稱和服務名稱 (不一定相同。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="4f4fc-202">例如，DHCP 用戶端服務的服務名稱是 Dhcp，而是顯示名稱 DHCP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="4f4fc-203">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="4f4fc-204">不過， **DisplayName** 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4f4fc-205">Constraint：接受與 **Name** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="4f4fc-206">範例： "Atdisk"</span><span class="sxs-lookup"><span data-stu-id="4f4fc-206">Example: "Atdisk"</span></span>

<span data-ttu-id="4f4fc-207">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-211">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動失敗的嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-212">當此服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="4f4fc-213">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4f4fc-214">電腦系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="4f4fc-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-216">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="4f4fc-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-218">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-218">User is notified.</span></span> <span data-ttu-id="4f4fc-219">通常這會是顯示通知使用者問題的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="4f4fc-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-221">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4f4fc-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-223">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="4f4fc-224">如果服務無法第二次啟動，則啟動會失敗。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f4fc-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-226">錯誤的嚴重性未知。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="4f4fc-227">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-229">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-231">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-232">定義啟動或停止服務時所發生之錯誤的 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="4f4fc-233">這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 **可見於 servicespecificexitcode** 屬性中取得。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="4f4fc-234">服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="4f4fc-235">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-237">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-239">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4f4fc-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-240">已安裝日期物件。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-240">Date object is installed.</span></span> <span data-ttu-id="4f4fc-241">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4f4fc-242">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-243">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-246">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4f4fc-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-247">提供受管理功能指示的服務的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="4f4fc-248">這項功能會在物件的 **Description** 屬性中說明。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="4f4fc-249">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-253">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Path Name" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-254">執行服務之服務二進位檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="4f4fc-255">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」</span><span class="sxs-lookup"><span data-stu-id="4f4fc-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="4f4fc-256">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-257">**進程**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-258">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-260">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態 \_ 進程**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "處理序識別碼" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-261">服務的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-261">Process identifier of the service.</span></span>

<span data-ttu-id="4f4fc-262">範例：324</span><span class="sxs-lookup"><span data-stu-id="4f4fc-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-263">**可見於 servicespecificexitcode**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-266">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Server 特定結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-267">服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="4f4fc-268">結束代碼是由這個類別所代表的服務所定義。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="4f4fc-269">只有當 **ExitCode** 屬性值為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="4f4fc-270">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-274">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Service Type" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-275">為呼叫處理序所提供的服務類型。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="4f4fc-276">值如下：</span><span class="sxs-lookup"><span data-stu-id="4f4fc-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="4f4fc-277">**核心驅動程式** ( 「核心驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="4f4fc-278">**檔案系統驅動程式** ( 「檔案系統驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="4f4fc-279">**介面卡** ( 「介面卡」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="4f4fc-280">辨識 **器驅動程式** ( 「辨識器驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="4f4fc-281">**自己的進程** ( 「自己的進程」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="4f4fc-282">**共用進程** ( 「共用進程」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="4f4fc-283">**互動式進程** ( 「互動式進程」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="4f4fc-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4f4fc-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="4f4fc-285">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-286">**已開始**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-287">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-289">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-290">指出服務是否已啟動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="4f4fc-291">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-295">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-296">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4f4fc-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**開機** ( 「開機」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-298">作業系統載入器啟動的設備磁碟機 (只對驅動程式服務) 有效。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4f4fc-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-300">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4f4fc-301">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="4f4fc-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-303">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="4f4fc-304">即使使用者沒有登入，也會啟動自動服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4f4fc-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-306">當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="4f4fc-307">除非使用者登入並啟動這些服務，否則這些服務將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4f4fc-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="4f4fc-309">在 StartMode 變更為 Auto 或 Manual 之前無法啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="4f4fc-310">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-314">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "起始帳戶名稱" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-315">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-315">Account name under which a service runs.</span></span> <span data-ttu-id="4f4fc-316">根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username" 或 UPN 格式 ( " *Username@DomainName* " ) 。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="4f4fc-317">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="4f4fc-318">如果帳戶屬於內建網域，則為 "。 \\您可以指定使用者名稱」。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="4f4fc-319">若為核心或系統層級的驅動程式， **StartName** 會包含驅動程式物件名稱 (也就是「 \\ FileSystem \\ Rdr」或「 \\ 驅動程式 Xns」，這是 \\ i/o 系統用來載入設備磁碟機的 ) 。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="4f4fc-320">此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="4f4fc-321">範例： "DWDOM \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="4f4fc-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="4f4fc-322">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-323">**State**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-325">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4f4fc-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-326">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "State" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-327">基底服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-327">Current state of the base service.</span></span>

<span data-ttu-id="4f4fc-328">值如下：</span><span class="sxs-lookup"><span data-stu-id="4f4fc-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="4f4fc-329">**停止** ( 「已停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="4f4fc-330">**開始暫** 止 ( 「開始暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="4f4fc-331">**停止暫** 止 ( 「停止暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4f4fc-332">**正在** 執行 ( 「正在執行」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="4f4fc-333">**繼續暫** 止 ( 「繼續暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="4f4fc-334">**暫停暫** 止 ( 「暫停暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4f4fc-335">**暫停** ( 「已暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f4fc-336">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="4f4fc-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4f4fc-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="4f4fc-338">**Windows Server 2008 和 Windows Vista：** 在 Windows 7 和 Windows Server 2008 R2 之前，此屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="4f4fc-339">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-340">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-341">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-343">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-344">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-344">Current status of the object.</span></span> <span data-ttu-id="4f4fc-345">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4f4fc-346">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4f4fc-347">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4f4fc-348">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4f4fc-349">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4f4fc-350">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4f4fc-351">值如下：</span><span class="sxs-lookup"><span data-stu-id="4f4fc-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4f4fc-352">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4f4fc-353">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4f4fc-354">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f4fc-355">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4f4fc-356">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4f4fc-357">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4f4fc-358">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4f4fc-359">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4f4fc-360">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4f4fc-361">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4f4fc-362">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4f4fc-363">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f4fc-364">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-367">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="4f4fc-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-368">裝載這項服務的系統類型名稱。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="4f4fc-369">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-371">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-373">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="4f4fc-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-374">裝載此服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="4f4fc-375">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-377">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-379">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "標記識別項" ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-380">群組中此服務的唯一標記值。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="4f4fc-381">值為 0 (零) 表示服務沒有標記。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="4f4fc-382">標記可以用來排序載入順序群組內的服務啟動，方法是在位於下列位置的登錄中指定標記順序向量：</span><span class="sxs-lookup"><span data-stu-id="4f4fc-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="4f4fc-383">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="4f4fc-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="4f4fc-384">標記只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務進行評估。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="4f4fc-385">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-387">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f4fc-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-389">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「估計的等候時間」 ) </span><span class="sxs-lookup"><span data-stu-id="4f4fc-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-390">暫止的啟動、停止、暫停或繼續作業所需的預估時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="4f4fc-391">經過指定的時間之後，服務會使用遞增的 **檢查點** 值或 **CurrentState** 中的變更，對 **>setservicestatus** 方法進行下一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="4f4fc-392">如果 **WaitHint** 所指定的時間量，且 **檢查點** 尚未遞增，或 **CurrentState** 尚未變更，服務控制管理員或服務控制程式會假設發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f4fc-393">備註</span><span class="sxs-lookup"><span data-stu-id="4f4fc-393">Remarks</span></span>

<span data-ttu-id="4f4fc-394">**Win32 \_ 服務** 類別衍生自 [**win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="4f4fc-395">您管理特定電腦的方式，主要取決於電腦扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="4f4fc-396">例如，您通常會監視 DNS 伺服器與 DHCP 伺服器不同的層面。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="4f4fc-397">雖然沒有任何單一屬性可以告訴您特定電腦是資料庫伺服器、電子郵件伺服器還是多媒體伺服器，但您通常可以藉由識別電腦上所安裝的服務來識別電腦所扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="4f4fc-398">在大型組織中，一部電腦上只能安裝一個主要服務 (，例如電子郵件) 。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="4f4fc-399">郵件伺服器也會以 Microsoft® Windows Media®技術播放機檔案的伺服器形式執行，這是不尋常的。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="4f4fc-400">因此，識別電腦上所安裝的服務可協助識別電腦在網路中的角色。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="4f4fc-401">如果電腦上已安裝並執行 Microsoft® Exchange Server 服務，通常會將這部電腦視為郵件伺服器，因此通常是安全的。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="4f4fc-402">您可以使用 WMI **Win32 \_ 服務** 類別來列舉電腦上所安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="4f4fc-403">此外，您可以使用這個類別來判斷這些服務目前是否正在執行，並傳回該服務的任何其他必要資訊，以及其設定方式。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="4f4fc-404">服務應用程式會符合服務控制管理員 (SCM) 的介面規則，而且可由使用者在系統啟動時自動啟動，方法是透過服務控制台公用程式，或由使用 Windows API 內含服務功能的應用程式來啟動。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="4f4fc-405">當沒有任何使用者登入電腦時，便可啟動服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="4f4fc-406">從遠端電腦連接的使用者必須啟用 **SC \_ MANAGER \_ CONNECT** 許可權，才能列舉此類別。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="4f4fc-407">如需詳細資訊，請參閱 [服務安全性和存取權限](../services/service-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4f4fc-408">範例</span><span class="sxs-lookup"><span data-stu-id="4f4fc-408">Examples</span></span>

<span data-ttu-id="4f4fc-409">在 TechNet 元件庫上的 PowerShell 範例中，傳回服務「狀態」的 [PS-WMI 查詢會](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) 使用 **Win32 \_ 服務** ，從 Active Directory 建立裝置清單，然後查詢每個 pingfor 特定服務執行回應的裝置。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="4f4fc-410">TechNet 元件庫上的 [伺服器報表](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell 範例會使用 **Win32 \_ 服務** 來收集伺服器資訊，並在 Word 檔中發行。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="4f4fc-411">下列 VBScript 程式碼範例會顯示所有目前已安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="4f4fc-412">下列 VBScript 程式碼範例說明指定電腦上已暫停、正在執行和已停止的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="4f4fc-413">下列 Perl 腳本示範如何從 **Win32 \_ 服務** 的實例取得執行中服務的清單。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="4f4fc-414">下列 c \# 範例會使用 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 來取得本機電腦上所有執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="4f4fc-415">下列 C 程式 \# 代碼範例會使用 [系統管理](/dotnet/api/system.management) 命名空間，以抓取本機電腦上所有執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="4f4fc-416">[系統管理](/dotnet/api/system.management) 包含用來存取 WMI 的原始類別;不過，它們會被視為較慢，而且通常不會進行調整，而且也不會調整其 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 的對應專案。</span><span class="sxs-lookup"><span data-stu-id="4f4fc-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="4f4fc-417">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f4fc-417">Requirements</span></span>



| <span data-ttu-id="4f4fc-418">需求</span><span class="sxs-lookup"><span data-stu-id="4f4fc-418">Requirement</span></span> | <span data-ttu-id="4f4fc-419">值</span><span class="sxs-lookup"><span data-stu-id="4f4fc-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4fc-420">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f4fc-420">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4fc-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f4fc-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f4fc-422">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f4fc-422">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4fc-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f4fc-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f4fc-424">命名空間</span><span class="sxs-lookup"><span data-stu-id="4f4fc-424">Namespace</span></span><br/>                | <span data-ttu-id="4f4fc-425">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4f4fc-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f4fc-426">MOF</span><span class="sxs-lookup"><span data-stu-id="4f4fc-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f4fc-427"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f4fc-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f4fc-428">DLL</span><span class="sxs-lookup"><span data-stu-id="4f4fc-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4fc-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f4fc-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4fc-430">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f4fc-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4fc-431">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="4f4fc-432">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="4f4fc-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4f4fc-433">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="4f4fc-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
