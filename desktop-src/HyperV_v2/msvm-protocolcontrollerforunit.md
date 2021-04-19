---
description: 此關聯表示邏輯裝置的子類別 (例如，存放磁片區) 透過特定的通訊協定控制器連線。
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986845"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="64894-103">Msvm \_ ProtocolControllerForUnit 類別</span><span class="sxs-lookup"><span data-stu-id="64894-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="64894-104">此關聯表示邏輯裝置的子類別 (例如，存放磁片區) 透過特定的通訊協定控制器連線。</span><span class="sxs-lookup"><span data-stu-id="64894-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="64894-105">在許多情況下 (例如儲存體 LUN 遮罩) ，可能會有許多這些關聯與不同的物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="64894-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="64894-106">因此，已定義子類別來優化關聯的列舉。</span><span class="sxs-lookup"><span data-stu-id="64894-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="64894-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="64894-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64894-108">語法</span><span class="sxs-lookup"><span data-stu-id="64894-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="64894-109">成員</span><span class="sxs-lookup"><span data-stu-id="64894-109">Members</span></span>

<span data-ttu-id="64894-110">**Msvm \_ ProtocolControllerForUnit** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64894-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="64894-111">屬性</span><span class="sxs-lookup"><span data-stu-id="64894-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64894-112">屬性</span><span class="sxs-lookup"><span data-stu-id="64894-112">Properties</span></span>

<span data-ttu-id="64894-113">**Msvm \_ ProtocolControllerForUnit** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="64894-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64894-114">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="64894-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-115">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64894-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64894-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-117">透過此控制器存取裝置所提供的優先權。</span><span class="sxs-lookup"><span data-stu-id="64894-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="64894-118">最高優先順序的路徑會有此參數的最小值。</span><span class="sxs-lookup"><span data-stu-id="64894-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="64894-119">此類別繼承自 **CIM \_ ProtocolControllerForDevice**。</span><span class="sxs-lookup"><span data-stu-id="64894-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="64894-120">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="64894-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-121">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64894-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64894-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-123">指出控制器是否正在主動命令或存取裝置 (2) 或不 (3) 。</span><span class="sxs-lookup"><span data-stu-id="64894-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="64894-124">此外，也可以定義值 0 (未知的) ）。</span><span class="sxs-lookup"><span data-stu-id="64894-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="64894-125">當邏輯裝置可透過多個通訊協定控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="64894-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="64894-126">此類別繼承自 **CIM \_ ProtocolControllerForDevice**。</span><span class="sxs-lookup"><span data-stu-id="64894-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="64894-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="64894-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64894-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2) </span><span class="sxs-lookup"><span data-stu-id="64894-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="64894-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**非** 使用中 (3 ) </span><span class="sxs-lookup"><span data-stu-id="64894-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64894-130">**先行**</span><span class="sxs-lookup"><span data-stu-id="64894-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-131">資料類型： **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="64894-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="64894-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-133">通訊協定控制器。</span><span class="sxs-lookup"><span data-stu-id="64894-133">The protocol controller.</span></span> <span data-ttu-id="64894-134">此類別繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="64894-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="64894-135">**依賴**</span><span class="sxs-lookup"><span data-stu-id="64894-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-136">資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="64894-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="64894-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-138">受控制的裝置。</span><span class="sxs-lookup"><span data-stu-id="64894-138">The controlled device.</span></span> <span data-ttu-id="64894-139">此類別繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="64894-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="64894-140">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="64894-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64894-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64894-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-143">透過此控制器授與裝置的存取權限。</span><span class="sxs-lookup"><span data-stu-id="64894-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="64894-144">此類別繼承自 **CIM \_ ProtocolControllerForUnit**。</span><span class="sxs-lookup"><span data-stu-id="64894-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="64894-145">值</span><span class="sxs-lookup"><span data-stu-id="64894-145">Value</span></span>                                                                               | <span data-ttu-id="64894-146">意義</span><span class="sxs-lookup"><span data-stu-id="64894-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="64894-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64894-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="64894-148">Unknown</span><span class="sxs-lookup"><span data-stu-id="64894-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="64894-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="64894-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="64894-150">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="64894-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="64894-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="64894-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="64894-152">唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="64894-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="64894-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="64894-154">沒有存取權。</span><span class="sxs-lookup"><span data-stu-id="64894-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="64894-155"><dt>5. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="64894-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="64894-156">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="64894-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="64894-157"><dt>16000 .。。</dt></span><span class="sxs-lookup"><span data-stu-id="64894-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="64894-158">保留的廠商</span><span class="sxs-lookup"><span data-stu-id="64894-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64894-159">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="64894-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64894-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64894-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64894-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64894-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64894-162">前一個控制器內容中相關聯裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="64894-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="64894-163">此類別繼承自 **CIM \_ ProtocolControllerForDevice**。</span><span class="sxs-lookup"><span data-stu-id="64894-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64894-164">備註</span><span class="sxs-lookup"><span data-stu-id="64894-164">Remarks</span></span>

<span data-ttu-id="64894-165">存取 **Msvm \_ ProtocolControllerForUnit** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="64894-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="64894-166">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="64894-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="64894-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="64894-167">Requirements</span></span>



| <span data-ttu-id="64894-168">需求</span><span class="sxs-lookup"><span data-stu-id="64894-168">Requirement</span></span> | <span data-ttu-id="64894-169">值</span><span class="sxs-lookup"><span data-stu-id="64894-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64894-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64894-170">Minimum supported client</span></span><br/> | <span data-ttu-id="64894-171">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64894-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64894-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64894-172">Minimum supported server</span></span><br/> | <span data-ttu-id="64894-173">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64894-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64894-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="64894-174">Namespace</span></span><br/>                | <span data-ttu-id="64894-175">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="64894-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64894-176">MOF</span><span class="sxs-lookup"><span data-stu-id="64894-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64894-177"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="64894-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64894-178">DLL</span><span class="sxs-lookup"><span data-stu-id="64894-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64894-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64894-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64894-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64894-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64894-181">**CIM \_ ProtocolControllerForUnit**</span><span class="sxs-lookup"><span data-stu-id="64894-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="64894-182">[**CIM \_ ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64894-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="64894-183">儲存類別</span><span class="sxs-lookup"><span data-stu-id="64894-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

