---
description: 代表 CIM \_ ControlledBy 關聯性，指出哪些裝置可透過 SCSI 控制器和存取特性來存取。
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: CIM_SCSIInterface 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688975"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="15e2d-103">CIM \_ SCSIInterface 類別</span><span class="sxs-lookup"><span data-stu-id="15e2d-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="15e2d-104">**Cim \_ SCSIInterface** 類別代表 [**cim \_ ControlledBy**](cim-controlledby.md)關聯性，指出哪些裝置可透過 SCSI 控制器和存取特性來存取。</span><span class="sxs-lookup"><span data-stu-id="15e2d-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15e2d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="15e2d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15e2d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="15e2d-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="15e2d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="15e2d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="15e2d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e2d-109">語法</span><span class="sxs-lookup"><span data-stu-id="15e2d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="15e2d-110">成員</span><span class="sxs-lookup"><span data-stu-id="15e2d-110">Members</span></span>

<span data-ttu-id="15e2d-111">**CIM \_ SCSIInterface** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15e2d-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="15e2d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="15e2d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15e2d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="15e2d-113">Properties</span></span>

<span data-ttu-id="15e2d-114">**CIM \_ SCSIInterface** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15e2d-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15e2d-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="15e2d-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="15e2d-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-118">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="15e2d-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="15e2d-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="15e2d-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="15e2d-120">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15e2d-121">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="15e2d-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="15e2d-122">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="15e2d-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="15e2d-123">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="15e2d-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15e2d-124">**先行**</span><span class="sxs-lookup"><span data-stu-id="15e2d-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-125">資料類型： **CIM \_ microsoft.hyperv.powershell.scsicontroller**</span><span class="sxs-lookup"><span data-stu-id="15e2d-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="15e2d-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-128">描述 SCSI 控制器的 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md) 。</span><span class="sxs-lookup"><span data-stu-id="15e2d-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-129">**依賴**</span><span class="sxs-lookup"><span data-stu-id="15e2d-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-130">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="15e2d-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="15e2d-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-133">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="15e2d-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="15e2d-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15e2d-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-137">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="15e2d-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-138">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="15e2d-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="15e2d-139">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="15e2d-139">Data width is specified in bits.</span></span> <span data-ttu-id="15e2d-140">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="15e2d-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="15e2d-141">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="15e2d-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="15e2d-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-145">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="15e2d-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-146">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="15e2d-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="15e2d-147">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="15e2d-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="15e2d-148">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="15e2d-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="15e2d-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="15e2d-150">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="15e2d-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15e2d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-154">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="15e2d-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="15e2d-155">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="15e2d-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="15e2d-156">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="15e2d-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="15e2d-157">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="15e2d-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15e2d-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-161">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="15e2d-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="15e2d-162">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="15e2d-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="15e2d-163">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="15e2d-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="15e2d-164">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-165">**SCSIRetries**</span><span class="sxs-lookup"><span data-stu-id="15e2d-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15e2d-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-168">自上次與受控制裝置相關的硬重設和軟重設之後，所發生的 SCSI 重試次數。</span><span class="sxs-lookup"><span data-stu-id="15e2d-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="15e2d-169">上次重設的時間會在 **TimeOfDeviceReset** 屬性中指出，此屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="15e2d-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="15e2d-170">**SCSITimeouts**</span><span class="sxs-lookup"><span data-stu-id="15e2d-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2d-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15e2d-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2d-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15e2d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2d-173">自上次硬性或軟重設（與受控制裝置相關）以來發生的 SCSI 超時時間。</span><span class="sxs-lookup"><span data-stu-id="15e2d-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="15e2d-174">上次重設的時間會在 **TimeOfDeviceReset** 屬性中指出，此屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="15e2d-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15e2d-175">備註</span><span class="sxs-lookup"><span data-stu-id="15e2d-175">Remarks</span></span>

<span data-ttu-id="15e2d-176">**Cim \_ SCSIInterface** 類別衍生自 [**cim \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="15e2d-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="15e2d-177">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="15e2d-177">WMI does not implement this class.</span></span>

<span data-ttu-id="15e2d-178">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="15e2d-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15e2d-179">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="15e2d-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e2d-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="15e2d-180">Requirements</span></span>



| <span data-ttu-id="15e2d-181">需求</span><span class="sxs-lookup"><span data-stu-id="15e2d-181">Requirement</span></span> | <span data-ttu-id="15e2d-182">值</span><span class="sxs-lookup"><span data-stu-id="15e2d-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15e2d-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15e2d-183">Minimum supported client</span></span><br/> | <span data-ttu-id="15e2d-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15e2d-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15e2d-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15e2d-185">Minimum supported server</span></span><br/> | <span data-ttu-id="15e2d-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15e2d-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15e2d-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="15e2d-187">Namespace</span></span><br/>                | <span data-ttu-id="15e2d-188">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15e2d-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15e2d-189">MOF</span><span class="sxs-lookup"><span data-stu-id="15e2d-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15e2d-190"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="15e2d-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15e2d-191">DLL</span><span class="sxs-lookup"><span data-stu-id="15e2d-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e2d-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e2d-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e2d-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15e2d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e2d-194">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="15e2d-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

