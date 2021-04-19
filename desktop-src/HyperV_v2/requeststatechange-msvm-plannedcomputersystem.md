---
description: 要求已規劃的系統狀態會變更為指定的值。
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Msvm_PlannedComputerSystem 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978958"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="c2271-103">Msvm PlannedComputerSystem 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c2271-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="c2271-104">要求已規劃的系統狀態會變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="c2271-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2271-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2271-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c2271-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2271-107">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2271-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2271-108">所規劃系統的要求狀態。</span><span class="sxs-lookup"><span data-stu-id="c2271-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c2271-109">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="c2271-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c2271-110">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="c2271-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="c2271-111">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="c2271-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="c2271-112">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="c2271-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="c2271-113">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="c2271-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="c2271-114">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="c2271-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c2271-115">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="c2271-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="c2271-116">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="c2271-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="c2271-117">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="c2271-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c2271-118">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c2271-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c2271-119">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="c2271-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c2271-120">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2271-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2271-121">未使用此參數，且應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c2271-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c2271-122">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2271-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2271-123">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c2271-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2271-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2271-124">Return value</span></span>

<span data-ttu-id="c2271-125">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c2271-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="c2271-126">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c2271-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="c2271-127">Description</span><span class="sxs-lookup"><span data-stu-id="c2271-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2271-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="c2271-129">Success</span><span class="sxs-lookup"><span data-stu-id="c2271-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c2271-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="c2271-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="c2271-133">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c2271-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="c2271-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="c2271-140">不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="c2271-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="c2271-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="c2271-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="c2271-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2271-144">Requirements</span></span>



| <span data-ttu-id="c2271-145">需求</span><span class="sxs-lookup"><span data-stu-id="c2271-145">Requirement</span></span> | <span data-ttu-id="c2271-146">值</span><span class="sxs-lookup"><span data-stu-id="c2271-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2271-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2271-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c2271-148">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2271-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c2271-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2271-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c2271-150">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2271-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2271-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="c2271-151">Namespace</span></span><br/>                | <span data-ttu-id="c2271-152">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c2271-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c2271-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c2271-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2271-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2271-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c2271-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2271-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2271-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2271-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2271-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2271-158">**Msvm \_ PlannedComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="c2271-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




