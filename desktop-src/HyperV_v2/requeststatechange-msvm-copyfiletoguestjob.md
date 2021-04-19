---
description: 變更作業的狀態。
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: Msvm_CopyFileToGuestJob：： RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983754"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="4100b-103">Msvm \_ CopyFileToGuestJob：： RequestStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="4100b-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="4100b-104">變更作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4100b-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4100b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4100b-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="4100b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4100b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4100b-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4100b-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4100b-108">新狀態。</span><span class="sxs-lookup"><span data-stu-id="4100b-108">The new state.</span></span> <span data-ttu-id="4100b-109">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="4100b-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="4100b-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="4100b-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4100b-111">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="4100b-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="4100b-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="4100b-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4100b-113">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="4100b-113">Stops the job temporarily.</span></span> <span data-ttu-id="4100b-114">接著，用戶端可以使用「開始」重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="4100b-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="4100b-115">用戶端可能會在暫停時進入「服務」狀態 (這是工作特定) 。</span><span class="sxs-lookup"><span data-stu-id="4100b-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="4100b-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="4100b-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4100b-117">以有條理的方式，完全停止工作、儲存資料、保留狀態，以及關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="4100b-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="4100b-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="4100b-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4100b-119">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="4100b-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4100b-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="4100b-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4100b-121">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="4100b-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="4100b-122">用戶端可能會重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="4100b-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4100b-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="4100b-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4100b-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="4100b-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="4100b-125">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4100b-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4100b-126">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="4100b-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="4100b-127">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="4100b-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="4100b-128">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="4100b-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="4100b-129">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="4100b-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4100b-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="4100b-130">Return value</span></span>

<span data-ttu-id="4100b-131">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4100b-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="4100b-132">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4100b-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="4100b-133">Description</span><span class="sxs-lookup"><span data-stu-id="4100b-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4100b-134"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="4100b-135">成功。</span><span class="sxs-lookup"><span data-stu-id="4100b-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="4100b-136"><dt>**不支援使用 Timeout 參數**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="4100b-137"><dt>**失敗**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="4100b-138"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="4100b-139">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="4100b-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="4100b-140"><dt>**不支援**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="4100b-141"><dt>**狀態為未知**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="4100b-142"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="4100b-143"><dt>**不正確參數**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="4100b-144"><dt>**系統使用中**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="4100b-145"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="4100b-146">不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="4100b-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="4100b-147"><dt>**不正確的資料類型**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="4100b-148"><dt>**系統無法使用**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="4100b-149"><dt>**記憶體不足**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="4100b-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="4100b-150">Requirements</span></span>



| <span data-ttu-id="4100b-151">需求</span><span class="sxs-lookup"><span data-stu-id="4100b-151">Requirement</span></span> | <span data-ttu-id="4100b-152">值</span><span class="sxs-lookup"><span data-stu-id="4100b-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4100b-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4100b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4100b-154">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4100b-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4100b-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4100b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4100b-156">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4100b-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4100b-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="4100b-157">Namespace</span></span><br/>                | <span data-ttu-id="4100b-158">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4100b-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="4100b-159">MOF</span><span class="sxs-lookup"><span data-stu-id="4100b-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4100b-160"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4100b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="4100b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4100b-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4100b-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4100b-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4100b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4100b-164">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="4100b-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




