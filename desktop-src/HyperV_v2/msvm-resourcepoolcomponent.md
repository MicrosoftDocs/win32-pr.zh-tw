---
description: 表示 Microsoft Windows Hyper-v 平臺的資源集區元素。
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992056"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="9ff69-103">Msvm \_ ResourcePoolComponent 類別</span><span class="sxs-lookup"><span data-stu-id="9ff69-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="9ff69-104">表示 Microsoft Windows Hyper-v 平臺的資源集區元素。</span><span class="sxs-lookup"><span data-stu-id="9ff69-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="9ff69-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ff69-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff69-106">語法</span><span class="sxs-lookup"><span data-stu-id="9ff69-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="9ff69-107">成員</span><span class="sxs-lookup"><span data-stu-id="9ff69-107">Members</span></span>

<span data-ttu-id="9ff69-108">**Msvm \_ ResourcePoolComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9ff69-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9ff69-109">屬性</span><span class="sxs-lookup"><span data-stu-id="9ff69-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ff69-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9ff69-110">Properties</span></span>

<span data-ttu-id="9ff69-111">**Msvm \_ ResourcePoolComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9ff69-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ff69-112">**AllocationCapabilitiesClassName**</span><span class="sxs-lookup"><span data-stu-id="9ff69-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-115">衍生自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) 的類別名稱，可描述此資源集區的配置功能。</span><span class="sxs-lookup"><span data-stu-id="9ff69-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-116">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="9ff69-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-119">**GUID** ，表示服務 COM 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ff69-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="9ff69-120">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="9ff69-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-121">**內容**</span><span class="sxs-lookup"><span data-stu-id="9ff69-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ff69-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-124">新建立的物件將在其中執行的內容。</span><span class="sxs-lookup"><span data-stu-id="9ff69-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="9ff69-125">此值會在 *dwClsCoNtext* 參數中傳遞至 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="9ff69-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="9ff69-126">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="9ff69-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="9ff69-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9ff69-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-130">如果這個實例已啟用，而且可以用來完成用戶端要求，則為 **True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="9ff69-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="9ff69-131">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="9ff69-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-132">**MaxParentPools**</span><span class="sxs-lookup"><span data-stu-id="9ff69-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-133">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9ff69-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-135">子集區支援的父資源集區數目上限。</span><span class="sxs-lookup"><span data-stu-id="9ff69-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-136">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9ff69-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-139">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9ff69-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-140">特定語言的字串，可唯一識別元素。</span><span class="sxs-lookup"><span data-stu-id="9ff69-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="9ff69-141">建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。</span><span class="sxs-lookup"><span data-stu-id="9ff69-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="9ff69-142">例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。</span><span class="sxs-lookup"><span data-stu-id="9ff69-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="9ff69-143">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="9ff69-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-144">**PhysicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="9ff69-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-147">衍生自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 的類別名稱，這個類別會從這個集區配置資源的實體裝置。</span><span class="sxs-lookup"><span data-stu-id="9ff69-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="9ff69-148">如果配置自這個集區的虛擬裝置類別與實體裝置類別相同，則此屬性可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9ff69-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-149">**ResourcePoolClassName**</span><span class="sxs-lookup"><span data-stu-id="9ff69-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-152">從執行資源集區之 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) 衍生的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9ff69-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-153">**ResourcePoolSettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="9ff69-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-156">衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) 的類別名稱，此名稱會描述資源集區的非配置相關設定。</span><span class="sxs-lookup"><span data-stu-id="9ff69-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="9ff69-157">**WmiFactoryCLSID**</span><span class="sxs-lookup"><span data-stu-id="9ff69-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff69-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ff69-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff69-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ff69-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff69-160">**GUID** ，表示元件之 WMI 物件 factory 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ff69-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ff69-161">備註</span><span class="sxs-lookup"><span data-stu-id="9ff69-161">Remarks</span></span>

<span data-ttu-id="9ff69-162">存取 **Msvm \_ ResourcePoolComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9ff69-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9ff69-163">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9ff69-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff69-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ff69-164">Requirements</span></span>



| <span data-ttu-id="9ff69-165">需求</span><span class="sxs-lookup"><span data-stu-id="9ff69-165">Requirement</span></span> | <span data-ttu-id="9ff69-166">值</span><span class="sxs-lookup"><span data-stu-id="9ff69-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff69-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ff69-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff69-168">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ff69-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9ff69-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ff69-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff69-170">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ff69-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ff69-171">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9ff69-171">End of client support</span></span><br/>    | <span data-ttu-id="9ff69-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9ff69-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9ff69-173">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9ff69-173">End of server support</span></span><br/>    | <span data-ttu-id="9ff69-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9ff69-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9ff69-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="9ff69-175">Namespace</span></span><br/>                | <span data-ttu-id="9ff69-176">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9ff69-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9ff69-177">MOF</span><span class="sxs-lookup"><span data-stu-id="9ff69-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ff69-178"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9ff69-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ff69-179">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff69-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff69-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ff69-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9ff69-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ff69-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff69-182">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="9ff69-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="9ff69-183">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="9ff69-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

