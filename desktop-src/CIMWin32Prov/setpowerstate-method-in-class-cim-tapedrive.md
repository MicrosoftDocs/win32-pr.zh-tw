---
description: CIM Disable-tapedrive 類別的 SetPowerState 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: CIM_TapeDrive 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510699"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="61732-103">CIM Disable-tapedrive 類別的 SetPowerState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61732-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="61732-104">CIM Disable-tapedrive 類別的 **SetPowerState** 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="61732-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="61732-105">在子類別中，您應該使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="61732-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="61732-106">您也應該在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="61732-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="61732-107">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="61732-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="61732-108">語法</span><span class="sxs-lookup"><span data-stu-id="61732-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="61732-109">參數</span><span class="sxs-lookup"><span data-stu-id="61732-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61732-110">*>powerstate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61732-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61732-111">指定此邏輯裝置所需電源狀態的 **ValueMap** 值。</span><span class="sxs-lookup"><span data-stu-id="61732-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="61732-112">1</span><span class="sxs-lookup"><span data-stu-id="61732-112">1</span></span>
</dt> <dd>

<span data-ttu-id="61732-113">完整功能。</span><span class="sxs-lookup"><span data-stu-id="61732-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="61732-114">2</span><span class="sxs-lookup"><span data-stu-id="61732-114">2</span></span>
</dt> <dd>

<span data-ttu-id="61732-115">省電低電源模式。</span><span class="sxs-lookup"><span data-stu-id="61732-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="61732-116">3</span><span class="sxs-lookup"><span data-stu-id="61732-116">3</span></span>
</dt> <dd>

<span data-ttu-id="61732-117">省電待命。</span><span class="sxs-lookup"><span data-stu-id="61732-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="61732-118">4</span><span class="sxs-lookup"><span data-stu-id="61732-118">4</span></span>
</dt> <dd>

<span data-ttu-id="61732-119">省電。</span><span class="sxs-lookup"><span data-stu-id="61732-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="61732-120">5</span><span class="sxs-lookup"><span data-stu-id="61732-120">5</span></span>
</dt> <dd>

<span data-ttu-id="61732-121">電源週期。</span><span class="sxs-lookup"><span data-stu-id="61732-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="61732-122">6</span><span class="sxs-lookup"><span data-stu-id="61732-122">6</span></span>
</dt> <dd>

<span data-ttu-id="61732-123">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="61732-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61732-124">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61732-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61732-125">指定何時應設定電源狀態，以做為一般日期時間值或做為間隔值， (在) 收到方法調用時的間隔開始時間。</span><span class="sxs-lookup"><span data-stu-id="61732-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="61732-126">當 *>powerstate* 參數等於 5 ( 「電源週期」 ) 時，時間參數會指出裝置應該重新開啟電源的 *時間* 。</span><span class="sxs-lookup"><span data-stu-id="61732-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="61732-127">立即關閉電源。</span><span class="sxs-lookup"><span data-stu-id="61732-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61732-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="61732-128">Return value</span></span>

<span data-ttu-id="61732-129">如果成功，則傳回 0 (零) 1 (一個) 如果不支援指定的 *>powerstate* 和 *時間* 要求，則傳回另一個值，如果發生任何其他錯誤，則傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="61732-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="61732-130">備註</span><span class="sxs-lookup"><span data-stu-id="61732-130">Remarks</span></span>

<span data-ttu-id="61732-131">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="61732-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="61732-132">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="61732-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="61732-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="61732-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="61732-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="61732-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="61732-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="61732-135">Requirements</span></span>



| <span data-ttu-id="61732-136">需求</span><span class="sxs-lookup"><span data-stu-id="61732-136">Requirement</span></span> | <span data-ttu-id="61732-137">值</span><span class="sxs-lookup"><span data-stu-id="61732-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61732-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61732-138">Minimum supported client</span></span><br/> | <span data-ttu-id="61732-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61732-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61732-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61732-140">Minimum supported server</span></span><br/> | <span data-ttu-id="61732-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61732-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61732-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="61732-142">Namespace</span></span><br/>                | <span data-ttu-id="61732-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="61732-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61732-144">MOF</span><span class="sxs-lookup"><span data-stu-id="61732-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61732-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="61732-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61732-146">DLL</span><span class="sxs-lookup"><span data-stu-id="61732-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61732-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61732-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61732-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61732-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61732-149">CIM \_ disable-tapedrive</span><span class="sxs-lookup"><span data-stu-id="61732-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="61732-150">**CIM \_ disable-tapedrive**</span><span class="sxs-lookup"><span data-stu-id="61732-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




