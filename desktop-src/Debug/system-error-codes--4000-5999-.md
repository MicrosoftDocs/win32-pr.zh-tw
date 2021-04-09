---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼4000-5999，適用于開發人員。
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: '系統錯誤碼 (4000-5999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110776"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="569a3-103">系統錯誤碼 (4000-5999) </span><span class="sxs-lookup"><span data-stu-id="569a3-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="569a3-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="569a3-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="569a3-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="569a3-106">下列清單描述錯誤4000到5999的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="569a3-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="569a3-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="569a3-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="569a3-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="569a3-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="569a3-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**\_內部錯誤獲勝 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-110">4000 (0xFA0) </span><span class="sxs-lookup"><span data-stu-id="569a3-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-111">WINS 在處理命令時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**錯誤 \_ \_ 無法 \_ DEL 到 \_ 本機 \_ WINS**</span><span class="sxs-lookup"><span data-stu-id="569a3-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-113">4001 (0xFA1) </span><span class="sxs-lookup"><span data-stu-id="569a3-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-114">無法刪除本機 WINS。</span><span class="sxs-lookup"><span data-stu-id="569a3-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**\_靜態 \_ INIT 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-116">4002 (0xFA2) </span><span class="sxs-lookup"><span data-stu-id="569a3-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-117">從檔案匯入失敗。</span><span class="sxs-lookup"><span data-stu-id="569a3-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**錯誤 \_ INC. \_ 備份**</span><span class="sxs-lookup"><span data-stu-id="569a3-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-119">4003 (0xFA3) </span><span class="sxs-lookup"><span data-stu-id="569a3-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-120">備份失敗。</span><span class="sxs-lookup"><span data-stu-id="569a3-120">The backup failed.</span></span> <span data-ttu-id="569a3-121">是否已完成完整備份？</span><span class="sxs-lookup"><span data-stu-id="569a3-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_完整 \_ 備份時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-123">4004 (0xFA4) </span><span class="sxs-lookup"><span data-stu-id="569a3-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-124">備份失敗。</span><span class="sxs-lookup"><span data-stu-id="569a3-124">The backup failed.</span></span> <span data-ttu-id="569a3-125">檢查您要備份資料庫的目錄。</span><span class="sxs-lookup"><span data-stu-id="569a3-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**錯誤 \_ REC \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-127">4005 (0xFA5) </span><span class="sxs-lookup"><span data-stu-id="569a3-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-128">WINS 資料庫中不存在此名稱。</span><span class="sxs-lookup"><span data-stu-id="569a3-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**\_ \_ 不允許錯誤 \_ RPL**</span><span class="sxs-lookup"><span data-stu-id="569a3-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-130">4006 (0xFA6) </span><span class="sxs-lookup"><span data-stu-id="569a3-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-131">不允許使用 nonconfigured 夥伴進行複寫。</span><span class="sxs-lookup"><span data-stu-id="569a3-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**未 \_ 支援的 PEERDIST 錯誤 \_ CONTENTINFO \_ 版本 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-133">4050 (0xFD2) </span><span class="sxs-lookup"><span data-stu-id="569a3-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-134">不支援所提供的內容資訊版本。</span><span class="sxs-lookup"><span data-stu-id="569a3-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST \_ 錯誤 \_ 無法 \_ 剖析 \_ CONTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="569a3-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-136">4051 (0xFD3) </span><span class="sxs-lookup"><span data-stu-id="569a3-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-137">提供的內容資訊格式不正確。</span><span class="sxs-lookup"><span data-stu-id="569a3-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ 遺漏 \_ 資料的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-139">4052 (0xFD4) </span><span class="sxs-lookup"><span data-stu-id="569a3-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-140">在本機或對等快取中找不到要求的資料。</span><span class="sxs-lookup"><span data-stu-id="569a3-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_未發生 PEERDIST 錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-142">4053 (0xFD5) </span><span class="sxs-lookup"><span data-stu-id="569a3-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-143">沒有其他資料可供使用或不需要。</span><span class="sxs-lookup"><span data-stu-id="569a3-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_ \_ 未 \_ 初始化的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-145">4054 (0xFD6) </span><span class="sxs-lookup"><span data-stu-id="569a3-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-146">提供的物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="569a3-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_ \_ 已 \_ 初始化的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-148">4055 (0xFD7) </span><span class="sxs-lookup"><span data-stu-id="569a3-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-149">提供的物件已經初始化。</span><span class="sxs-lookup"><span data-stu-id="569a3-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ \_ 正在關閉 \_ 正在進行的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-151">4056 (0xFD8) </span><span class="sxs-lookup"><span data-stu-id="569a3-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-152">關機操作已在進行中。</span><span class="sxs-lookup"><span data-stu-id="569a3-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**已 \_ 不正確 PEERDIST 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-154">4057 (0xFD9) </span><span class="sxs-lookup"><span data-stu-id="569a3-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-155">提供的物件已經無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**\_ \_ 已存在 PEERDIST \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-157">4058 (0xFDA) </span><span class="sxs-lookup"><span data-stu-id="569a3-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-158">元素已經存在，且未被取代。</span><span class="sxs-lookup"><span data-stu-id="569a3-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST \_ 錯誤 \_ 作業 \_ NOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="569a3-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-160">4059 (0xFDB) </span><span class="sxs-lookup"><span data-stu-id="569a3-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-161">無法取消要求的作業，因為它已經完成。</span><span class="sxs-lookup"><span data-stu-id="569a3-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_ \_ 已 \_ 完成的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-163">4060 (0xFDC) </span><span class="sxs-lookup"><span data-stu-id="569a3-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-164">無法執行依照作業，因為已執行此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST \_ 錯誤 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="569a3-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-166">4061 (0xFDD) </span><span class="sxs-lookup"><span data-stu-id="569a3-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-167">作業存取的資料超出有效資料的範圍。</span><span class="sxs-lookup"><span data-stu-id="569a3-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_不支援的 PEERDIST 錯誤 \_ 版本 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-169">4062 (0xFDE) </span><span class="sxs-lookup"><span data-stu-id="569a3-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-170">不支援要求的版本。</span><span class="sxs-lookup"><span data-stu-id="569a3-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST \_ 錯誤 \_ 不正確設定 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-172">4063 (0xFDF) </span><span class="sxs-lookup"><span data-stu-id="569a3-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-173">設定值無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_ \_ 未 \_ 授權的 PEERDIST 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-175">4064 (0xFE0) </span><span class="sxs-lookup"><span data-stu-id="569a3-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-176">SKU 未獲授權。</span><span class="sxs-lookup"><span data-stu-id="569a3-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_ \_ 無法使用 PEERDIST 錯誤服務 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-178">4065 (0xFE1) </span><span class="sxs-lookup"><span data-stu-id="569a3-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-179">PeerDist 服務仍在初始化中，很快就會推出。</span><span class="sxs-lookup"><span data-stu-id="569a3-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST \_ 錯誤 \_ 信任 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-181">4066 (0xFE2) </span><span class="sxs-lookup"><span data-stu-id="569a3-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-182">因為最近的錯誤，所以會暫時封鎖與一或多部電腦的通訊。</span><span class="sxs-lookup"><span data-stu-id="569a3-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**\_DHCP \_ 位址 \_ 發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-184">4100 (0x1004) </span><span class="sxs-lookup"><span data-stu-id="569a3-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-185">DHCP 用戶端已取得網路上已在使用中的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="569a3-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="569a3-186">本機介面將會停用，直到 DHCP 用戶端可以取得新的位址為止。</span><span class="sxs-lookup"><span data-stu-id="569a3-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**\_ \_ \_ 找不到 WMI \_ GUID 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-188">4200 (0x1068) </span><span class="sxs-lookup"><span data-stu-id="569a3-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-189">傳遞的 GUID 未被 WMI 資料提供者辨識為有效。</span><span class="sxs-lookup"><span data-stu-id="569a3-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**\_ \_ \_ 找不到 WMI \_ 實例錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-191">4201 (0x1069) </span><span class="sxs-lookup"><span data-stu-id="569a3-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-192">傳遞的實例名稱無法被 WMI 資料提供者辨識為有效。</span><span class="sxs-lookup"><span data-stu-id="569a3-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**\_ \_ \_ 找不到 WMI \_ ITEMID 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-194">4202 (0x106A) </span><span class="sxs-lookup"><span data-stu-id="569a3-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-195">傳遞的資料項目識別碼無法被 WMI 資料提供者辨識為有效。</span><span class="sxs-lookup"><span data-stu-id="569a3-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**\_WMI \_ 再次嘗試 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-197">4203 (0x106B) </span><span class="sxs-lookup"><span data-stu-id="569a3-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-198">WMI 要求無法完成，應該重試。</span><span class="sxs-lookup"><span data-stu-id="569a3-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**\_ \_ \_ 找不到 WMI \_ DP 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-200">4204 (0x106C) </span><span class="sxs-lookup"><span data-stu-id="569a3-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-201">找不到 WMI 資料提供者。</span><span class="sxs-lookup"><span data-stu-id="569a3-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**\_WMI \_ 無法解析的 \_ 實例 \_ 參考錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-203">4205 (0x106D) </span><span class="sxs-lookup"><span data-stu-id="569a3-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-204">WMI 資料提供者參考尚未註冊的實例集。</span><span class="sxs-lookup"><span data-stu-id="569a3-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**\_WMI \_ 已 \_ 啟用的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-206">4206 (0x106E) </span><span class="sxs-lookup"><span data-stu-id="569a3-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-207">WMI 資料區塊或事件通知已經啟用。</span><span class="sxs-lookup"><span data-stu-id="569a3-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**\_WMI \_ GUID 已 \_ 中斷連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-209">4207 (0x106F) </span><span class="sxs-lookup"><span data-stu-id="569a3-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-210">WMI 資料區塊無法再使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**\_WMI \_ 伺服器 \_ 無法使用的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-212">4208 (0x1070) </span><span class="sxs-lookup"><span data-stu-id="569a3-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-213">WMI 資料服務無法使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**\_WMI \_ DP \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-215">4209 (0x1071) </span><span class="sxs-lookup"><span data-stu-id="569a3-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-216">WMI 資料提供者無法執行要求。</span><span class="sxs-lookup"><span data-stu-id="569a3-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**錯誤 \_ WMI \_ 不正確 \_ MOF**</span><span class="sxs-lookup"><span data-stu-id="569a3-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-218">4210 (0x1072) </span><span class="sxs-lookup"><span data-stu-id="569a3-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-219">WMI MOF 資訊無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**錯誤 \_ WMI \_ 不正確 \_ REGINFO**</span><span class="sxs-lookup"><span data-stu-id="569a3-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-221">4211 (0x1073) </span><span class="sxs-lookup"><span data-stu-id="569a3-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-222">WMI 註冊資訊無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**\_WMI \_ 已 \_ 停用的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-224">4212 (0x1074) </span><span class="sxs-lookup"><span data-stu-id="569a3-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-225">WMI 資料區塊或事件通知已停用。</span><span class="sxs-lookup"><span data-stu-id="569a3-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**\_WMI \_ 唯讀錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-227">4213 (0x1075) </span><span class="sxs-lookup"><span data-stu-id="569a3-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-228">WMI 資料項目目或資料區塊是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="569a3-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**\_WMI \_ 設定 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-230">4214 (0x1076) </span><span class="sxs-lookup"><span data-stu-id="569a3-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-231">無法變更 WMI 資料項目或資料區塊。</span><span class="sxs-lookup"><span data-stu-id="569a3-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**錯誤 \_ 不是 \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="569a3-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-233">4250 (0x109A) </span><span class="sxs-lookup"><span data-stu-id="569a3-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-234">這項作業只會在應用程式容器的內容中有效。</span><span class="sxs-lookup"><span data-stu-id="569a3-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**\_需要錯誤 APPCONTAINER \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-236">4251 (0x109B) </span><span class="sxs-lookup"><span data-stu-id="569a3-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-237">此應用程式只能在應用程式容器的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="569a3-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**\_ \_ \_ APPCONTAINER 中不支援的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-239">4252 (0x109C) </span><span class="sxs-lookup"><span data-stu-id="569a3-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-240">應用程式容器的內容中不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="569a3-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**錯誤 \_ 不正確 \_ 封裝 \_ SID \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="569a3-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-242">4253 (0x109D) </span><span class="sxs-lookup"><span data-stu-id="569a3-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-243">提供的 SID 長度不是應用程式容器 Sid 的有效長度。</span><span class="sxs-lookup"><span data-stu-id="569a3-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**錯誤 \_ 不正確 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="569a3-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-245">4300 (0x10CC) </span><span class="sxs-lookup"><span data-stu-id="569a3-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-246">媒體識別碼不代表有效的媒體。</span><span class="sxs-lookup"><span data-stu-id="569a3-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**錯誤 \_ 不正確連結 \_ 庫**</span><span class="sxs-lookup"><span data-stu-id="569a3-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-248">4301 (0x10CD) </span><span class="sxs-lookup"><span data-stu-id="569a3-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-249">程式庫識別碼不代表有效的程式庫。</span><span class="sxs-lookup"><span data-stu-id="569a3-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**錯誤 \_ 不正確 \_ 媒體 \_ 集區**</span><span class="sxs-lookup"><span data-stu-id="569a3-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-251">4302 (0x10CE) </span><span class="sxs-lookup"><span data-stu-id="569a3-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-252">媒體集區識別碼不代表有效的媒體集區。</span><span class="sxs-lookup"><span data-stu-id="569a3-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**錯誤 \_ 磁片磁碟機 \_ 媒體 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="569a3-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-254">4303 (0x10CF) </span><span class="sxs-lookup"><span data-stu-id="569a3-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-255">磁片磁碟機和媒體不相容或存在於不同的程式庫中。</span><span class="sxs-lookup"><span data-stu-id="569a3-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**錯誤 \_ 媒體 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="569a3-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-257">4304 (0x10D0) </span><span class="sxs-lookup"><span data-stu-id="569a3-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-258">媒體目前存在於離線文件庫中，且必須在線上，才能執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**錯誤連結 \_ 庫 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="569a3-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-260">4305 (0x10D1) </span><span class="sxs-lookup"><span data-stu-id="569a3-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-261">無法在離線程式庫上執行操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**錯誤 \_ 空白**</span><span class="sxs-lookup"><span data-stu-id="569a3-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-263">4306 (0x10D2) </span><span class="sxs-lookup"><span data-stu-id="569a3-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-264">媒體櫃、磁片磁碟機或媒體集區是空的。</span><span class="sxs-lookup"><span data-stu-id="569a3-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**錯誤 \_ 不是 \_ 空的**</span><span class="sxs-lookup"><span data-stu-id="569a3-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-266">4307 (0x10D3) </span><span class="sxs-lookup"><span data-stu-id="569a3-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-267">媒體櫃、磁片磁碟機或媒體集區必須是空的，才能執行這種操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**錯誤 \_ 媒體 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-269">4308 (0x10D4) </span><span class="sxs-lookup"><span data-stu-id="569a3-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-270">此媒體集區或媒體櫃中目前沒有可用的媒體。</span><span class="sxs-lookup"><span data-stu-id="569a3-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**錯誤 \_ 資源 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="569a3-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-272">4309 (0x10D5) </span><span class="sxs-lookup"><span data-stu-id="569a3-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-273">此操作所需的資源已停用。</span><span class="sxs-lookup"><span data-stu-id="569a3-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**\_不正確 \_ 清除程式錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-275">4310 (0x10D6) </span><span class="sxs-lookup"><span data-stu-id="569a3-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-276">媒體識別碼不代表有效的清除程式。</span><span class="sxs-lookup"><span data-stu-id="569a3-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**\_無法 \_ \_ 清除錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-278">4311 (0x10D7) </span><span class="sxs-lookup"><span data-stu-id="569a3-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-279">磁片磁碟機無法清理或不支援清除。</span><span class="sxs-lookup"><span data-stu-id="569a3-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_ \_ 找不到錯誤物件 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-281">4312 (0x10D8) </span><span class="sxs-lookup"><span data-stu-id="569a3-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-282">物件識別碼不代表有效的物件。</span><span class="sxs-lookup"><span data-stu-id="569a3-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**錯誤 \_ 資料庫 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-284">4313 (0x10D9) </span><span class="sxs-lookup"><span data-stu-id="569a3-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-285">無法讀取或寫入資料庫。</span><span class="sxs-lookup"><span data-stu-id="569a3-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_資料庫已 \_ 滿的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-287">4314 (0x10DA) </span><span class="sxs-lookup"><span data-stu-id="569a3-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-288">資料庫已滿。</span><span class="sxs-lookup"><span data-stu-id="569a3-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**錯誤 \_ 媒體 \_ 不相容**</span><span class="sxs-lookup"><span data-stu-id="569a3-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-290">4315 (0x10DB) </span><span class="sxs-lookup"><span data-stu-id="569a3-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-291">媒體與裝置或媒體集區不相容。</span><span class="sxs-lookup"><span data-stu-id="569a3-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**錯誤 \_ 資源 \_ 不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-293">4316 (0x10DC) </span><span class="sxs-lookup"><span data-stu-id="569a3-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-294">此操作所需的資源不存在。</span><span class="sxs-lookup"><span data-stu-id="569a3-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**錯誤 \_ 不正確作業 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-296">4317 (0x10DD) </span><span class="sxs-lookup"><span data-stu-id="569a3-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-297">作業識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**錯誤 \_ 媒體 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-299">4318 (0x10DE) </span><span class="sxs-lookup"><span data-stu-id="569a3-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-300">媒體未裝載或可供使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**錯誤 \_ 裝置 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-302">4319 (0x10DF) </span><span class="sxs-lookup"><span data-stu-id="569a3-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-303">裝置尚未準備好可供使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**拒絕的錯誤 \_ 要求 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-305">4320 (0x10E0) </span><span class="sxs-lookup"><span data-stu-id="569a3-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-306">操作員或系統管理員已拒絕要求。</span><span class="sxs-lookup"><span data-stu-id="569a3-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**錯誤 \_ 不正確 \_ 磁片磁碟機 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="569a3-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-308">4321 (0x10E1) </span><span class="sxs-lookup"><span data-stu-id="569a3-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-309">磁片磁碟機識別碼不代表有效的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="569a3-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**錯誤 \_ 庫已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="569a3-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-311">4322 (0x10E2) </span><span class="sxs-lookup"><span data-stu-id="569a3-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-312">程式庫已滿。</span><span class="sxs-lookup"><span data-stu-id="569a3-312">Library is full.</span></span> <span data-ttu-id="569a3-313">沒有可供使用的位置。</span><span class="sxs-lookup"><span data-stu-id="569a3-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**錯誤 \_ 媒體 \_ 無法 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="569a3-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-315">4323 (0x10E3) </span><span class="sxs-lookup"><span data-stu-id="569a3-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-316">傳輸無法存取媒體。</span><span class="sxs-lookup"><span data-stu-id="569a3-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**\_無法 \_ \_ 載入媒體的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-318">4324 (0x10E4) </span><span class="sxs-lookup"><span data-stu-id="569a3-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-319">無法將媒體載入磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="569a3-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="569a3-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-321">4325 (0x10E5) </span><span class="sxs-lookup"><span data-stu-id="569a3-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-322">無法取出磁片磁碟機狀態。</span><span class="sxs-lookup"><span data-stu-id="569a3-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 插槽**</span><span class="sxs-lookup"><span data-stu-id="569a3-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-324">4326 (0x10E6) </span><span class="sxs-lookup"><span data-stu-id="569a3-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-325">無法取出位置狀態。</span><span class="sxs-lookup"><span data-stu-id="569a3-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="569a3-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-327">4327 (0x10E7) </span><span class="sxs-lookup"><span data-stu-id="569a3-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-328">無法取得傳輸的狀態。</span><span class="sxs-lookup"><span data-stu-id="569a3-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**錯誤 \_ 傳輸已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="569a3-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-330">4328 (0x10E8) </span><span class="sxs-lookup"><span data-stu-id="569a3-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-331">無法使用傳輸，因為它已在使用中。</span><span class="sxs-lookup"><span data-stu-id="569a3-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**\_控制 \_ IEPORT 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-333">4329 (0x10E9) </span><span class="sxs-lookup"><span data-stu-id="569a3-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-334">無法開啟或關閉插入/退出埠。</span><span class="sxs-lookup"><span data-stu-id="569a3-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**錯誤 \_ 無法 \_ \_ 退出 \_ 裝載的 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="569a3-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-336">4330 (0x10EA) </span><span class="sxs-lookup"><span data-stu-id="569a3-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-337">無法退出媒體，因為它位於磁片磁碟機中。</span><span class="sxs-lookup"><span data-stu-id="569a3-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**錯誤 \_ 清除 \_ 插槽位置 \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="569a3-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-339">4331 (0x10EB) </span><span class="sxs-lookup"><span data-stu-id="569a3-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-340">清除的位置已被保留。</span><span class="sxs-lookup"><span data-stu-id="569a3-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**錯誤 \_ 清除 \_ 插槽 \_ 未 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="569a3-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-342">4332 (0x10EC) </span><span class="sxs-lookup"><span data-stu-id="569a3-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-343">不會保留簡潔的位置。</span><span class="sxs-lookup"><span data-stu-id="569a3-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**花費的錯誤 \_ 清除 \_ 磁帶 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-345">4333 (0x10ED) </span><span class="sxs-lookup"><span data-stu-id="569a3-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-346">清除卷匣已執行磁片磁碟機清洗次數的上限。</span><span class="sxs-lookup"><span data-stu-id="569a3-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**非 \_ 預期的錯誤 \_ OMID**</span><span class="sxs-lookup"><span data-stu-id="569a3-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-348">4334 (0x10EE) </span><span class="sxs-lookup"><span data-stu-id="569a3-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-349">非預期的中型識別碼。</span><span class="sxs-lookup"><span data-stu-id="569a3-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**無法 \_ \_ 刪除 \_ 最後一個 \_ 專案的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-351">4335 (0x10EF) </span><span class="sxs-lookup"><span data-stu-id="569a3-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-352">無法刪除此群組或資源中最後一個剩餘的專案。</span><span class="sxs-lookup"><span data-stu-id="569a3-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**錯誤 \_ 訊息 \_ 超過 \_ \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="569a3-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-354">4336 (0x10F0) </span><span class="sxs-lookup"><span data-stu-id="569a3-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-355">提供的訊息超過此參數允許的最大大小。</span><span class="sxs-lookup"><span data-stu-id="569a3-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**錯誤 \_ 磁片區 \_ 包含 \_ SYS \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="569a3-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-357">4337 (0x10F1) </span><span class="sxs-lookup"><span data-stu-id="569a3-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-358">磁片區包含系統或分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="569a3-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**錯誤 \_ INDIGENOUS \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="569a3-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-360">4338 (0x10F2) </span><span class="sxs-lookup"><span data-stu-id="569a3-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-361">媒體類型無法從此媒體櫃中移除，因為媒體櫃中至少有一個磁片磁碟機報告它可以支援此媒體類型。</span><span class="sxs-lookup"><span data-stu-id="569a3-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**錯誤， \_ 不 \_ 支援 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="569a3-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-363">4339 (0x10F3) </span><span class="sxs-lookup"><span data-stu-id="569a3-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-364">此離線媒體無法在此系統上掛接，因為沒有任何已啟用的磁片磁碟機存在，可供使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**\_已安裝錯誤清除程式 \_ 墨水匣 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-366">4340 (0x10F4) </span><span class="sxs-lookup"><span data-stu-id="569a3-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-367">磁帶媒體櫃中有一個整潔的墨水匣。</span><span class="sxs-lookup"><span data-stu-id="569a3-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**\_IEPORT \_ FULL 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-369">4341 (0x10F5) </span><span class="sxs-lookup"><span data-stu-id="569a3-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-370">無法使用插入/退出埠，因為它不是空的。</span><span class="sxs-lookup"><span data-stu-id="569a3-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**離線的錯誤 \_ 檔 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-372">4350 (0x10FE) </span><span class="sxs-lookup"><span data-stu-id="569a3-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-373">此檔案目前無法在這部電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**\_遠端 \_ 儲存體 \_ 未 \_ 啟用時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-375">4351 (0x10FF) </span><span class="sxs-lookup"><span data-stu-id="569a3-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-376">遠端儲存體服務目前無法運作。</span><span class="sxs-lookup"><span data-stu-id="569a3-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**\_遠端 \_ 存放裝置 \_ 媒體 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-378">4352 (0x1100) </span><span class="sxs-lookup"><span data-stu-id="569a3-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-379">遠端儲存體服務發生媒體錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**錯誤 \_ 不 \_ 是重新 \_ 分析 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="569a3-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-381">4390 (0x1126) </span><span class="sxs-lookup"><span data-stu-id="569a3-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-382">檔案或目錄不是重新分析點。</span><span class="sxs-lookup"><span data-stu-id="569a3-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**錯誤重新 \_ 分析 \_ 屬性 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="569a3-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-384">4391 (0x1127) </span><span class="sxs-lookup"><span data-stu-id="569a3-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-385">無法設定重新分析點屬性，因為它與現有的屬性衝突。</span><span class="sxs-lookup"><span data-stu-id="569a3-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**不正確重新 \_ \_ 分析 \_ 資料錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-387">4392 (0x1128) </span><span class="sxs-lookup"><span data-stu-id="569a3-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-388">重新分析點緩衝區中的資料無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**錯誤重新 \_ 分析 \_ 標記 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="569a3-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-390">4393 (0x1129) </span><span class="sxs-lookup"><span data-stu-id="569a3-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-391">重新分析點緩衝區中出現的標記無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**錯誤重新 \_ 分析 \_ 標記 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="569a3-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-393">4394 (0x112A) </span><span class="sxs-lookup"><span data-stu-id="569a3-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-394">要求中指定的標記和重新分析點中的標記不符。</span><span class="sxs-lookup"><span data-stu-id="569a3-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**\_ \_ \_ \_ 找不到應用程式資料錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-396">4400 (0x1130) </span><span class="sxs-lookup"><span data-stu-id="569a3-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-397">找不到快取資料。</span><span class="sxs-lookup"><span data-stu-id="569a3-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**\_應用程式 \_ 資料 \_ 過期時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-399">4401 (0x1131) </span><span class="sxs-lookup"><span data-stu-id="569a3-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-400">快取資料已過期。</span><span class="sxs-lookup"><span data-stu-id="569a3-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**\_應用程式 \_ 資料損毀錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-402">4402 (0x1132) </span><span class="sxs-lookup"><span data-stu-id="569a3-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-403">快取資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="569a3-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**超過錯誤的 \_ 應用程式 \_ 資料 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-405">4403 (0x1133) </span><span class="sxs-lookup"><span data-stu-id="569a3-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-406">快取資料已超過其大小上限，因此無法更新。</span><span class="sxs-lookup"><span data-stu-id="569a3-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**\_ \_ \_ 需要重新開機應用程式資料錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-408">4404 (0x1134) </span><span class="sxs-lookup"><span data-stu-id="569a3-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-409">快速快取已 ReArmed，需要重新開機，直到可以更新為止。</span><span class="sxs-lookup"><span data-stu-id="569a3-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**偵測 \_ 到錯誤的 SECUREBOOT \_ 復原 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-411">4420 (0x1144) </span><span class="sxs-lookup"><span data-stu-id="569a3-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-412">安全開機偵測到已嘗試回復受保護的資料。</span><span class="sxs-lookup"><span data-stu-id="569a3-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**錯誤的 \_ SECUREBOOT \_ 原則 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="569a3-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-414">4421 (0x1145) </span><span class="sxs-lookup"><span data-stu-id="569a3-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-415">此值會受到安全開機原則的保護，且無法修改或刪除。</span><span class="sxs-lookup"><span data-stu-id="569a3-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**錯誤的 \_ SECUREBOOT \_ 無效 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="569a3-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-417">4422 (0x1146) </span><span class="sxs-lookup"><span data-stu-id="569a3-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-418">安全開機原則無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤的 SECUREBOOT 原則發行者**</span><span class="sxs-lookup"><span data-stu-id="569a3-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-420">4423 (0x1147) </span><span class="sxs-lookup"><span data-stu-id="569a3-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-421">新的安全開機原則未在其更新清單中包含目前的發行者。</span><span class="sxs-lookup"><span data-stu-id="569a3-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**\_ \_ \_ 未簽署錯誤的 SECUREBOOT 原則 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-423">4424 (0x1148) </span><span class="sxs-lookup"><span data-stu-id="569a3-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-424">安全開機原則可能未簽署，或由不信任的簽署者簽署。</span><span class="sxs-lookup"><span data-stu-id="569a3-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**\_ \_ 未啟用錯誤 \_ SECUREBOOT**</span><span class="sxs-lookup"><span data-stu-id="569a3-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-426">4425 (0x1149) </span><span class="sxs-lookup"><span data-stu-id="569a3-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-427">未在這部電腦上啟用安全開機。</span><span class="sxs-lookup"><span data-stu-id="569a3-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**\_ \_ \_ 已取代錯誤的 SECUREBOOT 檔案**</span><span class="sxs-lookup"><span data-stu-id="569a3-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-429">4426 (0x114A) </span><span class="sxs-lookup"><span data-stu-id="569a3-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-430">安全開機需要某些檔案和驅動程式不會被其他檔案或驅動程式取代。</span><span class="sxs-lookup"><span data-stu-id="569a3-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**錯誤 \_ 卸載 \_ 讀取 \_ FLT \_ 不 \_ 受支援**</span><span class="sxs-lookup"><span data-stu-id="569a3-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-432">4440 (0x1158) </span><span class="sxs-lookup"><span data-stu-id="569a3-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-433">篩選不支援「複製卸載讀取」作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**\_ \_ \_ \_ 不支援錯誤卸載寫入 \_ FLT**</span><span class="sxs-lookup"><span data-stu-id="569a3-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-435">4441 (0x1159) </span><span class="sxs-lookup"><span data-stu-id="569a3-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-436">篩選不支援「複製卸載寫入」作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤卸載讀取檔**</span><span class="sxs-lookup"><span data-stu-id="569a3-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-438">4442 (0x115A) </span><span class="sxs-lookup"><span data-stu-id="569a3-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-439">檔案不支援複製卸載讀取操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤卸載寫入檔案**</span><span class="sxs-lookup"><span data-stu-id="569a3-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-441">4443 (0x115B) </span><span class="sxs-lookup"><span data-stu-id="569a3-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-442">檔案不支援複製卸載寫入操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**錯誤 \_ 磁片 \_ 區 \_ 未 \_ 啟用 SIS**</span><span class="sxs-lookup"><span data-stu-id="569a3-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-444">4500 (0x1194) </span><span class="sxs-lookup"><span data-stu-id="569a3-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-445">此磁片區上無法使用單一實例儲存體。</span><span class="sxs-lookup"><span data-stu-id="569a3-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_相依 \_ 資源 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-447">5001 (0x1389) </span><span class="sxs-lookup"><span data-stu-id="569a3-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-448">無法完成操作，因為其他資源相依于此資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_ \_ \_ 找不到錯誤相依性**</span><span class="sxs-lookup"><span data-stu-id="569a3-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-450">5002 (0x138A) </span><span class="sxs-lookup"><span data-stu-id="569a3-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-451">找不到叢集資源相依性。</span><span class="sxs-lookup"><span data-stu-id="569a3-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**錯誤相依性 \_ \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-453">5003 (0x138B) </span><span class="sxs-lookup"><span data-stu-id="569a3-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-454">無法使叢集資源相依于指定的資源，因為它已經相依。</span><span class="sxs-lookup"><span data-stu-id="569a3-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**錯誤 \_ 資源 \_ 未 \_ 上線**</span><span class="sxs-lookup"><span data-stu-id="569a3-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-456">5004 (0x138C) </span><span class="sxs-lookup"><span data-stu-id="569a3-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-457">叢集資源不在線上。</span><span class="sxs-lookup"><span data-stu-id="569a3-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**錯誤 \_ 主機 \_ 節點 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-459">5005 (0x138D) </span><span class="sxs-lookup"><span data-stu-id="569a3-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-460">此作業無法使用叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**錯誤 \_ 資源 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-462">5006 (0x138E) </span><span class="sxs-lookup"><span data-stu-id="569a3-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-463">叢集資源無法使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_ \_ 找不到錯誤資源 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-465">5007 (0x138F) </span><span class="sxs-lookup"><span data-stu-id="569a3-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-466">找不到叢集資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**錯誤 \_ 關閉 \_ 叢集**</span><span class="sxs-lookup"><span data-stu-id="569a3-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-468">5008 (0x1390) </span><span class="sxs-lookup"><span data-stu-id="569a3-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-469">正在關閉叢集。</span><span class="sxs-lookup"><span data-stu-id="569a3-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**錯誤 \_ 無法 \_ 收回 \_ 主動 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-471">5009 (0x1391) </span><span class="sxs-lookup"><span data-stu-id="569a3-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-472">除非節點已關閉或為最後一個節點，否則無法從叢集收回叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**錯誤 \_ 物件 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-474">5010 (0x1392) </span><span class="sxs-lookup"><span data-stu-id="569a3-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-475">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="569a3-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_ \_ 清單中的 ERROR 物件 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-477">5011 (0x1393) </span><span class="sxs-lookup"><span data-stu-id="569a3-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-478">此物件已經在清單中。</span><span class="sxs-lookup"><span data-stu-id="569a3-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**錯誤 \_ 群組 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-480">5012 (0x1394) </span><span class="sxs-lookup"><span data-stu-id="569a3-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-481">叢集群組無法供任何新的要求使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_ \_ 找不到錯誤群組 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-483">5013 (0x1395) </span><span class="sxs-lookup"><span data-stu-id="569a3-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-484">找不到叢集群組。</span><span class="sxs-lookup"><span data-stu-id="569a3-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**錯誤 \_ 群組 \_ 未 \_ 上線**</span><span class="sxs-lookup"><span data-stu-id="569a3-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-486">5014 (0x1396) </span><span class="sxs-lookup"><span data-stu-id="569a3-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-487">無法完成操作，因為叢集群組不在線上。</span><span class="sxs-lookup"><span data-stu-id="569a3-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**錯誤 \_ 主機 \_ 節點 \_ 不是 \_ 資源 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="569a3-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-489">5015 (0x1397) </span><span class="sxs-lookup"><span data-stu-id="569a3-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-490">作業失敗，因為指定的叢集節點不是資源的擁有者，或節點不是資源的可能擁有者。</span><span class="sxs-lookup"><span data-stu-id="569a3-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**錯誤 \_ 主機 \_ 節點 \_ 不是 \_ 群組 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="569a3-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-492">5016 (0x1398) </span><span class="sxs-lookup"><span data-stu-id="569a3-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-493">作業失敗，因為指定的叢集節點不是群組擁有者，或者節點不是可能的群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="569a3-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**錯誤 \_ RESMON \_ 建立 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-495">5017 (0x1399) </span><span class="sxs-lookup"><span data-stu-id="569a3-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-496">無法在指定的資源監視器中建立叢集資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**\_線上錯誤 \_ RESMON \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-498">5018 (0x139A) </span><span class="sxs-lookup"><span data-stu-id="569a3-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-499">資源監視器無法使叢集資源上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**\_線上錯誤資源 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-501">5019 (0x139B) </span><span class="sxs-lookup"><span data-stu-id="569a3-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-502">因為叢集資源已上線，所以無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**錯誤 \_ 仲裁 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="569a3-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-504">5020 (0x139C) </span><span class="sxs-lookup"><span data-stu-id="569a3-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-505">叢集資源無法刪除或離線，因為它是仲裁資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**錯誤 \_ 無法 \_ \_ 支援仲裁**</span><span class="sxs-lookup"><span data-stu-id="569a3-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-507">5021 (0x139D) </span><span class="sxs-lookup"><span data-stu-id="569a3-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-508">叢集無法使指定的資源成為仲裁資源，因為它不能成為仲裁資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**錯誤 \_ 叢集 \_ 關機 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-510">5022 (0x139E) </span><span class="sxs-lookup"><span data-stu-id="569a3-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-511">叢集軟體正在關機。</span><span class="sxs-lookup"><span data-stu-id="569a3-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**錯誤 \_ 不正確 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="569a3-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-513">5023 (0x139F) </span><span class="sxs-lookup"><span data-stu-id="569a3-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-514">群組或資源不是正確的狀態，無法執行所要求的作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**儲存的錯誤 \_ 資源 \_ 屬性 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-516">5024 (0x13A0) </span><span class="sxs-lookup"><span data-stu-id="569a3-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-517">這些屬性已儲存，但在下一次資源上線之前，所有變更都不會生效。</span><span class="sxs-lookup"><span data-stu-id="569a3-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**錯誤 \_ 不是 \_ 仲裁 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="569a3-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-519">5025 (0x13A1) </span><span class="sxs-lookup"><span data-stu-id="569a3-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-520">叢集無法使指定的資源成為仲裁資源，因為它不屬於共用儲存類別。</span><span class="sxs-lookup"><span data-stu-id="569a3-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**錯誤 \_ 核心 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="569a3-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-522">5026 (0x13A2) </span><span class="sxs-lookup"><span data-stu-id="569a3-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-523">無法刪除叢集資源，因為它是核心資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**錯誤 \_ 仲裁 \_ 資源 \_ 線上 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-525">5027 (0x13A3) </span><span class="sxs-lookup"><span data-stu-id="569a3-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-526">仲裁資源無法上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**錯誤 \_ QUORUMLOG \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-528">5028 (0x13A4) </span><span class="sxs-lookup"><span data-stu-id="569a3-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-529">無法成功建立或裝載仲裁記錄檔。</span><span class="sxs-lookup"><span data-stu-id="569a3-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**錯誤 \_ CLUSTERLOG 損毀 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-531">5029 (0x13A5) </span><span class="sxs-lookup"><span data-stu-id="569a3-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-532">叢集記錄檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="569a3-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**\_CLUSTERLOG \_ 記錄 \_ 超過 \_ MAXSIZE 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-534">5030 (0x13A6) </span><span class="sxs-lookup"><span data-stu-id="569a3-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-535">無法將記錄寫入叢集記錄檔，因為它超過大小上限。</span><span class="sxs-lookup"><span data-stu-id="569a3-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**錯誤 \_ CLUSTERLOG \_ 超過 \_ MAXSIZE**</span><span class="sxs-lookup"><span data-stu-id="569a3-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-537">5031 (0x13A7) </span><span class="sxs-lookup"><span data-stu-id="569a3-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-538">叢集記錄檔超過其大小上限。</span><span class="sxs-lookup"><span data-stu-id="569a3-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**錯誤 \_ CLUSTERLOG \_ \_ 找不 \_ 到 CHKPOINT**</span><span class="sxs-lookup"><span data-stu-id="569a3-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-540">5032 (0x13A8) </span><span class="sxs-lookup"><span data-stu-id="569a3-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-541">在叢集記錄檔中找不到檢查點記錄。</span><span class="sxs-lookup"><span data-stu-id="569a3-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**錯誤 \_ CLUSTERLOG \_ \_ \_ 空間不足**</span><span class="sxs-lookup"><span data-stu-id="569a3-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-543">5033 (0x13A9) </span><span class="sxs-lookup"><span data-stu-id="569a3-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-544">無法使用記錄所需的磁碟空間下限。</span><span class="sxs-lookup"><span data-stu-id="569a3-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**錯誤 \_ 仲裁 \_ 擁有者運作中 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-546">5034 (0x13AA) </span><span class="sxs-lookup"><span data-stu-id="569a3-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-547">叢集節點無法取得仲裁資源的控制權，因為資源是由另一個作用中節點所擁有。</span><span class="sxs-lookup"><span data-stu-id="569a3-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**錯誤 \_ 網路 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-549">5035 (0x13AB) </span><span class="sxs-lookup"><span data-stu-id="569a3-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-550">此作業無法使用叢集網路。</span><span class="sxs-lookup"><span data-stu-id="569a3-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**錯誤 \_ 節點 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="569a3-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-552">5036 (0x13AC) </span><span class="sxs-lookup"><span data-stu-id="569a3-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-553">此作業無法使用叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**\_ \_ \_ 無法使用所有節點 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-555">5037 (0x13AD) </span><span class="sxs-lookup"><span data-stu-id="569a3-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-556">所有叢集節點都必須在執行中，才能執行此操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**錯誤 \_ 資源 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-558">5038 (0x13AE) </span><span class="sxs-lookup"><span data-stu-id="569a3-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-559">叢集資源失敗。</span><span class="sxs-lookup"><span data-stu-id="569a3-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**錯誤 \_ 叢集 \_ 無效 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-561">5039 (0x13AF) </span><span class="sxs-lookup"><span data-stu-id="569a3-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-562">叢集節點無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**錯誤 \_ 叢集 \_ 節點 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-564">5040 (0x13B0) </span><span class="sxs-lookup"><span data-stu-id="569a3-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-565">叢集節點已存在。</span><span class="sxs-lookup"><span data-stu-id="569a3-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**錯誤 \_ 叢集 \_ 加入 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-567">5041 (0x13B1) </span><span class="sxs-lookup"><span data-stu-id="569a3-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-568">節點正在加入叢集的進程中。</span><span class="sxs-lookup"><span data-stu-id="569a3-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**\_ \_ \_ \_ 找不到錯誤叢集節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-570">5042 (0x13B2) </span><span class="sxs-lookup"><span data-stu-id="569a3-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-571">找不到叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤叢集本機節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-573">5043 (0x13B3) </span><span class="sxs-lookup"><span data-stu-id="569a3-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-574">找不到叢集本機節點資訊。</span><span class="sxs-lookup"><span data-stu-id="569a3-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**錯誤 \_ 叢集 \_ 網路 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-576">5044 (0x13B4) </span><span class="sxs-lookup"><span data-stu-id="569a3-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-577">叢集網路已存在。</span><span class="sxs-lookup"><span data-stu-id="569a3-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-579">5045 (0x13B5) </span><span class="sxs-lookup"><span data-stu-id="569a3-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-580">找不到叢集網路。</span><span class="sxs-lookup"><span data-stu-id="569a3-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**錯誤 \_ 叢集 \_ NETINTERFACE \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="569a3-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-582">5046 (0x13B6) </span><span class="sxs-lookup"><span data-stu-id="569a3-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-583">叢集網路介面已經存在。</span><span class="sxs-lookup"><span data-stu-id="569a3-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 NETINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="569a3-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-585">5047 (0x13B7) </span><span class="sxs-lookup"><span data-stu-id="569a3-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-586">找不到叢集網路介面。</span><span class="sxs-lookup"><span data-stu-id="569a3-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**錯誤叢集的 \_ \_ \_ 要求無效**</span><span class="sxs-lookup"><span data-stu-id="569a3-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-588">5048 (0x13B8) </span><span class="sxs-lookup"><span data-stu-id="569a3-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-589">此物件的叢集要求無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**錯誤 \_ 群集 \_ 不正確 \_ 網路 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="569a3-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-591">5049 (0x13B9) </span><span class="sxs-lookup"><span data-stu-id="569a3-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-592">叢集網路提供者無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**錯誤 \_ 叢集 \_ 節點 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="569a3-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-594">5050 (0x13BA) </span><span class="sxs-lookup"><span data-stu-id="569a3-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-595">叢集節點已關閉。</span><span class="sxs-lookup"><span data-stu-id="569a3-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**無法連線到錯誤叢集 \_ \_ 節點 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-597">5051 (0x13BB) </span><span class="sxs-lookup"><span data-stu-id="569a3-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-598">無法連線到叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**錯誤 \_ 叢集 \_ 節點 \_ 不是 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="569a3-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-600">5052 (0x13BC) </span><span class="sxs-lookup"><span data-stu-id="569a3-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-601">叢集節點不是叢集的成員。</span><span class="sxs-lookup"><span data-stu-id="569a3-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**錯誤 \_ 叢集 \_ 加入 \_ 未 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-603">5053 (0x13BD) </span><span class="sxs-lookup"><span data-stu-id="569a3-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-604">叢集聯結作業不在進行中。</span><span class="sxs-lookup"><span data-stu-id="569a3-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-606">5054 (0x13BE) </span><span class="sxs-lookup"><span data-stu-id="569a3-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-607">叢集網路無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**錯誤 \_ 叢集 \_ 節點 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="569a3-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-609">5056 (0x13C0) </span><span class="sxs-lookup"><span data-stu-id="569a3-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-610">叢集節點已啟動。</span><span class="sxs-lookup"><span data-stu-id="569a3-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_ \_ \_ 使用中的錯誤叢集 IPADDR \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-612">5057 (0x13C1) </span><span class="sxs-lookup"><span data-stu-id="569a3-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-613">叢集 IP 位址已在使用中。</span><span class="sxs-lookup"><span data-stu-id="569a3-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**錯誤 \_ 叢集 \_ 節點 \_ 未 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="569a3-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-615">5058 (0x13C2) </span><span class="sxs-lookup"><span data-stu-id="569a3-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-616">叢集節點未暫停。</span><span class="sxs-lookup"><span data-stu-id="569a3-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**錯誤 \_ 群集 \_ 沒有 \_ 安全性 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="569a3-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-618">5059 (0x13C3) </span><span class="sxs-lookup"><span data-stu-id="569a3-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-619">沒有任何可用的叢集安全性內容。</span><span class="sxs-lookup"><span data-stu-id="569a3-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**錯誤 \_ 叢集 \_ 網路 \_ 不是 \_ 內部**</span><span class="sxs-lookup"><span data-stu-id="569a3-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-621">5060 (0x13C4) </span><span class="sxs-lookup"><span data-stu-id="569a3-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-622">叢集網路未設定為進行內部叢集通訊。</span><span class="sxs-lookup"><span data-stu-id="569a3-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="569a3-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-624">5061 (0x13C5) </span><span class="sxs-lookup"><span data-stu-id="569a3-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-625">叢集節點已啟動。</span><span class="sxs-lookup"><span data-stu-id="569a3-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="569a3-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-627">5062 (0x13C6) </span><span class="sxs-lookup"><span data-stu-id="569a3-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-628">叢集節點已關閉。</span><span class="sxs-lookup"><span data-stu-id="569a3-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**錯誤 \_ 叢集 \_ 網路 \_ 已 \_ 上線**</span><span class="sxs-lookup"><span data-stu-id="569a3-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-630">5063 (0x13C7) </span><span class="sxs-lookup"><span data-stu-id="569a3-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-631">叢集網路已上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**錯誤 \_ 叢集 \_ 網路 \_ 已 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="569a3-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-633">5064 (0x13C8) </span><span class="sxs-lookup"><span data-stu-id="569a3-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-634">叢集網路已離線。</span><span class="sxs-lookup"><span data-stu-id="569a3-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="569a3-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-636">5065 (0x13C9) </span><span class="sxs-lookup"><span data-stu-id="569a3-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-637">叢集節點已經是叢集的成員。</span><span class="sxs-lookup"><span data-stu-id="569a3-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**錯誤 \_ 叢集 \_ 最後一個 \_ 內部 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-639">5066 (0x13CA) </span><span class="sxs-lookup"><span data-stu-id="569a3-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-640">叢集網路是唯一針對兩個或多個作用中叢集節點之間的內部叢集通訊設定的網路。</span><span class="sxs-lookup"><span data-stu-id="569a3-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="569a3-641">無法從網路中移除內部通訊功能。</span><span class="sxs-lookup"><span data-stu-id="569a3-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**錯誤 \_ 叢集 \_ 網路 \_ 有相依 \_ 項**</span><span class="sxs-lookup"><span data-stu-id="569a3-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-643">5067 (0x13CB) </span><span class="sxs-lookup"><span data-stu-id="569a3-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-644">一或多個叢集資源相依于網路，以提供服務給用戶端。</span><span class="sxs-lookup"><span data-stu-id="569a3-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="569a3-645">用戶端存取功能無法從網路中移除。</span><span class="sxs-lookup"><span data-stu-id="569a3-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**\_ \_ \_ 在 \_ 仲裁上發生錯誤的作業無效**</span><span class="sxs-lookup"><span data-stu-id="569a3-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-647">5068 (0x13CC) </span><span class="sxs-lookup"><span data-stu-id="569a3-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-648">這是仲裁資源，因此無法在叢集資源上執行此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="569a3-649">您可能不會讓仲裁資源離線，或修改其可能的擁有者清單。</span><span class="sxs-lookup"><span data-stu-id="569a3-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_ \_ 不 \_ 允許錯誤相依性**</span><span class="sxs-lookup"><span data-stu-id="569a3-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-651">5069 (0x13CD) </span><span class="sxs-lookup"><span data-stu-id="569a3-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-652">叢集仲裁資源不允許有任何相依性。</span><span class="sxs-lookup"><span data-stu-id="569a3-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**錯誤 \_ 叢集 \_ 節點已 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="569a3-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-654">5070 (0x13CE) </span><span class="sxs-lookup"><span data-stu-id="569a3-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-655">叢集節點已暫停。</span><span class="sxs-lookup"><span data-stu-id="569a3-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**錯誤 \_ 節點 \_ 無法 \_ 裝載 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="569a3-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-657">5071 (0x13CF) </span><span class="sxs-lookup"><span data-stu-id="569a3-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-658">叢集資源無法上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="569a3-659">擁有者節點無法執行此資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**錯誤 \_ 叢集 \_ 節點 \_ 未 \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="569a3-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-661">5072 (0x13D0) </span><span class="sxs-lookup"><span data-stu-id="569a3-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-662">叢集節點尚未準備好執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**關閉錯誤叢集 \_ \_ 節點 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-664">5073 (0x13D1) </span><span class="sxs-lookup"><span data-stu-id="569a3-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-665">叢集節點正在關閉。</span><span class="sxs-lookup"><span data-stu-id="569a3-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**錯誤 \_ 叢集 \_ 加入已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="569a3-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-667">5074 (0x13D2) </span><span class="sxs-lookup"><span data-stu-id="569a3-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-668">叢集聯結作業已中止。</span><span class="sxs-lookup"><span data-stu-id="569a3-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**錯誤叢集的 \_ \_ 版本不相容 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-670">5075 (0x13D3) </span><span class="sxs-lookup"><span data-stu-id="569a3-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-671">叢集聯結作業失敗，因為加入的節點和其贊助者之間的軟體版本不相容。</span><span class="sxs-lookup"><span data-stu-id="569a3-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**已 \_ \_ \_ \_ 超過資源的 \_ 錯誤叢集 MAXNUM**</span><span class="sxs-lookup"><span data-stu-id="569a3-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-673">5076 (0x13D4) </span><span class="sxs-lookup"><span data-stu-id="569a3-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-674">因為叢集已達可監視的資源數量限制，所以無法建立此資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**錯誤 \_ 叢集 \_ 系統 \_ 配置 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="569a3-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-676">5077 (0x13D5) </span><span class="sxs-lookup"><span data-stu-id="569a3-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-677">在叢集聯結或表單作業期間，系統組態已變更。</span><span class="sxs-lookup"><span data-stu-id="569a3-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="569a3-678">聯結或表單作業已中止。</span><span class="sxs-lookup"><span data-stu-id="569a3-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤叢集資源類型**</span><span class="sxs-lookup"><span data-stu-id="569a3-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-680">5078 (0x13D6) </span><span class="sxs-lookup"><span data-stu-id="569a3-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-681">找不到指定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="569a3-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**\_ \_ \_ 不 \_ 支援的錯誤叢集 AZUREMMBLOBCONTAINER.RESTYPE**</span><span class="sxs-lookup"><span data-stu-id="569a3-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-683">5079 (0x13D7) </span><span class="sxs-lookup"><span data-stu-id="569a3-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-684">指定的節點不支援此類型的資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="569a3-685">這可能是因為版本不一致或此節點上沒有資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="569a3-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 RESNAME**</span><span class="sxs-lookup"><span data-stu-id="569a3-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-687">5080 (0x13D8) </span><span class="sxs-lookup"><span data-stu-id="569a3-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-688">此資源 DLL 不支援指定的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="569a3-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="569a3-689">這可能是因為提供給資源 DLL 的錯誤 (或變更) 名稱所致。</span><span class="sxs-lookup"><span data-stu-id="569a3-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**錯誤 \_ 叢集 \_ 未 \_ 註冊任何 RPC \_ 套件 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-691">5081 (0x13D9) </span><span class="sxs-lookup"><span data-stu-id="569a3-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-692">無法向 RPC 伺服器註冊任何驗證套件。</span><span class="sxs-lookup"><span data-stu-id="569a3-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**錯誤 \_ 叢集 \_ 擁有者 \_ 不 \_ 在 \_ PREFLIST 中**</span><span class="sxs-lookup"><span data-stu-id="569a3-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-694">5082 (0x13DA) </span><span class="sxs-lookup"><span data-stu-id="569a3-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-695">因為群組的擁有者不在群組的慣用清單中，所以無法讓群組上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="569a3-696">若要變更群組的擁有者節點，請移動群組。</span><span class="sxs-lookup"><span data-stu-id="569a3-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ SEQMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="569a3-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-698">5083 (0x13DB) </span><span class="sxs-lookup"><span data-stu-id="569a3-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-699">聯結作業失敗，因為叢集資料庫序號已變更或與保險箱節點不相容。</span><span class="sxs-lookup"><span data-stu-id="569a3-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="569a3-700">如果叢集資料庫在聯結期間有所變更，則可能會在聯結作業期間發生此問題。</span><span class="sxs-lookup"><span data-stu-id="569a3-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**\_RESMON \_ 無效 \_ 狀態時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-702">5084 (0x13DC) </span><span class="sxs-lookup"><span data-stu-id="569a3-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-703">當資源處於目前狀態時，資源監視器將不允許執行失敗作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="569a3-704">如果資源處於暫止狀態，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="569a3-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**錯誤 \_ 叢集 \_ 黏 \_ 非 \_ 保險箱**</span><span class="sxs-lookup"><span data-stu-id="569a3-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-706">5085 (0x13DD) </span><span class="sxs-lookup"><span data-stu-id="569a3-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-707">非保險箱程式碼會要求保留鎖定以進行全域更新。</span><span class="sxs-lookup"><span data-stu-id="569a3-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_ \_ \_ \_ 找不到錯誤仲裁磁碟**</span><span class="sxs-lookup"><span data-stu-id="569a3-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-709">5086 (0x13DE) </span><span class="sxs-lookup"><span data-stu-id="569a3-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-710">叢集服務找不到仲裁磁碟。</span><span class="sxs-lookup"><span data-stu-id="569a3-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**錯誤 \_ 資料庫 \_ 備份 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="569a3-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-712">5087 (0x13DF) </span><span class="sxs-lookup"><span data-stu-id="569a3-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-713">備份的叢集資料庫可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="569a3-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已經 \_ 有 \_ DFS \_ 根目錄**</span><span class="sxs-lookup"><span data-stu-id="569a3-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-715">5088 (0x13E0) </span><span class="sxs-lookup"><span data-stu-id="569a3-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-716">DFS 根目錄已經存在於此叢集節點中。</span><span class="sxs-lookup"><span data-stu-id="569a3-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**錯誤 \_ 資源 \_ 屬性無法變更 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-718">5089 (0x13E1) </span><span class="sxs-lookup"><span data-stu-id="569a3-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-719">嘗試修改資源屬性失敗，因為它與另一個現有的屬性衝突。</span><span class="sxs-lookup"><span data-stu-id="569a3-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**錯誤 \_ 叢集 \_ 成員資格的 \_ \_ 狀態無效**</span><span class="sxs-lookup"><span data-stu-id="569a3-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-721">5890 (0x1702) </span><span class="sxs-lookup"><span data-stu-id="569a3-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-722">嘗試的操作與節點目前的成員資格狀態不相容。</span><span class="sxs-lookup"><span data-stu-id="569a3-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 QUORUMLOG**</span><span class="sxs-lookup"><span data-stu-id="569a3-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-724">5891 (0x1703) </span><span class="sxs-lookup"><span data-stu-id="569a3-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-725">仲裁資源不包含仲裁記錄。</span><span class="sxs-lookup"><span data-stu-id="569a3-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**錯誤 \_ 叢集 \_ 成員資格 \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="569a3-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-727">5892 (0x1704) </span><span class="sxs-lookup"><span data-stu-id="569a3-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-728">成員資格引擎要求關閉此節點上的叢集服務。</span><span class="sxs-lookup"><span data-stu-id="569a3-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**錯誤 \_ 叢集 \_ 實例 \_ 識別碼 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="569a3-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-730">5893 (0x1705) </span><span class="sxs-lookup"><span data-stu-id="569a3-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-731">聯結作業失敗，因為聯結節點的叢集實例識別碼與贊助商節點的叢集實例識別碼不相符。</span><span class="sxs-lookup"><span data-stu-id="569a3-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**\_ \_ \_ \_ 找不到 \_ \_ IP 的錯誤叢集網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-733">5894 (0x1706) </span><span class="sxs-lookup"><span data-stu-id="569a3-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-734">找不到指定 IP 位址的相符叢集網路。</span><span class="sxs-lookup"><span data-stu-id="569a3-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**錯誤 \_ 群集 \_ 屬性 \_ 資料 \_ 類型 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="569a3-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-736">5895 (0x1707) </span><span class="sxs-lookup"><span data-stu-id="569a3-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-737">屬性的實際資料類型不符合屬性的預期資料類型。</span><span class="sxs-lookup"><span data-stu-id="569a3-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**錯誤叢集在 \_ \_ \_ 沒有清除的情況下收回 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-739">5896 (0x1708) </span><span class="sxs-lookup"><span data-stu-id="569a3-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-740">已成功從叢集收回叢集節點，但節點未清除。</span><span class="sxs-lookup"><span data-stu-id="569a3-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="569a3-741">若要判斷哪些清除步驟失敗以及如何復原，請參閱使用事件檢視器的容錯移轉叢集應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="569a3-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**錯誤 \_ 叢集 \_ 參數 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="569a3-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-743">5897 (0x1709) </span><span class="sxs-lookup"><span data-stu-id="569a3-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-744">針對資源的屬性所指定的兩個或多個參數值發生衝突。</span><span class="sxs-lookup"><span data-stu-id="569a3-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**無法叢集化錯誤 \_ 節點 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-746">5898 (0x170A) </span><span class="sxs-lookup"><span data-stu-id="569a3-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-747">這部電腦不能成為叢集的成員。</span><span class="sxs-lookup"><span data-stu-id="569a3-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**錯誤叢集錯誤的 \_ \_ \_ 作業系統 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="569a3-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-749">5899 (0x170B) </span><span class="sxs-lookup"><span data-stu-id="569a3-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-750">因為這部電腦未安裝正確的 Windows 版本，所以無法成為叢集的成員。</span><span class="sxs-lookup"><span data-stu-id="569a3-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**錯誤叢集無法 \_ \_ \_ 建立 \_ DUP \_ 叢集 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="569a3-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-752">5900 (0x170C) </span><span class="sxs-lookup"><span data-stu-id="569a3-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-753">因為叢集名稱已在使用中，所以無法使用指定的叢集名稱來建立叢集。</span><span class="sxs-lookup"><span data-stu-id="569a3-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="569a3-754">為叢集指定不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="569a3-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**\_CLUSCFG \_ 已 \_ 認可的錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-756">5901 (0x170D) </span><span class="sxs-lookup"><span data-stu-id="569a3-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-757">已認可叢集設定動作。</span><span class="sxs-lookup"><span data-stu-id="569a3-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**錯誤 \_ CLUSCFG \_ 復原 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-759">5902 (0x170E) </span><span class="sxs-lookup"><span data-stu-id="569a3-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-760">叢集設定動作無法復原。</span><span class="sxs-lookup"><span data-stu-id="569a3-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**\_CLUSCFG \_ 系統 \_ 磁片 \_ 磁碟機 \_ 號 \_ 衝突時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-762">5903 (0x170F) </span><span class="sxs-lookup"><span data-stu-id="569a3-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-763">指派給一個節點上之系統磁片的磁碟機號，與指派給另一個節點上的磁片的磁碟機號衝突。</span><span class="sxs-lookup"><span data-stu-id="569a3-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**錯誤 \_ 叢集 \_ 舊 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="569a3-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-765">5904 (0x1710) </span><span class="sxs-lookup"><span data-stu-id="569a3-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-766">叢集中有一或多個節點正在執行的 Windows 版本不支援此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**錯誤叢集不相符的 \_ \_ \_ 電腦 \_ 帳戶 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="569a3-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-768">5905 (0x1711) </span><span class="sxs-lookup"><span data-stu-id="569a3-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-769">對應的電腦帳戶名稱與此資源的網路名稱不相符。</span><span class="sxs-lookup"><span data-stu-id="569a3-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**錯誤 \_ 叢集 \_ 沒有 \_ 網路 \_ 配接器**</span><span class="sxs-lookup"><span data-stu-id="569a3-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-771">5906 (0x1712) </span><span class="sxs-lookup"><span data-stu-id="569a3-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-772">沒有任何可用的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="569a3-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**錯誤 \_ 叢集 \_ 有害**</span><span class="sxs-lookup"><span data-stu-id="569a3-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-774">5907 (0x1713) </span><span class="sxs-lookup"><span data-stu-id="569a3-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-775">已有害叢集節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**錯誤 \_ 群集 \_ 群組 \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="569a3-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-777">5908 (0x1714) </span><span class="sxs-lookup"><span data-stu-id="569a3-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-778">群組無法接受要求，因為它正在移至另一個節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**錯誤 \_ 叢集 \_ 資源 \_ 類型 \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="569a3-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-780">5909 (0x1715) </span><span class="sxs-lookup"><span data-stu-id="569a3-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-781">資源類型無法接受要求，因為太忙碌，無法執行另一個作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**錯誤 \_ 資源 \_ 呼叫 \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-783">5910 (0x1716) </span><span class="sxs-lookup"><span data-stu-id="569a3-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-784">叢集資源 DLL 的呼叫已超時。</span><span class="sxs-lookup"><span data-stu-id="569a3-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**\_不正確 \_ 叢集 \_ IPV6 \_ 位址錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-786">5911 (0x1717) </span><span class="sxs-lookup"><span data-stu-id="569a3-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-787">位址對 IPv6 位址資源而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="569a3-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="569a3-788">需要全域 IPv6 位址，且必須符合叢集網路。</span><span class="sxs-lookup"><span data-stu-id="569a3-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="569a3-789">不允許相容性位址。</span><span class="sxs-lookup"><span data-stu-id="569a3-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**錯誤 \_ 叢集 \_ 內部 \_ 無效 \_ 函數**</span><span class="sxs-lookup"><span data-stu-id="569a3-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-791">5912 (0x1718) </span><span class="sxs-lookup"><span data-stu-id="569a3-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-792">發生內部叢集錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-792">An internal cluster error occurred.</span></span> <span data-ttu-id="569a3-793">嘗試呼叫不正確函式。</span><span class="sxs-lookup"><span data-stu-id="569a3-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**錯誤 \_ 叢集 \_ 參數 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="569a3-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-795">5913 (0x1719) </span><span class="sxs-lookup"><span data-stu-id="569a3-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-796">參數值超出可接受的範圍。</span><span class="sxs-lookup"><span data-stu-id="569a3-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**錯誤 \_ 群集 \_ 部分 \_ 傳送**</span><span class="sxs-lookup"><span data-stu-id="569a3-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-798">5914 (0x171A) </span><span class="sxs-lookup"><span data-stu-id="569a3-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-799">將資料傳送至叢集中的另一個節點時發生網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="569a3-800">傳送的位元組數目小於所需的數目。</span><span class="sxs-lookup"><span data-stu-id="569a3-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**錯誤叢集登錄 \_ \_ \_ 無效 \_ 函數**</span><span class="sxs-lookup"><span data-stu-id="569a3-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-802">5915 (0x171B) </span><span class="sxs-lookup"><span data-stu-id="569a3-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-803">嘗試的叢集登錄操作無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**錯誤 \_ 群集 \_ 不正確 \_ 字串 \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="569a3-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-805">5916 (0x171C) </span><span class="sxs-lookup"><span data-stu-id="569a3-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-806">未正確地結束字元的輸入字串。</span><span class="sxs-lookup"><span data-stu-id="569a3-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**錯誤 \_ 群集 \_ 不正確 \_ 字串 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="569a3-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-808">5917 (0x171D) </span><span class="sxs-lookup"><span data-stu-id="569a3-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-809">字元的輸入字串不是其所代表之資料的有效格式。</span><span class="sxs-lookup"><span data-stu-id="569a3-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ 交易 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-811">5918 (0x171E) </span><span class="sxs-lookup"><span data-stu-id="569a3-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-812">發生內部叢集錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-812">An internal cluster error occurred.</span></span> <span data-ttu-id="569a3-813">交易正在進行時，嘗試了叢集資料庫交易。</span><span class="sxs-lookup"><span data-stu-id="569a3-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ 交易 \_ 未 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-815">5919 (0x171F) </span><span class="sxs-lookup"><span data-stu-id="569a3-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-816">發生內部叢集錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-816">An internal cluster error occurred.</span></span> <span data-ttu-id="569a3-817">未進行交易時，嘗試認可叢集資料庫交易。</span><span class="sxs-lookup"><span data-stu-id="569a3-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**錯誤 \_ 叢集 \_ Null \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="569a3-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-819">5920 (0x1720) </span><span class="sxs-lookup"><span data-stu-id="569a3-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-820">發生內部叢集錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-820">An internal cluster error occurred.</span></span> <span data-ttu-id="569a3-821">資料未正確初始化。</span><span class="sxs-lookup"><span data-stu-id="569a3-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**錯誤 \_ 群集 \_ 部分 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="569a3-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-823">5921 (0x1721) </span><span class="sxs-lookup"><span data-stu-id="569a3-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-824">從資料流程讀取時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="569a3-825">傳回非預期的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="569a3-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**錯誤 \_ 群集 \_ 部分 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="569a3-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-827">5922 (0x1722) </span><span class="sxs-lookup"><span data-stu-id="569a3-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-828">寫入資料流程時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="569a3-829">無法寫入所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="569a3-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**錯誤叢集無法還原序列化 \_ \_ \_ \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="569a3-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-831">5923 (0x1723) </span><span class="sxs-lookup"><span data-stu-id="569a3-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-832">還原序列化叢集資料的資料流程時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="569a3-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**錯誤 \_ 相依的 \_ 資源 \_ 屬性 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="569a3-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-834">5924 (0x1724) </span><span class="sxs-lookup"><span data-stu-id="569a3-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-835">此資源的一或多個屬性值與其相依資源 (s) 相關聯的一或多個屬性值發生衝突。</span><span class="sxs-lookup"><span data-stu-id="569a3-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**錯誤 \_ 叢集 \_ 無 \_ 仲裁**</span><span class="sxs-lookup"><span data-stu-id="569a3-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-837">5925 (0x1725) </span><span class="sxs-lookup"><span data-stu-id="569a3-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-838">叢集節點的仲裁不存在以形成叢集。</span><span class="sxs-lookup"><span data-stu-id="569a3-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ IPV6 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-840">5926 (0x1726) </span><span class="sxs-lookup"><span data-stu-id="569a3-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-841">叢集網路對 IPv6 位址資源無效，或不符合設定的位址。</span><span class="sxs-lookup"><span data-stu-id="569a3-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ IPV6 通道 \_ \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="569a3-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-843">5927 (0x1727) </span><span class="sxs-lookup"><span data-stu-id="569a3-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-844">叢集網路對 IPv6 通道資源而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="569a3-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="569a3-845">檢查 IPv6 通道資源相依的 IP 位址資源設定。</span><span class="sxs-lookup"><span data-stu-id="569a3-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_ \_ \_ \_ \_ 此 \_ 群組中不允許有錯誤仲裁**</span><span class="sxs-lookup"><span data-stu-id="569a3-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-847">5928 (0x1728) </span><span class="sxs-lookup"><span data-stu-id="569a3-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-848">仲裁資源不能位於可用的儲存群組中。</span><span class="sxs-lookup"><span data-stu-id="569a3-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**錯誤相依性 \_ \_ 樹狀結構 \_ 太 \_ 複雜**</span><span class="sxs-lookup"><span data-stu-id="569a3-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-850">5929 (0x1729) </span><span class="sxs-lookup"><span data-stu-id="569a3-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-851">這項資源的相依性太深。</span><span class="sxs-lookup"><span data-stu-id="569a3-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_ \_ \_ 資源 \_ 呼叫中發生錯誤例外狀況**</span><span class="sxs-lookup"><span data-stu-id="569a3-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-853">5930 (0x172A) </span><span class="sxs-lookup"><span data-stu-id="569a3-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-854">呼叫資源 DLL 產生未處理的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="569a3-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**錯誤 \_ 叢集 \_ RHS \_ 無法 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="569a3-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-856">5931 (0x172B) </span><span class="sxs-lookup"><span data-stu-id="569a3-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-857">RHS 進程無法初始化。</span><span class="sxs-lookup"><span data-stu-id="569a3-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**\_ \_ 未 \_ 安裝錯誤叢集**</span><span class="sxs-lookup"><span data-stu-id="569a3-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-859">5932 (0x172C) </span><span class="sxs-lookup"><span data-stu-id="569a3-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-860">此節點上未安裝容錯移轉叢集功能。</span><span class="sxs-lookup"><span data-stu-id="569a3-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ \_ \_ \_ \_ \_ \_ 相同節點上的 \_ 錯誤叢集資源必須在線上**</span><span class="sxs-lookup"><span data-stu-id="569a3-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-862">5933 (0x172D) </span><span class="sxs-lookup"><span data-stu-id="569a3-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-863">此作業的資源必須在相同的節點上上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**叢集中的錯誤叢集 \_ \_ 節點數上限 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-865">5934 (0x172E) </span><span class="sxs-lookup"><span data-stu-id="569a3-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-866">無法加入新節點，因為此叢集已經是節點的最大數目。</span><span class="sxs-lookup"><span data-stu-id="569a3-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**錯誤 \_ 群集 \_ 太 \_ 多 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-868">5935 (0x172F) </span><span class="sxs-lookup"><span data-stu-id="569a3-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-869">因為指定的節點數目超過允許的上限，所以無法建立此叢集。</span><span class="sxs-lookup"><span data-stu-id="569a3-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**錯誤 \_ 叢集 \_ 物件 \_ 已 \_ 在使用中**</span><span class="sxs-lookup"><span data-stu-id="569a3-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-871">5936 (0x1730) </span><span class="sxs-lookup"><span data-stu-id="569a3-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-872">嘗試使用指定的叢集名稱失敗，因為網域中已有啟用的電腦物件具有指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="569a3-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**\_找到 NONCORE 的 \_ 群組 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-874">5937 (0x1731) </span><span class="sxs-lookup"><span data-stu-id="569a3-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-875">此叢集無法終結。</span><span class="sxs-lookup"><span data-stu-id="569a3-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="569a3-876">它具有非核心的應用程式群組，必須先刪除才能終結叢集。</span><span class="sxs-lookup"><span data-stu-id="569a3-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**錯誤 \_ 檔案 \_ 共用 \_ 資源 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="569a3-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-878">5938 (0x1732) </span><span class="sxs-lookup"><span data-stu-id="569a3-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-879">與檔案共用見證資源相關聯的檔案共用無法由此叢集或其任何節點裝載。</span><span class="sxs-lookup"><span data-stu-id="569a3-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**錯誤 \_ 叢集 \_ 收回 \_ 不正確 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="569a3-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-881">5939 (0x1733) </span><span class="sxs-lookup"><span data-stu-id="569a3-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-882">此節點的收回目前無效。</span><span class="sxs-lookup"><span data-stu-id="569a3-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="569a3-883">由於仲裁需求節點收回會導致叢集關閉。</span><span class="sxs-lookup"><span data-stu-id="569a3-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="569a3-884">如果是叢集中的最後一個節點，則應該使用終結叢集命令。</span><span class="sxs-lookup"><span data-stu-id="569a3-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**錯誤 \_ 叢集 \_ 單一 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="569a3-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-886">5940 (0x1734) </span><span class="sxs-lookup"><span data-stu-id="569a3-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-887">叢集中只允許此資源類型的一個實例。</span><span class="sxs-lookup"><span data-stu-id="569a3-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**錯誤 \_ 叢集 \_ 群組 \_ 單一 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="569a3-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-889">5941 (0x1735) </span><span class="sxs-lookup"><span data-stu-id="569a3-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-890">每個資源群組只允許此資源類型的一個實例。</span><span class="sxs-lookup"><span data-stu-id="569a3-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**錯誤 \_ 叢集 \_ 資源 \_ 提供者 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="569a3-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-892">5942 (0x1736) </span><span class="sxs-lookup"><span data-stu-id="569a3-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-893">因為一或多個提供者資源失敗，所以資源無法上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**錯誤 \_ 叢集 \_ 資源 \_ 設定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-895">5943 (0x1737) </span><span class="sxs-lookup"><span data-stu-id="569a3-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-896">資源表示它無法在任何節點上上線。</span><span class="sxs-lookup"><span data-stu-id="569a3-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**錯誤 \_ 叢集 \_ 群組 \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="569a3-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-898">5944 (0x1738) </span><span class="sxs-lookup"><span data-stu-id="569a3-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-899">目前無法在此群組上執行目前的操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**錯誤 \_ 叢集 \_ 非 \_ 共用 \_ 磁片區**</span><span class="sxs-lookup"><span data-stu-id="569a3-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-901">5945 (0x1739) </span><span class="sxs-lookup"><span data-stu-id="569a3-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-902">目錄或檔案不在叢集共用磁片區上。</span><span class="sxs-lookup"><span data-stu-id="569a3-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**錯誤 \_ 群集 \_ 不正確 \_ 安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="569a3-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-904">5946 (0x173A) </span><span class="sxs-lookup"><span data-stu-id="569a3-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-905">安全描述項不符合叢集的需求。</span><span class="sxs-lookup"><span data-stu-id="569a3-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ \_ \_ 使用中的錯誤叢集共用磁片區 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-907">5947 (0x173B) </span><span class="sxs-lookup"><span data-stu-id="569a3-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-908">叢集中已設定一或多個共用磁片區資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="569a3-909">這些資源必須移至可用的儲存體，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="569a3-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**錯誤 \_ 叢集 \_ 使用 \_ 共用 \_ 磁片區 \_ API**</span><span class="sxs-lookup"><span data-stu-id="569a3-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-911">5948 (0x173C) </span><span class="sxs-lookup"><span data-stu-id="569a3-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-912">無法直接操作此群組或資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="569a3-913">使用共用磁片區 Api 來執行所需的作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**錯誤 \_ 叢集 \_ 備份 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-915">5949 (0x173D) </span><span class="sxs-lookup"><span data-stu-id="569a3-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-916">備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="569a3-916">Back up is in progress.</span></span> <span data-ttu-id="569a3-917">請等候備份完成，然後再次嘗試此操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**錯誤 \_ 非 \_ CSV \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="569a3-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-919">5950 (0x173E) </span><span class="sxs-lookup"><span data-stu-id="569a3-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-920">路徑不屬於叢集共用磁片區。</span><span class="sxs-lookup"><span data-stu-id="569a3-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**錯誤 \_ CSV \_ 磁片區 \_ 不在 \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="569a3-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-922">5951 (0x173F) </span><span class="sxs-lookup"><span data-stu-id="569a3-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-923">叢集共用磁片區未在本機掛接在此節點上。</span><span class="sxs-lookup"><span data-stu-id="569a3-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**錯誤 \_ 叢集 \_ 監視程式 \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="569a3-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-925">5952 (0x1740) </span><span class="sxs-lookup"><span data-stu-id="569a3-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-926">叢集監視程式即將終止。</span><span class="sxs-lookup"><span data-stu-id="569a3-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**錯誤 \_ 叢集 \_ 資源被 \_ 否決 \_ 移動 \_ 不相容的 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="569a3-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-928">5953 (0x1741) </span><span class="sxs-lookup"><span data-stu-id="569a3-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-929">因為資源不相容，所以已拒絕在兩個節點之間移動。</span><span class="sxs-lookup"><span data-stu-id="569a3-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**錯誤 \_ 叢集 \_ \_ 節點 \_ 權數無效**</span><span class="sxs-lookup"><span data-stu-id="569a3-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-931">5954 (0x1742) </span><span class="sxs-lookup"><span data-stu-id="569a3-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-932">要求無效，因為當叢集處於僅限磁碟仲裁模式時，無法變更節點權數，或因為變更節點權數會違反最低叢集仲裁需求。</span><span class="sxs-lookup"><span data-stu-id="569a3-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**錯誤 \_ 叢集 \_ 資源被 \_ 否決 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="569a3-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-934">5955 (0x1743) </span><span class="sxs-lookup"><span data-stu-id="569a3-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-935">資源拒絕呼叫。</span><span class="sxs-lookup"><span data-stu-id="569a3-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**\_RESMON \_ 缺少系統 \_ 資源 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="569a3-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-937">5956 (0x1744) </span><span class="sxs-lookup"><span data-stu-id="569a3-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-938">資源無法啟動或執行，因為無法保留足夠的系統資源。</span><span class="sxs-lookup"><span data-stu-id="569a3-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**錯誤 \_ 叢集 \_ 資源 \_ 被 \_ 否決 \_ 移動 \_ \_ \_ 到目的地的資源不足 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-940">5957 (0x1745) </span><span class="sxs-lookup"><span data-stu-id="569a3-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-941">資源拒絕在兩個節點之間移動，因為目的地目前沒有足夠的資源可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**錯誤 \_ 叢集 \_ 資源 \_ 被 \_ 否決 \_ 的資源無法移至 \_ \_ \_ 來源上的資源不足 \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-943">5958 (0x1746) </span><span class="sxs-lookup"><span data-stu-id="569a3-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-944">資源拒絕在兩個節點之間移動，因為來源目前沒有足夠的資源可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**錯誤 \_ 叢集 \_ 群組已 \_ 排入佇列**</span><span class="sxs-lookup"><span data-stu-id="569a3-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-946">5959 (0x1747) </span><span class="sxs-lookup"><span data-stu-id="569a3-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-947">無法完成要求的作業，因為群組已排入作業佇列中。</span><span class="sxs-lookup"><span data-stu-id="569a3-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**錯誤 \_ 叢集 \_ 資源 \_ 鎖定 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="569a3-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-949">5960 (0x1748) </span><span class="sxs-lookup"><span data-stu-id="569a3-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-950">因為資源已鎖定狀態，所以無法完成要求的操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**\_ \_ 不允許錯誤叢集共用磁片區的 \_ \_ 容錯移轉 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569a3-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-952">5961 (0x1749) </span><span class="sxs-lookup"><span data-stu-id="569a3-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-953">資源無法移至另一個節點，因為叢集共用磁片區已拒絕此作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**錯誤 \_ 叢集 \_ 節點 \_ 清空 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-955">5962 (0x174A) </span><span class="sxs-lookup"><span data-stu-id="569a3-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-956">節點清空已在進行中。</span><span class="sxs-lookup"><span data-stu-id="569a3-956">A node drain is already in progress.</span></span>

<span data-ttu-id="569a3-957">此值也稱為 **錯誤叢集 \_ \_ 節點撤離 \_ 正在 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="569a3-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**錯誤 \_ 叢集 \_ 磁片 \_ 未 \_ 連線**</span><span class="sxs-lookup"><span data-stu-id="569a3-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-959">5963 (0x174B) </span><span class="sxs-lookup"><span data-stu-id="569a3-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-960">叢集儲存體未連接到節點。</span><span class="sxs-lookup"><span data-stu-id="569a3-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**錯誤 \_ 磁片 \_ 無法 \_ \_ 支援 CSV**</span><span class="sxs-lookup"><span data-stu-id="569a3-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-962">5964 (0x174C) </span><span class="sxs-lookup"><span data-stu-id="569a3-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-963">磁片未設定成搭配 CSV 使用。</span><span class="sxs-lookup"><span data-stu-id="569a3-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="569a3-964">CSV 磁片至少必須有一個以 NTFS 格式化的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="569a3-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**錯誤 \_ 資源 \_ 不 \_ 在 \_ 可用的 \_ 儲存體中**</span><span class="sxs-lookup"><span data-stu-id="569a3-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-966">5965 (0x174D) </span><span class="sxs-lookup"><span data-stu-id="569a3-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-967">資源必須是可用儲存群組的一部分，才能完成此動作。</span><span class="sxs-lookup"><span data-stu-id="569a3-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**錯誤 \_ 叢集 \_ 共用 \_ 磁片區重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="569a3-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-969">5966 (0x174E) </span><span class="sxs-lookup"><span data-stu-id="569a3-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-970">因為磁片區處於重新導向模式，所以 CSVFS 失敗的作業。</span><span class="sxs-lookup"><span data-stu-id="569a3-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**錯誤 \_ 叢集 \_ 共用 \_ 磁片區 \_ 未重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="569a3-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-972">5967 (0x174F) </span><span class="sxs-lookup"><span data-stu-id="569a3-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-973">CSVFS 失敗的作業，因為磁片區不在重新導向模式中。</span><span class="sxs-lookup"><span data-stu-id="569a3-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**錯誤 \_ 叢集 \_ 無法 \_ 傳回 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="569a3-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-975">5968 (0x1750) </span><span class="sxs-lookup"><span data-stu-id="569a3-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-976">目前無法傳回叢集屬性。</span><span class="sxs-lookup"><span data-stu-id="569a3-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**錯誤 \_ 叢集 \_ 資源 \_ 包含 \_ \_ \_ \_ \_ 共用 \_ 磁片區不支援的 DIFF 區域**</span><span class="sxs-lookup"><span data-stu-id="569a3-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-978">5969 (0x1751) </span><span class="sxs-lookup"><span data-stu-id="569a3-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-979">叢集磁片資源包含不支援叢集共用磁片區的軟體快照差異區域。</span><span class="sxs-lookup"><span data-stu-id="569a3-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**錯誤 \_ 叢集 \_ 資源 \_ 處於 \_ \_ 維護 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="569a3-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-981">5970 (0x1752) </span><span class="sxs-lookup"><span data-stu-id="569a3-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-982">無法完成操作，因為資源處於維護模式。</span><span class="sxs-lookup"><span data-stu-id="569a3-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**錯誤 \_ 叢集 \_ 親和性 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="569a3-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-984">5971 (0x1753) </span><span class="sxs-lookup"><span data-stu-id="569a3-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-985">因為叢集親和性衝突，所以無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="569a3-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**錯誤 \_ 叢集 \_ 資源 \_ 是 \_ 複本 \_ 虛擬 \_ 機**</span><span class="sxs-lookup"><span data-stu-id="569a3-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569a3-987">5972 (0x1754) </span><span class="sxs-lookup"><span data-stu-id="569a3-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="569a3-988">因為資源是複本虛擬機器，所以無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="569a3-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="569a3-989">規格需求</span><span class="sxs-lookup"><span data-stu-id="569a3-989">Requirements</span></span>



| <span data-ttu-id="569a3-990">需求</span><span class="sxs-lookup"><span data-stu-id="569a3-990">Requirement</span></span> | <span data-ttu-id="569a3-991">值</span><span class="sxs-lookup"><span data-stu-id="569a3-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="569a3-992">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="569a3-992">Minimum supported client</span></span><br/> | <span data-ttu-id="569a3-993">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="569a3-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="569a3-994">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="569a3-994">Minimum supported server</span></span><br/> | <span data-ttu-id="569a3-995">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="569a3-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="569a3-996">標頭</span><span class="sxs-lookup"><span data-stu-id="569a3-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="569a3-997"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="569a3-998">另請參閱</span><span class="sxs-lookup"><span data-stu-id="569a3-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569a3-999">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="569a3-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




