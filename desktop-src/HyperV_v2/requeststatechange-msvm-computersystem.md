---
description: 要求將虛擬機器的狀態變更為指定的值。
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Msvm_ComputerSystem 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195599"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="3fb61-103">Msvm it 類別的 RequestStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3fb61-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="3fb61-104">要求將虛擬機器的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="3fb61-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="3fb61-105">多次叫用 **RequestStateChange** 方法可能會導致較早的要求被覆寫或遺失。</span><span class="sxs-lookup"><span data-stu-id="3fb61-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="3fb61-106">只有代表虛擬機器的 Msvm 同機類別 [**\_**](msvm-computersystem.md) 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3fb61-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="3fb61-107">當狀態變更正在進行時，會將 **requestedstate** 屬性變更為 *requestedstate* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="3fb61-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb61-108">語法</span><span class="sxs-lookup"><span data-stu-id="3fb61-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3fb61-109">參數</span><span class="sxs-lookup"><span data-stu-id="3fb61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb61-110">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3fb61-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb61-111">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fb61-111">Type: **uint16**</span></span>

<span data-ttu-id="3fb61-112">新狀態。</span><span class="sxs-lookup"><span data-stu-id="3fb61-112">The new state.</span></span> <span data-ttu-id="3fb61-113">大於32767的值為 **DMTF** 建議的值，可能會變更。</span><span class="sxs-lookup"><span data-stu-id="3fb61-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="3fb61-114">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="3fb61-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3fb61-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3fb61-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-116">對應至 [**CIM \_ EnabledLogicalElement。**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fb61-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3fb61-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="3fb61-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-118">對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Enabled。</span><span class="sxs-lookup"><span data-stu-id="3fb61-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3fb61-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="3fb61-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-120">對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Disabled。</span><span class="sxs-lookup"><span data-stu-id="3fb61-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="3fb61-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="3fb61-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-122">僅適用于第1版 (V1) 的 Hyper-v。</span><span class="sxs-lookup"><span data-stu-id="3fb61-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="3fb61-123">虛擬機器正在透過關機服務關閉。</span><span class="sxs-lookup"><span data-stu-id="3fb61-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="3fb61-124">對應至 [**CIM \_ EnabledLogicalElement。 EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown。</span><span class="sxs-lookup"><span data-stu-id="3fb61-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="3fb61-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="3fb61-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-126">對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = 已啟用但離線。</span><span class="sxs-lookup"><span data-stu-id="3fb61-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="3fb61-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="3fb61-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="3fb61-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="3fb61-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="3fb61-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="3fb61-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-130">對應至 [**CIM \_ EnabledLogicalElement。 EnabledState**](/previous-versions//cc136818(v=vs.85)) = 靜止、已啟用但已暫停。</span><span class="sxs-lookup"><span data-stu-id="3fb61-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="3fb61-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="3fb61-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-132">狀態從 **Off** 轉換或 **儲存** 為 **執行中。**</span><span class="sxs-lookup"><span data-stu-id="3fb61-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="3fb61-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="3fb61-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-134">重設虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3fb61-134">Reset the virtual machine.</span></span> <span data-ttu-id="3fb61-135">對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Reset。</span><span class="sxs-lookup"><span data-stu-id="3fb61-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="3fb61-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**正在儲存** (32773) </span><span class="sxs-lookup"><span data-stu-id="3fb61-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-137">在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStateSaving**。</span><span class="sxs-lookup"><span data-stu-id="3fb61-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="3fb61-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**暫停** (32776) </span><span class="sxs-lookup"><span data-stu-id="3fb61-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-139">在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStatePausing**。</span><span class="sxs-lookup"><span data-stu-id="3fb61-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="3fb61-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**繼續** (32777) </span><span class="sxs-lookup"><span data-stu-id="3fb61-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-141">在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStateResuming**。</span><span class="sxs-lookup"><span data-stu-id="3fb61-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="3fb61-142">狀態從 **暫停\*\*\*\*轉換成執行中。**</span><span class="sxs-lookup"><span data-stu-id="3fb61-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="3fb61-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779) </span><span class="sxs-lookup"><span data-stu-id="3fb61-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-144">對應至 **EnabledStateFastSuspend**。</span><span class="sxs-lookup"><span data-stu-id="3fb61-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="3fb61-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780) </span><span class="sxs-lookup"><span data-stu-id="3fb61-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="3fb61-146">對應至 **EnabledStateFastSuspending**。</span><span class="sxs-lookup"><span data-stu-id="3fb61-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="3fb61-147">從執行到 **FastSaved\*\*\*\*的狀態** 轉換。</span><span class="sxs-lookup"><span data-stu-id="3fb61-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="3fb61-148">這些值代表重大狀態：</span><span class="sxs-lookup"><span data-stu-id="3fb61-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="3fb61-149">**RunningCritical** (32781) </span><span class="sxs-lookup"><span data-stu-id="3fb61-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="3fb61-150">**OffCritical** (32782) </span><span class="sxs-lookup"><span data-stu-id="3fb61-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="3fb61-151">**StoppingCritical** (32783) </span><span class="sxs-lookup"><span data-stu-id="3fb61-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="3fb61-152">**SavedCritical** (32784) </span><span class="sxs-lookup"><span data-stu-id="3fb61-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="3fb61-153">**PausedCritical** (32785) </span><span class="sxs-lookup"><span data-stu-id="3fb61-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="3fb61-154">**StartingCritical** (32786) </span><span class="sxs-lookup"><span data-stu-id="3fb61-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="3fb61-155">**ResetCritical** (32787) </span><span class="sxs-lookup"><span data-stu-id="3fb61-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="3fb61-156">**SavingCritical** (32788) </span><span class="sxs-lookup"><span data-stu-id="3fb61-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="3fb61-157">**PausingCritical** (32789) </span><span class="sxs-lookup"><span data-stu-id="3fb61-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="3fb61-158">**ResumingCritical** (32790) </span><span class="sxs-lookup"><span data-stu-id="3fb61-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="3fb61-159">**FastSavedCritical** (32791) </span><span class="sxs-lookup"><span data-stu-id="3fb61-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="3fb61-160">**FastSavingCritical** (32792) </span><span class="sxs-lookup"><span data-stu-id="3fb61-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="3fb61-161">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3fb61-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb61-162">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3fb61-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="3fb61-163">如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="3fb61-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="3fb61-164">如果有，則會使用傳回的參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="3fb61-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="3fb61-165">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3fb61-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb61-166">類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fb61-166">Type: **datetime**</span></span>

<span data-ttu-id="3fb61-167">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3fb61-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb61-168">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fb61-168">Return value</span></span>

<span data-ttu-id="3fb61-169">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3fb61-169">Type: **uint32**</span></span>

<span data-ttu-id="3fb61-170">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3fb61-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="3fb61-171">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3fb61-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="3fb61-172">Description</span><span class="sxs-lookup"><span data-stu-id="3fb61-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3fb61-173"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="3fb61-174">成功。</span><span class="sxs-lookup"><span data-stu-id="3fb61-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="3fb61-175"><dt>**方法參數檢查-轉換已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="3fb61-176">轉換是非同步。</span><span class="sxs-lookup"><span data-stu-id="3fb61-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="3fb61-177"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="3fb61-178">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="3fb61-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="3fb61-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-185"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="3fb61-186">不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="3fb61-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="3fb61-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="3fb61-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3fb61-190">備註</span><span class="sxs-lookup"><span data-stu-id="3fb61-190">Remarks</span></span>

<span data-ttu-id="3fb61-191">UAC 篩選可能會限制對 Msvm 的 [未使用] 類別的存取。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="3fb61-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3fb61-192">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="3fb61-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3fb61-193">範例</span><span class="sxs-lookup"><span data-stu-id="3fb61-193">Examples</span></span>

<span data-ttu-id="3fb61-194">下列 c # 範例會啟動或停用虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3fb61-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="3fb61-195">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="3fb61-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fb61-196">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="3fb61-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="3fb61-197">下列 Visual Basic Scripting Edition (VBScript) 範例會啟動或停用虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3fb61-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fb61-198">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="3fb61-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="3fb61-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fb61-199">Requirements</span></span>



| <span data-ttu-id="3fb61-200">需求</span><span class="sxs-lookup"><span data-stu-id="3fb61-200">Requirement</span></span> | <span data-ttu-id="3fb61-201">值</span><span class="sxs-lookup"><span data-stu-id="3fb61-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb61-202">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fb61-202">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb61-203">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb61-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fb61-204">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fb61-204">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb61-205">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb61-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fb61-206">命名空間</span><span class="sxs-lookup"><span data-stu-id="3fb61-206">Namespace</span></span><br/>                | <span data-ttu-id="3fb61-207">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fb61-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fb61-208">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb61-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb61-209"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb61-210">DLL</span><span class="sxs-lookup"><span data-stu-id="3fb61-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb61-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fb61-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fb61-212">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fb61-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb61-213">**Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="3fb61-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

