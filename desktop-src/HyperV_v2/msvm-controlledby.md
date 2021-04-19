---
description: 將存放裝置與擁有裝置的儲存控制器產生關聯。
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990416"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="b7771-103">Msvm \_ ControlledBy 類別</span><span class="sxs-lookup"><span data-stu-id="b7771-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="b7771-104">將存放裝置與擁有裝置的儲存控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b7771-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="b7771-105">此關聯會與 IDE 和磁碟控制卡一起使用。</span><span class="sxs-lookup"><span data-stu-id="b7771-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="b7771-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b7771-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7771-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7771-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="b7771-108">成員</span><span class="sxs-lookup"><span data-stu-id="b7771-108">Members</span></span>

<span data-ttu-id="b7771-109">**Msvm \_ ControlledBy** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b7771-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="b7771-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b7771-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7771-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b7771-111">Properties</span></span>

<span data-ttu-id="b7771-112">**Msvm \_ ControlledBy** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b7771-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7771-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="b7771-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b7771-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-116">透過前一個控制器存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="b7771-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="b7771-117">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為 2 (讀取/寫入) 。</span><span class="sxs-lookup"><span data-stu-id="b7771-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="b7771-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="b7771-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b7771-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-121">透過此控制器存取裝置所提供的優先權。</span><span class="sxs-lookup"><span data-stu-id="b7771-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="b7771-122">最高優先順序的路徑會有最小值。</span><span class="sxs-lookup"><span data-stu-id="b7771-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="b7771-123">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="b7771-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7771-124">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="b7771-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b7771-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-127">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="b7771-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="b7771-128">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為 1 (作用中) 。</span><span class="sxs-lookup"><span data-stu-id="b7771-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="b7771-129">**先行**</span><span class="sxs-lookup"><span data-stu-id="b7771-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-130">資料類型： **[ **CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="b7771-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-132">控制器的參考。</span><span class="sxs-lookup"><span data-stu-id="b7771-132">A reference to the controller.</span></span> <span data-ttu-id="b7771-133">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。</span><span class="sxs-lookup"><span data-stu-id="b7771-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="b7771-134">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b7771-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-135">資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="b7771-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-137">受控制裝置的參考。</span><span class="sxs-lookup"><span data-stu-id="b7771-137">A reference to the controlled device.</span></span> <span data-ttu-id="b7771-138">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。</span><span class="sxs-lookup"><span data-stu-id="b7771-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="b7771-139">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="b7771-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b7771-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-142">前一個控制器內容中相關聯裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="b7771-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="b7771-143">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。</span><span class="sxs-lookup"><span data-stu-id="b7771-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="b7771-144">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="b7771-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b7771-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-147">這個屬性繼承自 [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="b7771-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7771-148">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b7771-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-149">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b7771-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-151">這個屬性繼承自 [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="b7771-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7771-152">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="b7771-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b7771-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-155">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b7771-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b7771-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="b7771-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b7771-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-159">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b7771-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b7771-160">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="b7771-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7771-161">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b7771-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7771-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b7771-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7771-163">這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b7771-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7771-164">備註</span><span class="sxs-lookup"><span data-stu-id="b7771-164">Remarks</span></span>

<span data-ttu-id="b7771-165">存取 **Msvm \_ ControlledBy** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="b7771-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b7771-166">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="b7771-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7771-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7771-167">Requirements</span></span>



| <span data-ttu-id="b7771-168">需求</span><span class="sxs-lookup"><span data-stu-id="b7771-168">Requirement</span></span> | <span data-ttu-id="b7771-169">值</span><span class="sxs-lookup"><span data-stu-id="b7771-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7771-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7771-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b7771-171">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7771-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b7771-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7771-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b7771-173">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7771-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7771-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="b7771-174">Namespace</span></span><br/>                | <span data-ttu-id="b7771-175">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b7771-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b7771-176">MOF</span><span class="sxs-lookup"><span data-stu-id="b7771-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7771-177"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b7771-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7771-178">DLL</span><span class="sxs-lookup"><span data-stu-id="b7771-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7771-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7771-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7771-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7771-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7771-181">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="b7771-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="b7771-182">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="b7771-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="b7771-183">儲存類別</span><span class="sxs-lookup"><span data-stu-id="b7771-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

