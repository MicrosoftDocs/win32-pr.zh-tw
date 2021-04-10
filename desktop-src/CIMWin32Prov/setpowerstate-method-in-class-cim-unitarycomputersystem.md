---
description: CIM UnitaryComputerSystem 類別的 SetPowerState 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: CIM_UnitaryComputerSystem 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936055"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="269a0-103">CIM UnitaryComputerSystem 類別的 SetPowerState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="269a0-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="269a0-104">CIM UnitaryComputerSystem 類別的 **SetPowerState** 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="269a0-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="269a0-105">在子類別中，您應該使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="269a0-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="269a0-106">您也應該在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="269a0-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="269a0-107">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="269a0-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="269a0-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="269a0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="269a0-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="269a0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="269a0-110">語法</span><span class="sxs-lookup"><span data-stu-id="269a0-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="269a0-111">參數</span><span class="sxs-lookup"><span data-stu-id="269a0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="269a0-112">*>powerstate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="269a0-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="269a0-113">指定此邏輯裝置所需電源狀態的 **ValueMap** 值。</span><span class="sxs-lookup"><span data-stu-id="269a0-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="269a0-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1) </span><span class="sxs-lookup"><span data-stu-id="269a0-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-115">完整功能。</span><span class="sxs-lookup"><span data-stu-id="269a0-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="269a0-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (2) </span><span class="sxs-lookup"><span data-stu-id="269a0-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-117">省電低電源模式。</span><span class="sxs-lookup"><span data-stu-id="269a0-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="269a0-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (3) </span><span class="sxs-lookup"><span data-stu-id="269a0-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-119">省電待命。</span><span class="sxs-lookup"><span data-stu-id="269a0-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="269a0-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>省 **電-其他** (4) </span><span class="sxs-lookup"><span data-stu-id="269a0-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-121">省電。</span><span class="sxs-lookup"><span data-stu-id="269a0-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="269a0-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**電源週期** (5) </span><span class="sxs-lookup"><span data-stu-id="269a0-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-123">電源週期。</span><span class="sxs-lookup"><span data-stu-id="269a0-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="269a0-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (6) 的電源</span><span class="sxs-lookup"><span data-stu-id="269a0-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-125">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="269a0-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="269a0-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="269a0-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-127">冬眠。</span><span class="sxs-lookup"><span data-stu-id="269a0-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="269a0-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**軟關閉** (8) </span><span class="sxs-lookup"><span data-stu-id="269a0-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="269a0-129">軟關閉。</span><span class="sxs-lookup"><span data-stu-id="269a0-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="269a0-130">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="269a0-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="269a0-131">指定何時應設定電源狀態，以做為一般日期時間值或做為間隔值， (在) 收到方法調用時的間隔開始時間。</span><span class="sxs-lookup"><span data-stu-id="269a0-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="269a0-132">當 *>powerstate* 參數等於 5 ( 「電源週期」 ) 時，時間參數會指出裝置應該重新開啟電源的 *時間* 。</span><span class="sxs-lookup"><span data-stu-id="269a0-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="269a0-133">立即關閉電源。</span><span class="sxs-lookup"><span data-stu-id="269a0-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="269a0-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="269a0-134">Return value</span></span>

<span data-ttu-id="269a0-135">如果成功，則傳回 0 (零) 1 (一個) 如果不支援指定的 *>powerstate* 和 *時間* 要求，則傳回另一個值，如果發生任何其他錯誤，則傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="269a0-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="269a0-136">備註</span><span class="sxs-lookup"><span data-stu-id="269a0-136">Remarks</span></span>

<span data-ttu-id="269a0-137">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="269a0-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="269a0-138">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="269a0-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="269a0-139">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="269a0-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="269a0-140">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="269a0-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="269a0-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="269a0-141">Requirements</span></span>



| <span data-ttu-id="269a0-142">需求</span><span class="sxs-lookup"><span data-stu-id="269a0-142">Requirement</span></span> | <span data-ttu-id="269a0-143">值</span><span class="sxs-lookup"><span data-stu-id="269a0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="269a0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="269a0-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="269a0-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="269a0-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="269a0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="269a0-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="269a0-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="269a0-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="269a0-148">Namespace</span></span><br/>                | <span data-ttu-id="269a0-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="269a0-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="269a0-150">MOF</span><span class="sxs-lookup"><span data-stu-id="269a0-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="269a0-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="269a0-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="269a0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="269a0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="269a0-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="269a0-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="269a0-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="269a0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269a0-155">CIM \_ UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="269a0-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="269a0-156">**CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="269a0-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




