---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼500-999，適用于開發人員。
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: '系統錯誤碼 (500-999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190969"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="7ca71-103">系統錯誤碼 (500-999) </span><span class="sxs-lookup"><span data-stu-id="7ca71-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="7ca71-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="7ca71-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="7ca71-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="7ca71-106">下列清單描述 (錯誤500到 999) 的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="7ca71-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="7ca71-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="7ca71-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="7ca71-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**\_使用者 \_ 設定檔 \_ 載入錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-110">500 (0x1F4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-111">無法載入使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="7ca71-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**錯誤 \_ 算術 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="7ca71-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-113">534 (0x216) </span><span class="sxs-lookup"><span data-stu-id="7ca71-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-114">算術結果超過32個位。</span><span class="sxs-lookup"><span data-stu-id="7ca71-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**連接的錯誤 \_ 管道 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-116">535 (0x217) </span><span class="sxs-lookup"><span data-stu-id="7ca71-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-117">管道的另一端有處理常式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**錯誤 \_ 管道 \_ 接聽**</span><span class="sxs-lookup"><span data-stu-id="7ca71-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-119">536 (0x218) </span><span class="sxs-lookup"><span data-stu-id="7ca71-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-120">等候進程開啟管道的另一端。</span><span class="sxs-lookup"><span data-stu-id="7ca71-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**錯誤 \_ 驗證器 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="7ca71-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-122">537 (0x219) </span><span class="sxs-lookup"><span data-stu-id="7ca71-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-123">應用程式驗證器在目前的進程中發現錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**錯誤 \_ ABIOS \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-125">538 (0x21A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-126">ABIOS 子系統發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**錯誤 \_ WX86 \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="7ca71-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-128">539 (0x21B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-129">WX86 子系統發生警告。</span><span class="sxs-lookup"><span data-stu-id="7ca71-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**錯誤 \_ WX86 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-131">540 (0x21C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-132">WX86 子系統發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**錯誤 \_ 計時器 \_ 未 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="7ca71-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-134">541 (0x21D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-135">嘗試取消或設定具有相關聯的 APC 的計時器，且主體執行緒不是最初以關聯的 APC 常式設定計時器的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**錯誤 \_ 回溯**</span><span class="sxs-lookup"><span data-stu-id="7ca71-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-137">542 (0x21E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-138">回溯例外狀況程式碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**錯誤 \_ \_ 堆疊錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-140">543 (0x21F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-141">在回溯操作期間遇到無效或未對齊的堆疊。</span><span class="sxs-lookup"><span data-stu-id="7ca71-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**錯誤 \_ 不正確回溯 \_ \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="7ca71-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-143">544 (0x220) </span><span class="sxs-lookup"><span data-stu-id="7ca71-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-144">回溯作業期間發生不正確回溯目標。</span><span class="sxs-lookup"><span data-stu-id="7ca71-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**錯誤 \_ 不正確 \_ 埠 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="7ca71-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-146">545 (0x221) </span><span class="sxs-lookup"><span data-stu-id="7ca71-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-147">指定給 NtCreatePort 的物件屬性無效或指定給 NtConnectPort 的埠屬性無效</span><span class="sxs-lookup"><span data-stu-id="7ca71-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**錯誤 \_ 埠 \_ 訊息 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="7ca71-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-149">546 (0x222) </span><span class="sxs-lookup"><span data-stu-id="7ca71-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-150">傳遞至 NtRequestPort 或 NtRequestWaitReplyPort 的訊息長度超過埠允許的最大訊息數。</span><span class="sxs-lookup"><span data-stu-id="7ca71-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**錯誤 \_ 不正確 \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-152">547 (0x223) </span><span class="sxs-lookup"><span data-stu-id="7ca71-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-153">嘗試降低低於目前使用量的配額限制。</span><span class="sxs-lookup"><span data-stu-id="7ca71-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**\_ \_ 已 \_ 附加的錯誤裝置**</span><span class="sxs-lookup"><span data-stu-id="7ca71-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-155">548 (0x224) </span><span class="sxs-lookup"><span data-stu-id="7ca71-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-156">嘗試附加至已附加至另一個裝置的裝置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**錯誤 \_ 指令 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="7ca71-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-158">549 (0x225) </span><span class="sxs-lookup"><span data-stu-id="7ca71-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-159">嘗試在未對齊的位址執行指令，而主機系統不支援未對齊的指令參考。</span><span class="sxs-lookup"><span data-stu-id="7ca71-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**\_ \_ 未啟動錯誤 \_ 分析**</span><span class="sxs-lookup"><span data-stu-id="7ca71-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-161">550 (0x226) </span><span class="sxs-lookup"><span data-stu-id="7ca71-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-162">未啟動程式碼剖析。</span><span class="sxs-lookup"><span data-stu-id="7ca71-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ 未 \_ 停止錯誤程式碼剖析**</span><span class="sxs-lookup"><span data-stu-id="7ca71-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-164">551 (0x227) </span><span class="sxs-lookup"><span data-stu-id="7ca71-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-165">未停止程式碼剖析。</span><span class="sxs-lookup"><span data-stu-id="7ca71-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**錯誤 \_ 無法 \_ \_ 解讀**</span><span class="sxs-lookup"><span data-stu-id="7ca71-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-167">552 (0x228) </span><span class="sxs-lookup"><span data-stu-id="7ca71-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-168">傳遞的 ACL 未包含必要的最小資訊。</span><span class="sxs-lookup"><span data-stu-id="7ca71-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**\_限制錯誤 \_ 分析 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-170">553 (0x229) </span><span class="sxs-lookup"><span data-stu-id="7ca71-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-171">使用中的分析物件數目已達上限，而且無法再啟動。</span><span class="sxs-lookup"><span data-stu-id="7ca71-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**錯誤 \_ 無法 \_ 等候**</span><span class="sxs-lookup"><span data-stu-id="7ca71-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-173">554 (0x22A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-174">用來表示作業無法繼續，而不會封鎖 i/o。</span><span class="sxs-lookup"><span data-stu-id="7ca71-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**錯誤 \_ 無法 \_ 終止 \_ 本身**</span><span class="sxs-lookup"><span data-stu-id="7ca71-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-176">555 (0x22B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-177">表示執行緒依預設會嘗試終止本身 (稱為 NtTerminateThread 與 **Null**) ，而且它是目前進程中的最後一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**未 \_ 預期的錯誤 \_ MM \_ CREATE \_ ERR**</span><span class="sxs-lookup"><span data-stu-id="7ca71-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-179">556 (0x22C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-180">如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="7ca71-181">不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**錯誤未 \_ 預期的 \_ MM \_ 對應 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-183">557 (0x22D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-184">如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="7ca71-185">不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**未預期的錯誤， \_ \_ \_ 擴充 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-187">558 (0x22E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-188">如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="7ca71-189">不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**錯誤 \_ 的 \_ 函數 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="7ca71-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-191">559 (0x22F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-192">在回溯作業期間遇到格式不正確的函式資料表。</span><span class="sxs-lookup"><span data-stu-id="7ca71-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**錯誤， \_ 不會 \_ \_ 轉譯 GUID**</span><span class="sxs-lookup"><span data-stu-id="7ca71-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-194">560 (0x230) </span><span class="sxs-lookup"><span data-stu-id="7ca71-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-195">指出嘗試將保護指派給檔案系統檔案或目錄，而安全描述項中的其中一個 Sid 無法轉譯為檔案系統可儲存的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7ca71-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="7ca71-196">這會導致保護嘗試失敗，這可能會導致檔案建立嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**\_不正確 \_ LDT \_ 大小錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-198">561 (0x231) </span><span class="sxs-lookup"><span data-stu-id="7ca71-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-199">指出嘗試藉由設定其大小來擴大 LDT，或大小不是偶數的選取器。</span><span class="sxs-lookup"><span data-stu-id="7ca71-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**錯誤 \_ 不正確 \_ LDT \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="7ca71-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-201">563 (0x233) </span><span class="sxs-lookup"><span data-stu-id="7ca71-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-202">指出 LDT 資訊的起始值不是選取器大小的整數倍數。</span><span class="sxs-lookup"><span data-stu-id="7ca71-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**錯誤 \_ 不正確 \_ LDT \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="7ca71-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-204">564 (0x234) </span><span class="sxs-lookup"><span data-stu-id="7ca71-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-205">指出使用者在嘗試設定 Ldt 描述項時，提供了不正確描述項。</span><span class="sxs-lookup"><span data-stu-id="7ca71-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**錯誤 \_ 太 \_ 多 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="7ca71-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-207">565 (0x235) </span><span class="sxs-lookup"><span data-stu-id="7ca71-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-208">表示進程的執行緒太多，無法執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="7ca71-209">例如，只有當進程有零個或一個執行緒時，才會執行主要權杖的指派。</span><span class="sxs-lookup"><span data-stu-id="7ca71-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**錯誤 \_ 執行緒 \_ 不 \_ 在 \_ 進程中**</span><span class="sxs-lookup"><span data-stu-id="7ca71-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-211">566 (0x236) </span><span class="sxs-lookup"><span data-stu-id="7ca71-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-212">嘗試在特定進程內的執行緒上操作，但指定的執行緒不在指定的處理常式中。</span><span class="sxs-lookup"><span data-stu-id="7ca71-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_超過錯誤分頁檔 \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-214">567 (0x237) </span><span class="sxs-lookup"><span data-stu-id="7ca71-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-215">超過分頁檔案配額。</span><span class="sxs-lookup"><span data-stu-id="7ca71-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**錯誤 \_ 登入 \_ 伺服器 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="7ca71-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-217">568 (0x238) </span><span class="sxs-lookup"><span data-stu-id="7ca71-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-218">Netlogon 服務無法啟動，因為網域中執行的另一個 Netlogon 服務與指定的角色發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7ca71-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**\_需要同步處理錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-220">569 (0x239) </span><span class="sxs-lookup"><span data-stu-id="7ca71-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-221">Windows 伺服器上的 SAM 資料庫與網域控制站上的複本之間的同步處理有明顯的差異。</span><span class="sxs-lookup"><span data-stu-id="7ca71-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="7ca71-222">需要完整的同步處理。</span><span class="sxs-lookup"><span data-stu-id="7ca71-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**錯誤 \_ 網路 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-224">570 (0x23A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-225">NtCreateFile API 失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="7ca71-226">此錯誤永遠不會傳回給應用程式，而是 Windows Lan Manager 重新導向程式在其內部錯誤對應常式中使用的預留位置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**錯誤 \_ IO \_ 許可權 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-228">571 (0x23B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-229">{許可權失敗}無法變更進程的 i/o 許可權。</span><span class="sxs-lookup"><span data-stu-id="7ca71-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR \_ CONTROL \_ C \_ EXIT**</span><span class="sxs-lookup"><span data-stu-id="7ca71-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-231">572 (0x23C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-232">{Application Exit by CTRL + C}應用程式因 CTRL + C 而終止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**錯誤 \_ 遺失 \_ SYSTEMFILE**</span><span class="sxs-lookup"><span data-stu-id="7ca71-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-234">573 (0x23D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-235">{遺失系統檔案}所需的系統檔案% hs 不正確或遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**錯誤 \_ 未處理的 \_ 例外狀況**</span><span class="sxs-lookup"><span data-stu-id="7ca71-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-237">574 (0x23E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-238">{應用程式錯誤}在位置 0x% 08lx 的應用程式中發生例外狀況% s (0x% 08lx) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**錯誤 \_ 應用程式 \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-240">575 (0x23F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-241">{應用程式錯誤}應用程式無法正確啟動 (0x% lx) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="7ca71-242">按一下 [確定] 以關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**錯誤 \_ 頁面 \_ 建立 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-244">576 (0x240) </span><span class="sxs-lookup"><span data-stu-id="7ca71-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-245">{無法建立分頁檔案}建立分頁檔案% hs 失敗 (% lx) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="7ca71-246">要求的大小為% ld。</span><span class="sxs-lookup"><span data-stu-id="7ca71-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**錯誤 \_ 不正確 \_ 影像 \_ 雜湊**</span><span class="sxs-lookup"><span data-stu-id="7ca71-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-248">577 (0x241) </span><span class="sxs-lookup"><span data-stu-id="7ca71-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-249">Windows 無法驗證此檔案的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="7ca71-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="7ca71-250">最近的硬體或軟體變更可能已安裝簽署錯誤或損毀的檔案，或可能是來自不明來源的惡意軟體。</span><span class="sxs-lookup"><span data-stu-id="7ca71-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**錯誤 \_ 的 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="7ca71-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-252">578 (0x242) </span><span class="sxs-lookup"><span data-stu-id="7ca71-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-253">{未指定分頁檔案}系統組態中未指定任何分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**錯誤不 \_ 合法的 \_ FLOAT \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7ca71-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-255">579 (0x243) </span><span class="sxs-lookup"><span data-stu-id="7ca71-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-256">意外發出浮點指令和浮點硬體的實際模式應用程式不存在。</span><span class="sxs-lookup"><span data-stu-id="7ca71-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**錯誤 \_ 無 \_ 事件 \_ 配對**</span><span class="sxs-lookup"><span data-stu-id="7ca71-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-258">580 (0x244) </span><span class="sxs-lookup"><span data-stu-id="7ca71-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-259">使用執行緒特定用戶端/伺服器事件組物件執行事件配對同步處理作業，但沒有與執行緒相關聯的事件配對物件。</span><span class="sxs-lookup"><span data-stu-id="7ca71-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**錯誤 \_ 網域 \_ CTRLR \_ 設定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-261">581 (0x245) </span><span class="sxs-lookup"><span data-stu-id="7ca71-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-262">Windows Server 的設定不正確。</span><span class="sxs-lookup"><span data-stu-id="7ca71-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**錯誤不 \_ 合法的 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="7ca71-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-264">582 (0x246) </span><span class="sxs-lookup"><span data-stu-id="7ca71-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-265">遇到不合法的字元。</span><span class="sxs-lookup"><span data-stu-id="7ca71-265">An illegal character was encountered.</span></span> <span data-ttu-id="7ca71-266">若為多位元組字元集，則會包含前導位元組，而不含後續的後隨位元組。</span><span class="sxs-lookup"><span data-stu-id="7ca71-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="7ca71-267">對於 Unicode 字元集，這包括了0xFFFF 和0xFFFE 的字元。</span><span class="sxs-lookup"><span data-stu-id="7ca71-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**錯誤 \_ 未定義 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="7ca71-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-269">583 (0x247) </span><span class="sxs-lookup"><span data-stu-id="7ca71-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-270">Unicode 字元不會在安裝于系統上的 Unicode 字元集中定義。</span><span class="sxs-lookup"><span data-stu-id="7ca71-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**磁片區錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-272">584 (0x248) </span><span class="sxs-lookup"><span data-stu-id="7ca71-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-273">無法在磁片磁碟機上建立分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**錯誤 \_ BIOS \_ 無法 \_ \_ 連接 \_ 中斷**</span><span class="sxs-lookup"><span data-stu-id="7ca71-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-275">585 (0x249) </span><span class="sxs-lookup"><span data-stu-id="7ca71-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-276">系統 BIOS 無法將系統中斷連接到裝置所連線的裝置或匯流排。</span><span class="sxs-lookup"><span data-stu-id="7ca71-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**\_備份 \_ 控制器時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-278">586 (0x24A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-279">這項作業只允許用於網域的主域控制站。</span><span class="sxs-lookup"><span data-stu-id="7ca71-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_超過錯誤變異 \_ 數限制 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-281">587 (0x24B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-282">嘗試取得變異數，使其最大計數已超過。</span><span class="sxs-lookup"><span data-stu-id="7ca71-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**\_需要錯誤 FS \_ 驅動程式 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-284">588 (0x24C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-285">已存取磁片區，但該磁片區的檔案系統驅動程式尚未載入。</span><span class="sxs-lookup"><span data-stu-id="7ca71-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**錯誤 \_ 無法 \_ 載入 \_ 登錄 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="7ca71-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-287">589 (0x24D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-288">{Registry File 失敗}登錄無法載入 hive (檔) ：% hs 或其記錄檔或其他檔案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="7ca71-289">它已損毀、不存在或不可寫入。</span><span class="sxs-lookup"><span data-stu-id="7ca71-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**錯誤的 \_ DEBUG \_ 附加 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-291">590 (0x24E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-292">{ [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)中發生未預期的失敗}處理 **DebugActiveProcess** API 要求時發生未預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="7ca71-293">您可以選擇 [確定] 終止進程，或選擇 [取消] 忽略錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**\_系統 \_ 進程 \_ 終止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-295">591 (0x24F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-296">{嚴重系統錯誤}% Hs 系統進程意外結束，狀態為 0x% 08x (0x% 08x 0x% 08x) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="7ca71-297">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="7ca71-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**錯誤 \_ 資料 \_ 不 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="7ca71-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-299">592 (0x250) </span><span class="sxs-lookup"><span data-stu-id="7ca71-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-300">{不接受資料}TDI 用戶端無法處理在指示期間收到的資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**錯誤的 \_ VDM \_ 硬性 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-302">593 (0x251) </span><span class="sxs-lookup"><span data-stu-id="7ca71-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-303">NTVDM 發生硬性錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**錯誤 \_ 驅動程式 \_ 取消 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7ca71-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-305">594 (0x252) </span><span class="sxs-lookup"><span data-stu-id="7ca71-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-306">{取消 Timeout}驅動程式% hs 無法在分配的時間內完成取消的 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="7ca71-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**錯誤 \_ 回復 \_ 訊息 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="7ca71-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-308">595 (0x253) </span><span class="sxs-lookup"><span data-stu-id="7ca71-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-309">{回復訊息不符}已嘗試回復 LPC 訊息，但訊息中的用戶端識別碼所指定的執行緒未在該訊息上等候。</span><span class="sxs-lookup"><span data-stu-id="7ca71-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**\_ \_ WRITEBEHIND 資料遺失 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-311">596 (0x254) </span><span class="sxs-lookup"><span data-stu-id="7ca71-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-312">{延遲寫入失敗}Windows 無法儲存檔案% hs 的所有資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="7ca71-313">資料已遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-313">The data has been lost.</span></span> <span data-ttu-id="7ca71-314">發生此錯誤的原因可能是您的電腦硬體或網路連線失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="7ca71-315">請嘗試將此檔案儲存在其他位置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**錯誤 \_ 用戶端 \_ 伺服器 \_ 參數 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="7ca71-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-317">597 (0x255) </span><span class="sxs-lookup"><span data-stu-id="7ca71-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-318">在 [用戶端/伺服器共用記憶體] 視窗中傳遞給伺服器的參數 (s) 無效。</span><span class="sxs-lookup"><span data-stu-id="7ca71-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="7ca71-319">共用記憶體視窗中可能已放置太多資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**錯誤 \_ 不是 \_ 小型 \_ 串流**</span><span class="sxs-lookup"><span data-stu-id="7ca71-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-321">598 (0x256) </span><span class="sxs-lookup"><span data-stu-id="7ca71-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-322">資料流程不是小型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7ca71-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**錯誤 \_ 堆疊 \_ 溢位 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="7ca71-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-324">599 (0x257) </span><span class="sxs-lookup"><span data-stu-id="7ca71-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-325">要求必須由堆疊溢位程式碼處理。</span><span class="sxs-lookup"><span data-stu-id="7ca71-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**\_轉換 \_ 成 \_ 大型的錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-327">600 (0x258) </span><span class="sxs-lookup"><span data-stu-id="7ca71-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-328">指出如何處理配置作業的內部 .OFS 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="7ca71-329">當包含的 onode 移動或範圍資料流程轉換成大型資料流程之後，就會重試。</span><span class="sxs-lookup"><span data-stu-id="7ca71-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**\_發現 \_ 超出 \_ 範圍的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-331">601 (0x259) </span><span class="sxs-lookup"><span data-stu-id="7ca71-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-332">嘗試尋找物件在磁片區上找到依識別碼比對的物件，但它不在用於作業的控制碼範圍內。</span><span class="sxs-lookup"><span data-stu-id="7ca71-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**\_配置 \_ BUCKET 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-334">602 (0x25A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-335">Bucket 陣列必須成長。</span><span class="sxs-lookup"><span data-stu-id="7ca71-335">The bucket array must be grown.</span></span> <span data-ttu-id="7ca71-336">這麼做之後，請重試交易。</span><span class="sxs-lookup"><span data-stu-id="7ca71-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**錯誤 \_ 馬紹爾 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="7ca71-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-338">603 (0x25B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-339">使用者/核心封送處理緩衝區已溢位。</span><span class="sxs-lookup"><span data-stu-id="7ca71-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**錯誤 \_ 不正確 \_ 變異**</span><span class="sxs-lookup"><span data-stu-id="7ca71-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-341">604 (0x25C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-342">提供的 variant 結構包含不正確資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**錯誤 \_ 的 \_ 壓縮 \_ 緩衝區錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-344">605 (0x25D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-345">指定的緩衝區包含格式不正確的資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**錯誤 \_ 審核 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-347">606 (0x25E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-348">{Audit Failed}嘗試產生安全性審核失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_ \_ \_ 未設定錯誤計時器 \_ 解析**</span><span class="sxs-lookup"><span data-stu-id="7ca71-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-350">607 (0x25F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-351">目前的進程先前未設定計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="7ca71-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**錯誤 \_ 的 \_ 登入 \_ 資訊不足**</span><span class="sxs-lookup"><span data-stu-id="7ca71-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-353">608 (0x260) </span><span class="sxs-lookup"><span data-stu-id="7ca71-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-354">沒有足夠的帳戶資訊可供您登入。</span><span class="sxs-lookup"><span data-stu-id="7ca71-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**錯誤 \_ 的 \_ DLL 進入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="7ca71-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-356">609 (0x261) </span><span class="sxs-lookup"><span data-stu-id="7ca71-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-357">{不正確 DLL Entrypoint}未正確寫入動態連結程式庫% hs。</span><span class="sxs-lookup"><span data-stu-id="7ca71-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="7ca71-358">堆疊指標處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="7ca71-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="7ca71-359">Entrypoint 應宣告為 WINAPI 或 STDCALL。</span><span class="sxs-lookup"><span data-stu-id="7ca71-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="7ca71-360">選取 [是] 以使 DLL 載入失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="7ca71-361">選取 [否] 以繼續執行。</span><span class="sxs-lookup"><span data-stu-id="7ca71-361">Select NO to continue execution.</span></span> <span data-ttu-id="7ca71-362">選取 [否] 可能會導致應用程式無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**錯誤錯誤的 \_ \_ 服務進入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="7ca71-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-364">610 (0x262) </span><span class="sxs-lookup"><span data-stu-id="7ca71-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-365">{不正確服務回呼 Entrypoint}% Hs 服務的寫入不正確。</span><span class="sxs-lookup"><span data-stu-id="7ca71-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="7ca71-366">堆疊指標處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="7ca71-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="7ca71-367">回呼進入點應宣告為 WINAPI 或 STDCALL。</span><span class="sxs-lookup"><span data-stu-id="7ca71-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="7ca71-368">選取 [確定] 將會導致服務繼續操作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="7ca71-369">不過，服務進程的運作方式可能不正確。</span><span class="sxs-lookup"><span data-stu-id="7ca71-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**\_IP \_ 位址 \_ CONFLICT1 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-371">611 (0x263) </span><span class="sxs-lookup"><span data-stu-id="7ca71-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-372">IP 位址與網路上的其他系統發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7ca71-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**\_IP \_ 位址 \_ CONFLICT2 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-374">612 (0x264) </span><span class="sxs-lookup"><span data-stu-id="7ca71-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-375">IP 位址與網路上的其他系統發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7ca71-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**錯誤 \_ 登錄 \_ 配額 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="7ca71-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-377">613 (0x265) </span><span class="sxs-lookup"><span data-stu-id="7ca71-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-378">{註冊表空間不足}系統已到達登錄的系統部分所允許的大小上限。</span><span class="sxs-lookup"><span data-stu-id="7ca71-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="7ca71-379">將會忽略其他儲存體要求。</span><span class="sxs-lookup"><span data-stu-id="7ca71-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**錯誤 \_ 不使用 \_ 回呼 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-381">614 (0x266) </span><span class="sxs-lookup"><span data-stu-id="7ca71-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-382">當沒有任何回呼處於作用中狀態時，無法執行回呼傳回系統服務。</span><span class="sxs-lookup"><span data-stu-id="7ca71-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**錯誤 \_ PWD \_ 太 \_ 短**</span><span class="sxs-lookup"><span data-stu-id="7ca71-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-384">615 (0x267) </span><span class="sxs-lookup"><span data-stu-id="7ca71-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-385">提供的密碼太短，無法符合您的使用者帳戶原則。</span><span class="sxs-lookup"><span data-stu-id="7ca71-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="7ca71-386">請選擇較長的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**錯誤 \_ PWD \_ 太 \_ 晚**</span><span class="sxs-lookup"><span data-stu-id="7ca71-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-388">616 (0x268) </span><span class="sxs-lookup"><span data-stu-id="7ca71-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-389">您的使用者帳戶原則不允許您太頻繁地變更密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="7ca71-390">這麼做是為了防止使用者變更回熟悉但可能發現的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="7ca71-391">如果您認為您的密碼已遭盜用，請立即洽詢您的系統管理員，以指派新的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**錯誤 \_ PWD \_ 記錄 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="7ca71-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-393">617 (0x269) </span><span class="sxs-lookup"><span data-stu-id="7ca71-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-394">您已嘗試將您的密碼變更為您過去使用過的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="7ca71-395">您的使用者帳戶原則不允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="7ca71-396">請選取您先前未使用過的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**錯誤 \_ 不支援的 \_ 壓縮**</span><span class="sxs-lookup"><span data-stu-id="7ca71-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-398">618 (0x26A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-399">不支援指定的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**錯誤 \_ 不正確 \_ HW \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="7ca71-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-401">619 (0x26B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-402">指定的硬體設定檔設定無效。</span><span class="sxs-lookup"><span data-stu-id="7ca71-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**錯誤 \_ 不正確 \_ PLUGPLAY \_ 裝置 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="7ca71-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-404">620 (0x26C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-405">指定的隨插即用登錄裝置路徑無效。</span><span class="sxs-lookup"><span data-stu-id="7ca71-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**錯誤 \_ 配額 \_ 清單 \_ 不一致**</span><span class="sxs-lookup"><span data-stu-id="7ca71-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-407">621 (0x26D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-408">指定的配額清單與其描述項在內部不一致。</span><span class="sxs-lookup"><span data-stu-id="7ca71-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**錯誤 \_ 評估 \_ 到期日**</span><span class="sxs-lookup"><span data-stu-id="7ca71-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-410">622 (0x26E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-411">{Windows 評估通知}此 Windows 安裝的評估期間已過期。</span><span class="sxs-lookup"><span data-stu-id="7ca71-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="7ca71-412">此系統會在1小時內關機。</span><span class="sxs-lookup"><span data-stu-id="7ca71-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="7ca71-413">若要還原此 Windows 安裝的存取權，請使用此產品的授權散發升級此安裝。</span><span class="sxs-lookup"><span data-stu-id="7ca71-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**錯誤不 \_ 合法的 \_ DLL 重新配置 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-415">623 (0x26F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-416">{不合法的系統 DLL 重新配置}系統 DLL% hs 已在記憶體中重新置放。</span><span class="sxs-lookup"><span data-stu-id="7ca71-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="7ca71-417">應用程式將無法正常執行。</span><span class="sxs-lookup"><span data-stu-id="7ca71-417">The application will not run properly.</span></span> <span data-ttu-id="7ca71-418">發生重新配置的原因是 DLL% hs 已佔用保留給 Windows 系統 Dll 的位址範圍。</span><span class="sxs-lookup"><span data-stu-id="7ca71-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="7ca71-419">提供 DLL 的廠商應該連接至新的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7ca71-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**錯誤 \_ DLL \_ 初始化 \_ 失敗 \_ 登出**</span><span class="sxs-lookup"><span data-stu-id="7ca71-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-421">624 (0x270) </span><span class="sxs-lookup"><span data-stu-id="7ca71-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-422">{DLL 初始化失敗}應用程式無法初始化，因為視窗站正在關機。</span><span class="sxs-lookup"><span data-stu-id="7ca71-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**錯誤 \_ 驗證 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="7ca71-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-424">625 (0x271) </span><span class="sxs-lookup"><span data-stu-id="7ca71-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-425">驗證程式必須繼續進行下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="7ca71-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**錯誤 \_ 不 \_ \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="7ca71-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-427">626 (0x272) </span><span class="sxs-lookup"><span data-stu-id="7ca71-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-428">目前的索引列舉沒有相符的專案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**錯誤 \_ 範圍 \_ 清單 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="7ca71-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-430">627 (0x273) </span><span class="sxs-lookup"><span data-stu-id="7ca71-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-431">因為發生衝突，所以無法將範圍加入至範圍清單。</span><span class="sxs-lookup"><span data-stu-id="7ca71-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**錯誤 \_ 伺服器 \_ SID \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="7ca71-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-433">628 (0x274) </span><span class="sxs-lookup"><span data-stu-id="7ca71-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-434">伺服器進程在與用戶端所需的 SID 不同的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="7ca71-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**錯誤 \_ 無法 \_ 啟用 \_ 拒絕 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-436">629 (0x275) </span><span class="sxs-lookup"><span data-stu-id="7ca71-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-437">無法啟用標示為僅供拒絕使用的群組。</span><span class="sxs-lookup"><span data-stu-id="7ca71-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**錯誤 \_ 浮點數 \_ 多個 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-439">630 (0x276) </span><span class="sxs-lookup"><span data-stu-id="7ca71-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-440">意外多個浮點錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR \_ FLOAT \_ 多重 \_ 陷阱**</span><span class="sxs-lookup"><span data-stu-id="7ca71-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-442">631 (0x277) </span><span class="sxs-lookup"><span data-stu-id="7ca71-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-443">意外多個浮點數陷阱。</span><span class="sxs-lookup"><span data-stu-id="7ca71-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**錯誤 \_ NOINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="7ca71-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-445">632 (0x278) </span><span class="sxs-lookup"><span data-stu-id="7ca71-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-446">不支援要求的介面。</span><span class="sxs-lookup"><span data-stu-id="7ca71-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**錯誤 \_ 驅動程式 \_ 無法 \_ 進入睡眠狀態**</span><span class="sxs-lookup"><span data-stu-id="7ca71-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-448">633 (0x279) </span><span class="sxs-lookup"><span data-stu-id="7ca71-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-449">{系統待命失敗}驅動程式% hs 不支援待命模式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="7ca71-450">更新此驅動程式可能會允許系統進入待命模式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**錯誤損毀的 \_ \_ 系統檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-452">634 (0x27A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-453">系統檔案 %1 已損毀，已被取代。</span><span class="sxs-lookup"><span data-stu-id="7ca71-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**錯誤 \_ 承諾用量 \_ 下限**</span><span class="sxs-lookup"><span data-stu-id="7ca71-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-455">635 (0x27B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-456">{虛擬記憶體下限太低}您系統的虛擬記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="7ca71-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="7ca71-457">Windows 正在增加虛擬記憶體分頁檔的大小。</span><span class="sxs-lookup"><span data-stu-id="7ca71-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="7ca71-458">在此過程中，某些應用程式的記憶體要求可能會被拒絕。</span><span class="sxs-lookup"><span data-stu-id="7ca71-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="7ca71-459">如需詳細資訊，請參閱說明。</span><span class="sxs-lookup"><span data-stu-id="7ca71-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**錯誤 \_ PNP \_ 重新開機 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="7ca71-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-461">636 (0x27C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-462">已移除裝置，因此必須重新開機列舉。</span><span class="sxs-lookup"><span data-stu-id="7ca71-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**錯誤 \_ 的 \_ 系統 \_ 映射 \_ 簽名錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-464">637 (0x27D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-465">{嚴重系統錯誤}系統映射% s 未正確簽署。</span><span class="sxs-lookup"><span data-stu-id="7ca71-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="7ca71-466">檔案已取代為已簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="7ca71-467">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="7ca71-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**\_ \_ 需要重新開機錯誤 PNP \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-469">638 (0x27E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-470">裝置不會在重新開機的情況下啟動。</span><span class="sxs-lookup"><span data-stu-id="7ca71-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**錯誤 \_ 的 \_ 電源不足**</span><span class="sxs-lookup"><span data-stu-id="7ca71-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-472">639 (0x27F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-473">沒有足夠的電源可以完成要求的作業。</span><span class="sxs-lookup"><span data-stu-id="7ca71-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**錯誤 \_ 多個錯誤 \_ \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="7ca71-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-475">640 (0x280) </span><span class="sxs-lookup"><span data-stu-id="7ca71-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-476">錯誤 \_ 多個錯誤 \_ \_ 違規</span><span class="sxs-lookup"><span data-stu-id="7ca71-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**錯誤 \_ 系統 \_ 關機**</span><span class="sxs-lookup"><span data-stu-id="7ca71-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-478">641 (0x281) </span><span class="sxs-lookup"><span data-stu-id="7ca71-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-479">系統正在關機。</span><span class="sxs-lookup"><span data-stu-id="7ca71-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_ \_ 未設定錯誤 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="7ca71-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-481">642 (0x282) </span><span class="sxs-lookup"><span data-stu-id="7ca71-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-482">嘗試移除 DebugPort 的進程，但尚未與進程建立關聯的埠。</span><span class="sxs-lookup"><span data-stu-id="7ca71-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**錯誤 \_ DS \_ 版本 \_ 檢查 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-484">643 (0x283) </span><span class="sxs-lookup"><span data-stu-id="7ca71-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-485">此版本的 Windows 與目錄樹系、網域或網域控制站的行為版本不相容。</span><span class="sxs-lookup"><span data-stu-id="7ca71-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_ \_ 找不到錯誤範圍 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-487">644 (0x284) </span><span class="sxs-lookup"><span data-stu-id="7ca71-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-488">在範圍清單中找不到指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="7ca71-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**錯誤 \_ 的 \_ 安全 \_ 模式 \_ 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="7ca71-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-490">646 (0x286) </span><span class="sxs-lookup"><span data-stu-id="7ca71-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-491">驅動程式未載入，因為系統開機進入安全模式。</span><span class="sxs-lookup"><span data-stu-id="7ca71-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**\_ \_ 驅動程式專案錯誤失敗 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-493">647 (0x287) </span><span class="sxs-lookup"><span data-stu-id="7ca71-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-494">驅動程式未載入，因為它的初始化呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**錯誤 \_ 裝置 \_ 列舉 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-496">648 (0x288) </span><span class="sxs-lookup"><span data-stu-id="7ca71-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-497">"% Hs" 在套用電源或讀取裝置設定時，發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="7ca71-498">這可能是因為您的硬體失敗或連線不佳所造成。</span><span class="sxs-lookup"><span data-stu-id="7ca71-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**錯誤 \_ 裝入 \_ 點 \_ 未 \_ 解決**</span><span class="sxs-lookup"><span data-stu-id="7ca71-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-500">649 (0x289) </span><span class="sxs-lookup"><span data-stu-id="7ca71-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-501">建立作業失敗，因為名稱至少包含一個掛接點，而該掛接點會解析成未附加指定之裝置物件的磁片區。</span><span class="sxs-lookup"><span data-stu-id="7ca71-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**錯誤 \_ 不正確 \_ 裝置 \_ 物件 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="7ca71-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-503">650 (0x28A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-504">裝置物件參數不是有效的裝置物件，或未附加至檔案名所指定的磁片區。</span><span class="sxs-lookup"><span data-stu-id="7ca71-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**\_發生錯誤 MCA \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-506">651 (0x28B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-507">發生電腦檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="7ca71-508">請檢查系統事件記錄檔以取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7ca71-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**錯誤 \_ 驅動程式 \_ 資料庫 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-510">652 (0x28C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-511">\[ \] 處理驅動程式資料庫時發生錯誤 %2。</span><span class="sxs-lookup"><span data-stu-id="7ca71-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**錯誤 \_ 系統 \_ HIVE \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="7ca71-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-513">653 (0x28D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-514">系統 hive 大小超過其限制。</span><span class="sxs-lookup"><span data-stu-id="7ca71-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**錯誤 \_ 驅動程式在 \_ \_ 卸載前失敗 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-516">654 (0x28E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-517">無法載入驅動程式，因為先前版本的驅動程式仍在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="7ca71-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**錯誤 \_ VOLSNAP \_ 準備 \_ 休眠**</span><span class="sxs-lookup"><span data-stu-id="7ca71-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-519">655 (0x28F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-520">{磁碟區陰影複製服務}請稍候，磁碟區陰影複製服務準備磁片區% hs 以進行休眠。</span><span class="sxs-lookup"><span data-stu-id="7ca71-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**錯誤 \_ 休眠 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-522">656 (0x290) </span><span class="sxs-lookup"><span data-stu-id="7ca71-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-523">系統無法休眠 (錯誤碼為% hs) 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="7ca71-524">休眠將會停用，直到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**錯誤 \_ PWD \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="7ca71-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-526">657 (0x291) </span><span class="sxs-lookup"><span data-stu-id="7ca71-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-527">提供的密碼太長，無法符合您的使用者帳戶原則。</span><span class="sxs-lookup"><span data-stu-id="7ca71-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="7ca71-528">請選擇較短的密碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**錯誤 \_ 檔 \_ 系統 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="7ca71-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-530">665 (0x299) </span><span class="sxs-lookup"><span data-stu-id="7ca71-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-531">無法完成要求的作業，因為檔案系統有限制。</span><span class="sxs-lookup"><span data-stu-id="7ca71-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**錯誤判斷提示 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-533">668 (0x29C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-534">發生判斷提示失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**錯誤 \_ ACPI \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-536">669 (0x29D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-537">ACPI 子系統發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**錯誤 \_ WOW 判斷提示 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-539">670 (0x29E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-540">WOW 判斷提示錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**錯誤 \_ PNP 錯誤的 \_ \_ MP \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="7ca71-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-542">671 (0x29F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-543">系統 BIOS MP 資料表中遺漏裝置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="7ca71-544">將不會使用此裝置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-544">This device will not be used.</span></span> <span data-ttu-id="7ca71-545">請洽詢您的系統廠商以取得系統 BIOS 更新。</span><span class="sxs-lookup"><span data-stu-id="7ca71-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**錯誤 \_ PNP \_ 轉譯 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-547">672 (0x2A0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-548">翻譯工具無法轉譯資源。</span><span class="sxs-lookup"><span data-stu-id="7ca71-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**錯誤 \_ PNP \_ IRQ \_ 轉譯 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-550">673 (0x2A1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-551">IRQ 翻譯工具無法轉譯資源。</span><span class="sxs-lookup"><span data-stu-id="7ca71-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**錯誤 \_ PNP \_ 無效 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="7ca71-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-553">674 (0x2A2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-554">驅動程式 %2 為子裝置 (% 3) 傳回了不正確識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**錯誤 \_ 喚醒 \_ 系統 \_ 偵錯工具**</span><span class="sxs-lookup"><span data-stu-id="7ca71-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-556">675 (0x2A3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-557">{內核偵錯工具喚醒} 系統偵錯工具是由插斷喚醒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**錯誤 \_ 控制碼 \_ 已關閉**</span><span class="sxs-lookup"><span data-stu-id="7ca71-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-559">676 (0x2A4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-560">{控制碼已關閉}物件的控制碼已自動關閉，因為要求的作業結果。</span><span class="sxs-lookup"><span data-stu-id="7ca71-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**錯誤 \_ 無關的 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7ca71-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-562">677 (0x2A5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-563">{太多資訊}指定的存取控制清單 (ACL) 包含的資訊比預期的還要多。</span><span class="sxs-lookup"><span data-stu-id="7ca71-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**\_RXACT \_ 需要認可 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-565">678 (0x2A6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-566">這個警告層級狀態表示登錄子樹已經有交易狀態，但先前已中止交易認可。</span><span class="sxs-lookup"><span data-stu-id="7ca71-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="7ca71-567">認可尚未完成，但尚未回復 (因此，如果需要) ，仍可進行認可。</span><span class="sxs-lookup"><span data-stu-id="7ca71-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**錯誤 \_ 媒體 \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="7ca71-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-569">679 (0x2A7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-570">{媒體已變更}媒體可能已變更。</span><span class="sxs-lookup"><span data-stu-id="7ca71-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**已 \_ 進行錯誤 GUID \_ 替代 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-572">680 (0x2A8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-573">{GUID 替代}在將全域識別碼 (GUID) 轉換為 Windows 安全識別碼 (SID) 時，找不到系統管理員定義的 GUID 前置詞。</span><span class="sxs-lookup"><span data-stu-id="7ca71-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="7ca71-574">使用替代首碼，這將不會危害系統安全性。</span><span class="sxs-lookup"><span data-stu-id="7ca71-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="7ca71-575">不過，這可能會提供比預期更嚴格的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ca71-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**\_ \_ 符號上的錯誤已停止 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-577">681 (0x2A9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-578">建立作業會在到達符號連結後停止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**錯誤 \_ LONGJUMP**</span><span class="sxs-lookup"><span data-stu-id="7ca71-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-580">682 (0x2AA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-581">已執行長時間跳躍。</span><span class="sxs-lookup"><span data-stu-id="7ca71-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**\_PLUGPLAY \_ 拒絕的查詢 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-583">683 (0x2AB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-584">隨插即用查詢作業不成功。</span><span class="sxs-lookup"><span data-stu-id="7ca71-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**錯誤 \_ 回溯 \_ 合併**</span><span class="sxs-lookup"><span data-stu-id="7ca71-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-586">684 (0x2AC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-587">已執行框架合併。</span><span class="sxs-lookup"><span data-stu-id="7ca71-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_復原登錄 \_ HIVE \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-589">685 (0x2AD) </span><span class="sxs-lookup"><span data-stu-id="7ca71-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-590">{登錄 Hive 已復原}登錄 hive (檔案) ：% hs 已損毀，且已復原。</span><span class="sxs-lookup"><span data-stu-id="7ca71-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="7ca71-591">某些資料可能已遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**錯誤 \_ DLL \_ 可能 \_ 不 \_ 安全**</span><span class="sxs-lookup"><span data-stu-id="7ca71-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-593">686 (0x2AE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-594">應用程式正在嘗試從模組% hs 執行可執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="7ca71-595">這可能不安全。</span><span class="sxs-lookup"><span data-stu-id="7ca71-595">This may be insecure.</span></span> <span data-ttu-id="7ca71-596">有替代方案% hs 可供使用。</span><span class="sxs-lookup"><span data-stu-id="7ca71-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="7ca71-597">應用程式是否應該使用安全模組% hs？</span><span class="sxs-lookup"><span data-stu-id="7ca71-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**錯誤 \_ DLL \_ 可能 \_ \_ 不相容**</span><span class="sxs-lookup"><span data-stu-id="7ca71-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-599">687 (0x2AF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-600">應用程式正在從模組% hs 載入可執行檔程式碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="7ca71-601">這是安全的，但可能與舊版的作業系統不相容。</span><span class="sxs-lookup"><span data-stu-id="7ca71-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="7ca71-602">有替代方案% hs 可供使用。</span><span class="sxs-lookup"><span data-stu-id="7ca71-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="7ca71-603">應用程式是否應該使用安全模組% hs？</span><span class="sxs-lookup"><span data-stu-id="7ca71-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**錯誤 \_ DBG \_ 例外狀況 \_ 未 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="7ca71-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-605">688 (0x2B0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-606">偵錯工具未處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**錯誤 \_ DBG \_ 于 \_ 稍後回復**</span><span class="sxs-lookup"><span data-stu-id="7ca71-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-608">689 (0x2B1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-609">偵錯工具稍後會回復。</span><span class="sxs-lookup"><span data-stu-id="7ca71-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**錯誤 \_ DBG \_ 無法 \_ \_ 提供 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="7ca71-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-611">690 (0x2B2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-612">偵錯工具無法提供控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**錯誤 \_ DBG \_ 終止 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="7ca71-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-614">691 (0x2B3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-615">偵錯工具終止的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**錯誤 \_ DBG \_ 終止 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="7ca71-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-617">692 (0x2B4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-618">偵錯工具已終止進程。</span><span class="sxs-lookup"><span data-stu-id="7ca71-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**錯誤 \_ DBG \_ 控制項 \_ C**</span><span class="sxs-lookup"><span data-stu-id="7ca71-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-620">693 (0x2B5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-621">偵錯工具得到控制項 C。</span><span class="sxs-lookup"><span data-stu-id="7ca71-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**錯誤 \_ DBG \_ PRINTEXCEPTION \_ C**</span><span class="sxs-lookup"><span data-stu-id="7ca71-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-623">694 (0x2B6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-624">控制項 C 上的偵錯工具列印例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**錯誤 \_ DBG \_ RIPEXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="7ca71-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-626">695 (0x2B7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-627">偵錯工具收到 RIP 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**錯誤 \_ DBG \_ 控制 \_ 中斷**</span><span class="sxs-lookup"><span data-stu-id="7ca71-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-629">696 (0x2B8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-630">偵錯工具收到控制中斷。</span><span class="sxs-lookup"><span data-stu-id="7ca71-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**錯誤 \_ DBG \_ 命令 \_ 例外狀況**</span><span class="sxs-lookup"><span data-stu-id="7ca71-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-632">697 (0x2B9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-633">偵錯工具命令通訊例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**錯誤 \_ 物件 \_ 名稱 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="7ca71-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-635">698 (0x2BA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-636">{Object Exists}嘗試建立物件，而物件名稱已存在。</span><span class="sxs-lookup"><span data-stu-id="7ca71-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**錯誤 \_ 執行緒 \_ 已 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="7ca71-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-638">699 (0x2BB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-639">{執行緒已暫止}執行緒暫止時發生執行緒終止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="7ca71-640">已繼續執行緒，並繼續進行終止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**錯誤 \_ 影像 \_ 不 \_ 在 \_ 基底**</span><span class="sxs-lookup"><span data-stu-id="7ca71-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-642">700 (0x2BC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-643">{重定位映射}影像檔案中所指定的位址無法對應影像檔案。</span><span class="sxs-lookup"><span data-stu-id="7ca71-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="7ca71-644">您必須對此映射執行本機修正。</span><span class="sxs-lookup"><span data-stu-id="7ca71-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**\_RXACT \_ 建立的狀態 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-646">701 (0x2BD) </span><span class="sxs-lookup"><span data-stu-id="7ca71-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-647">此資訊層級狀態表示指定的登錄子樹交易狀態尚未存在且必須建立。</span><span class="sxs-lookup"><span data-stu-id="7ca71-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**錯誤 \_ 區段 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="7ca71-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-649">702 (0x2BE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-650">{區段載入} (VDM 的虛擬 DOS 機器) 正在載入、卸載或移動 MS-DOS 或 Win16 程式區段映射。</span><span class="sxs-lookup"><span data-stu-id="7ca71-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="7ca71-651">引發例外狀況，讓偵錯工具可以載入、卸載或追蹤這些16位區段內的符號和中斷點。</span><span class="sxs-lookup"><span data-stu-id="7ca71-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**錯誤 \_ 的 \_ 當前 \_ 目錄錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-653">703 (0x2BF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-654">{不正確目前的目錄}進程無法切換至啟動的目前的目錄% hs。</span><span class="sxs-lookup"><span data-stu-id="7ca71-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="7ca71-655">選取 [確定] 將目前的目錄設為% hs，或選取 [取消] 以結束。</span><span class="sxs-lookup"><span data-stu-id="7ca71-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**\_備份的錯誤 FT \_ 讀取 \_ 修復 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-657">704 (0x2C0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-658">{多餘讀取}為了滿足讀取要求，NT 容錯檔案系統成功從重複的複本讀取要求的資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="7ca71-659">因為檔案系統在容錯磁片區的成員上發生失敗，但無法重新指派裝置的失敗區域，所以已完成此操作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**錯誤 \_ FT \_ 寫入 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="7ca71-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-661">705 (0x2C1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-662">{多餘寫入}為了滿足寫入要求，NT 容錯檔案系統已成功寫入一份重複的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ca71-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="7ca71-663">因為檔案系統在容錯磁片區的成員上發生失敗，但無法重新指派裝置的失敗區域，所以已完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="7ca71-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**錯誤 \_ 映射 \_ 電腦 \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="7ca71-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-665">706 (0x2C2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-666">{電腦類型不符}影像檔案% hs 有效，但適用于目前電腦以外的電腦類型。</span><span class="sxs-lookup"><span data-stu-id="7ca71-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="7ca71-667">選取 [確定] 以繼續，或選取 [取消] 以使 DLL 載入失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**錯誤 \_ 接收 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="7ca71-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-669">707 (0x2C3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-670">{已接收部分資料}網路傳輸會將部分資料傳回給其用戶端。</span><span class="sxs-lookup"><span data-stu-id="7ca71-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="7ca71-671">其餘的資料將會在稍後傳送。</span><span class="sxs-lookup"><span data-stu-id="7ca71-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**\_收到 \_ 快速錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-673">708 (0x2C4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-674">{已收到快速資料}網路傳輸會將資料傳回給用戶端，而該用戶端是由遠端系統標示為已加速。</span><span class="sxs-lookup"><span data-stu-id="7ca71-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**錯誤 \_ 接收 \_ 部分 \_ 加急**</span><span class="sxs-lookup"><span data-stu-id="7ca71-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-676">709 (0x2C5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-677">{已接收部分快速資料}網路傳輸會將部分資料傳回給其用戶端，而且此資料會被遠端系統標示為已加速。</span><span class="sxs-lookup"><span data-stu-id="7ca71-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="7ca71-678">其餘的資料將會在稍後傳送。</span><span class="sxs-lookup"><span data-stu-id="7ca71-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**錯誤 \_ 事件已 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="7ca71-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-680">710 (0x2C6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-681">{TDI 事件已完成}TDI 表示已順利完成。</span><span class="sxs-lookup"><span data-stu-id="7ca71-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**錯誤 \_ 事件 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="7ca71-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-683">711 (0x2C7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-684">{TDI 事件暫止}TDI 表示已進入擱置狀態。</span><span class="sxs-lookup"><span data-stu-id="7ca71-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**\_檢查 \_ 檔 \_ 系統時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-686">712 (0x2C8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-687">正在檢查% wZ 上的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="7ca71-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**錯誤 \_ 嚴重 \_ 應用程式結束 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-689">713 (0x2C9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-690">{嚴重的應用程式結束}% hs。</span><span class="sxs-lookup"><span data-stu-id="7ca71-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_預先定義的 \_ 控制碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-692">714 (0x2CA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-693">指定的登錄機碼由預先定義的控制碼參考。</span><span class="sxs-lookup"><span data-stu-id="7ca71-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**錯誤 \_ 已 \_ 解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="7ca71-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-695">715 (0x2CB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-696">{已解除鎖定頁面}鎖定頁面的頁面保護已變更為 [無存取]，而且頁面已從記憶體和進程解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="7ca71-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**錯誤 \_ 服務 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="7ca71-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-698">716 (0x2CC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-699">% hs</span><span class="sxs-lookup"><span data-stu-id="7ca71-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**錯誤 \_ 已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="7ca71-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-701">717 (0x2CD) </span><span class="sxs-lookup"><span data-stu-id="7ca71-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-702">{頁面鎖定}其中一個要鎖定的頁面已經鎖定。</span><span class="sxs-lookup"><span data-stu-id="7ca71-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**錯誤 \_ 記錄檔 \_ 硬性 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-704">718 (0x2CE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-705">應用程式快顯視窗： %1： %2</span><span class="sxs-lookup"><span data-stu-id="7ca71-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**錯誤 \_ 已經是 \_ WIN32**</span><span class="sxs-lookup"><span data-stu-id="7ca71-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-707">719 (0x2CF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-708">錯誤 \_ 已經是 \_ WIN32</span><span class="sxs-lookup"><span data-stu-id="7ca71-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**錯誤 \_ 映射 \_ 電腦 \_ 類型 \_ 不相符 \_ EXE**</span><span class="sxs-lookup"><span data-stu-id="7ca71-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-710">720 (0x2D0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-711">{電腦類型不符}影像檔案% hs 有效，但適用于目前電腦以外的電腦類型。</span><span class="sxs-lookup"><span data-stu-id="7ca71-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**\_未 \_ 執行任何 YIELD \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-713">721 (0x2D1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-714">執行了 yield 執行，而且沒有任何執行緒可以執行。</span><span class="sxs-lookup"><span data-stu-id="7ca71-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**已 \_ 忽略錯誤計時器 \_ 繼續 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-716">722 (0x2D2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-717">已忽略計時器 API 的可繼續旗標。</span><span class="sxs-lookup"><span data-stu-id="7ca71-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**錯誤 \_ 仲裁 \_ 未處理**</span><span class="sxs-lookup"><span data-stu-id="7ca71-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-719">723 (0x2D3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-720">仲裁者已將這些資源的仲裁延後到其父系。</span><span class="sxs-lookup"><span data-stu-id="7ca71-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**\_ \_ 不支援錯誤 \_ CARDBUS**</span><span class="sxs-lookup"><span data-stu-id="7ca71-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-722">724 (0x2D4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-723">因為 "% hs" 發生設定錯誤，所以無法啟動插入的 CardBus 裝置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**錯誤 \_ MP \_ 處理器 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="7ca71-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-725">725 (0x2D5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-726">此多處理器系統中的 Cpu 不是全部相同的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="7ca71-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="7ca71-727">若要使用所有處理器，作業系統會將其本身限制為系統中最少可用處理器的功能。</span><span class="sxs-lookup"><span data-stu-id="7ca71-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="7ca71-728">如果此系統發生問題，請洽詢 CPU 製造商以查看是否支援這種處理器組合。</span><span class="sxs-lookup"><span data-stu-id="7ca71-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**錯誤 \_ 休眠**</span><span class="sxs-lookup"><span data-stu-id="7ca71-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-730">726 (0x2D6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-731">系統已進入休眠狀態。</span><span class="sxs-lookup"><span data-stu-id="7ca71-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**錯誤 \_ 繼續 \_ 休眠**</span><span class="sxs-lookup"><span data-stu-id="7ca71-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-733">727 (0x2D7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-734">系統已從休眠狀態恢復。</span><span class="sxs-lookup"><span data-stu-id="7ca71-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**錯誤的 \_ 固件 \_ 已更新**</span><span class="sxs-lookup"><span data-stu-id="7ca71-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-736">728 (0x2D8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-737">Windows 偵測到系統固件 (BIOS) 更新了之前的 \[ 固件日期 = %2，目前的固件日期 %3 \] 。</span><span class="sxs-lookup"><span data-stu-id="7ca71-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**\_ \_ 洩漏 \_ 鎖定頁面的 \_ 錯誤驅動程式**</span><span class="sxs-lookup"><span data-stu-id="7ca71-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-739">729 (0x2D9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-740">設備磁碟機正在洩漏鎖定的 i/o 頁面，導致系統效能降低。</span><span class="sxs-lookup"><span data-stu-id="7ca71-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="7ca71-741">系統已自動啟用追蹤程式碼，以便嘗試並攔截問題。</span><span class="sxs-lookup"><span data-stu-id="7ca71-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**錯誤 \_ 喚醒 \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="7ca71-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-743">730 (0x2DA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-744">系統有喚醒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**錯誤 \_ 等候 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7ca71-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-746">731 (0x2DB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-747">錯誤 \_ 等候 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7ca71-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**錯誤 \_ 等候 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7ca71-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-749">732 (0x2DC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-750">錯誤 \_ 等候 \_ 2</span><span class="sxs-lookup"><span data-stu-id="7ca71-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**錯誤 \_ 等候 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="7ca71-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-752">733 (0x2DD) </span><span class="sxs-lookup"><span data-stu-id="7ca71-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-753">錯誤 \_ 等候 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7ca71-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**錯誤 \_ 等候 \_ 63**</span><span class="sxs-lookup"><span data-stu-id="7ca71-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-755">734 (0x2DE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-756">錯誤 \_ 等候 \_ 63</span><span class="sxs-lookup"><span data-stu-id="7ca71-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**錯誤 \_ 放棄 \_ 等候 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="7ca71-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-758">735 (0x2DF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-759">錯誤 \_ 放棄 \_ 等候 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ca71-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**錯誤 \_ 放棄 \_ 等候 \_ 63**</span><span class="sxs-lookup"><span data-stu-id="7ca71-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-761">736 (0x2E0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-762">錯誤 \_ 放棄 \_ 等候 \_ 63</span><span class="sxs-lookup"><span data-stu-id="7ca71-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**\_使用者 \_ APC 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-764">737 (0x2E1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-765">\_使用者 \_ APC 錯誤</span><span class="sxs-lookup"><span data-stu-id="7ca71-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**錯誤 \_ 核心 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-767">738 (0x2E2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-768">錯誤 \_ 核心 \_</span><span class="sxs-lookup"><span data-stu-id="7ca71-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**\_警示錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-770">739 (0x2E3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-771">\_警示錯誤</span><span class="sxs-lookup"><span data-stu-id="7ca71-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_需要提高許可權 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-773">740 (0x2E4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-774">要求的作業需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="7ca71-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**錯誤重新 \_ 分析**</span><span class="sxs-lookup"><span data-stu-id="7ca71-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-776">741 (0x2E5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-777">因為檔案的名稱會產生符號連結，所以物件管理員應該執行重新剖析。</span><span class="sxs-lookup"><span data-stu-id="7ca71-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**錯誤 \_ OPLOCK \_ 中斷 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="7ca71-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-779">742 (0x2E6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-780">當 oplock 中斷正在進行時，開啟/建立作業已完成。</span><span class="sxs-lookup"><span data-stu-id="7ca71-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**裝載的錯誤 \_ 磁片區 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-782">743 (0x2E7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-783">檔案系統已載入新的磁片區。</span><span class="sxs-lookup"><span data-stu-id="7ca71-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**\_RXACT \_ 認可的錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-785">744 (0x2E8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-786">此成功層級狀態表示登錄子樹已經有交易狀態，但先前已中止交易認可。</span><span class="sxs-lookup"><span data-stu-id="7ca71-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="7ca71-787">認可現在已完成。</span><span class="sxs-lookup"><span data-stu-id="7ca71-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_通知 \_ 清除時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-789">745 (0x2E9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-790">這表示通知變更要求已完成，因為關閉發出通知變更要求的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**\_主要 \_ 傳輸 \_ 連接 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-792">746 (0x2EA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-793">{主要傳輸上的連接失敗}嘗試連接到主要傳輸上的遠端伺服器% hs，但連線失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="7ca71-794">電腦可以在次要傳輸上連接。</span><span class="sxs-lookup"><span data-stu-id="7ca71-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="7ca71-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-796">747 (0x2EB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-797">分頁錯誤是轉換錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 要求 \_ 零**</span><span class="sxs-lookup"><span data-stu-id="7ca71-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-799">748 (0x2EC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-800">分頁錯誤是要求零錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**寫入時錯誤 \_ 分頁錯誤 \_ \_ 複製 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-802">749 (0x2ED) </span><span class="sxs-lookup"><span data-stu-id="7ca71-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-803">分頁錯誤是要求零錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 防護 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="7ca71-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-805">750 (0x2EE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-806">分頁錯誤是要求零錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**錯誤 \_ 分頁錯誤頁面 \_ \_ \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="7ca71-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-808">751 (0x2EF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-809">從次要儲存裝置讀取時，已滿足分頁錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**鎖定快取頁面時發生錯誤 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-811">752 (0x2F0) </span><span class="sxs-lookup"><span data-stu-id="7ca71-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-812">在作業期間鎖定快取頁面。</span><span class="sxs-lookup"><span data-stu-id="7ca71-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**錯誤損毀傾印 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-814">753 (0x2F1) </span><span class="sxs-lookup"><span data-stu-id="7ca71-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-815">分頁檔案中有損毀傾印。</span><span class="sxs-lookup"><span data-stu-id="7ca71-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**錯誤 \_ 緩衝區 \_ 全部為 \_ 零**</span><span class="sxs-lookup"><span data-stu-id="7ca71-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-817">754 (0x2F2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-818">指定的緩衝區包含所有零。</span><span class="sxs-lookup"><span data-stu-id="7ca71-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**錯誤重新 \_ 分析 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="7ca71-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-820">755 (0x2F3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-821">因為檔案的名稱會產生符號連結，所以物件管理員應該執行重新剖析。</span><span class="sxs-lookup"><span data-stu-id="7ca71-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**錯誤 \_ 資源 \_ 需求 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="7ca71-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-823">756 (0x2F4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-824">裝置已成功查詢-停止，且其資源需求已變更。</span><span class="sxs-lookup"><span data-stu-id="7ca71-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**錯誤 \_ 轉譯 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="7ca71-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-826">757 (0x2F5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-827">翻譯工具已將這些資源轉譯為全域空間，因此不應執行任何進一步的翻譯。</span><span class="sxs-lookup"><span data-stu-id="7ca71-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_沒有 \_ 終止的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-829">758 (0x2F6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-830">終止的進程沒有可終止的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7ca71-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**錯誤 \_ 處理常式 \_ 不 \_ 在 \_ 工作中**</span><span class="sxs-lookup"><span data-stu-id="7ca71-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-832">759 (0x2F7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-833">指定的進程不是作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="7ca71-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_ \_ 作業中的錯誤處理常式 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-835">760 (0x2F8) </span><span class="sxs-lookup"><span data-stu-id="7ca71-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-836">指定的進程是作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="7ca71-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**錯誤 \_ VOLSNAP \_ 休眠 \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="7ca71-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-838">761 (0x2F9) </span><span class="sxs-lookup"><span data-stu-id="7ca71-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-839">{磁碟區陰影複製服務}系統現在已準備好休眠。</span><span class="sxs-lookup"><span data-stu-id="7ca71-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**錯誤 \_ FSFILTER \_ OP \_ 已 \_ 順利完成**</span><span class="sxs-lookup"><span data-stu-id="7ca71-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-841">762 (0x2FA) </span><span class="sxs-lookup"><span data-stu-id="7ca71-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-842">檔案系統或檔案系統篩選器驅動程式已順利完成 FsFilter 操作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**\_ \_ \_ 已連線的錯誤中斷向量 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-844">763 (0x2FB) </span><span class="sxs-lookup"><span data-stu-id="7ca71-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-845">指定的中斷向量已連接。</span><span class="sxs-lookup"><span data-stu-id="7ca71-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**錯誤 \_ 中斷 \_ 仍 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="7ca71-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-847">764 (0x2FC) </span><span class="sxs-lookup"><span data-stu-id="7ca71-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-848">指定的中斷向量仍在連線。</span><span class="sxs-lookup"><span data-stu-id="7ca71-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**\_等候 \_ \_ OPLOCK 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-850">765 (0x2FD) </span><span class="sxs-lookup"><span data-stu-id="7ca71-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-851">作業已封鎖等候 oplock。</span><span class="sxs-lookup"><span data-stu-id="7ca71-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**\_處理錯誤 DBG \_ 例外 \_ 狀況**</span><span class="sxs-lookup"><span data-stu-id="7ca71-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-853">766 (0x2FE) </span><span class="sxs-lookup"><span data-stu-id="7ca71-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-854">偵錯工具處理的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ca71-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**錯誤 \_ DBG \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="7ca71-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-856">767 (0x2FF) </span><span class="sxs-lookup"><span data-stu-id="7ca71-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-857">偵錯工具繼續。</span><span class="sxs-lookup"><span data-stu-id="7ca71-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**錯誤 \_ 回呼 \_ POP \_ 堆疊**</span><span class="sxs-lookup"><span data-stu-id="7ca71-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-859">768 (0x300) </span><span class="sxs-lookup"><span data-stu-id="7ca71-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-860">使用者模式回呼中發生例外狀況，應移除核心回呼框架。</span><span class="sxs-lookup"><span data-stu-id="7ca71-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_ \_ 停用錯誤壓縮**</span><span class="sxs-lookup"><span data-stu-id="7ca71-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-862">769 (0x301) </span><span class="sxs-lookup"><span data-stu-id="7ca71-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-863">此磁片區的壓縮已停用。</span><span class="sxs-lookup"><span data-stu-id="7ca71-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**錯誤 \_ CANTFETCHBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="7ca71-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-865">770 (0x302) </span><span class="sxs-lookup"><span data-stu-id="7ca71-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-866">資料提供者無法透過結果集向後提取。</span><span class="sxs-lookup"><span data-stu-id="7ca71-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**錯誤 \_ CANTSCROLLBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="7ca71-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-868">771 (0x303) </span><span class="sxs-lookup"><span data-stu-id="7ca71-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-869">資料提供者無法在結果集中向後滾動。</span><span class="sxs-lookup"><span data-stu-id="7ca71-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**錯誤 \_ ROWSNOTRELEASED**</span><span class="sxs-lookup"><span data-stu-id="7ca71-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-871">772 (0x304) </span><span class="sxs-lookup"><span data-stu-id="7ca71-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-872">資料提供者需要先釋出先前提取的資料，然後再要求更多資料。</span><span class="sxs-lookup"><span data-stu-id="7ca71-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**錯誤 \_ \_ 存取子 \_ 旗標錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-874">773 (0x305) </span><span class="sxs-lookup"><span data-stu-id="7ca71-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-875">資料提供者無法解讀存取子中的資料行系結所設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="7ca71-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_遇到錯誤錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-877">774 (0x306) </span><span class="sxs-lookup"><span data-stu-id="7ca71-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-878">處理要求時發生一或多個錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**錯誤 \_ 無法 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="7ca71-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-880">775 (0x307) </span><span class="sxs-lookup"><span data-stu-id="7ca71-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-881">執行不能執行要求。</span><span class="sxs-lookup"><span data-stu-id="7ca71-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**錯誤 \_ 要求 \_ \_ \_ 順序錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-883">776 (0x308) </span><span class="sxs-lookup"><span data-stu-id="7ca71-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-884">元件的用戶端要求的作業在元件實例的狀態中是不正確。</span><span class="sxs-lookup"><span data-stu-id="7ca71-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**錯誤 \_ 版本 \_ 剖析 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-886">777 (0x309) </span><span class="sxs-lookup"><span data-stu-id="7ca71-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-887">無法剖析版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7ca71-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**錯誤 \_ BADSTARTPOSITION**</span><span class="sxs-lookup"><span data-stu-id="7ca71-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-889">778 (0x30A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-890">反覆運算器的開始位置無效。</span><span class="sxs-lookup"><span data-stu-id="7ca71-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**錯誤 \_ 記憶體 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="7ca71-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-892">779 (0x30B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-893">硬體回報了無法修正的記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**\_ \_ 停用磁片修復錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-895">780 (0x30C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-896">嘗試的作業必須啟用自我修復。</span><span class="sxs-lookup"><span data-stu-id="7ca71-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**\_資源不足 \_ \_ ，無法用於 \_ 指定的 \_ 共用 \_ 區段 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7ca71-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-898">781 (0x30D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-899">在配置會話記憶體時，桌面堆積發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="7ca71-900">系統事件記錄檔中有更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ca71-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**錯誤 \_ 系統 \_ >POWERSTATE \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="7ca71-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-902">782 (0x30E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-903">系統電源狀態是從 %2 轉換到 %3。</span><span class="sxs-lookup"><span data-stu-id="7ca71-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR \_ SYSTEM \_ >POWERSTATE \_ 複雜 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="7ca71-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-905">783 (0x30F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-906">系統電源狀態是從 %2 轉換到 %3，但可以輸入 %4。</span><span class="sxs-lookup"><span data-stu-id="7ca71-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**錯誤 \_ MCA \_ 例外狀況**</span><span class="sxs-lookup"><span data-stu-id="7ca71-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-908">784 (0x310) </span><span class="sxs-lookup"><span data-stu-id="7ca71-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-909">因為 MCA，所以執行緒會因為 mca 例外狀況而分派。</span><span class="sxs-lookup"><span data-stu-id="7ca71-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_ \_ \_ 依原則的存取審核錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-911">785 (0x311) </span><span class="sxs-lookup"><span data-stu-id="7ca71-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-912">原則規則 %2 會監視 %1 的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ca71-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**錯誤 \_ 存取 \_ 已停用 \_ \_ \_ \_ 原則的 \_ 不安全 UI**</span><span class="sxs-lookup"><span data-stu-id="7ca71-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-914">786 (0x312) </span><span class="sxs-lookup"><span data-stu-id="7ca71-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-915">原則規則 %2 的系統管理員已限制存取 %1。</span><span class="sxs-lookup"><span data-stu-id="7ca71-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**錯誤 \_ 放棄 \_ HIBERFILE**</span><span class="sxs-lookup"><span data-stu-id="7ca71-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-917">787 (0x313) </span><span class="sxs-lookup"><span data-stu-id="7ca71-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-918">有效的休眠檔已失效，應予以放棄。</span><span class="sxs-lookup"><span data-stu-id="7ca71-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 網路 \_ 連線中斷時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-920">788 (0x314) </span><span class="sxs-lookup"><span data-stu-id="7ca71-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-921">{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="7ca71-922">發生此錯誤的原因可能是網路連線問題。</span><span class="sxs-lookup"><span data-stu-id="7ca71-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="7ca71-923">請嘗試將此檔案儲存在其他位置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 網路 \_ 伺服器 \_ 錯誤遺失錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-925">789 (0x315) </span><span class="sxs-lookup"><span data-stu-id="7ca71-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-926">{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="7ca71-927">檔案所在的伺服器傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="7ca71-928">請嘗試將此檔案儲存在其他位置。</span><span class="sxs-lookup"><span data-stu-id="7ca71-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 本機 \_ 磁片 \_ 錯誤遺失**</span><span class="sxs-lookup"><span data-stu-id="7ca71-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-930">790 (0x316) </span><span class="sxs-lookup"><span data-stu-id="7ca71-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-931">{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。</span><span class="sxs-lookup"><span data-stu-id="7ca71-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="7ca71-932">如果裝置已移除或媒體受到寫入保護，可能會導致此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**錯誤 \_ 的 \_ MCFG \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="7ca71-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-934">791 (0x317) </span><span class="sxs-lookup"><span data-stu-id="7ca71-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-935">此裝置所需的資源與 MCFG 資料表發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7ca71-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**重新 \_ \_ 導向磁片修復 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-937">792 (0x318) </span><span class="sxs-lookup"><span data-stu-id="7ca71-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-938">磁片區修復在上線時無法執行。</span><span class="sxs-lookup"><span data-stu-id="7ca71-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="7ca71-939">請排程讓磁片區離線，讓它可以修復。</span><span class="sxs-lookup"><span data-stu-id="7ca71-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**錯誤 \_ 磁片 \_ 修復 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7ca71-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-941">793 (0x319) </span><span class="sxs-lookup"><span data-stu-id="7ca71-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-942">磁片區修復失敗。</span><span class="sxs-lookup"><span data-stu-id="7ca71-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**錯誤損毀 \_ \_ 記錄檔 \_ OVERFULL**</span><span class="sxs-lookup"><span data-stu-id="7ca71-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-944">794 (0x31A) </span><span class="sxs-lookup"><span data-stu-id="7ca71-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-945">其中一個磁片區損毀記錄已滿。</span><span class="sxs-lookup"><span data-stu-id="7ca71-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="7ca71-946">可能偵測到的進一步損毀不會記錄下來。</span><span class="sxs-lookup"><span data-stu-id="7ca71-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**錯誤 \_ \_ \_ 損毀記錄損毀**</span><span class="sxs-lookup"><span data-stu-id="7ca71-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-948">795 (0x31B) </span><span class="sxs-lookup"><span data-stu-id="7ca71-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-949">其中一個磁片區損毀記錄在內部損毀，需要重新建立。</span><span class="sxs-lookup"><span data-stu-id="7ca71-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="7ca71-950">磁片區可能包含未偵測到的損毀，且必須進行掃描。</span><span class="sxs-lookup"><span data-stu-id="7ca71-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**錯誤損毀 \_ \_ 記錄檔 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="7ca71-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-952">796 (0x31C) </span><span class="sxs-lookup"><span data-stu-id="7ca71-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-953">其中一個磁片區損毀記錄無法用於操作。</span><span class="sxs-lookup"><span data-stu-id="7ca71-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**\_ \_ \_ 已刪除完整記錄 \_ 檔時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="7ca71-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-955">797 (0x31D) </span><span class="sxs-lookup"><span data-stu-id="7ca71-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-956">其中一個磁片區損毀記錄檔已刪除，但仍有損毀記錄。</span><span class="sxs-lookup"><span data-stu-id="7ca71-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="7ca71-957">磁片區包含偵測到的損毀，且必須進行掃描。</span><span class="sxs-lookup"><span data-stu-id="7ca71-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**已清除錯誤損毀 \_ \_ 記錄檔 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-959">798 (0x31E) </span><span class="sxs-lookup"><span data-stu-id="7ca71-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-960">Chkdsk 已清除其中一個磁片區損毀記錄，不再包含真正損毀的記錄。</span><span class="sxs-lookup"><span data-stu-id="7ca71-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**錯誤的 \_ 孤立 \_ 名稱已 \_ 用盡**</span><span class="sxs-lookup"><span data-stu-id="7ca71-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-962">799 (0x31F) </span><span class="sxs-lookup"><span data-stu-id="7ca71-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-963">磁片區上有孤立的檔案，但無法復原，因為無法在復原目錄中建立更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ca71-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="7ca71-964">檔案必須從修復目錄移動。</span><span class="sxs-lookup"><span data-stu-id="7ca71-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**錯誤 \_ OPLOCK \_ 切換 \_ 至 \_ 新的 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="7ca71-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-966">800 (0x320) </span><span class="sxs-lookup"><span data-stu-id="7ca71-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-967">與此控制碼相關聯的 oplock 現在與不同的控制碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="7ca71-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**錯誤 \_ 無法 \_ 授與 \_ 要求的 \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="7ca71-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-969">801 (0x321) </span><span class="sxs-lookup"><span data-stu-id="7ca71-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-970">無法授與所要求層級的 oplock。</span><span class="sxs-lookup"><span data-stu-id="7ca71-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="7ca71-971">較低層級的 oplock 可能可供使用。</span><span class="sxs-lookup"><span data-stu-id="7ca71-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**錯誤 \_ 無法 \_ 中斷 \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="7ca71-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-973">802 (0x322) </span><span class="sxs-lookup"><span data-stu-id="7ca71-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-974">作業未順利完成，因為它會導致 oplock 中斷。</span><span class="sxs-lookup"><span data-stu-id="7ca71-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="7ca71-975">呼叫端要求現有的 oplock 不會中斷。</span><span class="sxs-lookup"><span data-stu-id="7ca71-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**錯誤 \_ OPLOCK \_ 控制碼 \_ 已關閉**</span><span class="sxs-lookup"><span data-stu-id="7ca71-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-977">803 (0x323) </span><span class="sxs-lookup"><span data-stu-id="7ca71-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-978">與此 oplock 相關聯的控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="7ca71-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="7ca71-979">Oplock 現在已中斷。</span><span class="sxs-lookup"><span data-stu-id="7ca71-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**錯誤 \_ 無 \_ ACE \_ 條件**</span><span class="sxs-lookup"><span data-stu-id="7ca71-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-981">804 (0x324) </span><span class="sxs-lookup"><span data-stu-id="7ca71-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-982">指定的存取控制專案 (ACE) 不包含條件。</span><span class="sxs-lookup"><span data-stu-id="7ca71-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**錯誤 \_ 不正確 \_ ACE \_ 條件**</span><span class="sxs-lookup"><span data-stu-id="7ca71-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-984">805 (0x325) </span><span class="sxs-lookup"><span data-stu-id="7ca71-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-985">指定的存取控制專案 (ACE) 包含不正確條件。</span><span class="sxs-lookup"><span data-stu-id="7ca71-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**已 \_ 撤銷錯誤檔 \_ 控制碼 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-987">806 (0x326) </span><span class="sxs-lookup"><span data-stu-id="7ca71-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-988">已撤銷對指定檔案控制代碼的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ca71-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_ \_ \_ 不同 \_ 基底的錯誤影像**</span><span class="sxs-lookup"><span data-stu-id="7ca71-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-990">807 (0x327) </span><span class="sxs-lookup"><span data-stu-id="7ca71-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-991">影像檔案的對應位置與影像檔案中指定的位址不同，但仍會在映射上自動執行修正。</span><span class="sxs-lookup"><span data-stu-id="7ca71-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**\_ \_ 拒絕存取 EA 的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="7ca71-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-993">994 (0x3E2) </span><span class="sxs-lookup"><span data-stu-id="7ca71-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-994">拒絕存取擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="7ca71-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**錯誤作業已 \_ \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="7ca71-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-996">995 (0x3E3) </span><span class="sxs-lookup"><span data-stu-id="7ca71-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-997">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="7ca71-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**錯誤 \_ IO \_ 不完整**</span><span class="sxs-lookup"><span data-stu-id="7ca71-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-999">996 (0x3E4) </span><span class="sxs-lookup"><span data-stu-id="7ca71-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-1000">重迭的 i/o 事件未處於已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="7ca71-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**錯誤 \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="7ca71-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-1002">997 (0x3E5) </span><span class="sxs-lookup"><span data-stu-id="7ca71-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-1003">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="7ca71-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**錯誤 \_ NOACCESS**</span><span class="sxs-lookup"><span data-stu-id="7ca71-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-1005">998 (0x3E6) </span><span class="sxs-lookup"><span data-stu-id="7ca71-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-1006">存取記憶體位置無效。</span><span class="sxs-lookup"><span data-stu-id="7ca71-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ca71-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**錯誤 \_ SWAPERROR**</span><span class="sxs-lookup"><span data-stu-id="7ca71-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca71-1008">999 (0x3E7) </span><span class="sxs-lookup"><span data-stu-id="7ca71-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="7ca71-1009">執行 inpage 操作時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ca71-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="7ca71-1010">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ca71-1010">Requirements</span></span>



| <span data-ttu-id="7ca71-1011">需求</span><span class="sxs-lookup"><span data-stu-id="7ca71-1011">Requirement</span></span> | <span data-ttu-id="7ca71-1012">值</span><span class="sxs-lookup"><span data-stu-id="7ca71-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca71-1013">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ca71-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca71-1014">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ca71-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ca71-1015">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ca71-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca71-1016">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ca71-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ca71-1017">標頭</span><span class="sxs-lookup"><span data-stu-id="7ca71-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca71-1018"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca71-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca71-1019">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ca71-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca71-1020">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7ca71-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
