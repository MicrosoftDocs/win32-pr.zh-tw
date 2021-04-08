---
description: 要求來賓服務的狀態變更為指定的值。
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: Msvm_GuestService：： RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693740"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="a0252-103">Msvm \_ GuestService：： RequestStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="a0252-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="a0252-104">要求來賓服務的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="a0252-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0252-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0252-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a0252-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0252-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0252-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0252-108">新狀態。</span><span class="sxs-lookup"><span data-stu-id="a0252-108">The new state.</span></span> <span data-ttu-id="a0252-109">如果 **RequestStateChange** 方法的傳回碼為0或4096，資訊就會放在實例的 **RequestedState** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="a0252-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="a0252-110">如需詳細資訊，請參閱元素的 **EnabledState** 和 **RequestedState** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="a0252-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="a0252-111">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="a0252-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0252-112">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="a0252-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0252-113">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="a0252-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="a0252-114">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="a0252-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="a0252-115">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="a0252-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="a0252-116">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="a0252-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="a0252-117">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="a0252-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="a0252-118">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="a0252-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="a0252-119">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="a0252-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="a0252-120">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="a0252-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a0252-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a0252-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a0252-122">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a0252-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a0252-123">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a0252-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0252-124">如果以非同步方式執行作業，則為所傳回之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 物件的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="a0252-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="a0252-125">如果有，則會使用傳回的參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="a0252-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="a0252-126">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0252-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0252-127">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="a0252-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="a0252-128">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="a0252-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="a0252-129">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="a0252-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="a0252-130">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="a0252-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0252-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0252-131">Return value</span></span>

<span data-ttu-id="a0252-132">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a0252-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="a0252-133">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a0252-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a0252-134">Description</span><span class="sxs-lookup"><span data-stu-id="a0252-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0252-135"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="a0252-136">成功。</span><span class="sxs-lookup"><span data-stu-id="a0252-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a0252-137"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="a0252-138"><dt>**方法參數檢查-轉換已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="a0252-139">轉換是非同步。</span><span class="sxs-lookup"><span data-stu-id="a0252-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a0252-140"><dt>**不支援使用 Timeout 參數**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="a0252-141"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="a0252-142">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a0252-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="a0252-143"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="a0252-144">不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="a0252-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0252-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0252-145">Requirements</span></span>



| <span data-ttu-id="a0252-146">需求</span><span class="sxs-lookup"><span data-stu-id="a0252-146">Requirement</span></span> | <span data-ttu-id="a0252-147">值</span><span class="sxs-lookup"><span data-stu-id="a0252-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0252-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0252-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a0252-149">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0252-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a0252-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0252-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a0252-151">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0252-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0252-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0252-152">Namespace</span></span><br/>                | <span data-ttu-id="a0252-153">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0252-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="a0252-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a0252-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0252-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0252-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a0252-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0252-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0252-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0252-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0252-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0252-159">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="a0252-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




