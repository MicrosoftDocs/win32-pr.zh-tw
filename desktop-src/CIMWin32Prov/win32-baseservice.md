---
description: Win32 \_ BaseService ABSTRACT WMI 類別代表安裝在服務控制管理員所維護之登錄資料庫中的可執行物件。
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111372"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="8e7e9-103">Win32 \_ BaseService 類別</span><span class="sxs-lookup"><span data-stu-id="8e7e9-103">Win32\_BaseService class</span></span>

<span data-ttu-id="8e7e9-104">**Win32 \_ BaseService** abstract [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表安裝在服務控制管理員所維護之登錄資料庫中的可執行物件。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="8e7e9-105">與服務相關聯的可執行檔可以由開機程式或系統在開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="8e7e9-106">服務控制管理員也可以視需要啟動它。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="8e7e9-107">任何不是由特定使用者所擁有，而且提供電腦系統支援之功能介面的任何服務或進程，都是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="8e7e9-108">範例：在執行 Windows Server 的電腦系統上，動態主機設定通訊協定 (DHCP) 用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="8e7e9-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e7e9-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7e9-111">語法</span><span class="sxs-lookup"><span data-stu-id="8e7e9-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="8e7e9-112">成員</span><span class="sxs-lookup"><span data-stu-id="8e7e9-112">Members</span></span>

<span data-ttu-id="8e7e9-113">**Win32 \_ BaseService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e7e9-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="8e7e9-114">方法</span><span class="sxs-lookup"><span data-stu-id="8e7e9-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e7e9-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8e7e9-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e7e9-116">方法</span><span class="sxs-lookup"><span data-stu-id="8e7e9-116">Methods</span></span>

<span data-ttu-id="8e7e9-117">**Win32 \_ BaseService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="8e7e9-118">方法</span><span class="sxs-lookup"><span data-stu-id="8e7e9-118">Method</span></span>                                                                             | <span data-ttu-id="8e7e9-119">描述</span><span class="sxs-lookup"><span data-stu-id="8e7e9-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="8e7e9-120">**變更**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="8e7e9-121">修改服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="8e7e9-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="8e7e9-123">修改服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="8e7e9-124">**建立**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="8e7e9-125">建立新的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="8e7e9-126">**刪除**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="8e7e9-127">刪除現有的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="8e7e9-128">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="8e7e9-129">要求服務將其狀態更新至 service manager。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="8e7e9-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="8e7e9-131">嘗試將此服務置於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="8e7e9-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="8e7e9-133">嘗試將此服務置於繼續狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="8e7e9-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="8e7e9-135">嘗試將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="8e7e9-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="8e7e9-137">將服務置於已停止狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="8e7e9-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="8e7e9-139">嘗試將使用者定義的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="8e7e9-140">屬性</span><span class="sxs-lookup"><span data-stu-id="8e7e9-140">Properties</span></span>

<span data-ttu-id="8e7e9-141">**Win32 \_ BaseService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e7e9-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-145">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「服務接受暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-146">服務可以暫停。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-150">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "服務接受停止" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-151">可以停止服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-152">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-155">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-156">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-156">Short description of the object.</span></span>

<span data-ttu-id="8e7e9-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-161">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-162">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8e7e9-163">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8e7e9-164">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-165">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-168">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-169">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-169">Description of the object.</span></span>

<span data-ttu-id="8e7e9-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-174">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( [與桌面互動] ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-175">服務可以在桌面上建立 windows 或與 windows 通訊。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-179">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Display Name" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-180">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-180">Display name of the service.</span></span> <span data-ttu-id="8e7e9-181">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="8e7e9-182">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="8e7e9-183">**DisplayName** 的比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="8e7e9-184">條件約束：接受與 **Name** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="8e7e9-185">範例： "Atdisk"</span><span class="sxs-lookup"><span data-stu-id="8e7e9-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-189">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動失敗的嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-190">錯誤的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-190">Severity of the error.</span></span> <span data-ttu-id="8e7e9-191">服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-191">Service fails to start.</span></span> <span data-ttu-id="8e7e9-192">值指出如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="8e7e9-193">電腦系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="8e7e9-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-195">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="8e7e9-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-197">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="8e7e9-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-199">系統以最後一次的已知良好設定重新開機。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="8e7e9-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-201">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e7e9-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-203">未指定採取的動作。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7e9-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-207">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-208">定義啟動或停止服務時所遇到的任何問題。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="8e7e9-209">這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 **可見於 servicespecificexitcode** 屬性中取得。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="8e7e9-210">服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-212">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-214">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8e7e9-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-215">已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-215">Object was installed.</span></span> <span data-ttu-id="8e7e9-216">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8e7e9-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-218">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-221">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e7e9-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-222">服務的唯一識別碼，以提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="8e7e9-223">此功能在物件的 **Description** 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="8e7e9-224">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-226">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-228">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Path Name" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-229">執行服務之服務二進位檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="8e7e9-230">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」</span><span class="sxs-lookup"><span data-stu-id="8e7e9-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-231">**可見於 servicespecificexitcode**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-232">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-234">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Server 特定結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-235">服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="8e7e9-236">結束代碼是由這個類別所代表的服務所定義。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="8e7e9-237">只有當 **ExitCodeproperty** 值是 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-241">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Service Type" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-242">提供給呼叫進程的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="8e7e9-243">**核心驅動程式** ( 「核心驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="8e7e9-244">**檔案系統驅動程式** ( 「檔案系統驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="8e7e9-245">**介面卡** ( 「介面卡」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="8e7e9-246">辨識 **器驅動程式** ( 「辨識器驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="8e7e9-247">**自己的進程** ( 「自己的進程」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="8e7e9-248">**共用進程** ( 「共用進程」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="8e7e9-249">**互動式進程** ( 「互動式進程」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7e9-250">**已開始**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-253">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-254">服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-254">Service has been started.</span></span>

<span data-ttu-id="8e7e9-255">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-259">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "StartMode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "啟動模式" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-260">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="8e7e9-261">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="8e7e9-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**開機** ( 「開機」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-263">作業系統載入器啟動的設備磁碟機 (只對驅動程式服務) 有效。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="8e7e9-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-265">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="8e7e9-266">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="8e7e9-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-268">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="8e7e9-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-270">當進程呼叫 [**StartService**](startservice-method-in-class-win32-baseservice.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e7e9-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="8e7e9-272">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7e9-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-276">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "起始帳戶名稱" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-277">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-277">Account name under which the service runs.</span></span> <span data-ttu-id="8e7e9-278">根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username" 或 UPN 格式 (Username@DomainName) 。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="8e7e9-279">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="8e7e9-280">如果帳戶屬於內建網域，則為」。 \\您可以指定使用者名稱」。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="8e7e9-281">如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="8e7e9-282">若是核心或系統層級的驅動程式， **StartName** 會包含驅動程式物件名稱 (也就是 \\ FileSystem \\ Rdr 或 \\ 驅動程式 \\ Xns) ，) 系統會使用這些輸入和 (輸出來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="8e7e9-283">此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="8e7e9-284">範例： "DWDOM \\ Admin"。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-285">**State**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7e9-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-288">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "State" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-289">基底服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="8e7e9-290">**停止** ( 「已停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="8e7e9-291">**開始暫** 止 ( 「開始暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="8e7e9-292">**停止暫** 止 ( 「停止暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="8e7e9-293">**正在** 執行 ( 「正在執行」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="8e7e9-294">**繼續暫** 止 ( 「繼續暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="8e7e9-295">**暫停暫** 止 ( 「暫停暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8e7e9-296">**暫停** ( 「已暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e7e9-297">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="8e7e9-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e7e9-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="8e7e9-299">**Windows Server 2008 和 Windows Vista：** 這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-300">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-303">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-304">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-304">Current status of the object.</span></span> <span data-ttu-id="8e7e9-305">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8e7e9-306">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8e7e9-307">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e7e9-308">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e7e9-309">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e7e9-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e7e9-311">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8e7e9-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e7e9-312">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e7e9-313">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e7e9-314">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e7e9-315">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e7e9-316">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e7e9-317">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e7e9-318">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e7e9-319">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e7e9-320">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e7e9-321">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e7e9-322">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e7e9-323">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7e9-324">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-327">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="8e7e9-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-328">裝載這項服務的系統類型名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="8e7e9-329">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-333">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="8e7e9-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-334">裝載此服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="8e7e9-335">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7e9-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7e9-337">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7e9-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7e9-339">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "標記識別項" ) </span><span class="sxs-lookup"><span data-stu-id="8e7e9-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="8e7e9-340">群組中此服務的唯一標記值。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="8e7e9-341">值為 0 (零) 表示尚未指派標記給服務。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="8e7e9-342">您可以在位於： HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList 的登錄中指定標記順序向量，以使用標記在載入順序群組內排序服務星星設定。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="8e7e9-343">系統只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務來評估標記。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e7e9-344">備註</span><span class="sxs-lookup"><span data-stu-id="8e7e9-344">Remarks</span></span>

<span data-ttu-id="8e7e9-345">**Win32 \_ BaseService** 類別衍生自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7e9-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e7e9-346">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e7e9-346">Requirements</span></span>



| <span data-ttu-id="8e7e9-347">需求</span><span class="sxs-lookup"><span data-stu-id="8e7e9-347">Requirement</span></span> | <span data-ttu-id="8e7e9-348">值</span><span class="sxs-lookup"><span data-stu-id="8e7e9-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7e9-349">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e7e9-349">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7e9-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e7e9-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e7e9-351">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e7e9-351">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7e9-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e7e9-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e7e9-353">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e7e9-353">Namespace</span></span><br/>                | <span data-ttu-id="8e7e9-354">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e7e9-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e7e9-355">MOF</span><span class="sxs-lookup"><span data-stu-id="8e7e9-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e7e9-356"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e7e9-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e7e9-357">DLL</span><span class="sxs-lookup"><span data-stu-id="8e7e9-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e7e9-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e7e9-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e7e9-359">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e7e9-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7e9-360">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="8e7e9-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="8e7e9-361">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e7e9-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

