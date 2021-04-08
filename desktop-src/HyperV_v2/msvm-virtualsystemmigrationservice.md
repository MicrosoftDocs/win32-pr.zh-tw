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
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="4d15f-104">Msvm \_ VirtualSystemMigrationService 類別</span><span class="sxs-lookup"><span data-stu-id="4d15f-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="4d15f-105">表示虛擬系統移轉服務。</span><span class="sxs-lookup"><span data-stu-id="4d15f-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="4d15f-106">它是用來遷移虛擬系統，或將虛擬系統的儲存體從一個虛擬化平臺遷移到另一個虛擬化平臺。</span><span class="sxs-lookup"><span data-stu-id="4d15f-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="4d15f-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d15f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4d15f-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4d15f-109">成員</span><span class="sxs-lookup"><span data-stu-id="4d15f-109">Members</span></span>

<span data-ttu-id="4d15f-110">**Msvm \_ VirtualSystemMigrationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4d15f-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="4d15f-111">方法</span><span class="sxs-lookup"><span data-stu-id="4d15f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d15f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4d15f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d15f-113">方法</span><span class="sxs-lookup"><span data-stu-id="4d15f-113">Methods</span></span>

<span data-ttu-id="4d15f-114">**Msvm \_ VirtualSystemMigrationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4d15f-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="4d15f-115">方法</span><span class="sxs-lookup"><span data-stu-id="4d15f-115">Method</span></span>                                                                                                                  | <span data-ttu-id="4d15f-116">描述</span><span class="sxs-lookup"><span data-stu-id="4d15f-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d15f-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="4d15f-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="4d15f-118">新增虛擬系統移轉服務的遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="4d15f-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4d15f-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="4d15f-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="4d15f-120">檢查相容性資訊是否與主控電腦系統相容。</span><span class="sxs-lookup"><span data-stu-id="4d15f-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="4d15f-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="4d15f-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="4d15f-122">方法，將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。</span><span class="sxs-lookup"><span data-stu-id="4d15f-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="4d15f-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="4d15f-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="4d15f-124">判斷指定的虛擬系統是否可以遷移至網路名稱或 IP 位址所指定的目標主機。</span><span class="sxs-lookup"><span data-stu-id="4d15f-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="4d15f-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="4d15f-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="4d15f-126">產生不透明的資料 blob，其中包含指定系統的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="4d15f-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="4d15f-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="4d15f-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="4d15f-128">取得虛擬機器或主機的相容性向量。</span><span class="sxs-lookup"><span data-stu-id="4d15f-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="4d15f-129">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="4d15f-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="4d15f-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="4d15f-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="4d15f-131">將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。</span><span class="sxs-lookup"><span data-stu-id="4d15f-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="4d15f-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="4d15f-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="4d15f-133">移動、遷移或重新置放虛擬系統至目標系統。</span><span class="sxs-lookup"><span data-stu-id="4d15f-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="4d15f-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="4d15f-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="4d15f-135">修改虛擬系統移轉服務的遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="4d15f-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4d15f-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="4d15f-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="4d15f-137">修改遷移服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="4d15f-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="4d15f-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="4d15f-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="4d15f-139">從虛擬系統移轉服務移除遷移網路子網。</span><span class="sxs-lookup"><span data-stu-id="4d15f-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4d15f-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4d15f-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="4d15f-141">要求狀態變更</span><span class="sxs-lookup"><span data-stu-id="4d15f-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="4d15f-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4d15f-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="4d15f-143">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="4d15f-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="4d15f-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4d15f-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="4d15f-145">停止服務。</span><span class="sxs-lookup"><span data-stu-id="4d15f-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="4d15f-146">屬性</span><span class="sxs-lookup"><span data-stu-id="4d15f-146">Properties</span></span>

<span data-ttu-id="4d15f-147">**Msvm \_ VirtualSystemMigrationService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d15f-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="4d15f-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4d15f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-151">目前正在遷移的儲存體數目。</span><span class="sxs-lookup"><span data-stu-id="4d15f-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="4d15f-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4d15f-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-155">目前正在進行的虛擬系統移轉數目。</span><span class="sxs-lookup"><span data-stu-id="4d15f-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4d15f-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-157">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4d15f-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-159">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="4d15f-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4d15f-160">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4d15f-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-161">**標題**</span><span class="sxs-lookup"><span data-stu-id="4d15f-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-164">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4d15f-164">A short description of the object.</span></span> <span data-ttu-id="4d15f-165">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="4d15f-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4d15f-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-169">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="4d15f-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4d15f-170">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4d15f-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d15f-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-175">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d15f-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4d15f-176">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualSystemMigrationService"。</span><span class="sxs-lookup"><span data-stu-id="4d15f-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-177">**說明**</span><span class="sxs-lookup"><span data-stu-id="4d15f-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-180">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4d15f-180">A description of the object.</span></span> <span data-ttu-id="4d15f-181">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="4d15f-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4d15f-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-185">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4d15f-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4d15f-186">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4d15f-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4d15f-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-191">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4d15f-191">A display name for the object.</span></span> <span data-ttu-id="4d15f-192">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「hyper-v 遷移服務」。</span><span class="sxs-lookup"><span data-stu-id="4d15f-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4d15f-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-196">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4d15f-197">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4d15f-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-201">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4d15f-202">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="4d15f-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4d15f-203">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4d15f-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-207">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="4d15f-207">The current health of the element.</span></span> <span data-ttu-id="4d15f-208">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="4d15f-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4d15f-209">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4d15f-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4d15f-210">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4d15f-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-212">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4d15f-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-214">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4d15f-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4d15f-215">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4d15f-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-219">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="4d15f-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-220">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4d15f-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4d15f-221">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d15f-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="4d15f-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-223">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4d15f-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-225">可用於虛擬系統移轉的主機 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="4d15f-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-226">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4d15f-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-229">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4d15f-229">The label by which the object is known.</span></span> <span data-ttu-id="4d15f-230">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "migrationwmi"。</span><span class="sxs-lookup"><span data-stu-id="4d15f-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4d15f-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-232">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-234">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4d15f-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4d15f-235">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4d15f-236">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4d15f-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-238">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4d15f-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-240">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-240">The current statuses of the object.</span></span> <span data-ttu-id="4d15f-241">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4d15f-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-245">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="4d15f-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4d15f-246">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4d15f-247">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d15f-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4d15f-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-251">值，提供有關如何聯繫服務主要擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="4d15f-252">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d15f-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4d15f-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-256">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="4d15f-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="4d15f-257">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="4d15f-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="4d15f-258">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d15f-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4d15f-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-260">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-262">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4d15f-262">Provides high level status information.</span></span> <span data-ttu-id="4d15f-263">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4d15f-264">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d15f-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4d15f-265">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4d15f-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-269">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="4d15f-270">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="4d15f-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4d15f-271">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="4d15f-272">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="4d15f-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="4d15f-273">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="4d15f-274">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-275">**已開始**</span><span class="sxs-lookup"><span data-stu-id="4d15f-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-276">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4d15f-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-278">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="4d15f-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="4d15f-279">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4d15f-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-283">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="4d15f-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="4d15f-284">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d15f-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-285">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4d15f-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="4d15f-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4d15f-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-290">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4d15f-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-292">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="4d15f-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4d15f-293">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，字串一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="4d15f-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d15f-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-297">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4d15f-297">The scoping system's creation class name.</span></span> <span data-ttu-id="4d15f-298">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4d15f-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4d15f-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4d15f-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-302">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d15f-302">The name of the hosting computer system.</span></span> <span data-ttu-id="4d15f-303">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="4d15f-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4d15f-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-305">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4d15f-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-307">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="4d15f-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4d15f-308">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4d15f-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4d15f-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4d15f-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d15f-310">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4d15f-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d15f-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4d15f-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d15f-312">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="4d15f-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4d15f-313">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4d15f-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d15f-314">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d15f-314">Requirements</span></span>



| <span data-ttu-id="4d15f-315">需求</span><span class="sxs-lookup"><span data-stu-id="4d15f-315">Requirement</span></span> | <span data-ttu-id="4d15f-316">值</span><span class="sxs-lookup"><span data-stu-id="4d15f-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d15f-317">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d15f-317">Minimum supported client</span></span><br/> | <span data-ttu-id="4d15f-318">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d15f-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4d15f-319">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d15f-319">Minimum supported server</span></span><br/> | <span data-ttu-id="4d15f-320">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d15f-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d15f-321">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d15f-321">Namespace</span></span><br/>                | <span data-ttu-id="4d15f-322">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4d15f-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4d15f-323">MOF</span><span class="sxs-lookup"><span data-stu-id="4d15f-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d15f-324"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4d15f-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d15f-325">DLL</span><span class="sxs-lookup"><span data-stu-id="4d15f-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d15f-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d15f-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

