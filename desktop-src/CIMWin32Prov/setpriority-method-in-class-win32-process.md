---
description: SetPriority&\# 32;WMI 類別方法會嘗試變更進程的執行優先權。
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Win32_Process 類別的 SetPriority 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510697"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="c9794-103">Win32 進程類別的 SetPriority 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c9794-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="c9794-104">**SetPriority** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試變更進程的執行優先權。</span><span class="sxs-lookup"><span data-stu-id="c9794-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="c9794-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c9794-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c9794-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c9794-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9794-107">語法</span><span class="sxs-lookup"><span data-stu-id="c9794-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="c9794-108">參數</span><span class="sxs-lookup"><span data-stu-id="c9794-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9794-109">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9794-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9794-110">進程的新優先順序類別。</span><span class="sxs-lookup"><span data-stu-id="c9794-110">New priority class for the process.</span></span> <span data-ttu-id="c9794-111">請注意，這些值與 [**Win32 \_ 進程**](win32-process.md)的 **Priority** 屬性中明確陳述的值不同。</span><span class="sxs-lookup"><span data-stu-id="c9794-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="c9794-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (64) </span><span class="sxs-lookup"><span data-stu-id="c9794-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-113">針對只有當系統閒置時才會執行之執行緒的進程指定。</span><span class="sxs-lookup"><span data-stu-id="c9794-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="c9794-114">進程的執行緒會被在較高優先順序類別中執行之進程的執行緒佔用，例如螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c9794-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="c9794-115">子進程會繼承閒置優先順序類別。</span><span class="sxs-lookup"><span data-stu-id="c9794-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="c9794-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**低於標準** (16384) </span><span class="sxs-lookup"><span data-stu-id="c9794-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-117">指出優先順序高於 **閒置 \_ 優先順序 \_ 類別**，但低於 **一般 \_ 優先順序 \_ 類別** 的進程。</span><span class="sxs-lookup"><span data-stu-id="c9794-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="c9794-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (32) </span><span class="sxs-lookup"><span data-stu-id="c9794-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-119">針對沒有特殊排程需求的進程指定。</span><span class="sxs-lookup"><span data-stu-id="c9794-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="c9794-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**高於一般** (32768) </span><span class="sxs-lookup"><span data-stu-id="c9794-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-121">指出優先順序高於 **一般 \_ 優先順序 \_ 類別** 但優先順序高於 **高 \_ 優先順序 \_** 類別的進程。</span><span class="sxs-lookup"><span data-stu-id="c9794-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="c9794-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**高優先順序** (128) </span><span class="sxs-lookup"><span data-stu-id="c9794-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-123">針對執行必須立即執行之時間關鍵工作的進程指定。</span><span class="sxs-lookup"><span data-stu-id="c9794-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="c9794-124">該處理序的執行緒會優先於正常或閒置優先權類別處理序的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c9794-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="c9794-125">其中一個範例是工作清單，當使用者呼叫時，無論作業系統上的負載為何，都必須快速回應。</span><span class="sxs-lookup"><span data-stu-id="c9794-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="c9794-126">使用高優先順序類別時請特別小心，因為高優先順序的類別應用程式幾乎可以使用所有可用的 CPU 時間。</span><span class="sxs-lookup"><span data-stu-id="c9794-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="c9794-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**即時** (256) </span><span class="sxs-lookup"><span data-stu-id="c9794-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="c9794-128">指定給具有最高優先順序的進程。</span><span class="sxs-lookup"><span data-stu-id="c9794-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="c9794-129">進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的作業系統進程。</span><span class="sxs-lookup"><span data-stu-id="c9794-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="c9794-130">例如，執行超過一小段時間間隔的即時程式可能導致磁碟快取無法排清或滑鼠沒有回應。</span><span class="sxs-lookup"><span data-stu-id="c9794-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9794-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9794-131">Return value</span></span>

<span data-ttu-id="c9794-132">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9794-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c9794-133">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="c9794-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c9794-134">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="c9794-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c9794-135">**成功完成** (0) </span><span class="sxs-lookup"><span data-stu-id="c9794-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-136">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="c9794-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-137">**許可權不足** (3) </span><span class="sxs-lookup"><span data-stu-id="c9794-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-138">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="c9794-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-139"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="c9794-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-140">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="c9794-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="c9794-141">**其他** (22 4294967295) </span><span class="sxs-lookup"><span data-stu-id="c9794-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c9794-142">備註</span><span class="sxs-lookup"><span data-stu-id="c9794-142">Remarks</span></span>

<span data-ttu-id="c9794-143">若要將優先權設定為即時，呼叫端必須具有 **SeIncreaseBasePriorityPrivilege** (**SE \_ inc. \_ 基本 \_ 優先權 \_ 許可權**) 。</span><span class="sxs-lookup"><span data-stu-id="c9794-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="c9794-144">如果沒有此許可權，優先順序最高的優先順序可以設定為高優先順序。</span><span class="sxs-lookup"><span data-stu-id="c9794-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="c9794-145">範例</span><span class="sxs-lookup"><span data-stu-id="c9794-145">Examples</span></span>

<span data-ttu-id="c9794-146">[ [修改執行中進程的優先順序](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) ] VBScript 範例會將執行中的 Notepad.exe 實例的優先順序從一般變更為一般。</span><span class="sxs-lookup"><span data-stu-id="c9794-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9794-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9794-147">Requirements</span></span>



| <span data-ttu-id="c9794-148">需求</span><span class="sxs-lookup"><span data-stu-id="c9794-148">Requirement</span></span> | <span data-ttu-id="c9794-149">值</span><span class="sxs-lookup"><span data-stu-id="c9794-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9794-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9794-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c9794-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9794-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9794-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9794-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c9794-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9794-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9794-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9794-154">Namespace</span></span><br/>                | <span data-ttu-id="c9794-155">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c9794-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9794-156">MOF</span><span class="sxs-lookup"><span data-stu-id="c9794-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9794-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9794-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9794-158">DLL</span><span class="sxs-lookup"><span data-stu-id="c9794-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9794-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9794-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9794-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9794-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9794-161">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9794-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c9794-162">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="c9794-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

