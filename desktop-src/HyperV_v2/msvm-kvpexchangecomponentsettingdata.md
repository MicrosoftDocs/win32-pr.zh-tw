---
description: 代表索引鍵/值組 exchange 服務的設定狀態。
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Msvm_KvpExchangeComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988782"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="a9365-103">Msvm \_ KvpExchangeComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="a9365-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="a9365-104">代表索引鍵/值組 exchange 服務的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="a9365-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="a9365-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9365-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9365-106">語法</span><span class="sxs-lookup"><span data-stu-id="a9365-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="a9365-107">成員</span><span class="sxs-lookup"><span data-stu-id="a9365-107">Members</span></span>

<span data-ttu-id="a9365-108">**Msvm \_ KvpExchangeComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9365-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a9365-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a9365-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9365-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a9365-110">Properties</span></span>

<span data-ttu-id="a9365-111">**Msvm \_ KvpExchangeComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a9365-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9365-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="a9365-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="a9365-115">The address of the resource.</span></span> <span data-ttu-id="a9365-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9365-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="a9365-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="a9365-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="a9365-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="a9365-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="a9365-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="a9365-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="a9365-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="a9365-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="a9365-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9365-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="a9365-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="a9365-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="a9365-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9365-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-136">指出是否會自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="a9365-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="a9365-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="a9365-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a9365-141">A short description of the object.</span></span> <span data-ttu-id="a9365-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a9365-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-143">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="a9365-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-144">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a9365-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9365-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-146">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="a9365-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="a9365-147">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9365-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="a9365-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a9365-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-151">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="a9365-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="a9365-152">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="a9365-153">值</span><span class="sxs-lookup"><span data-stu-id="a9365-153">Value</span></span>                                                                        | <span data-ttu-id="a9365-154">意義</span><span class="sxs-lookup"><span data-stu-id="a9365-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a9365-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9365-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a9365-156">虛擬</span><span class="sxs-lookup"><span data-stu-id="a9365-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9365-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="a9365-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a9365-160">A description of the object.</span></span> <span data-ttu-id="a9365-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a9365-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-162">**DisableHostKVPItems**</span><span class="sxs-lookup"><span data-stu-id="a9365-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-163">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a9365-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9365-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a9365-165">此屬性會停用主機，使其無法自動 populatinghost 來賓內的名稱和作業系統資訊。</span><span class="sxs-lookup"><span data-stu-id="a9365-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="a9365-166">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="a9365-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="a9365-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9365-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-170">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a9365-170">A display name for the object.</span></span> <span data-ttu-id="a9365-171">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a9365-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a9365-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a9365-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-175">元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a9365-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a9365-176">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="a9365-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a9365-177">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="a9365-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9365-178">**HostExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="a9365-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-179">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a9365-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="a9365-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9365-181">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) </span><span class="sxs-lookup"><span data-stu-id="a9365-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="a9365-182">代表索引鍵/值組的內嵌 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 實例陣列。</span><span class="sxs-lookup"><span data-stu-id="a9365-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-183">**HostOnlyItems**</span><span class="sxs-lookup"><span data-stu-id="a9365-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-184">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a9365-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="a9365-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9365-186">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) </span><span class="sxs-lookup"><span data-stu-id="a9365-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="a9365-187">[**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)實例的陣列，其中包含儲存在設定檔中但未與客體作業系統交換的索引鍵/值組。</span><span class="sxs-lookup"><span data-stu-id="a9365-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="a9365-188">這可讓應用程式儲存客體作業系統不需要看見的虛擬機器專屬資料。</span><span class="sxs-lookup"><span data-stu-id="a9365-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="a9365-189">專案的格式與 **HostExchangeItems** 屬性中的專案相同，不同之處在于 **Msvm \_ KvpExchangeDataItem** 實例的 [**來源**] 屬性設定為 [4]。</span><span class="sxs-lookup"><span data-stu-id="a9365-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="a9365-190">每個設定檔的限制為128個索引鍵/值組，其中每個值欄位的大小上限為 16 KB，而索引鍵欄位則允許最多512個位元組。</span><span class="sxs-lookup"><span data-stu-id="a9365-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-191">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="a9365-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-192">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a9365-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9365-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-194">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="a9365-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="a9365-195">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9365-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9365-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9365-199">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a9365-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a9365-200">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a9365-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a9365-201">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a9365-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-202">**限制**</span><span class="sxs-lookup"><span data-stu-id="a9365-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a9365-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-205">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="a9365-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="a9365-206">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="a9365-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a9365-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-210">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="a9365-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="a9365-211">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9365-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="a9365-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-215">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="a9365-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="a9365-216">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-217">**父系**</span><span class="sxs-lookup"><span data-stu-id="a9365-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-220">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="a9365-220">The parent of the resource.</span></span> <span data-ttu-id="a9365-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a9365-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9365-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="a9365-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-225">從中配置資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9365-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="a9365-226">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-227">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="a9365-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a9365-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-230">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="a9365-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="a9365-231">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a9365-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-235">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="a9365-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="a9365-236">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a9365-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a9365-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-240">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="a9365-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="a9365-241">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="a9365-242">值</span><span class="sxs-lookup"><span data-stu-id="a9365-242">Value</span></span>                                                                        | <span data-ttu-id="a9365-243">意義</span><span class="sxs-lookup"><span data-stu-id="a9365-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="a9365-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a9365-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a9365-245">其他</span><span class="sxs-lookup"><span data-stu-id="a9365-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9365-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="a9365-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-247">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a9365-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-249">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="a9365-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="a9365-250">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-251">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="a9365-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9365-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-254">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="a9365-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="a9365-255">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="a9365-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="a9365-256">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a9365-257">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a9365-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9365-258">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a9365-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9365-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9365-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9365-260">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="a9365-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="a9365-261">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a9365-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9365-262">備註</span><span class="sxs-lookup"><span data-stu-id="a9365-262">Remarks</span></span>

<span data-ttu-id="a9365-263">存取 **Msvm \_ KvpExchangeComponentSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a9365-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a9365-264">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a9365-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9365-265">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9365-265">Requirements</span></span>



| <span data-ttu-id="a9365-266">需求</span><span class="sxs-lookup"><span data-stu-id="a9365-266">Requirement</span></span> | <span data-ttu-id="a9365-267">值</span><span class="sxs-lookup"><span data-stu-id="a9365-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9365-268">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9365-268">Minimum supported client</span></span><br/> | <span data-ttu-id="a9365-269">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9365-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9365-270">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9365-270">Minimum supported server</span></span><br/> | <span data-ttu-id="a9365-271">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9365-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9365-272">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9365-272">Namespace</span></span><br/>                | <span data-ttu-id="a9365-273">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a9365-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9365-274">MOF</span><span class="sxs-lookup"><span data-stu-id="a9365-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9365-275"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a9365-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9365-276">DLL</span><span class="sxs-lookup"><span data-stu-id="a9365-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9365-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9365-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9365-278">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9365-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9365-279">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="a9365-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="a9365-280">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="a9365-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

