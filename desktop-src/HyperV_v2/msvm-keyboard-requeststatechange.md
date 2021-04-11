---
description: 要求變更元素的狀態。
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Msvm_Keyboard 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943532"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="50466-103">Msvm 鍵盤類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="50466-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="50466-104">要求變更元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="50466-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="50466-105">語法</span><span class="sxs-lookup"><span data-stu-id="50466-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="50466-106">參數</span><span class="sxs-lookup"><span data-stu-id="50466-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50466-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50466-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50466-108">針對元素要求的新狀態。</span><span class="sxs-lookup"><span data-stu-id="50466-108">The new state requested for the element.</span></span> <span data-ttu-id="50466-109">如果傳回碼為 0 ( ' 已完成且沒有錯誤 ' ) 、3 ( ' Timeout ' ) 或 4096 (0x1000)  ( ' 工作已啟動 ' ) ，則會將這項資訊放入實例的 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="50466-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="50466-110">如需有關 *RequestedState* 值的詳細說明，請參閱 **EnabledState** 和 **RequestedState** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="50466-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="50466-111">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="50466-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="50466-112">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="50466-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="50466-113">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="50466-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="50466-114">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="50466-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="50466-115">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="50466-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="50466-116">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="50466-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="50466-117">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="50466-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="50466-118">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="50466-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="50466-119">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="50466-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="50466-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="50466-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="50466-121">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="50466-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="50466-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50466-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50466-123">作業的參考。</span><span class="sxs-lookup"><span data-stu-id="50466-123">A reference to the job.</span></span> <span data-ttu-id="50466-124">如果工作已完成，此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="50466-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="50466-125">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50466-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50466-126">用戶端預期轉換至新狀態所需的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="50466-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="50466-127">間隔格式必須用來指定此超時時間。</span><span class="sxs-lookup"><span data-stu-id="50466-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="50466-128">值為0或 **Null** 表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="50466-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="50466-129">如果這個屬性不包含0或 **Null**，且執行不支援這個參數，則會傳回錯誤碼 4098 ( 「不支援使用 Timeout 參數」 ) 。</span><span class="sxs-lookup"><span data-stu-id="50466-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50466-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="50466-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="50466-131">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="50466-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50466-132">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="50466-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="50466-133">**未知或未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="50466-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="50466-134">**無法在 Timeout 期間內完成** (3) </span><span class="sxs-lookup"><span data-stu-id="50466-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="50466-135">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="50466-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="50466-136">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="50466-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="50466-137">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="50466-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="50466-138">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="50466-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="50466-139">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="50466-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="50466-140">**不正確狀態轉換** (4097) </span><span class="sxs-lookup"><span data-stu-id="50466-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="50466-141"> (4098) **不支援使用 Timeout 參數**</span><span class="sxs-lookup"><span data-stu-id="50466-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="50466-142">**忙碌** (4099) </span><span class="sxs-lookup"><span data-stu-id="50466-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="50466-143">**方法保留** (4100. 32767) </span><span class="sxs-lookup"><span data-stu-id="50466-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="50466-144">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="50466-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50466-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="50466-145">Requirements</span></span>



| <span data-ttu-id="50466-146">需求</span><span class="sxs-lookup"><span data-stu-id="50466-146">Requirement</span></span> | <span data-ttu-id="50466-147">值</span><span class="sxs-lookup"><span data-stu-id="50466-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50466-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50466-148">Minimum supported client</span></span><br/> | <span data-ttu-id="50466-149">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50466-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="50466-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50466-150">Minimum supported server</span></span><br/> | <span data-ttu-id="50466-151">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50466-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50466-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="50466-152">Namespace</span></span><br/>                | <span data-ttu-id="50466-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="50466-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="50466-154">MOF</span><span class="sxs-lookup"><span data-stu-id="50466-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50466-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="50466-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50466-156">DLL</span><span class="sxs-lookup"><span data-stu-id="50466-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50466-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50466-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50466-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50466-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50466-159">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="50466-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




