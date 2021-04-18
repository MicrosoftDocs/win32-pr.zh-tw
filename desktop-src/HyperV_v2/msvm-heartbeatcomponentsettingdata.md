---
description: 代表已設定的信號服務狀態。
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Msvm_HeartbeatComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971439"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="8377c-103">Msvm \_ HeartbeatComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="8377c-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="8377c-104">代表已設定的信號服務狀態。</span><span class="sxs-lookup"><span data-stu-id="8377c-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="8377c-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8377c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8377c-106">語法</span><span class="sxs-lookup"><span data-stu-id="8377c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="8377c-107">成員</span><span class="sxs-lookup"><span data-stu-id="8377c-107">Members</span></span>

<span data-ttu-id="8377c-108">**Msvm \_ HeartbeatComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8377c-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8377c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8377c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8377c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8377c-110">Properties</span></span>

<span data-ttu-id="8377c-111">**Msvm \_ HeartbeatComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8377c-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8377c-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="8377c-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="8377c-115">The address of the resource.</span></span> <span data-ttu-id="8377c-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="8377c-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="8377c-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="8377c-121">**父** / **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="8377c-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="8377c-122">例如，如果父系是 PCI 控制器，則此屬性會指定此子裝置的 PCI 插槽。</span><span class="sxs-lookup"><span data-stu-id="8377c-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="8377c-123">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="8377c-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-127">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="8377c-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="8377c-128">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為「整合元件」。</span><span class="sxs-lookup"><span data-stu-id="8377c-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="8377c-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8377c-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-132">指出是否自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="8377c-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="8377c-133">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="8377c-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="8377c-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8377c-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-137">指出是否自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="8377c-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="8377c-138">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="8377c-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="8377c-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8377c-142">A short description of the object.</span></span> <span data-ttu-id="8377c-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，且一律設定為「心跳」。</span><span class="sxs-lookup"><span data-stu-id="8377c-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-144">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="8377c-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-145">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8377c-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8377c-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-147">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="8377c-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="8377c-148">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="8377c-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8377c-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-152">描述取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="8377c-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="8377c-153">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，且一律設定為 3 (虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="8377c-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="8377c-154">**說明**</span><span class="sxs-lookup"><span data-stu-id="8377c-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-157">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8377c-157">A description of the object.</span></span> <span data-ttu-id="8377c-158">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 心跳服務設定資料」。</span><span class="sxs-lookup"><span data-stu-id="8377c-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8377c-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-162">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8377c-162">A display name for the object.</span></span> <span data-ttu-id="8377c-163">這個屬性是從 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))繼承而來的，而且一律會設定為「心跳」。</span><span class="sxs-lookup"><span data-stu-id="8377c-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="8377c-164">變更這個屬性將會變更相關聯之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)衍生的 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8377c-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="8377c-165">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8377c-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8377c-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8377c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-169">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="8377c-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="8377c-170">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8377c-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8377c-171">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="8377c-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8377c-172">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="8377c-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8377c-173">**ErrorThreshold**</span><span class="sxs-lookup"><span data-stu-id="8377c-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8377c-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-176">系統管理員的啟動設定，適用于已啟用的元素狀態。</span><span class="sxs-lookup"><span data-stu-id="8377c-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8377c-177">此屬性一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="8377c-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="8377c-178">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8377c-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-179">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="8377c-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-180">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8377c-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8377c-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-182">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="8377c-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="8377c-183">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8377c-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8377c-187">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="8377c-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8377c-188">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8377c-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8377c-189">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。</span><span class="sxs-lookup"><span data-stu-id="8377c-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-190">**間隔**</span><span class="sxs-lookup"><span data-stu-id="8377c-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-191">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8377c-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-193">Ping 嘗試之間的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8377c-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="8377c-194">這一律會設定為2000。</span><span class="sxs-lookup"><span data-stu-id="8377c-194">This is always set to 2000.</span></span>

<span data-ttu-id="8377c-195">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8377c-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-196">**延遲**</span><span class="sxs-lookup"><span data-stu-id="8377c-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8377c-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-199">在指定要求被捨棄之前，要求偵測和回應之間的最大預期延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8377c-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="8377c-200">此屬性一律設定為1000。</span><span class="sxs-lookup"><span data-stu-id="8377c-200">This property is always set to 1000.</span></span>

<span data-ttu-id="8377c-201">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8377c-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-202">**限制**</span><span class="sxs-lookup"><span data-stu-id="8377c-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8377c-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-205">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="8377c-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="8377c-206">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="8377c-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="8377c-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8377c-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-210">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="8377c-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="8377c-211">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="8377c-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-215">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 屬性的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="8377c-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="8377c-216">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為「Microsoft 心跳元件」。</span><span class="sxs-lookup"><span data-stu-id="8377c-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-217">**父系**</span><span class="sxs-lookup"><span data-stu-id="8377c-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-220">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="8377c-220">The parent of the resource.</span></span> <span data-ttu-id="8377c-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="8377c-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-225">從中配置資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="8377c-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="8377c-226">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8377c-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8377c-227">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="8377c-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8377c-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-230">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="8377c-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="8377c-231">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="8377c-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8377c-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-235">此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="8377c-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="8377c-236">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8377c-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8377c-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8377c-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-240">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8377c-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="8377c-241">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 類別，而且一律設定為 1 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="8377c-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="8377c-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8377c-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-243">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8377c-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-245">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="8377c-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="8377c-246">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="8377c-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8377c-247">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="8377c-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8377c-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-250">指定 **VirtualQuantity** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="8377c-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="8377c-251">例如，如果 ResourceType = Processor， **VirtualQuantityUnits** 屬性的值可以設定為 "count"，表示 **VirtualQuantity** 屬性的值會表示為計數。</span><span class="sxs-lookup"><span data-stu-id="8377c-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="8377c-252">如果 ResourceType = Memory， **VirtualQuantityUnits** 屬性的值可以設定為 "bytes \* 10 ^ 3"，表示 **VirtualQuantity** 屬性的值是以 kb 表示。</span><span class="sxs-lookup"><span data-stu-id="8377c-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="8377c-253">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 "count"。</span><span class="sxs-lookup"><span data-stu-id="8377c-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="8377c-254">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8377c-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377c-255">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8377c-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8377c-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8377c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8377c-257">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="8377c-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="8377c-258">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="8377c-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8377c-259">備註</span><span class="sxs-lookup"><span data-stu-id="8377c-259">Remarks</span></span>

<span data-ttu-id="8377c-260">存取 **Msvm \_ HeartbeatComponentSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="8377c-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8377c-261">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="8377c-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8377c-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="8377c-262">Requirements</span></span>



| <span data-ttu-id="8377c-263">需求</span><span class="sxs-lookup"><span data-stu-id="8377c-263">Requirement</span></span> | <span data-ttu-id="8377c-264">值</span><span class="sxs-lookup"><span data-stu-id="8377c-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8377c-265">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8377c-265">Minimum supported client</span></span><br/> | <span data-ttu-id="8377c-266">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8377c-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8377c-267">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8377c-267">Minimum supported server</span></span><br/> | <span data-ttu-id="8377c-268">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8377c-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8377c-269">命名空間</span><span class="sxs-lookup"><span data-stu-id="8377c-269">Namespace</span></span><br/>                | <span data-ttu-id="8377c-270">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8377c-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8377c-271">MOF</span><span class="sxs-lookup"><span data-stu-id="8377c-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8377c-272"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8377c-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8377c-273">DLL</span><span class="sxs-lookup"><span data-stu-id="8377c-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8377c-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8377c-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8377c-275">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8377c-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8377c-276">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="8377c-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="8377c-277">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="8377c-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="8377c-278">**Msvm \_ HeartbeatComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="8377c-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

