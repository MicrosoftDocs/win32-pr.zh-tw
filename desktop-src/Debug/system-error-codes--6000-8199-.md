---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼6000-8199，適用于開發人員。
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: '系統錯誤碼 (6000-8199)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847420"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="fda70-103">系統錯誤碼 (6000-8199) </span><span class="sxs-lookup"><span data-stu-id="fda70-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="fda70-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="fda70-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="fda70-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="fda70-106">下列清單描述 (錯誤6000到 8199) 的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="fda70-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="fda70-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="fda70-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="fda70-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="fda70-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="fda70-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**錯誤 \_ 加密 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-110">6000 (0x1770) </span><span class="sxs-lookup"><span data-stu-id="fda70-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-111">無法加密指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**錯誤 \_ 解密 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-113">6001 (0x1771) </span><span class="sxs-lookup"><span data-stu-id="fda70-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-114">無法解密指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**錯誤檔案已 \_ \_ 加密**</span><span class="sxs-lookup"><span data-stu-id="fda70-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-116">6002 (0x1772) </span><span class="sxs-lookup"><span data-stu-id="fda70-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-117">指定的檔案已加密，且使用者沒有解密的能力。</span><span class="sxs-lookup"><span data-stu-id="fda70-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**錯誤的復原 \_ \_ \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="fda70-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-119">6003 (0x1773) </span><span class="sxs-lookup"><span data-stu-id="fda70-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-120">未針對此系統設定有效的加密修復原則。</span><span class="sxs-lookup"><span data-stu-id="fda70-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**錯誤 \_ 無 \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="fda70-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-122">6004 (0x1774) </span><span class="sxs-lookup"><span data-stu-id="fda70-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-123">未針對此系統載入所需的加密驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda70-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**錯誤 \_ 的 \_ EFS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-125">6005 (0x1775) </span><span class="sxs-lookup"><span data-stu-id="fda70-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-126">檔案使用的加密驅動程式與目前載入的不同。</span><span class="sxs-lookup"><span data-stu-id="fda70-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**錯誤 \_ 的 \_ 使用者 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="fda70-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-128">6006 (0x1776) </span><span class="sxs-lookup"><span data-stu-id="fda70-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-129">沒有為使用者定義 EFS 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fda70-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**錯誤 \_ 檔案 \_ 未 \_ 加密**</span><span class="sxs-lookup"><span data-stu-id="fda70-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-131">6007 (0x1777) </span><span class="sxs-lookup"><span data-stu-id="fda70-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-132">指定的檔案未加密。</span><span class="sxs-lookup"><span data-stu-id="fda70-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**錯誤 \_ 不是 \_ 匯出 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="fda70-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-134">6008 (0x1778) </span><span class="sxs-lookup"><span data-stu-id="fda70-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-135">指定的檔案不是定義的 EFS 匯出格式。</span><span class="sxs-lookup"><span data-stu-id="fda70-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**錯誤 \_ 檔案 \_ 唯讀 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-137">6009 (0x1779) </span><span class="sxs-lookup"><span data-stu-id="fda70-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-138">指定的檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fda70-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**錯誤 \_ DIR \_ 不 \_ 允許的 EFS**</span><span class="sxs-lookup"><span data-stu-id="fda70-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-140">6010 (0x177A) </span><span class="sxs-lookup"><span data-stu-id="fda70-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-141">目錄已停用加密。</span><span class="sxs-lookup"><span data-stu-id="fda70-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**錯誤的 \_ EFS \_ 伺服器 \_ 不 \_ 受信任**</span><span class="sxs-lookup"><span data-stu-id="fda70-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-143">6011 (0x177B) </span><span class="sxs-lookup"><span data-stu-id="fda70-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-144">伺服器不受遠端加密作業的信任。</span><span class="sxs-lookup"><span data-stu-id="fda70-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**錯誤的復原 \_ \_ \_ 原則錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-146">6012 (0x177C) </span><span class="sxs-lookup"><span data-stu-id="fda70-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-147">為此系統設定的復原原則包含不正確修復憑證。</span><span class="sxs-lookup"><span data-stu-id="fda70-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**錯誤 \_ EFS \_ ALG \_ BLOB \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="fda70-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-149">6013 (0x177D) </span><span class="sxs-lookup"><span data-stu-id="fda70-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-150">來源檔案上所使用的加密演算法需要比目的地檔案上更大的金鑰緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fda70-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**錯誤 \_ 磁片區 \_ 不 \_ 支援 \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="fda70-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-152">6014 (0x177E) </span><span class="sxs-lookup"><span data-stu-id="fda70-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-153">磁碟分割不支援檔案加密。</span><span class="sxs-lookup"><span data-stu-id="fda70-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**\_ \_ 停用 EFS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-155">6015 (0x177F) </span><span class="sxs-lookup"><span data-stu-id="fda70-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-156">此電腦已停用檔案加密。</span><span class="sxs-lookup"><span data-stu-id="fda70-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**\_ \_ \_ 不支援的 EFS 版本錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-158">6016 (0x1780) </span><span class="sxs-lookup"><span data-stu-id="fda70-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-159">需要較新的系統才能將這個加密的檔案解密。</span><span class="sxs-lookup"><span data-stu-id="fda70-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**錯誤 \_ CS \_ 加密 \_ 不正確 \_ 伺服器 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="fda70-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-161">6017 (0x1781) </span><span class="sxs-lookup"><span data-stu-id="fda70-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-162">遠端伺服器針對以用戶端加密開啟的檔案傳送了不正確回應。</span><span class="sxs-lookup"><span data-stu-id="fda70-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**錯誤 \_ CS \_ 加密 \_ 不支援的 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="fda70-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-164">6018 (0x1782) </span><span class="sxs-lookup"><span data-stu-id="fda70-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-165">遠端伺服器不支援用戶端加密，即使它宣稱支援它也一樣。</span><span class="sxs-lookup"><span data-stu-id="fda70-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**錯誤 \_ CS \_ 加密 \_ 現有的 \_ 加密 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="fda70-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-167">6019 (0x1783) </span><span class="sxs-lookup"><span data-stu-id="fda70-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-168">檔案已加密，應以用戶端加密模式開啟。</span><span class="sxs-lookup"><span data-stu-id="fda70-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**錯誤 \_ CS \_ 加密 \_ 新的 \_ 加密 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="fda70-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-170">6020 (0x1784) </span><span class="sxs-lookup"><span data-stu-id="fda70-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-171">正在建立新的加密檔案，因此必須提供 $EFS。</span><span class="sxs-lookup"><span data-stu-id="fda70-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**錯誤 \_ CS \_ 加密 \_ 檔 \_ 不是 \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="fda70-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-173">6021 (0x1785) </span><span class="sxs-lookup"><span data-stu-id="fda70-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-174">SMB 用戶端在非 CSE 檔案上要求 CSE FSCTL。</span><span class="sxs-lookup"><span data-stu-id="fda70-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**錯誤 \_ 加密 \_ 原則 \_ 拒絕 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="fda70-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-176">6022 (0x1786) </span><span class="sxs-lookup"><span data-stu-id="fda70-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-177">原則封鎖了要求的作業。</span><span class="sxs-lookup"><span data-stu-id="fda70-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="fda70-178">如需相關資訊，請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="fda70-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**錯誤 \_ \_ 找不到瀏覽器 \_ 伺服器 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-180">6118 (0x17E6) </span><span class="sxs-lookup"><span data-stu-id="fda70-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-181">目前無法使用此工作組的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="fda70-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**已計畫的 \_ 電子 \_ 服務 \_ 非 \_ LOCALSYSTEM**</span><span class="sxs-lookup"><span data-stu-id="fda70-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-183">6200 (0x1838) </span><span class="sxs-lookup"><span data-stu-id="fda70-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-184">工作排程器服務必須設定為在系統帳戶中執行，才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="fda70-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="fda70-185">個別工作可設定為在其他帳戶中執行。</span><span class="sxs-lookup"><span data-stu-id="fda70-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**錯誤 \_ 記錄 \_ 磁區 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-187">6600 (0x19C8) </span><span class="sxs-lookup"><span data-stu-id="fda70-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-188">記錄服務遇到不正確記錄磁區。</span><span class="sxs-lookup"><span data-stu-id="fda70-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**錯誤 \_ 記錄 \_ 磁區同位檢查 \_ \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-190">6601 (0x19C9) </span><span class="sxs-lookup"><span data-stu-id="fda70-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-191">記錄服務遇到區塊同位不正確記錄磁區。</span><span class="sxs-lookup"><span data-stu-id="fda70-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**錯誤 \_ 記錄 \_ 磁區重新對應 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-193">6602 (0x19CA) </span><span class="sxs-lookup"><span data-stu-id="fda70-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-194">Log service 發生重新對應的記錄磁區。</span><span class="sxs-lookup"><span data-stu-id="fda70-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**錯誤 \_ 記錄檔 \_ 區塊 \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="fda70-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-196">6603 (0x19CB) </span><span class="sxs-lookup"><span data-stu-id="fda70-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-197">記錄服務遇到部分或不完整的記錄區塊。</span><span class="sxs-lookup"><span data-stu-id="fda70-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**錯誤 \_ 記錄檔 \_ 不正確 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="fda70-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-199">6604 (0x19CC) </span><span class="sxs-lookup"><span data-stu-id="fda70-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-200">記錄服務嘗試存取使用中記錄範圍以外的資料時。</span><span class="sxs-lookup"><span data-stu-id="fda70-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**錯誤 \_ 記錄 \_ 區塊已 \_ 用盡**</span><span class="sxs-lookup"><span data-stu-id="fda70-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-202">6605 (0x19CD) </span><span class="sxs-lookup"><span data-stu-id="fda70-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-203">記錄服務使用者封送處理緩衝區已用盡。</span><span class="sxs-lookup"><span data-stu-id="fda70-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**錯誤 \_ 記錄檔 \_ 讀取 \_ 內容 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-205">6606 (0x19CE) </span><span class="sxs-lookup"><span data-stu-id="fda70-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-206">記錄服務嘗試從讀取內容不正確封送處理區域讀取。</span><span class="sxs-lookup"><span data-stu-id="fda70-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**錯誤 \_ 記錄檔 \_ 重新開機 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-208">6607 (0x19CF) </span><span class="sxs-lookup"><span data-stu-id="fda70-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-209">記錄服務發生不正確記錄重新開機區域。</span><span class="sxs-lookup"><span data-stu-id="fda70-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**錯誤 \_ 記錄 \_ 區塊 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="fda70-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-211">6608 (0x19D0) </span><span class="sxs-lookup"><span data-stu-id="fda70-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-212">記錄服務遇到不正確記錄區塊版本。</span><span class="sxs-lookup"><span data-stu-id="fda70-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**錯誤 \_ 記錄檔 \_ 區塊 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-214">6609 (0x19D1) </span><span class="sxs-lookup"><span data-stu-id="fda70-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-215">記錄服務遇到不正確記錄區塊。</span><span class="sxs-lookup"><span data-stu-id="fda70-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**錯誤 \_ 記錄 \_ 讀取 \_ 模式 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-217">6610 (0x19D2) </span><span class="sxs-lookup"><span data-stu-id="fda70-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-218">記錄服務嘗試以不正確讀取模式讀取記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**錯誤 \_ 記錄檔 \_ 無 \_ 重新開機**</span><span class="sxs-lookup"><span data-stu-id="fda70-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-220">6611 (0x19D3) </span><span class="sxs-lookup"><span data-stu-id="fda70-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-221">記錄服務發現沒有重新開機區域的記錄資料流程。</span><span class="sxs-lookup"><span data-stu-id="fda70-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="fda70-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-223">6612 (0x19D4) </span><span class="sxs-lookup"><span data-stu-id="fda70-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-224">記錄服務發生損毀的中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-226">6613 (0x19D5) </span><span class="sxs-lookup"><span data-stu-id="fda70-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-227">記錄服務發現無法由記錄檔系統建立的中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 不一致**</span><span class="sxs-lookup"><span data-stu-id="fda70-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-229">6614 (0x19D6) </span><span class="sxs-lookup"><span data-stu-id="fda70-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-230">記錄服務發現具有不一致資料的中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**錯誤 \_ 記錄檔 \_ 保留 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-232">6615 (0x19D7) </span><span class="sxs-lookup"><span data-stu-id="fda70-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-233">記錄服務嘗試配置或處置保留空間時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**錯誤 \_ 記錄檔無法 \_ \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="fda70-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-235">6616 (0x19D8) </span><span class="sxs-lookup"><span data-stu-id="fda70-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-236">記錄服務無法刪除記錄檔或檔案系統容器。</span><span class="sxs-lookup"><span data-stu-id="fda70-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**\_超過錯誤記錄 \_ 容器 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-238">6617 (0x19D9) </span><span class="sxs-lookup"><span data-stu-id="fda70-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-239">記錄服務已達到配置給記錄檔的可允許容器數目上限。</span><span class="sxs-lookup"><span data-stu-id="fda70-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_記錄檔 \_ 開頭 \_ 的錯誤記錄 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="fda70-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-241">6618 (0x19DA) </span><span class="sxs-lookup"><span data-stu-id="fda70-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-242">記錄服務已嘗試在記錄檔的開頭之前讀取或寫下。</span><span class="sxs-lookup"><span data-stu-id="fda70-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**\_ \_ \_ 已安裝錯誤記錄檔原則 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-244">6619 (0x19DB) </span><span class="sxs-lookup"><span data-stu-id="fda70-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-245">無法安裝記錄原則，因為已有相同類型的原則。</span><span class="sxs-lookup"><span data-stu-id="fda70-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**\_ \_ \_ 未安裝錯誤記錄檔原則 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-247">6620 (0x19DC) </span><span class="sxs-lookup"><span data-stu-id="fda70-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-248">要求時未安裝有問題的記錄檔原則。</span><span class="sxs-lookup"><span data-stu-id="fda70-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**錯誤 \_ 記錄檔 \_ 原則 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-250">6621 (0x19DD) </span><span class="sxs-lookup"><span data-stu-id="fda70-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-251">記錄上已安裝的原則集無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**錯誤 \_ 記錄檔 \_ 原則 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="fda70-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-253">6622 (0x19DE) </span><span class="sxs-lookup"><span data-stu-id="fda70-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-254">記錄檔中有問題的原則導致作業無法完成。</span><span class="sxs-lookup"><span data-stu-id="fda70-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**錯誤記錄檔已釘選封存 \_ \_ \_ \_ 結尾**</span><span class="sxs-lookup"><span data-stu-id="fda70-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-256">6623 (0x19DF) </span><span class="sxs-lookup"><span data-stu-id="fda70-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-257">無法回收記錄檔空間，因為記錄檔會由封存結尾釘選。</span><span class="sxs-lookup"><span data-stu-id="fda70-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**錯誤記錄檔 \_ \_ 記錄不 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="fda70-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-259">6624 (0x19E0) </span><span class="sxs-lookup"><span data-stu-id="fda70-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-260">記錄檔記錄不是記錄檔中的記錄。</span><span class="sxs-lookup"><span data-stu-id="fda70-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ \_ 保留 \_ 不正確錯誤記錄檔記錄**</span><span class="sxs-lookup"><span data-stu-id="fda70-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-262">6625 (0x19E1) </span><span class="sxs-lookup"><span data-stu-id="fda70-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-263">保留的記錄檔記錄數目或保留的記錄檔記錄數目的調整無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**錯誤 \_ 記錄 \_ 檔 \_ 保留的空間 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-265">6626 (0x19E2) </span><span class="sxs-lookup"><span data-stu-id="fda70-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-266">保留的記錄檔空間或記錄空間的調整無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**錯誤 \_ 記錄 \_ 結尾 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-268">6627 (0x19E3) </span><span class="sxs-lookup"><span data-stu-id="fda70-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-269">現用記錄檔的新或現有封存結尾或基底無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**錯誤 \_ 記錄檔已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="fda70-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-271">6628 (0x19E4) </span><span class="sxs-lookup"><span data-stu-id="fda70-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-272">記錄檔空間已用盡。</span><span class="sxs-lookup"><span data-stu-id="fda70-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**錯誤 \_ 無法 \_ \_ 調整 \_ 記錄大小**</span><span class="sxs-lookup"><span data-stu-id="fda70-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-274">6629 (0x19E5) </span><span class="sxs-lookup"><span data-stu-id="fda70-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-275">記錄檔無法設定為要求的大小。</span><span class="sxs-lookup"><span data-stu-id="fda70-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**錯誤記錄檔多工 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-277">6630 (0x19E6) </span><span class="sxs-lookup"><span data-stu-id="fda70-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-278">記錄已多工，不允許直接寫入實體記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**錯誤 \_ 記錄檔 \_ 專用**</span><span class="sxs-lookup"><span data-stu-id="fda70-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-280">6631 (0x19E7) </span><span class="sxs-lookup"><span data-stu-id="fda70-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-281">作業失敗，因為記錄檔是專用的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**錯誤 \_ 記錄檔封存 \_ \_ 未 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="fda70-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-283">6632 (0x19E8) </span><span class="sxs-lookup"><span data-stu-id="fda70-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-284">作業需要保存內容。</span><span class="sxs-lookup"><span data-stu-id="fda70-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**錯誤 \_ 記錄 \_ 檔 \_ 保存 \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="fda70-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-286">6633 (0x19E9) </span><span class="sxs-lookup"><span data-stu-id="fda70-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-287">記錄檔封存正在進行中。</span><span class="sxs-lookup"><span data-stu-id="fda70-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**錯誤 \_ 記錄檔 \_ 暫時**</span><span class="sxs-lookup"><span data-stu-id="fda70-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-289">6634 (0x19EA) </span><span class="sxs-lookup"><span data-stu-id="fda70-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-290">作業需要非暫時記錄檔，但記錄是暫時的。</span><span class="sxs-lookup"><span data-stu-id="fda70-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**錯誤 \_ 記錄檔 \_ 沒有 \_ 足夠的 \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="fda70-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-292">6635 (0x19EB) </span><span class="sxs-lookup"><span data-stu-id="fda70-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-293">記錄檔的讀取或寫入之前，必須至少有兩個容器。</span><span class="sxs-lookup"><span data-stu-id="fda70-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_ \_ \_ 已註冊錯誤記錄用戶端 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-295">6636 (0x19EC) </span><span class="sxs-lookup"><span data-stu-id="fda70-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-296">記錄用戶端已經在資料流程上註冊。</span><span class="sxs-lookup"><span data-stu-id="fda70-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**錯誤 \_ 記錄 \_ 用戶端 \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="fda70-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-298">6637 (0x19ED) </span><span class="sxs-lookup"><span data-stu-id="fda70-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-299">尚未在資料流程上註冊記錄用戶端。</span><span class="sxs-lookup"><span data-stu-id="fda70-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**錯誤 \_ 記錄檔 \_ 完整 \_ 處理常式 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="fda70-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-301">6638 (0x19EE) </span><span class="sxs-lookup"><span data-stu-id="fda70-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-302">已經提出要求來處理記錄檔的完整狀況。</span><span class="sxs-lookup"><span data-stu-id="fda70-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 讀取 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-304">6639 (0x19EF) </span><span class="sxs-lookup"><span data-stu-id="fda70-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-305">記錄服務嘗試從記錄容器讀取時，發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 寫入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-307">6640 (0x19F0) </span><span class="sxs-lookup"><span data-stu-id="fda70-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-308">記錄服務嘗試寫入記錄容器時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 開啟 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-310">6641 (0x19F1) </span><span class="sxs-lookup"><span data-stu-id="fda70-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-311">Log service 嘗試開啟記錄容器時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**錯誤 \_ 記錄 \_ 容器 \_ 狀態 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-313">6642 (0x19F2) </span><span class="sxs-lookup"><span data-stu-id="fda70-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-314">記錄服務在嘗試要求的動作時，發生不正確容器狀態。</span><span class="sxs-lookup"><span data-stu-id="fda70-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**錯誤 \_ 記錄檔 \_ 狀態 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-316">6643 (0x19F3) </span><span class="sxs-lookup"><span data-stu-id="fda70-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-317">記錄服務的狀態不正確，無法執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="fda70-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**已 \_ 釘選錯誤記錄檔 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-319">6644 (0x19F4) </span><span class="sxs-lookup"><span data-stu-id="fda70-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-320">記錄檔空間無法回收，因為已釘選記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**錯誤 \_ 記錄 \_ 中繼資料排清 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-322">6645 (0x19F5) </span><span class="sxs-lookup"><span data-stu-id="fda70-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-323">記錄中繼資料排清失敗。</span><span class="sxs-lookup"><span data-stu-id="fda70-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**錯誤 \_ 記錄 \_ 不一致的 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="fda70-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-325">6646 (0x19F6) </span><span class="sxs-lookup"><span data-stu-id="fda70-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-326">記錄和其容器的安全性不一致。</span><span class="sxs-lookup"><span data-stu-id="fda70-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**錯誤 \_ 記錄 \_ 附加的 \_ 清除 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-328">6647 (0x19F7) </span><span class="sxs-lookup"><span data-stu-id="fda70-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-329">記錄已附加至記錄檔或保留變更，但無法排清記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**錯誤記錄檔已釘選的 \_ \_ \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="fda70-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-331">6648 (0x19F8) </span><span class="sxs-lookup"><span data-stu-id="fda70-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-332">由於保留使用大部分的記錄空間，因此會釘選記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="fda70-333">釋放一些保留的記錄，讓空間可供使用。</span><span class="sxs-lookup"><span data-stu-id="fda70-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**錯誤 \_ 不正確 \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="fda70-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-335">6700 (0x1A2C) </span><span class="sxs-lookup"><span data-stu-id="fda70-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-336">與這項作業相關聯的交易控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**錯誤 \_ 交易 \_ 未 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="fda70-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-338">6701 (0x1A2D) </span><span class="sxs-lookup"><span data-stu-id="fda70-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-339">要求的作業是在已不再使用的交易內容中進行。</span><span class="sxs-lookup"><span data-stu-id="fda70-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**錯誤 \_ 交易 \_ 要求 \_ 無效 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-341">6702 (0x1A2E) </span><span class="sxs-lookup"><span data-stu-id="fda70-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-342">在交易對象的目前狀態中，要求的作業無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**\_ \_ 未要求錯誤 \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="fda70-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-344">6703 (0x1A2F) </span><span class="sxs-lookup"><span data-stu-id="fda70-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-345">呼叫端已呼叫回應 API，但因為 TM 未對呼叫端發出對應的要求，所以不需要回應。</span><span class="sxs-lookup"><span data-stu-id="fda70-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**錯誤 \_ 交易 \_ 已經 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="fda70-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-347">6704 (0x1A30) </span><span class="sxs-lookup"><span data-stu-id="fda70-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-348">因為交易已經中止，所以執行要求的作業太晚。</span><span class="sxs-lookup"><span data-stu-id="fda70-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**錯誤 \_ 交易 \_ 已 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="fda70-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-350">6705 (0x1A31) </span><span class="sxs-lookup"><span data-stu-id="fda70-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-351">因為交易已經過認可，所以執行要求的作業太晚。</span><span class="sxs-lookup"><span data-stu-id="fda70-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**錯誤 \_ TM \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-353">6706 (0x1A32) </span><span class="sxs-lookup"><span data-stu-id="fda70-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-354">交易管理員無法成功初始化。</span><span class="sxs-lookup"><span data-stu-id="fda70-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="fda70-355">不支援交易作業。</span><span class="sxs-lookup"><span data-stu-id="fda70-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**錯誤 \_ RESOURCEMANAGER \_ 唯讀 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-357">6707 (0x1A33) </span><span class="sxs-lookup"><span data-stu-id="fda70-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-358">指定的 ResourceManager 對此交易下的資源沒有任何變更或更新。</span><span class="sxs-lookup"><span data-stu-id="fda70-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**錯誤 \_ 交易 \_ 未 \_ 聯結**</span><span class="sxs-lookup"><span data-stu-id="fda70-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-360">6708 (0x1A34) </span><span class="sxs-lookup"><span data-stu-id="fda70-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-361">資源管理員已嘗試準備尚未成功聯結的交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**錯誤 \_ 交易 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="fda70-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-363">6709 (0x1A35) </span><span class="sxs-lookup"><span data-stu-id="fda70-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-364">交易對象已有較佳的登記，而且呼叫端嘗試的作業已建立新的高階。</span><span class="sxs-lookup"><span data-stu-id="fda70-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="fda70-365">只允許單一的上級登記。</span><span class="sxs-lookup"><span data-stu-id="fda70-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**錯誤 \_ CRM \_ 通訊協定 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="fda70-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-367">6710 (0x1A36) </span><span class="sxs-lookup"><span data-stu-id="fda70-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-368">RM 嘗試註冊已存在的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fda70-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**錯誤 \_ 交易 \_ 傳播 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-370">6711 (0x1A37) </span><span class="sxs-lookup"><span data-stu-id="fda70-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-371">嘗試傳播交易失敗。</span><span class="sxs-lookup"><span data-stu-id="fda70-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**\_ \_ \_ 找不到 CRM 通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-373">6712 (0x1A38) </span><span class="sxs-lookup"><span data-stu-id="fda70-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-374">要求的傳播通訊協定未註冊為 CRM。</span><span class="sxs-lookup"><span data-stu-id="fda70-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**錯誤 \_ 交易 \_ 不正確 \_ 馬紹爾 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="fda70-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-376">6713 (0x1A39) </span><span class="sxs-lookup"><span data-stu-id="fda70-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-377">傳入 PushTransaction 或 PullTransaction 的緩衝區格式不正確。</span><span class="sxs-lookup"><span data-stu-id="fda70-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**錯誤 \_ 目前 \_ 的 \_ 交易 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-379">6714 (0x1A3A) </span><span class="sxs-lookup"><span data-stu-id="fda70-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-380">與執行緒相關聯的目前交易內容不是交易對象的有效控制碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ 找不到錯誤交易 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-382">6715 (0x1A3B) </span><span class="sxs-lookup"><span data-stu-id="fda70-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-383">無法開啟指定的交易對象，因為找不到該物件。</span><span class="sxs-lookup"><span data-stu-id="fda70-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**\_ \_ 找不到錯誤 RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-385">6716 (0x1A3C) </span><span class="sxs-lookup"><span data-stu-id="fda70-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-386">無法開啟指定的 ResourceManager 物件，因為找不到它。</span><span class="sxs-lookup"><span data-stu-id="fda70-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ 找不到錯誤登記 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-388">6717 (0x1A3D) </span><span class="sxs-lookup"><span data-stu-id="fda70-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-389">無法開啟指定的登錄物件，因為找不到該物件。</span><span class="sxs-lookup"><span data-stu-id="fda70-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**\_ \_ \_ 找不到錯誤的錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-391">6718 (0x1A3E) </span><span class="sxs-lookup"><span data-stu-id="fda70-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-392">無法開啟指定的 TransactionManager 物件，因為找不到它。</span><span class="sxs-lookup"><span data-stu-id="fda70-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**錯誤的 \_ TRANSACTIONMANAGER \_ 未 \_ 上線**</span><span class="sxs-lookup"><span data-stu-id="fda70-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-394">6719 (0x1A3F) </span><span class="sxs-lookup"><span data-stu-id="fda70-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-395">無法建立或開啟指定的物件，因為其相關聯的 TransactionManager 不在線上。</span><span class="sxs-lookup"><span data-stu-id="fda70-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="fda70-396">您必須先呼叫 RecoverTransactionManager 來復原到記錄檔的結尾，然後才能開啟其交易或 ResourceManager 命名空間中的物件，以使其完全上線。</span><span class="sxs-lookup"><span data-stu-id="fda70-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="fda70-397">此外，將記錄寫入記錄檔的錯誤可能會導致 TransactionManager 離線。</span><span class="sxs-lookup"><span data-stu-id="fda70-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**錯誤 \_ TRANSACTIONMANAGER \_ 修復 \_ 名稱 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="fda70-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-399">6720 (0x1A40) </span><span class="sxs-lookup"><span data-stu-id="fda70-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-400">指定的 TransactionManager 無法在 Ob 命名空間中建立其記錄檔中所包含的物件。</span><span class="sxs-lookup"><span data-stu-id="fda70-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="fda70-401">因此，無法復原 TransactionManager。</span><span class="sxs-lookup"><span data-stu-id="fda70-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**錯誤 \_ 交易 \_ 非 \_ 根**</span><span class="sxs-lookup"><span data-stu-id="fda70-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-403">6721 (0x1A41) </span><span class="sxs-lookup"><span data-stu-id="fda70-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-404">因為為登記指定的交易對象是交易的次級分支，所以無法完成在此交易對象上建立高階登記的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fda70-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="fda70-405">只有交易的根目錄才能以較上層的形式登記。</span><span class="sxs-lookup"><span data-stu-id="fda70-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**錯誤 \_ 交易 \_ 物件已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="fda70-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-407">6722 (0x1A42) </span><span class="sxs-lookup"><span data-stu-id="fda70-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-408">因為相關聯的交易管理員或資源管理員已經關閉，所以控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="fda70-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**錯誤 \_ 交易 \_ 回應 \_ 未 \_ 登記**</span><span class="sxs-lookup"><span data-stu-id="fda70-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-410">6723 (0x1A43) </span><span class="sxs-lookup"><span data-stu-id="fda70-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-411">無法在這個高階登記上執行指定的作業，因為未在 NotificationMask 中使用對應的完成回應來建立登記。</span><span class="sxs-lookup"><span data-stu-id="fda70-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**錯誤 \_ 交易 \_ 記錄 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="fda70-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-413">6724 (0x1A44) </span><span class="sxs-lookup"><span data-stu-id="fda70-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-414">無法執行指定的作業，因為記錄的記錄太長。</span><span class="sxs-lookup"><span data-stu-id="fda70-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="fda70-415">發生這種情況的原因有兩種：這項交易的登記太多，或代表這些登記記錄的組合 Ms-fve-recoveryinformation 太長。</span><span class="sxs-lookup"><span data-stu-id="fda70-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_ \_ \_ 不支援隱含交易 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-417">6725 (0x1A45) </span><span class="sxs-lookup"><span data-stu-id="fda70-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-418">不支援隱含交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**\_違反錯誤交易 \_ 完整性 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-420">6726 (0x1A46) </span><span class="sxs-lookup"><span data-stu-id="fda70-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-421">核心交易管理員必須中止或忘記交易，因為它封鎖了轉寄進度。</span><span class="sxs-lookup"><span data-stu-id="fda70-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**錯誤 \_ TRANSACTIONMANAGER \_ 識別 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="fda70-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-423">6727 (0x1A47) </span><span class="sxs-lookup"><span data-stu-id="fda70-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-424">提供的 TransactionManager 身分識別不符合 TransactionManager 記錄檔中所記錄的身分識別。</span><span class="sxs-lookup"><span data-stu-id="fda70-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**錯誤 \_ RM \_ 無法 \_ \_ 凍結 \_ \_ 快照集**</span><span class="sxs-lookup"><span data-stu-id="fda70-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-426">6728 (0x1A48) </span><span class="sxs-lookup"><span data-stu-id="fda70-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-427">此快照集作業無法繼續，因為交易式資源管理員無法以其目前的狀態凍結。</span><span class="sxs-lookup"><span data-stu-id="fda70-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="fda70-428">請再試一次。</span><span class="sxs-lookup"><span data-stu-id="fda70-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**錯誤 \_ 交易 \_ 必須 \_ WRITETHROUGH**</span><span class="sxs-lookup"><span data-stu-id="fda70-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-430">6729 (0x1A49) </span><span class="sxs-lookup"><span data-stu-id="fda70-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-431">無法使用指定的 EnlistmentMask 來登記交易，因為交易已完成 PrePrepare 階段。</span><span class="sxs-lookup"><span data-stu-id="fda70-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="fda70-432">為了確保正確性，ResourceManager 必須切換至寫入模式，並停止在此交易內快取資料。</span><span class="sxs-lookup"><span data-stu-id="fda70-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="fda70-433">只針對後續的交易階段進行登記，可能仍會成功。</span><span class="sxs-lookup"><span data-stu-id="fda70-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**錯誤 \_ 交易 \_ 沒有 \_ 卓越的**</span><span class="sxs-lookup"><span data-stu-id="fda70-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-435">6730 (0x1A4A) </span><span class="sxs-lookup"><span data-stu-id="fda70-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-436">交易沒有較佳的登記。</span><span class="sxs-lookup"><span data-stu-id="fda70-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**可能發生錯誤 \_ 啟發式 \_ 損毀 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-438">6731 (0x1A4B) </span><span class="sxs-lookup"><span data-stu-id="fda70-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-439">嘗試認可交易已完成，但交易樹狀結構的某些部分可能因為啟發學習法而無法成功認可。</span><span class="sxs-lookup"><span data-stu-id="fda70-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="fda70-440">因此，可能在交易中修改某些資料可能尚未認可，而導致交易不一致。</span><span class="sxs-lookup"><span data-stu-id="fda70-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="fda70-441">可能的話，請檢查相關資料的一致性。</span><span class="sxs-lookup"><span data-stu-id="fda70-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**\_交易 \_ 衝突錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-443">6800 (0x1A90) </span><span class="sxs-lookup"><span data-stu-id="fda70-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-444">函數嘗試使用保留給另一個交易使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="fda70-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**錯誤 \_ RM \_ 未 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="fda70-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-446">6801 (0x1A91) </span><span class="sxs-lookup"><span data-stu-id="fda70-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-447">指定資源管理員內的交易支援未啟動，或由於錯誤而關閉。</span><span class="sxs-lookup"><span data-stu-id="fda70-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**錯誤的 \_ RM \_ 中繼資料 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="fda70-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-449">6802 (0x1A92) </span><span class="sxs-lookup"><span data-stu-id="fda70-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-450">RM 的中繼資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="fda70-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="fda70-451">RM 將無法運作。</span><span class="sxs-lookup"><span data-stu-id="fda70-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**錯誤 \_ 目錄 \_ 不是 \_ RM**</span><span class="sxs-lookup"><span data-stu-id="fda70-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-453">6803 (0x1A93) </span><span class="sxs-lookup"><span data-stu-id="fda70-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-454">指定的目錄不包含 resource manager。</span><span class="sxs-lookup"><span data-stu-id="fda70-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**錯誤 \_ 交易 \_ 不支援 \_ 遠端**</span><span class="sxs-lookup"><span data-stu-id="fda70-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-456">6805 (0x1A95) </span><span class="sxs-lookup"><span data-stu-id="fda70-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-457">遠端伺服器或共用不支援交易檔案作業。</span><span class="sxs-lookup"><span data-stu-id="fda70-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**錯誤 \_ 記錄 \_ 重 \_ 設 \_ 大小無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-459">6806 (0x1A96) </span><span class="sxs-lookup"><span data-stu-id="fda70-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-460">要求的記錄檔大小無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**錯誤 \_ 物件 \_ 不再 \_ \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="fda70-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-462">6807 (0x1A97) </span><span class="sxs-lookup"><span data-stu-id="fda70-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-463">交易儲存點復原已刪除對應至控制碼 (檔案、資料流程、連結) 的物件。</span><span class="sxs-lookup"><span data-stu-id="fda70-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資料流程迷你**</span><span class="sxs-lookup"><span data-stu-id="fda70-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-465">6808 (0x1A98) </span><span class="sxs-lookup"><span data-stu-id="fda70-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-466">在開啟此交易檔案時，找不到指定的檔案迷你檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**錯誤 \_ 資料流程 \_ 迷你 \_ 版本 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-468">6809 (0x1A99) </span><span class="sxs-lookup"><span data-stu-id="fda70-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-469">找到指定的檔案迷你檔案，但已失效。</span><span class="sxs-lookup"><span data-stu-id="fda70-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="fda70-470">最可能的原因是交易儲存點復原。</span><span class="sxs-lookup"><span data-stu-id="fda70-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**\_ \_ \_ 從 \_ 指定的 \_ 交易無法存取的錯誤迷你**</span><span class="sxs-lookup"><span data-stu-id="fda70-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-472">6810 (0x1A9A) </span><span class="sxs-lookup"><span data-stu-id="fda70-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-473">只有在建立迷你的交易時，才會在其內容中開啟。</span><span class="sxs-lookup"><span data-stu-id="fda70-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**錯誤 \_ 無法 \_ \_ \_ 使用 \_ MODIFY \_ 意圖開啟迷你**</span><span class="sxs-lookup"><span data-stu-id="fda70-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-475">6811 (0x1A9B) </span><span class="sxs-lookup"><span data-stu-id="fda70-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-476">您無法使用修改存取來開啟迷你。</span><span class="sxs-lookup"><span data-stu-id="fda70-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**錯誤 \_ 無法 \_ 建立 \_ 更多 \_ 串流 \_ MINIVERSIONS**</span><span class="sxs-lookup"><span data-stu-id="fda70-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-478">6812 (0x1A9C) </span><span class="sxs-lookup"><span data-stu-id="fda70-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-479">您無法為此資料流程建立任何其他 miniversions。</span><span class="sxs-lookup"><span data-stu-id="fda70-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**\_遠端檔案 \_ \_ 版本 \_ 不符的錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-481">6814 (0x1A9E) </span><span class="sxs-lookup"><span data-stu-id="fda70-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-482">遠端伺服器針對以交易開啟的檔案傳送了不相符的版本號碼或 Fid。</span><span class="sxs-lookup"><span data-stu-id="fda70-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**錯誤 \_ 控制碼不再 \_ \_ \_ 有效**</span><span class="sxs-lookup"><span data-stu-id="fda70-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-484">6815 (0x1A9F) </span><span class="sxs-lookup"><span data-stu-id="fda70-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-485">交易已將控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="fda70-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="fda70-486">最可能的原因是當交易結束或回復至儲存點時，檔案上有記憶體對應或開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**\_沒有 \_ TXF \_ 中繼資料的錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-488">6816 (0x1AA0) </span><span class="sxs-lookup"><span data-stu-id="fda70-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-489">檔案上沒有交易中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fda70-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**偵測 \_ 到錯誤記錄檔 \_ 損毀 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-491">6817 (0x1AA1) </span><span class="sxs-lookup"><span data-stu-id="fda70-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-492">記錄資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="fda70-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**無法 \_ \_ \_ 使用 \_ 控制碼 \_ 開啟來復原錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-494">6818 (0x1AA2) </span><span class="sxs-lookup"><span data-stu-id="fda70-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-495">無法復原檔案，因為它上仍有控制碼開啟。</span><span class="sxs-lookup"><span data-stu-id="fda70-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**\_RM \_ 中斷連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-497">6819 (0x1AA3) </span><span class="sxs-lookup"><span data-stu-id="fda70-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-498">交易結果無法使用，因為負責該交易的資源管理員已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="fda70-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**錯誤 \_ 登記 \_ 不 \_ 佳**</span><span class="sxs-lookup"><span data-stu-id="fda70-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-500">6820 (0x1AA4) </span><span class="sxs-lookup"><span data-stu-id="fda70-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-501">要求遭到拒絕，因為有問題的登記不是高階登記。</span><span class="sxs-lookup"><span data-stu-id="fda70-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**\_ \_ 不 \_ 需要復原錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-503">6821 (0x1AA5) </span><span class="sxs-lookup"><span data-stu-id="fda70-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-504">交易式資源管理員已經是一致的。</span><span class="sxs-lookup"><span data-stu-id="fda70-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="fda70-505">不需要復原。</span><span class="sxs-lookup"><span data-stu-id="fda70-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**錯誤 \_ RM \_ 已 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="fda70-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-507">6822 (0x1AA6) </span><span class="sxs-lookup"><span data-stu-id="fda70-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-508">交易式資源管理員已經啟動。</span><span class="sxs-lookup"><span data-stu-id="fda70-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**錯誤檔案身分 \_ \_ 識別 \_ 不是 \_ 持續性**</span><span class="sxs-lookup"><span data-stu-id="fda70-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-510">6823 (0x1AA7) </span><span class="sxs-lookup"><span data-stu-id="fda70-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-511">無法以交易方式開啟檔案，因為它的身分識別取決於無法解析之交易的結果。</span><span class="sxs-lookup"><span data-stu-id="fda70-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**錯誤 \_ 無法 \_ 中斷 \_ 交易 \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="fda70-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-513">6824 (0x1AA8) </span><span class="sxs-lookup"><span data-stu-id="fda70-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-514">無法執行作業，因為另一個交易取決於此屬性不會變更的事實。</span><span class="sxs-lookup"><span data-stu-id="fda70-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**無法 \_ \_ 跨 \_ RM \_ 界限的錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-516">6825 (0x1AA9) </span><span class="sxs-lookup"><span data-stu-id="fda70-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-517">作業牽涉到具有兩個交易式資源管理員的單一檔案，因此不允許。</span><span class="sxs-lookup"><span data-stu-id="fda70-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**錯誤 \_ TXF \_ 目錄 \_ 不是 \_ 空的**</span><span class="sxs-lookup"><span data-stu-id="fda70-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-519">6826 (0x1AAA) </span><span class="sxs-lookup"><span data-stu-id="fda70-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-520">$Txf 目錄必須是空的，此作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="fda70-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_INDOUBT \_ 交易 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-522">6827 (0x1AAB) </span><span class="sxs-lookup"><span data-stu-id="fda70-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-523">作業會讓交易式資源管理員處於不一致的狀態，因此不允許。</span><span class="sxs-lookup"><span data-stu-id="fda70-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**錯誤 \_ TM \_ VOLATILE**</span><span class="sxs-lookup"><span data-stu-id="fda70-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-525">6828 (0x1AAC) </span><span class="sxs-lookup"><span data-stu-id="fda70-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-526">無法完成作業，因為交易管理員沒有記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fda70-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**錯誤 \_ 復原 \_ 計時器已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="fda70-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-528">6829 (0x1AAD) </span><span class="sxs-lookup"><span data-stu-id="fda70-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-529">無法排程復原，因為先前排程的復原已執行或已排入佇列等候執行。</span><span class="sxs-lookup"><span data-stu-id="fda70-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**錯誤 \_ TXF \_ 屬性 \_ 已損毀**</span><span class="sxs-lookup"><span data-stu-id="fda70-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-531">6830 (0x1AAE) </span><span class="sxs-lookup"><span data-stu-id="fda70-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-532">檔案或目錄上的交易式中繼資料屬性已損毀且無法讀取。</span><span class="sxs-lookup"><span data-stu-id="fda70-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許有錯誤 \_ 的 EFS \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-534">6831 (0x1AAF) </span><span class="sxs-lookup"><span data-stu-id="fda70-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-535">因為交易正在使用中，所以無法完成加密作業。</span><span class="sxs-lookup"><span data-stu-id="fda70-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**錯誤 \_ 交易 \_ 開啟 \_ 不 \_ 允許**</span><span class="sxs-lookup"><span data-stu-id="fda70-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-537">6832 (0x1AB0) </span><span class="sxs-lookup"><span data-stu-id="fda70-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-538">此物件不允許在交易中開啟。</span><span class="sxs-lookup"><span data-stu-id="fda70-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**錯誤 \_ 記錄檔 \_ 成長 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fda70-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-540">6833 (0x1AB1) </span><span class="sxs-lookup"><span data-stu-id="fda70-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-541">嘗試在交易式資源管理員的記錄檔中建立空間失敗。</span><span class="sxs-lookup"><span data-stu-id="fda70-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="fda70-542">失敗狀態已記錄在事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="fda70-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**錯誤 \_ 交易 \_ 對應 \_ 不支援的 \_ 遠端**</span><span class="sxs-lookup"><span data-stu-id="fda70-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-544">6834 (0x1AB2) </span><span class="sxs-lookup"><span data-stu-id="fda70-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-545">記憶體對應 (建立對應的區段) 不支援交易下的遠端檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**\_已有錯誤的 TXF \_ 中繼資料 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-547">6835 (0x1AB3) </span><span class="sxs-lookup"><span data-stu-id="fda70-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-548">交易中繼資料已存在於此檔案中，無法被取代。</span><span class="sxs-lookup"><span data-stu-id="fda70-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_ \_ \_ \_ 未設定錯誤交易範圍 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="fda70-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-550">6836 (0x1AB4) </span><span class="sxs-lookup"><span data-stu-id="fda70-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-551">無法輸入交易範圍，因為範圍處理常式尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="fda70-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ 需要升級錯誤 \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="fda70-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-553">6837 (0x1AB5) </span><span class="sxs-lookup"><span data-stu-id="fda70-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-554">需要升級，才能讓資源管理員登錄，但交易已設定為不允許。</span><span class="sxs-lookup"><span data-stu-id="fda70-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**錯誤 \_ 無法 \_ \_ \_ 在交易中 \_ 執行檔案**</span><span class="sxs-lookup"><span data-stu-id="fda70-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-556">6838 (0x1AB6) </span><span class="sxs-lookup"><span data-stu-id="fda70-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-557">這個檔案會在未解析的交易中開啟以供修改，而且只能由交易讀取器開啟以供執行。</span><span class="sxs-lookup"><span data-stu-id="fda70-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**錯誤 \_ 交易 \_ 未 \_ 凍結**</span><span class="sxs-lookup"><span data-stu-id="fda70-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-559">6839 (0x1AB7) </span><span class="sxs-lookup"><span data-stu-id="fda70-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-560">已忽略解除凍結凍結交易的要求，因為先前尚未凍結交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**錯誤 \_ 交易 \_ 凍結 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="fda70-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-562">6840 (0x1AB8) </span><span class="sxs-lookup"><span data-stu-id="fda70-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-563">因為凍結已在進行中，所以無法凍結交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**錯誤 \_ 而非 \_ 快照集 \_ 磁片區**</span><span class="sxs-lookup"><span data-stu-id="fda70-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-565">6841 (0x1AB9) </span><span class="sxs-lookup"><span data-stu-id="fda70-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-566">目標磁片區不是快照集磁片區。</span><span class="sxs-lookup"><span data-stu-id="fda70-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="fda70-567">這項作業只適用于裝載為快照集的磁片區。</span><span class="sxs-lookup"><span data-stu-id="fda70-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**\_沒有 \_ \_ 開啟的檔案的儲存點 \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-569">6842 (0x1ABA) </span><span class="sxs-lookup"><span data-stu-id="fda70-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-570">儲存點作業失敗，因為交易上的檔案已開啟。</span><span class="sxs-lookup"><span data-stu-id="fda70-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="fda70-571">這是不允許的。</span><span class="sxs-lookup"><span data-stu-id="fda70-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**錯誤 \_ 資料 \_ 遺失 \_ 修復**</span><span class="sxs-lookup"><span data-stu-id="fda70-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-573">6843 (0x1ABB) </span><span class="sxs-lookup"><span data-stu-id="fda70-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-574">Windows 已在檔案中發現損毀，且該檔案已修復。</span><span class="sxs-lookup"><span data-stu-id="fda70-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="fda70-575">可能發生資料遺失。</span><span class="sxs-lookup"><span data-stu-id="fda70-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許 \_ 錯誤 \_ SPARSE**</span><span class="sxs-lookup"><span data-stu-id="fda70-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-577">6844 (0x1ABC) </span><span class="sxs-lookup"><span data-stu-id="fda70-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-578">無法完成稀疏作業，因為檔案上有作用中的交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**錯誤 \_ TM 身分 \_ 識別 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="fda70-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-580">6845 (0x1ABD) </span><span class="sxs-lookup"><span data-stu-id="fda70-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-581">因為儲存在記錄檔中的 Tm 身分識別不符合作為引數傳入的 Tm 身分識別，所以建立 TransactionManager 物件的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="fda70-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**錯誤 \_ 浮動 \_ 區段**</span><span class="sxs-lookup"><span data-stu-id="fda70-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-583">6846 (0x1ABE) </span><span class="sxs-lookup"><span data-stu-id="fda70-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-584">嘗試在已浮動為交易結束結果的區段物件上使用 i/o。</span><span class="sxs-lookup"><span data-stu-id="fda70-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="fda70-585">沒有有效的資料。</span><span class="sxs-lookup"><span data-stu-id="fda70-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**錯誤 \_ 無法 \_ 接受 \_ 交易 \_ 工作**</span><span class="sxs-lookup"><span data-stu-id="fda70-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-587">6847 (0x1ABF) </span><span class="sxs-lookup"><span data-stu-id="fda70-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-588">交易式資源管理員目前無法接受交易工作，因為暫時性狀況（例如資源不足）。</span><span class="sxs-lookup"><span data-stu-id="fda70-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**錯誤 \_ 無法 \_ 中止 \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="fda70-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-590">6848 (0x1AC0) </span><span class="sxs-lookup"><span data-stu-id="fda70-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-591">交易式資源管理員的 tranactions 未處理太多，無法中止。</span><span class="sxs-lookup"><span data-stu-id="fda70-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="fda70-592">交易式資源管理器已關閉。</span><span class="sxs-lookup"><span data-stu-id="fda70-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**錯誤 \_ 的 \_ 群集錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-594">6849 (0x1AC1) </span><span class="sxs-lookup"><span data-stu-id="fda70-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-595">因為磁片上的叢集不正確，所以無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="fda70-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許 \_ \_ 有錯誤壓縮**</span><span class="sxs-lookup"><span data-stu-id="fda70-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-597">6850 (0x1AC2) </span><span class="sxs-lookup"><span data-stu-id="fda70-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-598">無法完成壓縮作業，因為檔案上有作用中的交易。</span><span class="sxs-lookup"><span data-stu-id="fda70-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**錯誤 \_ 磁片區中途 \_ 損壞**</span><span class="sxs-lookup"><span data-stu-id="fda70-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-600">6851 (0x1AC3) </span><span class="sxs-lookup"><span data-stu-id="fda70-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-601">無法完成操作，因為磁片區已中途變更。</span><span class="sxs-lookup"><span data-stu-id="fda70-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="fda70-602">請執行 chkdsk，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="fda70-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**\_ \_ \_ \_ 在交易中沒有連結追蹤的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-604">6852 (0x1AC4) </span><span class="sxs-lookup"><span data-stu-id="fda70-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-605">因為交易正在使用中，所以無法完成連結追蹤作業。</span><span class="sxs-lookup"><span data-stu-id="fda70-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_ \_ \_ 交易中不支援 \_ \_ 錯誤作業**</span><span class="sxs-lookup"><span data-stu-id="fda70-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-607">6853 (0x1AC5) </span><span class="sxs-lookup"><span data-stu-id="fda70-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-608">這項作業無法在交易中執行。</span><span class="sxs-lookup"><span data-stu-id="fda70-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**錯誤 \_ 過期的 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="fda70-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-610">6854 (0x1AC6) </span><span class="sxs-lookup"><span data-stu-id="fda70-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-611">控制碼已不再與交易的關聯正確。</span><span class="sxs-lookup"><span data-stu-id="fda70-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="fda70-612">它可能已在交易式資源管理員中開啟，之後會強制重新開機。</span><span class="sxs-lookup"><span data-stu-id="fda70-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="fda70-613">請關閉控點，並開啟一個新控制碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**錯誤 \_ 交易 \_ 未 \_ 登記**</span><span class="sxs-lookup"><span data-stu-id="fda70-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-615">6855 (0x1AC7) </span><span class="sxs-lookup"><span data-stu-id="fda70-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-616">無法執行指定的作業，因為未在交易中登記資源管理員。</span><span class="sxs-lookup"><span data-stu-id="fda70-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**錯誤 \_ CTX \_ WINSTATION \_ 名稱 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-618">7001 (0x1B59) </span><span class="sxs-lookup"><span data-stu-id="fda70-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-619">指定的會話名稱無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**\_CTX \_ 不正確 \_ PD 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-621">7002 (0x1B5A) </span><span class="sxs-lookup"><span data-stu-id="fda70-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-622">指定的通訊協定驅動程式無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**\_ \_ \_ 找不到 CTX \_ PD 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-624">7003 (0x1B5B) </span><span class="sxs-lookup"><span data-stu-id="fda70-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-625">在系統路徑中找不到指定的通訊協定驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda70-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**錯誤 \_ CTX \_ \_ 找不 \_ 到 WD**</span><span class="sxs-lookup"><span data-stu-id="fda70-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-627">7004 (0x1B5C) </span><span class="sxs-lookup"><span data-stu-id="fda70-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-628">在系統路徑中找不到指定的終端機連接驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda70-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**\_CTX \_ 無法 \_ 建立 \_ EVENTLOG \_ 專案時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-630">7005 (0x1B5D) </span><span class="sxs-lookup"><span data-stu-id="fda70-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-631">無法為此會話建立事件記錄的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**\_CTX \_ 服務 \_ 名稱 \_ 衝突時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-633">7006 (0x1B5E) </span><span class="sxs-lookup"><span data-stu-id="fda70-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-634">系統上已有相同名稱的服務存在。</span><span class="sxs-lookup"><span data-stu-id="fda70-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**\_CTX \_ 關閉 \_ 擱置中時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-636">7007 (0x1B5F) </span><span class="sxs-lookup"><span data-stu-id="fda70-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-637">會話上的關閉作業暫止。</span><span class="sxs-lookup"><span data-stu-id="fda70-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**\_CTX \_ 無 \_ OUTBUF 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-639">7008 (0x1B60) </span><span class="sxs-lookup"><span data-stu-id="fda70-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-640">沒有可用的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fda70-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**\_CTX \_ \_ \_ \_ 找不到數據機 INF 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-642">7009 (0x1B61) </span><span class="sxs-lookup"><span data-stu-id="fda70-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-643">數據機。找不到 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fda70-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**\_CTX \_ 不正確 \_ MODEMNAME 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-645">7010 (0x1B62) </span><span class="sxs-lookup"><span data-stu-id="fda70-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-646">在數據機中找不到數據機名稱。</span><span class="sxs-lookup"><span data-stu-id="fda70-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**\_CTX \_ 數據機 \_ 回應 \_ 錯誤時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-648">7011 (0x1B63) </span><span class="sxs-lookup"><span data-stu-id="fda70-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-649">數據機未接受傳送給它的命令。</span><span class="sxs-lookup"><span data-stu-id="fda70-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="fda70-650">確認設定的數據機名稱符合連接的數據機。</span><span class="sxs-lookup"><span data-stu-id="fda70-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**\_CTX \_ 數據機 \_ 回應 \_ 超時時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-652">7012 (0x1B64) </span><span class="sxs-lookup"><span data-stu-id="fda70-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-653">數據機未回應傳送給它的命令。</span><span class="sxs-lookup"><span data-stu-id="fda70-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="fda70-654">確認數據機已正確連接電源並開啟電源。</span><span class="sxs-lookup"><span data-stu-id="fda70-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**\_CTX \_ 數據機 \_ 回應 \_ 無 \_ 貨運公司時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-656">7013 (0x1B65) </span><span class="sxs-lookup"><span data-stu-id="fda70-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-657">因為中斷連線，所以電訊廠商偵測失敗或貨運公司已中斷。</span><span class="sxs-lookup"><span data-stu-id="fda70-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**\_CTX \_ 數據機 \_ 回應 \_ 沒有 \_ 撥號撥號時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-659">7014 (0x1B66) </span><span class="sxs-lookup"><span data-stu-id="fda70-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-660">在所需時間內未偵測到撥號音。</span><span class="sxs-lookup"><span data-stu-id="fda70-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="fda70-661">確認電話纜線已正確連接且正常運作。</span><span class="sxs-lookup"><span data-stu-id="fda70-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**\_CTX \_ 數據機 \_ 回應 \_ 忙碌時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-663">7015 (0x1B67) </span><span class="sxs-lookup"><span data-stu-id="fda70-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-664">在回呼上的遠端網站偵測到忙碌信號。</span><span class="sxs-lookup"><span data-stu-id="fda70-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**\_CTX \_ 數據機 \_ 回應 \_ 聲音時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-666">7016 (0x1B68) </span><span class="sxs-lookup"><span data-stu-id="fda70-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-667">在回呼上的遠端網站偵測到語音。</span><span class="sxs-lookup"><span data-stu-id="fda70-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**\_CTX \_ TD \_ 錯誤時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-669">7017 (0x1B69) </span><span class="sxs-lookup"><span data-stu-id="fda70-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-670">傳輸驅動程式錯誤。</span><span class="sxs-lookup"><span data-stu-id="fda70-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**錯誤 \_ CTX \_ \_ 找不 \_ 到 WINSTATION**</span><span class="sxs-lookup"><span data-stu-id="fda70-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-672">7022 (0x1B6E) </span><span class="sxs-lookup"><span data-stu-id="fda70-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-673">找不到指定的會話。</span><span class="sxs-lookup"><span data-stu-id="fda70-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**錯誤 \_ CTX \_ WINSTATION \_ 已經 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="fda70-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-675">7023 (0x1B6F) </span><span class="sxs-lookup"><span data-stu-id="fda70-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-676">指定的會話名稱已在使用中。</span><span class="sxs-lookup"><span data-stu-id="fda70-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**\_CTX \_ WINSTATION \_ 忙碌時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-678">7024 (0x1B70) </span><span class="sxs-lookup"><span data-stu-id="fda70-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-679">因為遠端桌面服務目前忙碌中，所以您嘗試執行的工作無法完成。</span><span class="sxs-lookup"><span data-stu-id="fda70-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="fda70-680">請等候一段時間後再試一次。</span><span class="sxs-lookup"><span data-stu-id="fda70-680">Please try again in a few minutes.</span></span> <span data-ttu-id="fda70-681">其他使用者仍應能夠登入。</span><span class="sxs-lookup"><span data-stu-id="fda70-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**\_CTX 錯誤 \_ 的 \_ 影片 \_ 模式時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-683">7025 (0x1B71) </span><span class="sxs-lookup"><span data-stu-id="fda70-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-684">嘗試連接到目前的用戶端不支援其影片模式的會話。</span><span class="sxs-lookup"><span data-stu-id="fda70-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**\_CTX \_ 圖形 \_ 無效時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-686">7035 (0x1B7B) </span><span class="sxs-lookup"><span data-stu-id="fda70-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-687">應用程式嘗試啟用 DOS 圖形模式。</span><span class="sxs-lookup"><span data-stu-id="fda70-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="fda70-688">不支援 DOS 圖形模式。</span><span class="sxs-lookup"><span data-stu-id="fda70-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**錯誤 \_ CTX \_ 登入 \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="fda70-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-690">7037 (0x1B7D) </span><span class="sxs-lookup"><span data-stu-id="fda70-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-691">您的互動式登入許可權已停用。</span><span class="sxs-lookup"><span data-stu-id="fda70-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="fda70-692">請連絡您的管理員。</span><span class="sxs-lookup"><span data-stu-id="fda70-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**\_CTX \_ 不是 \_ 主控台時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-694">7038 (0x1B7E) </span><span class="sxs-lookup"><span data-stu-id="fda70-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-695">要求的操作只能在系統主控台上執行。</span><span class="sxs-lookup"><span data-stu-id="fda70-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="fda70-696">這通常是需要直接存取主控台的驅動程式或系統 DLL 的結果。</span><span class="sxs-lookup"><span data-stu-id="fda70-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**\_CTX \_ 用戶端 \_ 查詢 \_ 逾時錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-698">7040 (0x1B80) </span><span class="sxs-lookup"><span data-stu-id="fda70-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-699">用戶端無法回應伺服器連接訊息。</span><span class="sxs-lookup"><span data-stu-id="fda70-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**\_CTX \_ 主控台 \_ 中斷連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-701">7041 (0x1B81) </span><span class="sxs-lookup"><span data-stu-id="fda70-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-702">不支援中斷連線主控台會話。</span><span class="sxs-lookup"><span data-stu-id="fda70-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**\_CTX \_ 主控台 \_ 連接時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-704">7042 (0x1B82) </span><span class="sxs-lookup"><span data-stu-id="fda70-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-705">不支援將已中斷連線的會話重新連接到主控台。</span><span class="sxs-lookup"><span data-stu-id="fda70-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**錯誤 \_ CTX \_ 陰影 \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="fda70-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-707">7044 (0x1B84) </span><span class="sxs-lookup"><span data-stu-id="fda70-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-708">遠端控制另一個會話的要求遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="fda70-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**錯誤 \_ CTX \_ \_ 拒絕存取 \_ WINSTATION**</span><span class="sxs-lookup"><span data-stu-id="fda70-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-710">7045 (0x1B85) </span><span class="sxs-lookup"><span data-stu-id="fda70-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-711">要求的會話存取被拒。</span><span class="sxs-lookup"><span data-stu-id="fda70-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**\_CTX \_ 不正確 \_ WD 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-713">7049 (0x1B89) </span><span class="sxs-lookup"><span data-stu-id="fda70-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-714">指定的終端機連接驅動程式無效。</span><span class="sxs-lookup"><span data-stu-id="fda70-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**\_CTX \_ 陰影 \_ 無效時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-716">7050 (0x1B8A) </span><span class="sxs-lookup"><span data-stu-id="fda70-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-717">要求的會話無法從遠端控制。</span><span class="sxs-lookup"><span data-stu-id="fda70-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="fda70-718">這可能是因為會話已中斷連線，或目前沒有使用者登入。</span><span class="sxs-lookup"><span data-stu-id="fda70-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**\_CTX \_ \_ 停用陰影時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-720">7051 (0x1B8B) </span><span class="sxs-lookup"><span data-stu-id="fda70-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-721">要求的會話未設定為允許遠端控制。</span><span class="sxs-lookup"><span data-stu-id="fda70-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**\_CTX \_ \_ \_ 使用中的用戶端授權 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-723">7052 (0x1B8C) </span><span class="sxs-lookup"><span data-stu-id="fda70-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-724">您對此終端機伺服器的連線要求已被拒絕。</span><span class="sxs-lookup"><span data-stu-id="fda70-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="fda70-725">您的終端機伺服器用戶端授權號碼目前正由另一位使用者使用中。</span><span class="sxs-lookup"><span data-stu-id="fda70-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="fda70-726">請呼叫您的系統管理員以取得唯一的授權號碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**\_CTX \_ 用戶端 \_ 授權 \_ 未 \_ 設定時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-728">7053 (0x1B8D) </span><span class="sxs-lookup"><span data-stu-id="fda70-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-729">您對此終端機伺服器的連線要求已被拒絕。</span><span class="sxs-lookup"><span data-stu-id="fda70-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="fda70-730">尚未輸入終端機伺服器用戶端副本的終端機伺服器用戶端授權號碼。</span><span class="sxs-lookup"><span data-stu-id="fda70-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="fda70-731">請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="fda70-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**\_ \_ \_ 無法使用 CTX 授權 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-733">7054 (0x1B8E) </span><span class="sxs-lookup"><span data-stu-id="fda70-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-734">與這部電腦的連線數目會受到限制，且目前正在使用所有連接。</span><span class="sxs-lookup"><span data-stu-id="fda70-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="fda70-735">請稍後再嘗試連接，或洽詢您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="fda70-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**\_CTX \_ 授權 \_ 用戶端 \_ 無效時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-737">7055 (0x1B8F) </span><span class="sxs-lookup"><span data-stu-id="fda70-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-738">您使用的用戶端未獲得使用此系統的授權。</span><span class="sxs-lookup"><span data-stu-id="fda70-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="fda70-739">您的登入要求遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="fda70-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**\_CTX \_ 授權 \_ 過期時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-741">7056 (0x1B90) </span><span class="sxs-lookup"><span data-stu-id="fda70-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-742">系統授權已過期。</span><span class="sxs-lookup"><span data-stu-id="fda70-742">The system license has expired.</span></span> <span data-ttu-id="fda70-743">您的登入要求遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="fda70-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**錯誤 \_ CTX \_ 陰影 \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="fda70-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-745">7057 (0x1B91) </span><span class="sxs-lookup"><span data-stu-id="fda70-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-746">無法終止遠端控制，因為指定的會話目前不在遠端控制。</span><span class="sxs-lookup"><span data-stu-id="fda70-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**\_CTX \_ \_ \_ 由 \_ 模式 \_ 變更結束時的陰影**</span><span class="sxs-lookup"><span data-stu-id="fda70-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-748">7058 (0x1B92) </span><span class="sxs-lookup"><span data-stu-id="fda70-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-749">主控台的遠端控制已終止，因為顯示模式已變更。</span><span class="sxs-lookup"><span data-stu-id="fda70-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="fda70-750">不支援在遠端控制會話中變更顯示模式。</span><span class="sxs-lookup"><span data-stu-id="fda70-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_超過錯誤啟用 \_ 計數 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-752">7059 (0x1B93) </span><span class="sxs-lookup"><span data-stu-id="fda70-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-753">此安裝已重設啟用的次數上限。</span><span class="sxs-lookup"><span data-stu-id="fda70-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="fda70-754">將不會清除您的啟用計時器。</span><span class="sxs-lookup"><span data-stu-id="fda70-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**錯誤 \_ CTX \_ WINSTATIONS \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="fda70-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-756">7060 (0x1B94) </span><span class="sxs-lookup"><span data-stu-id="fda70-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-757">遠端登入目前已停用。</span><span class="sxs-lookup"><span data-stu-id="fda70-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**\_CTX \_ 所需的加密 \_ 層級 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-759">7061 (0x1B95) </span><span class="sxs-lookup"><span data-stu-id="fda70-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-760">您沒有適當的加密層級可存取此會話。</span><span class="sxs-lookup"><span data-stu-id="fda70-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**\_CTX \_ \_ 使用中的 \_ 會話時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-762">7062 (0x1B96) </span><span class="sxs-lookup"><span data-stu-id="fda70-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-763">使用者% s \\ \\ % s 目前已登入這部電腦。</span><span class="sxs-lookup"><span data-stu-id="fda70-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="fda70-764">只有目前的使用者或系統管理員可以登入這部電腦。</span><span class="sxs-lookup"><span data-stu-id="fda70-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**錯誤 \_ CTX \_ 無 \_ 強制 \_ 登出**</span><span class="sxs-lookup"><span data-stu-id="fda70-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-766">7063 (0x1B97) </span><span class="sxs-lookup"><span data-stu-id="fda70-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-767">使用者% s \\ \\ % s 已經登入這部電腦的主控台。</span><span class="sxs-lookup"><span data-stu-id="fda70-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="fda70-768">您目前沒有登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="fda70-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="fda70-769">若要解決此問題，請洽詢% s \\ \\ % s 並登出。</span><span class="sxs-lookup"><span data-stu-id="fda70-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**\_CTX \_ 帳戶 \_ 限制時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-771">7064 (0x1B98) </span><span class="sxs-lookup"><span data-stu-id="fda70-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-772">因為帳戶限制，所以無法將您登入。</span><span class="sxs-lookup"><span data-stu-id="fda70-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**錯誤 \_ RDP \_ 通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-774">7065 (0x1B99) </span><span class="sxs-lookup"><span data-stu-id="fda70-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-775">RDP 通訊協定元件 %2 偵測到通訊協定資料流程中的錯誤，並已中斷用戶端連線。</span><span class="sxs-lookup"><span data-stu-id="fda70-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**\_CTX \_ CDM \_ CONNECT 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-777">7066 (0x1B9A) </span><span class="sxs-lookup"><span data-stu-id="fda70-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-778">用戶端磁片磁碟機對應服務已在終端機連線上連接。</span><span class="sxs-lookup"><span data-stu-id="fda70-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**\_CTX \_ CDM \_ 中斷連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-780">7067 (0x1B9B) </span><span class="sxs-lookup"><span data-stu-id="fda70-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-781">用戶端磁片磁碟機對應服務已在終端機連接中斷連線。</span><span class="sxs-lookup"><span data-stu-id="fda70-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**\_CTX \_ 安全性層 \_ 級 \_ 錯誤時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-783">7068 (0x1B9C) </span><span class="sxs-lookup"><span data-stu-id="fda70-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-784">終端機伺服器安全性階層偵測到通訊協定資料流程中的錯誤，並已中斷用戶端連線。</span><span class="sxs-lookup"><span data-stu-id="fda70-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**\_TS \_ 不相容 \_ 會話錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-786">7069 (0x1B9D) </span><span class="sxs-lookup"><span data-stu-id="fda70-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-787">目標會話與目前的會話不相容。</span><span class="sxs-lookup"><span data-stu-id="fda70-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**錯誤 \_ TS \_ 影片 \_ 子系統 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fda70-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-789">7070 (0x1B9E) </span><span class="sxs-lookup"><span data-stu-id="fda70-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-790">Windows 無法連線到您的會話，因為 Windows video 子系統發生問題。</span><span class="sxs-lookup"><span data-stu-id="fda70-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="fda70-791">請稍後再試一次連接，或洽詢伺服器管理員以取得協助。</span><span class="sxs-lookup"><span data-stu-id="fda70-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS \_ 錯誤 \_ 的 \_ API \_ 序列無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-793">8001 (0x1F41) </span><span class="sxs-lookup"><span data-stu-id="fda70-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-794">檔案複寫服務 API 的呼叫不正確。</span><span class="sxs-lookup"><span data-stu-id="fda70-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS \_ ERR \_ 正在啟動 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="fda70-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-796">8002 (0x1F42) </span><span class="sxs-lookup"><span data-stu-id="fda70-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-797">無法啟動 file replication service。</span><span class="sxs-lookup"><span data-stu-id="fda70-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ 錯誤 \_ 停止 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="fda70-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-799">8003 (0x1F43) </span><span class="sxs-lookup"><span data-stu-id="fda70-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-800">無法停止 file replication service。</span><span class="sxs-lookup"><span data-stu-id="fda70-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS \_ ERR \_ 內部 \_ API**</span><span class="sxs-lookup"><span data-stu-id="fda70-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-802">8004 (0x1F44) </span><span class="sxs-lookup"><span data-stu-id="fda70-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-803">檔案複寫服務 API 已終止要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="fda70-804">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ ERR \_ 內部**</span><span class="sxs-lookup"><span data-stu-id="fda70-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-806">8005 (0x1F45) </span><span class="sxs-lookup"><span data-stu-id="fda70-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-807">檔案複寫服務已終止要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-807">The file replication service terminated the request.</span></span> <span data-ttu-id="fda70-808">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ ERR \_ 服務 \_ 通訊**</span><span class="sxs-lookup"><span data-stu-id="fda70-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-810">8006 (0x1F46) </span><span class="sxs-lookup"><span data-stu-id="fda70-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-811">無法連絡檔案複寫服務。</span><span class="sxs-lookup"><span data-stu-id="fda70-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="fda70-812">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ 錯誤 \_ 的 \_ 特權不足**</span><span class="sxs-lookup"><span data-stu-id="fda70-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-814">8007 (0x1F47) </span><span class="sxs-lookup"><span data-stu-id="fda70-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-815">因為使用者的許可權不足，所以檔案複寫服務無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="fda70-816">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS \_ ERR \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="fda70-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-818">8008 (0x1F48) </span><span class="sxs-lookup"><span data-stu-id="fda70-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-819">因為無法使用已驗證的 RPC，所以檔案複寫服務無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="fda70-820">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ ERR \_ 父系的 \_ 許可權不足 \_**</span><span class="sxs-lookup"><span data-stu-id="fda70-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-822">8009 (0x1F49) </span><span class="sxs-lookup"><span data-stu-id="fda70-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-823">因為使用者的網域控制站許可權不足，所以檔案複寫服務無法滿足要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="fda70-824">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS \_ ERR \_ 父 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="fda70-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-826">8010 (0x1F4A) </span><span class="sxs-lookup"><span data-stu-id="fda70-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-827">檔案複寫服務無法滿足要求，因為網域控制站上無法使用已驗證的 RPC。</span><span class="sxs-lookup"><span data-stu-id="fda70-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="fda70-828">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ ERR \_ 子系 \_ 對 \_ 父 \_ 通訊**</span><span class="sxs-lookup"><span data-stu-id="fda70-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-830">8011 (0x1F4B) </span><span class="sxs-lookup"><span data-stu-id="fda70-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-831">檔案複寫服務無法與網域控制站上的檔案複寫服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="fda70-832">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ ERR \_ 父代 \_ 至 \_ 子 \_ 通訊**</span><span class="sxs-lookup"><span data-stu-id="fda70-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-834">8012 (0x1F4C) </span><span class="sxs-lookup"><span data-stu-id="fda70-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-835">網域控制站上的檔案複寫服務無法與這部電腦上的檔案複寫服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="fda70-836">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ 錯誤 \_ SYSVOL \_ 填入**</span><span class="sxs-lookup"><span data-stu-id="fda70-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-838">8013 (0x1F4D) </span><span class="sxs-lookup"><span data-stu-id="fda70-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-839">因為發生內部錯誤，所以檔案複寫服務無法填入系統磁碟區。</span><span class="sxs-lookup"><span data-stu-id="fda70-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="fda70-840">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ 錯誤 \_ SYSVOL \_ 填入 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="fda70-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-842">8014 (0x1F4E) </span><span class="sxs-lookup"><span data-stu-id="fda70-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-843">因為發生內部超時，所以檔案複寫服務無法填入系統磁碟區。</span><span class="sxs-lookup"><span data-stu-id="fda70-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="fda70-844">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ ERR \_ SYSVOL \_ \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="fda70-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-846">8015 (0x1F4F) </span><span class="sxs-lookup"><span data-stu-id="fda70-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-847">檔案複寫服務無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="fda70-848">系統磁碟區正忙於先前的要求。</span><span class="sxs-lookup"><span data-stu-id="fda70-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ ERR \_ SYSVOL \_ 降級**</span><span class="sxs-lookup"><span data-stu-id="fda70-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-850">8016 (0x1F50) </span><span class="sxs-lookup"><span data-stu-id="fda70-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-851">因為發生內部錯誤，所以檔案複寫服務無法停止複寫系統磁碟區。</span><span class="sxs-lookup"><span data-stu-id="fda70-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="fda70-852">事件記錄檔可能會有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fda70-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fda70-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ 錯誤 \_ 的 \_ 服務 \_ 參數無效**</span><span class="sxs-lookup"><span data-stu-id="fda70-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda70-854">8017 (0x1F51) </span><span class="sxs-lookup"><span data-stu-id="fda70-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="fda70-855">檔案複寫服務偵測到不正確參數。</span><span class="sxs-lookup"><span data-stu-id="fda70-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fda70-856">規格需求</span><span class="sxs-lookup"><span data-stu-id="fda70-856">Requirements</span></span>



| <span data-ttu-id="fda70-857">需求</span><span class="sxs-lookup"><span data-stu-id="fda70-857">Requirement</span></span> | <span data-ttu-id="fda70-858">值</span><span class="sxs-lookup"><span data-stu-id="fda70-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fda70-859">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fda70-859">Minimum supported client</span></span><br/> | <span data-ttu-id="fda70-860">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fda70-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fda70-861">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fda70-861">Minimum supported server</span></span><br/> | <span data-ttu-id="fda70-862">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fda70-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fda70-863">標頭</span><span class="sxs-lookup"><span data-stu-id="fda70-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda70-864"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="fda70-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fda70-865">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fda70-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda70-866">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fda70-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




