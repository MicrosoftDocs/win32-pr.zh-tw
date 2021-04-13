---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1000-1299，適用于開發人員。
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: '系統錯誤碼 (1000-1299)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510590"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="5f34a-103">系統錯誤碼 (1000-1299) </span><span class="sxs-lookup"><span data-stu-id="5f34a-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="5f34a-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="5f34a-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="5f34a-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="5f34a-106">下列清單描述錯誤1000到1299的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5f34a-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="5f34a-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="5f34a-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="5f34a-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="5f34a-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="5f34a-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**錯誤 \_ 堆疊 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="5f34a-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-110">1001 (0x3E9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-111">遞迴太深;堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="5f34a-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**錯誤 \_ 不正確 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="5f34a-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-113">1002 (0x3EA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-114">視窗無法對傳送的訊息採取動作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**錯誤 \_ \_ 無法 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="5f34a-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-116">1003 (0x3EB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-117">無法完成此函數。</span><span class="sxs-lookup"><span data-stu-id="5f34a-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**錯誤 \_ 不正確 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="5f34a-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-119">1004 (0x3EC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-120">不正確旗標。</span><span class="sxs-lookup"><span data-stu-id="5f34a-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**\_無法辨識的磁片區錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-122">1005 (0x3ED) </span><span class="sxs-lookup"><span data-stu-id="5f34a-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-123">磁片區未包含已辨識的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5f34a-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="5f34a-124">請確定已載入所有必要的檔案系統驅動程式，且磁片區未損毀。</span><span class="sxs-lookup"><span data-stu-id="5f34a-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**錯誤 \_ 檔案 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="5f34a-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-126">1006 (0x3EE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-127">檔案的磁片區已從外部改變，因此開啟的檔案已不再有效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**錯誤 \_ 全螢幕 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="5f34a-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-129">1007 (0x3EF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-130">要求的作業無法以全螢幕模式執行。</span><span class="sxs-lookup"><span data-stu-id="5f34a-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**錯誤 \_ 無 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="5f34a-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-132">1008 (0x3F0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-133">嘗試參考不存在的權杖。</span><span class="sxs-lookup"><span data-stu-id="5f34a-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**錯誤 \_ BADDB**</span><span class="sxs-lookup"><span data-stu-id="5f34a-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-135">1009 (0x3F1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-136">Configuration registry 資料庫已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f34a-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**錯誤 \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="5f34a-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-138">1010 (0x3F2) </span><span class="sxs-lookup"><span data-stu-id="5f34a-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-139">設定登錄機碼無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**錯誤 \_ CANTOPEN**</span><span class="sxs-lookup"><span data-stu-id="5f34a-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-141">1011 (0x3F3) </span><span class="sxs-lookup"><span data-stu-id="5f34a-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-142">無法開啟設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**錯誤 \_ CANTREAD**</span><span class="sxs-lookup"><span data-stu-id="5f34a-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-144">1012 (0x3F4) </span><span class="sxs-lookup"><span data-stu-id="5f34a-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-145">無法讀取設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**錯誤 \_ CANTWRITE**</span><span class="sxs-lookup"><span data-stu-id="5f34a-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-147">1013 (0x3F5) </span><span class="sxs-lookup"><span data-stu-id="5f34a-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-148">無法寫入設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**復原錯誤登錄 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-150">1014 (0x3F6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-151">您必須使用記錄檔或替代複本來復原登錄資料庫中的其中一個檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="5f34a-152">復原成功。</span><span class="sxs-lookup"><span data-stu-id="5f34a-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**錯誤登錄已損毀 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-154">1015 (0x3F7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-155">登錄已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f34a-155">The registry is corrupted.</span></span> <span data-ttu-id="5f34a-156">其中一個包含登錄資料的檔案的結構已損毀，或檔案的系統記憶體映射已損毀，或因為替代複製或記錄檔不存在或損毀，所以無法復原檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**登錄 \_ \_ IO \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-158">1016 (0x3F8) </span><span class="sxs-lookup"><span data-stu-id="5f34a-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-159">登錄 unrecoverably 所起始的 i/o 作業失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="5f34a-160">登錄無法讀取或寫出或清除其中一個檔案，其中包含系統的登錄映射。</span><span class="sxs-lookup"><span data-stu-id="5f34a-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**錯誤，不是登錄檔 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-162">1017 (0x3F9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-163">系統已嘗試將檔案載入或還原到登錄中，但指定的檔案不是登錄檔案格式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**\_ \_ 已刪除錯誤索引鍵**</span><span class="sxs-lookup"><span data-stu-id="5f34a-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-165">1018 (0x3FA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-166">在已標示為要刪除的登錄機碼上嘗試了不合法的操作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**錯誤 \_ 無 \_ 記錄檔 \_ 空間**</span><span class="sxs-lookup"><span data-stu-id="5f34a-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-168">1019 (0x3FB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-169">系統無法在登錄記錄檔中配置所需的空間。</span><span class="sxs-lookup"><span data-stu-id="5f34a-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**錯誤索引 \_ 鍵 \_ 具有 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="5f34a-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-171">1020 (0x3FC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-172">無法在已有子機碼或值的登錄機碼中建立符號連結。</span><span class="sxs-lookup"><span data-stu-id="5f34a-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**錯誤 \_ 子 \_ 必須 \_ 為 \_ VOLATILE**</span><span class="sxs-lookup"><span data-stu-id="5f34a-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-174">1021 (0x3FD) </span><span class="sxs-lookup"><span data-stu-id="5f34a-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-175">無法在 volatile 父機碼下建立穩定的子機碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**\_通知 \_ 列舉 \_ 目錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-177">1022 (0x3FE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-178">正在完成通知變更要求，且未在呼叫端的緩衝區中傳回信息。</span><span class="sxs-lookup"><span data-stu-id="5f34a-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="5f34a-179">呼叫端現在必須列舉檔案以找出變更。</span><span class="sxs-lookup"><span data-stu-id="5f34a-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**錯誤 \_ 相依的 \_ 服務執行 \_ 中**</span><span class="sxs-lookup"><span data-stu-id="5f34a-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-181">1051 (0x41B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-182">停止控制項已傳送至其他正在執行之服務所相依的服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**錯誤 \_ 不正確 \_ 服務 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="5f34a-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-184">1052 (0x41C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-185">要求的控制項對此服務無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**錯誤 \_ 服務 \_ 要求 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="5f34a-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-187">1053 (0x41D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-188">服務未即時回應啟動或控制要求。</span><span class="sxs-lookup"><span data-stu-id="5f34a-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**錯誤 \_ 服務 \_ 無 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="5f34a-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-190">1054 (0x41E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-191">無法為服務建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="5f34a-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**錯誤 \_ 服務 \_ 資料庫已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="5f34a-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-193">1055 (0x41F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-194">服務資料庫已鎖定。</span><span class="sxs-lookup"><span data-stu-id="5f34a-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**錯誤 \_ 服務 \_ 已在執行 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-196">1056 (0x420) </span><span class="sxs-lookup"><span data-stu-id="5f34a-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-197">服務的實例已在執行中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**錯誤 \_ 不正確 \_ 服務 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="5f34a-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-199">1057 (0x421) </span><span class="sxs-lookup"><span data-stu-id="5f34a-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-200">帳戶名稱無效或不存在，或密碼對指定的帳號名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**錯誤 \_ 服務 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="5f34a-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-202">1058 (0x422) </span><span class="sxs-lookup"><span data-stu-id="5f34a-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-203">無法啟動服務，原因可能是服務已停用，或服務沒有已啟用的裝置與其相關聯。</span><span class="sxs-lookup"><span data-stu-id="5f34a-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**錯誤 \_ 迴圈相依性 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-205">1059 (0x423) </span><span class="sxs-lookup"><span data-stu-id="5f34a-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-206">已指定迴圈服務相依性。</span><span class="sxs-lookup"><span data-stu-id="5f34a-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**錯誤 \_ 服務 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="5f34a-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-208">1060 (0x424) </span><span class="sxs-lookup"><span data-stu-id="5f34a-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-209">指定的服務不是以已安裝的服務形式存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**錯誤 \_ 服務 \_ 無法 \_ 接受 \_ CTRL**</span><span class="sxs-lookup"><span data-stu-id="5f34a-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-211">1061 (0x425) </span><span class="sxs-lookup"><span data-stu-id="5f34a-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-212">這次服務無法接受控制訊息。</span><span class="sxs-lookup"><span data-stu-id="5f34a-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**錯誤 \_ 服務 \_ 未 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="5f34a-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-214">1062 (0x426) </span><span class="sxs-lookup"><span data-stu-id="5f34a-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-215">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**錯誤 \_ 失敗的 \_ SERVICE \_ CONTROLLER \_ CONNECT**</span><span class="sxs-lookup"><span data-stu-id="5f34a-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-217">1063 (0x427) </span><span class="sxs-lookup"><span data-stu-id="5f34a-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-218">服務處理常式無法連接到服務控制器。</span><span class="sxs-lookup"><span data-stu-id="5f34a-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**服務發生錯誤 \_ 例外狀況 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-220">1064 (0x428) </span><span class="sxs-lookup"><span data-stu-id="5f34a-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-221">處理控制項要求時，在服務中發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5f34a-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**錯誤 \_ 資料庫 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="5f34a-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-223">1065 (0x429) </span><span class="sxs-lookup"><span data-stu-id="5f34a-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-224">指定的資料庫不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**錯誤 \_ 服務 \_ 特定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-226">1066 (0x42A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-227">服務傳回服務特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**錯誤 \_ 進程已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="5f34a-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-229">1067 (0x42B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-230">進程意外結束。</span><span class="sxs-lookup"><span data-stu-id="5f34a-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**錯誤 \_ 服務相依性 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-232">1068 (0x42C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-233">相依性服務或群組無法啟動。</span><span class="sxs-lookup"><span data-stu-id="5f34a-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**錯誤 \_ 服務 \_ 登入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-235">1069 (0x42D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-236">登入失敗，因此服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="5f34a-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**錯誤 \_ 服務 \_ 啟動停止 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="5f34a-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-238">1070 (0x42E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-239">啟動之後，服務會在啟動暫止狀態下無反應。</span><span class="sxs-lookup"><span data-stu-id="5f34a-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**錯誤 \_ 不正確 \_ 服務 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="5f34a-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-241">1071 (0x42F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-242">指定的服務資料庫鎖定無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_ \_ 標記 \_ 為刪除的錯誤服務 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-244">1072 (0x430) </span><span class="sxs-lookup"><span data-stu-id="5f34a-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-245">指定的服務已標示為要刪除。</span><span class="sxs-lookup"><span data-stu-id="5f34a-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**錯誤 \_ 服務 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="5f34a-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-247">1073 (0x431) </span><span class="sxs-lookup"><span data-stu-id="5f34a-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-248">指定的服務已經存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**錯誤 \_ 已在執行 \_ \_ LKG**</span><span class="sxs-lookup"><span data-stu-id="5f34a-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-250">1074 (0x432) </span><span class="sxs-lookup"><span data-stu-id="5f34a-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-251">系統目前是以最後一個已知良好的設定來執行。</span><span class="sxs-lookup"><span data-stu-id="5f34a-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**錯誤 \_ 服務相依性 \_ \_ 已刪除**</span><span class="sxs-lookup"><span data-stu-id="5f34a-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-253">1075 (0x433) </span><span class="sxs-lookup"><span data-stu-id="5f34a-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-254">相依性服務不存在或已標示為要刪除。</span><span class="sxs-lookup"><span data-stu-id="5f34a-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**\_ \_ 已接受錯誤 \_ 開機**</span><span class="sxs-lookup"><span data-stu-id="5f34a-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-256">1076 (0x434) </span><span class="sxs-lookup"><span data-stu-id="5f34a-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-257">目前的開機已被接受，可做為最後一個已知良好的控制集。</span><span class="sxs-lookup"><span data-stu-id="5f34a-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**錯誤 \_ 服務 \_ 從未 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="5f34a-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-259">1077 (0x435) </span><span class="sxs-lookup"><span data-stu-id="5f34a-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-260">自上次開機之後，不會嘗試啟動服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**\_ \_ 服務名稱重複 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-262">1078 (0x436) </span><span class="sxs-lookup"><span data-stu-id="5f34a-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-263">名稱已用來作為服務名稱或服務顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5f34a-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**錯誤 \_ 不同的 \_ 服務 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="5f34a-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-265">1079 (0x437) </span><span class="sxs-lookup"><span data-stu-id="5f34a-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-266">針對此服務指定的帳號不同于在相同進程中執行的其他服務所指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="5f34a-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**錯誤 \_ 無法 \_ 偵測 \_ 驅動程式 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-268">1080 (0x438) </span><span class="sxs-lookup"><span data-stu-id="5f34a-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-269">失敗動作只能針對 Win32 服務設定，而不能針對驅動程式進行設定。</span><span class="sxs-lookup"><span data-stu-id="5f34a-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**錯誤 \_ 無法 \_ 偵測 \_ 進程 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="5f34a-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-271">1081 (0x439) </span><span class="sxs-lookup"><span data-stu-id="5f34a-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-272">這項服務會在與服務控制管理員相同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="5f34a-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="5f34a-273">因此，如果此服務的進程非預期地終止，服務控制管理員就無法採取動作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**錯誤 \_ 的 \_ 修復 \_ 程式**</span><span class="sxs-lookup"><span data-stu-id="5f34a-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-275">1082 (0x43A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-276">尚未針對此服務設定任何修復程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**錯誤 \_ 服務 \_ 不 \_ 在 \_ EXE 中**</span><span class="sxs-lookup"><span data-stu-id="5f34a-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-278">1083 (0x43B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-279">這項服務設定為在其中執行的可執行程式，不會執行服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**錯誤 \_ 未 \_ 安全開機 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="5f34a-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-281">1084 (0x43C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-282">這項服務無法以安全模式啟動。</span><span class="sxs-lookup"><span data-stu-id="5f34a-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_ \_ 媒體的錯誤 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="5f34a-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-284">1100 (0x44C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-285">已達到磁帶的實體結尾。</span><span class="sxs-lookup"><span data-stu-id="5f34a-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**偵測到錯誤的標記 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-287">1101 (0x44D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-288">磁帶存取已達到標記。</span><span class="sxs-lookup"><span data-stu-id="5f34a-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**\_媒體開始 \_ 時發生 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-290">1102 (0x44E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-291">遇到磁帶或磁碟分割的開頭。</span><span class="sxs-lookup"><span data-stu-id="5f34a-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**偵測 \_ 到錯誤 SETMARK \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-293">1103 (0x44F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-294">磁帶存取已達一組檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="5f34a-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**\_未偵測 \_ 到任何資料時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-296">1104 (0x450) </span><span class="sxs-lookup"><span data-stu-id="5f34a-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-297">磁帶上沒有其他資料。</span><span class="sxs-lookup"><span data-stu-id="5f34a-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**錯誤 \_ 分割區 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-299">1105 (0x451) </span><span class="sxs-lookup"><span data-stu-id="5f34a-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-300">無法分割磁帶。</span><span class="sxs-lookup"><span data-stu-id="5f34a-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**錯誤 \_ 不正確 \_ 區塊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="5f34a-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-302">1106 (0x452) </span><span class="sxs-lookup"><span data-stu-id="5f34a-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-303">存取 multivolume 磁碟分割的新磁帶時，目前的區塊大小不正確。</span><span class="sxs-lookup"><span data-stu-id="5f34a-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**錯誤 \_ 裝置 \_ 未 \_ 分割**</span><span class="sxs-lookup"><span data-stu-id="5f34a-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-305">1107 (0x453) </span><span class="sxs-lookup"><span data-stu-id="5f34a-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-306">載入磁帶時，找不到磁帶磁碟分割資訊。</span><span class="sxs-lookup"><span data-stu-id="5f34a-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**\_無法 \_ \_ 鎖定媒體的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-308">1108 (0x454) </span><span class="sxs-lookup"><span data-stu-id="5f34a-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-309">無法鎖定媒體退出機制。</span><span class="sxs-lookup"><span data-stu-id="5f34a-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**\_無法卸載 \_ \_ 媒體的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-311">1109 (0x455) </span><span class="sxs-lookup"><span data-stu-id="5f34a-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-312">無法卸載媒體。</span><span class="sxs-lookup"><span data-stu-id="5f34a-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**錯誤 \_ 媒體 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="5f34a-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-314">1110 (0x456) </span><span class="sxs-lookup"><span data-stu-id="5f34a-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-315">磁片磁碟機中的媒體可能已變更。</span><span class="sxs-lookup"><span data-stu-id="5f34a-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**錯誤 \_ 匯流排 \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="5f34a-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-317">1111 (0x457) </span><span class="sxs-lookup"><span data-stu-id="5f34a-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-318">I/o 匯流排已重設。</span><span class="sxs-lookup"><span data-stu-id="5f34a-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**\_ \_ \_ 磁片磁碟機中沒有媒體的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-320">1112 (0x458) </span><span class="sxs-lookup"><span data-stu-id="5f34a-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-321">磁片磁碟機中沒有任何媒體。</span><span class="sxs-lookup"><span data-stu-id="5f34a-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**\_沒有 \_ UNICODE \_ 轉譯的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-323">1113 (0x459) </span><span class="sxs-lookup"><span data-stu-id="5f34a-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-324">目標多位元組字碼頁中不存在 Unicode 字元的對應。</span><span class="sxs-lookup"><span data-stu-id="5f34a-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**錯誤 \_ DLL \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-326">1114 (0x45A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-327">動態連結程式庫 (DLL) 初始化常式失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**錯誤 \_ 關閉 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="5f34a-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-329">1115 (0x45B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-330">系統關機正在進行中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**錯誤 \_ \_ ，無法 \_ \_ 進行關閉**</span><span class="sxs-lookup"><span data-stu-id="5f34a-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-332">1116 (0x45C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-333">無法中止系統關機，因為沒有正在進行的關機。</span><span class="sxs-lookup"><span data-stu-id="5f34a-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**錯誤 \_ IO \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="5f34a-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-335">1117 (0x45D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-336">因為 I/O 裝置錯誤，所以無法執行要求。</span><span class="sxs-lookup"><span data-stu-id="5f34a-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**錯誤 \_ 序列 \_ 無 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="5f34a-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-338">1118 (0x45E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-339">未成功初始化任何序列裝置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="5f34a-340">序列驅動程式將會卸載。</span><span class="sxs-lookup"><span data-stu-id="5f34a-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**錯誤 \_ IRQ \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="5f34a-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-342">1119 (0x45F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-343">無法開啟與其他裝置 (IRQ) 共用中斷要求的裝置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="5f34a-344">至少有一個使用該 IRQ 的其他裝置已開啟。</span><span class="sxs-lookup"><span data-stu-id="5f34a-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**\_寫入錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-346">1120 (0x460) </span><span class="sxs-lookup"><span data-stu-id="5f34a-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-347">序列 i/o 作業已由另一個寫入至序列埠來完成。</span><span class="sxs-lookup"><span data-stu-id="5f34a-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="5f34a-348">IOCTL \_ 序列 \_ XOFF 計數器已 \_ 達到零。 ) </span><span class="sxs-lookup"><span data-stu-id="5f34a-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**錯誤 \_ 計數器 \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="5f34a-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-350">1121 (0x461) </span><span class="sxs-lookup"><span data-stu-id="5f34a-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-351">序列 i/o 作業已完成，因為超時時間已過期。</span><span class="sxs-lookup"><span data-stu-id="5f34a-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="5f34a-352">IOCTL \_ 序列 \_ XOFF 計數器未 \_ 達到零。 ) </span><span class="sxs-lookup"><span data-stu-id="5f34a-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤的軟碟識別碼標記**</span><span class="sxs-lookup"><span data-stu-id="5f34a-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-354">1122 (0x462) </span><span class="sxs-lookup"><span data-stu-id="5f34a-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-355">在磁片磁碟機上找不到任何識別碼位址標記。</span><span class="sxs-lookup"><span data-stu-id="5f34a-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**錯誤的磁片 \_ 磁碟機 \_ \_ 圖錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-357">1123 (0x463) </span><span class="sxs-lookup"><span data-stu-id="5f34a-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-358">磁片磁區識別碼欄位與磁碟控制卡播放軌位址不符。</span><span class="sxs-lookup"><span data-stu-id="5f34a-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**錯誤 \_ 磁片 \_ 不明 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-360">1124 (0x464) </span><span class="sxs-lookup"><span data-stu-id="5f34a-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-361">磁碟控制卡回報磁片磁碟機無法辨識的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**錯誤的 \_ 軟碟登錄 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-363">1125 (0x465) </span><span class="sxs-lookup"><span data-stu-id="5f34a-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-364">磁碟控制卡在其暫存器中傳回不一致的結果。</span><span class="sxs-lookup"><span data-stu-id="5f34a-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**錯誤 \_ 磁片重新 \_ 校準 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-366">1126 (0x466) </span><span class="sxs-lookup"><span data-stu-id="5f34a-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-367">存取硬碟時，即使在重試之後，重新校準作業也會失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**錯誤 \_ 磁片 \_ 操作 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-369">1127 (0x467) </span><span class="sxs-lookup"><span data-stu-id="5f34a-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-370">存取硬碟時，即使在重試之後，磁片作業也會失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**錯誤 \_ 磁片 \_ 重設 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-372">1128 (0x468) </span><span class="sxs-lookup"><span data-stu-id="5f34a-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-373">存取硬碟時，需要重設磁碟控制卡，但即使失敗也是如此。</span><span class="sxs-lookup"><span data-stu-id="5f34a-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**錯誤 \_ EOM \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="5f34a-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-375">1129 (0x469) </span><span class="sxs-lookup"><span data-stu-id="5f34a-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-376">遇到磁帶的實體結尾。</span><span class="sxs-lookup"><span data-stu-id="5f34a-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**錯誤 \_ 的 \_ \_ 伺服器 \_ 記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="5f34a-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-378">1130 (0x46A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-379">沒有足夠的可用伺服器儲存空間來處理此命令。</span><span class="sxs-lookup"><span data-stu-id="5f34a-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**錯誤 \_ 可能的 \_ 鎖死**</span><span class="sxs-lookup"><span data-stu-id="5f34a-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-381">1131 (0x46B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-382">偵測到潛在的鎖死狀況。</span><span class="sxs-lookup"><span data-stu-id="5f34a-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**錯誤 \_ 對應 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="5f34a-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-384">1132 (0x46C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-385">基底位址或指定的檔案位移沒有適當的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**\_設定 \_ 拒絕電源 \_ 狀態 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-387">1140 (0x474) </span><span class="sxs-lookup"><span data-stu-id="5f34a-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-388">嘗試變更系統電源狀態是由另一個應用程式或驅動程式所拒絕。</span><span class="sxs-lookup"><span data-stu-id="5f34a-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**錯誤 \_ 設定 \_ 電源 \_ 狀態 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-390">1141 (0x475) </span><span class="sxs-lookup"><span data-stu-id="5f34a-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-391">系統 BIOS 無法嘗試變更系統電源狀態。</span><span class="sxs-lookup"><span data-stu-id="5f34a-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**錯誤 \_ 太 \_ 多 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="5f34a-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-393">1142 (0x476) </span><span class="sxs-lookup"><span data-stu-id="5f34a-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-394">嘗試在檔案系統所支援的檔案上建立更多連結。</span><span class="sxs-lookup"><span data-stu-id="5f34a-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**\_舊的 \_ WIN \_ 版本錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-396">1150 (0x47E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-397">指定的程式需要較新版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="5f34a-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**錯誤 \_ 應用程式錯誤的 \_ \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="5f34a-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-399">1151 (0x47F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-400">所指定的程式不是 Windows 或 MS-DOS 程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**\_單一 \_ 實例 \_ 應用程式錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-402">1152 (0x480) </span><span class="sxs-lookup"><span data-stu-id="5f34a-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-403">無法啟動一個以上指定之程式的實例。</span><span class="sxs-lookup"><span data-stu-id="5f34a-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**\_RMODE \_ 應用程式時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-405">1153 (0x481) </span><span class="sxs-lookup"><span data-stu-id="5f34a-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-406">指定的程式是針對較早版本的 Windows 所撰寫。</span><span class="sxs-lookup"><span data-stu-id="5f34a-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**錯誤 \_ 不正確 \_ DLL**</span><span class="sxs-lookup"><span data-stu-id="5f34a-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-408">1154 (0x482) </span><span class="sxs-lookup"><span data-stu-id="5f34a-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-409">執行此應用程式所需的其中一個程式庫檔案已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f34a-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**錯誤 \_ 沒有 \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="5f34a-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-411">1155 (0x483) </span><span class="sxs-lookup"><span data-stu-id="5f34a-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-412">沒有任何應用程式與指定的檔案相關聯，無法進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**錯誤 \_ DDE \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-414">1156 (0x484) </span><span class="sxs-lookup"><span data-stu-id="5f34a-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-415">將命令傳送至應用程式時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_ \_ 找不到錯誤 DLL \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-417">1157 (0x485) </span><span class="sxs-lookup"><span data-stu-id="5f34a-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-418">找不到執行此應用程式所需的程式庫檔案之一。</span><span class="sxs-lookup"><span data-stu-id="5f34a-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**\_沒有 \_ 其他 \_ 使用者 \_ 控制碼的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-420">1158 (0x486) </span><span class="sxs-lookup"><span data-stu-id="5f34a-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-421">目前的進程已使用其系統管理員物件的所有系統額度。</span><span class="sxs-lookup"><span data-stu-id="5f34a-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ 僅限錯誤訊息同步 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-423">1159 (0x487) </span><span class="sxs-lookup"><span data-stu-id="5f34a-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-424">訊息只能與同步作業搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5f34a-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**錯誤 \_ 來源 \_ 元素 \_ 空白**</span><span class="sxs-lookup"><span data-stu-id="5f34a-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-426">1160 (0x488) </span><span class="sxs-lookup"><span data-stu-id="5f34a-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-427">指出的來源元素沒有任何媒體。</span><span class="sxs-lookup"><span data-stu-id="5f34a-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**錯誤 \_ 目的地 \_ 元素已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="5f34a-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-429">1161 (0x489) </span><span class="sxs-lookup"><span data-stu-id="5f34a-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-430">指出的目的地元素已包含媒體。</span><span class="sxs-lookup"><span data-stu-id="5f34a-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**錯誤 \_ 的 \_ 元素 \_ 位址無效**</span><span class="sxs-lookup"><span data-stu-id="5f34a-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-432">1162 (0x48A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-433">指出的元素不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**錯誤 \_ 雜誌 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="5f34a-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-435">1163 (0x48B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-436">指出的專案是不存在之雜誌的一部分。</span><span class="sxs-lookup"><span data-stu-id="5f34a-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**\_需要重新 \_ 初始化錯誤裝置 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-438">1164 (0x48C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-439">指出的裝置需要重新初始化，因為硬體發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**錯誤 \_ 裝置 \_ 需要 \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="5f34a-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-441">1165 (0x48D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-442">裝置已指出需要先清除，再嘗試進行進一步的作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**\_裝置 \_ 門 \_ 開啟時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-444">1166 (0x48E) </span><span class="sxs-lookup"><span data-stu-id="5f34a-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-445">裝置已指出其門已開啟。</span><span class="sxs-lookup"><span data-stu-id="5f34a-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**錯誤 \_ 裝置 \_ 未 \_ 連線**</span><span class="sxs-lookup"><span data-stu-id="5f34a-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-447">1167 (0x48F) </span><span class="sxs-lookup"><span data-stu-id="5f34a-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-448">裝置未連接。</span><span class="sxs-lookup"><span data-stu-id="5f34a-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**\_找不 \_ 到錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-450">1168 (0x490) </span><span class="sxs-lookup"><span data-stu-id="5f34a-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-451">Element not found.</span><span class="sxs-lookup"><span data-stu-id="5f34a-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**錯誤 \_ 無 \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="5f34a-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-453">1169 (0x491) </span><span class="sxs-lookup"><span data-stu-id="5f34a-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-454">索引中的指定索引鍵沒有相符的結果。</span><span class="sxs-lookup"><span data-stu-id="5f34a-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ 找不到錯誤集 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-456">1170 (0x492) </span><span class="sxs-lookup"><span data-stu-id="5f34a-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-457">指定的屬性集不存在物件上。</span><span class="sxs-lookup"><span data-stu-id="5f34a-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_ \_ 找不到錯誤點 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-459">1171 (0x493) </span><span class="sxs-lookup"><span data-stu-id="5f34a-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-460">傳遞至 GetMouseMovePoints 的點不在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**錯誤 \_ 無 \_ 追蹤 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="5f34a-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-462">1172 (0x494) </span><span class="sxs-lookup"><span data-stu-id="5f34a-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-463">追蹤 (工作站) 服務未執行。</span><span class="sxs-lookup"><span data-stu-id="5f34a-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**錯誤 \_ 的 \_ 磁片區 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="5f34a-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-465">1173 (0x495) </span><span class="sxs-lookup"><span data-stu-id="5f34a-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-466">找不到磁片區識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f34a-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**\_無法 \_ \_ 移除 \_ 已取代的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-468">1175 (0x497) </span><span class="sxs-lookup"><span data-stu-id="5f34a-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-469">無法移除要取代的檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**錯誤 \_ 無法 \_ \_ 移動 \_ 取代**</span><span class="sxs-lookup"><span data-stu-id="5f34a-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-471">1176 (0x498) </span><span class="sxs-lookup"><span data-stu-id="5f34a-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-472">無法將取代檔案移至要取代的檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="5f34a-473">要取代的檔案已保留其原始名稱。</span><span class="sxs-lookup"><span data-stu-id="5f34a-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**錯誤 \_ 無法 \_ \_ 移動 \_ 更換 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5f34a-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-475">1177 (0x499) </span><span class="sxs-lookup"><span data-stu-id="5f34a-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-476">無法將取代檔案移至要取代的檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="5f34a-477">要取代的檔案已使用備份名稱重新命名。</span><span class="sxs-lookup"><span data-stu-id="5f34a-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**錯誤 \_ 日誌 \_ 刪除 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="5f34a-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-479">1178 (0x49A) </span><span class="sxs-lookup"><span data-stu-id="5f34a-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-480">正在刪除磁片區變更日誌。</span><span class="sxs-lookup"><span data-stu-id="5f34a-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**錯誤 \_ 日誌 \_ 未 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="5f34a-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-482">1179 (0x49B) </span><span class="sxs-lookup"><span data-stu-id="5f34a-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-483">磁片區變更日誌未啟用。</span><span class="sxs-lookup"><span data-stu-id="5f34a-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_發現可能 \_ 的檔案錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-485">1180 (0x49C) </span><span class="sxs-lookup"><span data-stu-id="5f34a-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-486">找到檔案，但它可能不是正確的檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_ \_ 已刪除錯誤記錄項目 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-488">1181 (0x49D) </span><span class="sxs-lookup"><span data-stu-id="5f34a-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-489">記錄項目已從日誌中刪除。</span><span class="sxs-lookup"><span data-stu-id="5f34a-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**\_ \_ 已排程錯誤 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="5f34a-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-491">1190 (0x4A6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-492">已排程系統關機。</span><span class="sxs-lookup"><span data-stu-id="5f34a-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**\_關機 \_ 使用者 \_ 登入 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-494">1191 (0x4A7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-495">因為有其他使用者登入電腦，所以無法起始系統關機。</span><span class="sxs-lookup"><span data-stu-id="5f34a-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**錯誤 \_ 錯誤 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="5f34a-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-497">1200 (0x4B0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-498">指定的裝置名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**錯誤 \_ 連接 \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="5f34a-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-500">1201 (0x4B1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-501">裝置目前未連線，但它是記住的連接。</span><span class="sxs-lookup"><span data-stu-id="5f34a-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**\_ \_ 已記住錯誤 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="5f34a-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-503">1202 (0x4B2) </span><span class="sxs-lookup"><span data-stu-id="5f34a-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-504">本機裝置名稱已記住與另一個網路資源的連線。</span><span class="sxs-lookup"><span data-stu-id="5f34a-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**錯誤 \_ 沒有 \_ 淨 \_ 或不 \_ 正確的 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="5f34a-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-506">1203 (0x4B3) </span><span class="sxs-lookup"><span data-stu-id="5f34a-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-507">網路路徑的輸入不正確、不存在，或網路提供者目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f34a-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="5f34a-508">請嘗試重新鍵入路徑，或洽詢您的網路系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5f34a-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**錯誤 \_ 的 \_ 提供者錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-510">1204 (0x4B4) </span><span class="sxs-lookup"><span data-stu-id="5f34a-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-511">指定的網路提供者名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**錯誤 \_ 無法 \_ 開啟 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="5f34a-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-513">1205 (0x4B5) </span><span class="sxs-lookup"><span data-stu-id="5f34a-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-514">無法開啟網路連線設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f34a-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**錯誤 \_ 的 \_ 設定檔錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-516">1206 (0x4B6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-517">網路連接設定檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f34a-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**錯誤 \_ 不是 \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="5f34a-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-519">1207 (0x4B7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-520">無法列舉非容器。</span><span class="sxs-lookup"><span data-stu-id="5f34a-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**錯誤 \_ 擴充 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-522">1208 (0x4B8) </span><span class="sxs-lookup"><span data-stu-id="5f34a-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-523">發生擴充錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**錯誤 \_ 不正確擁有 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-525">1209 (0x4B9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-526">指定組名的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**錯誤 \_ 不正確 \_ COMPUTERNAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-528">1210 (0x4BA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-529">指定電腦名稱稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**錯誤 \_ 不正確 \_ 事件名稱**</span><span class="sxs-lookup"><span data-stu-id="5f34a-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-531">1211 (0x4BB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-532">指定之事件名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**錯誤 \_ 不正確 \_ DOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-534">1212 (0x4BC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-535">指定功能變數名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**錯誤 \_ 不正確 \_ SERVICENAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-537">1213 (0x4BD) </span><span class="sxs-lookup"><span data-stu-id="5f34a-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-538">指定服務名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**錯誤 \_ 的 \_ 網路名稱無效**</span><span class="sxs-lookup"><span data-stu-id="5f34a-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-540">1214 (0x4BE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-541">指定之網路名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**錯誤 \_ 不正確 \_ 共用名稱**</span><span class="sxs-lookup"><span data-stu-id="5f34a-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-543">1215 (0x4BF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-544">指定之共用名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**錯誤 \_ 無效 \_ PASSWORDNAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-546">1216 (0x4C0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-547">指定之密碼的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**錯誤 \_ 無效 \_ MESSAGENAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-549">1217 (0x4C1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-550">指定之訊息名稱的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**錯誤 \_ 無效 \_ MESSAGEDEST**</span><span class="sxs-lookup"><span data-stu-id="5f34a-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-552">1218 (0x4C2) </span><span class="sxs-lookup"><span data-stu-id="5f34a-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-553">指定之訊息目的地的格式無效。</span><span class="sxs-lookup"><span data-stu-id="5f34a-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**錯誤 \_ 會話 \_ 認證 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="5f34a-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-555">1219 (0x4C3) </span><span class="sxs-lookup"><span data-stu-id="5f34a-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-556">不允許使用多個使用者名稱對伺服器或共用資源進行多個連接。</span><span class="sxs-lookup"><span data-stu-id="5f34a-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="5f34a-557">中斷伺服器或共用資源的所有先前連接，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="5f34a-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_超過遠端 \_ 會話 \_ 限制 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-559">1220 (0x4C4) </span><span class="sxs-lookup"><span data-stu-id="5f34a-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-560">嘗試建立網路伺服器的會話，但已為該伺服器建立了太多會話。</span><span class="sxs-lookup"><span data-stu-id="5f34a-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**錯誤 \_ DUP \_ DOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="5f34a-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-562">1221 (0x4C5) </span><span class="sxs-lookup"><span data-stu-id="5f34a-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-563">網路上的另一部電腦已在使用工作組或功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="5f34a-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**錯誤 \_ 的 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="5f34a-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-565">1222 (0x4C6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-566">網路不存在或未啟動。</span><span class="sxs-lookup"><span data-stu-id="5f34a-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**錯誤已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="5f34a-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-568">1223 (0x4C7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-569">使用者已取消作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_使用者 \_ 對應檔 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-571">1224 (0x4C8) </span><span class="sxs-lookup"><span data-stu-id="5f34a-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-572">在開啟使用者對應區段的檔案上，無法執行所要求的作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**\_拒絕連接 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-574">1225 (0x4C9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-575">遠端電腦拒絕網路連線。</span><span class="sxs-lookup"><span data-stu-id="5f34a-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**錯誤 \_ 正常 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="5f34a-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-577">1226 (0x4CA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-578">網路連接已正常關閉。</span><span class="sxs-lookup"><span data-stu-id="5f34a-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_ \_ 已 \_ 關聯的錯誤位址**</span><span class="sxs-lookup"><span data-stu-id="5f34a-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-580">1227 (0x4CB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-581">網路傳輸端點已經有與其相關聯的位址。</span><span class="sxs-lookup"><span data-stu-id="5f34a-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**錯誤 \_ 位址 \_ 未 \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="5f34a-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-583">1228 (0x4CC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-584">尚未與網路端點相關聯的位址。</span><span class="sxs-lookup"><span data-stu-id="5f34a-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**\_連接 \_ 不正確錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-586">1229 (0x4CD) </span><span class="sxs-lookup"><span data-stu-id="5f34a-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-587">嘗試在不存在的網路連接上進行作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**使用中的 \_ 連接錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-589">1230 (0x4CE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-590">在使用中的網路連接上嘗試了不正確作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**無法連線到 \_ 網路錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-592">1231 (0x4CF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-593">無法到達網路位置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-593">The network location cannot be reached.</span></span> <span data-ttu-id="5f34a-594">如需網路疑難排解的詳細資訊，請參閱 Windows 說明。</span><span class="sxs-lookup"><span data-stu-id="5f34a-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**錯誤 \_ 主機 \_ 無法連線**</span><span class="sxs-lookup"><span data-stu-id="5f34a-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-596">1232 (0x4D0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-597">無法到達網路位置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-597">The network location cannot be reached.</span></span> <span data-ttu-id="5f34a-598">如需網路疑難排解的詳細資訊，請參閱 Windows 說明。</span><span class="sxs-lookup"><span data-stu-id="5f34a-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**錯誤 \_ 通訊協定 \_ 無法連線**</span><span class="sxs-lookup"><span data-stu-id="5f34a-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-600">1233 (0x4D1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-601">無法到達網路位置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-601">The network location cannot be reached.</span></span> <span data-ttu-id="5f34a-602">如需網路疑難排解的詳細資訊，請參閱 Windows 說明。</span><span class="sxs-lookup"><span data-stu-id="5f34a-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**錯誤 \_ 埠 \_ 無法連線**</span><span class="sxs-lookup"><span data-stu-id="5f34a-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-604">1234 (0x4D2) </span><span class="sxs-lookup"><span data-stu-id="5f34a-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-605">遠端系統上的目的地網路端點沒有任何服務正在運作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**錯誤 \_ 要求已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="5f34a-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-607">1235 (0x4D3) </span><span class="sxs-lookup"><span data-stu-id="5f34a-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-608">要求已中止。</span><span class="sxs-lookup"><span data-stu-id="5f34a-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**錯誤 \_ 連接已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="5f34a-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-610">1236 (0x4D4) </span><span class="sxs-lookup"><span data-stu-id="5f34a-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-611">本機系統已中止網路連接。</span><span class="sxs-lookup"><span data-stu-id="5f34a-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**錯誤 \_ 重試**</span><span class="sxs-lookup"><span data-stu-id="5f34a-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-613">1237 (0x4D5) </span><span class="sxs-lookup"><span data-stu-id="5f34a-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-614">無法完成作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-614">The operation could not be completed.</span></span> <span data-ttu-id="5f34a-615">應執行重試。</span><span class="sxs-lookup"><span data-stu-id="5f34a-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_連接 \_ 計數 \_ 限制錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-617">1238 (0x4D6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-618">無法連接到伺服器，因為已達到此帳戶的並行連接數目限制。</span><span class="sxs-lookup"><span data-stu-id="5f34a-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**錯誤 \_ 登入 \_ 時間 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="5f34a-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-620">1239 (0x4D7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-621">在此帳戶的一天未授權時間內嘗試登入。</span><span class="sxs-lookup"><span data-stu-id="5f34a-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**錯誤 \_ 登入 \_ WKSTA \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="5f34a-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-623">1240 (0x4D8) </span><span class="sxs-lookup"><span data-stu-id="5f34a-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-624">帳戶未經授權，無法從此工作站登入。</span><span class="sxs-lookup"><span data-stu-id="5f34a-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**錯誤 \_ 的 \_ 位址不正確**</span><span class="sxs-lookup"><span data-stu-id="5f34a-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-626">1241 (0x4D9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-627">網路位址無法用於要求的操作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**\_已 \_ 註冊錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-629">1242 (0x4DA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-630">服務已註冊。</span><span class="sxs-lookup"><span data-stu-id="5f34a-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ 找不到錯誤服務 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-632">1243 (0x4DB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-633">指定的服務不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**錯誤 \_ 未 \_ 通過驗證**</span><span class="sxs-lookup"><span data-stu-id="5f34a-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-635">1244 (0x4DC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-636">未執行所要求的作業，因為使用者尚未經過驗證。</span><span class="sxs-lookup"><span data-stu-id="5f34a-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**錯誤 \_ 未 \_ 登入 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-638">1245 (0x4DD) </span><span class="sxs-lookup"><span data-stu-id="5f34a-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-639">未執行所要求的作業，因為使用者尚未登入網路。</span><span class="sxs-lookup"><span data-stu-id="5f34a-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="5f34a-640">指定的服務不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**錯誤 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="5f34a-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-642">1246 (0x4DE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-643">繼續進行中的工作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**錯誤 \_ 已 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="5f34a-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-645">1247 (0x4DF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-646">已嘗試在初始化完成時執行初始化作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**\_沒有 \_ 其他 \_ 裝置的錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-648">1248 (0x4E0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-649">沒有其他本機裝置。</span><span class="sxs-lookup"><span data-stu-id="5f34a-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**錯誤 \_ 的 \_ \_ 網站錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-651">1249 (0x4E1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-652">指定的網站不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**\_域 \_ 控制器 \_ 存在錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-654">1250 (0x4E2) </span><span class="sxs-lookup"><span data-stu-id="5f34a-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-655">具有指定名稱的網域控制站已經存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**\_只有 \_ 在 \_ 連接時才會發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-657">1251 (0x4E3) </span><span class="sxs-lookup"><span data-stu-id="5f34a-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-658">只有當您連接到伺服器時，才支援這項作業。</span><span class="sxs-lookup"><span data-stu-id="5f34a-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**錯誤覆 \_ 寫 \_ NOCHANGES**</span><span class="sxs-lookup"><span data-stu-id="5f34a-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-660">1252 (0x4E4) </span><span class="sxs-lookup"><span data-stu-id="5f34a-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-661">即使沒有任何變更，群組原則架構也應該呼叫延伸模組。</span><span class="sxs-lookup"><span data-stu-id="5f34a-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**錯誤 \_ 的 \_ 使用者 \_ 設定檔錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-663">1253 (0x4E5) </span><span class="sxs-lookup"><span data-stu-id="5f34a-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-664">指定的使用者沒有有效的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f34a-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**\_SBS 不 \_ 支援 \_ 的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-666">1254 (0x4E6) </span><span class="sxs-lookup"><span data-stu-id="5f34a-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-667">執行 Windows Server 2003 for Small Business Server 的電腦不支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="5f34a-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**錯誤 \_ 伺服器 \_ 關閉 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="5f34a-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-669">1255 (0x4E7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-670">伺服器電腦正在關機。</span><span class="sxs-lookup"><span data-stu-id="5f34a-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**錯誤 \_ 主機 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="5f34a-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-672">1256 (0x4E8) </span><span class="sxs-lookup"><span data-stu-id="5f34a-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-673">遠端系統無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f34a-673">The remote system is not available.</span></span> <span data-ttu-id="5f34a-674">如需網路疑難排解的詳細資訊，請參閱 Windows 說明。</span><span class="sxs-lookup"><span data-stu-id="5f34a-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**錯誤 \_ 非 \_ 帳戶 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="5f34a-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-676">1257 (0x4E9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-677">提供的安全識別碼並非來自帳戶網域。</span><span class="sxs-lookup"><span data-stu-id="5f34a-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**錯誤 \_ 非 \_ 網域 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="5f34a-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-679">1258 (0x4EA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-680">提供的安全識別碼沒有網域元件。</span><span class="sxs-lookup"><span data-stu-id="5f34a-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**\_APPHELP \_ 區塊時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-682">1259 (0x4EB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-683">AppHelp 對話方塊已取消，因此無法啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_ \_ 原則停用存取錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-685">1260 (0x4EC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-686">群組原則封鎖了此程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-686">This program is blocked by group policy.</span></span> <span data-ttu-id="5f34a-687">如需相關資訊，請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5f34a-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**錯誤的 \_ REG \_ NAT \_ 耗用量**</span><span class="sxs-lookup"><span data-stu-id="5f34a-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-689">1261 (0x4ED) </span><span class="sxs-lookup"><span data-stu-id="5f34a-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-690">程式嘗試使用不正確註冊值。</span><span class="sxs-lookup"><span data-stu-id="5f34a-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="5f34a-691">通常是因為未初始化的登錄所造成。</span><span class="sxs-lookup"><span data-stu-id="5f34a-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="5f34a-692">此錯誤是 Itanium 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**\_離線 CSCSHARE 時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-694">1262 (0x4EE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-695">共用目前為離線或不存在。</span><span class="sxs-lookup"><span data-stu-id="5f34a-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**錯誤 \_ PKINIT \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-697">1263 (0x4EF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-698">Kerberos 通訊協定在智慧卡登入期間驗證 KDC 憑證時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="5f34a-699">系統事件記錄檔中有更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="5f34a-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**錯誤的 \_ 智慧卡 \_ 子系統 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-701">1264 (0x4F0) </span><span class="sxs-lookup"><span data-stu-id="5f34a-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-702">Kerberos 通訊協定嘗試利用智慧卡子系統時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**偵測 \_ 到錯誤降級 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-704">1265 (0x4F1) </span><span class="sxs-lookup"><span data-stu-id="5f34a-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-705">系統無法連絡網域控制站來服務驗證要求。</span><span class="sxs-lookup"><span data-stu-id="5f34a-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="5f34a-706">請稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="5f34a-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**錯誤 \_ 電腦已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="5f34a-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-708">1271 (0x4F7) </span><span class="sxs-lookup"><span data-stu-id="5f34a-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-709">電腦已鎖定，無法在沒有強制選項的情況下關閉。</span><span class="sxs-lookup"><span data-stu-id="5f34a-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**錯誤 \_ 回呼 \_ 提供 \_ 不正確 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5f34a-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-711">1273 (0x4F9) </span><span class="sxs-lookup"><span data-stu-id="5f34a-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-712">應用程式定義的回呼在呼叫時，會給予不正確資料。</span><span class="sxs-lookup"><span data-stu-id="5f34a-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_需要錯誤同步處理 \_ 前景重新 \_ 整理 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-714">1274 (0x4FA) </span><span class="sxs-lookup"><span data-stu-id="5f34a-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-715">群組原則架構應該在同步的前景原則重新整理中呼叫延伸模組。</span><span class="sxs-lookup"><span data-stu-id="5f34a-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**錯誤 \_ 驅動程式已 \_ 封鎖**</span><span class="sxs-lookup"><span data-stu-id="5f34a-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-717">1275 (0x4FB) </span><span class="sxs-lookup"><span data-stu-id="5f34a-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-718">此驅動程式已被封鎖而無法載入。</span><span class="sxs-lookup"><span data-stu-id="5f34a-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**錯誤 \_ 無效 \_ 的匯入 \_ \_ 非 \_ DLL**</span><span class="sxs-lookup"><span data-stu-id="5f34a-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-720">1276 (0x4FC) </span><span class="sxs-lookup"><span data-stu-id="5f34a-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-721">動態連結程式庫 (DLL) 參考的模組不是 DLL 也不是進程的可執行檔映射。</span><span class="sxs-lookup"><span data-stu-id="5f34a-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_存取 \_ 停用 \_ WEBBLADE 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-723">1277 (0x4FD) </span><span class="sxs-lookup"><span data-stu-id="5f34a-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-724">Windows 無法開啟此程式，因為它已停用。</span><span class="sxs-lookup"><span data-stu-id="5f34a-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**\_存取 \_ 停用的錯誤 \_ WEBBLADE \_ 篡改**</span><span class="sxs-lookup"><span data-stu-id="5f34a-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-726">1278 (0x4FE) </span><span class="sxs-lookup"><span data-stu-id="5f34a-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-727">因為授權強制系統已遭篡改或損毀，所以 Windows 無法開啟此程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**錯誤 \_ 復原 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-729">1279 (0x4FF) </span><span class="sxs-lookup"><span data-stu-id="5f34a-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-730">交易復原失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**錯誤 \_ 已經是 \_ 光纖**</span><span class="sxs-lookup"><span data-stu-id="5f34a-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="5f34a-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-733">目前的執行緒已轉換為光纖。</span><span class="sxs-lookup"><span data-stu-id="5f34a-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**錯誤 \_ 已經是 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="5f34a-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="5f34a-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-736">目前的執行緒已經從光纖轉換。</span><span class="sxs-lookup"><span data-stu-id="5f34a-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**錯誤 \_ 堆疊 \_ 緩衝區 \_ 溢出**</span><span class="sxs-lookup"><span data-stu-id="5f34a-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="5f34a-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-739">系統在此應用程式中偵測到堆疊型緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="5f34a-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="5f34a-740">此溢出可能會讓惡意使用者能夠掌控此應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**\_超過錯誤參數 \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="5f34a-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-743">其中一個參數中的資料比函式可操作的更多。</span><span class="sxs-lookup"><span data-stu-id="5f34a-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**錯誤 \_ 偵錯工具非使用中 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="5f34a-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-746">嘗試對 debug 物件進行作業失敗，因為物件正在刪除中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**錯誤 \_ 延遲 \_ 載入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5f34a-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-748">1285 (0x505) </span><span class="sxs-lookup"><span data-stu-id="5f34a-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-749">嘗試延遲載入 .dll 或取得延遲載入的函式位址。 dll 失敗。</span><span class="sxs-lookup"><span data-stu-id="5f34a-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**不 \_ 允許錯誤的 VDM \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="5f34a-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-752">%1 是16位應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f34a-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="5f34a-753">您沒有執行16位應用程式的許可權。</span><span class="sxs-lookup"><span data-stu-id="5f34a-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="5f34a-754">請向您的系統管理員確認您的許可權。</span><span class="sxs-lookup"><span data-stu-id="5f34a-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**錯誤 \_ 不明 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="5f34a-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-757">沒有足夠的資訊可找出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="5f34a-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**錯誤 \_ 不正確 \_ CRUNTIME \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="5f34a-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="5f34a-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-760">傳遞至 C 執行時間函數的參數不正確。</span><span class="sxs-lookup"><span data-stu-id="5f34a-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**\_VDL 以外的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="5f34a-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-763">作業發生超過檔案的有效資料長度。</span><span class="sxs-lookup"><span data-stu-id="5f34a-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**錯誤 \_ 的 \_ 服務 \_ SID \_ 類型不相容**</span><span class="sxs-lookup"><span data-stu-id="5f34a-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="5f34a-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-766">服務啟動失敗，因為相同進程中的一或多個服務具有不相容的服務 SID 類型設定。</span><span class="sxs-lookup"><span data-stu-id="5f34a-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="5f34a-767">具有受限制服務 SID 類型的服務，只能與具有受限 SID 類型的其他服務並存于相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="5f34a-768">如果這項服務的服務 SID 類型是剛設定的，則必須重新開機裝載進程，才能啟動此服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="5f34a-769">在 Windows Server 2003 和 Windows XP 上，不受限制的服務無法與其他服務並存于相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="5f34a-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="5f34a-770">具有不受限制服務 SID 類型的服務必須移至擁有的進程，才能啟動此服務。</span><span class="sxs-lookup"><span data-stu-id="5f34a-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**錯誤 \_ 驅動程式 \_ 進程已 \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="5f34a-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="5f34a-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-773">裝載此裝置之驅動程式的進程已終止。</span><span class="sxs-lookup"><span data-stu-id="5f34a-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**錯誤的 \_ 執行 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="5f34a-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="5f34a-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-776">作業嘗試超過執行定義的限制。</span><span class="sxs-lookup"><span data-stu-id="5f34a-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**錯誤 \_ 進程 \_ 受到 \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="5f34a-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="5f34a-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-779">目標進程或目標執行緒的包含進程是受保護的進程。</span><span class="sxs-lookup"><span data-stu-id="5f34a-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**錯誤 \_ 服務 \_ 通知 \_ 用戶端 \_ 延遲**</span><span class="sxs-lookup"><span data-stu-id="5f34a-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="5f34a-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-782">服務通知用戶端延遲到電腦目前的服務狀態之後太遠。</span><span class="sxs-lookup"><span data-stu-id="5f34a-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_超過錯誤磁片 \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="5f34a-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-785">要求的檔案作業失敗，因為已超過儲存配額。</span><span class="sxs-lookup"><span data-stu-id="5f34a-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="5f34a-786">若要釋出磁碟空間，請將檔案移到不同的位置，或刪除不必要的檔案。</span><span class="sxs-lookup"><span data-stu-id="5f34a-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="5f34a-787">如需相關資訊，請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5f34a-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**封鎖的錯誤 \_ 內容 \_**</span><span class="sxs-lookup"><span data-stu-id="5f34a-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="5f34a-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-790">要求的檔案作業失敗，因為儲存原則封鎖了該類型的檔。</span><span class="sxs-lookup"><span data-stu-id="5f34a-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="5f34a-791">如需相關資訊，請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5f34a-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**錯誤 \_ 的 \_ 服務 \_ 許可權不相容**</span><span class="sxs-lookup"><span data-stu-id="5f34a-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="5f34a-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-794">服務帳戶設定中沒有正常運作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="5f34a-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="5f34a-795">您可以使用服務 Microsoft Management Console (MMC) 嵌入式管理單元 (services.msc) 和本機安全性設定 MMC 嵌入式管理單元 (secpol.msc，以查看服務設定和帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="5f34a-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**錯誤 \_ 應用程式停止 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="5f34a-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="5f34a-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-798">這項作業所涉及的執行緒似乎沒有回應。</span><span class="sxs-lookup"><span data-stu-id="5f34a-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f34a-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**錯誤 \_ 不正確 \_ 標籤**</span><span class="sxs-lookup"><span data-stu-id="5f34a-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f34a-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="5f34a-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="5f34a-801">指出特定的安全識別碼可能無法指派為物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5f34a-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="5f34a-802">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f34a-802">Requirements</span></span>



| <span data-ttu-id="5f34a-803">需求</span><span class="sxs-lookup"><span data-stu-id="5f34a-803">Requirement</span></span> | <span data-ttu-id="5f34a-804">值</span><span class="sxs-lookup"><span data-stu-id="5f34a-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f34a-805">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f34a-805">Minimum supported client</span></span><br/> | <span data-ttu-id="5f34a-806">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f34a-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f34a-807">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f34a-807">Minimum supported server</span></span><br/> | <span data-ttu-id="5f34a-808">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f34a-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f34a-809">標頭</span><span class="sxs-lookup"><span data-stu-id="5f34a-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f34a-810"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f34a-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f34a-811">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f34a-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f34a-812">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5f34a-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




