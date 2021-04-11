---
description: CIM \_ ControlledBy 關聯性會指出哪些裝置是由控制器邏輯裝置所發出或存取。
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: 'CIM_ControlledBy 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847248"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="d3ddc-103">CIM_ControlledBy 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d3ddc-104">**CIM \_ ControlledBy** 關聯性會指出哪些裝置是由控制器邏輯裝置所發出或存取。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3ddc-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d3ddc-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d3ddc-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d3ddc-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ddc-109">語法</span><span class="sxs-lookup"><span data-stu-id="d3ddc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="d3ddc-110">成員</span><span class="sxs-lookup"><span data-stu-id="d3ddc-110">Members</span></span>

<span data-ttu-id="d3ddc-111">**CIM \_ ControlledBy** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3ddc-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="d3ddc-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d3ddc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3ddc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d3ddc-113">Properties</span></span>

<span data-ttu-id="d3ddc-114">**CIM \_ ControlledBy** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3ddc-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-118">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="d3ddc-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d3ddc-120">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="d3ddc-121">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="d3ddc-122">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d3ddc-123">**先行**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-124">資料類型： **CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-126">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-127">代表控制器的 [**CIM \_ 控制器**](cim-controller.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="d3ddc-128">**依賴**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-129">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-131">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-132">代表受控制裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="d3ddc-133">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-136">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-137">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="d3ddc-138">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-138">Data width is specified in bits.</span></span> <span data-ttu-id="d3ddc-139">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d3ddc-140">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3ddc-141">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-142">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-144">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="d3ddc-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-145">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="d3ddc-146">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="d3ddc-147">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d3ddc-148">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d3ddc-149">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3ddc-150">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-153">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="d3ddc-154">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="d3ddc-155">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="d3ddc-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ddc-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3ddc-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ddc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3ddc-159">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="d3ddc-160">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="d3ddc-161">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3ddc-162">備註</span><span class="sxs-lookup"><span data-stu-id="d3ddc-162">Remarks</span></span>

<span data-ttu-id="d3ddc-163">**Cim \_ ControlledBy** 類別衍生自 [**cim \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="d3ddc-164">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-164">WMI does not implement this class.</span></span> <span data-ttu-id="d3ddc-165">如需衍生自 **CIM \_ ControlledBy** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d3ddc-166">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d3ddc-167">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d3ddc-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ddc-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3ddc-168">Requirements</span></span>



| <span data-ttu-id="d3ddc-169">需求</span><span class="sxs-lookup"><span data-stu-id="d3ddc-169">Requirement</span></span> | <span data-ttu-id="d3ddc-170">值</span><span class="sxs-lookup"><span data-stu-id="d3ddc-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ddc-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3ddc-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ddc-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3ddc-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3ddc-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3ddc-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ddc-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3ddc-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3ddc-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3ddc-175">Namespace</span></span><br/>                | <span data-ttu-id="d3ddc-176">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d3ddc-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3ddc-177">MOF</span><span class="sxs-lookup"><span data-stu-id="d3ddc-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3ddc-178"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3ddc-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3ddc-179">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ddc-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ddc-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ddc-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3ddc-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3ddc-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ddc-182">**CIM \_ DeviceConnection**</span><span class="sxs-lookup"><span data-stu-id="d3ddc-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

