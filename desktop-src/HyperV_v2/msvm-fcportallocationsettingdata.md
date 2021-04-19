---
description: 代表綜合光纖通道埠或光纖通道交換器埠的設定狀態。
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Msvm_FcPortAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973669"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="68636-103">Msvm \_ FcPortAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="68636-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="68636-104">代表綜合光纖通道埠或光纖通道交換器埠的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="68636-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="68636-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="68636-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68636-106">語法</span><span class="sxs-lookup"><span data-stu-id="68636-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="68636-107">成員</span><span class="sxs-lookup"><span data-stu-id="68636-107">Members</span></span>

<span data-ttu-id="68636-108">**Msvm \_ FcPortAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="68636-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="68636-109">屬性</span><span class="sxs-lookup"><span data-stu-id="68636-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68636-110">屬性</span><span class="sxs-lookup"><span data-stu-id="68636-110">Properties</span></span>

<span data-ttu-id="68636-111">**Msvm \_ FcPortAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="68636-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68636-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="68636-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="68636-115">The address of the resource.</span></span> <span data-ttu-id="68636-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="68636-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="68636-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="68636-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="68636-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="68636-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="68636-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="68636-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="68636-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="68636-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="68636-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68636-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="68636-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="68636-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="68636-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="68636-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68636-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-136">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="68636-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="68636-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="68636-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68636-141">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="68636-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="68636-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="68636-142">A short description of the object.</span></span> <span data-ttu-id="68636-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="68636-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68636-144">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="68636-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-145">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="68636-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68636-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-147">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="68636-147">The device to which this resource is connected.</span></span> <span data-ttu-id="68636-148">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="68636-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="68636-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68636-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-152">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="68636-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="68636-153">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-154">**說明**</span><span class="sxs-lookup"><span data-stu-id="68636-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-157">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="68636-157">A description of the object.</span></span> <span data-ttu-id="68636-158">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="68636-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68636-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="68636-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-162">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="68636-162">A display name for the object.</span></span> <span data-ttu-id="68636-163">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="68636-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="68636-164">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="68636-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="68636-165">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="68636-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68636-166">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="68636-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-167">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="68636-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68636-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-169">只有一個主機資源可以指派給虛擬機器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="68636-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="68636-170">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="68636-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="68636-171">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68636-172">這是唯讀屬性，但是如果 **ResourceType** 屬性是 22 (磁片) 而且 **ResourceSubType** 屬性是 "Microsoft 實體磁片磁碟機"，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="68636-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68636-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="68636-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68636-176">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="68636-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="68636-177">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="68636-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="68636-178">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="68636-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="68636-179">**限制**</span><span class="sxs-lookup"><span data-stu-id="68636-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-180">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="68636-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68636-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-182">將為此配置授與的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="68636-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="68636-183">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="68636-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68636-184">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-185">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="68636-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-186">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="68636-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68636-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-188">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="68636-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="68636-189">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-190">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="68636-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-193">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="68636-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="68636-194">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-195">**父系**</span><span class="sxs-lookup"><span data-stu-id="68636-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-198">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="68636-198">The parent of the resource.</span></span> <span data-ttu-id="68636-199">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-200">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="68636-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-203">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="68636-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="68636-204">針對與虛擬機器相關聯的實例，這將會是「Microsoft：*GUID* \\ *裝置特定資料*」。</span><span class="sxs-lookup"><span data-stu-id="68636-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="68636-205">針對定義虛擬機器潛在設定的實例，這會是「Microsoft：定義 \\ *GUID* \\ *類型*」，其中 *類型* 可以是「最大值」、「最小值」、「預設」或「遞增」的其中一個。</span><span class="sxs-lookup"><span data-stu-id="68636-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="68636-206">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-207">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="68636-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-208">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="68636-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68636-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-210">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="68636-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="68636-211">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="68636-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68636-212">這些資源保證可供虛擬機器取用。</span><span class="sxs-lookup"><span data-stu-id="68636-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="68636-213">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="68636-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-217">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="68636-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="68636-218">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="68636-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="68636-219">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="68636-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="68636-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68636-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-223">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="68636-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="68636-224">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="68636-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="68636-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="68636-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="68636-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68636-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="68636-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68636-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="68636-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68636-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="68636-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="68636-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="68636-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="68636-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="68636-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="68636-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="68636-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="68636-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="68636-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="68636-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="68636-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="68636-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="68636-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="68636-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="68636-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="68636-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="68636-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="68636-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="68636-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="68636-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="68636-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="68636-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="68636-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="68636-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (17) </span><span class="sxs-lookup"><span data-stu-id="68636-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="68636-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (18) </span><span class="sxs-lookup"><span data-stu-id="68636-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="68636-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (19) </span><span class="sxs-lookup"><span data-stu-id="68636-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="68636-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (20) </span><span class="sxs-lookup"><span data-stu-id="68636-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="68636-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (21) </span><span class="sxs-lookup"><span data-stu-id="68636-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="68636-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**磁片** (22) </span><span class="sxs-lookup"><span data-stu-id="68636-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="68636-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**磁帶** (23) </span><span class="sxs-lookup"><span data-stu-id="68636-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="68636-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (24) </span><span class="sxs-lookup"><span data-stu-id="68636-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="68636-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="68636-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="68636-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="68636-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="68636-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="68636-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="68636-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) </span><span class="sxs-lookup"><span data-stu-id="68636-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="68636-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) </span><span class="sxs-lookup"><span data-stu-id="68636-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="68636-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (30 32767) </span><span class="sxs-lookup"><span data-stu-id="68636-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="68636-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="68636-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68636-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="68636-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-257">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="68636-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68636-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-259">指定向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="68636-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="68636-260">這個屬性的度量單位是由 **VirtualQuantityUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="68636-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68636-261">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-262">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="68636-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="68636-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68636-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-265">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="68636-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="68636-266">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="68636-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="68636-267">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68636-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="68636-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68636-269">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68636-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68636-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68636-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68636-271">為每個虛擬機器處理器定義相對權數的整數。</span><span class="sxs-lookup"><span data-stu-id="68636-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="68636-272">符合所有保留之後，裝載平臺的剩餘實體處理器容量將會根據其相對權數配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="68636-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="68636-273">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="68636-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68636-274">範圍： 0 1000</span><span class="sxs-lookup"><span data-stu-id="68636-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68636-275">規格需求</span><span class="sxs-lookup"><span data-stu-id="68636-275">Requirements</span></span>



| <span data-ttu-id="68636-276">需求</span><span class="sxs-lookup"><span data-stu-id="68636-276">Requirement</span></span> | <span data-ttu-id="68636-277">值</span><span class="sxs-lookup"><span data-stu-id="68636-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68636-278">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68636-278">Minimum supported client</span></span><br/> | <span data-ttu-id="68636-279">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68636-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68636-280">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68636-280">Minimum supported server</span></span><br/> | <span data-ttu-id="68636-281">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68636-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68636-282">命名空間</span><span class="sxs-lookup"><span data-stu-id="68636-282">Namespace</span></span><br/>                | <span data-ttu-id="68636-283">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="68636-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68636-284">MOF</span><span class="sxs-lookup"><span data-stu-id="68636-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68636-285"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="68636-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68636-286">DLL</span><span class="sxs-lookup"><span data-stu-id="68636-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68636-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68636-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

