---
description: 要求狀態變更。
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Msvm_StorageJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1ce563fdae2e73ba2e6994afc3d70c8d4d6fe34a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850279"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="9a583-103">Msvm Get-storagejob 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9a583-103">RequestStateChange method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="9a583-104">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9a583-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a583-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a583-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9a583-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a583-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a583-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a583-108">RequestStateChange 會變更工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="9a583-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="9a583-109">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="9a583-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="9a583-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) </span><span class="sxs-lookup"><span data-stu-id="9a583-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9a583-111">將狀態變更為「正在執行」。</span><span class="sxs-lookup"><span data-stu-id="9a583-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="9a583-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) </span><span class="sxs-lookup"><span data-stu-id="9a583-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9a583-113">暫時停止作業。</span><span class="sxs-lookup"><span data-stu-id="9a583-113">Stops the job temporarily.</span></span> <span data-ttu-id="9a583-114">其目的是要以 ' Start ' 重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="9a583-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="9a583-115">您可能可以在暫停時輸入「服務」狀態。</span><span class="sxs-lookup"><span data-stu-id="9a583-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="9a583-116"> (這是特定作業。 ) </span><span class="sxs-lookup"><span data-stu-id="9a583-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="9a583-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) </span><span class="sxs-lookup"><span data-stu-id="9a583-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9a583-118">完全停止工作、儲存資料、保留狀態，並以有條理的方式關閉所有基礎進程。</span><span class="sxs-lookup"><span data-stu-id="9a583-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="9a583-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) </span><span class="sxs-lookup"><span data-stu-id="9a583-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9a583-120">立即終止工作，不需要儲存資料或保留狀態。</span><span class="sxs-lookup"><span data-stu-id="9a583-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9a583-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) </span><span class="sxs-lookup"><span data-stu-id="9a583-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9a583-122">將工作放入廠商特定的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="9a583-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="9a583-123">您可以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="9a583-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9a583-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="9a583-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9a583-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="9a583-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9a583-126">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a583-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a583-127">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="9a583-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="9a583-128">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="9a583-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="9a583-129">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="9a583-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="9a583-130">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="9a583-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a583-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a583-131">Return value</span></span>

<span data-ttu-id="9a583-132">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9a583-132">This method returns one of the following values:</span></span>

<dl> <dt>

 <span data-ttu-id="9a583-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="9a583-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-134"> (32768) </span><span class="sxs-lookup"><span data-stu-id="9a583-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-135"> (32769) </span><span class="sxs-lookup"><span data-stu-id="9a583-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-136"> (32770) </span><span class="sxs-lookup"><span data-stu-id="9a583-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-137"> (32771) </span><span class="sxs-lookup"><span data-stu-id="9a583-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-138"> (32772) </span><span class="sxs-lookup"><span data-stu-id="9a583-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-139"> (32773) </span><span class="sxs-lookup"><span data-stu-id="9a583-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-140"> (32774) </span><span class="sxs-lookup"><span data-stu-id="9a583-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-141"> (32775) </span><span class="sxs-lookup"><span data-stu-id="9a583-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-142"> (32776) </span><span class="sxs-lookup"><span data-stu-id="9a583-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-143"> (32777) </span><span class="sxs-lookup"><span data-stu-id="9a583-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="9a583-144"> (32778) </span><span class="sxs-lookup"><span data-stu-id="9a583-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9a583-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a583-145">Requirements</span></span>



| <span data-ttu-id="9a583-146">需求</span><span class="sxs-lookup"><span data-stu-id="9a583-146">Requirement</span></span> | <span data-ttu-id="9a583-147">值</span><span class="sxs-lookup"><span data-stu-id="9a583-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a583-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a583-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9a583-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9a583-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9a583-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a583-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9a583-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9a583-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9a583-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="9a583-152">Namespace</span></span><br/>                | <span data-ttu-id="9a583-153">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9a583-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a583-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9a583-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a583-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9a583-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a583-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9a583-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a583-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a583-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a583-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a583-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a583-159">**Msvm \_ get-storagejob**</span><span class="sxs-lookup"><span data-stu-id="9a583-159">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




