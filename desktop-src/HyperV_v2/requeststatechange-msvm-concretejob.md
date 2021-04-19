---
description: 要求作業狀態變更為指定的狀態。
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Msvm_ConcreteJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984584"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="75ef2-103">Msvm ConcreteJob 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="75ef2-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="75ef2-104">要求作業狀態變更為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="75ef2-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="75ef2-105">多次叫用 **RequestStateChange** 方法可能會導致較早的要求被覆寫或遺失。</span><span class="sxs-lookup"><span data-stu-id="75ef2-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="75ef2-106">如果傳回0，表示工作已順利完成。</span><span class="sxs-lookup"><span data-stu-id="75ef2-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="75ef2-107">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="75ef2-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ef2-108">語法</span><span class="sxs-lookup"><span data-stu-id="75ef2-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="75ef2-109">參數</span><span class="sxs-lookup"><span data-stu-id="75ef2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ef2-110">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75ef2-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ef2-111">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="75ef2-111">Type: **uint16**</span></span>

<span data-ttu-id="75ef2-112">作業的新狀態。</span><span class="sxs-lookup"><span data-stu-id="75ef2-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="75ef2-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="75ef2-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-114">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="75ef2-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="75ef2-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="75ef2-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-116">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="75ef2-116">Stops the job temporarily.</span></span> <span data-ttu-id="75ef2-117">其目的是要使用 "Start" 重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="75ef2-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="75ef2-118">您可能可以在暫停時輸入「服務」狀態。</span><span class="sxs-lookup"><span data-stu-id="75ef2-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="75ef2-119"> (這是特定作業。 ) </span><span class="sxs-lookup"><span data-stu-id="75ef2-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="75ef2-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="75ef2-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-121">以有條理的方式，完全停止工作、儲存資料、保留狀態，以及關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="75ef2-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="75ef2-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="75ef2-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-123">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="75ef2-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="75ef2-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="75ef2-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-125">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="75ef2-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="75ef2-126">您可以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="75ef2-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="75ef2-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**已保留 DMTF**</span><span class="sxs-lookup"><span data-stu-id="75ef2-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="75ef2-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="75ef2-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**保留的廠商**</span><span class="sxs-lookup"><span data-stu-id="75ef2-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="75ef2-130">保留的。</span><span class="sxs-lookup"><span data-stu-id="75ef2-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="75ef2-131">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75ef2-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ef2-132">類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="75ef2-132">Type: **datetime**</span></span>

<span data-ttu-id="75ef2-133">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="75ef2-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="75ef2-134">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="75ef2-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="75ef2-135">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="75ef2-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="75ef2-136">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (不支援使用 Timeout 參數) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="75ef2-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ef2-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="75ef2-137">Return value</span></span>

<span data-ttu-id="75ef2-138">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="75ef2-138">Type: **uint32**</span></span>

<span data-ttu-id="75ef2-139">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="75ef2-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75ef2-140">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="75ef2-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-141">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="75ef2-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-142">**未知/未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="75ef2-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-143">**無法在 Timeout 期間內完成** (3) </span><span class="sxs-lookup"><span data-stu-id="75ef2-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-144">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="75ef2-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-145">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="75ef2-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-146">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="75ef2-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-147">**DMTF 保留** 的 (7 4095) </span><span class="sxs-lookup"><span data-stu-id="75ef2-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-148">**方法參數已檢查-轉換已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="75ef2-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-149">**不正確狀態轉換** (4097) </span><span class="sxs-lookup"><span data-stu-id="75ef2-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-150"> (4098) **不支援使用 Timeout 參數**</span><span class="sxs-lookup"><span data-stu-id="75ef2-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-151">**忙碌** (4099) </span><span class="sxs-lookup"><span data-stu-id="75ef2-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-152">**方法保留** (4100 32767) </span><span class="sxs-lookup"><span data-stu-id="75ef2-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="75ef2-153">**廠商專用** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="75ef2-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="75ef2-154">備註</span><span class="sxs-lookup"><span data-stu-id="75ef2-154">Remarks</span></span>

<span data-ttu-id="75ef2-155">存取 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="75ef2-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="75ef2-156">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="75ef2-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="75ef2-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="75ef2-157">Requirements</span></span>



| <span data-ttu-id="75ef2-158">需求</span><span class="sxs-lookup"><span data-stu-id="75ef2-158">Requirement</span></span> | <span data-ttu-id="75ef2-159">值</span><span class="sxs-lookup"><span data-stu-id="75ef2-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ef2-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75ef2-160">Minimum supported client</span></span><br/> | <span data-ttu-id="75ef2-161">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75ef2-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75ef2-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75ef2-162">Minimum supported server</span></span><br/> | <span data-ttu-id="75ef2-163">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75ef2-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75ef2-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="75ef2-164">Namespace</span></span><br/>                | <span data-ttu-id="75ef2-165">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="75ef2-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75ef2-166">MOF</span><span class="sxs-lookup"><span data-stu-id="75ef2-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75ef2-167"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="75ef2-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75ef2-168">DLL</span><span class="sxs-lookup"><span data-stu-id="75ef2-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ef2-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75ef2-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75ef2-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ef2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ef2-171">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="75ef2-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

