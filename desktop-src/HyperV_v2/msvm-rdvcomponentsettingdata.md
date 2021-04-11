---
description: 代表遠端桌面虛擬化 (RDV) 元件的設定狀態。 預設狀態為 [已啟用]。
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Msvm_RdvComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849495"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="4dfcd-104">Msvm \_ RdvComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="4dfcd-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="4dfcd-105">代表遠端桌面虛擬化 (RDV) 元件的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="4dfcd-106">預設狀態為 [已啟用]。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-106">The default state is Enabled.</span></span>

<span data-ttu-id="4dfcd-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dfcd-108">語法</span><span class="sxs-lookup"><span data-stu-id="4dfcd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
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
};
```

## <a name="members"></a><span data-ttu-id="4dfcd-109">成員</span><span class="sxs-lookup"><span data-stu-id="4dfcd-109">Members</span></span>

<span data-ttu-id="4dfcd-110">**Msvm \_ RdvComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4dfcd-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4dfcd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4dfcd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dfcd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4dfcd-112">Properties</span></span>

<span data-ttu-id="4dfcd-113">**Msvm \_ RdvComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dfcd-114">**位址**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-117">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-117">The address of the resource.</span></span> <span data-ttu-id="4dfcd-118">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-122">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="4dfcd-123">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="4dfcd-124">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-128">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="4dfcd-129">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-133">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="4dfcd-134">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-138">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="4dfcd-139">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-140">**標題**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-143">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="4dfcd-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-144">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-144">A short description of the object.</span></span> <span data-ttu-id="4dfcd-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠設定」。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-146">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-147">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4dfcd-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-149">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-149">The device to which this resource is connected.</span></span> <span data-ttu-id="4dfcd-150">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-151">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-154">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="4dfcd-155">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-156">**說明**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-159">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-159">A description of the object.</span></span> <span data-ttu-id="4dfcd-160">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠設定」。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-164">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-164">A display name for the object.</span></span> <span data-ttu-id="4dfcd-165">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="4dfcd-166">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-170">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4dfcd-171">有效的值為 2 (啟用) ，而 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="4dfcd-172">預設值為 2 (已啟用) 。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="4dfcd-173">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-175">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4dfcd-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-177">只有一個主機資源可以指派給虛擬交換器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="4dfcd-178">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="4dfcd-179">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-183">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-184">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4dfcd-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-186">**限制**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-187">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-189">虛擬交換器可以取用的相對應主機資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="4dfcd-190">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-191">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-194">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="4dfcd-195">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-196">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-199">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="4dfcd-200">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-201">**父系**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-204">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-204">The parent of the resource.</span></span> <span data-ttu-id="4dfcd-205">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-206">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-209">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="4dfcd-210">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-211">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-212">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-214">保留供虛擬交換器使用的資源數量。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="4dfcd-215">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-219">字串，描述此資源的實作為特定子類型。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="4dfcd-220">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="4dfcd-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-225">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="4dfcd-226">這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律會設定為 33 (Ethernet 連接) 。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-230">虛擬交換器中的埠總數。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="4dfcd-231">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-232">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-235">指定 **VirtualQuantity** 屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="4dfcd-236">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="4dfcd-237">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4dfcd-238">**Weight**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfcd-239">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dfcd-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dfcd-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dfcd-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfcd-241">定義每個虛擬交換器之權數的整數。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="4dfcd-242">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="4dfcd-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="4dfcd-243">範圍： 0 1000</span><span class="sxs-lookup"><span data-stu-id="4dfcd-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4dfcd-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dfcd-244">Requirements</span></span>



| <span data-ttu-id="4dfcd-245">需求</span><span class="sxs-lookup"><span data-stu-id="4dfcd-245">Requirement</span></span> | <span data-ttu-id="4dfcd-246">值</span><span class="sxs-lookup"><span data-stu-id="4dfcd-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dfcd-247">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dfcd-247">Minimum supported client</span></span><br/> | <span data-ttu-id="4dfcd-248">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dfcd-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4dfcd-249">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dfcd-249">Minimum supported server</span></span><br/> | <span data-ttu-id="4dfcd-250">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dfcd-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4dfcd-251">命名空間</span><span class="sxs-lookup"><span data-stu-id="4dfcd-251">Namespace</span></span><br/>                | <span data-ttu-id="4dfcd-252">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4dfcd-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4dfcd-253">MOF</span><span class="sxs-lookup"><span data-stu-id="4dfcd-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dfcd-254"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4dfcd-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dfcd-255">DLL</span><span class="sxs-lookup"><span data-stu-id="4dfcd-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dfcd-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4dfcd-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

