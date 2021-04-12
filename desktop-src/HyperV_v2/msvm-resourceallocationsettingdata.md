---
description: 代表虛擬資源目前和記錄的配置狀態。
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Msvm_ResourceAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319396"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="3e1ac-103">Msvm \_ ResourceAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="3e1ac-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="3e1ac-104">代表虛擬資源目前和記錄的配置狀態。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="3e1ac-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="3e1ac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="3e1ac-107">成員</span><span class="sxs-lookup"><span data-stu-id="3e1ac-107">Members</span></span>

<span data-ttu-id="3e1ac-108">**Msvm \_ ResourceAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e1ac-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3e1ac-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3e1ac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e1ac-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3e1ac-110">Properties</span></span>

<span data-ttu-id="3e1ac-111">**Msvm \_ ResourceAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e1ac-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-115">The address of the resource.</span></span> <span data-ttu-id="3e1ac-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3e1ac-117">這是唯讀屬性，但是如果 **ResourceType** 屬性是 20 (圖形控制器) ，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-121">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="3e1ac-122">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="3e1ac-123">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-127">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="3e1ac-128">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-132">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="3e1ac-133">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-137">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="3e1ac-138">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-142">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-143">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-143">A short description of the object.</span></span> <span data-ttu-id="3e1ac-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-145">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-146">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3e1ac-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-148">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-148">The device to which this resource is connected.</span></span> <span data-ttu-id="3e1ac-149">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3e1ac-150">這是一個唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-150">This is a read-only property.</span></span> <span data-ttu-id="3e1ac-151">但是，如果 **ResourceType** 屬性為 21 (序列埠) 且 **ResourceSubType** 屬性為 "Microsoft： hyper-v：序列埠"，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更 **連接** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-155">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="3e1ac-156">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-160">A description of the object.</span></span> <span data-ttu-id="3e1ac-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-165">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-165">A display name for the object.</span></span> <span data-ttu-id="3e1ac-166">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="3e1ac-167">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="3e1ac-168">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-169">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-170">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3e1ac-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-172">只有一個主機資源可以指派給虛擬機器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="3e1ac-173">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="3e1ac-174">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3e1ac-175">這是一個唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-175">This is a read-only property.</span></span> <span data-ttu-id="3e1ac-176">但是，如果 **ResourceType** 屬性為 17 (Disk) 且 **ResourceSubType** 屬性為 "Microsoft： Hyper-v：實體磁片磁碟機"，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更 **HostResource** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-180">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-181">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3e1ac-182">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-183">**限制**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-184">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-186">將為此配置授與的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="3e1ac-187">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="3e1ac-188">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-189">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-192">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="3e1ac-193">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-194">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-197">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="3e1ac-198">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-199">**父系**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-202">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-202">The parent of the resource.</span></span> <span data-ttu-id="3e1ac-203">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-204">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-207">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="3e1ac-208">針對與虛擬機器相關聯的實例，這將會是「Microsoft：*GUID* \\ *裝置特定資料*」。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="3e1ac-209">針對定義虛擬機器潛在設定的實例，這會是「Microsoft：定義 \\ *GUID* \\ *類型*」，其中 *類型* 可以是「最大值」、「最小值」、「預設」或「遞增」的其中一個。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="3e1ac-210">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-211">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-212">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-214">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="3e1ac-215">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="3e1ac-216">這些資源保證可供虛擬機器取用。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="3e1ac-217">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-221">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="3e1ac-222">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="3e1ac-223">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-225">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-227">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3e1ac-228">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="3e1ac-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (30 32767) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e1ac-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-265">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-267">指定向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="3e1ac-268">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="3e1ac-269">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-270">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-273">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="3e1ac-274">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="3e1ac-275">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-276">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-277">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3e1ac-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-279">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="3e1ac-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-280">此資源的識別碼字串陣列，會呈現給虛擬機器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="3e1ac-281">只有當 **ResourceType** 屬性設為 6 (平行 SCSI HBA) ，而且 **ResourceSubType** 屬性設定為「Microsoft 綜合 scsi 控制器」時，才會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="3e1ac-282">這個屬性會設定為 "*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="3e1ac-283">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3e1ac-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1ac-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e1ac-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e1ac-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1ac-287">為每個虛擬機器處理器定義相對權數的整數。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="3e1ac-288">符合所有保留之後，裝載平臺的剩餘實體處理器容量將會根據其相對權數配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="3e1ac-289">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3e1ac-290">範圍： 0 1000</span><span class="sxs-lookup"><span data-stu-id="3e1ac-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e1ac-291">備註</span><span class="sxs-lookup"><span data-stu-id="3e1ac-291">Remarks</span></span>

<span data-ttu-id="3e1ac-292">存取 **Msvm \_ ResourceAllocationSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3e1ac-293">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="3e1ac-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1ac-294">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e1ac-294">Requirements</span></span>



| <span data-ttu-id="3e1ac-295">需求</span><span class="sxs-lookup"><span data-stu-id="3e1ac-295">Requirement</span></span> | <span data-ttu-id="3e1ac-296">值</span><span class="sxs-lookup"><span data-stu-id="3e1ac-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1ac-297">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e1ac-297">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1ac-298">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e1ac-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e1ac-299">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e1ac-299">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1ac-300">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e1ac-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e1ac-301">命名空間</span><span class="sxs-lookup"><span data-stu-id="3e1ac-301">Namespace</span></span><br/>                | <span data-ttu-id="3e1ac-302">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3e1ac-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e1ac-303">MOF</span><span class="sxs-lookup"><span data-stu-id="3e1ac-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e1ac-304"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3e1ac-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e1ac-305">DLL</span><span class="sxs-lookup"><span data-stu-id="3e1ac-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e1ac-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e1ac-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e1ac-307">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e1ac-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1ac-308">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="3e1ac-309">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="3e1ac-310">**Msvm \_ ResourceAllocationSettingData (V1)**</span><span class="sxs-lookup"><span data-stu-id="3e1ac-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="3e1ac-311">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="3e1ac-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

