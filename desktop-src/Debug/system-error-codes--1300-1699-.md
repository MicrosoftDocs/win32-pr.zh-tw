---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1300-1699，適用于開發人員。
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: '系統錯誤碼 (1300-1699)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468245"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="56fa1-103">系統錯誤碼 (1300-1699) </span><span class="sxs-lookup"><span data-stu-id="56fa1-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="56fa1-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="56fa1-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="56fa1-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="56fa1-106">下列清單描述錯誤1300到1699的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="56fa1-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="56fa1-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="56fa1-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="56fa1-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="56fa1-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="56fa1-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**\_未 \_ 全部 \_ 指派的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="56fa1-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-111">並非所有被參考的許可權或群組都會指派給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="56fa1-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**\_部分 \_ 未 \_ 對應的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-113">1301 (0x515) </span><span class="sxs-lookup"><span data-stu-id="56fa1-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-114">帳戶名稱與安全性識別碼之間的部分對應尚未完成。</span><span class="sxs-lookup"><span data-stu-id="56fa1-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**\_沒有 \_ \_ 帳戶的配額 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="56fa1-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-117">未特別為此帳戶設定任何系統配額限制。</span><span class="sxs-lookup"><span data-stu-id="56fa1-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**\_本機 \_ 使用者 \_ 會話 \_ 金鑰錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="56fa1-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-120">沒有可用的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="56fa1-120">No encryption key is available.</span></span> <span data-ttu-id="56fa1-121">已傳回已知的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="56fa1-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**錯誤 \_ Null \_ LM \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="56fa1-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-124">密碼太複雜，無法轉換為 LAN Manager 密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="56fa1-125">傳回的 LAN Manager 密碼是 **Null** 字串。</span><span class="sxs-lookup"><span data-stu-id="56fa1-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**錯誤 \_ 不明 \_ 修訂**</span><span class="sxs-lookup"><span data-stu-id="56fa1-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="56fa1-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-128">修訂層級未知。</span><span class="sxs-lookup"><span data-stu-id="56fa1-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**錯誤 \_ 修訂 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="56fa1-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-131">表示兩個修訂層級不相容。</span><span class="sxs-lookup"><span data-stu-id="56fa1-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**錯誤 \_ 不正確 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="56fa1-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="56fa1-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-134">此安全識別碼可能不會被指派為此物件的擁有者。</span><span class="sxs-lookup"><span data-stu-id="56fa1-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**錯誤 \_ 不正確 \_ 主要 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="56fa1-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="56fa1-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-137">此安全識別碼可能不會被指派為物件的主要群組。</span><span class="sxs-lookup"><span data-stu-id="56fa1-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**錯誤 \_ 無 \_ 模擬 \_ 權杖**</span><span class="sxs-lookup"><span data-stu-id="56fa1-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="56fa1-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-140">嘗試透過目前未模擬用戶端的執行緒，對模擬權杖操作。</span><span class="sxs-lookup"><span data-stu-id="56fa1-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**錯誤 \_ 無法 \_ 停用 \_ 強制**</span><span class="sxs-lookup"><span data-stu-id="56fa1-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-143">群組可能未停用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**\_沒有 \_ 登入 \_ 伺服器的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="56fa1-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-146">目前沒有登入伺服器可用來服務登入要求。</span><span class="sxs-lookup"><span data-stu-id="56fa1-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**\_沒有 \_ 這類 \_ 登入 \_ 會話的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="56fa1-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-149">指定的登入工作階段不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-149">A specified logon session does not exist.</span></span> <span data-ttu-id="56fa1-150">它可能已經被終止。</span><span class="sxs-lookup"><span data-stu-id="56fa1-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**錯誤 \_ 沒有 \_ 這類 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="56fa1-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="56fa1-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-153">指定的許可權不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**\_ \_ 未保留錯誤 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="56fa1-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="56fa1-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-156">用戶端沒有必要的權限。</span><span class="sxs-lookup"><span data-stu-id="56fa1-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**錯誤 \_ 不正確 \_ 帳戶 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="56fa1-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-158">1315 (0x523) </span><span class="sxs-lookup"><span data-stu-id="56fa1-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-159">提供的名稱不是正確格式的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="56fa1-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**\_使用者 \_ 存在錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="56fa1-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-162">指定的帳戶已經存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**\_沒有 \_ 這類 \_ 使用者的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="56fa1-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-165">指定的帳號不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**錯誤 \_ 群組 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="56fa1-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-168">指定的群組已存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**錯誤 \_ 的 \_ \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="56fa1-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="56fa1-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-171">指定的群組不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_ \_ 群組中的錯誤成員 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="56fa1-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-174">指定的使用者帳戶已經是指定群組的成員，或無法刪除指定的群組，因為它包含成員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**錯誤 \_ 成員 \_ 不 \_ 在 \_ 群組中**</span><span class="sxs-lookup"><span data-stu-id="56fa1-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="56fa1-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-177">指定的使用者帳戶不是指定之群組帳戶的成員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**\_上次系統 \_ 管理員錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-180">不允許此作業，因為它可能會導致系統管理帳戶被停用、刪除或無法登入。</span><span class="sxs-lookup"><span data-stu-id="56fa1-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**錯誤 \_ 的 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="56fa1-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-183">無法更新密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-183">Unable to update the password.</span></span> <span data-ttu-id="56fa1-184">提供的值為目前的密碼不正確。</span><span class="sxs-lookup"><span data-stu-id="56fa1-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**\_格式錯誤 \_ 的 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="56fa1-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-187">無法更新密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-187">Unable to update the password.</span></span> <span data-ttu-id="56fa1-188">提供給新密碼的值包含密碼中不允許的值。</span><span class="sxs-lookup"><span data-stu-id="56fa1-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**錯誤 \_ 密碼 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="56fa1-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-190">1325 (0x52D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-191">無法更新密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-191">Unable to update the password.</span></span> <span data-ttu-id="56fa1-192">針對新密碼所提供的值不符合網域的長度、複雜度或歷程記錄需求。</span><span class="sxs-lookup"><span data-stu-id="56fa1-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**錯誤 \_ 登入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-195">使用者名稱或密碼不正確。</span><span class="sxs-lookup"><span data-stu-id="56fa1-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**錯誤 \_ 帳戶 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="56fa1-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="56fa1-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-198">帳戶限制導致此使用者無法登入。</span><span class="sxs-lookup"><span data-stu-id="56fa1-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="56fa1-199">例如：不允許空白密碼、登入時間有限，或已強制執行原則限制。</span><span class="sxs-lookup"><span data-stu-id="56fa1-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**錯誤 \_ 不正確 \_ 登入 \_ 時段**</span><span class="sxs-lookup"><span data-stu-id="56fa1-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-201">1328 (0x530) </span><span class="sxs-lookup"><span data-stu-id="56fa1-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-202">您的帳戶有時間限制，讓您無法立即登入。</span><span class="sxs-lookup"><span data-stu-id="56fa1-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**錯誤 \_ 不正確 \_ 工作站**</span><span class="sxs-lookup"><span data-stu-id="56fa1-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="56fa1-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-205">此使用者不允許登入這部電腦。</span><span class="sxs-lookup"><span data-stu-id="56fa1-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**錯誤 \_ 密碼已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="56fa1-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-207">1330 (0x532) </span><span class="sxs-lookup"><span data-stu-id="56fa1-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-208">此帳戶的密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="56fa1-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**錯誤 \_ 帳戶 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="56fa1-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-210">1331 (0x533) </span><span class="sxs-lookup"><span data-stu-id="56fa1-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-211">此使用者無法登入，因為此帳戶目前已停用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**\_未 \_ 對應的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-213">1332 (0x534) </span><span class="sxs-lookup"><span data-stu-id="56fa1-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-214">帳戶名稱與安全識別碼之間沒有對應。</span><span class="sxs-lookup"><span data-stu-id="56fa1-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**\_ \_ \_ LUID 要求的錯誤太多 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="56fa1-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-217"> (Luid) 一次要求的本機使用者識別碼太多。</span><span class="sxs-lookup"><span data-stu-id="56fa1-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**錯誤 \_ LUID 已 \_ 用盡**</span><span class="sxs-lookup"><span data-stu-id="56fa1-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="56fa1-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-220">沒有 (Luid) 可用的本機使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**錯誤 \_ 不正確 \_ 子 \_ 授權單位**</span><span class="sxs-lookup"><span data-stu-id="56fa1-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-222">1335 (0x537) </span><span class="sxs-lookup"><span data-stu-id="56fa1-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-223">安全識別碼的 subauthority 部分對於此特定用途無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**錯誤 \_ 不正確 \_ ACL**</span><span class="sxs-lookup"><span data-stu-id="56fa1-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="56fa1-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-226">ACL) 結構 (的存取控制清單無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**錯誤 \_ 不正確 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="56fa1-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="56fa1-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-229">安全性識別碼結構無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**錯誤 \_ 不正確 \_ 安全性 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="56fa1-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-232">安全描述項結構無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**錯誤 \_ 的 \_ 繼承 \_ ACL 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-234">1340 (0x53C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-235">無法建立繼承的存取控制清單 (ACL) 或存取控制專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="56fa1-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**錯誤 \_ 伺服器 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="56fa1-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="56fa1-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-238">伺服器目前已停用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**錯誤 \_ 伺服器 \_ 未 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="56fa1-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-241">伺服器目前已啟用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**錯誤 \_ 不正確 \_ 識別碼 \_ 授權單位**</span><span class="sxs-lookup"><span data-stu-id="56fa1-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="56fa1-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-244">提供的值對識別碼授權單位而言是無效值。</span><span class="sxs-lookup"><span data-stu-id="56fa1-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_超過錯誤分配 \_ 空間 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="56fa1-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-247">沒有更多可用的記憶體可進行安全性資訊更新。</span><span class="sxs-lookup"><span data-stu-id="56fa1-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**錯誤 \_ 不正確 \_ 群組 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="56fa1-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="56fa1-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-250">指定的屬性無效，或與整個群組的屬性不相容。</span><span class="sxs-lookup"><span data-stu-id="56fa1-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**錯誤的模擬 \_ \_ \_ 層級錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="56fa1-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-253">未提供所要求的模擬層，或所提供的模擬層不正確。</span><span class="sxs-lookup"><span data-stu-id="56fa1-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**錯誤 \_ 無法 \_ 開啟 \_ 匿名**</span><span class="sxs-lookup"><span data-stu-id="56fa1-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="56fa1-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-256">無法開啟匿名層級安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="56fa1-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**錯誤 \_ 的 \_ 驗證 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="56fa1-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="56fa1-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-259">要求的驗證資訊類別無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**錯誤錯誤的 \_ \_ 標記 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="56fa1-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="56fa1-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-262">權杖的類型不適用於其嘗試的使用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**\_沒有 \_ \_ 物件的安全性 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="56fa1-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-265">無法在沒有相關聯安全性的物件上執行安全性操作。</span><span class="sxs-lookup"><span data-stu-id="56fa1-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**無法 \_ \_ 存取 \_ 網域 \_ 資訊時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="56fa1-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-268">無法從網域控制站讀取設定資訊，可能是因為電腦無法使用，或存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="56fa1-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**錯誤 \_ 不正確 \_ 伺服器 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="56fa1-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="56fa1-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-271">安全性帳戶管理員 (SAM) 或本地安全機構 (LSA) 伺服器的狀態不正確，無法執行安全性作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**錯誤 \_ 不正確 \_ 網域 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="56fa1-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="56fa1-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-274">網域的狀態不正確，無法執行安全性作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**錯誤 \_ 不正確 \_ 網域 \_ 角色**</span><span class="sxs-lookup"><span data-stu-id="56fa1-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-277">這項作業只允許用於網域的主域控制站。</span><span class="sxs-lookup"><span data-stu-id="56fa1-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**\_沒有 \_ 這類 \_ 網域的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-279">1355 (0x54B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-280">指定的網域可能不存在或無法連絡。</span><span class="sxs-lookup"><span data-stu-id="56fa1-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**錯誤 \_ 網域 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="56fa1-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-283">指定的網域已經存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_超過錯誤網域 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-285">1357 (0x54D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-286">嘗試超過每一伺服器的網域數目上限。</span><span class="sxs-lookup"><span data-stu-id="56fa1-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**\_內部 \_ 資料庫 \_ 損毀錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-288">1358 (0x54E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-289">無法完成要求的操作，因為磁片上發生重大媒體失敗或資料結構損毀。</span><span class="sxs-lookup"><span data-stu-id="56fa1-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**錯誤 \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-291">1359 (0x54F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-292">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**錯誤 \_ 泛型 \_ 未 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="56fa1-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-294">1360 (0x550) </span><span class="sxs-lookup"><span data-stu-id="56fa1-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-295">一般存取類型包含在應該已經對應到非泛型型別的存取遮罩中。</span><span class="sxs-lookup"><span data-stu-id="56fa1-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**錯誤 \_ \_ 描述項 \_ 格式錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-297">1361 (0x551) </span><span class="sxs-lookup"><span data-stu-id="56fa1-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-298">安全描述項的格式不正確 (絕對或自我相對) 。</span><span class="sxs-lookup"><span data-stu-id="56fa1-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**錯誤 \_ 未 \_ 登入 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="56fa1-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-300">1362 (0x552) </span><span class="sxs-lookup"><span data-stu-id="56fa1-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-301">要求的動作僅限登入處理常式使用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="56fa1-302">呼叫進程尚未註冊為登入程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**錯誤 \_ 登入 \_ 會話 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-304">1363 (0x553) </span><span class="sxs-lookup"><span data-stu-id="56fa1-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-305">無法以已在使用中的識別碼啟動新的登入會話。</span><span class="sxs-lookup"><span data-stu-id="56fa1-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**錯誤 \_ 沒有 \_ 這類 \_ 套件**</span><span class="sxs-lookup"><span data-stu-id="56fa1-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-307">1364 (0x554) </span><span class="sxs-lookup"><span data-stu-id="56fa1-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-308">指定的驗證封裝未知。</span><span class="sxs-lookup"><span data-stu-id="56fa1-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**錯誤 \_ 的 \_ 登入 \_ 會話 \_ 狀態錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-310">1365 (0x555) </span><span class="sxs-lookup"><span data-stu-id="56fa1-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-311">登入會話的狀態與要求的作業不一致。</span><span class="sxs-lookup"><span data-stu-id="56fa1-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**錯誤 \_ 登入 \_ 會話 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="56fa1-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-313">1366 (0x556) </span><span class="sxs-lookup"><span data-stu-id="56fa1-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-314">登入會話識別碼已在使用中。</span><span class="sxs-lookup"><span data-stu-id="56fa1-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**錯誤 \_ 不正確 \_ 登入 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="56fa1-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-316">1367 (0x557) </span><span class="sxs-lookup"><span data-stu-id="56fa1-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-317">登入要求包含不正確登入類型值。</span><span class="sxs-lookup"><span data-stu-id="56fa1-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**錯誤 \_ 無法 \_ 模擬**</span><span class="sxs-lookup"><span data-stu-id="56fa1-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="56fa1-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-320">除非已從該管道讀取資料，否則無法使用具名管道進行模擬。</span><span class="sxs-lookup"><span data-stu-id="56fa1-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**\_RXACT \_ 無效 \_ 狀態時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-322">1369 (0x559) </span><span class="sxs-lookup"><span data-stu-id="56fa1-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-323">登錄子樹的交易狀態與要求的作業不相容。</span><span class="sxs-lookup"><span data-stu-id="56fa1-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**\_RXACT \_ 認可 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-325">1370 (0x55A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-326">發生內部安全性資料庫損毀。</span><span class="sxs-lookup"><span data-stu-id="56fa1-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**錯誤 \_ 特殊 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="56fa1-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-328">1371 (0x55B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-329">無法對內建帳戶執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**錯誤 \_ 特殊 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="56fa1-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-331">1372 (0x55C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-332">無法在這個內建的特殊群組上執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_特殊 \_ 使用者錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="56fa1-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-335">無法對這個內建的特殊使用者執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**錯誤 \_ 成員 \_ 主要 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="56fa1-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-338">無法從群組中移除使用者，因為群組目前是使用者的主要群組。</span><span class="sxs-lookup"><span data-stu-id="56fa1-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**錯誤 \_ 權杖 \_ 已 \_ 在 \_ 使用中**</span><span class="sxs-lookup"><span data-stu-id="56fa1-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-340">1375 (0x55F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-341">權杖已使用做為主要權杖。</span><span class="sxs-lookup"><span data-stu-id="56fa1-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**錯誤 \_ 沒有 \_ 這類 \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="56fa1-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-343">1376 (0x560) </span><span class="sxs-lookup"><span data-stu-id="56fa1-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-344">指定的本機群組不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**錯誤 \_ 成員 \_ 不 \_ 在 \_ 別名中**</span><span class="sxs-lookup"><span data-stu-id="56fa1-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="56fa1-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-347">指定的帳號名稱不是群組的成員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_ \_ 別名中的錯誤成員 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="56fa1-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-350">指定的帳號名稱已是群組的成員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**錯誤 \_ 別名 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="56fa1-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-353">指定的本機群組已經存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**\_ \_ 未 \_ 授與錯誤登入**</span><span class="sxs-lookup"><span data-stu-id="56fa1-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="56fa1-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-356">登入失敗：未在這部電腦上授與使用者所要求的登入類型。</span><span class="sxs-lookup"><span data-stu-id="56fa1-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**錯誤 \_ 太 \_ 多 \_ 秘密**</span><span class="sxs-lookup"><span data-stu-id="56fa1-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="56fa1-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-359">已超過可能儲存在單一系統中的秘密數目上限。</span><span class="sxs-lookup"><span data-stu-id="56fa1-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**錯誤 \_ 密碼 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="56fa1-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="56fa1-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-362">秘密的長度超過允許的最大長度。</span><span class="sxs-lookup"><span data-stu-id="56fa1-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**錯誤 \_ 內部 \_ 資料庫 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="56fa1-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-365">本地安全機構資料庫包含內部不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="56fa1-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**錯誤 \_ 太 \_ 多 \_ 內容 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="56fa1-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-368">在登入嘗試期間，使用者的安全性內容累積了太多的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_ \_ \_ 未 \_ 授與錯誤登入類型**</span><span class="sxs-lookup"><span data-stu-id="56fa1-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="56fa1-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-371">登入失敗：未在這部電腦上授與使用者所要求的登入類型。</span><span class="sxs-lookup"><span data-stu-id="56fa1-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**錯誤 \_ NT \_ \_ 需要跨加密 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-374">需要跨加密密碼才能變更使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**錯誤 \_ 的 \_ \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="56fa1-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="56fa1-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-377">無法在本機群組中加入或移除成員，因為該成員不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**錯誤 \_ 不正確 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="56fa1-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="56fa1-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-380">因為成員的帳戶類型錯誤，所以無法將新成員新增至本機群組。</span><span class="sxs-lookup"><span data-stu-id="56fa1-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**錯誤 \_ 太 \_ 多 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="56fa1-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-382">1389 (0x56D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-383">指定了太多的安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**\_需要 LM \_ 跨 \_ 加密 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-386">需要跨加密密碼才能變更此使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**錯誤 \_ 無 \_ 繼承**</span><span class="sxs-lookup"><span data-stu-id="56fa1-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-388">1391 (0x56F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-389">表示 ACL 未包含可繼承的元件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**錯誤檔案已損毀 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="56fa1-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-392">檔案或目錄已損毀且無法讀取。</span><span class="sxs-lookup"><span data-stu-id="56fa1-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**錯誤 \_ 磁片 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="56fa1-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="56fa1-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-395">磁片結構已損毀且無法讀取。</span><span class="sxs-lookup"><span data-stu-id="56fa1-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**錯誤 \_ 的 \_ 使用者 \_ 會話 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="56fa1-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="56fa1-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-398">指定的登入會話沒有使用者工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="56fa1-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_超過錯誤授權 \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="56fa1-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-401">正在存取的服務已獲得特定數目的連線授權。</span><span class="sxs-lookup"><span data-stu-id="56fa1-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="56fa1-402">目前無法再對服務進行連接，因為服務可以接受的連線數目已經過多。</span><span class="sxs-lookup"><span data-stu-id="56fa1-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**錯誤 \_ 的 \_ 目標 \_ 名稱錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="56fa1-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-405">目標帳戶名稱不正確。</span><span class="sxs-lookup"><span data-stu-id="56fa1-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**錯誤 \_ 相互 \_ 驗證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="56fa1-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-408">相互驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-408">Mutual Authentication failed.</span></span> <span data-ttu-id="56fa1-409">伺服器的密碼在網域控制站上已過期。</span><span class="sxs-lookup"><span data-stu-id="56fa1-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**錯誤 \_ 時間 \_ 誤差**</span><span class="sxs-lookup"><span data-stu-id="56fa1-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="56fa1-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-412">用戶端與伺服器之間有時間及/或日期的差異。</span><span class="sxs-lookup"><span data-stu-id="56fa1-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**\_ \_ \_ 不允許目前的網域錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="56fa1-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-415">無法在目前的網域上執行此作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**錯誤 \_ 不正確 \_ 視窗 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="56fa1-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-418">不正確視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**\_不正確 \_ 功能表 \_ 控制碼時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="56fa1-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-421">功能表控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**錯誤 \_ 不正確資料 \_ 指標 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="56fa1-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-424">不正確資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**錯誤 \_ 不正確 \_ ACCEL \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="56fa1-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-427">快速鍵對應表控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**錯誤 \_ 不正確攔截 \_ \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-429">1404 (0x57C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-430">不正確攔截控制碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**錯誤 \_ 不正確 \_ .DWP \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="56fa1-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-433">多視窗位置結構的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**\_ \_ 使用 WSCHILD TLW \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-435">1406 (0x57E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-436">無法建立最上層子視窗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**\_找不 \_ 到 \_ WND<> \_ 類別的錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-438">1407 (0x57F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-439">找不到視窗類別。</span><span class="sxs-lookup"><span data-stu-id="56fa1-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_ \_ \_ 其他 \_ 執行緒的錯誤視窗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-441">1408 (0x580) </span><span class="sxs-lookup"><span data-stu-id="56fa1-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-442">不正確視窗;它屬於其他執行緒。</span><span class="sxs-lookup"><span data-stu-id="56fa1-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**\_ \_ 已 \_ 註冊錯誤的熱鍵**</span><span class="sxs-lookup"><span data-stu-id="56fa1-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-444">1409 (0x581) </span><span class="sxs-lookup"><span data-stu-id="56fa1-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-445">快速鍵已註冊。</span><span class="sxs-lookup"><span data-stu-id="56fa1-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**錯誤 \_ 類別 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-447">1410 (0x582) </span><span class="sxs-lookup"><span data-stu-id="56fa1-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-448">類別已經存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**錯誤 \_ 類別 \_ 不 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-450">1411 (0x583) </span><span class="sxs-lookup"><span data-stu-id="56fa1-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-451">類別不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR \_ 類別 \_ 具有 \_ WINDOWS**</span><span class="sxs-lookup"><span data-stu-id="56fa1-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-453">1412 (0x584) </span><span class="sxs-lookup"><span data-stu-id="56fa1-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-454">類別仍有開啟的視窗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**錯誤 \_ 不正確 \_ 索引**</span><span class="sxs-lookup"><span data-stu-id="56fa1-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-456">1413 (0x585) </span><span class="sxs-lookup"><span data-stu-id="56fa1-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-457">不正確索引。</span><span class="sxs-lookup"><span data-stu-id="56fa1-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**錯誤 \_ 不正確 \_ 圖示 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-459">1414 (0x586) </span><span class="sxs-lookup"><span data-stu-id="56fa1-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-460">不正確圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**\_私用 \_ 對話 \_ 索引錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-462">1415 (0x587) </span><span class="sxs-lookup"><span data-stu-id="56fa1-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-463">使用私用交談視窗文字。</span><span class="sxs-lookup"><span data-stu-id="56fa1-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 LISTBOX 識別碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-465">1416 (0x588) </span><span class="sxs-lookup"><span data-stu-id="56fa1-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-466">找不到清單方塊識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**錯誤 \_ 沒有 \_ 萬用字元 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-468">1417 (0x589) </span><span class="sxs-lookup"><span data-stu-id="56fa1-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-469">找不到任何萬用字元。</span><span class="sxs-lookup"><span data-stu-id="56fa1-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**錯誤 \_ 剪貼簿 \_ 未 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="56fa1-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-471">1418 (0x58A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-472">執行緒沒有開啟剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="56fa1-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**錯誤的 \_ 熱鍵 \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="56fa1-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-474">1419 (0x58B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-475">快速鍵未註冊。</span><span class="sxs-lookup"><span data-stu-id="56fa1-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**錯誤 \_ 視窗 \_ 未 \_ 對話方塊**</span><span class="sxs-lookup"><span data-stu-id="56fa1-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-477">1420 (0x58C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-478">視窗不是有效的交談視窗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ \_ \_ \_ 找不到錯誤控制識別碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-480">1421 (0x58D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-481">找不到控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**\_不正確 \_ COMBOBOX \_ 訊息錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-483">1422 (0x58E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-484">下拉式方塊的訊息無效，因為它沒有編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="56fa1-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**錯誤 \_ 視窗 \_ 不是 \_ COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="56fa1-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-486">1423 (0x58F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-487">視窗不是下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="56fa1-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**錯誤 \_ 不正確 \_ 編輯 \_ 高度**</span><span class="sxs-lookup"><span data-stu-id="56fa1-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-489">1424 (0x590) </span><span class="sxs-lookup"><span data-stu-id="56fa1-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-490">高度必須小於256。</span><span class="sxs-lookup"><span data-stu-id="56fa1-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_ \_ 找不到錯誤 DC \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-492">1425 (0x591) </span><span class="sxs-lookup"><span data-stu-id="56fa1-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-493">裝置內容 (DC) 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**錯誤 \_ 不正確攔截 \_ \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="56fa1-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-495">1426 (0x592) </span><span class="sxs-lookup"><span data-stu-id="56fa1-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-496">不正確掛勾程式類型。</span><span class="sxs-lookup"><span data-stu-id="56fa1-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**錯誤 \_ 不正確 \_ 篩選器 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="56fa1-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-498">1427 (0x593) </span><span class="sxs-lookup"><span data-stu-id="56fa1-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-499">不正確攔截程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**錯誤 \_ 攔截 \_ 需要 \_ HMOD**</span><span class="sxs-lookup"><span data-stu-id="56fa1-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-501">1428 (0x594) </span><span class="sxs-lookup"><span data-stu-id="56fa1-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-502">無法在沒有模組控制碼的情況下設定非本機掛勾。</span><span class="sxs-lookup"><span data-stu-id="56fa1-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_全域 \_ 唯一攔截 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-504">1429 (0x595) </span><span class="sxs-lookup"><span data-stu-id="56fa1-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-505">此攔截程式只能在全域設定。</span><span class="sxs-lookup"><span data-stu-id="56fa1-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**錯誤 \_ 日誌 \_ 掛勾 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="56fa1-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-507">1430 (0x596) </span><span class="sxs-lookup"><span data-stu-id="56fa1-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-508">已安裝日誌攔截程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**\_ \_ 未 \_ 安裝錯誤攔截**</span><span class="sxs-lookup"><span data-stu-id="56fa1-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-510">1431 (0x597) </span><span class="sxs-lookup"><span data-stu-id="56fa1-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-511">未安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**錯誤 \_ 不正確 \_ LB \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="56fa1-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-513">1432 (0x598) </span><span class="sxs-lookup"><span data-stu-id="56fa1-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-514">單一選取清單方塊的訊息無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**錯誤 \_ \_ LB 上的錯誤 SETCOUNT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-516">1433 (0x599) </span><span class="sxs-lookup"><span data-stu-id="56fa1-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-517">LB \_ SETCOUNT 傳送至非延遲清單方塊。</span><span class="sxs-lookup"><span data-stu-id="56fa1-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**錯誤 \_ LB \_ 但沒有 \_ TABSTOPS**</span><span class="sxs-lookup"><span data-stu-id="56fa1-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-519">1434 (0x59A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-520">此清單方塊不支援定位停駐點。</span><span class="sxs-lookup"><span data-stu-id="56fa1-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**損 \_ 毀 \_ \_ \_ 其他執行緒的 \_ 物件時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-522">1435 (0x59B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-523">無法終結另一個執行緒所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**錯誤 \_ 子 \_ 視窗 \_ 功能表**</span><span class="sxs-lookup"><span data-stu-id="56fa1-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-525">1436 (0x59C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-526">子視窗不可以有功能表。</span><span class="sxs-lookup"><span data-stu-id="56fa1-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**錯誤 \_ 的 \_ 系統 \_ 功能表**</span><span class="sxs-lookup"><span data-stu-id="56fa1-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-528">1437 (0x59D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-529">視窗沒有系統功能表。</span><span class="sxs-lookup"><span data-stu-id="56fa1-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**\_不正確 \_ MSGBOX \_ 樣式錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-531">1438 (0x59E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-532">訊息方塊樣式無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**錯誤 \_ 不正確 \_ SPI \_ 值**</span><span class="sxs-lookup"><span data-stu-id="56fa1-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-534">1439 (0x59F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-535">不正確全系統 (SPI \_ \*) 參數。</span><span class="sxs-lookup"><span data-stu-id="56fa1-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**錯誤 \_ 畫面 \_ 已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="56fa1-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-537">1440 (0x5A0) </span><span class="sxs-lookup"><span data-stu-id="56fa1-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-538">螢幕已鎖定。</span><span class="sxs-lookup"><span data-stu-id="56fa1-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**錯誤 \_ HWND \_ 具有 \_ 差異 \_ 父系**</span><span class="sxs-lookup"><span data-stu-id="56fa1-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-540">1441 (0x5A1) </span><span class="sxs-lookup"><span data-stu-id="56fa1-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-541">多視窗位置結構中的所有 windows 控制碼都必須具有相同的父系。</span><span class="sxs-lookup"><span data-stu-id="56fa1-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**錯誤 \_ 不是 \_ 子 \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-543">1442 (0x5A2) </span><span class="sxs-lookup"><span data-stu-id="56fa1-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-544">視窗不是子視窗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**錯誤 \_ 不正確 \_ GW \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="56fa1-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-546">1443 (0x5A3) </span><span class="sxs-lookup"><span data-stu-id="56fa1-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-547">GW \_ \* 命令無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**錯誤 \_ 不正確 \_ 執行緒 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-549">1444 (0x5A4) </span><span class="sxs-lookup"><span data-stu-id="56fa1-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-550">不正確執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**錯誤 \_ 非 \_ MDICHILD \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-552">1445 (0x5A5) </span><span class="sxs-lookup"><span data-stu-id="56fa1-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-553">無法從非多重文件介面 (MDI) 視窗的視窗處理訊息。</span><span class="sxs-lookup"><span data-stu-id="56fa1-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**錯誤 \_ 快顯視窗 \_ 已在 \_ 使用中**</span><span class="sxs-lookup"><span data-stu-id="56fa1-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-555">1446 (0x5A6) </span><span class="sxs-lookup"><span data-stu-id="56fa1-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-556">快顯功能表已在使用中。</span><span class="sxs-lookup"><span data-stu-id="56fa1-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**錯誤 \_ 的 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="56fa1-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-558">1447 (0x5A7) </span><span class="sxs-lookup"><span data-stu-id="56fa1-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-559">視窗沒有捲軸。</span><span class="sxs-lookup"><span data-stu-id="56fa1-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**錯誤 \_ 的 \_ 捲軸 \_ 範圍無效**</span><span class="sxs-lookup"><span data-stu-id="56fa1-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-561">1448 (0x5A8) </span><span class="sxs-lookup"><span data-stu-id="56fa1-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-562">捲軸範圍不能大於 MAXLONG。</span><span class="sxs-lookup"><span data-stu-id="56fa1-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**錯誤 \_ 不正確 \_ SHOWWIN \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="56fa1-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-564">1449 (0x5A9) </span><span class="sxs-lookup"><span data-stu-id="56fa1-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-565">無法以指定的方式顯示或移除視窗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**錯誤 \_ 的 \_ 系統 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="56fa1-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-567">1450 (0x5AA) </span><span class="sxs-lookup"><span data-stu-id="56fa1-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-568">沒有足夠的系統資源，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**錯誤的未 \_ 分頁 \_ 系統 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="56fa1-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-570">1451 (0x5AB) </span><span class="sxs-lookup"><span data-stu-id="56fa1-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-571">沒有足夠的系統資源，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**\_分頁 \_ 系統 \_ 資源錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-573">1452 (0x5AC) </span><span class="sxs-lookup"><span data-stu-id="56fa1-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-574">沒有足夠的系統資源，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**\_工作 \_ 集 \_ 配額錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-576">1453 (0x5AD) </span><span class="sxs-lookup"><span data-stu-id="56fa1-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-577">配額不足，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**錯誤 \_ 分頁檔 \_ 配額**</span><span class="sxs-lookup"><span data-stu-id="56fa1-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-579">1454 (0x5AE) </span><span class="sxs-lookup"><span data-stu-id="56fa1-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-580">配額不足，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**錯誤 \_ 承諾用量 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="56fa1-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-582">1455 (0x5AF) </span><span class="sxs-lookup"><span data-stu-id="56fa1-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-583">分頁檔案太小，所以無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="56fa1-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ \_ \_ 找不到錯誤功能表項目**</span><span class="sxs-lookup"><span data-stu-id="56fa1-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-585">1456 (0x5B0) </span><span class="sxs-lookup"><span data-stu-id="56fa1-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-586">找不到功能表項目。</span><span class="sxs-lookup"><span data-stu-id="56fa1-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**\_不正確 \_ 鍵盤 \_ 控制碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-588">1457 (0x5B1) </span><span class="sxs-lookup"><span data-stu-id="56fa1-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-589">鍵盤配置控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_ \_ \_ 不 \_ 允許錯誤攔截類型**</span><span class="sxs-lookup"><span data-stu-id="56fa1-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-591">1458 (0x5B2) </span><span class="sxs-lookup"><span data-stu-id="56fa1-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-592">不允許使用勾點類型。</span><span class="sxs-lookup"><span data-stu-id="56fa1-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**錯誤 \_ 需要 \_ 互動式 \_ WINDOWSTATION**</span><span class="sxs-lookup"><span data-stu-id="56fa1-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-594">1459 (0x5B3) </span><span class="sxs-lookup"><span data-stu-id="56fa1-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-595">這種操作需要互動式的視窗站。</span><span class="sxs-lookup"><span data-stu-id="56fa1-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**錯誤 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="56fa1-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-597">1460 (0x5B4) </span><span class="sxs-lookup"><span data-stu-id="56fa1-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-598">因為超時時間已過，所以會傳回此作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**錯誤 \_ 不正確 \_ 監視器 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="56fa1-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-600">1461 (0x5B5) </span><span class="sxs-lookup"><span data-stu-id="56fa1-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-601">不正確監視器控制碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**錯誤 \_ 的 \_ 大小不正確**</span><span class="sxs-lookup"><span data-stu-id="56fa1-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-603">1462 (0x5B6) </span><span class="sxs-lookup"><span data-stu-id="56fa1-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-604">大小引數不正確。</span><span class="sxs-lookup"><span data-stu-id="56fa1-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**錯誤 \_ 符號符號 \_ 類別 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="56fa1-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-606">1463 (0x5B7) </span><span class="sxs-lookup"><span data-stu-id="56fa1-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-607">無法遵循符號連結，因為它的類型已停用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**\_ \_ 不支援錯誤符號符號 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-609">1464 (0x5B8) </span><span class="sxs-lookup"><span data-stu-id="56fa1-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-610">此應用程式不支援符號連結上的目前作業。</span><span class="sxs-lookup"><span data-stu-id="56fa1-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**錯誤 \_ XML \_ 剖析 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-612">1465 (0x5B9) </span><span class="sxs-lookup"><span data-stu-id="56fa1-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-613">Windows 無法剖析要求的 XML 資料。</span><span class="sxs-lookup"><span data-stu-id="56fa1-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**錯誤 \_ XMLDSIG \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-615">1466 (0x5BA) </span><span class="sxs-lookup"><span data-stu-id="56fa1-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-616">處理 XML 數位簽章時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**\_重新開機 \_ 應用程式時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-618">1467 (0x5BB) </span><span class="sxs-lookup"><span data-stu-id="56fa1-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-619">此應用程式必須重新開機。</span><span class="sxs-lookup"><span data-stu-id="56fa1-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**錯誤 \_ 的 \_ 區間**</span><span class="sxs-lookup"><span data-stu-id="56fa1-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-621">1468 (0x5BC) </span><span class="sxs-lookup"><span data-stu-id="56fa1-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-622">呼叫者在錯誤的路由區間中提出了連線要求。</span><span class="sxs-lookup"><span data-stu-id="56fa1-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**錯誤 \_ AUTHIP \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-624">1469 (0x5BD) </span><span class="sxs-lookup"><span data-stu-id="56fa1-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-625">嘗試連接到遠端主機時發生 AuthIP 失敗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**錯誤 \_ 的 \_ NVRAM \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="56fa1-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-627">1470 (0x5BE) </span><span class="sxs-lookup"><span data-stu-id="56fa1-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-628">沒有足夠的 NVRAM 資源，無法完成要求的服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="56fa1-629">可能需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="56fa1-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**錯誤 \_ 而非 \_ GUI \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="56fa1-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-631">1471 (0x5BF) </span><span class="sxs-lookup"><span data-stu-id="56fa1-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-632">無法完成要求的操作，因為指定的進程不是 GUI 進程。</span><span class="sxs-lookup"><span data-stu-id="56fa1-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**錯誤 \_ EVENTLOG \_ 檔 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="56fa1-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-634">1500 (0x5DC) </span><span class="sxs-lookup"><span data-stu-id="56fa1-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-635">事件記錄檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="56fa1-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**錯誤 \_ EVENTLOG \_ 無法 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="56fa1-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-637">1501 (0x5DD) </span><span class="sxs-lookup"><span data-stu-id="56fa1-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-638">無法開啟任何事件記錄檔，因此事件記錄服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="56fa1-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**錯誤 \_ 記錄檔已 \_ \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="56fa1-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-640">1502 (0x5DE) </span><span class="sxs-lookup"><span data-stu-id="56fa1-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-641">事件記錄檔已滿。</span><span class="sxs-lookup"><span data-stu-id="56fa1-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**錯誤 \_ EVENTLOG \_ 檔 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="56fa1-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-643">1503 (0x5DF) </span><span class="sxs-lookup"><span data-stu-id="56fa1-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-644">事件記錄檔已在讀取作業之間變更。</span><span class="sxs-lookup"><span data-stu-id="56fa1-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**錯誤 \_ 不正確工作 \_ \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="56fa1-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="56fa1-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-647">指定的工作名稱無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**錯誤 \_ 不正確工作 \_ \_ 索引**</span><span class="sxs-lookup"><span data-stu-id="56fa1-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="56fa1-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-650">指定的任務索引無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**工作 \_ \_ 中已經 \_ 有錯誤執行緒 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="56fa1-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-653">指定的執行緒已經加入工作。</span><span class="sxs-lookup"><span data-stu-id="56fa1-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**\_安裝 \_ 服務 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-655">1601 (0x641) </span><span class="sxs-lookup"><span data-stu-id="56fa1-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-656">無法存取 Windows Installer 服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="56fa1-657">如果未正確安裝 Windows Installer，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="56fa1-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="56fa1-658">請洽詢支援人員以取得協助。</span><span class="sxs-lookup"><span data-stu-id="56fa1-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**\_安裝 \_ USEREXIT 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-660">1602 (0x642) </span><span class="sxs-lookup"><span data-stu-id="56fa1-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-661">使用者已取消安裝。</span><span class="sxs-lookup"><span data-stu-id="56fa1-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**\_安裝 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-663">1603 (0x643) </span><span class="sxs-lookup"><span data-stu-id="56fa1-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-664">安裝時發生嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**\_安裝 \_ 暫止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-666">1604 (0x644) </span><span class="sxs-lookup"><span data-stu-id="56fa1-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-667">安裝已暫停，未完成。</span><span class="sxs-lookup"><span data-stu-id="56fa1-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**錯誤 \_ 未知的 \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="56fa1-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-669">1605 (0x645) </span><span class="sxs-lookup"><span data-stu-id="56fa1-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-670">這個動作只對目前安裝的產品有效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**錯誤 \_ 未知的 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="56fa1-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-672">1606 (0x646) </span><span class="sxs-lookup"><span data-stu-id="56fa1-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-673">未註冊功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**錯誤 \_ 不明的 \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="56fa1-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-675">1607 (0x647) </span><span class="sxs-lookup"><span data-stu-id="56fa1-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-676">未註冊元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="56fa1-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**錯誤 \_ 未知的 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="56fa1-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-678">1608 (0x648) </span><span class="sxs-lookup"><span data-stu-id="56fa1-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-679">未知的屬性。</span><span class="sxs-lookup"><span data-stu-id="56fa1-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**錯誤 \_ 不正確 \_ 控制碼 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="56fa1-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-681">1609 (0x649) </span><span class="sxs-lookup"><span data-stu-id="56fa1-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-682">控制碼處於不正確狀態。</span><span class="sxs-lookup"><span data-stu-id="56fa1-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**錯誤的設定不 \_ 正確 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-684">1610 (0x64A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-685">此產品的設定資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="56fa1-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="56fa1-686">請聯絡支援人員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**錯誤 \_ 索引不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="56fa1-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-688">1611 (0x64B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-689">元件辨識符號不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**\_安裝 \_ 來源不 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-691">1612 (0x64C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-692">無法使用此產品的安裝來源。</span><span class="sxs-lookup"><span data-stu-id="56fa1-692">The installation source for this product is not available.</span></span> <span data-ttu-id="56fa1-693">請確認來源是否存在，以及您是否可以存取它。</span><span class="sxs-lookup"><span data-stu-id="56fa1-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**\_安裝 \_ 套件 \_ 版本時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-695">1613 (0x64D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-696">Windows Installer 服務無法安裝這個安裝套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="56fa1-697">您必須安裝包含較新版本之 Windows Installer 服務的 Windows service pack。</span><span class="sxs-lookup"><span data-stu-id="56fa1-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**卸載的錯誤 \_ 產品 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-699">1614 (0x64E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-700">解除安裝產品。</span><span class="sxs-lookup"><span data-stu-id="56fa1-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**錯誤 \_ \_ 查詢 \_ 語法錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-702">1615 (0x64F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-703">SQL 查詢語法無效或不受支援。</span><span class="sxs-lookup"><span data-stu-id="56fa1-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**錯誤 \_ 不正確 \_ 欄位**</span><span class="sxs-lookup"><span data-stu-id="56fa1-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-705">1616 (0x650) </span><span class="sxs-lookup"><span data-stu-id="56fa1-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-706">記錄欄位不存在。</span><span class="sxs-lookup"><span data-stu-id="56fa1-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**\_ \_ 已移除錯誤裝置**</span><span class="sxs-lookup"><span data-stu-id="56fa1-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-708">1617 (0x651) </span><span class="sxs-lookup"><span data-stu-id="56fa1-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-709">裝置已移除。</span><span class="sxs-lookup"><span data-stu-id="56fa1-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**\_安裝 \_ 已在執行中時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-711">1618 (0x652) </span><span class="sxs-lookup"><span data-stu-id="56fa1-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-712">另一個安裝已在進行中。</span><span class="sxs-lookup"><span data-stu-id="56fa1-712">Another installation is already in progress.</span></span> <span data-ttu-id="56fa1-713">繼續進行此安裝之前，請先完成該安裝。</span><span class="sxs-lookup"><span data-stu-id="56fa1-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**錯誤 \_ 安裝 \_ 套件 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-715">1619 (0x653) </span><span class="sxs-lookup"><span data-stu-id="56fa1-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-716">無法開啟此安裝套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-716">This installation package could not be opened.</span></span> <span data-ttu-id="56fa1-717">請確認封裝存在，而且您可以存取它，或洽詢應用程式廠商，確認這是有效的 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**\_安裝 \_ 套件 \_ 不正確錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-719">1620 (0x654) </span><span class="sxs-lookup"><span data-stu-id="56fa1-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-720">無法開啟此安裝套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-720">This installation package could not be opened.</span></span> <span data-ttu-id="56fa1-721">請聯繫應用程式廠商，確認這是有效的 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**\_安裝 \_ UI \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-723">1621 (0x655) </span><span class="sxs-lookup"><span data-stu-id="56fa1-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-724">啟動 Windows Installer 服務使用者介面時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="56fa1-725">請聯絡支援人員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**\_安裝 \_ 記錄檔 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-727">1622 (0x656) </span><span class="sxs-lookup"><span data-stu-id="56fa1-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-728">開啟安裝記錄檔時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-728">Error opening installation log file.</span></span> <span data-ttu-id="56fa1-729">確認指定的記錄檔位置存在，而且您可以寫入它。</span><span class="sxs-lookup"><span data-stu-id="56fa1-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**\_ \_ 不支援的安裝語言錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-731">1623 (0x657) </span><span class="sxs-lookup"><span data-stu-id="56fa1-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-732">系統不支援此安裝套件的語言。</span><span class="sxs-lookup"><span data-stu-id="56fa1-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**\_安裝 \_ 轉換 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-734">1624 (0x658) </span><span class="sxs-lookup"><span data-stu-id="56fa1-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-735">套用轉換時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-735">Error applying transforms.</span></span> <span data-ttu-id="56fa1-736">確認指定的轉換路徑有效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**\_拒絕安裝 \_ 套件的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-738">1625 (0x659) </span><span class="sxs-lookup"><span data-stu-id="56fa1-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-739">系統原則禁止此安裝。</span><span class="sxs-lookup"><span data-stu-id="56fa1-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="56fa1-740">請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**\_ \_ 未 \_ 呼叫錯誤函式**</span><span class="sxs-lookup"><span data-stu-id="56fa1-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-742">1626 (0x65A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-743">無法執行函數。</span><span class="sxs-lookup"><span data-stu-id="56fa1-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**錯誤函式 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-745">1627 (0x65B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-746">函數在執行期間失敗。</span><span class="sxs-lookup"><span data-stu-id="56fa1-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**錯誤 \_ 不正確 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="56fa1-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-748">1628 (0x65C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-749">指定的資料表無效或未知。</span><span class="sxs-lookup"><span data-stu-id="56fa1-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**錯誤 \_ 資料類型 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="56fa1-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-751">1629 (0x65D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-752">提供的資料類型錯誤。</span><span class="sxs-lookup"><span data-stu-id="56fa1-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**錯誤 \_ 不支援的 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="56fa1-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-754">1630 (0x65E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-755">不支援此類型的資料。</span><span class="sxs-lookup"><span data-stu-id="56fa1-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**錯誤 \_ 建立 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-757">1631 (0x65F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-758">Windows Installer 服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="56fa1-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="56fa1-759">請聯絡支援人員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**\_安裝 \_ TEMP \_ 資料流程時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-761">1632 (0x660) </span><span class="sxs-lookup"><span data-stu-id="56fa1-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-762">Temp 資料夾位於已滿或無法存取的磁片磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="56fa1-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="56fa1-763">釋放磁片磁碟機上的空間，或確認您擁有 Temp 資料夾的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="56fa1-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**\_ \_ 不支援的安裝平臺錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-765">1633 (0x661) </span><span class="sxs-lookup"><span data-stu-id="56fa1-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-766">此處理器類型不支援此安裝套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="56fa1-767">請洽詢您的產品廠商。</span><span class="sxs-lookup"><span data-stu-id="56fa1-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**\_安裝 \_ NOTUSED 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-769">1634 (0x662) </span><span class="sxs-lookup"><span data-stu-id="56fa1-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-770">元件未在這部電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="56fa1-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**錯誤 \_ 修補 \_ 套件 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="56fa1-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-772">1635 (0x663) </span><span class="sxs-lookup"><span data-stu-id="56fa1-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-773">無法開啟此更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-773">This update package could not be opened.</span></span> <span data-ttu-id="56fa1-774">確認更新封裝存在，而且您可以存取它，或聯繫應用程式廠商，確認這是有效的 Windows Installer 更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**錯誤 \_ 修補程式 \_ 套件 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="56fa1-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-776">1636 (0x664) </span><span class="sxs-lookup"><span data-stu-id="56fa1-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-777">無法開啟此更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-777">This update package could not be opened.</span></span> <span data-ttu-id="56fa1-778">請聯繫應用程式廠商，確認這是有效的 Windows Installer 更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**\_不支援錯誤修補程式 \_ 套件 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-780">1637 (0x665) </span><span class="sxs-lookup"><span data-stu-id="56fa1-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-781">Windows Installer 服務無法處理此更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="56fa1-782">您必須安裝包含較新版本之 Windows Installer 服務的 Windows service pack。</span><span class="sxs-lookup"><span data-stu-id="56fa1-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**錯誤 \_ 產品 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="56fa1-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-784">1638 (0x666) </span><span class="sxs-lookup"><span data-stu-id="56fa1-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-785">已安裝此產品的其他版本。</span><span class="sxs-lookup"><span data-stu-id="56fa1-785">Another version of this product is already installed.</span></span> <span data-ttu-id="56fa1-786">無法繼續安裝這個版本。</span><span class="sxs-lookup"><span data-stu-id="56fa1-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="56fa1-787">若要設定或移除此產品的現有版本，請使用主控台上的 [新增/移除程式]。</span><span class="sxs-lookup"><span data-stu-id="56fa1-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**錯誤 \_ 不正確 \_ 命令 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="56fa1-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-789">1639 (0x667) </span><span class="sxs-lookup"><span data-stu-id="56fa1-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-790">不正確命令列引數。</span><span class="sxs-lookup"><span data-stu-id="56fa1-790">Invalid command line argument.</span></span> <span data-ttu-id="56fa1-791">如需詳細的命令列說明，請參閱 Windows Installer SDK。</span><span class="sxs-lookup"><span data-stu-id="56fa1-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**不 \_ \_ 允許遠端 \_ 安裝錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-793">1640 (0x668) </span><span class="sxs-lookup"><span data-stu-id="56fa1-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-794">只有系統管理員有權在終端機服務遠端會話期間加入、移除或設定伺服器軟體。</span><span class="sxs-lookup"><span data-stu-id="56fa1-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="56fa1-795">如果您想要在伺服器上安裝或設定軟體，請洽詢您的網路系統管理員。</span><span class="sxs-lookup"><span data-stu-id="56fa1-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**\_起始錯誤成功 \_ 重新開機 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-797">1641 (0x669) </span><span class="sxs-lookup"><span data-stu-id="56fa1-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-798">要求的作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="56fa1-798">The requested operation completed successfully.</span></span> <span data-ttu-id="56fa1-799">系統將會重新開機，讓變更生效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_ \_ \_ \_ 找不到錯誤修補程式目標**</span><span class="sxs-lookup"><span data-stu-id="56fa1-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-801">1642 (0x66A) </span><span class="sxs-lookup"><span data-stu-id="56fa1-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-802">Windows Installer 服務無法安裝升級，因為要升級的程式可能已遺失，或升級可能會更新不同版本的程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="56fa1-803">確認要升級的程式存在於您的電腦上，而且您有正確的升級。</span><span class="sxs-lookup"><span data-stu-id="56fa1-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**\_拒絕錯誤修補程式 \_ 套件 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-805">1643 (0x66B) </span><span class="sxs-lookup"><span data-stu-id="56fa1-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-806">軟體限制原則不允許更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**\_拒絕安裝 \_ 轉換的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-808">1644 (0x66C) </span><span class="sxs-lookup"><span data-stu-id="56fa1-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-809">軟體限制原則不允許有一或多個自訂專案。</span><span class="sxs-lookup"><span data-stu-id="56fa1-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**\_禁止安裝 \_ 遠端的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-811">1645 (0x66D) </span><span class="sxs-lookup"><span data-stu-id="56fa1-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-812">Windows Installer 不允許從遠端桌面連線進行安裝。</span><span class="sxs-lookup"><span data-stu-id="56fa1-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_ \_ 不支援移除錯誤修補程式 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-814">1646 (0x66E) </span><span class="sxs-lookup"><span data-stu-id="56fa1-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-815">不支援卸載更新套件。</span><span class="sxs-lookup"><span data-stu-id="56fa1-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**錯誤 \_ 不明的 \_ 修補程式**</span><span class="sxs-lookup"><span data-stu-id="56fa1-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-817">1647 (0x66F) </span><span class="sxs-lookup"><span data-stu-id="56fa1-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-818">此產品不會套用更新。</span><span class="sxs-lookup"><span data-stu-id="56fa1-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**錯誤 \_ 修補程式 \_ 沒有 \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="56fa1-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-820">1648 (0x670) </span><span class="sxs-lookup"><span data-stu-id="56fa1-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-821">找不到更新集的有效順序。</span><span class="sxs-lookup"><span data-stu-id="56fa1-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**不 \_ \_ 允許移除錯誤修補程式 \_**</span><span class="sxs-lookup"><span data-stu-id="56fa1-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-823">1649 (0x671) </span><span class="sxs-lookup"><span data-stu-id="56fa1-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-824">原則不允許更新移除。</span><span class="sxs-lookup"><span data-stu-id="56fa1-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**錯誤 \_ 不正確 \_ PATCH \_ XML**</span><span class="sxs-lookup"><span data-stu-id="56fa1-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-826">1650 (0x672) </span><span class="sxs-lookup"><span data-stu-id="56fa1-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-827">XML 更新資料無效。</span><span class="sxs-lookup"><span data-stu-id="56fa1-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**錯誤 \_ 修補 \_ 受管理的 \_ 公告 \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="56fa1-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-829">1651 (0x673) </span><span class="sxs-lookup"><span data-stu-id="56fa1-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-830">Windows Installer 不允許更新受管理的公告產品。</span><span class="sxs-lookup"><span data-stu-id="56fa1-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="56fa1-831">套用更新之前，必須先安裝產品的至少一個功能。</span><span class="sxs-lookup"><span data-stu-id="56fa1-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**\_安裝 \_ 服務 \_ 安全開機時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-833">1652 (0x674) </span><span class="sxs-lookup"><span data-stu-id="56fa1-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-834">在安全模式下，無法存取 Windows Installer 服務。</span><span class="sxs-lookup"><span data-stu-id="56fa1-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="56fa1-835">請在您的電腦不是處於安全模式時再試一次，也可以使用系統還原將電腦恢復為先前的良好狀態。</span><span class="sxs-lookup"><span data-stu-id="56fa1-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**錯誤 \_ 失敗 \_ 快速 \_ 例外狀況**</span><span class="sxs-lookup"><span data-stu-id="56fa1-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-837">1653 (0x675) </span><span class="sxs-lookup"><span data-stu-id="56fa1-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-838">發生失敗的快速例外狀況。</span><span class="sxs-lookup"><span data-stu-id="56fa1-838">A fail fast exception occurred.</span></span> <span data-ttu-id="56fa1-839">系統將不會叫用例外狀況處理常式，而且會立即終止進程。</span><span class="sxs-lookup"><span data-stu-id="56fa1-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56fa1-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**\_拒絕安裝 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="56fa1-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fa1-841">1654 (0x676) </span><span class="sxs-lookup"><span data-stu-id="56fa1-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="56fa1-842">此版本的 Windows 不支援您嘗試執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="56fa1-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56fa1-843">規格需求</span><span class="sxs-lookup"><span data-stu-id="56fa1-843">Requirements</span></span>



| <span data-ttu-id="56fa1-844">需求</span><span class="sxs-lookup"><span data-stu-id="56fa1-844">Requirement</span></span> | <span data-ttu-id="56fa1-845">值</span><span class="sxs-lookup"><span data-stu-id="56fa1-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56fa1-846">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56fa1-846">Minimum supported client</span></span><br/> | <span data-ttu-id="56fa1-847">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56fa1-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56fa1-848">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56fa1-848">Minimum supported server</span></span><br/> | <span data-ttu-id="56fa1-849">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56fa1-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56fa1-850">標頭</span><span class="sxs-lookup"><span data-stu-id="56fa1-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="56fa1-851"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="56fa1-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fa1-852">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56fa1-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fa1-853">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="56fa1-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




