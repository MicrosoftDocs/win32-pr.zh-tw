---
description: 代表控制器與受控制器管理的邏輯裝置之間的關聯性。
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: 'CIM_ControlledBy 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848295"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="ac077-103">CIM_ControlledBy 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="ac077-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="ac077-104">代表控制器與受控制器管理的邏輯裝置之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ac077-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac077-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac077-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="ac077-106">成員</span><span class="sxs-lookup"><span data-stu-id="ac077-106">Members</span></span>

<span data-ttu-id="ac077-107">**CIM \_ ControlledBy** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac077-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="ac077-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ac077-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac077-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ac077-109">Properties</span></span>

<span data-ttu-id="ac077-110">**CIM \_ ControlledBy** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ac077-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac077-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="ac077-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ac077-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac077-114">此屬性描述裝置透過控制器的存取範圍。</span><span class="sxs-lookup"><span data-stu-id="ac077-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="ac077-115">**ReadWrite** (2) </span><span class="sxs-lookup"><span data-stu-id="ac077-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="ac077-116">**ReadOnly** (3) </span><span class="sxs-lookup"><span data-stu-id="ac077-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="ac077-117">**NoAccess** (4) </span><span class="sxs-lookup"><span data-stu-id="ac077-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac077-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="ac077-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ac077-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac077-121">透過控制器存取裝置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac077-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="ac077-122">較低的值表示較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac077-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-123">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="ac077-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ac077-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac077-126">指出控制器是否正在主動管理裝置。</span><span class="sxs-lookup"><span data-stu-id="ac077-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac077-127">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ac077-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ac077-128">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="ac077-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ac077-129">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="ac077-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac077-130">**先行**</span><span class="sxs-lookup"><span data-stu-id="ac077-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-131">資料類型： **CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="ac077-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac077-133">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="ac077-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ac077-134">控制器。</span><span class="sxs-lookup"><span data-stu-id="ac077-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-135">**依賴**</span><span class="sxs-lookup"><span data-stu-id="ac077-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-136">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ac077-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac077-138">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="ac077-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ac077-139">邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="ac077-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-140">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="ac077-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac077-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac077-143">控制器內容中相關聯裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="ac077-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-144">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="ac077-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ac077-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac077-147">限定詞： **計數器**</span><span class="sxs-lookup"><span data-stu-id="ac077-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ac077-148">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="ac077-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="ac077-149">硬重設會將裝置傳回到其初始化或啟動狀態，之後所有的內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="ac077-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-150">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="ac077-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ac077-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac077-153">限定詞： **計數器**</span><span class="sxs-lookup"><span data-stu-id="ac077-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ac077-154">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="ac077-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="ac077-155">軟重設不會清除裝置狀態或資料。</span><span class="sxs-lookup"><span data-stu-id="ac077-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="ac077-156">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="ac077-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac077-157">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ac077-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac077-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac077-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac077-159">控制器上次重設下游裝置的時間。</span><span class="sxs-lookup"><span data-stu-id="ac077-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac077-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac077-160">Requirements</span></span>



| <span data-ttu-id="ac077-161">需求</span><span class="sxs-lookup"><span data-stu-id="ac077-161">Requirement</span></span> | <span data-ttu-id="ac077-162">值</span><span class="sxs-lookup"><span data-stu-id="ac077-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac077-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac077-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ac077-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac077-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ac077-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac077-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ac077-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac077-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ac077-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac077-167">Namespace</span></span><br/>                | <span data-ttu-id="ac077-168">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ac077-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac077-169">MOF</span><span class="sxs-lookup"><span data-stu-id="ac077-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac077-170"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ac077-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac077-171">DLL</span><span class="sxs-lookup"><span data-stu-id="ac077-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac077-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac077-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac077-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac077-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac077-174">**CIM \_ DeviceConnection**</span><span class="sxs-lookup"><span data-stu-id="ac077-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

