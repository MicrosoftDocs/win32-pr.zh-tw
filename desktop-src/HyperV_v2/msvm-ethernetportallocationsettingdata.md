---
description: 代表靜態或動態切換埠的配置要求，或代表目前配置之靜態或動態切換埠的使用中設定。
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Msvm_EthernetPortAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974707"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="fca0d-103">Msvm \_ EthernetPortAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="fca0d-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="fca0d-104">代表靜態或動態切換埠的配置要求，或代表目前配置之靜態或動態切換埠的使用中設定。</span><span class="sxs-lookup"><span data-stu-id="fca0d-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="fca0d-105">動態交換器埠的配置要求也稱為連接要求。</span><span class="sxs-lookup"><span data-stu-id="fca0d-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="fca0d-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca0d-107">語法</span><span class="sxs-lookup"><span data-stu-id="fca0d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="fca0d-108">成員</span><span class="sxs-lookup"><span data-stu-id="fca0d-108">Members</span></span>

<span data-ttu-id="fca0d-109">**Msvm \_ EthernetPortAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fca0d-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fca0d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fca0d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fca0d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fca0d-111">Properties</span></span>

<span data-ttu-id="fca0d-112">**Msvm \_ EthernetPortAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fca0d-113">**位址**</span><span class="sxs-lookup"><span data-stu-id="fca0d-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-116">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="fca0d-116">The address of the resource.</span></span> <span data-ttu-id="fca0d-117">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="fca0d-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-121">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="fca0d-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fca0d-122">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="fca0d-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fca0d-123">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="fca0d-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-127">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="fca0d-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fca0d-128">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="fca0d-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fca0d-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-132">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="fca0d-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fca0d-133">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="fca0d-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fca0d-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-137">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="fca0d-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="fca0d-138">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="fca0d-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-142">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="fca0d-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-143">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="fca0d-143">A short description of the object.</span></span> <span data-ttu-id="fca0d-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠設定」。</span><span class="sxs-lookup"><span data-stu-id="fca0d-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-145">**CompartmentGuid**</span><span class="sxs-lookup"><span data-stu-id="fca0d-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fca0d-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-148">這個屬性會指定埠的目標網路區間。</span><span class="sxs-lookup"><span data-stu-id="fca0d-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="fca0d-149">只有內部介面卡支援此功能。</span><span class="sxs-lookup"><span data-stu-id="fca0d-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="fca0d-150">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="fca0d-151">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="fca0d-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-152">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fca0d-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-154">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="fca0d-154">The device to which this resource is connected.</span></span> <span data-ttu-id="fca0d-155">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-156">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="fca0d-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fca0d-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-159">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="fca0d-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="fca0d-160">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="fca0d-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="fca0d-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-164">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="fca0d-164">A description of the object.</span></span> <span data-ttu-id="fca0d-165">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠設定」。</span><span class="sxs-lookup"><span data-stu-id="fca0d-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-166">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="fca0d-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fca0d-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-169">VLAN 端點所需的設定模式。</span><span class="sxs-lookup"><span data-stu-id="fca0d-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="fca0d-170">這個屬性是用來設定與目標 Ethernet 埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)類別的實例中的初始 **OperationalEndpointMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="fca0d-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="fca0d-171">如需可能的值，請參閱 **Msvm \_ VLANEndpoint** 類別的 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="fca0d-172">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="fca0d-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fca0d-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-176">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fca0d-176">A display name for the object.</span></span> <span data-ttu-id="fca0d-177">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fca0d-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="fca0d-178">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="fca0d-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fca0d-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fca0d-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-182">指出配置要求是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="fca0d-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="fca0d-183">當配置要求標記為停用時 (3) ，則不會處理配置。</span><span class="sxs-lookup"><span data-stu-id="fca0d-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="fca0d-184">作用中設定的 **EnabledState** 一律會標示為已啟用 (2) 。</span><span class="sxs-lookup"><span data-stu-id="fca0d-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fca0d-185">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="fca0d-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fca0d-186">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="fca0d-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fca0d-187">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="fca0d-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-188">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fca0d-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-190">只有一個主機資源可以指派給虛擬交換器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="fca0d-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="fca0d-191">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="fca0d-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="fca0d-192">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fca0d-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-196">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="fca0d-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-197">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="fca0d-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fca0d-198">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。</span><span class="sxs-lookup"><span data-stu-id="fca0d-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-199">**LastKnownSwitchName**</span><span class="sxs-lookup"><span data-stu-id="fca0d-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-202">交換器的最後已知易記名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="fca0d-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="fca0d-203">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="fca0d-204">**限制**</span><span class="sxs-lookup"><span data-stu-id="fca0d-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-205">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fca0d-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-207">虛擬交換器可以取用的相對應主機資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="fca0d-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="fca0d-208">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-209">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="fca0d-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-210">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fca0d-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-212">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="fca0d-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fca0d-213">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-214">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="fca0d-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-217">字串，描述此 VLAN 端點所支援的 VLAN 端點模型類型。</span><span class="sxs-lookup"><span data-stu-id="fca0d-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="fca0d-218">只有當 **DesiredVLANEndpointMode** 屬性設定為 1 (其他) 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fca0d-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="fca0d-219">當 **DesiredVLANEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fca0d-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="fca0d-220">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="fca0d-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-221">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fca0d-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-224">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="fca0d-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="fca0d-225">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="fca0d-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-226">**父系**</span><span class="sxs-lookup"><span data-stu-id="fca0d-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-229">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="fca0d-229">The parent of the resource.</span></span> <span data-ttu-id="fca0d-230">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-231">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="fca0d-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-234">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="fca0d-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="fca0d-235">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-236">**RequiredFeatureHints**</span><span class="sxs-lookup"><span data-stu-id="fca0d-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-237">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fca0d-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-239">對應至 **RequiredFeatures** 陣列中每個專案的顯示名稱清單。</span><span class="sxs-lookup"><span data-stu-id="fca0d-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-240">**RequiredFeatures**</span><span class="sxs-lookup"><span data-stu-id="fca0d-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-241">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fca0d-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-242">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fca0d-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-243">功能識別碼的清單，代表埠所需的所有功能。</span><span class="sxs-lookup"><span data-stu-id="fca0d-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-244">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="fca0d-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-245">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fca0d-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-247">保留供虛擬交換器使用的資源數量。</span><span class="sxs-lookup"><span data-stu-id="fca0d-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="fca0d-248">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fca0d-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-252">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="fca0d-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="fca0d-253">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="fca0d-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="fca0d-254">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fca0d-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-256">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fca0d-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-258">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="fca0d-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fca0d-259">這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律會設定為 33 (Ethernet 連接) 。</span><span class="sxs-lookup"><span data-stu-id="fca0d-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-260">**TestReplicaPoolID**</span><span class="sxs-lookup"><span data-stu-id="fca0d-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fca0d-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-263">指定當建立連接時，會將連接配置給測試複本系統的網路資源集區。</span><span class="sxs-lookup"><span data-stu-id="fca0d-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-264">**TestReplicaSwitchName**</span><span class="sxs-lookup"><span data-stu-id="fca0d-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-265">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-266">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fca0d-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-267">指定虛擬網路交換器的顯示名稱，該名稱會在建立時為測試複本系統組態連接。</span><span class="sxs-lookup"><span data-stu-id="fca0d-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fca0d-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fca0d-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-271">虛擬交換器中的埠總數。</span><span class="sxs-lookup"><span data-stu-id="fca0d-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="fca0d-272">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="fca0d-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fca0d-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-276">指定 **VirtualQuantity** 屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="fca0d-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="fca0d-277">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="fca0d-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fca0d-278">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fca0d-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="fca0d-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fca0d-280">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fca0d-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fca0d-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fca0d-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fca0d-282">定義每個虛擬交換器之權數的整數。</span><span class="sxs-lookup"><span data-stu-id="fca0d-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="fca0d-283">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="fca0d-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="fca0d-284">範圍： 0 1000</span><span class="sxs-lookup"><span data-stu-id="fca0d-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fca0d-285">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca0d-285">Requirements</span></span>



| <span data-ttu-id="fca0d-286">需求</span><span class="sxs-lookup"><span data-stu-id="fca0d-286">Requirement</span></span> | <span data-ttu-id="fca0d-287">值</span><span class="sxs-lookup"><span data-stu-id="fca0d-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca0d-288">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fca0d-288">Minimum supported client</span></span><br/> | <span data-ttu-id="fca0d-289">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca0d-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fca0d-290">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fca0d-290">Minimum supported server</span></span><br/> | <span data-ttu-id="fca0d-291">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca0d-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fca0d-292">命名空間</span><span class="sxs-lookup"><span data-stu-id="fca0d-292">Namespace</span></span><br/>                | <span data-ttu-id="fca0d-293">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fca0d-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fca0d-294">MOF</span><span class="sxs-lookup"><span data-stu-id="fca0d-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fca0d-295"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fca0d-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fca0d-296">DLL</span><span class="sxs-lookup"><span data-stu-id="fca0d-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fca0d-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fca0d-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

