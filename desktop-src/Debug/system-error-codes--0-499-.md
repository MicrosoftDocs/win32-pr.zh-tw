---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼0-499，適用于開發人員。
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: '系統錯誤碼 (0-499)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847334"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="c87fa-103">系統錯誤碼 (0-499) </span><span class="sxs-lookup"><span data-stu-id="c87fa-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="c87fa-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="c87fa-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="c87fa-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="c87fa-106">下列清單說明 [系統錯誤碼](system-error-codes.md) (錯誤0到 499) 。</span><span class="sxs-lookup"><span data-stu-id="c87fa-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="c87fa-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="c87fa-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="c87fa-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="c87fa-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="c87fa-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**錯誤 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="c87fa-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-110">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-111">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c87fa-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**錯誤不正確函式 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-113">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="c87fa-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-114">不正確的函數。</span><span class="sxs-lookup"><span data-stu-id="c87fa-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_ \_ \_ 找不到錯誤檔案**</span><span class="sxs-lookup"><span data-stu-id="c87fa-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-116">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="c87fa-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-117">系統找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_ \_ 找不到錯誤路徑 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-119">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="c87fa-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-120">系統找不到所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="c87fa-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**錯誤 \_ 太 \_ 多 \_ 開啟 \_ 的檔案**</span><span class="sxs-lookup"><span data-stu-id="c87fa-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-122">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="c87fa-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-123">系統無法開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-125">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="c87fa-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-126">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c87fa-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="c87fa-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-128">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="c87fa-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-129">控制代碼無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**錯誤 \_ 領域 \_ 垃圾桶**</span><span class="sxs-lookup"><span data-stu-id="c87fa-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-131">7 (0x7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-132">儲存體控制區塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="c87fa-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="c87fa-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-134">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="c87fa-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-135">沒有足夠的記憶體資源可用來處理此命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**錯誤 \_ 不正確 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="c87fa-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-137">9 (0x9) </span><span class="sxs-lookup"><span data-stu-id="c87fa-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-138">儲存體控制區塊位址無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**錯誤 \_ 的 \_ 環境錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-140">10 (0xA) </span><span class="sxs-lookup"><span data-stu-id="c87fa-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-141">環境不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**錯誤 \_ \_ 格式錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-143">11 (0xB) </span><span class="sxs-lookup"><span data-stu-id="c87fa-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-144">嘗試載入了格式不正確的程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**\_存取不正確錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-146">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="c87fa-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-147">存取程式碼無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**錯誤 \_ 不正確 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c87fa-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-149">13 (0xD) </span><span class="sxs-lookup"><span data-stu-id="c87fa-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-150">資料無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**錯誤 \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="c87fa-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-152">14 (0xE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-153">沒有足夠的儲存空間可用來完成此操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**錯誤 \_ 不正確 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="c87fa-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-155">15 (0xF) </span><span class="sxs-lookup"><span data-stu-id="c87fa-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-156">系統找不到指定的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c87fa-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**錯誤的 \_ 當前 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="c87fa-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-158">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="c87fa-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-159">無法移除目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**錯誤 \_ 不是 \_ 相同的 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="c87fa-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-161">17 (0x11) </span><span class="sxs-lookup"><span data-stu-id="c87fa-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-162">系統無法將檔案移至不同的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c87fa-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**錯誤 \_ 的 \_ 檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-164">18 (0x12) </span><span class="sxs-lookup"><span data-stu-id="c87fa-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-165">沒有其他檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**錯誤 \_ 寫入 \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="c87fa-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-167">19 (0x13) </span><span class="sxs-lookup"><span data-stu-id="c87fa-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-168">媒體受到寫入保護。</span><span class="sxs-lookup"><span data-stu-id="c87fa-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**錯誤 \_ 錯誤 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="c87fa-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-170">20 (0x14) </span><span class="sxs-lookup"><span data-stu-id="c87fa-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-171">系統找不到指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="c87fa-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**錯誤 \_ 未 \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="c87fa-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-173">21 (0x15) </span><span class="sxs-lookup"><span data-stu-id="c87fa-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-174">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c87fa-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**錯誤錯誤的 \_ \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="c87fa-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-176">22 (0x16) </span><span class="sxs-lookup"><span data-stu-id="c87fa-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-177">裝置無法辨識命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**錯誤 \_ CRC**</span><span class="sxs-lookup"><span data-stu-id="c87fa-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-179">23 (0x17) </span><span class="sxs-lookup"><span data-stu-id="c87fa-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-180">資料錯誤 (迴圈冗余檢查) 。</span><span class="sxs-lookup"><span data-stu-id="c87fa-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**錯誤 \_ \_ 長度錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-182">24 (0x18) </span><span class="sxs-lookup"><span data-stu-id="c87fa-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-183">程式發出命令，但命令長度不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**錯誤 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="c87fa-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-185">25 (0x19) </span><span class="sxs-lookup"><span data-stu-id="c87fa-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-186">磁片磁碟機在磁片上找不到特定的區域或曲目。</span><span class="sxs-lookup"><span data-stu-id="c87fa-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**錯誤 \_ 非 \_ DOS \_ 磁片**</span><span class="sxs-lookup"><span data-stu-id="c87fa-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-188">26 (0x1A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-189">無法存取指定的磁片或磁片。</span><span class="sxs-lookup"><span data-stu-id="c87fa-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ 找不到錯誤磁區 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-191">27 (0x1B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-192">磁片磁碟機找不到要求的磁區。</span><span class="sxs-lookup"><span data-stu-id="c87fa-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**錯誤 \_ 出 \_ \_ 紙**</span><span class="sxs-lookup"><span data-stu-id="c87fa-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-194">28 (0x1C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-195">印表機紙張用完。</span><span class="sxs-lookup"><span data-stu-id="c87fa-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**錯誤 \_ 寫入 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-197">29 (Bugcheck 0x1d) </span><span class="sxs-lookup"><span data-stu-id="c87fa-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-198">系統無法寫入指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="c87fa-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**錯誤 \_ 讀取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-200">30 (0x1E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-201">系統無法從指定的裝置讀取。</span><span class="sxs-lookup"><span data-stu-id="c87fa-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**錯誤 \_ GEN \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="c87fa-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-203">31 (0x1F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-204">連接至系統的裝置無法運作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**錯誤 \_ 共用 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="c87fa-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-206">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="c87fa-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-207">由於已有另一個處理序正在使用該檔案，所以此處理序無法存取該檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**錯誤 \_ 鎖定 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="c87fa-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-209">33 (0x21) </span><span class="sxs-lookup"><span data-stu-id="c87fa-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-210">處理序無法存取檔案，因為其他處理序鎖定了該檔案的一部分。</span><span class="sxs-lookup"><span data-stu-id="c87fa-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**錯誤 \_ 的 \_ 磁片**</span><span class="sxs-lookup"><span data-stu-id="c87fa-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-212">34 (0x22) </span><span class="sxs-lookup"><span data-stu-id="c87fa-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-213">磁片磁碟機中有錯誤的磁片。</span><span class="sxs-lookup"><span data-stu-id="c87fa-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="c87fa-214">插入 %2 (磁片區序號： %3) 到磁片磁碟機 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**\_超出共用 \_ 緩衝區時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-216">36 (0x24) </span><span class="sxs-lookup"><span data-stu-id="c87fa-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-217">開啟太多檔案進行共用。</span><span class="sxs-lookup"><span data-stu-id="c87fa-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**錯誤 \_ 處理 \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="c87fa-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-219">38 (0x26) </span><span class="sxs-lookup"><span data-stu-id="c87fa-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-220">已到達檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="c87fa-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**錯誤 \_ 處理 \_ 磁片已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="c87fa-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-222">39 (0x27) </span><span class="sxs-lookup"><span data-stu-id="c87fa-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-223">磁碟已滿。</span><span class="sxs-lookup"><span data-stu-id="c87fa-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**\_不 \_ 支援的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-225">50 (0x32) </span><span class="sxs-lookup"><span data-stu-id="c87fa-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-226">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="c87fa-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**錯誤 \_ REM \_ 非 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="c87fa-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-228">51 (0x33) </span><span class="sxs-lookup"><span data-stu-id="c87fa-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-229">Windows 找不到網路路徑。</span><span class="sxs-lookup"><span data-stu-id="c87fa-229">Windows cannot find the network path.</span></span> <span data-ttu-id="c87fa-230">請確認網路路徑是否正確，且目的地電腦未忙碌或已關閉。</span><span class="sxs-lookup"><span data-stu-id="c87fa-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="c87fa-231">如果 Windows 仍找不到網路路徑，請洽詢您的網路系統管理員。</span><span class="sxs-lookup"><span data-stu-id="c87fa-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**錯誤 \_ DUP \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="c87fa-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-233">52 (0x34) </span><span class="sxs-lookup"><span data-stu-id="c87fa-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-234">您未連線，因為網路上有重複的名稱。</span><span class="sxs-lookup"><span data-stu-id="c87fa-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="c87fa-235">如果要加入網域，請移至主控台中的 [系統] 變更電腦名稱稱，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="c87fa-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="c87fa-236">如果加入工作組，請選擇另一個工作組名稱。</span><span class="sxs-lookup"><span data-stu-id="c87fa-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**錯誤 \_ 錯誤 \_ NETPATH**</span><span class="sxs-lookup"><span data-stu-id="c87fa-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-238">53 (0x35) </span><span class="sxs-lookup"><span data-stu-id="c87fa-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-239">找不到網路路徑。</span><span class="sxs-lookup"><span data-stu-id="c87fa-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**\_網路 \_ 忙碌時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-241">54 (0x36) </span><span class="sxs-lookup"><span data-stu-id="c87fa-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-242">網路忙碌中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**錯誤 \_ 開發人員 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="c87fa-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-244">55 (0x37) </span><span class="sxs-lookup"><span data-stu-id="c87fa-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-245">無法再使用指定的網路資源或裝置。</span><span class="sxs-lookup"><span data-stu-id="c87fa-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**錯誤 \_ 太 \_ 多 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-247">56 (0x38) </span><span class="sxs-lookup"><span data-stu-id="c87fa-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-248">已達到網路 BIOS 命令的限制。</span><span class="sxs-lookup"><span data-stu-id="c87fa-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**錯誤 \_ ADAP \_ HDW \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-250">57 (0x39) </span><span class="sxs-lookup"><span data-stu-id="c87fa-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-251">發生網路介面卡硬體錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**錯誤 \_ 的 \_ NET \_ RESP**</span><span class="sxs-lookup"><span data-stu-id="c87fa-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-253">58 (0x3A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-254">指定的伺服器無法執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="c87fa-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**\_UNEXP \_ NET \_ ERR 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-256">59 (0x3B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-257">發生未預期的網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**錯誤錯誤的 \_ \_ REM \_ ADAP**</span><span class="sxs-lookup"><span data-stu-id="c87fa-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-259">60 (0x3C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-260">遠端介面卡不相容。</span><span class="sxs-lookup"><span data-stu-id="c87fa-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**\_PRINTQ \_ FULL 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-262">61 (0x3D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-263">印表機佇列已滿。</span><span class="sxs-lookup"><span data-stu-id="c87fa-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**錯誤的多工 \_ \_ 緩衝處理 \_ 空間**</span><span class="sxs-lookup"><span data-stu-id="c87fa-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-265">62 (0x3E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-266">伺服器上無法使用儲存等候列印之檔案的空間。</span><span class="sxs-lookup"><span data-stu-id="c87fa-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**錯誤 \_ 列印已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="c87fa-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-268">63 (0x3F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-269">您等候列印的檔案已刪除。</span><span class="sxs-lookup"><span data-stu-id="c87fa-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**\_ \_ 已刪除錯誤的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-271">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="c87fa-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-272">指定的網路名稱不再可用。</span><span class="sxs-lookup"><span data-stu-id="c87fa-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**\_拒絕網路 \_ 存取時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-274">65 (0x41 向) </span><span class="sxs-lookup"><span data-stu-id="c87fa-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-275">網路存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c87fa-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**錯誤 \_ 的 \_ 開發 \_ 類型錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-277">66 (0x42) </span><span class="sxs-lookup"><span data-stu-id="c87fa-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-278">網路資源類型不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**錯誤 \_ 的 \_ 網路 \_ 名稱錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-280">67 (0x43) </span><span class="sxs-lookup"><span data-stu-id="c87fa-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-281">找不到網路名稱。</span><span class="sxs-lookup"><span data-stu-id="c87fa-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**錯誤 \_ 太 \_ 多 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="c87fa-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-283">68 (0x44) </span><span class="sxs-lookup"><span data-stu-id="c87fa-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-284">已超過本機電腦網路介面卡的名稱限制。</span><span class="sxs-lookup"><span data-stu-id="c87fa-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**錯誤 \_ 太 \_ 多 \_ SES 之始**</span><span class="sxs-lookup"><span data-stu-id="c87fa-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-286">69 (0x45) </span><span class="sxs-lookup"><span data-stu-id="c87fa-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-287">已超過網路 BIOS 會話限制。</span><span class="sxs-lookup"><span data-stu-id="c87fa-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**\_共用錯誤 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="c87fa-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-289">70 (0x46) </span><span class="sxs-lookup"><span data-stu-id="c87fa-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-290">遠端伺服器已暫停或正在啟動中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**錯誤 \_ 需求 \_ 未 \_ ACCEP**</span><span class="sxs-lookup"><span data-stu-id="c87fa-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-292">71 (0x47) </span><span class="sxs-lookup"><span data-stu-id="c87fa-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-293">目前無法再對此遠端電腦進行連線，因為電腦可以接受的連線數目已經過多。</span><span class="sxs-lookup"><span data-stu-id="c87fa-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**錯誤 \_ REDIR \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="c87fa-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-295">72 (0x48) </span><span class="sxs-lookup"><span data-stu-id="c87fa-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-296">指定的印表機或磁片裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c87fa-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**錯誤檔案已 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="c87fa-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-298">80 (0x50) </span><span class="sxs-lookup"><span data-stu-id="c87fa-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-299">檔案存在。</span><span class="sxs-lookup"><span data-stu-id="c87fa-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**錯誤 \_ 無法 \_ 進行**</span><span class="sxs-lookup"><span data-stu-id="c87fa-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-301">82 (0x52) </span><span class="sxs-lookup"><span data-stu-id="c87fa-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-302">無法建立目錄或檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**錯誤 \_ 失敗 \_ I24**</span><span class="sxs-lookup"><span data-stu-id="c87fa-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-304">83 (0x53) </span><span class="sxs-lookup"><span data-stu-id="c87fa-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-305">在 INT 24 上失敗。</span><span class="sxs-lookup"><span data-stu-id="c87fa-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**\_結構錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-307">84 (0x54) </span><span class="sxs-lookup"><span data-stu-id="c87fa-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-308">無法使用儲存體來處理此要求。</span><span class="sxs-lookup"><span data-stu-id="c87fa-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**\_已 \_ 指派錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-310">85 (0x55) </span><span class="sxs-lookup"><span data-stu-id="c87fa-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-311">本機裝置名稱已在使用中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**錯誤 \_ 不正確 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="c87fa-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-313">86 (0x56) </span><span class="sxs-lookup"><span data-stu-id="c87fa-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-314">指定的網路密碼不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c87fa-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-316">87 (0x57) </span><span class="sxs-lookup"><span data-stu-id="c87fa-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-317">參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**錯誤 \_ 網路 \_ 寫入 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-319">88 (0x58) </span><span class="sxs-lookup"><span data-stu-id="c87fa-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-320">網路上發生寫入錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**錯誤 \_ 無 \_ 處理器 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="c87fa-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-322">89 (0x59) </span><span class="sxs-lookup"><span data-stu-id="c87fa-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-323">系統目前無法啟動另一個進程。</span><span class="sxs-lookup"><span data-stu-id="c87fa-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**錯誤 \_ 太 \_ 多 \_ 信號**</span><span class="sxs-lookup"><span data-stu-id="c87fa-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-325">100 (0x64) </span><span class="sxs-lookup"><span data-stu-id="c87fa-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-326">無法建立另一個系統信號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**\_排除 \_ SEM \_ 已 \_ 擁有的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-328">101 (0x65) </span><span class="sxs-lookup"><span data-stu-id="c87fa-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-329">獨佔信號是由另一個進程所擁有。</span><span class="sxs-lookup"><span data-stu-id="c87fa-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**\_ \_ 設定的錯誤 \_ SEM**</span><span class="sxs-lookup"><span data-stu-id="c87fa-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-331">102 (0x66) </span><span class="sxs-lookup"><span data-stu-id="c87fa-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-332">信號已設定且無法關閉。</span><span class="sxs-lookup"><span data-stu-id="c87fa-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**錯誤 \_ 太 \_ 多 \_ SEM \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="c87fa-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-334">103 (0x67) </span><span class="sxs-lookup"><span data-stu-id="c87fa-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-335">無法再次設定信號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**插 \_ 斷 \_ \_ 時間無效 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-337">104 (0x68) </span><span class="sxs-lookup"><span data-stu-id="c87fa-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-338">無法在插斷時間要求獨佔的信號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**\_SEM \_ 擁有者 \_ 壞掉時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-340">105 (0x69) </span><span class="sxs-lookup"><span data-stu-id="c87fa-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-341">此信號的先前擁有權已結束。</span><span class="sxs-lookup"><span data-stu-id="c87fa-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_SEM \_ 使用者 \_ 限制時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-343">106 (0x6A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-344">插入磁片磁碟機 %1 的磁片。</span><span class="sxs-lookup"><span data-stu-id="c87fa-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**錯誤 \_ 磁片 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="c87fa-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-346">107 (0x6B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-347">程式已停止，因為未插入替代的磁片。</span><span class="sxs-lookup"><span data-stu-id="c87fa-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**錯誤 \_ 磁片磁碟機已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="c87fa-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-349">108 (0x6C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-350">磁片正在使用中，或已被其他進程鎖定。</span><span class="sxs-lookup"><span data-stu-id="c87fa-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**錯誤 \_ 中斷的 \_ 管道**</span><span class="sxs-lookup"><span data-stu-id="c87fa-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-352">109 (0x6D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-353">已結束管道。</span><span class="sxs-lookup"><span data-stu-id="c87fa-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**錯誤 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="c87fa-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-355">110 (0x6E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-356">系統無法開啟指定的裝置或檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**錯誤 \_ 緩衝區 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="c87fa-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-358">111 (0x6F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-359">檔案名稱太長。</span><span class="sxs-lookup"><span data-stu-id="c87fa-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**錯誤 \_ 磁片已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="c87fa-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-361">112 (0x70) </span><span class="sxs-lookup"><span data-stu-id="c87fa-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-362">磁碟的空間不足。</span><span class="sxs-lookup"><span data-stu-id="c87fa-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**\_沒有 \_ 其他 \_ 搜尋 \_ 控制碼的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-364">113 (0x71) </span><span class="sxs-lookup"><span data-stu-id="c87fa-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-365">沒有其他可用的內部檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="c87fa-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**錯誤 \_ 不正確 \_ 目標 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="c87fa-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-367">114 (0x72) </span><span class="sxs-lookup"><span data-stu-id="c87fa-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-368">目標內部檔案識別碼不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**錯誤 \_ 不正確 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="c87fa-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-370">117 (0x75) </span><span class="sxs-lookup"><span data-stu-id="c87fa-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-371">應用程式所進行的 IOCTL 呼叫不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**錯誤 \_ 不正確 \_ 驗證 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c87fa-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-373">118 (0x76) </span><span class="sxs-lookup"><span data-stu-id="c87fa-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-374">驗證寫切換參數值不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**錯誤 \_ 的 \_ 驅動程式 \_ 等級錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-376">119 (0x77) </span><span class="sxs-lookup"><span data-stu-id="c87fa-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-377">系統不支援要求的命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**\_ \_ 未執行錯誤 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="c87fa-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-379">120 (0x78) </span><span class="sxs-lookup"><span data-stu-id="c87fa-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-380">此系統不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c87fa-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**錯誤 \_ SEM \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="c87fa-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-382">121 (0x79) </span><span class="sxs-lookup"><span data-stu-id="c87fa-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-383">信號超時時間已過期。</span><span class="sxs-lookup"><span data-stu-id="c87fa-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-385">122 (0x7A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-386">傳遞給系統呼叫的資料區域太小。</span><span class="sxs-lookup"><span data-stu-id="c87fa-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**錯誤 \_ 不正確 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="c87fa-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-388">123 (0x7B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-389">檔案名、目錄名稱或磁片區標籤語法不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**錯誤 \_ 不正確 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="c87fa-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-391">124 (0x7C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-392">系統呼叫層級不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**錯誤 \_ 的 \_ 磁片區卷 \_ 標**</span><span class="sxs-lookup"><span data-stu-id="c87fa-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-394">125 (0x7D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-395">磁片沒有磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**\_ \_ 找不到錯誤 MOD \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-397">126 (0x7E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-398">找不到指定的模組。</span><span class="sxs-lookup"><span data-stu-id="c87fa-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**\_ \_ 找不到錯誤處理器 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-400">127 (0x7F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-401">找不到指定的程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**錯誤 \_ 等候 \_ 沒有 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="c87fa-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-403">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="c87fa-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-404">沒有任何子進程需要等候。</span><span class="sxs-lookup"><span data-stu-id="c87fa-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**錯誤 \_ 子系 \_ 未 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="c87fa-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-406">129 (0x81) </span><span class="sxs-lookup"><span data-stu-id="c87fa-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-407">%1 應用程式無法在 Win32 模式中執行。</span><span class="sxs-lookup"><span data-stu-id="c87fa-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**錯誤 \_ 直接 \_ 存取 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="c87fa-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-409">130 (0x82) </span><span class="sxs-lookup"><span data-stu-id="c87fa-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-410">嘗試針對原始磁片 i/o 以外的作業，使用開啟磁碟分割的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="c87fa-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**錯誤 \_ 負 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="c87fa-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-412">131 (0x83) </span><span class="sxs-lookup"><span data-stu-id="c87fa-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-413">嘗試在檔開頭之前移動檔案指標。</span><span class="sxs-lookup"><span data-stu-id="c87fa-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_ \_ 裝置上的錯誤搜尋 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-415">132 (0x84) </span><span class="sxs-lookup"><span data-stu-id="c87fa-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-416">無法在指定的裝置或檔案上設定檔案指標。</span><span class="sxs-lookup"><span data-stu-id="c87fa-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**錯誤 \_ 為 \_ 聯結 \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="c87fa-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-418">133 (0x85) </span><span class="sxs-lookup"><span data-stu-id="c87fa-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-419">JOIN 或 SUBST 命令無法用於包含先前已加入之磁片磁碟機的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c87fa-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**\_已 \_ 加入錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-421">134 (0x86) </span><span class="sxs-lookup"><span data-stu-id="c87fa-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-422">嘗試在已加入的磁片磁碟機上使用 JOIN 或 SUBST 命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**錯誤 \_ 為 \_ SUBSTED**</span><span class="sxs-lookup"><span data-stu-id="c87fa-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-424">135 (0x87) </span><span class="sxs-lookup"><span data-stu-id="c87fa-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-425">嘗試在已替代的磁片磁碟機上使用 JOIN 或 SUBST 命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**錯誤 \_ 未 \_ 加入**</span><span class="sxs-lookup"><span data-stu-id="c87fa-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-427">136 (0x88) </span><span class="sxs-lookup"><span data-stu-id="c87fa-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-428">系統嘗試刪除未聯結之磁片磁碟機的聯結。</span><span class="sxs-lookup"><span data-stu-id="c87fa-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**錯誤 \_ 未 \_ SUBSTED**</span><span class="sxs-lookup"><span data-stu-id="c87fa-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-430">137 (0x89) </span><span class="sxs-lookup"><span data-stu-id="c87fa-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-431">系統嘗試刪除未替代之磁片磁碟機的替換。</span><span class="sxs-lookup"><span data-stu-id="c87fa-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**聯結 \_ 時發生 \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-433">138 (0x8A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-434">系統嘗試將磁片磁碟機加入聯結磁片磁碟機上的目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**\_將 SUBST 錯誤替代 \_ 為 \_ SUBST**</span><span class="sxs-lookup"><span data-stu-id="c87fa-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-436">139 (0x8B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-437">系統嘗試將磁片磁碟機替換成替代磁片磁碟機上的目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**\_將錯誤加入 \_ 至 \_ SUBST**</span><span class="sxs-lookup"><span data-stu-id="c87fa-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-439">140 (0x8C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-440">系統嘗試將磁片磁碟機加入替代磁片磁碟機上的目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**\_ \_ 要聯結的錯誤 SUBST \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-442">141 (0x8D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-443">系統嘗試將磁片磁碟機替代為已加入磁片磁碟機上的目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**錯誤 \_ 忙碌 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="c87fa-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-445">142 (0x8E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-446">系統目前無法執行聯結或 SUBST。</span><span class="sxs-lookup"><span data-stu-id="c87fa-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**錯誤 \_ 的 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="c87fa-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-448">143 (0x8F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-449">系統無法將磁片磁碟機加入或替代相同磁片磁碟機上的目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**錯誤 \_ 目錄 \_ 不是 \_ 根目錄**</span><span class="sxs-lookup"><span data-stu-id="c87fa-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-451">144 (0x90) </span><span class="sxs-lookup"><span data-stu-id="c87fa-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-452">目錄不是根目錄的子目錄。</span><span class="sxs-lookup"><span data-stu-id="c87fa-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**錯誤 \_ 目錄 \_ 不是 \_ 空的**</span><span class="sxs-lookup"><span data-stu-id="c87fa-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-454">145 (0x91) </span><span class="sxs-lookup"><span data-stu-id="c87fa-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-455">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="c87fa-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**錯誤 \_ 是 \_ SUBST \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="c87fa-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-457">146 (0x92) </span><span class="sxs-lookup"><span data-stu-id="c87fa-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-458">指定的路徑正在替代中使用。</span><span class="sxs-lookup"><span data-stu-id="c87fa-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**錯誤 \_ 為 \_ 聯結 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="c87fa-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-460">147 (0x93) </span><span class="sxs-lookup"><span data-stu-id="c87fa-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-461">沒有足夠的資源可用來處理此命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**錯誤 \_ 路徑 \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="c87fa-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-463">148 (0x94) </span><span class="sxs-lookup"><span data-stu-id="c87fa-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-464">目前無法使用指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="c87fa-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**錯誤 \_ 為 \_ SUBST \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="c87fa-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-466">149 (0x95) </span><span class="sxs-lookup"><span data-stu-id="c87fa-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-467">嘗試加入或取代磁片磁碟機上的目錄是先前替代目標的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c87fa-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**錯誤 \_ 系統 \_ 追蹤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-469">150 (0x96) </span><span class="sxs-lookup"><span data-stu-id="c87fa-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-470">未在 CONFIG.SYS 檔案中指定系統追蹤資訊，或不允許追蹤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**錯誤 \_ 不正確 \_ 事件 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="c87fa-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-472">151 (0x97) </span><span class="sxs-lookup"><span data-stu-id="c87fa-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-473">DosMuxSemWait 的指定訊號事件數目不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**錯誤 \_ 太 \_ 多 \_ MUXWAITERS**</span><span class="sxs-lookup"><span data-stu-id="c87fa-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-475">152 (0x98) </span><span class="sxs-lookup"><span data-stu-id="c87fa-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-476">DosMuxSemWait 未執行;已設定過多的信號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**錯誤 \_ \_ 清單 \_ 格式無效**</span><span class="sxs-lookup"><span data-stu-id="c87fa-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-478">153 (0x99) </span><span class="sxs-lookup"><span data-stu-id="c87fa-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-479">DosMuxSemWait 清單不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**錯誤 \_ 標籤 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="c87fa-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-481">154 (0x9A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-482">您輸入的磁片區標籤超過目的檔案系統的標籤字元限制。</span><span class="sxs-lookup"><span data-stu-id="c87fa-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**錯誤 \_ 太 \_ 多 \_ TCBS**</span><span class="sxs-lookup"><span data-stu-id="c87fa-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-484">155 (0x9B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-485">無法建立另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="c87fa-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**拒絕的錯誤 \_ 信號 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-487">156 (0x9C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-488">收件者進程拒絕了信號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**捨棄的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-490">157 (0x9D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-491">區段已經捨棄，無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="c87fa-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**錯誤 \_ 未 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="c87fa-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-493">158 (0x9E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-494">區段已經解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="c87fa-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**錯誤 \_ \_ THREADID \_ 位址錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-496">159 (0x9F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-497">執行緒識別碼的位址不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**錯誤 \_ 的 \_ 引數錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-499">160 (0xA0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-500">一或多個引數不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**錯誤 \_ \_ 路徑名稱錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-502">161 (0xA1) </span><span class="sxs-lookup"><span data-stu-id="c87fa-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-503">指定的路徑無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**錯誤 \_ 信號 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="c87fa-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-505">162 (0xA2) </span><span class="sxs-lookup"><span data-stu-id="c87fa-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-506">信號已暫止。</span><span class="sxs-lookup"><span data-stu-id="c87fa-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**已 \_ \_ 達到 THRDS 的錯誤最大值 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-508">164 (0xA4) </span><span class="sxs-lookup"><span data-stu-id="c87fa-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-509">無法在系統中建立其他執行緒。</span><span class="sxs-lookup"><span data-stu-id="c87fa-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**錯誤 \_ 鎖定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="c87fa-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-511">167 (0xA7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-512">無法鎖定檔案的區域。</span><span class="sxs-lookup"><span data-stu-id="c87fa-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**錯誤 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="c87fa-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-514">170 (0xAA) </span><span class="sxs-lookup"><span data-stu-id="c87fa-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-515">要求的資源正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**錯誤 \_ 裝置 \_ 支援 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="c87fa-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-517">171 (0xAB) </span><span class="sxs-lookup"><span data-stu-id="c87fa-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-518">裝置的命令支援偵測正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**錯誤 \_ 取消 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="c87fa-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-520">173 (0xAD) </span><span class="sxs-lookup"><span data-stu-id="c87fa-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-521">提供的取消區域沒有未處理的鎖定要求。</span><span class="sxs-lookup"><span data-stu-id="c87fa-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**\_ \_ \_ 不 \_ 支援錯誤的不可部分完成鎖定**</span><span class="sxs-lookup"><span data-stu-id="c87fa-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-523">174 (0xAE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-524">檔案系統不支援對鎖定類型進行不可部分完成的變更。</span><span class="sxs-lookup"><span data-stu-id="c87fa-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**錯誤 \_ 不正確 \_ 區段 \_ 編號**</span><span class="sxs-lookup"><span data-stu-id="c87fa-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-526">180 (0xB4) </span><span class="sxs-lookup"><span data-stu-id="c87fa-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-527">系統偵測到不正確的區段編號。</span><span class="sxs-lookup"><span data-stu-id="c87fa-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**錯誤 \_ 不正確 \_ 序數**</span><span class="sxs-lookup"><span data-stu-id="c87fa-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-529">182 (0xB6) </span><span class="sxs-lookup"><span data-stu-id="c87fa-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-530">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**錯誤 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="c87fa-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-532">183 (0xB7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-533">無法建立檔案，該檔案已存在。</span><span class="sxs-lookup"><span data-stu-id="c87fa-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**錯誤 \_ 不正確 \_ 旗標 \_ 編號**</span><span class="sxs-lookup"><span data-stu-id="c87fa-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-535">186 (0xBA) </span><span class="sxs-lookup"><span data-stu-id="c87fa-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-536">傳遞的旗標不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**\_ \_ 找不到錯誤 SEM \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-538">187 (0xBB) </span><span class="sxs-lookup"><span data-stu-id="c87fa-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-539">找不到指定的系統信號名稱。</span><span class="sxs-lookup"><span data-stu-id="c87fa-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**\_ \_ 啟動 \_ CODESEG 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-541">188 (0xBC) </span><span class="sxs-lookup"><span data-stu-id="c87fa-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-542">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**錯誤 \_ 無效 \_ STACKSEG**</span><span class="sxs-lookup"><span data-stu-id="c87fa-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-544">189 (0xBD) </span><span class="sxs-lookup"><span data-stu-id="c87fa-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-545">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**錯誤 \_ 不正確 \_ MODULETYPE**</span><span class="sxs-lookup"><span data-stu-id="c87fa-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-547">190 (0xBE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-548">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**錯誤 \_ 不正確 \_ EXE 簽 \_ 章**</span><span class="sxs-lookup"><span data-stu-id="c87fa-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-550">191 (0xBF) </span><span class="sxs-lookup"><span data-stu-id="c87fa-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-551">無法在 Win32 模式中執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**錯誤 \_ EXE \_ 標示為 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="c87fa-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-553">192 (0xC0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-554">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**錯誤 \_ 的 \_ EXE \_ 格式錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-556">193 (0xC1) </span><span class="sxs-lookup"><span data-stu-id="c87fa-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-557">%1 不是有效的 Win32 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**反復 \_ 資料的錯誤 \_ \_ 超過 \_ 64k**</span><span class="sxs-lookup"><span data-stu-id="c87fa-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-559">194 (0xC2) </span><span class="sxs-lookup"><span data-stu-id="c87fa-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-560">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**錯誤 \_ 無效 \_ MINALLOCSIZE**</span><span class="sxs-lookup"><span data-stu-id="c87fa-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-562">195 (0xC3) </span><span class="sxs-lookup"><span data-stu-id="c87fa-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-563">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**\_ \_ 從不正確 \_ \_ 環形 DYNLINK 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-565">196 (0xC4) </span><span class="sxs-lookup"><span data-stu-id="c87fa-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-566">作業系統無法執行此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**\_ \_ 未啟用錯誤 \_ IOPL**</span><span class="sxs-lookup"><span data-stu-id="c87fa-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-568">197 (0xC5) </span><span class="sxs-lookup"><span data-stu-id="c87fa-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-569">作業系統目前尚未設定為執行此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**錯誤 \_ 無效 \_ SEGDPL**</span><span class="sxs-lookup"><span data-stu-id="c87fa-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-571">198 (0xC6) </span><span class="sxs-lookup"><span data-stu-id="c87fa-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-572">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**錯誤 \_ AUTODATASEG \_ 超過 \_ 64k**</span><span class="sxs-lookup"><span data-stu-id="c87fa-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-574">199 (0xC7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-575">作業系統無法執行此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**錯誤 \_ RING2SEG \_ 必須 \_ \_ 可移動**</span><span class="sxs-lookup"><span data-stu-id="c87fa-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-577">200 (0xC8) </span><span class="sxs-lookup"><span data-stu-id="c87fa-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-578">程式碼片段不能大於或等於64K。</span><span class="sxs-lookup"><span data-stu-id="c87fa-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**\_RELOC \_ 鏈 \_ XEEDS \_ SEGLIM 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-580">201 (0xC9) </span><span class="sxs-lookup"><span data-stu-id="c87fa-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-581">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**\_ \_ \_ RELOC 鏈中的錯誤 INFLOOP \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-583">202 (元素 0xca) </span><span class="sxs-lookup"><span data-stu-id="c87fa-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-584">作業系統無法執行 %1。</span><span class="sxs-lookup"><span data-stu-id="c87fa-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**\_ \_ 找不到錯誤 ENVVAR \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-586">203 (0xCB) </span><span class="sxs-lookup"><span data-stu-id="c87fa-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-587">系統找不到所輸入的環境選項。</span><span class="sxs-lookup"><span data-stu-id="c87fa-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**錯誤 \_ 未 \_ \_ 傳送信號**</span><span class="sxs-lookup"><span data-stu-id="c87fa-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-589">205 (0xCD) </span><span class="sxs-lookup"><span data-stu-id="c87fa-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-590">命令子樹中沒有進程有信號處理常式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**錯誤 \_ 檔案名 \_ EXCED \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="c87fa-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-592">206 (0xCE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-593">檔案名或副檔名太長。</span><span class="sxs-lookup"><span data-stu-id="c87fa-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**\_RING2 \_ \_ 使用中堆疊 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-595">207 (0xCF) </span><span class="sxs-lookup"><span data-stu-id="c87fa-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-596">環形2堆疊正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**錯誤 \_ 中繼 \_ 擴充 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="c87fa-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-598">208 (0xD0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-599">通用檔案名字元 \* 或？的輸入不正確，或指定了太多的通用檔案名字元。</span><span class="sxs-lookup"><span data-stu-id="c87fa-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**錯誤 \_ 不正確 \_ 信號 \_ 號碼**</span><span class="sxs-lookup"><span data-stu-id="c87fa-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-601">209 (0xD1) </span><span class="sxs-lookup"><span data-stu-id="c87fa-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-602">張貼的信號不正確。</span><span class="sxs-lookup"><span data-stu-id="c87fa-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**錯誤 \_ 執行緒 \_ 1 \_ 非使用中**</span><span class="sxs-lookup"><span data-stu-id="c87fa-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-604">210 (0xD2) </span><span class="sxs-lookup"><span data-stu-id="c87fa-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-605">無法設定信號處理常式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**\_鎖定錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-607">212 (0xD4) </span><span class="sxs-lookup"><span data-stu-id="c87fa-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-608">區段已鎖定，無法重新配置。</span><span class="sxs-lookup"><span data-stu-id="c87fa-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**錯誤 \_ 太 \_ 多 \_ 模組**</span><span class="sxs-lookup"><span data-stu-id="c87fa-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-610">214 (0xD6) </span><span class="sxs-lookup"><span data-stu-id="c87fa-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-611">有太多動態連結模組附加到這個程式或動態連結模組。</span><span class="sxs-lookup"><span data-stu-id="c87fa-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_ \_ 不 \_ 允許錯誤的嵌套**</span><span class="sxs-lookup"><span data-stu-id="c87fa-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-613">215 (0xD7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-614">無法將呼叫嵌套至 LoadModule。</span><span class="sxs-lookup"><span data-stu-id="c87fa-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**錯誤 \_ EXE \_ 電腦 \_ 類型 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="c87fa-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-616">216 (0xD8) </span><span class="sxs-lookup"><span data-stu-id="c87fa-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-617">此版本的 %1 與您正在執行的 Windows 版本不相容。</span><span class="sxs-lookup"><span data-stu-id="c87fa-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="c87fa-618">檢查電腦的系統資訊，然後洽詢軟體發行者。</span><span class="sxs-lookup"><span data-stu-id="c87fa-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**錯誤 \_ EXE \_ 無法 \_ 修改 \_ 帶正負號的 \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="c87fa-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-620">217 (0xD9) </span><span class="sxs-lookup"><span data-stu-id="c87fa-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-621">影像檔案 %1 已簽署，無法修改。</span><span class="sxs-lookup"><span data-stu-id="c87fa-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**錯誤 \_ EXE \_ 無法 \_ 修改 \_ 強式 \_ 帶正負 \_ 號的二進位檔**</span><span class="sxs-lookup"><span data-stu-id="c87fa-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-623">218 (0xDA) </span><span class="sxs-lookup"><span data-stu-id="c87fa-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-624">影像檔案 %1 經過強式簽署，無法修改。</span><span class="sxs-lookup"><span data-stu-id="c87fa-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**錯誤 \_ 檔案 \_ 簽 \_ 出**</span><span class="sxs-lookup"><span data-stu-id="c87fa-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-626">220 (0xDC) </span><span class="sxs-lookup"><span data-stu-id="c87fa-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-627">此檔案已簽出或鎖定，可供其他使用者編輯。</span><span class="sxs-lookup"><span data-stu-id="c87fa-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_需要錯誤簽出 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-629">221 (0xDD) </span><span class="sxs-lookup"><span data-stu-id="c87fa-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-630">您必須先簽出檔案，然後再儲存變更。</span><span class="sxs-lookup"><span data-stu-id="c87fa-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**錯誤 \_ 錯誤 \_ 檔 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c87fa-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-632">222 (0xDE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-633">已封鎖要儲存或抓取的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="c87fa-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**錯誤 \_ 檔案 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="c87fa-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-635">223 (0xDF) </span><span class="sxs-lookup"><span data-stu-id="c87fa-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-636">檔案大小超過允許的限制，因此無法儲存。</span><span class="sxs-lookup"><span data-stu-id="c87fa-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_需要驗證錯誤表單 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-638">224 (0xE0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-639">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c87fa-639">Access Denied.</span></span> <span data-ttu-id="c87fa-640">在此位置開啟檔案之前，您必須先將網站新增至 [信任的網站] 清單、流覽至網站，然後選取要自動登入的選項。</span><span class="sxs-lookup"><span data-stu-id="c87fa-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**\_受病毒 \_ 感染的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-642">225 (0xE1) </span><span class="sxs-lookup"><span data-stu-id="c87fa-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-643">因為檔案包含病毒或潛在的垃圾軟體，所以操作未順利完成。</span><span class="sxs-lookup"><span data-stu-id="c87fa-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**\_已刪除病毒的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-645">226 (0xE2) </span><span class="sxs-lookup"><span data-stu-id="c87fa-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-646">此檔案包含病毒或潛在的垃圾軟體，無法開啟。</span><span class="sxs-lookup"><span data-stu-id="c87fa-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="c87fa-647">由於這種病毒或潛在的垃圾軟體的本質，檔案已從這個位置移除。</span><span class="sxs-lookup"><span data-stu-id="c87fa-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**錯誤 \_ 輸送 \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="c87fa-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-649">229 (0xE5) </span><span class="sxs-lookup"><span data-stu-id="c87fa-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-650">管道為本機。</span><span class="sxs-lookup"><span data-stu-id="c87fa-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**錯誤的 \_ 無效 \_ 管道**</span><span class="sxs-lookup"><span data-stu-id="c87fa-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-652">230 (0xE6) </span><span class="sxs-lookup"><span data-stu-id="c87fa-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-653">管道狀態無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**錯誤 \_ 管道 \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="c87fa-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-655">231 (0xE7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-656">所有管道實例都忙碌中。</span><span class="sxs-lookup"><span data-stu-id="c87fa-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**錯誤 \_ 的 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c87fa-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-658">232 (0xE8) </span><span class="sxs-lookup"><span data-stu-id="c87fa-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-659">正在關閉管道。</span><span class="sxs-lookup"><span data-stu-id="c87fa-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**錯誤 \_ 管道 \_ 未 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="c87fa-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-661">233 (0xE9) </span><span class="sxs-lookup"><span data-stu-id="c87fa-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-662">管道的另一端沒有進程。</span><span class="sxs-lookup"><span data-stu-id="c87fa-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**錯誤 \_ 的 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c87fa-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-664">234 (0xEA) </span><span class="sxs-lookup"><span data-stu-id="c87fa-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-665">有更多可用的資料。</span><span class="sxs-lookup"><span data-stu-id="c87fa-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**\_VC \_ 中斷連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-667">240 (0xF0) </span><span class="sxs-lookup"><span data-stu-id="c87fa-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-668">會話已取消。</span><span class="sxs-lookup"><span data-stu-id="c87fa-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**錯誤 \_ 不正確 \_ EA \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="c87fa-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-670">254 (0xFE) </span><span class="sxs-lookup"><span data-stu-id="c87fa-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-671">指定的擴充屬性名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**錯誤 \_ EA \_ 清單 \_ 不一致**</span><span class="sxs-lookup"><span data-stu-id="c87fa-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-673">255 (0xFF) </span><span class="sxs-lookup"><span data-stu-id="c87fa-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-674">擴充屬性不一致。</span><span class="sxs-lookup"><span data-stu-id="c87fa-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**等候 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="c87fa-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-676">258 (0x102) </span><span class="sxs-lookup"><span data-stu-id="c87fa-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-677">等候作業逾時。</span><span class="sxs-lookup"><span data-stu-id="c87fa-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_沒有 \_ 其他 \_ 專案的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-679">259 (0x103) </span><span class="sxs-lookup"><span data-stu-id="c87fa-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-680">沒有其他可用的資料。</span><span class="sxs-lookup"><span data-stu-id="c87fa-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_無法 \_ 複製錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="c87fa-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-683">無法使用複製函數。</span><span class="sxs-lookup"><span data-stu-id="c87fa-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**錯誤 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="c87fa-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="c87fa-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-686">目錄名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**錯誤 \_ EAS \_ 無法 \_ 適用**</span><span class="sxs-lookup"><span data-stu-id="c87fa-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="c87fa-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-689">擴充屬性不符合緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c87fa-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**錯誤 \_ EA \_ 檔案 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="c87fa-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="c87fa-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-692">裝載的檔案系統上的擴充屬性檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="c87fa-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**錯誤 \_ EA \_ 資料表已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="c87fa-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="c87fa-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-695">擴充屬性資料表檔案已滿。</span><span class="sxs-lookup"><span data-stu-id="c87fa-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**\_不正確 \_ EA \_ 控制碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="c87fa-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-698">指定的擴充屬性控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**\_ \_ 不 \_ 支援的錯誤 EAS**</span><span class="sxs-lookup"><span data-stu-id="c87fa-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="c87fa-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-701">裝載的檔案系統不支援擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="c87fa-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**錯誤 \_ 非 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="c87fa-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="c87fa-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-704">嘗試釋放不是由呼叫端所擁有的 mutex。</span><span class="sxs-lookup"><span data-stu-id="c87fa-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**錯誤 \_ 太 \_ 多 \_ 貼文**</span><span class="sxs-lookup"><span data-stu-id="c87fa-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="c87fa-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-707">對信號發出太多貼文。</span><span class="sxs-lookup"><span data-stu-id="c87fa-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**錯誤 \_ 部分 \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="c87fa-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="c87fa-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-710">只有部分的 ReadProcessMemory 或 WriteProcessMemory 要求已完成。</span><span class="sxs-lookup"><span data-stu-id="c87fa-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**\_ \_ 未 \_ 授與錯誤 OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="c87fa-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="c87fa-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-713">Oplock 要求遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c87fa-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**\_不正確 \_ OPLOCK \_ 通訊協定錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-715">301 (0x12D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-716">系統收到不正確 oplock 通知。</span><span class="sxs-lookup"><span data-stu-id="c87fa-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**錯誤 \_ 磁片 \_ 太過 \_ 分散**</span><span class="sxs-lookup"><span data-stu-id="c87fa-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="c87fa-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-719">磁片區太過分散，無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**\_刪除 \_ 暫止錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="c87fa-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-722">無法開啟檔案，因為正在刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="c87fa-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**\_ \_ 與 \_ 全域 \_ 簡短名稱登錄 \_ \_ \_ 設定不相容的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="c87fa-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-725">因為全域登錄設定的緣故，所以可能不會變更這個磁片區的簡短名稱設定。</span><span class="sxs-lookup"><span data-stu-id="c87fa-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_ \_ \_ 未 \_ \_ 在磁片區上啟用錯誤簡短名稱 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="c87fa-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-728">此磁片區未啟用簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="c87fa-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**錯誤 \_ 安全性 \_ 資料流程 \_ 不 \_ 一致**</span><span class="sxs-lookup"><span data-stu-id="c87fa-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="c87fa-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-731">指定磁片區的安全性資料流程處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="c87fa-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="c87fa-732">請在磁片區上執行 CHKDSK。</span><span class="sxs-lookup"><span data-stu-id="c87fa-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**\_不正確 \_ 鎖定 \_ 範圍錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="c87fa-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-735">因為不正確位元組範圍，所以無法處理要求的檔案鎖定作業。</span><span class="sxs-lookup"><span data-stu-id="c87fa-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**錯誤 \_ 映射 \_ 子系統 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="c87fa-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="c87fa-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-738">支援映射類型所需的子系統不存在。</span><span class="sxs-lookup"><span data-stu-id="c87fa-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**\_ \_ \_ 已定義錯誤通知 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="c87fa-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="c87fa-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-741">指定的檔案已經有與其相關聯的通知 GUID。</span><span class="sxs-lookup"><span data-stu-id="c87fa-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**錯誤 \_ 不正確 \_ 例外狀況 \_ 處理常式**</span><span class="sxs-lookup"><span data-stu-id="c87fa-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="c87fa-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-744">偵測到不正確例外狀況處理常式常式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**錯誤的 \_ 重複 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="c87fa-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="c87fa-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-747">為權杖指定了重複的許可權。</span><span class="sxs-lookup"><span data-stu-id="c87fa-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**錯誤 \_ 未 \_ 處理任何範圍 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="c87fa-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-750">無法處理指定操作的範圍。</span><span class="sxs-lookup"><span data-stu-id="c87fa-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**\_系統檔案不 \_ 允許錯誤 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="c87fa-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-753">不允許在檔案系統內部檔案上執行操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**錯誤 \_ 磁片 \_ 資源已 \_ 用盡**</span><span class="sxs-lookup"><span data-stu-id="c87fa-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-755">314 (0x13A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-756">此磁片的實體資源已用盡。</span><span class="sxs-lookup"><span data-stu-id="c87fa-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**錯誤 \_ 不正確 \_ 權杖**</span><span class="sxs-lookup"><span data-stu-id="c87fa-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="c87fa-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-759">代表資料的權杖無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**\_ \_ \_ 不支援的錯誤裝置功能 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="c87fa-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-762">裝置不支援命令功能。</span><span class="sxs-lookup"><span data-stu-id="c87fa-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**錯誤 \_ MR \_ 中間找 \_ 不 \_ 到**</span><span class="sxs-lookup"><span data-stu-id="c87fa-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="c87fa-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-765">系統在 %2 的訊息檔中找不到訊息編號 0x %1 的郵件內文。</span><span class="sxs-lookup"><span data-stu-id="c87fa-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ \_ 找不到錯誤範圍 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="c87fa-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-768">找不到指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="c87fa-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**錯誤 \_ 未定義 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="c87fa-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="c87fa-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-771">目的電腦上未定義指定的集中存取原則。</span><span class="sxs-lookup"><span data-stu-id="c87fa-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**錯誤 \_ 不正確 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="c87fa-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-773">320 (0x140) </span><span class="sxs-lookup"><span data-stu-id="c87fa-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-774">從 Active Directory 取得的集中存取原則無效。</span><span class="sxs-lookup"><span data-stu-id="c87fa-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**錯誤 \_ 裝置 \_ 無法連線**</span><span class="sxs-lookup"><span data-stu-id="c87fa-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="c87fa-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-777">無法連線到裝置。</span><span class="sxs-lookup"><span data-stu-id="c87fa-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**錯誤 \_ 裝置 \_ 沒有 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="c87fa-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="c87fa-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-780">目標裝置的資源不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**錯誤 \_ 資料總和 \_ 檢查碼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="c87fa-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-783">發生資料完整性總和檢查碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="c87fa-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="c87fa-784">檔案資料流程中的資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="c87fa-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**錯誤 \_ 混合的 \_ 核心 \_ EA \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="c87fa-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-786">324 (0x144) </span><span class="sxs-lookup"><span data-stu-id="c87fa-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-787">在相同的作業中，嘗試修改核心和一般擴充屬性 (EA) 。</span><span class="sxs-lookup"><span data-stu-id="c87fa-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤檔層級修剪**</span><span class="sxs-lookup"><span data-stu-id="c87fa-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-789">326 (0x146) </span><span class="sxs-lookup"><span data-stu-id="c87fa-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-790">裝置不支援檔案層級修剪。</span><span class="sxs-lookup"><span data-stu-id="c87fa-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**錯誤 \_ 位移 \_ 對齊 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="c87fa-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="c87fa-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-793">命令指定的資料位移與裝置的資料細微性/對齊方式不一致。</span><span class="sxs-lookup"><span data-stu-id="c87fa-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_ \_ \_ \_ 參數清單中的無效 \_ 欄位**</span><span class="sxs-lookup"><span data-stu-id="c87fa-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="c87fa-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-796">命令在其參數清單中指定了不正確欄位。</span><span class="sxs-lookup"><span data-stu-id="c87fa-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_ \_ \_ 正在進行錯誤作業**</span><span class="sxs-lookup"><span data-stu-id="c87fa-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-798">329 (0x149) </span><span class="sxs-lookup"><span data-stu-id="c87fa-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-799">目前正在與裝置進行操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**錯誤錯誤的 \_ \_ 裝置 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="c87fa-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-801">330 (0x14A) </span><span class="sxs-lookup"><span data-stu-id="c87fa-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-802">嘗試透過目標裝置的無效路徑來傳送命令。</span><span class="sxs-lookup"><span data-stu-id="c87fa-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**錯誤 \_ 太 \_ 多 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="c87fa-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-804">331 (0x14B) </span><span class="sxs-lookup"><span data-stu-id="c87fa-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-805">命令指定了超過裝置所支援之最大值的一些描述項。</span><span class="sxs-lookup"><span data-stu-id="c87fa-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**\_ \_ 停用清除資料的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-807">332 (0x14C) </span><span class="sxs-lookup"><span data-stu-id="c87fa-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-808">指定的檔案上已停用清除。</span><span class="sxs-lookup"><span data-stu-id="c87fa-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**錯誤 \_ 不是 \_ 重複的 \_ 儲存體**</span><span class="sxs-lookup"><span data-stu-id="c87fa-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-810">333 (0x14D) </span><span class="sxs-lookup"><span data-stu-id="c87fa-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-811">存放裝置不提供冗余。</span><span class="sxs-lookup"><span data-stu-id="c87fa-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_ \_ \_ 不支援錯誤的常駐檔 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-813">334 (0x14E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-814">常駐檔案不支援操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**\_ \_ \_ 不支援錯誤壓縮檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-816">335 (0x14F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-817">壓縮檔案不支援操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_ \_ 不支援錯誤 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="c87fa-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="c87fa-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-820">目錄不支援操作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**\_無法 \_ \_ 從複製讀取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c87fa-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="c87fa-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-823">無法讀取指定的要求資料複本。</span><span class="sxs-lookup"><span data-stu-id="c87fa-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**錯誤 \_ 失敗 \_ NOACTION \_ 重新開機**</span><span class="sxs-lookup"><span data-stu-id="c87fa-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-825">350 (0x15E) </span><span class="sxs-lookup"><span data-stu-id="c87fa-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-826">需要系統重新開機時，不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="c87fa-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**錯誤 \_ 失敗 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c87fa-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-828">351 (0x15F) </span><span class="sxs-lookup"><span data-stu-id="c87fa-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-829">關機操作失敗。</span><span class="sxs-lookup"><span data-stu-id="c87fa-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**錯誤 \_ \_ 重新開機失敗**</span><span class="sxs-lookup"><span data-stu-id="c87fa-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="c87fa-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-832">重新開機作業失敗。</span><span class="sxs-lookup"><span data-stu-id="c87fa-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**\_達到的 \_ 會話數上限 \_**</span><span class="sxs-lookup"><span data-stu-id="c87fa-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="c87fa-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-835">已達到會話的數目上限。</span><span class="sxs-lookup"><span data-stu-id="c87fa-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**錯誤 \_ 執行緒 \_ 模式 \_ 已經是 \_ 背景**</span><span class="sxs-lookup"><span data-stu-id="c87fa-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="c87fa-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-838">執行緒已處於背景處理模式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**錯誤 \_ 執行緒 \_ 模式 \_ 不是 \_ 背景**</span><span class="sxs-lookup"><span data-stu-id="c87fa-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="c87fa-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-841">執行緒不是處於背景處理模式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**錯誤 \_ 進程 \_ 模式 \_ 已經是 \_ 背景**</span><span class="sxs-lookup"><span data-stu-id="c87fa-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-843">402 (0x192) </span><span class="sxs-lookup"><span data-stu-id="c87fa-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-844">進程已經處於背景處理模式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**錯誤 \_ 進程 \_ 模式 \_ 不是 \_ 背景**</span><span class="sxs-lookup"><span data-stu-id="c87fa-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-846">403 (0x193) </span><span class="sxs-lookup"><span data-stu-id="c87fa-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-847">進程並非處於背景處理模式。</span><span class="sxs-lookup"><span data-stu-id="c87fa-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c87fa-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**錯誤 \_ 不正確 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="c87fa-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87fa-849">487 (0x1E7) </span><span class="sxs-lookup"><span data-stu-id="c87fa-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="c87fa-850">嘗試存取不正確位址。</span><span class="sxs-lookup"><span data-stu-id="c87fa-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="c87fa-851">規格需求</span><span class="sxs-lookup"><span data-stu-id="c87fa-851">Requirements</span></span>



| <span data-ttu-id="c87fa-852">需求</span><span class="sxs-lookup"><span data-stu-id="c87fa-852">Requirement</span></span> | <span data-ttu-id="c87fa-853">值</span><span class="sxs-lookup"><span data-stu-id="c87fa-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c87fa-854">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c87fa-854">Minimum supported client</span></span><br/> | <span data-ttu-id="c87fa-855">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c87fa-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c87fa-856">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c87fa-856">Minimum supported server</span></span><br/> | <span data-ttu-id="c87fa-857">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c87fa-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c87fa-858">標頭</span><span class="sxs-lookup"><span data-stu-id="c87fa-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87fa-859"><dt>Winerror.h (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c87fa-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87fa-860">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c87fa-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87fa-861">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c87fa-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




