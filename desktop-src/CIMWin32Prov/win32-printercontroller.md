---
description: Win32 \_ PrinterController 關聯 WMI 類別會使印表機和印表機所連線的本機裝置產生關聯。 請注意，這個類別只會傳回本機印表機的實例。
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847321"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="5bccf-104">Win32 \_ PrinterController 類別</span><span class="sxs-lookup"><span data-stu-id="5bccf-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="5bccf-105">**Win32 \_ PrinterController** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會使印表機和印表機所連線的本機裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5bccf-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="5bccf-106">請注意，這個類別只會傳回本機印表機的實例。</span><span class="sxs-lookup"><span data-stu-id="5bccf-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="5bccf-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bccf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5bccf-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5bccf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bccf-109">語法</span><span class="sxs-lookup"><span data-stu-id="5bccf-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="5bccf-110">成員</span><span class="sxs-lookup"><span data-stu-id="5bccf-110">Members</span></span>

<span data-ttu-id="5bccf-111">**Win32 \_ PrinterController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5bccf-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="5bccf-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5bccf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bccf-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5bccf-113">Properties</span></span>

<span data-ttu-id="5bccf-114">**Win32 \_ PrinterController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5bccf-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bccf-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="5bccf-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5bccf-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-118">控制器存取裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="5bccf-118">State of the controller access to the device.</span></span> <span data-ttu-id="5bccf-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="5bccf-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="5bccf-120">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="5bccf-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="5bccf-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="5bccf-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="5bccf-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="5bccf-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="5bccf-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="5bccf-124">使用中</span><span class="sxs-lookup"><span data-stu-id="5bccf-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="5bccf-125"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="5bccf-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="5bccf-126">非使用中</span><span class="sxs-lookup"><span data-stu-id="5bccf-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5bccf-127">**先行**</span><span class="sxs-lookup"><span data-stu-id="5bccf-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-128">資料類型： **CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="5bccf-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-130">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5bccf-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-131">參考 [**CIM \_ 控制器**](cim-controller.md) 實例，代表與此印表機相關聯的本機裝置。</span><span class="sxs-lookup"><span data-stu-id="5bccf-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="5bccf-132">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="5bccf-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bccf-133">**依賴**</span><span class="sxs-lookup"><span data-stu-id="5bccf-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-134">資料類型： **Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="5bccf-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-136">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5bccf-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-137">[**Win32 \_ 印表機**](win32-printer.md)實例的參考，代表與本機裝置相關聯的印表機。</span><span class="sxs-lookup"><span data-stu-id="5bccf-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="5bccf-138">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="5bccf-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bccf-139">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5bccf-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5bccf-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-142">當有多個匯流排或連接資料寬度) 時，裝置之間的使用資料寬度 (。</span><span class="sxs-lookup"><span data-stu-id="5bccf-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="5bccf-143">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="5bccf-143">Data width is specified in bits.</span></span> <span data-ttu-id="5bccf-144">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5bccf-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5bccf-145">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bccf-146">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="5bccf-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-147">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5bccf-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-149">當) 可能有數個匯流排或連線速度時，裝置 (的使用速度。</span><span class="sxs-lookup"><span data-stu-id="5bccf-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="5bccf-150">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="5bccf-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="5bccf-151">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5bccf-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5bccf-152">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="5bccf-153">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bccf-154">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="5bccf-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5bccf-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-157">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="5bccf-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="5bccf-158">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bccf-159">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="5bccf-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bccf-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5bccf-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bccf-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bccf-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bccf-162">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="5bccf-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="5bccf-163">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bccf-164">備註</span><span class="sxs-lookup"><span data-stu-id="5bccf-164">Remarks</span></span>

<span data-ttu-id="5bccf-165">**Win32 \_ PrinterController** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5bccf-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bccf-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bccf-166">Requirements</span></span>



| <span data-ttu-id="5bccf-167">需求</span><span class="sxs-lookup"><span data-stu-id="5bccf-167">Requirement</span></span> | <span data-ttu-id="5bccf-168">值</span><span class="sxs-lookup"><span data-stu-id="5bccf-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bccf-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bccf-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5bccf-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bccf-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5bccf-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bccf-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5bccf-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bccf-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5bccf-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="5bccf-173">Namespace</span></span><br/>                | <span data-ttu-id="5bccf-174">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5bccf-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5bccf-175">MOF</span><span class="sxs-lookup"><span data-stu-id="5bccf-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bccf-176"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bccf-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bccf-177">DLL</span><span class="sxs-lookup"><span data-stu-id="5bccf-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bccf-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bccf-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5bccf-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bccf-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bccf-180">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="5bccf-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="5bccf-181">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5bccf-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
