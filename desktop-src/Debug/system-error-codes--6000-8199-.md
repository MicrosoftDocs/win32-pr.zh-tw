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
# <a name="system-error-codes-6000-8199"></a>系統錯誤碼 (6000-8199) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述 (錯誤6000到 8199) 的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**錯誤 \_ 加密 \_ 失敗**
</dt> <dd> <dl> <dt>

6000 (0x1770) 
</dt> <dt>



無法加密指定的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**錯誤 \_ 解密 \_ 失敗**
</dt> <dd> <dl> <dt>

6001 (0x1771) 
</dt> <dt>



無法解密指定的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**錯誤檔案已 \_ \_ 加密**
</dt> <dd> <dl> <dt>

6002 (0x1772) 
</dt> <dt>



指定的檔案已加密，且使用者沒有解密的能力。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**錯誤的復原 \_ \_ \_ 原則**
</dt> <dd> <dl> <dt>

6003 (0x1773) 
</dt> <dt>



未針對此系統設定有效的加密修復原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**錯誤 \_ 無 \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774) 
</dt> <dt>



未針對此系統載入所需的加密驅動程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**錯誤 \_ 的 \_ EFS 錯誤**
</dt> <dd> <dl> <dt>

6005 (0x1775) 
</dt> <dt>



檔案使用的加密驅動程式與目前載入的不同。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**錯誤 \_ 的 \_ 使用者 \_ 金鑰**
</dt> <dd> <dl> <dt>

6006 (0x1776) 
</dt> <dt>



沒有為使用者定義 EFS 金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**錯誤 \_ 檔案 \_ 未 \_ 加密**
</dt> <dd> <dl> <dt>

6007 (0x1777) 
</dt> <dt>



指定的檔案未加密。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**錯誤 \_ 不是 \_ 匯出 \_ 格式**
</dt> <dd> <dl> <dt>

6008 (0x1778) 
</dt> <dt>



指定的檔案不是定義的 EFS 匯出格式。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**錯誤 \_ 檔案 \_ 唯讀 \_**
</dt> <dd> <dl> <dt>

6009 (0x1779) 
</dt> <dt>



指定的檔案是唯讀的。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**錯誤 \_ DIR \_ 不 \_ 允許的 EFS**
</dt> <dd> <dl> <dt>

6010 (0x177A) 
</dt> <dt>



目錄已停用加密。


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**錯誤的 \_ EFS \_ 伺服器 \_ 不 \_ 受信任**
</dt> <dd> <dl> <dt>

6011 (0x177B) 
</dt> <dt>



伺服器不受遠端加密作業的信任。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**錯誤的復原 \_ \_ \_ 原則錯誤**
</dt> <dd> <dl> <dt>

6012 (0x177C) 
</dt> <dt>



為此系統設定的復原原則包含不正確修復憑證。


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**錯誤 \_ EFS \_ ALG \_ BLOB \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

6013 (0x177D) 
</dt> <dt>



來源檔案上所使用的加密演算法需要比目的地檔案上更大的金鑰緩衝區。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**錯誤 \_ 磁片區 \_ 不 \_ 支援 \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E) 
</dt> <dt>



磁碟分割不支援檔案加密。


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**\_ \_ 停用 EFS 錯誤**
</dt> <dd> <dl> <dt>

6015 (0x177F) 
</dt> <dt>



此電腦已停用檔案加密。


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**\_ \_ \_ 不支援的 EFS 版本錯誤 \_**
</dt> <dd> <dl> <dt>

6016 (0x1780) 
</dt> <dt>



需要較新的系統才能將這個加密的檔案解密。


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**錯誤 \_ CS \_ 加密 \_ 不正確 \_ 伺服器 \_ 回應**
</dt> <dd> <dl> <dt>

6017 (0x1781) 
</dt> <dt>



遠端伺服器針對以用戶端加密開啟的檔案傳送了不正確回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**錯誤 \_ CS \_ 加密 \_ 不支援的 \_ 伺服器**
</dt> <dd> <dl> <dt>

6018 (0x1782) 
</dt> <dt>



遠端伺服器不支援用戶端加密，即使它宣稱支援它也一樣。


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**錯誤 \_ CS \_ 加密 \_ 現有的 \_ 加密 \_ 檔案**
</dt> <dd> <dl> <dt>

6019 (0x1783) 
</dt> <dt>



檔案已加密，應以用戶端加密模式開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**錯誤 \_ CS \_ 加密 \_ 新的 \_ 加密 \_ 檔案**
</dt> <dd> <dl> <dt>

6020 (0x1784) 
</dt> <dt>



正在建立新的加密檔案，因此必須提供 $EFS。


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**錯誤 \_ CS \_ 加密 \_ 檔 \_ 不是 \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785) 
</dt> <dt>



SMB 用戶端在非 CSE 檔案上要求 CSE FSCTL。


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**錯誤 \_ 加密 \_ 原則 \_ 拒絕 \_ 操作**
</dt> <dd> <dl> <dt>

6022 (0x1786) 
</dt> <dt>



原則封鎖了要求的作業。 如需相關資訊，請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**錯誤 \_ \_ 找不到瀏覽器 \_ 伺服器 \_**
</dt> <dd> <dl> <dt>

6118 (0x17E6) 
</dt> <dt>



目前無法使用此工作組的伺服器清單。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**已計畫的 \_ 電子 \_ 服務 \_ 非 \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838) 
</dt> <dt>



工作排程器服務必須設定為在系統帳戶中執行，才能正常運作。 個別工作可設定為在其他帳戶中執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**錯誤 \_ 記錄 \_ 磁區 \_ 無效**
</dt> <dd> <dl> <dt>

6600 (0x19C8) 
</dt> <dt>



記錄服務遇到不正確記錄磁區。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**錯誤 \_ 記錄 \_ 磁區同位檢查 \_ \_ 無效**
</dt> <dd> <dl> <dt>

6601 (0x19C9) 
</dt> <dt>



記錄服務遇到區塊同位不正確記錄磁區。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**錯誤 \_ 記錄 \_ 磁區重新對應 \_**
</dt> <dd> <dl> <dt>

6602 (0x19CA) 
</dt> <dt>



Log service 發生重新對應的記錄磁區。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**錯誤 \_ 記錄檔 \_ 區塊 \_ 未完成**
</dt> <dd> <dl> <dt>

6603 (0x19CB) 
</dt> <dt>



記錄服務遇到部分或不完整的記錄區塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**錯誤 \_ 記錄檔 \_ 不正確 \_ 範圍**
</dt> <dd> <dl> <dt>

6604 (0x19CC) 
</dt> <dt>



記錄服務嘗試存取使用中記錄範圍以外的資料時。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**錯誤 \_ 記錄 \_ 區塊已 \_ 用盡**
</dt> <dd> <dl> <dt>

6605 (0x19CD) 
</dt> <dt>



記錄服務使用者封送處理緩衝區已用盡。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**錯誤 \_ 記錄檔 \_ 讀取 \_ 內容 \_ 無效**
</dt> <dd> <dl> <dt>

6606 (0x19CE) 
</dt> <dt>



記錄服務嘗試從讀取內容不正確封送處理區域讀取。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**錯誤 \_ 記錄檔 \_ 重新開機 \_ 無效**
</dt> <dd> <dl> <dt>

6607 (0x19CF) 
</dt> <dt>



記錄服務發生不正確記錄重新開機區域。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**錯誤 \_ 記錄 \_ 區塊 \_ 版本**
</dt> <dd> <dl> <dt>

6608 (0x19D0) 
</dt> <dt>



記錄服務遇到不正確記錄區塊版本。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**錯誤 \_ 記錄檔 \_ 區塊 \_ 無效**
</dt> <dd> <dl> <dt>

6609 (0x19D1) 
</dt> <dt>



記錄服務遇到不正確記錄區塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**錯誤 \_ 記錄 \_ 讀取 \_ 模式 \_ 無效**
</dt> <dd> <dl> <dt>

6610 (0x19D2) 
</dt> <dt>



記錄服務嘗試以不正確讀取模式讀取記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**錯誤 \_ 記錄檔 \_ 無 \_ 重新開機**
</dt> <dd> <dl> <dt>

6611 (0x19D3) 
</dt> <dt>



記錄服務發現沒有重新開機區域的記錄資料流程。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 已損毀**
</dt> <dd> <dl> <dt>

6612 (0x19D4) 
</dt> <dt>



記錄服務發生損毀的中繼資料檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 無效**
</dt> <dd> <dl> <dt>

6613 (0x19D5) 
</dt> <dt>



記錄服務發現無法由記錄檔系統建立的中繼資料檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**錯誤 \_ 記錄 \_ 中繼資料 \_ 不一致**
</dt> <dd> <dl> <dt>

6614 (0x19D6) 
</dt> <dt>



記錄服務發現具有不一致資料的中繼資料檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**錯誤 \_ 記錄檔 \_ 保留 \_ 無效**
</dt> <dd> <dl> <dt>

6615 (0x19D7) 
</dt> <dt>



記錄服務嘗試配置或處置保留空間時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**錯誤 \_ 記錄檔無法 \_ \_ 刪除**
</dt> <dd> <dl> <dt>

6616 (0x19D8) 
</dt> <dt>



記錄服務無法刪除記錄檔或檔案系統容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**\_超過錯誤記錄 \_ 容器 \_ 限制 \_**
</dt> <dd> <dl> <dt>

6617 (0x19D9) 
</dt> <dt>



記錄服務已達到配置給記錄檔的可允許容器數目上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_記錄檔 \_ 開頭 \_ 的錯誤記錄 \_ 檔**
</dt> <dd> <dl> <dt>

6618 (0x19DA) 
</dt> <dt>



記錄服務已嘗試在記錄檔的開頭之前讀取或寫下。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**\_ \_ \_ 已安裝錯誤記錄檔原則 \_**
</dt> <dd> <dl> <dt>

6619 (0x19DB) 
</dt> <dt>



無法安裝記錄原則，因為已有相同類型的原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**\_ \_ \_ 未安裝錯誤記錄檔原則 \_**
</dt> <dd> <dl> <dt>

6620 (0x19DC) 
</dt> <dt>



要求時未安裝有問題的記錄檔原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**錯誤 \_ 記錄檔 \_ 原則 \_ 無效**
</dt> <dd> <dl> <dt>

6621 (0x19DD) 
</dt> <dt>



記錄上已安裝的原則集無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**錯誤 \_ 記錄檔 \_ 原則 \_ 衝突**
</dt> <dd> <dl> <dt>

6622 (0x19DE) 
</dt> <dt>



記錄檔中有問題的原則導致作業無法完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**錯誤記錄檔已釘選封存 \_ \_ \_ \_ 結尾**
</dt> <dd> <dl> <dt>

6623 (0x19DF) 
</dt> <dt>



無法回收記錄檔空間，因為記錄檔會由封存結尾釘選。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**錯誤記錄檔 \_ \_ 記錄不 \_ 存在**
</dt> <dd> <dl> <dt>

6624 (0x19E0) 
</dt> <dt>



記錄檔記錄不是記錄檔中的記錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ \_ 保留 \_ 不正確錯誤記錄檔記錄**
</dt> <dd> <dl> <dt>

6625 (0x19E1) 
</dt> <dt>



保留的記錄檔記錄數目或保留的記錄檔記錄數目的調整無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**錯誤 \_ 記錄 \_ 檔 \_ 保留的空間 \_ 無效**
</dt> <dd> <dl> <dt>

6626 (0x19E2) 
</dt> <dt>



保留的記錄檔空間或記錄空間的調整無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**錯誤 \_ 記錄 \_ 結尾 \_ 無效**
</dt> <dd> <dl> <dt>

6627 (0x19E3) 
</dt> <dt>



現用記錄檔的新或現有封存結尾或基底無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**錯誤 \_ 記錄檔已 \_ 滿**
</dt> <dd> <dl> <dt>

6628 (0x19E4) 
</dt> <dt>



記錄檔空間已用盡。


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**錯誤 \_ 無法 \_ \_ 調整 \_ 記錄大小**
</dt> <dd> <dl> <dt>

6629 (0x19E5) 
</dt> <dt>



記錄檔無法設定為要求的大小。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**錯誤記錄檔多工 \_ \_**
</dt> <dd> <dl> <dt>

6630 (0x19E6) 
</dt> <dt>



記錄已多工，不允許直接寫入實體記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**錯誤 \_ 記錄檔 \_ 專用**
</dt> <dd> <dl> <dt>

6631 (0x19E7) 
</dt> <dt>



作業失敗，因為記錄檔是專用的記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**錯誤 \_ 記錄檔封存 \_ \_ 未 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

6632 (0x19E8) 
</dt> <dt>



作業需要保存內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**錯誤 \_ 記錄 \_ 檔 \_ 保存 \_ 進行中**
</dt> <dd> <dl> <dt>

6633 (0x19E9) 
</dt> <dt>



記錄檔封存正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**錯誤 \_ 記錄檔 \_ 暫時**
</dt> <dd> <dl> <dt>

6634 (0x19EA) 
</dt> <dt>



作業需要非暫時記錄檔，但記錄是暫時的。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**錯誤 \_ 記錄檔 \_ 沒有 \_ 足夠的 \_ 容器**
</dt> <dd> <dl> <dt>

6635 (0x19EB) 
</dt> <dt>



記錄檔的讀取或寫入之前，必須至少有兩個容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_ \_ \_ 已註冊錯誤記錄用戶端 \_**
</dt> <dd> <dl> <dt>

6636 (0x19EC) 
</dt> <dt>



記錄用戶端已經在資料流程上註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**錯誤 \_ 記錄 \_ 用戶端 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

6637 (0x19ED) 
</dt> <dt>



尚未在資料流程上註冊記錄用戶端。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**錯誤 \_ 記錄檔 \_ 完整 \_ 處理常式 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

6638 (0x19EE) 
</dt> <dt>



已經提出要求來處理記錄檔的完整狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 讀取 \_ 失敗**
</dt> <dd> <dl> <dt>

6639 (0x19EF) 
</dt> <dt>



記錄服務嘗試從記錄容器讀取時，發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 寫入 \_ 失敗**
</dt> <dd> <dl> <dt>

6640 (0x19F0) 
</dt> <dt>



記錄服務嘗試寫入記錄容器時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**錯誤 \_ 記錄 \_ 容器 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

6641 (0x19F1) 
</dt> <dt>



Log service 嘗試開啟記錄容器時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**錯誤 \_ 記錄 \_ 容器 \_ 狀態 \_ 無效**
</dt> <dd> <dl> <dt>

6642 (0x19F2) 
</dt> <dt>



記錄服務在嘗試要求的動作時，發生不正確容器狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**錯誤 \_ 記錄檔 \_ 狀態 \_ 無效**
</dt> <dd> <dl> <dt>

6643 (0x19F3) 
</dt> <dt>



記錄服務的狀態不正確，無法執行要求的動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**已 \_ 釘選錯誤記錄檔 \_**
</dt> <dd> <dl> <dt>

6644 (0x19F4) 
</dt> <dt>



記錄檔空間無法回收，因為已釘選記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**錯誤 \_ 記錄 \_ 中繼資料排清 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

6645 (0x19F5) 
</dt> <dt>



記錄中繼資料排清失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**錯誤 \_ 記錄 \_ 不一致的 \_ 安全性**
</dt> <dd> <dl> <dt>

6646 (0x19F6) 
</dt> <dt>



記錄和其容器的安全性不一致。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**錯誤 \_ 記錄 \_ 附加的 \_ 清除 \_ 失敗**
</dt> <dd> <dl> <dt>

6647 (0x19F7) 
</dt> <dt>



記錄已附加至記錄檔或保留變更，但無法排清記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**錯誤記錄檔已釘選的 \_ \_ \_ 保留**
</dt> <dd> <dl> <dt>

6648 (0x19F8) 
</dt> <dt>



由於保留使用大部分的記錄空間，因此會釘選記錄檔。 釋放一些保留的記錄，讓空間可供使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**錯誤 \_ 不正確 \_ 交易**
</dt> <dd> <dl> <dt>

6700 (0x1A2C) 
</dt> <dt>



與這項作業相關聯的交易控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**錯誤 \_ 交易 \_ 未 \_ 啟用**
</dt> <dd> <dl> <dt>

6701 (0x1A2D) 
</dt> <dt>



要求的作業是在已不再使用的交易內容中進行。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**錯誤 \_ 交易 \_ 要求 \_ 無效 \_**
</dt> <dd> <dl> <dt>

6702 (0x1A2E) 
</dt> <dt>



在交易對象的目前狀態中，要求的作業無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**\_ \_ 未要求錯誤 \_ 交易**
</dt> <dd> <dl> <dt>

6703 (0x1A2F) 
</dt> <dt>



呼叫端已呼叫回應 API，但因為 TM 未對呼叫端發出對應的要求，所以不需要回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**錯誤 \_ 交易 \_ 已經 \_ 中止**
</dt> <dd> <dl> <dt>

6704 (0x1A30) 
</dt> <dt>



因為交易已經中止，所以執行要求的作業太晚。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**錯誤 \_ 交易 \_ 已 \_ 認可**
</dt> <dd> <dl> <dt>

6705 (0x1A31) 
</dt> <dt>



因為交易已經過認可，所以執行要求的作業太晚。


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**錯誤 \_ TM \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

6706 (0x1A32) 
</dt> <dt>



交易管理員無法成功初始化。 不支援交易作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**錯誤 \_ RESOURCEMANAGER \_ 唯讀 \_**
</dt> <dd> <dl> <dt>

6707 (0x1A33) 
</dt> <dt>



指定的 ResourceManager 對此交易下的資源沒有任何變更或更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**錯誤 \_ 交易 \_ 未 \_ 聯結**
</dt> <dd> <dl> <dt>

6708 (0x1A34) 
</dt> <dt>



資源管理員已嘗試準備尚未成功聯結的交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**錯誤 \_ 交易 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

6709 (0x1A35) 
</dt> <dt>



交易對象已有較佳的登記，而且呼叫端嘗試的作業已建立新的高階。 只允許單一的上級登記。


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**錯誤 \_ CRM \_ 通訊協定 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

6710 (0x1A36) 
</dt> <dt>



RM 嘗試註冊已存在的通訊協定。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**錯誤 \_ 交易 \_ 傳播 \_ 失敗**
</dt> <dd> <dl> <dt>

6711 (0x1A37) 
</dt> <dt>



嘗試傳播交易失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**\_ \_ \_ 找不到 CRM 通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

6712 (0x1A38) 
</dt> <dt>



要求的傳播通訊協定未註冊為 CRM。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**錯誤 \_ 交易 \_ 不正確 \_ 馬紹爾 \_ 緩衝區**
</dt> <dd> <dl> <dt>

6713 (0x1A39) 
</dt> <dt>



傳入 PushTransaction 或 PullTransaction 的緩衝區格式不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**錯誤 \_ 目前 \_ 的 \_ 交易 \_ 無效**
</dt> <dd> <dl> <dt>

6714 (0x1A3A) 
</dt> <dt>



與執行緒相關聯的目前交易內容不是交易對象的有效控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ 找不到錯誤交易 \_**
</dt> <dd> <dl> <dt>

6715 (0x1A3B) 
</dt> <dt>



無法開啟指定的交易對象，因為找不到該物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**\_ \_ 找不到錯誤 RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>

6716 (0x1A3C) 
</dt> <dt>



無法開啟指定的 ResourceManager 物件，因為找不到它。


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ 找不到錯誤登記 \_**
</dt> <dd> <dl> <dt>

6717 (0x1A3D) 
</dt> <dt>



無法開啟指定的登錄物件，因為找不到該物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**\_ \_ \_ 找不到錯誤的錯誤**
</dt> <dd> <dl> <dt>

6718 (0x1A3E) 
</dt> <dt>



無法開啟指定的 TransactionManager 物件，因為找不到它。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**錯誤的 \_ TRANSACTIONMANAGER \_ 未 \_ 上線**
</dt> <dd> <dl> <dt>

6719 (0x1A3F) 
</dt> <dt>



無法建立或開啟指定的物件，因為其相關聯的 TransactionManager 不在線上。 您必須先呼叫 RecoverTransactionManager 來復原到記錄檔的結尾，然後才能開啟其交易或 ResourceManager 命名空間中的物件，以使其完全上線。 此外，將記錄寫入記錄檔的錯誤可能會導致 TransactionManager 離線。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**錯誤 \_ TRANSACTIONMANAGER \_ 修復 \_ 名稱 \_ 衝突**
</dt> <dd> <dl> <dt>

6720 (0x1A40) 
</dt> <dt>



指定的 TransactionManager 無法在 Ob 命名空間中建立其記錄檔中所包含的物件。 因此，無法復原 TransactionManager。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**錯誤 \_ 交易 \_ 非 \_ 根**
</dt> <dd> <dl> <dt>

6721 (0x1A41) 
</dt> <dt>



因為為登記指定的交易對象是交易的次級分支，所以無法完成在此交易對象上建立高階登記的呼叫。 只有交易的根目錄才能以較上層的形式登記。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**錯誤 \_ 交易 \_ 物件已 \_ 過期**
</dt> <dd> <dl> <dt>

6722 (0x1A42) 
</dt> <dt>



因為相關聯的交易管理員或資源管理員已經關閉，所以控制碼不再有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**錯誤 \_ 交易 \_ 回應 \_ 未 \_ 登記**
</dt> <dd> <dl> <dt>

6723 (0x1A43) 
</dt> <dt>



無法在這個高階登記上執行指定的作業，因為未在 NotificationMask 中使用對應的完成回應來建立登記。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**錯誤 \_ 交易 \_ 記錄 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

6724 (0x1A44) 
</dt> <dt>



無法執行指定的作業，因為記錄的記錄太長。 發生這種情況的原因有兩種：這項交易的登記太多，或代表這些登記記錄的組合 Ms-fve-recoveryinformation 太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_ \_ \_ 不支援隱含交易 \_ 錯誤**
</dt> <dd> <dl> <dt>

6725 (0x1A45) 
</dt> <dt>



不支援隱含交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**\_違反錯誤交易 \_ 完整性 \_**
</dt> <dd> <dl> <dt>

6726 (0x1A46) 
</dt> <dt>



核心交易管理員必須中止或忘記交易，因為它封鎖了轉寄進度。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**錯誤 \_ TRANSACTIONMANAGER \_ 識別 \_ 不相符**
</dt> <dd> <dl> <dt>

6727 (0x1A47) 
</dt> <dt>



提供的 TransactionManager 身分識別不符合 TransactionManager 記錄檔中所記錄的身分識別。


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**錯誤 \_ RM \_ 無法 \_ \_ 凍結 \_ \_ 快照集**
</dt> <dd> <dl> <dt>

6728 (0x1A48) 
</dt> <dt>



此快照集作業無法繼續，因為交易式資源管理員無法以其目前的狀態凍結。 請再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**錯誤 \_ 交易 \_ 必須 \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49) 
</dt> <dt>



無法使用指定的 EnlistmentMask 來登記交易，因為交易已完成 PrePrepare 階段。 為了確保正確性，ResourceManager 必須切換至寫入模式，並停止在此交易內快取資料。 只針對後續的交易階段進行登記，可能仍會成功。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**錯誤 \_ 交易 \_ 沒有 \_ 卓越的**
</dt> <dd> <dl> <dt>

6730 (0x1A4A) 
</dt> <dt>



交易沒有較佳的登記。


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**可能發生錯誤 \_ 啟發式 \_ 損毀 \_**
</dt> <dd> <dl> <dt>

6731 (0x1A4B) 
</dt> <dt>



嘗試認可交易已完成，但交易樹狀結構的某些部分可能因為啟發學習法而無法成功認可。 因此，可能在交易中修改某些資料可能尚未認可，而導致交易不一致。 可能的話，請檢查相關資料的一致性。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**\_交易 \_ 衝突錯誤**
</dt> <dd> <dl> <dt>

6800 (0x1A90) 
</dt> <dt>



函數嘗試使用保留給另一個交易使用的名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**錯誤 \_ RM \_ 未 \_ 啟用**
</dt> <dd> <dl> <dt>

6801 (0x1A91) 
</dt> <dt>



指定資源管理員內的交易支援未啟動，或由於錯誤而關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**錯誤的 \_ RM \_ 中繼資料 \_ 已損毀**
</dt> <dd> <dl> <dt>

6802 (0x1A92) 
</dt> <dt>



RM 的中繼資料已損毀。 RM 將無法運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**錯誤 \_ 目錄 \_ 不是 \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93) 
</dt> <dt>



指定的目錄不包含 resource manager。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**錯誤 \_ 交易 \_ 不支援 \_ 遠端**
</dt> <dd> <dl> <dt>

6805 (0x1A95) 
</dt> <dt>



遠端伺服器或共用不支援交易檔案作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**錯誤 \_ 記錄 \_ 重 \_ 設 \_ 大小無效**
</dt> <dd> <dl> <dt>

6806 (0x1A96) 
</dt> <dt>



要求的記錄檔大小無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**錯誤 \_ 物件 \_ 不再 \_ \_ 存在**
</dt> <dd> <dl> <dt>

6807 (0x1A97) 
</dt> <dt>



交易儲存點復原已刪除對應至控制碼 (檔案、資料流程、連結) 的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ \_ 找不到錯誤資料流程迷你**
</dt> <dd> <dl> <dt>

6808 (0x1A98) 
</dt> <dt>



在開啟此交易檔案時，找不到指定的檔案迷你檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**錯誤 \_ 資料流程 \_ 迷你 \_ 版本 \_ 無效**
</dt> <dd> <dl> <dt>

6809 (0x1A99) 
</dt> <dt>



找到指定的檔案迷你檔案，但已失效。 最可能的原因是交易儲存點復原。


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**\_ \_ \_ 從 \_ 指定的 \_ 交易無法存取的錯誤迷你**
</dt> <dd> <dl> <dt>

6810 (0x1A9A) 
</dt> <dt>



只有在建立迷你的交易時，才會在其內容中開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**錯誤 \_ 無法 \_ \_ \_ 使用 \_ MODIFY \_ 意圖開啟迷你**
</dt> <dd> <dl> <dt>

6811 (0x1A9B) 
</dt> <dt>



您無法使用修改存取來開啟迷你。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**錯誤 \_ 無法 \_ 建立 \_ 更多 \_ 串流 \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C) 
</dt> <dt>



您無法為此資料流程建立任何其他 miniversions。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**\_遠端檔案 \_ \_ 版本 \_ 不符的錯誤**
</dt> <dd> <dl> <dt>

6814 (0x1A9E) 
</dt> <dt>



遠端伺服器針對以交易開啟的檔案傳送了不相符的版本號碼或 Fid。


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**錯誤 \_ 控制碼不再 \_ \_ \_ 有效**
</dt> <dd> <dl> <dt>

6815 (0x1A9F) 
</dt> <dt>



交易已將控制碼失效。 最可能的原因是當交易結束或回復至儲存點時，檔案上有記憶體對應或開啟控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**\_沒有 \_ TXF \_ 中繼資料的錯誤**
</dt> <dd> <dl> <dt>

6816 (0x1AA0) 
</dt> <dt>



檔案上沒有交易中繼資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**偵測 \_ 到錯誤記錄檔 \_ 損毀 \_**
</dt> <dd> <dl> <dt>

6817 (0x1AA1) 
</dt> <dt>



記錄資料已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**無法 \_ \_ \_ 使用 \_ 控制碼 \_ 開啟來復原錯誤**
</dt> <dd> <dl> <dt>

6818 (0x1AA2) 
</dt> <dt>



無法復原檔案，因為它上仍有控制碼開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**\_RM \_ 中斷連線時發生錯誤**
</dt> <dd> <dl> <dt>

6819 (0x1AA3) 
</dt> <dt>



交易結果無法使用，因為負責該交易的資源管理員已中斷連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**錯誤 \_ 登記 \_ 不 \_ 佳**
</dt> <dd> <dl> <dt>

6820 (0x1AA4) 
</dt> <dt>



要求遭到拒絕，因為有問題的登記不是高階登記。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**\_ \_ 不 \_ 需要復原錯誤**
</dt> <dd> <dl> <dt>

6821 (0x1AA5) 
</dt> <dt>



交易式資源管理員已經是一致的。 不需要復原。


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**錯誤 \_ RM \_ 已 \_ 啟動**
</dt> <dd> <dl> <dt>

6822 (0x1AA6) 
</dt> <dt>



交易式資源管理員已經啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**錯誤檔案身分 \_ \_ 識別 \_ 不是 \_ 持續性**
</dt> <dd> <dl> <dt>

6823 (0x1AA7) 
</dt> <dt>



無法以交易方式開啟檔案，因為它的身分識別取決於無法解析之交易的結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**錯誤 \_ 無法 \_ 中斷 \_ 交易 \_ 相依性**
</dt> <dd> <dl> <dt>

6824 (0x1AA8) 
</dt> <dt>



無法執行作業，因為另一個交易取決於此屬性不會變更的事實。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**無法 \_ \_ 跨 \_ RM \_ 界限的錯誤**
</dt> <dd> <dl> <dt>

6825 (0x1AA9) 
</dt> <dt>



作業牽涉到具有兩個交易式資源管理員的單一檔案，因此不允許。


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**錯誤 \_ TXF \_ 目錄 \_ 不是 \_ 空的**
</dt> <dd> <dl> <dt>

6826 (0x1AAA) 
</dt> <dt>



$Txf 目錄必須是空的，此作業才會成功。


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_INDOUBT \_ 交易 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

6827 (0x1AAB) 
</dt> <dt>



作業會讓交易式資源管理員處於不一致的狀態，因此不允許。


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**錯誤 \_ TM \_ VOLATILE**
</dt> <dd> <dl> <dt>

6828 (0x1AAC) 
</dt> <dt>



無法完成作業，因為交易管理員沒有記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**錯誤 \_ 復原 \_ 計時器已 \_ 過期**
</dt> <dd> <dl> <dt>

6829 (0x1AAD) 
</dt> <dt>



無法排程復原，因為先前排程的復原已執行或已排入佇列等候執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**錯誤 \_ TXF \_ 屬性 \_ 已損毀**
</dt> <dd> <dl> <dt>

6830 (0x1AAE) 
</dt> <dt>



檔案或目錄上的交易式中繼資料屬性已損毀且無法讀取。


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許有錯誤 \_ 的 EFS \_**
</dt> <dd> <dl> <dt>

6831 (0x1AAF) 
</dt> <dt>



因為交易正在使用中，所以無法完成加密作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**錯誤 \_ 交易 \_ 開啟 \_ 不 \_ 允許**
</dt> <dd> <dl> <dt>

6832 (0x1AB0) 
</dt> <dt>



此物件不允許在交易中開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**錯誤 \_ 記錄檔 \_ 成長 \_ 失敗**
</dt> <dd> <dl> <dt>

6833 (0x1AB1) 
</dt> <dt>



嘗試在交易式資源管理員的記錄檔中建立空間失敗。 失敗狀態已記錄在事件記錄檔中。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**錯誤 \_ 交易 \_ 對應 \_ 不支援的 \_ 遠端**
</dt> <dd> <dl> <dt>

6834 (0x1AB2) 
</dt> <dt>



記憶體對應 (建立對應的區段) 不支援交易下的遠端檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**\_已有錯誤的 TXF \_ 中繼資料 \_ \_**
</dt> <dd> <dl> <dt>

6835 (0x1AB3) 
</dt> <dt>



交易中繼資料已存在於此檔案中，無法被取代。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_ \_ \_ \_ 未設定錯誤交易範圍 \_ 回呼**
</dt> <dd> <dl> <dt>

6836 (0x1AB4) 
</dt> <dt>



無法輸入交易範圍，因為範圍處理常式尚未初始化。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ 需要升級錯誤 \_ 交易**
</dt> <dd> <dl> <dt>

6837 (0x1AB5) 
</dt> <dt>



需要升級，才能讓資源管理員登錄，但交易已設定為不允許。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**錯誤 \_ 無法 \_ \_ \_ 在交易中 \_ 執行檔案**
</dt> <dd> <dl> <dt>

6838 (0x1AB6) 
</dt> <dt>



這個檔案會在未解析的交易中開啟以供修改，而且只能由交易讀取器開啟以供執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**錯誤 \_ 交易 \_ 未 \_ 凍結**
</dt> <dd> <dl> <dt>

6839 (0x1AB7) 
</dt> <dt>



已忽略解除凍結凍結交易的要求，因為先前尚未凍結交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**錯誤 \_ 交易 \_ 凍結 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

6840 (0x1AB8) 
</dt> <dt>



因為凍結已在進行中，所以無法凍結交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**錯誤 \_ 而非 \_ 快照集 \_ 磁片區**
</dt> <dd> <dl> <dt>

6841 (0x1AB9) 
</dt> <dt>



目標磁片區不是快照集磁片區。 這項作業只適用于裝載為快照集的磁片區。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**\_沒有 \_ \_ 開啟的檔案的儲存點 \_ 錯誤 \_**
</dt> <dd> <dl> <dt>

6842 (0x1ABA) 
</dt> <dt>



儲存點作業失敗，因為交易上的檔案已開啟。 這是不允許的。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**錯誤 \_ 資料 \_ 遺失 \_ 修復**
</dt> <dd> <dl> <dt>

6843 (0x1ABB) 
</dt> <dt>



Windows 已在檔案中發現損毀，且該檔案已修復。 可能發生資料遺失。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許 \_ 錯誤 \_ SPARSE**
</dt> <dd> <dl> <dt>

6844 (0x1ABC) 
</dt> <dt>



無法完成稀疏作業，因為檔案上有作用中的交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**錯誤 \_ TM 身分 \_ 識別 \_ 不相符**
</dt> <dd> <dl> <dt>

6845 (0x1ABD) 
</dt> <dt>



因為儲存在記錄檔中的 Tm 身分識別不符合作為引數傳入的 Tm 身分識別，所以建立 TransactionManager 物件的呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**錯誤 \_ 浮動 \_ 區段**
</dt> <dd> <dl> <dt>

6846 (0x1ABE) 
</dt> <dt>



嘗試在已浮動為交易結束結果的區段物件上使用 i/o。 沒有有效的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**錯誤 \_ 無法 \_ 接受 \_ 交易 \_ 工作**
</dt> <dd> <dl> <dt>

6847 (0x1ABF) 
</dt> <dt>



交易式資源管理員目前無法接受交易工作，因為暫時性狀況（例如資源不足）。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**錯誤 \_ 無法 \_ 中止 \_ 交易**
</dt> <dd> <dl> <dt>

6848 (0x1AC0) 
</dt> <dt>



交易式資源管理員的 tranactions 未處理太多，無法中止。 交易式資源管理器已關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**錯誤 \_ 的 \_ 群集錯誤**
</dt> <dd> <dl> <dt>

6849 (0x1AC1) 
</dt> <dt>



因為磁片上的叢集不正確，所以無法完成操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_ \_ \_ 交易中不允許 \_ \_ 有錯誤壓縮**
</dt> <dd> <dl> <dt>

6850 (0x1AC2) 
</dt> <dt>



無法完成壓縮作業，因為檔案上有作用中的交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**錯誤 \_ 磁片區中途 \_ 損壞**
</dt> <dd> <dl> <dt>

6851 (0x1AC3) 
</dt> <dt>



無法完成操作，因為磁片區已中途變更。 請執行 chkdsk，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**\_ \_ \_ \_ 在交易中沒有連結追蹤的錯誤 \_**
</dt> <dd> <dl> <dt>

6852 (0x1AC4) 
</dt> <dt>



因為交易正在使用中，所以無法完成連結追蹤作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_ \_ \_ 交易中不支援 \_ \_ 錯誤作業**
</dt> <dd> <dl> <dt>

6853 (0x1AC5) 
</dt> <dt>



這項作業無法在交易中執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**錯誤 \_ 過期的 \_ 控制碼**
</dt> <dd> <dl> <dt>

6854 (0x1AC6) 
</dt> <dt>



控制碼已不再與交易的關聯正確。 它可能已在交易式資源管理員中開啟，之後會強制重新開機。 請關閉控點，並開啟一個新控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**錯誤 \_ 交易 \_ 未 \_ 登記**
</dt> <dd> <dl> <dt>

6855 (0x1AC7) 
</dt> <dt>



無法執行指定的作業，因為未在交易中登記資源管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**錯誤 \_ CTX \_ WINSTATION \_ 名稱 \_ 無效**
</dt> <dd> <dl> <dt>

7001 (0x1B59) 
</dt> <dt>



指定的會話名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**\_CTX \_ 不正確 \_ PD 時發生錯誤**
</dt> <dd> <dl> <dt>

7002 (0x1B5A) 
</dt> <dt>



指定的通訊協定驅動程式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**\_ \_ \_ 找不到 CTX \_ PD 的錯誤**
</dt> <dd> <dl> <dt>

7003 (0x1B5B) 
</dt> <dt>



在系統路徑中找不到指定的通訊協定驅動程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**錯誤 \_ CTX \_ \_ 找不 \_ 到 WD**
</dt> <dd> <dl> <dt>

7004 (0x1B5C) 
</dt> <dt>



在系統路徑中找不到指定的終端機連接驅動程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**\_CTX \_ 無法 \_ 建立 \_ EVENTLOG \_ 專案時發生錯誤**
</dt> <dd> <dl> <dt>

7005 (0x1B5D) 
</dt> <dt>



無法為此會話建立事件記錄的登錄機碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**\_CTX \_ 服務 \_ 名稱 \_ 衝突時發生錯誤**
</dt> <dd> <dl> <dt>

7006 (0x1B5E) 
</dt> <dt>



系統上已有相同名稱的服務存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**\_CTX \_ 關閉 \_ 擱置中時發生錯誤**
</dt> <dd> <dl> <dt>

7007 (0x1B5F) 
</dt> <dt>



會話上的關閉作業暫止。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**\_CTX \_ 無 \_ OUTBUF 時發生錯誤**
</dt> <dd> <dl> <dt>

7008 (0x1B60) 
</dt> <dt>



沒有可用的輸出緩衝區。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**\_CTX \_ \_ \_ \_ 找不到數據機 INF 時發生錯誤**
</dt> <dd> <dl> <dt>

7009 (0x1B61) 
</dt> <dt>



數據機。找不到 INF 檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**\_CTX \_ 不正確 \_ MODEMNAME 時發生錯誤**
</dt> <dd> <dl> <dt>

7010 (0x1B62) 
</dt> <dt>



在數據機中找不到數據機名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**\_CTX \_ 數據機 \_ 回應 \_ 錯誤時發生錯誤**
</dt> <dd> <dl> <dt>

7011 (0x1B63) 
</dt> <dt>



數據機未接受傳送給它的命令。 確認設定的數據機名稱符合連接的數據機。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**\_CTX \_ 數據機 \_ 回應 \_ 超時時發生錯誤**
</dt> <dd> <dl> <dt>

7012 (0x1B64) 
</dt> <dt>



數據機未回應傳送給它的命令。 確認數據機已正確連接電源並開啟電源。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**\_CTX \_ 數據機 \_ 回應 \_ 無 \_ 貨運公司時發生錯誤**
</dt> <dd> <dl> <dt>

7013 (0x1B65) 
</dt> <dt>



因為中斷連線，所以電訊廠商偵測失敗或貨運公司已中斷。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**\_CTX \_ 數據機 \_ 回應 \_ 沒有 \_ 撥號撥號時發生錯誤**
</dt> <dd> <dl> <dt>

7014 (0x1B66) 
</dt> <dt>



在所需時間內未偵測到撥號音。 確認電話纜線已正確連接且正常運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**\_CTX \_ 數據機 \_ 回應 \_ 忙碌時發生錯誤**
</dt> <dd> <dl> <dt>

7015 (0x1B67) 
</dt> <dt>



在回呼上的遠端網站偵測到忙碌信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**\_CTX \_ 數據機 \_ 回應 \_ 聲音時發生錯誤**
</dt> <dd> <dl> <dt>

7016 (0x1B68) 
</dt> <dt>



在回呼上的遠端網站偵測到語音。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**\_CTX \_ TD \_ 錯誤時發生錯誤**
</dt> <dd> <dl> <dt>

7017 (0x1B69) 
</dt> <dt>



傳輸驅動程式錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**錯誤 \_ CTX \_ \_ 找不 \_ 到 WINSTATION**
</dt> <dd> <dl> <dt>

7022 (0x1B6E) 
</dt> <dt>



找不到指定的會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**錯誤 \_ CTX \_ WINSTATION \_ 已經 \_ 存在**
</dt> <dd> <dl> <dt>

7023 (0x1B6F) 
</dt> <dt>



指定的會話名稱已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**\_CTX \_ WINSTATION \_ 忙碌時發生錯誤**
</dt> <dd> <dl> <dt>

7024 (0x1B70) 
</dt> <dt>



因為遠端桌面服務目前忙碌中，所以您嘗試執行的工作無法完成。 請等候一段時間後再試一次。 其他使用者仍應能夠登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**\_CTX 錯誤 \_ 的 \_ 影片 \_ 模式時發生錯誤**
</dt> <dd> <dl> <dt>

7025 (0x1B71) 
</dt> <dt>



嘗試連接到目前的用戶端不支援其影片模式的會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**\_CTX \_ 圖形 \_ 無效時發生錯誤**
</dt> <dd> <dl> <dt>

7035 (0x1B7B) 
</dt> <dt>



應用程式嘗試啟用 DOS 圖形模式。 不支援 DOS 圖形模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**錯誤 \_ CTX \_ 登入 \_ 已停用**
</dt> <dd> <dl> <dt>

7037 (0x1B7D) 
</dt> <dt>



您的互動式登入許可權已停用。 請連絡您的管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**\_CTX \_ 不是 \_ 主控台時發生錯誤**
</dt> <dd> <dl> <dt>

7038 (0x1B7E) 
</dt> <dt>



要求的操作只能在系統主控台上執行。 這通常是需要直接存取主控台的驅動程式或系統 DLL 的結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**\_CTX \_ 用戶端 \_ 查詢 \_ 逾時錯誤**
</dt> <dd> <dl> <dt>

7040 (0x1B80) 
</dt> <dt>



用戶端無法回應伺服器連接訊息。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**\_CTX \_ 主控台 \_ 中斷連線時發生錯誤**
</dt> <dd> <dl> <dt>

7041 (0x1B81) 
</dt> <dt>



不支援中斷連線主控台會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**\_CTX \_ 主控台 \_ 連接時發生錯誤**
</dt> <dd> <dl> <dt>

7042 (0x1B82) 
</dt> <dt>



不支援將已中斷連線的會話重新連接到主控台。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**錯誤 \_ CTX \_ 陰影 \_ 拒絕**
</dt> <dd> <dl> <dt>

7044 (0x1B84) 
</dt> <dt>



遠端控制另一個會話的要求遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**錯誤 \_ CTX \_ \_ 拒絕存取 \_ WINSTATION**
</dt> <dd> <dl> <dt>

7045 (0x1B85) 
</dt> <dt>



要求的會話存取被拒。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**\_CTX \_ 不正確 \_ WD 時發生錯誤**
</dt> <dd> <dl> <dt>

7049 (0x1B89) 
</dt> <dt>



指定的終端機連接驅動程式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**\_CTX \_ 陰影 \_ 無效時發生錯誤**
</dt> <dd> <dl> <dt>

7050 (0x1B8A) 
</dt> <dt>



要求的會話無法從遠端控制。 這可能是因為會話已中斷連線，或目前沒有使用者登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**\_CTX \_ \_ 停用陰影時發生錯誤**
</dt> <dd> <dl> <dt>

7051 (0x1B8B) 
</dt> <dt>



要求的會話未設定為允許遠端控制。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**\_CTX \_ \_ \_ 使用中的用戶端授權 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

7052 (0x1B8C) 
</dt> <dt>



您對此終端機伺服器的連線要求已被拒絕。 您的終端機伺服器用戶端授權號碼目前正由另一位使用者使用中。 請呼叫您的系統管理員以取得唯一的授權號碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**\_CTX \_ 用戶端 \_ 授權 \_ 未 \_ 設定時發生錯誤**
</dt> <dd> <dl> <dt>

7053 (0x1B8D) 
</dt> <dt>



您對此終端機伺服器的連線要求已被拒絕。 尚未輸入終端機伺服器用戶端副本的終端機伺服器用戶端授權號碼。 請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**\_ \_ \_ 無法使用 CTX 授權 \_ 錯誤**
</dt> <dd> <dl> <dt>

7054 (0x1B8E) 
</dt> <dt>



與這部電腦的連線數目會受到限制，且目前正在使用所有連接。 請稍後再嘗試連接，或洽詢您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**\_CTX \_ 授權 \_ 用戶端 \_ 無效時發生錯誤**
</dt> <dd> <dl> <dt>

7055 (0x1B8F) 
</dt> <dt>



您使用的用戶端未獲得使用此系統的授權。 您的登入要求遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**\_CTX \_ 授權 \_ 過期時發生錯誤**
</dt> <dd> <dl> <dt>

7056 (0x1B90) 
</dt> <dt>



系統授權已過期。 您的登入要求遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**錯誤 \_ CTX \_ 陰影 \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

7057 (0x1B91) 
</dt> <dt>



無法終止遠端控制，因為指定的會話目前不在遠端控制。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**\_CTX \_ \_ \_ 由 \_ 模式 \_ 變更結束時的陰影**
</dt> <dd> <dl> <dt>

7058 (0x1B92) 
</dt> <dt>



主控台的遠端控制已終止，因為顯示模式已變更。 不支援在遠端控制會話中變更顯示模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_超過錯誤啟用 \_ 計數 \_**
</dt> <dd> <dl> <dt>

7059 (0x1B93) 
</dt> <dt>



此安裝已重設啟用的次數上限。 將不會清除您的啟用計時器。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**錯誤 \_ CTX \_ WINSTATIONS \_ 已停用**
</dt> <dd> <dl> <dt>

7060 (0x1B94) 
</dt> <dt>



遠端登入目前已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**\_CTX \_ 所需的加密 \_ 層級 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

7061 (0x1B95) 
</dt> <dt>



您沒有適當的加密層級可存取此會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**\_CTX \_ \_ 使用中的 \_ 會話時發生錯誤**
</dt> <dd> <dl> <dt>

7062 (0x1B96) 
</dt> <dt>



使用者% s \\ \\ % s 目前已登入這部電腦。 只有目前的使用者或系統管理員可以登入這部電腦。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**錯誤 \_ CTX \_ 無 \_ 強制 \_ 登出**
</dt> <dd> <dl> <dt>

7063 (0x1B97) 
</dt> <dt>



使用者% s \\ \\ % s 已經登入這部電腦的主控台。 您目前沒有登入的許可權。 若要解決此問題，請洽詢% s \\ \\ % s 並登出。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**\_CTX \_ 帳戶 \_ 限制時發生錯誤**
</dt> <dd> <dl> <dt>

7064 (0x1B98) 
</dt> <dt>



因為帳戶限制，所以無法將您登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**錯誤 \_ RDP \_ 通訊協定 \_ 錯誤**
</dt> <dd> <dl> <dt>

7065 (0x1B99) 
</dt> <dt>



RDP 通訊協定元件 %2 偵測到通訊協定資料流程中的錯誤，並已中斷用戶端連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**\_CTX \_ CDM \_ CONNECT 時發生錯誤**
</dt> <dd> <dl> <dt>

7066 (0x1B9A) 
</dt> <dt>



用戶端磁片磁碟機對應服務已在終端機連線上連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**\_CTX \_ CDM \_ 中斷連線時發生錯誤**
</dt> <dd> <dl> <dt>

7067 (0x1B9B) 
</dt> <dt>



用戶端磁片磁碟機對應服務已在終端機連接中斷連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**\_CTX \_ 安全性層 \_ 級 \_ 錯誤時發生錯誤**
</dt> <dd> <dl> <dt>

7068 (0x1B9C) 
</dt> <dt>



終端機伺服器安全性階層偵測到通訊協定資料流程中的錯誤，並已中斷用戶端連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**\_TS \_ 不相容 \_ 會話錯誤**
</dt> <dd> <dl> <dt>

7069 (0x1B9D) 
</dt> <dt>



目標會話與目前的會話不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**錯誤 \_ TS \_ 影片 \_ 子系統 \_ 錯誤**
</dt> <dd> <dl> <dt>

7070 (0x1B9E) 
</dt> <dt>



Windows 無法連線到您的會話，因為 Windows video 子系統發生問題。 請稍後再試一次連接，或洽詢伺服器管理員以取得協助。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS \_ 錯誤 \_ 的 \_ API \_ 序列無效**
</dt> <dd> <dl> <dt>

8001 (0x1F41) 
</dt> <dt>



檔案複寫服務 API 的呼叫不正確。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS \_ ERR \_ 正在啟動 \_ 服務**
</dt> <dd> <dl> <dt>

8002 (0x1F42) 
</dt> <dt>



無法啟動 file replication service。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ 錯誤 \_ 停止 \_ 服務**
</dt> <dd> <dl> <dt>

8003 (0x1F43) 
</dt> <dt>



無法停止 file replication service。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS \_ ERR \_ 內部 \_ API**
</dt> <dd> <dl> <dt>

8004 (0x1F44) 
</dt> <dt>



檔案複寫服務 API 已終止要求。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ ERR \_ 內部**
</dt> <dd> <dl> <dt>

8005 (0x1F45) 
</dt> <dt>



檔案複寫服務已終止要求。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ ERR \_ 服務 \_ 通訊**
</dt> <dd> <dl> <dt>

8006 (0x1F46) 
</dt> <dt>



無法連絡檔案複寫服務。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ 錯誤 \_ 的 \_ 特權不足**
</dt> <dd> <dl> <dt>

8007 (0x1F47) 
</dt> <dt>



因為使用者的許可權不足，所以檔案複寫服務無法滿足要求。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS \_ ERR \_ 驗證**
</dt> <dd> <dl> <dt>

8008 (0x1F48) 
</dt> <dt>



因為無法使用已驗證的 RPC，所以檔案複寫服務無法滿足要求。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ ERR \_ 父系的 \_ 許可權不足 \_**
</dt> <dd> <dl> <dt>

8009 (0x1F49) 
</dt> <dt>



因為使用者的網域控制站許可權不足，所以檔案複寫服務無法滿足要求。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS \_ ERR \_ 父 \_ 驗證**
</dt> <dd> <dl> <dt>

8010 (0x1F4A) 
</dt> <dt>



檔案複寫服務無法滿足要求，因為網域控制站上無法使用已驗證的 RPC。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ ERR \_ 子系 \_ 對 \_ 父 \_ 通訊**
</dt> <dd> <dl> <dt>

8011 (0x1F4B) 
</dt> <dt>



檔案複寫服務無法與網域控制站上的檔案複寫服務進行通訊。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ ERR \_ 父代 \_ 至 \_ 子 \_ 通訊**
</dt> <dd> <dl> <dt>

8012 (0x1F4C) 
</dt> <dt>



網域控制站上的檔案複寫服務無法與這部電腦上的檔案複寫服務進行通訊。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ 錯誤 \_ SYSVOL \_ 填入**
</dt> <dd> <dl> <dt>

8013 (0x1F4D) 
</dt> <dt>



因為發生內部錯誤，所以檔案複寫服務無法填入系統磁碟區。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ 錯誤 \_ SYSVOL \_ 填入 \_ 超時**
</dt> <dd> <dl> <dt>

8014 (0x1F4E) 
</dt> <dt>



因為發生內部超時，所以檔案複寫服務無法填入系統磁碟區。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ ERR \_ SYSVOL \_ \_ 忙碌中**
</dt> <dd> <dl> <dt>

8015 (0x1F4F) 
</dt> <dt>



檔案複寫服務無法處理要求。 系統磁碟區正忙於先前的要求。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ ERR \_ SYSVOL \_ 降級**
</dt> <dd> <dl> <dt>

8016 (0x1F50) 
</dt> <dt>



因為發生內部錯誤，所以檔案複寫服務無法停止複寫系統磁碟區。 事件記錄檔可能會有詳細資訊。


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ 錯誤 \_ 的 \_ 服務 \_ 參數無效**
</dt> <dd> <dl> <dt>

8017 (0x1F51) 
</dt> <dt>



檔案複寫服務偵測到不正確參數。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




