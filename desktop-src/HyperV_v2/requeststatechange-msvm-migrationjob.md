---
description: 要求將遷移作業的狀態變更為指定的狀態。
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Msvm_MigrationJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001366"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="7808c-103">Msvm MigrationJob 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7808c-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="7808c-104">要求將遷移作業的狀態變更為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="7808c-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="7808c-105">多次叫用 **RequestStateChange** 方法可能會導致較早的要求被覆寫或遺失。</span><span class="sxs-lookup"><span data-stu-id="7808c-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="7808c-106">如果傳回0，表示工作已順利完成。</span><span class="sxs-lookup"><span data-stu-id="7808c-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="7808c-107">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="7808c-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7808c-108">語法</span><span class="sxs-lookup"><span data-stu-id="7808c-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="7808c-109">參數</span><span class="sxs-lookup"><span data-stu-id="7808c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7808c-110">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7808c-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7808c-111">作業的新狀態。</span><span class="sxs-lookup"><span data-stu-id="7808c-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="7808c-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="7808c-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7808c-113">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="7808c-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="7808c-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="7808c-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7808c-115">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="7808c-115">Stops the job temporarily.</span></span> <span data-ttu-id="7808c-116">其目的是要使用 "Start" 重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="7808c-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="7808c-117">您可能可以在暫停時輸入「服務」狀態。</span><span class="sxs-lookup"><span data-stu-id="7808c-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="7808c-118"> (這是特定作業。 ) </span><span class="sxs-lookup"><span data-stu-id="7808c-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="7808c-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="7808c-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7808c-120">以有條理的方式，完全停止工作、儲存資料、保留狀態，以及關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="7808c-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="7808c-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="7808c-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7808c-122">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="7808c-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7808c-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="7808c-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7808c-124">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="7808c-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="7808c-125">您可以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="7808c-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7808c-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**已保留 DMTF**</span><span class="sxs-lookup"><span data-stu-id="7808c-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="7808c-127">保留的。</span><span class="sxs-lookup"><span data-stu-id="7808c-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7808c-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**保留的廠商**</span><span class="sxs-lookup"><span data-stu-id="7808c-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="7808c-129">保留的。</span><span class="sxs-lookup"><span data-stu-id="7808c-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7808c-130">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7808c-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7808c-131">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="7808c-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="7808c-132">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="7808c-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="7808c-133">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="7808c-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="7808c-134">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (不支援使用 Timeout 參數) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="7808c-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7808c-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="7808c-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="7808c-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="7808c-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-137"> (32768) </span><span class="sxs-lookup"><span data-stu-id="7808c-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-138"> (32769) </span><span class="sxs-lookup"><span data-stu-id="7808c-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-139"> (32770) </span><span class="sxs-lookup"><span data-stu-id="7808c-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-140"> (32771) </span><span class="sxs-lookup"><span data-stu-id="7808c-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-141"> (32772) </span><span class="sxs-lookup"><span data-stu-id="7808c-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-142"> (32773) </span><span class="sxs-lookup"><span data-stu-id="7808c-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-143"> (32774) </span><span class="sxs-lookup"><span data-stu-id="7808c-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-144"> (32775) </span><span class="sxs-lookup"><span data-stu-id="7808c-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-145"> (32776) </span><span class="sxs-lookup"><span data-stu-id="7808c-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-146"> (32777) </span><span class="sxs-lookup"><span data-stu-id="7808c-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="7808c-147"> (32778) </span><span class="sxs-lookup"><span data-stu-id="7808c-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7808c-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="7808c-148">Requirements</span></span>



| <span data-ttu-id="7808c-149">需求</span><span class="sxs-lookup"><span data-stu-id="7808c-149">Requirement</span></span> | <span data-ttu-id="7808c-150">值</span><span class="sxs-lookup"><span data-stu-id="7808c-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7808c-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7808c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7808c-152">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7808c-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7808c-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7808c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7808c-154">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7808c-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7808c-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="7808c-155">Namespace</span></span><br/>                | <span data-ttu-id="7808c-156">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7808c-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7808c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="7808c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7808c-158"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7808c-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7808c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="7808c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7808c-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7808c-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7808c-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7808c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7808c-162">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="7808c-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




