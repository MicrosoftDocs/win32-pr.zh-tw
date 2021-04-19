---
description: 要求 guest 服務介面元件的狀態變更為指定的值。
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: Msvm_GuestServiceInterfaceComponent：： RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976881"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="dc9b9-103">Msvm \_ GuestServiceInterfaceComponent：： RequestStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="dc9b9-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="dc9b9-104">要求 guest 服務介面元件的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9b9-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc9b9-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="dc9b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc9b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9b9-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc9b9-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9b9-108">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dc9b9-108">Type: **uint16**</span></span>

<span data-ttu-id="dc9b9-109">新狀態。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-109">The new state.</span></span> <span data-ttu-id="dc9b9-110">如果 **RequestStateChange** 方法的傳回碼為0或4096，資訊就會放在實例的 **RequestedState** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="dc9b9-111">如需詳細資訊，請參閱元素的 **EnabledState** 和 **RequestedState** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="dc9b9-112">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dc9b9-113">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc9b9-114">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="dc9b9-115">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="dc9b9-116">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="dc9b9-117">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="dc9b9-118">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="dc9b9-119">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="dc9b9-120">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="dc9b9-121">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dc9b9-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dc9b9-123">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="dc9b9-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="dc9b9-124">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dc9b9-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9b9-125">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dc9b9-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="dc9b9-126">如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="dc9b9-127">如果有，則會使用傳回的參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="dc9b9-128">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc9b9-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9b9-129">類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dc9b9-129">Type: **datetime**</span></span>

<span data-ttu-id="dc9b9-130">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="dc9b9-131">間隔格式必須用來指定時間長度。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="dc9b9-132">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="dc9b9-133">如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc9b9-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc9b9-134">Return value</span></span>

<span data-ttu-id="dc9b9-135">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc9b9-135">Type: **uint32**</span></span>

<span data-ttu-id="dc9b9-136">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="dc9b9-137">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="dc9b9-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="dc9b9-138">Description</span><span class="sxs-lookup"><span data-stu-id="dc9b9-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dc9b9-139"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="dc9b9-140">成功。</span><span class="sxs-lookup"><span data-stu-id="dc9b9-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="dc9b9-141"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="dc9b9-142"><dt>**未知/未指定的錯誤**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="dc9b9-143"><dt>**無法在 Timeout 期限3內完成**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="dc9b9-144"><dt>**失敗**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="dc9b9-145"><dt>**不正確參數**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="dc9b9-146"><dt>**使用中**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="dc9b9-147">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="dc9b9-148"><dt>**方法參數檢查-轉換已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="dc9b9-149"><dt>**不正確狀態轉換**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="dc9b9-150"><dt>**不支援使用 Timeout 參數**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="dc9b9-151"><dt>**忙碌**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="dc9b9-152"><dt>**方法保留**</dt><dt>的 4100. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="dc9b9-153"><dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="dc9b9-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc9b9-154">Requirements</span></span>



| <span data-ttu-id="dc9b9-155">需求</span><span class="sxs-lookup"><span data-stu-id="dc9b9-155">Requirement</span></span> | <span data-ttu-id="dc9b9-156">值</span><span class="sxs-lookup"><span data-stu-id="dc9b9-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9b9-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc9b9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9b9-158">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc9b9-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dc9b9-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc9b9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9b9-160">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc9b9-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc9b9-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc9b9-161">Namespace</span></span><br/>                | <span data-ttu-id="dc9b9-162">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="dc9b9-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="dc9b9-163">MOF</span><span class="sxs-lookup"><span data-stu-id="dc9b9-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc9b9-164"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc9b9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9b9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc9b9-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc9b9-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc9b9-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc9b9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9b9-168">**Msvm \_ GuestServiceInterfaceComponent**</span><span class="sxs-lookup"><span data-stu-id="dc9b9-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

