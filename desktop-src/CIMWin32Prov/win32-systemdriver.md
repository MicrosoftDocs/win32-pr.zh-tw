---
description: 代表基底服務的系統驅動程式。
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688879"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="05969-103">Win32 \_ >systemdriver 類別</span><span class="sxs-lookup"><span data-stu-id="05969-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="05969-104">**Win32 \_ >systemdriver** [WMI 類別](../wmisdk/retrieving-a-class.md)代表基底服務的系統驅動程式。</span><span class="sxs-lookup"><span data-stu-id="05969-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="05969-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="05969-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="05969-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="05969-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05969-107">語法</span><span class="sxs-lookup"><span data-stu-id="05969-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="05969-108">成員</span><span class="sxs-lookup"><span data-stu-id="05969-108">Members</span></span>

<span data-ttu-id="05969-109">**Win32 \_ >systemdriver** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="05969-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="05969-110">方法</span><span class="sxs-lookup"><span data-stu-id="05969-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="05969-111">屬性</span><span class="sxs-lookup"><span data-stu-id="05969-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05969-112">方法</span><span class="sxs-lookup"><span data-stu-id="05969-112">Methods</span></span>

<span data-ttu-id="05969-113">**Win32 \_ >systemdriver** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="05969-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="05969-114">方法</span><span class="sxs-lookup"><span data-stu-id="05969-114">Method</span></span>                                                                              | <span data-ttu-id="05969-115">描述</span><span class="sxs-lookup"><span data-stu-id="05969-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05969-116">**變更**</span><span class="sxs-lookup"><span data-stu-id="05969-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="05969-117">修改服務的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="05969-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="05969-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="05969-119">修改服務啟動模式的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="05969-120">**建立**</span><span class="sxs-lookup"><span data-stu-id="05969-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="05969-121">建立新服務的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="05969-122">**刪除**</span><span class="sxs-lookup"><span data-stu-id="05969-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="05969-123">刪除現有服務的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="05969-124">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="05969-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="05969-125">要求服務將其狀態更新為 service manager 的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="05969-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="05969-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="05969-127">嘗試將服務置於暫停狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="05969-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="05969-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="05969-129">嘗試將服務置於繼續狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="05969-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="05969-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="05969-131">嘗試將服務置於啟動狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="05969-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="05969-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="05969-133">將服務置於已停止狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="05969-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="05969-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="05969-135">嘗試傳送使用者定義控制項程式碼至服務的類別方法。</span><span class="sxs-lookup"><span data-stu-id="05969-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="05969-136">屬性</span><span class="sxs-lookup"><span data-stu-id="05969-136">Properties</span></span>

<span data-ttu-id="05969-137">**Win32 \_ >systemdriver** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="05969-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05969-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="05969-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05969-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05969-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-141">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「服務接受暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="05969-142">服務可以暫停。</span><span class="sxs-lookup"><span data-stu-id="05969-142">Service can be paused.</span></span>

<span data-ttu-id="05969-143">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="05969-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05969-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05969-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-147">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "服務接受停止" ) </span><span class="sxs-lookup"><span data-stu-id="05969-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="05969-148">可以停止服務。</span><span class="sxs-lookup"><span data-stu-id="05969-148">Service can be stopped.</span></span>

<span data-ttu-id="05969-149">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-150">**標題**</span><span class="sxs-lookup"><span data-stu-id="05969-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-153">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="05969-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="05969-154">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="05969-154">Short description of the object.</span></span>

<span data-ttu-id="05969-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05969-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-159">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="05969-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-160">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="05969-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="05969-161">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="05969-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="05969-162">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-163">**說明**</span><span class="sxs-lookup"><span data-stu-id="05969-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-166">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="05969-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="05969-167">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="05969-167">Description of the object.</span></span>

<span data-ttu-id="05969-168">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="05969-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05969-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05969-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-172">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( [與桌面互動] ) </span><span class="sxs-lookup"><span data-stu-id="05969-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="05969-173">這種服務可以在桌面上建立 windows 或與 windows 通訊。</span><span class="sxs-lookup"><span data-stu-id="05969-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="05969-174">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="05969-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-178">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Display Name" ) </span><span class="sxs-lookup"><span data-stu-id="05969-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-179">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="05969-179">Display name of the service.</span></span> <span data-ttu-id="05969-180">這個字串的最大長度為 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="05969-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="05969-181">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="05969-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="05969-182">**DisplayName** 比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="05969-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="05969-183">條件約束：接受與 **Name** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="05969-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="05969-184">範例： "Atdisk"</span><span class="sxs-lookup"><span data-stu-id="05969-184">Example: "Atdisk"</span></span>

<span data-ttu-id="05969-185">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="05969-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-189">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動失敗的嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="05969-190">當此服務在啟動期間無法啟動時的錯誤嚴重性。</span><span class="sxs-lookup"><span data-stu-id="05969-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="05969-191">此值表示如果發生失敗，啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="05969-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="05969-192">電腦系統會記錄所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="05969-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="05969-193">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="05969-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) </span><span class="sxs-lookup"><span data-stu-id="05969-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="05969-195">不通知使用者。</span><span class="sxs-lookup"><span data-stu-id="05969-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="05969-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="05969-197">通知使用者。</span><span class="sxs-lookup"><span data-stu-id="05969-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="05969-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="05969-199">使用上次的正確組態重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="05969-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="05969-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="05969-201">系統嘗試以正確的組態重新啟動。</span><span class="sxs-lookup"><span data-stu-id="05969-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05969-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="05969-203">失敗的原因不明。</span><span class="sxs-lookup"><span data-stu-id="05969-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05969-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="05969-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05969-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05969-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-207">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="05969-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="05969-208">定義啟動或停止服務時所遇到之任何問題的 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="05969-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="05969-209">這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 **可見於 servicespecificexitcode** 屬性中取得。</span><span class="sxs-lookup"><span data-stu-id="05969-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="05969-210">服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="05969-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="05969-211">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="05969-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-213">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="05969-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05969-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-215">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="05969-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="05969-216">已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="05969-216">Object was installed.</span></span> <span data-ttu-id="05969-217">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="05969-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="05969-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-219">**名稱**</span><span class="sxs-lookup"><span data-stu-id="05969-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-222">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="05969-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="05969-223">提供受管理功能指示的服務的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="05969-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="05969-224">這項功能在 [物件 **描述** ] 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="05969-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="05969-225">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="05969-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-229">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Path Name" ) </span><span class="sxs-lookup"><span data-stu-id="05969-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-230">執行服務之服務二進位檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="05969-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="05969-231">範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」</span><span class="sxs-lookup"><span data-stu-id="05969-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="05969-232">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-233">**可見於 servicespecificexitcode**</span><span class="sxs-lookup"><span data-stu-id="05969-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-234">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05969-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05969-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-236">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Server 特定結束代碼" ) </span><span class="sxs-lookup"><span data-stu-id="05969-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="05969-237">服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="05969-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="05969-238">結束代碼是由這個類別所代表的服務所定義。</span><span class="sxs-lookup"><span data-stu-id="05969-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="05969-239">只有當 **ExitCode** 屬性值為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="05969-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="05969-240">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="05969-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-244">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Service Type" ) </span><span class="sxs-lookup"><span data-stu-id="05969-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="05969-245">為呼叫處理序所提供的服務類型。</span><span class="sxs-lookup"><span data-stu-id="05969-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="05969-246">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="05969-247">值如下：</span><span class="sxs-lookup"><span data-stu-id="05969-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="05969-248">**核心驅動程式** ( 「核心驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="05969-249">**檔案系統驅動程式** ( 「檔案系統驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="05969-250">**介面卡** ( 「介面卡」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="05969-251">辨識 **器驅動程式** ( 「辨識器驅動程式」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="05969-252">**自己的進程** ( 「自己的進程」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="05969-253">**共用進程** ( 「共用進程」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="05969-254">**互動式進程** ( 「互動式進程」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05969-255">**已開始**</span><span class="sxs-lookup"><span data-stu-id="05969-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-256">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05969-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05969-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-258">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="05969-259">服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="05969-259">Service has been started.</span></span>

<span data-ttu-id="05969-260">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="05969-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-264">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="05969-265">系統驅動程式的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="05969-265">Start mode of the system driver.</span></span>

<span data-ttu-id="05969-266">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="05969-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**開機** ( 「開機」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="05969-268">作業系統載入器啟動的設備磁碟機 (只對驅動程式服務) 有效。</span><span class="sxs-lookup"><span data-stu-id="05969-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="05969-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="05969-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="05969-270">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05969-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="05969-271">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="05969-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="05969-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="05969-273">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="05969-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="05969-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="05969-275">當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="05969-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="05969-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="05969-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="05969-277">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="05969-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05969-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="05969-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-281">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "起始帳戶名稱" ) </span><span class="sxs-lookup"><span data-stu-id="05969-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-282">用來執行服務的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="05969-282">Account name under which the service runs.</span></span> <span data-ttu-id="05969-283">根據服務類型而定，帳戶名稱的格式可能是 DomainName \\ Username。</span><span class="sxs-lookup"><span data-stu-id="05969-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="05969-284">服務進程會在執行時使用這兩種形式的其中一種來記錄。</span><span class="sxs-lookup"><span data-stu-id="05969-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="05969-285">如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="05969-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="05969-286">如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。</span><span class="sxs-lookup"><span data-stu-id="05969-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="05969-287">若是核心或系統層級的驅動程式， **StartName** 會包含驅動程式物件名稱 (也就是 \\ FileSystem \\ Rdr 或 \\ 驅動程式 \\ Xns) ，) 系統會使用這些輸入和 (輸出來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05969-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="05969-288">此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。</span><span class="sxs-lookup"><span data-stu-id="05969-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="05969-289">範例： "DWDOM \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="05969-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="05969-290">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-291">**State**</span><span class="sxs-lookup"><span data-stu-id="05969-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="05969-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05969-294">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "State" ) </span><span class="sxs-lookup"><span data-stu-id="05969-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="05969-295">基底服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="05969-295">Current state of the base service.</span></span>

<span data-ttu-id="05969-296">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="05969-297">值如下：</span><span class="sxs-lookup"><span data-stu-id="05969-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="05969-298">**停止** ( 「已停止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="05969-299">**開始暫** 止 ( 「開始暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="05969-300">**停止暫** 止 ( 「停止暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="05969-301">**正在** 執行 ( 「正在執行」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="05969-302">**繼續暫** 止 ( 「繼續暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="05969-303">**暫停暫** 止 ( 「暫停暫止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="05969-304">**暫停** ( 「已暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05969-305">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05969-306">**狀態**</span><span class="sxs-lookup"><span data-stu-id="05969-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-309">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="05969-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="05969-310">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="05969-310">Current status of the object.</span></span> <span data-ttu-id="05969-311">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="05969-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="05969-312">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="05969-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="05969-313">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="05969-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="05969-314">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="05969-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="05969-315">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="05969-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="05969-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="05969-317">值如下：</span><span class="sxs-lookup"><span data-stu-id="05969-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="05969-318">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="05969-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="05969-319">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="05969-320">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05969-321">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="05969-322">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="05969-323">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="05969-324">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="05969-325">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="05969-326">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="05969-327">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="05969-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="05969-328">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="05969-329">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="05969-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05969-330">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05969-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-333">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="05969-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-334">裝載這項服務的系統類型名稱。</span><span class="sxs-lookup"><span data-stu-id="05969-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="05969-335">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="05969-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05969-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05969-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-339">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="05969-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="05969-340">裝載此服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="05969-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="05969-341">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="05969-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="05969-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05969-343">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05969-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05969-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05969-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05969-345">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "標記識別項" ) </span><span class="sxs-lookup"><span data-stu-id="05969-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="05969-346">群組中此服務的唯一標記值。</span><span class="sxs-lookup"><span data-stu-id="05969-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="05969-347">值為 0 (零) 表示尚未指派標記給服務。</span><span class="sxs-lookup"><span data-stu-id="05969-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="05969-348">標記可以用來排序載入順序群組內的服務啟動，方法是在位於下列位置的登錄中指定標記順序向量：</span><span class="sxs-lookup"><span data-stu-id="05969-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="05969-349">這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="05969-350">**HKEY \_本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項 \\ GroupOrderList**。</span><span class="sxs-lookup"><span data-stu-id="05969-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="05969-351">系統只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務來評估標記。</span><span class="sxs-lookup"><span data-stu-id="05969-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05969-352">備註</span><span class="sxs-lookup"><span data-stu-id="05969-352">Remarks</span></span>

<span data-ttu-id="05969-353">**Win32 \_ >systemdriver** 類別衍生自 [**win32 \_ BaseService**](win32-baseservice.md)。</span><span class="sxs-lookup"><span data-stu-id="05969-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="05969-354">範例</span><span class="sxs-lookup"><span data-stu-id="05969-354">Examples</span></span>

<span data-ttu-id="05969-355">[列出系統驅動程式](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141)VBScript 範例會在 HTML 檔案中顯示已安裝的系統驅動程式。</span><span class="sxs-lookup"><span data-stu-id="05969-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="05969-356">下列 PowerShell 範例會從電腦上的執行中系統驅動程式抓取許多屬性。</span><span class="sxs-lookup"><span data-stu-id="05969-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="05969-357">規格需求</span><span class="sxs-lookup"><span data-stu-id="05969-357">Requirements</span></span>



| <span data-ttu-id="05969-358">需求</span><span class="sxs-lookup"><span data-stu-id="05969-358">Requirement</span></span> | <span data-ttu-id="05969-359">值</span><span class="sxs-lookup"><span data-stu-id="05969-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05969-360">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05969-360">Minimum supported client</span></span><br/> | <span data-ttu-id="05969-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05969-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05969-362">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05969-362">Minimum supported server</span></span><br/> | <span data-ttu-id="05969-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05969-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05969-364">命名空間</span><span class="sxs-lookup"><span data-stu-id="05969-364">Namespace</span></span><br/>                | <span data-ttu-id="05969-365">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05969-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05969-366">MOF</span><span class="sxs-lookup"><span data-stu-id="05969-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05969-367"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="05969-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05969-368">DLL</span><span class="sxs-lookup"><span data-stu-id="05969-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05969-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05969-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05969-370">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05969-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05969-371">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="05969-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="05969-372">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="05969-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
