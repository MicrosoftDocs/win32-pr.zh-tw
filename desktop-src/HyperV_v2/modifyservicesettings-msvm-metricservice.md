---
description: 修改服務的設定資料。
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Msvm_MetricService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690788"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="961a2-103">Msvm MetricService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="961a2-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="961a2-104">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="961a2-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="961a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="961a2-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="961a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="961a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961a2-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="961a2-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961a2-108">包含 [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) 類別的內嵌實例，其中包含服務已修改的設定資料。</span><span class="sxs-lookup"><span data-stu-id="961a2-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="961a2-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="961a2-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961a2-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="961a2-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961a2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="961a2-111">Return value</span></span>

<span data-ttu-id="961a2-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="961a2-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="961a2-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="961a2-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="961a2-114">Description</span><span class="sxs-lookup"><span data-stu-id="961a2-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="961a2-115"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="961a2-116">成功。</span><span class="sxs-lookup"><span data-stu-id="961a2-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="961a2-117"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="961a2-118">已檢查方法參數，作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="961a2-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="961a2-119"><dt>**失敗**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="961a2-120">失敗。</span><span class="sxs-lookup"><span data-stu-id="961a2-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="961a2-121"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="961a2-122">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="961a2-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="961a2-123"><dt>**不支援**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="961a2-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="961a2-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="961a2-125"><dt>**狀態為未知**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="961a2-126">狀態未知。</span><span class="sxs-lookup"><span data-stu-id="961a2-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="961a2-127"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="961a2-128">超時時間。</span><span class="sxs-lookup"><span data-stu-id="961a2-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="961a2-129"><dt>**不正確參數**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="961a2-130">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="961a2-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="961a2-131"><dt>**系統使用中**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="961a2-132">系統正在使用中。</span><span class="sxs-lookup"><span data-stu-id="961a2-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="961a2-133"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="961a2-134">此操作的狀態無效。</span><span class="sxs-lookup"><span data-stu-id="961a2-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="961a2-135"><dt>**不正確的資料類型**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="961a2-136">不正確的資料類型。</span><span class="sxs-lookup"><span data-stu-id="961a2-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="961a2-137"><dt>**系統無法使用**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="961a2-138">系統無法使用。</span><span class="sxs-lookup"><span data-stu-id="961a2-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="961a2-139"><dt>**記憶體不足**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="961a2-140">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="961a2-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="961a2-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="961a2-141">Requirements</span></span>



| <span data-ttu-id="961a2-142">需求</span><span class="sxs-lookup"><span data-stu-id="961a2-142">Requirement</span></span> | <span data-ttu-id="961a2-143">值</span><span class="sxs-lookup"><span data-stu-id="961a2-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961a2-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="961a2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="961a2-145">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="961a2-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="961a2-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="961a2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="961a2-147">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="961a2-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="961a2-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="961a2-148">Namespace</span></span><br/>                | <span data-ttu-id="961a2-149">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="961a2-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="961a2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="961a2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="961a2-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="961a2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="961a2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="961a2-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="961a2-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="961a2-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="961a2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961a2-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="961a2-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

