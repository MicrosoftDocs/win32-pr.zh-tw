---
description: 要求狀態變更。
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Msvm_VirtualSystemReferencePointExportJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993789"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="90db1-103">Msvm VirtualSystemReferencePointExportJob 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="90db1-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="90db1-104">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="90db1-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="90db1-105">語法</span><span class="sxs-lookup"><span data-stu-id="90db1-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="90db1-106">參數</span><span class="sxs-lookup"><span data-stu-id="90db1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90db1-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90db1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90db1-108">變更作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="90db1-108">Changes the state of a job.</span></span> <span data-ttu-id="90db1-109">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="90db1-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="90db1-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="90db1-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="90db1-111">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="90db1-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="90db1-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="90db1-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="90db1-113">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="90db1-113">Stops the job temporarily.</span></span> <span data-ttu-id="90db1-114">其目的是要以 ' Start ' 重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="90db1-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="90db1-115">您可能可以在暫停時輸入「服務」狀態。</span><span class="sxs-lookup"><span data-stu-id="90db1-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="90db1-116"> (這是特定作業。 ) </span><span class="sxs-lookup"><span data-stu-id="90db1-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="90db1-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="90db1-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="90db1-118">完全停止工作、儲存資料、保留狀態，並以有條理的方式關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="90db1-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="90db1-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="90db1-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="90db1-120">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="90db1-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="90db1-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="90db1-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="90db1-122">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="90db1-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="90db1-123">您可以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="90db1-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="90db1-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="90db1-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="90db1-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="90db1-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="90db1-126">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90db1-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90db1-127">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="90db1-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="90db1-128">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="90db1-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="90db1-129">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="90db1-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="90db1-130">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="90db1-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90db1-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="90db1-131">Return value</span></span>

<span data-ttu-id="90db1-132">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="90db1-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="90db1-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="90db1-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-134"> (32768) </span><span class="sxs-lookup"><span data-stu-id="90db1-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-135"> (32769) </span><span class="sxs-lookup"><span data-stu-id="90db1-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-136"> (32770) </span><span class="sxs-lookup"><span data-stu-id="90db1-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-137"> (32771) </span><span class="sxs-lookup"><span data-stu-id="90db1-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-138"> (32772) </span><span class="sxs-lookup"><span data-stu-id="90db1-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-139"> (32773) </span><span class="sxs-lookup"><span data-stu-id="90db1-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-140"> (32774) </span><span class="sxs-lookup"><span data-stu-id="90db1-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-141"> (32775) </span><span class="sxs-lookup"><span data-stu-id="90db1-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-142"> (32776) </span><span class="sxs-lookup"><span data-stu-id="90db1-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-143"> (32777) </span><span class="sxs-lookup"><span data-stu-id="90db1-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="90db1-144"> (32778) </span><span class="sxs-lookup"><span data-stu-id="90db1-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90db1-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="90db1-145">Requirements</span></span>



| <span data-ttu-id="90db1-146">需求</span><span class="sxs-lookup"><span data-stu-id="90db1-146">Requirement</span></span> | <span data-ttu-id="90db1-147">值</span><span class="sxs-lookup"><span data-stu-id="90db1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90db1-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90db1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="90db1-149">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90db1-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90db1-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90db1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="90db1-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="90db1-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="90db1-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="90db1-152">Namespace</span></span><br/>                | <span data-ttu-id="90db1-153">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="90db1-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90db1-154">MOF</span><span class="sxs-lookup"><span data-stu-id="90db1-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90db1-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="90db1-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90db1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="90db1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90db1-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90db1-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90db1-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90db1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90db1-159">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="90db1-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




