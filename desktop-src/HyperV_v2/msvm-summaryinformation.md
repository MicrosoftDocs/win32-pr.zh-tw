---
description: 用於 Msvm VirtualSystemManagementService 類別中的 GetSummaryInformation 和 GetDefinitionFileSummaryInformation 方法 \_ ，以快速取得與虛擬機器或快照集相關的一般資訊。
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980949"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="a5291-103">Msvm \_ SummaryInformation 類別</span><span class="sxs-lookup"><span data-stu-id="a5291-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="a5291-104">用於 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別中的 [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)和 [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md)方法，以快速取得與虛擬機器或快照集相關的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="a5291-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="a5291-105">下列語法已簡化受控物件格式 (MOF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5291-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5291-106">語法</span><span class="sxs-lookup"><span data-stu-id="a5291-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="a5291-107">成員</span><span class="sxs-lookup"><span data-stu-id="a5291-107">Members</span></span>

<span data-ttu-id="a5291-108">**Msvm \_ SummaryInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a5291-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="a5291-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a5291-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5291-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a5291-110">Properties</span></span>

<span data-ttu-id="a5291-111">**Msvm \_ SummaryInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5291-112">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="a5291-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-115">實體圖形處理單元的識別碼 (GPU) 配置給此虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5291-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="a5291-116">這個屬性只適用于使用 RemoteFX 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5291-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-117">**ApplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="a5291-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-120">虛擬機器目前的應用程式健康情況狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="a5291-121">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a5291-122">**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="a5291-123">**應用程式關鍵性** (32782) </span><span class="sxs-lookup"><span data-stu-id="a5291-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a5291-124">**停用** (32896) </span><span class="sxs-lookup"><span data-stu-id="a5291-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-125">**AsynchronousTasks**</span><span class="sxs-lookup"><span data-stu-id="a5291-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-126">資料類型： **CIM \_ ConcreteJob** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-128">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-129">[**Msvm \_ ConcreteJob**](msvm-concretejob.md)實例的陣列，代表與目前正在執行之虛擬機器相關的任何非同步作業。</span><span class="sxs-lookup"><span data-stu-id="a5291-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="a5291-130">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-131">**AvailableMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="a5291-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5291-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-134">虛擬機器的可用記憶體緩衝區百分比。</span><span class="sxs-lookup"><span data-stu-id="a5291-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="a5291-135">當虛擬機器啟用動態記憶體時，此屬性會表示可用記憶體緩衝區與虛擬機器理想記憶體緩衝區的比率。</span><span class="sxs-lookup"><span data-stu-id="a5291-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="a5291-136">理想的記憶體緩衝區大小是使用 [**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md)類別的 **TargetMemoryBuffer** 屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="a5291-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="a5291-137">對於代表未啟用動態記憶體之虛擬機器的 **Msvm \_ SummaryInformation** 類別實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="a5291-138">這個屬性對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 類別的實例而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="a5291-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-140">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a5291-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-142">建立虛擬機器或快照集的時間。</span><span class="sxs-lookup"><span data-stu-id="a5291-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a5291-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-146">虛擬機器或快照的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a5291-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a5291-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-150">虛擬機器或快照的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="a5291-151">如需可能的值，請參閱 Msvm 非程式類型類別的 **EnabledState** 屬性。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="a5291-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-152">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="a5291-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-155">指出主機是否允許增強模式連接，以及是否允許虛擬機器使用。</span><span class="sxs-lookup"><span data-stu-id="a5291-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="a5291-156">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a5291-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="a5291-157">**允許和可用** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="a5291-158">**不允許** (3) </span><span class="sxs-lookup"><span data-stu-id="a5291-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="a5291-159">**允許但無法使用** (6 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-160">**GuestOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a5291-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-163">客體作業系統的名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a5291-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="a5291-164">如果無法使用這項資訊，則此屬性的值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a5291-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="a5291-165">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a5291-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-169">虛擬機器目前的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="a5291-170">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-171">**活動訊號**</span><span class="sxs-lookup"><span data-stu-id="a5291-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-174">虛擬機器目前的信號狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="a5291-175">如需詳細資訊，請參閱 **Msvm \_ HeartbeatComponent** 類別的 [**StatusDescriptions**](msvm-heartbeatcomponent.md)屬性檔。</span><span class="sxs-lookup"><span data-stu-id="a5291-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="a5291-176">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="a5291-177"><span id="OK"></span><span id="ok"></span>**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5291-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="a5291-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a5291-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) </span><span class="sxs-lookup"><span data-stu-id="a5291-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a5291-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) </span><span class="sxs-lookup"><span data-stu-id="a5291-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5291-181">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="a5291-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-184">裝載此虛擬機器的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a5291-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-185">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5291-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-189">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. InstanceID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5291-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a5291-190">InstanceID 是選擇性屬性，可在具現化命名空間的範圍內，用來以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a5291-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="a5291-191">此類別的各種子類別可覆寫這個屬性，使其成為必要或索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5291-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="a5291-192">這類子類別也可以修改慣用的演算法，以確保以下定義的唯一性。</span><span class="sxs-lookup"><span data-stu-id="a5291-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="a5291-193">為確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立：</span><span class="sxs-lookup"><span data-stu-id="a5291-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="a5291-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="a5291-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="a5291-195">Where <OrgID> 和 <LocalID> 會以冒號分隔 (： ) ，其中 <OrgID> 必須包含受著作權、商標或其他唯一的名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5291-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="a5291-196"> (這項需求類似于 <Schema Name> \_ <Class Name> 架構類別名稱的結構。此外，) 此外，為了確保唯一性， <OrgID> 不能包含冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="a5291-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="a5291-197">使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 <OrgID> 和之間 <LocalID> 。</span><span class="sxs-lookup"><span data-stu-id="a5291-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="a5291-198"><LocalID> 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。</span><span class="sxs-lookup"><span data-stu-id="a5291-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="a5291-199">如果不是 null，而且未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。</span><span class="sxs-lookup"><span data-stu-id="a5291-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="a5291-200">如果未針對 DMTF 定義的實例將設定為 null，就必須使用「慣用」演算法搭配 <OrgID> 將設定為 CIM。</span><span class="sxs-lookup"><span data-stu-id="a5291-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-201">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-202">**IntegrationServicesVersionState**</span><span class="sxs-lookup"><span data-stu-id="a5291-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-205">指出安裝在虛擬機器中的 integration services 是否為最新狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5291-206">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="a5291-207">**UpToDate** (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="a5291-208"> (2) **不符**</span><span class="sxs-lookup"><span data-stu-id="a5291-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-209">**MemoryAvailable**</span><span class="sxs-lookup"><span data-stu-id="a5291-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-210">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5291-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-212">虛擬機器目前可用記憶體的百分比。</span><span class="sxs-lookup"><span data-stu-id="a5291-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="a5291-213">當虛擬機器啟用動態記憶體時，此屬性會代表虛擬機器的可用記憶體與指派給虛擬機器的實體記憶體總計的比率。</span><span class="sxs-lookup"><span data-stu-id="a5291-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="a5291-214">當虛擬機器沒有可用的記憶體時，這個屬性會是負數，而且會包含虛擬機器所需的記憶體與指派給虛擬機器的總實體記憶體的比率。</span><span class="sxs-lookup"><span data-stu-id="a5291-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="a5291-215">對於代表未啟用動態記憶體之虛擬機器的 **Msvm \_ SummaryInformation** 類別實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="a5291-216">這個屬性對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 類別的實例而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-217">**MemorySpansPhysicalNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="a5291-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-218">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a5291-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-220">指出虛擬機器的一或多個虛擬非統一記憶體存取 (NUMA) 節點的記憶體是否跨越裝載電腦系統的多個實體 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="a5291-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="a5291-221">如果記憶體跨越多個實體 NUMA 節點，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="a5291-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="a5291-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-223">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a5291-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-225">虛擬機器目前的記憶體使用量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5291-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="a5291-226">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-227">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a5291-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-230">虛擬機器或快照的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a5291-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-231">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="a5291-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-234">與虛擬機器或快照集相關的附注。</span><span class="sxs-lookup"><span data-stu-id="a5291-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="a5291-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-236">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-238">配置給虛擬機器或快照集的虛擬處理器總數。</span><span class="sxs-lookup"><span data-stu-id="a5291-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a5291-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-240">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-242">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-243">虛擬機器目前的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="a5291-244">如需可能的值，請參閱 Msvm 非程式類型類別的 **OperationalStatus** 屬性。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="a5291-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-245">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a5291-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-248">字串，描述當 **EnabledState** 屬性設定為1時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="a5291-249">當 **EnabledState** 是1以外的任何值時，這個屬性會設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a5291-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-250">**ProcessorLoad**</span><span class="sxs-lookup"><span data-stu-id="a5291-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-251">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-253">虛擬機器目前的處理器使用量（以百分比為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5291-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="a5291-254">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-255">**ProcessorLoadHistory**</span><span class="sxs-lookup"><span data-stu-id="a5291-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-256">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-258">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-259">虛擬機器之處理器使用量的先前100範例陣列（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="a5291-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="a5291-260">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="a5291-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-264">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "**Msvm \_ SummaryInformation**.**ReplicationHealthEx**") </span><span class="sxs-lookup"><span data-stu-id="a5291-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-265">虛擬機器的複寫健全狀況。</span><span class="sxs-lookup"><span data-stu-id="a5291-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="a5291-266">如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationHealth** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-267">從 Windows 8.1 開始，這個屬性已被取代。相反地，請使用 **ReplicationHealthEx**。</span><span class="sxs-lookup"><span data-stu-id="a5291-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a5291-268">**不適用** (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="a5291-269">**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a5291-270">**警告** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5291-271">**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="a5291-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-272">**ReplicationHealthEx**</span><span class="sxs-lookup"><span data-stu-id="a5291-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-273">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-275">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-276">虛擬機器的各種複寫關聯性的複寫健全狀況值陣列。</span><span class="sxs-lookup"><span data-stu-id="a5291-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="a5291-277">如需可能的值，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationHealth** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a5291-278">**不適用** (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="a5291-279">**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a5291-280">**警告** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5291-281">**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="a5291-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="a5291-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-285">虛擬機器的複寫類型。</span><span class="sxs-lookup"><span data-stu-id="a5291-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="a5291-286">如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationMode** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a5291-287">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="a5291-288">**主要** (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="a5291-289">**複本** (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="a5291-290">**測試複本** (3) </span><span class="sxs-lookup"><span data-stu-id="a5291-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="a5291-291">**擴充複本** (4) </span><span class="sxs-lookup"><span data-stu-id="a5291-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="a5291-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-293">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-295">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-296">針對主要或擴展複本虛擬機器，這是主要複寫提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5291-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="a5291-297">若為複本虛擬機器，而且如果已啟用延伸複寫，這就是延伸關聯性的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5291-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="a5291-298">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a5291-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="a5291-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-300">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-302">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "**Msvm \_ SummaryInformation**.**ReplicationStateEx**") </span><span class="sxs-lookup"><span data-stu-id="a5291-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-303">虛擬機器的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="a5291-304">如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationState** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-305">從 Windows 8.1 開始，這個屬性已被取代。相反地，請使用 **ReplicationStateEx**。</span><span class="sxs-lookup"><span data-stu-id="a5291-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a5291-306">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="a5291-307">**準備好** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="a5291-308">**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="a5291-309">複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="a5291-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="a5291-310">**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="a5291-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="a5291-311">已 **復原** (5) </span><span class="sxs-lookup"><span data-stu-id="a5291-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="a5291-312">**認可** (6) </span><span class="sxs-lookup"><span data-stu-id="a5291-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="a5291-313">已 **暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="a5291-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5291-314">**重大** (8) </span><span class="sxs-lookup"><span data-stu-id="a5291-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="a5291-315">**等候啟動重新同步** (9) </span><span class="sxs-lookup"><span data-stu-id="a5291-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="a5291-316">重新 **同步** 處理 (10) </span><span class="sxs-lookup"><span data-stu-id="a5291-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="a5291-317">**重新同步** 處理已暫停 (11) </span><span class="sxs-lookup"><span data-stu-id="a5291-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="a5291-318">**正在進行容錯移轉** (12) </span><span class="sxs-lookup"><span data-stu-id="a5291-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-319">**ReplicationStateEx**</span><span class="sxs-lookup"><span data-stu-id="a5291-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-320">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-322">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-323">虛擬機器的各種複寫關聯性的複寫狀態值陣列。</span><span class="sxs-lookup"><span data-stu-id="a5291-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="a5291-324">如需可能的值，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a5291-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="a5291-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="a5291-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**準備好** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="a5291-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="a5291-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="a5291-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="a5291-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="a5291-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="a5291-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="a5291-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="a5291-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>已 **復原** (5) </span><span class="sxs-lookup"><span data-stu-id="a5291-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="a5291-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**認可** (6) </span><span class="sxs-lookup"><span data-stu-id="a5291-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="a5291-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="a5291-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5291-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (8) </span><span class="sxs-lookup"><span data-stu-id="a5291-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="a5291-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**等候啟動重新同步** (9) </span><span class="sxs-lookup"><span data-stu-id="a5291-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="a5291-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>重新 **同步** 處理 (10) </span><span class="sxs-lookup"><span data-stu-id="a5291-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="a5291-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**重新同步** 處理已暫停 (11) </span><span class="sxs-lookup"><span data-stu-id="a5291-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="a5291-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**正在進行容錯移轉** (12) </span><span class="sxs-lookup"><span data-stu-id="a5291-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="a5291-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**正在進行容錯回復** (13) </span><span class="sxs-lookup"><span data-stu-id="a5291-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="a5291-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>容錯 **回復完成** (14) </span><span class="sxs-lookup"><span data-stu-id="a5291-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="a5291-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**磁片更新進行中** (15) </span><span class="sxs-lookup"><span data-stu-id="a5291-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-341">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="a5291-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**磁片更新嚴重** (16) </span><span class="sxs-lookup"><span data-stu-id="a5291-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-343">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5291-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (17) </span><span class="sxs-lookup"><span data-stu-id="a5291-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-345">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="a5291-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**進行複寫的** 重設用途 (18) </span><span class="sxs-lookup"><span data-stu-id="a5291-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-347">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="a5291-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>已 **準備同步** 複寫 (19) </span><span class="sxs-lookup"><span data-stu-id="a5291-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-349">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="a5291-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**針對群組反向複寫做好準備** (20) </span><span class="sxs-lookup"><span data-stu-id="a5291-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-351">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="a5291-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill 進行中** (21) </span><span class="sxs-lookup"><span data-stu-id="a5291-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5291-353">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a5291-354">**受防護**</span><span class="sxs-lookup"><span data-stu-id="a5291-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-355">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a5291-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-357">指出是否已為虛擬機器設定防護。</span><span class="sxs-lookup"><span data-stu-id="a5291-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-358">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-359">**快照集**</span><span class="sxs-lookup"><span data-stu-id="a5291-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-360">資料類型： **CIM \_ VirtualSystemSettingData** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-362">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-363">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例的陣列，代表虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="a5291-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="a5291-364">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-365">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a5291-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-366">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-368">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-369">描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="a5291-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="a5291-370">這會對應到 [**Msvm \_**](msvm-computersystem.md)的 [ **StatusDescriptions** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5291-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-371">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="a5291-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-372">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a5291-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-374">指出第二層分頁是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="a5291-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="a5291-375">如果第二層分頁為使用中，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="a5291-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-376">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="a5291-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-377">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="a5291-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-379">參考代表虛擬機器之測試複本虛擬機器的 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例實例。</span><span class="sxs-lookup"><span data-stu-id="a5291-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="a5291-380">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-381">**ThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="a5291-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-382">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-384">限定詞： **OctetString**、 [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImageWidth**"，"**Msvm \_ SummaryInformation**。**ThumbnailImageHeight**") </span><span class="sxs-lookup"><span data-stu-id="a5291-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-385">陣列，其中包含 RGB565 格式之虛擬機器或快照的小型、縮圖大小的影像。</span><span class="sxs-lookup"><span data-stu-id="a5291-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-386">**ThumbnailImageHeight**</span><span class="sxs-lookup"><span data-stu-id="a5291-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-389">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImage**") </span><span class="sxs-lookup"><span data-stu-id="a5291-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-390">ThumbnailImage 屬性中影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5291-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-391">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="a5291-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-393">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5291-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-395">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImage**") </span><span class="sxs-lookup"><span data-stu-id="a5291-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-396">ThumbnailImage 屬性中影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5291-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="a5291-397">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-398">**99.99**</span><span class="sxs-lookup"><span data-stu-id="a5291-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-399">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a5291-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-401">虛擬機器上次開機之後的時間量。</span><span class="sxs-lookup"><span data-stu-id="a5291-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="a5291-402">對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。</span><span class="sxs-lookup"><span data-stu-id="a5291-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-403">**版本**</span><span class="sxs-lookup"><span data-stu-id="a5291-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-404">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-406">虛擬系統的版本，格式為「主要. 次要」，例如 "2.0"。</span><span class="sxs-lookup"><span data-stu-id="a5291-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="a5291-407">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="a5291-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5291-408">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="a5291-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-409">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a5291-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5291-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5291-411">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="a5291-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a5291-412">字串，指定虛擬機器所連接之虛擬交換器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a5291-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="a5291-413">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a5291-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a5291-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="a5291-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5291-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a5291-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5291-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5291-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5291-417">虛擬系統的子類型。</span><span class="sxs-lookup"><span data-stu-id="a5291-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="a5291-418">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a5291-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="a5291-419">**Microsoft： hyper-v：子類型： 1** () </span><span class="sxs-lookup"><span data-stu-id="a5291-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="a5291-420">**Microsoft： hyper-v：子類型： 2** () </span><span class="sxs-lookup"><span data-stu-id="a5291-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="a5291-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a5291-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a5291-422">備註</span><span class="sxs-lookup"><span data-stu-id="a5291-422">Remarks</span></span>

<span data-ttu-id="a5291-423">存取 **Msvm \_ SummaryInformation** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a5291-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a5291-424">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a5291-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5291-425">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5291-425">Requirements</span></span>



| <span data-ttu-id="a5291-426">需求</span><span class="sxs-lookup"><span data-stu-id="a5291-426">Requirement</span></span> | <span data-ttu-id="a5291-427">值</span><span class="sxs-lookup"><span data-stu-id="a5291-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5291-428">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5291-428">Minimum supported client</span></span><br/> | <span data-ttu-id="a5291-429">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5291-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a5291-430">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5291-430">Minimum supported server</span></span><br/> | <span data-ttu-id="a5291-431">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5291-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5291-432">命名空間</span><span class="sxs-lookup"><span data-stu-id="a5291-432">Namespace</span></span><br/>                | <span data-ttu-id="a5291-433">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a5291-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5291-434">MOF</span><span class="sxs-lookup"><span data-stu-id="a5291-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5291-435"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a5291-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5291-436">DLL</span><span class="sxs-lookup"><span data-stu-id="a5291-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5291-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5291-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5291-438">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5291-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5291-439">**Msvm \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="a5291-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="a5291-440">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="a5291-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

