---
description: 代表模擬乙太網路介面卡設定的狀態。
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Msvm_EmulatedEthernetPortSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848671"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="658d1-103">Msvm \_ EmulatedEthernetPortSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="658d1-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="658d1-104">代表模擬乙太網路介面卡設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="658d1-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="658d1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="658d1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="658d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="658d1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="658d1-107">成員</span><span class="sxs-lookup"><span data-stu-id="658d1-107">Members</span></span>

<span data-ttu-id="658d1-108">**Msvm \_ EmulatedEthernetPortSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="658d1-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="658d1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="658d1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="658d1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="658d1-110">Properties</span></span>

<span data-ttu-id="658d1-111">**Msvm \_ EmulatedEthernetPortSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="658d1-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="658d1-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="658d1-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="658d1-115">The address of the resource.</span></span> <span data-ttu-id="658d1-116">例如，乙太網路埠的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="658d1-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="658d1-117">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="658d1-118">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="658d1-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="658d1-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-122">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="658d1-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="658d1-123">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="658d1-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="658d1-124">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="658d1-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-128">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="658d1-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="658d1-129">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 "埠"。</span><span class="sxs-lookup"><span data-stu-id="658d1-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="658d1-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="658d1-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658d1-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-133">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="658d1-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="658d1-134">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="658d1-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="658d1-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658d1-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-138">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="658d1-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="658d1-139">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="658d1-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-140">**標題**</span><span class="sxs-lookup"><span data-stu-id="658d1-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-143">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="658d1-143">A short description of the object.</span></span> <span data-ttu-id="658d1-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="658d1-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="658d1-145">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="658d1-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658d1-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-148">指出此乙太網路介面卡是否由叢集監視。</span><span class="sxs-lookup"><span data-stu-id="658d1-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="658d1-149">如果未設定，此屬性會預設為 true。</span><span class="sxs-lookup"><span data-stu-id="658d1-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="658d1-150">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="658d1-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="658d1-151">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="658d1-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-152">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="658d1-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-153">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="658d1-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="658d1-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-155">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="658d1-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="658d1-156">例如，名為網路或交換器埠。</span><span class="sxs-lookup"><span data-stu-id="658d1-156">For example, a named network or switch port.</span></span> <span data-ttu-id="658d1-157">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="658d1-158">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="658d1-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="658d1-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="658d1-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-162">描述已配置資源的取用者可見度。</span><span class="sxs-lookup"><span data-stu-id="658d1-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="658d1-163">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="658d1-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-164">**說明**</span><span class="sxs-lookup"><span data-stu-id="658d1-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-167">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="658d1-167">A description of the object.</span></span> <span data-ttu-id="658d1-168">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「Microsoft 模擬 Ethernet 埠的設定」。</span><span class="sxs-lookup"><span data-stu-id="658d1-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="658d1-169">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="658d1-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-170">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="658d1-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-172">VLAN 端點所需的設定模式。</span><span class="sxs-lookup"><span data-stu-id="658d1-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="658d1-173">這個屬性是用來設定與目標 Ethernet 埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)類別的實例中的初始 **OperationalEndpointMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="658d1-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="658d1-174">如需可能的值，請參閱 **Msvm \_ VLANEndpoint** 類別的 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="658d1-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="658d1-175">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="658d1-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="658d1-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-179">與此 RASD 實例相關聯之裝置的使用者可設定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="658d1-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="658d1-180">這個屬性會繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，而且會設定為「Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="658d1-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="658d1-181">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="658d1-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="658d1-182">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="658d1-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="658d1-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-184">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="658d1-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="658d1-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-186">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="658d1-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="658d1-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-190">在具現化命名空間的範圍內， **InstanceID** 會以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="658d1-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="658d1-191">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，且一律設定為 "Microsoft：*VMID* \\ *VDID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="658d1-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="658d1-192">**限制**</span><span class="sxs-lookup"><span data-stu-id="658d1-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-193">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="658d1-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-195">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="658d1-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="658d1-196">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="658d1-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-197">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="658d1-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="658d1-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-200">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="658d1-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="658d1-201">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="658d1-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-202">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="658d1-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-205">字串，描述此 VLAN 端點所支援的 VLAN 端點模型類型。</span><span class="sxs-lookup"><span data-stu-id="658d1-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="658d1-206">只有當 **DesiredVLANEndpointMode** 屬性設定為 1 (其他) 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="658d1-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="658d1-207">當 **DesiredVLANEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="658d1-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="658d1-208">這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="658d1-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-209">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="658d1-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-212">描述資源類型的字串，當無法使用定義完善的值，並將 ResourceType 設定為 0 ( "Other" ) 。</span><span class="sxs-lookup"><span data-stu-id="658d1-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="658d1-213">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="658d1-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-214">**父系**</span><span class="sxs-lookup"><span data-stu-id="658d1-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-217">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="658d1-217">The parent of the resource.</span></span> <span data-ttu-id="658d1-218">例如，目前配置的控制器。</span><span class="sxs-lookup"><span data-stu-id="658d1-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="658d1-219">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-220">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="658d1-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-223">資源目前配置來源的集區，或當配置發生時，將會配置資源的集區。</span><span class="sxs-lookup"><span data-stu-id="658d1-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="658d1-224">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-225">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="658d1-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-226">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="658d1-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-228">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="658d1-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="658d1-229">在支援過度使用資源的系統上，此值通常用於許可控制，以防止配置被接受。</span><span class="sxs-lookup"><span data-stu-id="658d1-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="658d1-230">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="658d1-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="658d1-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-234">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="658d1-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="658d1-235">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="658d1-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="658d1-236">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為「Microsoft 模擬 Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="658d1-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="658d1-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="658d1-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="658d1-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-240">套用此設定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="658d1-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="658d1-241">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 10 (乙太網路介面卡) 。</span><span class="sxs-lookup"><span data-stu-id="658d1-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-242">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="658d1-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-243">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658d1-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-245">指出是否要使用靜態 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="658d1-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="658d1-246">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="658d1-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="658d1-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-248">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="658d1-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-250">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="658d1-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="658d1-251">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="658d1-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="658d1-252">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="658d1-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658d1-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-255">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="658d1-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="658d1-256">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="658d1-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="658d1-257">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="658d1-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="658d1-258">**Weight**</span><span class="sxs-lookup"><span data-stu-id="658d1-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658d1-259">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="658d1-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="658d1-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658d1-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658d1-261">相對於相同 ResourcePool 中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="658d1-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="658d1-262">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="658d1-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="658d1-263">備註</span><span class="sxs-lookup"><span data-stu-id="658d1-263">Remarks</span></span>

<span data-ttu-id="658d1-264">存取 **Msvm \_ EmulatedEthernetPortSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="658d1-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="658d1-265">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="658d1-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="658d1-266">範例</span><span class="sxs-lookup"><span data-stu-id="658d1-266">Examples</span></span>

<span data-ttu-id="658d1-267">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="658d1-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="658d1-268">規格需求</span><span class="sxs-lookup"><span data-stu-id="658d1-268">Requirements</span></span>



| <span data-ttu-id="658d1-269">需求</span><span class="sxs-lookup"><span data-stu-id="658d1-269">Requirement</span></span> | <span data-ttu-id="658d1-270">值</span><span class="sxs-lookup"><span data-stu-id="658d1-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="658d1-271">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="658d1-271">Minimum supported client</span></span><br/> | <span data-ttu-id="658d1-272">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="658d1-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="658d1-273">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="658d1-273">Minimum supported server</span></span><br/> | <span data-ttu-id="658d1-274">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="658d1-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="658d1-275">命名空間</span><span class="sxs-lookup"><span data-stu-id="658d1-275">Namespace</span></span><br/>                | <span data-ttu-id="658d1-276">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="658d1-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="658d1-277">MOF</span><span class="sxs-lookup"><span data-stu-id="658d1-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="658d1-278"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="658d1-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="658d1-279">DLL</span><span class="sxs-lookup"><span data-stu-id="658d1-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="658d1-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="658d1-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="658d1-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="658d1-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658d1-282">**CIM \_ EthernetPortAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="658d1-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="658d1-283">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="658d1-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

