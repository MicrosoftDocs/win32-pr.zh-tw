---
description: 計算 RemoteFX 虛擬機器所需的視訊記憶體數量。
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Msvm_Synth3dVideoPool 類別的 CalculateVideoMemoryRequirements 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113629"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="7e888-103">Msvm Synth3dVideoPool 類別的 CalculateVideoMemoryRequirements 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7e888-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="7e888-104">計算 RemoteFX 虛擬機器所需的視訊記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="7e888-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e888-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e888-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="7e888-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e888-107">*monitorResolution* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e888-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e888-108">虛擬機器的最大監視器解析度。</span><span class="sxs-lookup"><span data-stu-id="7e888-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="7e888-109">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="7e888-109">This must be one of the following values.</span></span>



| <span data-ttu-id="7e888-110">值</span><span class="sxs-lookup"><span data-stu-id="7e888-110">Value</span></span>                                                                        | <span data-ttu-id="7e888-111">意義</span><span class="sxs-lookup"><span data-stu-id="7e888-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="7e888-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7e888-113">最大解析度為 1024 768。</span><span class="sxs-lookup"><span data-stu-id="7e888-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="7e888-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7e888-115">最大解析度為 1280 1024。</span><span class="sxs-lookup"><span data-stu-id="7e888-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="7e888-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7e888-117">最大解析度為 1600 1200。</span><span class="sxs-lookup"><span data-stu-id="7e888-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="7e888-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7e888-119">最大解析度為 1920 1200。</span><span class="sxs-lookup"><span data-stu-id="7e888-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7e888-120">*numberOfMonitors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e888-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e888-121">虛擬機器的監視器數目上限。</span><span class="sxs-lookup"><span data-stu-id="7e888-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="7e888-122">監視器的最小數目是1，而最大值則取決於螢幕解析度上限。</span><span class="sxs-lookup"><span data-stu-id="7e888-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="7e888-123">下表定義允許不同解析度的監視器數目上限。</span><span class="sxs-lookup"><span data-stu-id="7e888-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="7e888-124">解決方案</span><span class="sxs-lookup"><span data-stu-id="7e888-124">Resolution</span></span>             | <span data-ttu-id="7e888-125">監視器上限</span><span class="sxs-lookup"><span data-stu-id="7e888-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="7e888-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="7e888-126">1024   768</span></span><br/>  | <span data-ttu-id="7e888-127">4</span><span class="sxs-lookup"><span data-stu-id="7e888-127">4</span></span><br/>     |
| <span data-ttu-id="7e888-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="7e888-128">1280   1024</span></span><br/> | <span data-ttu-id="7e888-129">4</span><span class="sxs-lookup"><span data-stu-id="7e888-129">4</span></span><br/>     |
| <span data-ttu-id="7e888-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="7e888-130">1600   1200</span></span><br/> | <span data-ttu-id="7e888-131">3</span><span class="sxs-lookup"><span data-stu-id="7e888-131">3</span></span><br/>     |
| <span data-ttu-id="7e888-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="7e888-132">1920   1200</span></span><br/> | <span data-ttu-id="7e888-133">2</span><span class="sxs-lookup"><span data-stu-id="7e888-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="7e888-134">*requiredVideoMemory* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7e888-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e888-135">接收所需的視訊記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e888-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e888-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e888-136">Return value</span></span>

<span data-ttu-id="7e888-137">傳回狀態碼，這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e888-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="7e888-138">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7e888-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="7e888-139">Description</span><span class="sxs-lookup"><span data-stu-id="7e888-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="7e888-140"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="7e888-141">成功。</span><span class="sxs-lookup"><span data-stu-id="7e888-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="7e888-142"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="7e888-143">作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="7e888-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="7e888-144"><dt>**失敗**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="7e888-145">失敗。</span><span class="sxs-lookup"><span data-stu-id="7e888-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7e888-146"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="7e888-147">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="7e888-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="7e888-148"><dt>**不支援**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="7e888-149">不支援。</span><span class="sxs-lookup"><span data-stu-id="7e888-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="7e888-150"><dt>**狀態為未知**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="7e888-151">狀態未知。</span><span class="sxs-lookup"><span data-stu-id="7e888-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="7e888-152"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="7e888-153">逾時。</span><span class="sxs-lookup"><span data-stu-id="7e888-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7e888-154"><dt>**不正確參數**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="7e888-155">參數無效。</span><span class="sxs-lookup"><span data-stu-id="7e888-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="7e888-156"><dt>**系統使用的是**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="7e888-157">系統正在使用中。</span><span class="sxs-lookup"><span data-stu-id="7e888-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="7e888-158"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="7e888-159">此操作的狀態無效。</span><span class="sxs-lookup"><span data-stu-id="7e888-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="7e888-160"><dt>**不正確的資料類型**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="7e888-161">不正確的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7e888-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="7e888-162"><dt>**系統無法使用**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="7e888-163">系統無法使用。</span><span class="sxs-lookup"><span data-stu-id="7e888-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="7e888-164"><dt>**記憶體不足**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="7e888-165">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="7e888-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="7e888-166">備註</span><span class="sxs-lookup"><span data-stu-id="7e888-166">Remarks</span></span>

<span data-ttu-id="7e888-167">通常會在主機系統上呼叫這個方法，以判斷主機是否有足夠的可用視訊記憶體來裝載 RemoteFX 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7e888-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="7e888-168">若要這樣做，請將這個方法所計算的視訊記憶體數量與 [**Msvm \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) 屬性進行比較，以判斷主機電腦是否有足夠的可用視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="7e888-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="7e888-169">您可以使用此資訊來判斷是否可以將虛擬機器移至主機系統。</span><span class="sxs-lookup"><span data-stu-id="7e888-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e888-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e888-170">Requirements</span></span>



| <span data-ttu-id="7e888-171">需求</span><span class="sxs-lookup"><span data-stu-id="7e888-171">Requirement</span></span> | <span data-ttu-id="7e888-172">值</span><span class="sxs-lookup"><span data-stu-id="7e888-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e888-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e888-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7e888-174">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e888-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7e888-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e888-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7e888-176">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e888-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e888-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="7e888-177">Namespace</span></span><br/>                | <span data-ttu-id="7e888-178">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7e888-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7e888-179">MOF</span><span class="sxs-lookup"><span data-stu-id="7e888-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e888-180"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e888-181">DLL</span><span class="sxs-lookup"><span data-stu-id="7e888-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e888-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e888-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e888-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e888-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e888-184">**Msvm \_ PhysicalGPUInfo**</span><span class="sxs-lookup"><span data-stu-id="7e888-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="7e888-185">**Msvm \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="7e888-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




