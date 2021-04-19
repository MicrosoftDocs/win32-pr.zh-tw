---
description: 代表綜合乙太網路介面卡已設定的狀態。
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Msvm_SyntheticEthernetPortSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970959"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="d6b8c-103">Msvm \_ SyntheticEthernetPortSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="d6b8c-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="d6b8c-104">代表綜合乙太網路介面卡已設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="d6b8c-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b8c-106">語法</span><span class="sxs-lookup"><span data-stu-id="d6b8c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="d6b8c-107">成員</span><span class="sxs-lookup"><span data-stu-id="d6b8c-107">Members</span></span>

<span data-ttu-id="d6b8c-108">**Msvm \_ SyntheticEthernetPortSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d6b8c-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d6b8c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d6b8c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6b8c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d6b8c-110">Properties</span></span>

<span data-ttu-id="d6b8c-111">**Msvm \_ SyntheticEthernetPortSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6b8c-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-115">The address of the resource.</span></span> <span data-ttu-id="d6b8c-116">例如，乙太網路埠的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="d6b8c-117">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-121">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d6b8c-122">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d6b8c-123">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-127">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d6b8c-128">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-129">**AllowPacketDirect**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d6b8c-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-132">指出是否已啟用 VM 的 PacketDirect 投影。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="d6b8c-133">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d6b8c-134">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-137">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="d6b8c-138">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-139">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-142">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="d6b8c-143">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-144">**標題**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-147">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-147">A short description of the object.</span></span> <span data-ttu-id="d6b8c-148">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-149">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-152">指出此乙太網路介面卡是否由叢集監視。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="d6b8c-153">如果未設定，此屬性會預設為 true。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="d6b8c-154">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="d6b8c-155">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-156">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-157">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6b8c-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-159">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="d6b8c-160">例如，名為網路或交換器埠。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-160">For example, a named network or switch port.</span></span> <span data-ttu-id="d6b8c-161">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-162">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-165">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="d6b8c-166">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-167">**說明**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-170">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-170">A description of the object.</span></span> <span data-ttu-id="d6b8c-171">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-172">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-175">VLAN 端點所需的設定模式。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="d6b8c-176">這個屬性是用來設定與目標 Ethernet 埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)類別的實例中的初始 **OperationalEndpointMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="d6b8c-177">如需可能的值，請參閱 **Msvm \_ VLANEndpoint** 類別的 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="d6b8c-178">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-179">**DeviceNamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-182">指出此乙太網路介面卡是否支援裝置命名。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="d6b8c-183">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="d6b8c-184">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d6b8c-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-188">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-188">A short description of the object.</span></span> <span data-ttu-id="d6b8c-189">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-190">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-191">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6b8c-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-193">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-197">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-198">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d6b8c-199">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-200">**限制**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-201">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-203">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="d6b8c-204">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-205">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-206">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-208">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d6b8c-209">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-210">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-213">字串，描述此 VLAN 端點所支援的 VLAN 端點模型類型。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="d6b8c-214">只有當 **DesiredVLANEndpointMode** 屬性設定為 1 (其他) 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="d6b8c-215">當 **DesiredVLANEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="d6b8c-216">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-220">當定義完善的值無法使用且 **ResourceType** 設定為 "Other" (0) 時，描述資源類型的字串。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="d6b8c-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-222">**父系**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-225">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-225">The parent of the resource.</span></span> <span data-ttu-id="d6b8c-226">例如，目前配置的控制器。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="d6b8c-227">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-231">資源目前配置來源的集區，或當配置發生時，將配置資源的集區。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="d6b8c-232">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-233">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-234">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-236">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="d6b8c-237">在支援過度使用資源的系統上，此值通常用於許可控制，以防止配置被接受。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="d6b8c-238">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-242">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="d6b8c-243">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="d6b8c-244">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-248">套用此設定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="d6b8c-249">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 10 (乙太網路介面卡) 。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-250">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-253">指定 MAC 位址是否為靜態。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-255">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-257">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="d6b8c-258">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-259">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-262">指定 **VirtualQuantity** 屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="d6b8c-263">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="d6b8c-264">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-265">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-266">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d6b8c-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-268">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="d6b8c-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-269">此資源的識別碼字串陣列，會呈現給虛擬機器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="d6b8c-270">每個索引的索引和值都是以每個資源為基礎來定義 (也就是每個列舉 **ResourceType** 屬性值) 。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="d6b8c-271">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6b8c-272">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6b8c-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6b8c-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6b8c-274">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="d6b8c-275">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6b8c-276">備註</span><span class="sxs-lookup"><span data-stu-id="d6b8c-276">Remarks</span></span>

<span data-ttu-id="d6b8c-277">存取 **Msvm \_ SyntheticEthernetPortSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d6b8c-278">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d6b8c-279">範例</span><span class="sxs-lookup"><span data-stu-id="d6b8c-279">Examples</span></span>

<span data-ttu-id="d6b8c-280">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="d6b8c-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b8c-281">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6b8c-281">Requirements</span></span>



| <span data-ttu-id="d6b8c-282">需求</span><span class="sxs-lookup"><span data-stu-id="d6b8c-282">Requirement</span></span> | <span data-ttu-id="d6b8c-283">值</span><span class="sxs-lookup"><span data-stu-id="d6b8c-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b8c-284">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6b8c-284">Minimum supported client</span></span><br/> | <span data-ttu-id="d6b8c-285">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6b8c-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d6b8c-286">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6b8c-286">Minimum supported server</span></span><br/> | <span data-ttu-id="d6b8c-287">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6b8c-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6b8c-288">命名空間</span><span class="sxs-lookup"><span data-stu-id="d6b8c-288">Namespace</span></span><br/>                | <span data-ttu-id="d6b8c-289">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d6b8c-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d6b8c-290">MOF</span><span class="sxs-lookup"><span data-stu-id="d6b8c-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6b8c-291"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d6b8c-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6b8c-292">DLL</span><span class="sxs-lookup"><span data-stu-id="d6b8c-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6b8c-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6b8c-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6b8c-294">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6b8c-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b8c-295">**CIM \_ EthernetPortAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="d6b8c-296">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d6b8c-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

