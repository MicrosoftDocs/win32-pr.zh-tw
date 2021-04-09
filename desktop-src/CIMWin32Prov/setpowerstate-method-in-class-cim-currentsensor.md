---
description: SetPowerState 方法會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。
ms.assetid: 8dd54a71-152a-4668-bdb6-c0968d8ff094
ms.tgt_platform: multiple
title: CIM_CurrentSensor 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3da58796e783ef9b1c9141a6e226935c881a95f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847330"
---
# <a name="setpowerstate-method-of-the-cim_currentsensor-class"></a><span data-ttu-id="fecbe-103">CIM CurrentSensor 類別的 SetPowerState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fecbe-103">SetPowerState method of the CIM\_CurrentSensor class</span></span>

<span data-ttu-id="fecbe-104">**SetPowerState** 方法會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="fecbe-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="fecbe-105">在子類別中，應該使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="fecbe-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fecbe-106">您也應該在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="fecbe-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="fecbe-107">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fecbe-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fecbe-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fecbe-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fecbe-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fecbe-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fecbe-110">語法</span><span class="sxs-lookup"><span data-stu-id="fecbe-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="fecbe-111">參數</span><span class="sxs-lookup"><span data-stu-id="fecbe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fecbe-112">*>powerstate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fecbe-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-113">指定此邏輯裝置所需電源狀態的 **ValueMap** 值。</span><span class="sxs-lookup"><span data-stu-id="fecbe-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="fecbe-114">1</span><span class="sxs-lookup"><span data-stu-id="fecbe-114">1</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-115">完整功能。</span><span class="sxs-lookup"><span data-stu-id="fecbe-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="fecbe-116">2</span><span class="sxs-lookup"><span data-stu-id="fecbe-116">2</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-117">省電低電源模式。</span><span class="sxs-lookup"><span data-stu-id="fecbe-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="fecbe-118">3</span><span class="sxs-lookup"><span data-stu-id="fecbe-118">3</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-119">省電待命。</span><span class="sxs-lookup"><span data-stu-id="fecbe-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="fecbe-120">4</span><span class="sxs-lookup"><span data-stu-id="fecbe-120">4</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-121">省電。</span><span class="sxs-lookup"><span data-stu-id="fecbe-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="fecbe-122">5</span><span class="sxs-lookup"><span data-stu-id="fecbe-122">5</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-123">電源週期。</span><span class="sxs-lookup"><span data-stu-id="fecbe-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="fecbe-124">6</span><span class="sxs-lookup"><span data-stu-id="fecbe-124">6</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-125">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="fecbe-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fecbe-126">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fecbe-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fecbe-127">指定何時應設定電源狀態，以做為一般日期時間值或做為間隔值， (在) 收到方法調用時的間隔開始時間。</span><span class="sxs-lookup"><span data-stu-id="fecbe-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="fecbe-128">當 *>powerstate* 參數等於 5 ( 「電源週期」 ) 時，時間參數會指出裝置應該重新開啟電源的 *時間* 。</span><span class="sxs-lookup"><span data-stu-id="fecbe-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="fecbe-129">立即關閉電源。</span><span class="sxs-lookup"><span data-stu-id="fecbe-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fecbe-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="fecbe-130">Return value</span></span>

<span data-ttu-id="fecbe-131">如果成功，則傳回 0 (零) 1 (一個) 如果不支援指定的 *>powerstate* 和 *時間* 要求，則傳回另一個值，如果發生任何其他錯誤，則傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="fecbe-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="fecbe-132">備註</span><span class="sxs-lookup"><span data-stu-id="fecbe-132">Remarks</span></span>

<span data-ttu-id="fecbe-133">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="fecbe-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fecbe-134">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="fecbe-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fecbe-135">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="fecbe-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fecbe-136">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fecbe-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fecbe-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="fecbe-137">Requirements</span></span>



| <span data-ttu-id="fecbe-138">需求</span><span class="sxs-lookup"><span data-stu-id="fecbe-138">Requirement</span></span> | <span data-ttu-id="fecbe-139">值</span><span class="sxs-lookup"><span data-stu-id="fecbe-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fecbe-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fecbe-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fecbe-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fecbe-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fecbe-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fecbe-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fecbe-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fecbe-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fecbe-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="fecbe-144">Namespace</span></span><br/>                | <span data-ttu-id="fecbe-145">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fecbe-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fecbe-146">MOF</span><span class="sxs-lookup"><span data-stu-id="fecbe-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fecbe-147"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fecbe-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fecbe-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fecbe-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fecbe-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fecbe-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fecbe-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fecbe-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecbe-151">CIM \_ CurrentSensor</span><span class="sxs-lookup"><span data-stu-id="fecbe-151">CIM\_CurrentSensor</span></span>](setpowerstate-method-in-class-cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="fecbe-152">**CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="fecbe-152">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> </dl>

 

 




