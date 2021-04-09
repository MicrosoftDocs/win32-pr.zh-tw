---
description: CIM \_ USBControllerHasHub 類別定義了 USB 控制器下游的中樞。
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: CIM_USBControllerHasHub 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110052"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="68b4b-103">CIM \_ USBControllerHasHub 類別</span><span class="sxs-lookup"><span data-stu-id="68b4b-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="68b4b-104">**CIM \_ USBControllerHasHub** 類別定義了 USB 控制器下游的中樞。</span><span class="sxs-lookup"><span data-stu-id="68b4b-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68b4b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="68b4b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68b4b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68b4b-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="68b4b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="68b4b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="68b4b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b4b-109">語法</span><span class="sxs-lookup"><span data-stu-id="68b4b-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="68b4b-110">成員</span><span class="sxs-lookup"><span data-stu-id="68b4b-110">Members</span></span>

<span data-ttu-id="68b4b-111">**CIM \_ USBControllerHasHub** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="68b4b-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="68b4b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="68b4b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68b4b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="68b4b-113">Properties</span></span>

<span data-ttu-id="68b4b-114">**CIM \_ USBControllerHasHub** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="68b4b-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68b4b-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="68b4b-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="68b4b-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-118">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="68b4b-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="68b4b-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="68b4b-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="68b4b-120">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68b4b-121">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="68b4b-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="68b4b-122">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="68b4b-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="68b4b-123">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="68b4b-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68b4b-124">**先行**</span><span class="sxs-lookup"><span data-stu-id="68b4b-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-125">資料類型： **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="68b4b-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="68b4b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-128">描述 USBController 的 [**CIM \_ USBController**](cim-usbcontroller.md) 。</span><span class="sxs-lookup"><span data-stu-id="68b4b-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="68b4b-129">**依賴**</span><span class="sxs-lookup"><span data-stu-id="68b4b-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-130">資料類型： **CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="68b4b-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="68b4b-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-133">[**CIM \_ USBHub**](cim-usbhub.md) ，描述與控制器相關聯的 USBHub。</span><span class="sxs-lookup"><span data-stu-id="68b4b-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="68b4b-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="68b4b-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68b4b-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-137">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="68b4b-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-138">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="68b4b-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="68b4b-139">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="68b4b-139">Data width is specified in bits.</span></span> <span data-ttu-id="68b4b-140">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="68b4b-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="68b4b-141">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="68b4b-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="68b4b-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="68b4b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-145">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="68b4b-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-146">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="68b4b-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="68b4b-147">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="68b4b-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="68b4b-148">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="68b4b-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="68b4b-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68b4b-150">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="68b4b-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="68b4b-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68b4b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-154">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="68b4b-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="68b4b-155">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="68b4b-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="68b4b-156">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="68b4b-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="68b4b-157">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="68b4b-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="68b4b-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68b4b-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68b4b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68b4b-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="68b4b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68b4b-161">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="68b4b-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="68b4b-162">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="68b4b-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="68b4b-163">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="68b4b-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="68b4b-164">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68b4b-165">備註</span><span class="sxs-lookup"><span data-stu-id="68b4b-165">Remarks</span></span>

<span data-ttu-id="68b4b-166">**Cim \_ USBControllerHasHub** 類別衍生自 [**cim \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="68b4b-167">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="68b4b-167">WMI does not implement this class.</span></span> <span data-ttu-id="68b4b-168">針對衍生自 **CIM \_ USBCONTROLLERHASHUB** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="68b4b-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="68b4b-169">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="68b4b-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68b4b-170">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="68b4b-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b4b-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="68b4b-171">Requirements</span></span>



| <span data-ttu-id="68b4b-172">需求</span><span class="sxs-lookup"><span data-stu-id="68b4b-172">Requirement</span></span> | <span data-ttu-id="68b4b-173">值</span><span class="sxs-lookup"><span data-stu-id="68b4b-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b4b-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68b4b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="68b4b-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68b4b-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68b4b-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68b4b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="68b4b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68b4b-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68b4b-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="68b4b-178">Namespace</span></span><br/>                | <span data-ttu-id="68b4b-179">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68b4b-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68b4b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="68b4b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68b4b-181"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="68b4b-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68b4b-182">DLL</span><span class="sxs-lookup"><span data-stu-id="68b4b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b4b-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b4b-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b4b-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68b4b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b4b-185">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="68b4b-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

