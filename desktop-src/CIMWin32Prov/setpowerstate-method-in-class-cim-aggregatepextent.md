---
description: SetPowerState 方法會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: CIM_AggregatePExtent 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936338"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="d972e-103">CIM AggregatePExtent 類別的 SetPowerState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d972e-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="d972e-104">**SetPowerState** 方法會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="d972e-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="d972e-105">在子類別中，應該使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="d972e-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d972e-106">您也應該在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="d972e-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d972e-107">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d972e-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d972e-108">如需搭配使用此方法與 C/c + + 的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d972e-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d972e-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d972e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d972e-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d972e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d972e-111">語法</span><span class="sxs-lookup"><span data-stu-id="d972e-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d972e-112">參數</span><span class="sxs-lookup"><span data-stu-id="d972e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d972e-113">*>powerstate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d972e-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d972e-114">指定此邏輯裝置所需電源狀態的 **ValueMap** 值。</span><span class="sxs-lookup"><span data-stu-id="d972e-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="d972e-115">1</span><span class="sxs-lookup"><span data-stu-id="d972e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="d972e-116">完整電源</span><span class="sxs-lookup"><span data-stu-id="d972e-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="d972e-117">2</span><span class="sxs-lookup"><span data-stu-id="d972e-117">2</span></span>
</dt> <dd>

<span data-ttu-id="d972e-118">省電低電源模式</span><span class="sxs-lookup"><span data-stu-id="d972e-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="d972e-119">3</span><span class="sxs-lookup"><span data-stu-id="d972e-119">3</span></span>
</dt> <dd>

<span data-ttu-id="d972e-120">省電待命</span><span class="sxs-lookup"><span data-stu-id="d972e-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="d972e-121">4</span><span class="sxs-lookup"><span data-stu-id="d972e-121">4</span></span>
</dt> <dd>

<span data-ttu-id="d972e-122">省電</span><span class="sxs-lookup"><span data-stu-id="d972e-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="d972e-123">5</span><span class="sxs-lookup"><span data-stu-id="d972e-123">5</span></span>
</dt> <dd>

<span data-ttu-id="d972e-124">電源週期</span><span class="sxs-lookup"><span data-stu-id="d972e-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="d972e-125">6</span><span class="sxs-lookup"><span data-stu-id="d972e-125">6</span></span>
</dt> <dd>

<span data-ttu-id="d972e-126">關閉電源</span><span class="sxs-lookup"><span data-stu-id="d972e-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d972e-127">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d972e-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d972e-128">當應該設定電源狀態時，請將其設定為一般日期時間值，或做為間隔值， (在收到方法調用時，間隔開始時間) 。</span><span class="sxs-lookup"><span data-stu-id="d972e-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d972e-129">當 *>powerstate* 參數等於 5 (電源週期) 時，時間參數會指出裝置應該重新開啟電源的 *時間* 。</span><span class="sxs-lookup"><span data-stu-id="d972e-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="d972e-130">立即關閉電源。</span><span class="sxs-lookup"><span data-stu-id="d972e-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d972e-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="d972e-131">Return value</span></span>

<span data-ttu-id="d972e-132">如果成功，則傳回 0 (零) 1 (一個) 如果不支援指定的 *>powerstate* 和 *時間* 要求，則傳回另一個值，如果發生任何其他錯誤，則傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="d972e-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d972e-133">備註</span><span class="sxs-lookup"><span data-stu-id="d972e-133">Remarks</span></span>

<span data-ttu-id="d972e-134">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d972e-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d972e-135">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="d972e-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d972e-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d972e-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d972e-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d972e-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d972e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="d972e-138">Requirements</span></span>



| <span data-ttu-id="d972e-139">需求</span><span class="sxs-lookup"><span data-stu-id="d972e-139">Requirement</span></span> | <span data-ttu-id="d972e-140">值</span><span class="sxs-lookup"><span data-stu-id="d972e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d972e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d972e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d972e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d972e-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d972e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d972e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d972e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d972e-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d972e-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="d972e-145">Namespace</span></span><br/>                | <span data-ttu-id="d972e-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d972e-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d972e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d972e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d972e-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d972e-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d972e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d972e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d972e-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d972e-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d972e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d972e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d972e-152">**CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="d972e-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="d972e-153">**CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="d972e-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

