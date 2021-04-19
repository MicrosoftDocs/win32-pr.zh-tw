---
description: 代表虛擬機器的綜合立體顯示控制器設定。
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Msvm_Synthetic3DDisplayControllerSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974198"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="3f03e-103">Msvm \_ Synthetic3DDisplayControllerSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="3f03e-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="3f03e-104">代表虛擬機器的綜合立體顯示控制器設定。</span><span class="sxs-lookup"><span data-stu-id="3f03e-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="3f03e-105">此類別只會與使用 RemoteFX 的虛擬機器搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3f03e-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="3f03e-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f03e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f03e-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f03e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
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
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="3f03e-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f03e-108">Members</span></span>

<span data-ttu-id="3f03e-109">**Msvm \_ Synthetic3DDisplayControllerSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f03e-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3f03e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3f03e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f03e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3f03e-111">Properties</span></span>

<span data-ttu-id="3f03e-112">**Msvm \_ Synthetic3DDisplayControllerSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3f03e-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f03e-113">**位址**</span><span class="sxs-lookup"><span data-stu-id="3f03e-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-116">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="3f03e-116">The address of the resource.</span></span> <span data-ttu-id="3f03e-117">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f03e-118">這是唯讀屬性，但是如果 **ResourceType** 屬性是 20 (圖形控制器) ，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3f03e-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="3f03e-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-122">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="3f03e-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="3f03e-123">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="3f03e-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="3f03e-124">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3f03e-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-128">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="3f03e-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="3f03e-129">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="3f03e-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3f03e-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-133">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="3f03e-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="3f03e-134">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="3f03e-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3f03e-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-138">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="3f03e-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="3f03e-139">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-140">**標題**</span><span class="sxs-lookup"><span data-stu-id="3f03e-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-143">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="3f03e-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-144">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3f03e-144">A short description of the object.</span></span> <span data-ttu-id="3f03e-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-146">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="3f03e-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-147">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3f03e-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-149">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="3f03e-149">The device to which this resource is connected.</span></span> <span data-ttu-id="3f03e-150">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f03e-151">這是唯讀屬性，但如果 1) **resourcetype** 屬性為 17 (序列埠) ，或 2) **resourcetype** 屬性為 21 (儲存範圍) 且 **ResourceSubType** 屬性為 "Microsoft Virtual Hard Disk"，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3f03e-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="3f03e-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3f03e-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-155">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="3f03e-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="3f03e-156">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="3f03e-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3f03e-160">A description of the object.</span></span> <span data-ttu-id="3f03e-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3f03e-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-165">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3f03e-165">A display name for the object.</span></span> <span data-ttu-id="3f03e-166">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3f03e-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="3f03e-167">變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="3f03e-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-168">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="3f03e-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-169">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3f03e-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-171">只有一個主機資源可以指派給虛擬機器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="3f03e-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="3f03e-172">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="3f03e-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="3f03e-173">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f03e-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-177">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3f03e-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3f03e-178">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-179">**限制**</span><span class="sxs-lookup"><span data-stu-id="3f03e-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-180">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3f03e-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-182">可供虛擬機器使用的對應主機資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="3f03e-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="3f03e-183">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-184">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="3f03e-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3f03e-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-187">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="3f03e-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="3f03e-188">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-189">**MaximumMonitors**</span><span class="sxs-lookup"><span data-stu-id="3f03e-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-190">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="3f03e-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3f03e-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-192">3D 顯示控制器可用的監視器數目上限。</span><span class="sxs-lookup"><span data-stu-id="3f03e-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="3f03e-193">監視器的最小數目是1，而最大值則取決於螢幕解析度上限。</span><span class="sxs-lookup"><span data-stu-id="3f03e-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="3f03e-194">下表定義允許不同解析度的監視器數目上限。</span><span class="sxs-lookup"><span data-stu-id="3f03e-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="3f03e-195">解決方案</span><span class="sxs-lookup"><span data-stu-id="3f03e-195">Resolution</span></span>            | <span data-ttu-id="3f03e-196">監視器上限</span><span class="sxs-lookup"><span data-stu-id="3f03e-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="3f03e-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="3f03e-197">1024  768</span></span><br/>  | <span data-ttu-id="3f03e-198">4</span><span class="sxs-lookup"><span data-stu-id="3f03e-198">4</span></span><br/>     |
| <span data-ttu-id="3f03e-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="3f03e-199">1280  1024</span></span><br/> | <span data-ttu-id="3f03e-200">4</span><span class="sxs-lookup"><span data-stu-id="3f03e-200">4</span></span><br/>     |
| <span data-ttu-id="3f03e-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="3f03e-201">1600  1200</span></span><br/> | <span data-ttu-id="3f03e-202">3</span><span class="sxs-lookup"><span data-stu-id="3f03e-202">3</span></span><br/>     |
| <span data-ttu-id="3f03e-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="3f03e-203">1920  1200</span></span><br/> | <span data-ttu-id="3f03e-204">2</span><span class="sxs-lookup"><span data-stu-id="3f03e-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3f03e-205">**MaximumScreenResolution**</span><span class="sxs-lookup"><span data-stu-id="3f03e-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-206">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="3f03e-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-208">指定立體顯示控制器的螢幕解析度上限。</span><span class="sxs-lookup"><span data-stu-id="3f03e-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="3f03e-209">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="3f03e-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="3f03e-210"><span id="1024___768"></span>**1024 \* 768** (0) </span><span class="sxs-lookup"><span data-stu-id="3f03e-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-211">最大解析度為 1024 768。</span><span class="sxs-lookup"><span data-stu-id="3f03e-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="3f03e-212"><span id="1280___1024"></span>**1280 \* 1024** (1) </span><span class="sxs-lookup"><span data-stu-id="3f03e-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-213">最大解析度為 1280 1024。</span><span class="sxs-lookup"><span data-stu-id="3f03e-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="3f03e-214"><span id="1600___1200"></span>**1600 \* 1200** (2) </span><span class="sxs-lookup"><span data-stu-id="3f03e-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-215">最大解析度為 1600 1200。</span><span class="sxs-lookup"><span data-stu-id="3f03e-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="3f03e-216"><span id="1920___1200"></span>**1920 \* 1200** (3) </span><span class="sxs-lookup"><span data-stu-id="3f03e-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-217">最大解析度為 1920 1200。</span><span class="sxs-lookup"><span data-stu-id="3f03e-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="3f03e-218"><span id="2560___1600"></span>**2560 \* 1600** (4) </span><span class="sxs-lookup"><span data-stu-id="3f03e-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-219">最大解析度為 2650 1600。</span><span class="sxs-lookup"><span data-stu-id="3f03e-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="3f03e-220"><span id="3840___2160"></span>**3840 \* 2160** (5) </span><span class="sxs-lookup"><span data-stu-id="3f03e-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3f03e-221">最大解析度為 3840 2160。</span><span class="sxs-lookup"><span data-stu-id="3f03e-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="3f03e-222">在 Windows 10 和 Windows Server 2016 中新增。 msvm \_ synte</span><span class="sxs-lookup"><span data-stu-id="3f03e-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3f03e-223">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3f03e-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-226">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="3f03e-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="3f03e-227">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-228">**父系**</span><span class="sxs-lookup"><span data-stu-id="3f03e-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-231">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="3f03e-231">The parent of the resource.</span></span> <span data-ttu-id="3f03e-232">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-233">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="3f03e-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-236">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f03e-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="3f03e-237">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-238">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="3f03e-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-239">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3f03e-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-241">保留給虛擬機器使用的 CPU 資源數量。</span><span class="sxs-lookup"><span data-stu-id="3f03e-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="3f03e-242">這些資源保證可供虛擬機器取用。</span><span class="sxs-lookup"><span data-stu-id="3f03e-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="3f03e-243">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3f03e-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-247">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="3f03e-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="3f03e-248">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="3f03e-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="3f03e-249">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3f03e-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-251">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3f03e-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-253">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="3f03e-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3f03e-254">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3f03e-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-256">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3f03e-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-258">虛擬機器的核心總數。</span><span class="sxs-lookup"><span data-stu-id="3f03e-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="3f03e-259">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-260">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="3f03e-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f03e-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-263">指定 **VirtualQuantity** 屬性的度量單位。</span><span class="sxs-lookup"><span data-stu-id="3f03e-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="3f03e-264">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="3f03e-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="3f03e-265">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f03e-266">**VRAMSizeBytes**</span><span class="sxs-lookup"><span data-stu-id="3f03e-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-267">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3f03e-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3f03e-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-269">虛擬機器的視訊記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="3f03e-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="3f03e-270">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="3f03e-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="3f03e-271"> (67108864) </span><span class="sxs-lookup"><span data-stu-id="3f03e-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f03e-272"> (134217728) </span><span class="sxs-lookup"><span data-stu-id="3f03e-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f03e-273"> (268435456) </span><span class="sxs-lookup"><span data-stu-id="3f03e-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f03e-274"> (536870912) </span><span class="sxs-lookup"><span data-stu-id="3f03e-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f03e-275"> (1073741824) </span><span class="sxs-lookup"><span data-stu-id="3f03e-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f03e-276">**Weight**</span><span class="sxs-lookup"><span data-stu-id="3f03e-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f03e-277">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3f03e-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f03e-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f03e-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f03e-279">為每個虛擬機器處理器定義權數的整數。</span><span class="sxs-lookup"><span data-stu-id="3f03e-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="3f03e-280">符合所有保留之後，裝載平臺的剩餘實體處理器容量將會根據其相對權數配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3f03e-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="3f03e-281">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="3f03e-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f03e-282">0</span><span class="sxs-lookup"><span data-stu-id="3f03e-282">0</span></span>

<span data-ttu-id="3f03e-283">範圍： 0 1000</span><span class="sxs-lookup"><span data-stu-id="3f03e-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f03e-284">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f03e-284">Requirements</span></span>



| <span data-ttu-id="3f03e-285">需求</span><span class="sxs-lookup"><span data-stu-id="3f03e-285">Requirement</span></span> | <span data-ttu-id="3f03e-286">值</span><span class="sxs-lookup"><span data-stu-id="3f03e-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f03e-287">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f03e-287">Minimum supported client</span></span><br/> | <span data-ttu-id="3f03e-288">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f03e-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f03e-289">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f03e-289">Minimum supported server</span></span><br/> | <span data-ttu-id="3f03e-290">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f03e-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f03e-291">命名空間</span><span class="sxs-lookup"><span data-stu-id="3f03e-291">Namespace</span></span><br/>                | <span data-ttu-id="3f03e-292">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3f03e-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f03e-293">MOF</span><span class="sxs-lookup"><span data-stu-id="3f03e-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f03e-294"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3f03e-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f03e-295">DLL</span><span class="sxs-lookup"><span data-stu-id="3f03e-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f03e-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f03e-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

