---
description: 表示虛擬系統移轉服務。 它是用來遷移虛擬系統，或將虛擬系統的儲存體從一個虛擬化平臺遷移到另一個虛擬化平臺。
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Msvm_VirtualSystemMigrationService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689755"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="6f05e-104">Msvm \_ VirtualSystemMigrationService 類別</span><span class="sxs-lookup"><span data-stu-id="6f05e-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="6f05e-105">表示虛擬系統移轉服務。</span><span class="sxs-lookup"><span data-stu-id="6f05e-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="6f05e-106">它是用來遷移虛擬系統，或將虛擬系統的儲存體從一個虛擬化平臺遷移到另一個虛擬化平臺。</span><span class="sxs-lookup"><span data-stu-id="6f05e-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="6f05e-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f05e-108">語法</span><span class="sxs-lookup"><span data-stu-id="6f05e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="6f05e-109">成員</span><span class="sxs-lookup"><span data-stu-id="6f05e-109">Members</span></span>

<span data-ttu-id="6f05e-110">**Msvm \_ VirtualSystemMigrationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f05e-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="6f05e-111">方法</span><span class="sxs-lookup"><span data-stu-id="6f05e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f05e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="6f05e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f05e-113">方法</span><span class="sxs-lookup"><span data-stu-id="6f05e-113">Methods</span></span>

<span data-ttu-id="6f05e-114">**Msvm \_ VirtualSystemMigrationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f05e-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="6f05e-115">方法</span><span class="sxs-lookup"><span data-stu-id="6f05e-115">Method</span></span>                                                                                                                  | <span data-ttu-id="6f05e-116">描述</span><span class="sxs-lookup"><span data-stu-id="6f05e-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f05e-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6f05e-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="6f05e-118">新增虛擬系統移轉服務的遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="6f05e-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6f05e-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="6f05e-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="6f05e-120">檢查相容性資訊是否與主控電腦系統相容。</span><span class="sxs-lookup"><span data-stu-id="6f05e-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="6f05e-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="6f05e-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="6f05e-122">方法，將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。</span><span class="sxs-lookup"><span data-stu-id="6f05e-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="6f05e-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="6f05e-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="6f05e-124">判斷指定的虛擬系統是否可以遷移至網路名稱或 IP 位址所指定的目標主機。</span><span class="sxs-lookup"><span data-stu-id="6f05e-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="6f05e-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="6f05e-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="6f05e-126">產生不透明的資料 blob，其中包含指定系統的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="6f05e-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="6f05e-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="6f05e-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="6f05e-128">取得虛擬機器或主機的相容性向量。</span><span class="sxs-lookup"><span data-stu-id="6f05e-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="6f05e-129">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="6f05e-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="6f05e-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="6f05e-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="6f05e-131">將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。</span><span class="sxs-lookup"><span data-stu-id="6f05e-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="6f05e-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="6f05e-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="6f05e-133">移動、遷移或重新置放虛擬系統至目標系統。</span><span class="sxs-lookup"><span data-stu-id="6f05e-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="6f05e-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6f05e-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="6f05e-135">修改虛擬系統移轉服務的遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="6f05e-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="6f05e-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f05e-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="6f05e-137">修改遷移服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="6f05e-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6f05e-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6f05e-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="6f05e-139">從虛擬系統移轉服務移除遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="6f05e-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6f05e-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6f05e-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="6f05e-141">要求狀態變更</span><span class="sxs-lookup"><span data-stu-id="6f05e-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="6f05e-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="6f05e-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="6f05e-143">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="6f05e-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="6f05e-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="6f05e-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="6f05e-145">停止服務。</span><span class="sxs-lookup"><span data-stu-id="6f05e-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="6f05e-146">屬性</span><span class="sxs-lookup"><span data-stu-id="6f05e-146">Properties</span></span>

<span data-ttu-id="6f05e-147">**Msvm \_ VirtualSystemMigrationService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f05e-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="6f05e-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6f05e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-151">目前正在遷移的儲存體數目。</span><span class="sxs-lookup"><span data-stu-id="6f05e-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="6f05e-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6f05e-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-155">目前正在進行的虛擬系統移轉數目。</span><span class="sxs-lookup"><span data-stu-id="6f05e-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6f05e-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-157">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f05e-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-159">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="6f05e-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="6f05e-160">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6f05e-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-161">**標題**</span><span class="sxs-lookup"><span data-stu-id="6f05e-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-164">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="6f05e-164">A short description of the object.</span></span> <span data-ttu-id="6f05e-165">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="6f05e-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6f05e-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-169">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="6f05e-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6f05e-170">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f05e-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f05e-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-175">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f05e-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6f05e-176">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualSystemMigrationService"。</span><span class="sxs-lookup"><span data-stu-id="6f05e-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-177">**說明**</span><span class="sxs-lookup"><span data-stu-id="6f05e-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-180">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="6f05e-180">A description of the object.</span></span> <span data-ttu-id="6f05e-181">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="6f05e-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6f05e-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-185">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f05e-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6f05e-186">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f05e-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6f05e-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-191">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6f05e-191">A display name for the object.</span></span> <span data-ttu-id="6f05e-192">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="6f05e-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6f05e-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-196">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6f05e-197">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6f05e-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-201">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6f05e-202">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="6f05e-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6f05e-203">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6f05e-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-207">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="6f05e-207">The current health of the element.</span></span> <span data-ttu-id="6f05e-208">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="6f05e-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6f05e-209">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f05e-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6f05e-210">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f05e-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-212">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6f05e-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-214">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6f05e-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6f05e-215">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f05e-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-219">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="6f05e-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-220">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6f05e-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6f05e-221">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f05e-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="6f05e-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-223">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f05e-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-225">可用於虛擬系統移轉的主機 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="6f05e-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-226">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6f05e-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-229">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="6f05e-229">The label by which the object is known.</span></span> <span data-ttu-id="6f05e-230">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "migrationwmi"。</span><span class="sxs-lookup"><span data-stu-id="6f05e-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6f05e-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-232">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-234">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f05e-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6f05e-235">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f05e-236">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6f05e-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-238">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f05e-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-240">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-240">The current statuses of the object.</span></span> <span data-ttu-id="6f05e-241">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6f05e-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-245">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="6f05e-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6f05e-246">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6f05e-247">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f05e-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="6f05e-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-251">值，提供有關如何聯繫服務主要擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="6f05e-252">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f05e-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="6f05e-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-256">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="6f05e-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="6f05e-257">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="6f05e-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="6f05e-258">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f05e-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6f05e-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-260">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-262">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="6f05e-262">Provides high level status information.</span></span> <span data-ttu-id="6f05e-263">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6f05e-264">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f05e-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f05e-265">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6f05e-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-269">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="6f05e-270">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="6f05e-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6f05e-271">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6f05e-272">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="6f05e-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="6f05e-273">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="6f05e-274">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-275">**已開始**</span><span class="sxs-lookup"><span data-stu-id="6f05e-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-276">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f05e-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-278">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="6f05e-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="6f05e-279">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="6f05e-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-283">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="6f05e-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="6f05e-284">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f05e-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-285">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6f05e-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="6f05e-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6f05e-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-290">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f05e-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-292">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="6f05e-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6f05e-293">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，字串一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="6f05e-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f05e-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-297">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="6f05e-297">The scoping system's creation class name.</span></span> <span data-ttu-id="6f05e-298">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6f05e-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6f05e-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f05e-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-302">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f05e-302">The name of the hosting computer system.</span></span> <span data-ttu-id="6f05e-303">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="6f05e-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6f05e-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-305">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6f05e-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-307">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="6f05e-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6f05e-308">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6f05e-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f05e-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6f05e-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f05e-310">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f05e-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f05e-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f05e-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f05e-312">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="6f05e-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6f05e-313">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6f05e-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f05e-314">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f05e-314">Requirements</span></span>



| <span data-ttu-id="6f05e-315">需求</span><span class="sxs-lookup"><span data-stu-id="6f05e-315">Requirement</span></span> | <span data-ttu-id="6f05e-316">值</span><span class="sxs-lookup"><span data-stu-id="6f05e-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f05e-317">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f05e-317">Minimum supported client</span></span><br/> | <span data-ttu-id="6f05e-318">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f05e-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f05e-319">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f05e-319">Minimum supported server</span></span><br/> | <span data-ttu-id="6f05e-320">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f05e-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f05e-321">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f05e-321">Namespace</span></span><br/>                | <span data-ttu-id="6f05e-322">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f05e-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f05e-323">MOF</span><span class="sxs-lookup"><span data-stu-id="6f05e-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f05e-324"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6f05e-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f05e-325">DLL</span><span class="sxs-lookup"><span data-stu-id="6f05e-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f05e-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f05e-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

