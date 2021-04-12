---
description: 要求狀態變更。
ms.assetid: 836ee3a1-e28e-4f84-8e1c-09f4a2ff0a25
title: Msvm_Memory 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 761a486f21f6c1cd8c61978038cc2d37bba8c288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320599"
---
# <a name="requeststatechange-method-of-the-msvm_memory-class"></a><span data-ttu-id="c6e52-103">Msvm Memory 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c6e52-103">RequestStateChange method of the Msvm\_Memory class</span></span>

<span data-ttu-id="c6e52-104">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c6e52-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e52-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6e52-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c6e52-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e52-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e52-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e52-108">新狀態。</span><span class="sxs-lookup"><span data-stu-id="c6e52-108">The new state.</span></span> <span data-ttu-id="c6e52-109">如果 **RequestStateChange** 方法的傳回碼為0或4096，資訊就會放在實例的 **RequestedState** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="c6e52-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="c6e52-110">如需詳細資訊，請參閱元素的 **EnabledState** 和 **RequestedState** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="c6e52-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="c6e52-111">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="c6e52-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c6e52-112">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="c6e52-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c6e52-113">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="c6e52-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="c6e52-114">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="c6e52-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="c6e52-115">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="c6e52-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="c6e52-116">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="c6e52-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="c6e52-117">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="c6e52-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c6e52-118">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="c6e52-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="c6e52-119">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="c6e52-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="c6e52-120">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="c6e52-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c6e52-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c6e52-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c6e52-122">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="c6e52-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c6e52-123">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6e52-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e52-124">可能包含建立之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 的參考，以追蹤方法調用所起始的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="c6e52-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="c6e52-125">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e52-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e52-126">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="c6e52-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c6e52-127">間隔格式必須用來指定 TimeoutPeriod。</span><span class="sxs-lookup"><span data-stu-id="c6e52-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="c6e52-128">值為0或 null 參數表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="c6e52-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="c6e52-129">如果這個屬性不包含0或 null，且執行不支援這個參數，則應該傳回「不支援使用 Timeout 參數」的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="c6e52-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e52-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6e52-130">Return value</span></span>

<span data-ttu-id="c6e52-131">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="c6e52-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c6e52-132">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c6e52-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6e52-133">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c6e52-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c6e52-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6e52-134">Requirements</span></span>



| <span data-ttu-id="c6e52-135">需求</span><span class="sxs-lookup"><span data-stu-id="c6e52-135">Requirement</span></span> | <span data-ttu-id="c6e52-136">值</span><span class="sxs-lookup"><span data-stu-id="c6e52-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e52-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6e52-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e52-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c6e52-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c6e52-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6e52-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e52-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6e52-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c6e52-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="c6e52-141">Namespace</span></span><br/>                | <span data-ttu-id="c6e52-142">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c6e52-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c6e52-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c6e52-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6e52-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c6e52-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6e52-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e52-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e52-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6e52-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c6e52-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6e52-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e52-148">**Msvm \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="c6e52-148">**Msvm\_Memory**</span></span>](msvm-memory.md)
</dt> </dl>

 

 




