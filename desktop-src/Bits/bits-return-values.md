---
title: BITS 傳回值
description: Bitsmsg 檔案包含下列傳回值常數。
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- 錯誤位
- 錯誤位，代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933485"
---
# <a name="bits-return-values"></a>BITS 傳回值

Bitsmsg 檔案包含下列傳回值常數。 常數代表 BITS 產生的傳回值，以及 BITS 所捕捉的 HTTP 傳回值。 您可以接收的所有其他傳回值為 COM、RPC 或轉換的 Windows 傳回值 (位使用 [ \_ \_ WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) 宏的 hresult 將 windows 傳回值轉換成 hresult 值) 。

請注意，Bitsmsg 檔案包含以下未列出的其他傳回值。

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S \_ 部分 \_ 完整 (0x00200017) 
</dt> <dd>

在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法之前，已成功傳輸作業檔案的子集。 未完成的已刪除。

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ \_ 無法 \_ 刪除檔案 \_ \_ (0x0020001A) 
</dt> <dd>

無法刪除與作業相關聯的所有暫存檔案。

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>\_ \_ \_ 由原則覆寫的 BG \_ (0x00200055) 
</dt> <dd>

已成功儲存設定喜好設定，但因為設定的群組原則設定會覆寫喜好設定，所以不會使用喜好設定。

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>\_ \_ \_ (0x80200001) 找不到 BG E
</dt> <dd>

找不到要求的作業。

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E \_ 不正確 \_ 狀態 (0x80200002) 
</dt> <dd>

目前的作業狀態不允許要求的動作。

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ EMPTY (0x80200003) 
</dt> <dd>

作業必須包含一或多個檔案，您才能繼續作業。

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_無法使用 BG E 檔案 \_ \_ \_ (0x80200004) 
</dt> <dd>

因為錯誤未與本機或遠端檔案相關聯，所以無法使用檔案資訊。

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG \_ E \_ 通訊協定 \_ 無法 \_ 使用 (0x80200005) 
</dt> <dd>

因為錯誤未與指定的傳輸通訊協定相關聯，所以無法使用通訊協定資訊。

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ 目的地已 \_ 鎖定 (0x8020000D) 
</dt> <dd>

本機檔案名中指定的目的地檔案系統磁片區已被鎖定。

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E \_ 磁片區 \_ 變更 (0x8020000E) 
</dt> <dd>

本機檔案名中指定的目的地磁片區已變更。 例如，原始磁片磁碟機已被不同的磁片磁碟機取代。

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ \_ \_ (0X8020000F) 無法使用 BG E 錯誤資訊
</dt> <dd>

只有當作業的狀態為 [BG 作業狀態] 錯誤時，才可使用錯誤資訊 \_ \_ \_ 。 在 BITS 開始傳送作業的資料或用戶端結束之後，無法使用錯誤資訊。

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ 網路已 \_ 中斷連線 (0x80200010) 
</dt> <dd>

網路介面卡為非使用中或已中斷連線。 所有作業都會處於「BG \_ 作業 \_ 狀態」 \_ 暫時性 \_ 錯誤狀態。

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ 遺失 \_ 檔案 \_ 大小 (0x80200011) 
</dt> <dd>

伺服器未傳回檔案大小。 BITS 只會傳送靜態內容，而且需要 HTTP 伺服器傳回內容長度標頭。 如果 URL 指向動態內容，傳送要求就會失敗。

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E \_ \_ HTTP \_ 支援 (0x80200012) 
</dt> <dd>

伺服器不支援 HTTP/1.1 通訊協定。

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E \_ 的 \_ 範圍 \_ 支援 (0x80200013) 
</dt> <dd>

伺服器不支援內容約制標頭。 一般來說，當您嘗試下載動態內容時，您會收到這個錯誤。 如果中繼 proxy 正在移除內容約制或內容長度標頭，您也可能會收到此錯誤。

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ 不支援 BG E 遠端 \_ \_ (0x80200014) 
</dt> <dd>

不支援 BITS 的遠端使用。 如需詳細資訊，請參閱 [使用者和網路連接](users-and-network-connections.md)。

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ 新的 \_ 擁有者 \_ 差異 \_ 對應 (0x80200015) 
</dt> <dd>

本機檔案的網路磁碟機機對應與先前擁有者的目前擁有者不同。

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ 新 \_ 擁有 \_ 者 \_ 沒有 \_ (0x80200016) 的檔案存取權
</dt> <dd>

新擁有者的許可權不足，無法暫存工作檔案。

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG \_ E \_ PROXY \_ 列出 \_ 太 \_ 大的 (0x80200018) 
</dt> <dd>

HTTP proxy 清單太長。 清單不得超過 32 KB。

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E \_ PROXY \_ 略過 \_ 清單 \_ 太 \_ 大 (0x80200019) 
</dt> <dd>

HTTP proxy 略過清單太長。 清單不得超過 32 KB。

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ % \_ \_ \_ (0x8020001C) 的檔太多
</dt> <dd>

您無法將一個以上的檔案新增至上傳作業。

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG \_ E \_ 本機 \_ 檔 \_ 已變更 (0x8020001D) 
</dt> <dd>

本機檔案的內容會在傳送程式開始之後變更。 在上傳或上傳回復作業開始傳送程式之後，無法變更本機檔案的內容。

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ 太 \_ 大 (0x80200020) 
</dt> <dd>

上傳檔案的大小超過伺服器上指定的允許上傳大小上限。

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E \_ 字串 \_ 太 \_ 長 (0x80200021) 
</dt> <dd>

指定的字串太長。

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG \_ E \_ 用戶端 \_ 伺服器 \_ 通訊協定 \_ 不相符 (0x80200022) 
</dt> <dd>

用戶端和伺服器無法協商要用於上傳作業的通訊協定。

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_ \_ 已啟用 BG E SERVER \_ 執行 \_ (0x80200023) 
</dt> <dd>

腳本或執行許可權會在與作業相關聯的 IIS 虛擬目錄上啟用。 若要將檔案上傳至虛擬目錄，請停用虛擬目錄的腳本和執行許可權。

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E 使用者 \_ 名稱 \_ 太 \_ 大 (0x80200025) 
</dt> <dd>

使用者名稱不能超過300個字元。

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ 密碼 \_ 太 \_ 大 (0x80200026) 
</dt> <dd>

密碼不能超過65535個字元。

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ 不正確 \_ 驗證 \_ 目標 (0x80200027) 
</dt> <dd>

指定的驗證目標無效。

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ 不正確 \_ 驗證 \_ 配置 (0x80200028) 
</dt> <dd>

指定的驗證配置無效。

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ 不正確 \_ 範圍 (0x8020002B) 
</dt> <dd>

指定的位元組範圍無效。 位元組範圍必須存在於指定的遠端檔案中。

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG \_ E 重 \_ 迭 \_ 範圍 (0x8020002C) 
</dt> <dd>

位元組範圍清單包含重迭或重複的範圍，但不受支援。

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ \_ \_ (0x8020003E) 的原則封鎖
</dt> <dd>

群組原則設定會防止背景工作在此時間執行。 如需詳細資訊，請參閱 [MaxInternetBandwidth](group-policies.md) 原則。

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ 不正確 \_ PROXY \_ 資訊 (0x8020003F) 
</dt> <dd>

指出您使用 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 方法指定的 proxy 清單或 proxy 略過清單不正確執行階段錯誤。

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ 不正確 \_ 認證 (0x80200040) 
</dt> <dd>

提供的安全性認證格式無效。

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_ \_ 已刪除 BG E 記錄 \_ (0x80200042) 
</dt> <dd>

快取記錄已刪除。 嘗試更新它已被放棄。

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG \_ E \_ UPNP \_ 錯誤 (0x80200045) 
</dt> <dd>

發生通用隨插即用 (UPnP) 錯誤。 請檢查您的網際網路閘道裝置。

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>\_已停用 BG E 對等 \_ \_ (0x80200047) 
</dt> <dd>

對等快取已停用。

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048) 
</dt> <dd>

快取記錄正在使用中，無法變更或刪除。 請在幾秒後再試一次。

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ \_ \_ \_ \_ \_ (0x80200049) 的每位使用者太多作業
</dt> <dd>

使用者的作業計數已超過 MaxJobsPerUser 群組原則設定所設定的每個使用者作業限制。

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ \_ \_ \_ \_ 每 \_ 台電腦 (0x80200050) 的作業太多
</dt> <dd>

電腦的工作計數已超過 MaxJobsPerMachine 群組原則設定所設定的每一電腦作業限制。

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ \_ \_ \_ \_ (0x80200051) 中有太多檔案在 \_ 工作中
</dt> <dd>

作業的檔案計數已超過 MaxFilesPerJob 群組原則設定所設定的每個作業檔限制。

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG% 檔案 \_ \_ \_ \_ \_ (0x80200052 中有太多範圍 \_) 
</dt> <dd>

檔案的範圍計數已超過 MaxRangesPerFile 群組原則設定所設定的每個檔案範圍限制。

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG \_ E \_ 驗證 \_ 失敗 (0x80200053) 
</dt> <dd>

應用程式要求來自網站的資料，但回應無效。 如需詳細資訊，請使用事件檢視器來查看 \\ Microsoft \\ Windows \\ Bits-用戶端作業記錄檔的應用程式記錄 \\ 。

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ MAXDOWNLOAD \_ TIMEOUT (0x80200054) 
</dt> <dd>

BITS 的下載作業已超時。 下載作業未在作業或 MaxDownloadTime 群組原則設定上設定的下載時間上限內完成。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 400 (0x80190190) 
</dt> <dd>

伺服器無法處理傳送要求，因為遠端檔案名的語法無效。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 401 (0x80190191) 
</dt> <dd>

使用者沒有存取遠端檔案的許可權。 要求的資源需要進行使用者驗證。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 404 (0x80190194) 
</dt> <dd>

要求的 URL 不存在於伺服器上。

在 IIS 7 中，此錯誤可能表示

-   在伺服器上 (vdir) 的虛擬目錄上，不會啟用該位上傳。
-   上傳大小超過最大上傳限制 (如需詳細資訊，請參閱 [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS 延伸模組屬性) 。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 407 (0x80190197) 
</dt> <dd>

使用者沒有存取 proxy 的許可權。 Proxy 需要使用者驗證。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 414 (0x8019019E) 
</dt> <dd>

伺服器無法處理傳送要求。 遠端檔案名 (URI) 的統一資源識別項長度超過伺服器可解讀的長度。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 501 (0x801901F5) 
</dt> <dd>

伺服器不支援完成要求所需的功能。 在 IIS 6 中，此錯誤表示伺服器上 (vdir) 的虛擬目錄上未啟用 BITS 上傳。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 503 (0x801901F7) 
</dt> <dd>

服務暫時超載，無法處理要求。 稍後再繼續作業。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 504 (0x801901F8) 
</dt> <dd>

等候閘道時，傳送要求超時。 稍後再繼續作業。

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 505 (0x801901F9) 
</dt> <dd>

伺服器不支援遠端檔案名中指定的 HTTP 通訊協定版本。

</dd> </dl>

Bitsmsg 標頭檔包含上面未列出的額外 HTTP 傳回值，位在內部使用。 如需這些和其他您可以接收之 HTTP 傳回值的相關資訊，請參閱來自網際網路工程任務推動小組的 RFC 2616 規格 [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) 。

 

 