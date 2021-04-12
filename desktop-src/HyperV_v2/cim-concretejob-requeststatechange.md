---
description: 要求作業狀態變更為 RequestedState 參數中指定的值。 多次叫用 RequestStateChange 方法可能會導致較早的要求被覆寫或遺失。
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: CIM_ConcreteJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318628"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="a4580-104">CIM ConcreteJob 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a4580-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="a4580-105">要求作業狀態變更為 RequestedState 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="a4580-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="a4580-106">多次叫用 RequestStateChange 方法可能會導致較早的要求被覆寫或遺失。</span><span class="sxs-lookup"><span data-stu-id="a4580-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="a4580-107">如果傳回0，表示工作已順利完成。</span><span class="sxs-lookup"><span data-stu-id="a4580-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="a4580-108">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="a4580-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4580-109">語法</span><span class="sxs-lookup"><span data-stu-id="a4580-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a4580-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4580-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4580-111">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4580-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4580-112">要求作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4580-112">The state to request for a job.</span></span> <span data-ttu-id="a4580-113">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="a4580-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="a4580-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="a4580-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4580-115">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="a4580-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="a4580-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="a4580-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a4580-117">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="a4580-117">Stops the job temporarily.</span></span> <span data-ttu-id="a4580-118">其目的是要以 ' Start ' 重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="a4580-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="a4580-119">您可能可以在暫停時輸入「服務」狀態。</span><span class="sxs-lookup"><span data-stu-id="a4580-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="a4580-120"> (這是特定作業。 ) </span><span class="sxs-lookup"><span data-stu-id="a4580-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="a4580-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="a4580-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a4580-122">完全停止工作、儲存資料、保留狀態，並以有條理的方式關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="a4580-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="a4580-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="a4580-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a4580-124">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="a4580-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a4580-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="a4580-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a4580-126">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="a4580-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="a4580-127">您可以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="a4580-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a4580-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="a4580-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a4580-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a4580-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a4580-130">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4580-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4580-131">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="a4580-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="a4580-132">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="a4580-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="a4580-133">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="a4580-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="a4580-134">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="a4580-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4580-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4580-135">Return value</span></span>

<span data-ttu-id="a4580-136">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4580-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a4580-137">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a4580-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-138">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a4580-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-139">**未知/未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="a4580-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-140">**無法在 Timeout 期間內完成** (3) </span><span class="sxs-lookup"><span data-stu-id="a4580-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-141">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="a4580-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-142">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="a4580-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-143">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="a4580-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-144">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a4580-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-145">**方法參數已檢查-轉換已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a4580-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-146">**不正確狀態轉換** (4097) </span><span class="sxs-lookup"><span data-stu-id="a4580-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-147"> (4098) **不支援使用 Timeout 參數**</span><span class="sxs-lookup"><span data-stu-id="a4580-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-148">**忙碌** (4099) </span><span class="sxs-lookup"><span data-stu-id="a4580-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-149">**方法保留** (4100. 32767) </span><span class="sxs-lookup"><span data-stu-id="a4580-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a4580-150">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a4580-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a4580-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4580-151">Requirements</span></span>



| <span data-ttu-id="a4580-152">需求</span><span class="sxs-lookup"><span data-stu-id="a4580-152">Requirement</span></span> | <span data-ttu-id="a4580-153">值</span><span class="sxs-lookup"><span data-stu-id="a4580-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4580-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4580-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a4580-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4580-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a4580-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4580-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a4580-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a4580-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a4580-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4580-158">Namespace</span></span><br/>                | <span data-ttu-id="a4580-159">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4580-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a4580-160">MOF</span><span class="sxs-lookup"><span data-stu-id="a4580-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4580-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a4580-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4580-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a4580-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4580-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4580-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4580-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4580-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4580-165">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="a4580-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




