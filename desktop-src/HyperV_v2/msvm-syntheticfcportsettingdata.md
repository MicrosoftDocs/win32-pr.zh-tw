---
description: 代表綜合光纖通道埠的已設定狀態。
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Msvm_SyntheticFcPortSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689776"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="89aef-103">Msvm \_ SyntheticFcPortSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="89aef-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="89aef-104">代表綜合光纖通道埠的已設定狀態。</span><span class="sxs-lookup"><span data-stu-id="89aef-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="89aef-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="89aef-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89aef-106">語法</span><span class="sxs-lookup"><span data-stu-id="89aef-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="89aef-107">成員</span><span class="sxs-lookup"><span data-stu-id="89aef-107">Members</span></span>

<span data-ttu-id="89aef-108">**Msvm \_ SyntheticFcPortSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89aef-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="89aef-109">屬性</span><span class="sxs-lookup"><span data-stu-id="89aef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89aef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="89aef-110">Properties</span></span>

<span data-ttu-id="89aef-111">**Msvm \_ SyntheticFcPortSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89aef-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89aef-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="89aef-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="89aef-115">The address of the resource.</span></span> <span data-ttu-id="89aef-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="89aef-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="89aef-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="89aef-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="89aef-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="89aef-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="89aef-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="89aef-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="89aef-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="89aef-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="89aef-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="89aef-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="89aef-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="89aef-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="89aef-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-136">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="89aef-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="89aef-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="89aef-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89aef-141">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="89aef-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="89aef-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="89aef-142">A short description of the object.</span></span> <span data-ttu-id="89aef-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="89aef-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-144">**ChapEnabled**</span><span class="sxs-lookup"><span data-stu-id="89aef-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="89aef-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-147">指出此埠已使用 DH-CHAP 以共用密碼設定，這可讓光纖通道網狀架構驗證此虛擬機器可以合法地使用指派給此埠的全球名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-148">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="89aef-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-149">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89aef-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89aef-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-151">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="89aef-151">The device to which this resource is connected.</span></span> <span data-ttu-id="89aef-152">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-153">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="89aef-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89aef-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-156">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="89aef-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="89aef-157">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-158">**說明**</span><span class="sxs-lookup"><span data-stu-id="89aef-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-161">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="89aef-161">A description of the object.</span></span> <span data-ttu-id="89aef-162">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="89aef-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="89aef-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-166">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-166">A display name for the object.</span></span> <span data-ttu-id="89aef-167">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89aef-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="89aef-168">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="89aef-169">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="89aef-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-170">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="89aef-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-171">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89aef-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89aef-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-173">只有一個主機資源可以指派給虛擬機器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="89aef-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="89aef-174">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="89aef-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="89aef-175">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89aef-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89aef-179">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="89aef-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="89aef-180">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="89aef-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="89aef-181">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89aef-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-182">**限制**</span><span class="sxs-lookup"><span data-stu-id="89aef-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-183">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="89aef-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-185">可供虛擬機器使用的對應主機資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="89aef-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="89aef-186">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-187">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="89aef-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89aef-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-190">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="89aef-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="89aef-191">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-192">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="89aef-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-195">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="89aef-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="89aef-196">這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="89aef-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-197">**父系**</span><span class="sxs-lookup"><span data-stu-id="89aef-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-200">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="89aef-200">The parent of the resource.</span></span> <span data-ttu-id="89aef-201">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-202">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="89aef-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-205">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="89aef-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="89aef-206">針對與虛擬機器相關聯的實例，這將會是「Microsoft：*GUID* \\ *裝置特定資料*」。</span><span class="sxs-lookup"><span data-stu-id="89aef-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="89aef-207">針對定義虛擬機器潛在設定的實例，這會是「Microsoft：定義 \\ *GUID* \\ *類型*」，其中 *類型* 可以是「最大值」、「最小值」、「預設」或「遞增」的其中一個。</span><span class="sxs-lookup"><span data-stu-id="89aef-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="89aef-208">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-209">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="89aef-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-210">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="89aef-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-212">保留給虛擬機器使用的資源數量。</span><span class="sxs-lookup"><span data-stu-id="89aef-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="89aef-213">這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="89aef-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="89aef-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-217">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="89aef-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="89aef-218">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="89aef-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="89aef-219">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="89aef-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89aef-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-223">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="89aef-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="89aef-224">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="89aef-225">值</span><span class="sxs-lookup"><span data-stu-id="89aef-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="89aef-226">意義</span><span class="sxs-lookup"><span data-stu-id="89aef-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="89aef-227"><dt>**FC HBA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="89aef-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="89aef-228">光纖通道</span><span class="sxs-lookup"><span data-stu-id="89aef-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89aef-229">**SecondaryWWNN**</span><span class="sxs-lookup"><span data-stu-id="89aef-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-232">表示在虛擬機器的即時移轉期間，所要使用之虛擬 HBA 埠的全球節點名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-233">**SecondaryWWPN**</span><span class="sxs-lookup"><span data-stu-id="89aef-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-236">表示在虛擬機器的即時移轉期間，所要使用之虛擬 HBA 埠的全球埠名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-237">**VirtualPortWWNN**</span><span class="sxs-lookup"><span data-stu-id="89aef-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-240">表示虛擬 HBA 埠的全球節點名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-241">**VirtualPortWWPN**</span><span class="sxs-lookup"><span data-stu-id="89aef-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-244">表示虛擬 HBA 埠的全球埠名稱。</span><span class="sxs-lookup"><span data-stu-id="89aef-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="89aef-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="89aef-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-246">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="89aef-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-248">指定向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="89aef-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="89aef-249">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-250">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="89aef-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89aef-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-253">指定 **VirtualQuantity** 屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="89aef-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="89aef-254">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="89aef-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="89aef-255">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="89aef-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89aef-256">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="89aef-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-257">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89aef-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89aef-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89aef-259">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="89aef-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="89aef-260">此資源的識別碼字串陣列，會呈現給虛擬機器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="89aef-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="89aef-261">每個索引的索引和值都是以每個資源為基礎來定義 (也就是每個列舉的 **ResourceType** 值) 。</span><span class="sxs-lookup"><span data-stu-id="89aef-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="89aef-262">未使用此屬性</span><span class="sxs-lookup"><span data-stu-id="89aef-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="89aef-263">**Weight**</span><span class="sxs-lookup"><span data-stu-id="89aef-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89aef-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89aef-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89aef-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89aef-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89aef-266">為每個虛擬機器處理器定義相對權數的整數。</span><span class="sxs-lookup"><span data-stu-id="89aef-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="89aef-267">這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="89aef-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89aef-268">規格需求</span><span class="sxs-lookup"><span data-stu-id="89aef-268">Requirements</span></span>



| <span data-ttu-id="89aef-269">需求</span><span class="sxs-lookup"><span data-stu-id="89aef-269">Requirement</span></span> | <span data-ttu-id="89aef-270">值</span><span class="sxs-lookup"><span data-stu-id="89aef-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89aef-271">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89aef-271">Minimum supported client</span></span><br/> | <span data-ttu-id="89aef-272">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89aef-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89aef-273">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89aef-273">Minimum supported server</span></span><br/> | <span data-ttu-id="89aef-274">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89aef-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89aef-275">命名空間</span><span class="sxs-lookup"><span data-stu-id="89aef-275">Namespace</span></span><br/>                | <span data-ttu-id="89aef-276">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="89aef-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89aef-277">MOF</span><span class="sxs-lookup"><span data-stu-id="89aef-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89aef-278"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="89aef-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89aef-279">DLL</span><span class="sxs-lookup"><span data-stu-id="89aef-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89aef-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89aef-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

