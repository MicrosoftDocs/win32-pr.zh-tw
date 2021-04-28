---
description: Msvm_SyntheticKeyboard 類別的 RequestStateChange 方法-要求狀態變更。
ms.assetid: 984e8a68-bc95-4a8b-99d6-ac248e96c45e
title: Msvm_SyntheticKeyboard 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: eb8714dfc652cd1ba1a581b99cf5a4066159fb1e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109544"
---
# <a name="requeststatechange-method-of-the-msvm_synthetickeyboard-class"></a><span data-ttu-id="9675d-103">Msvm SyntheticKeyboard 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9675d-103">RequestStateChange method of the Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="9675d-104">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9675d-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="9675d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9675d-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9675d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9675d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9675d-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9675d-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9675d-108">針對元素要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="9675d-108">The state requested for the element.</span></span> <span data-ttu-id="9675d-109">如果 RequestStateChange 方法的傳回碼為 0 ( ' 已完成且沒有錯誤 ' ) ，或 4096 (0x1000)  ( ' 作業已啟動 ' ) ，則會將這項資訊放入實例的 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9675d-109">This information will be placed into the **RequestedState** property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="9675d-110">如需有關 *RequestedState* 值的詳細說明，請參閱 **EnabledState** 和 **RequestedState** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="9675d-110">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the *RequestedState* values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9675d-111">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="9675d-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9675d-112">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="9675d-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="9675d-113">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="9675d-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="9675d-114">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="9675d-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="9675d-115">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="9675d-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="9675d-116">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="9675d-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="9675d-117">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="9675d-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="9675d-118">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="9675d-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="9675d-119">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="9675d-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9675d-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9675d-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9675d-121">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="9675d-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9675d-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9675d-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9675d-123">可能包含建立之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 的參考，以追蹤方法調用所起始的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="9675d-123">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="9675d-124">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9675d-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9675d-125">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="9675d-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="9675d-126">間隔格式必須用來指定 TimeoutPeriod。</span><span class="sxs-lookup"><span data-stu-id="9675d-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="9675d-127">值為0或 null 參數表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="9675d-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="9675d-128">如果這個屬性不包含0或 null，且執行不支援這個參數，則應該傳回「不支援使用 Timeout 參數」的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9675d-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9675d-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="9675d-129">Return value</span></span>

<span data-ttu-id="9675d-130">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9675d-130">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9675d-131">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9675d-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9675d-132">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="9675d-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9675d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9675d-133">Requirements</span></span>



| <span data-ttu-id="9675d-134">需求</span><span class="sxs-lookup"><span data-stu-id="9675d-134">Requirement</span></span> | <span data-ttu-id="9675d-135">值</span><span class="sxs-lookup"><span data-stu-id="9675d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9675d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9675d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9675d-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9675d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9675d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9675d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9675d-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9675d-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9675d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="9675d-140">Namespace</span></span><br/>                | <span data-ttu-id="9675d-141">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9675d-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9675d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9675d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9675d-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9675d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9675d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9675d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9675d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9675d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9675d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9675d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9675d-147">**Msvm \_ SyntheticKeyboard**</span><span class="sxs-lookup"><span data-stu-id="9675d-147">**Msvm\_SyntheticKeyboard**</span></span>](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




