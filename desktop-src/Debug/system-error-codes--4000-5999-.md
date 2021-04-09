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
# <a name="system-error-codes-4000-5999"></a>系統錯誤碼 (4000-5999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述錯誤4000到5999的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**\_內部錯誤獲勝 \_**
</dt> <dd> <dl> <dt>

4000 (0xFA0) 
</dt> <dt>



WINS 在處理命令時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**錯誤 \_ \_ 無法 \_ DEL 到 \_ 本機 \_ WINS**
</dt> <dd> <dl> <dt>

4001 (0xFA1) 
</dt> <dt>



無法刪除本機 WINS。


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**\_靜態 \_ INIT 錯誤**
</dt> <dd> <dl> <dt>

4002 (0xFA2) 
</dt> <dt>



從檔案匯入失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**錯誤 \_ INC. \_ 備份**
</dt> <dd> <dl> <dt>

4003 (0xFA3) 
</dt> <dt>



備份失敗。 是否已完成完整備份？


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_完整 \_ 備份時發生錯誤**
</dt> <dd> <dl> <dt>

4004 (0xFA4) 
</dt> <dt>



備份失敗。 檢查您要備份資料庫的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**錯誤 \_ REC \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

4005 (0xFA5) 
</dt> <dt>



WINS 資料庫中不存在此名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**\_ \_ 不允許錯誤 \_ RPL**
</dt> <dd> <dl> <dt>

4006 (0xFA6) 
</dt> <dt>



不允許使用 nonconfigured 夥伴進行複寫。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**未 \_ 支援的 PEERDIST 錯誤 \_ CONTENTINFO \_ 版本 \_**
</dt> <dd> <dl> <dt>

4050 (0xFD2) 
</dt> <dt>



不支援所提供的內容資訊版本。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST \_ 錯誤 \_ 無法 \_ 剖析 \_ CONTENTINFO**
</dt> <dd> <dl> <dt>

4051 (0xFD3) 
</dt> <dt>



提供的內容資訊格式不正確。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ 遺漏 \_ 資料的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4052 (0xFD4) 
</dt> <dt>



在本機或對等快取中找不到要求的資料。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_未發生 PEERDIST 錯誤 \_ \_**
</dt> <dd> <dl> <dt>

4053 (0xFD5) 
</dt> <dt>



沒有其他資料可供使用或不需要。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_ \_ 未 \_ 初始化的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4054 (0xFD6) 
</dt> <dt>



提供的物件尚未初始化。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_ \_ 已 \_ 初始化的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4055 (0xFD7) 
</dt> <dt>



提供的物件已經初始化。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ \_ 正在關閉 \_ 正在進行的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4056 (0xFD8) 
</dt> <dt>



關機操作已在進行中。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**已 \_ 不正確 PEERDIST 錯誤 \_**
</dt> <dd> <dl> <dt>

4057 (0xFD9) 
</dt> <dt>



提供的物件已經無效。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**\_ \_ 已存在 PEERDIST \_ 錯誤**
</dt> <dd> <dl> <dt>

4058 (0xFDA) 
</dt> <dt>



元素已經存在，且未被取代。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST \_ 錯誤 \_ 作業 \_ NOTFOUND**
</dt> <dd> <dl> <dt>

4059 (0xFDB) 
</dt> <dt>



無法取消要求的作業，因為它已經完成。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_ \_ 已 \_ 完成的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4060 (0xFDC) 
</dt> <dt>



無法執行依照作業，因為已執行此作業。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST \_ 錯誤 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

4061 (0xFDD) 
</dt> <dt>



作業存取的資料超出有效資料的範圍。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_不支援的 PEERDIST 錯誤 \_ 版本 \_**
</dt> <dd> <dl> <dt>

4062 (0xFDE) 
</dt> <dt>



不支援要求的版本。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST \_ 錯誤 \_ 不正確設定 \_**
</dt> <dd> <dl> <dt>

4063 (0xFDF) 
</dt> <dt>



設定值無效。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_ \_ 未 \_ 授權的 PEERDIST 錯誤**
</dt> <dd> <dl> <dt>

4064 (0xFE0) 
</dt> <dt>



SKU 未獲授權。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_ \_ 無法使用 PEERDIST 錯誤服務 \_**
</dt> <dd> <dl> <dt>

4065 (0xFE1) 
</dt> <dt>



PeerDist 服務仍在初始化中，很快就會推出。


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST \_ 錯誤 \_ 信任 \_ 失敗**
</dt> <dd> <dl> <dt>

4066 (0xFE2) 
</dt> <dt>



因為最近的錯誤，所以會暫時封鎖與一或多部電腦的通訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**\_DHCP \_ 位址 \_ 發生錯誤**
</dt> <dd> <dl> <dt>

4100 (0x1004) 
</dt> <dt>



DHCP 用戶端已取得網路上已在使用中的 IP 位址。 本機介面將會停用，直到 DHCP 用戶端可以取得新的位址為止。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**\_ \_ \_ 找不到 WMI \_ GUID 的錯誤**
</dt> <dd> <dl> <dt>

4200 (0x1068) 
</dt> <dt>



傳遞的 GUID 未被 WMI 資料提供者辨識為有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**\_ \_ \_ 找不到 WMI \_ 實例錯誤**
</dt> <dd> <dl> <dt>

4201 (0x1069) 
</dt> <dt>



傳遞的實例名稱無法被 WMI 資料提供者辨識為有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**\_ \_ \_ 找不到 WMI \_ ITEMID 的錯誤**
</dt> <dd> <dl> <dt>

4202 (0x106A) 
</dt> <dt>



傳遞的資料項目識別碼無法被 WMI 資料提供者辨識為有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**\_WMI \_ 再次嘗試 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

4203 (0x106B) 
</dt> <dt>



WMI 要求無法完成，應該重試。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**\_ \_ \_ 找不到 WMI \_ DP 錯誤**
</dt> <dd> <dl> <dt>

4204 (0x106C) 
</dt> <dt>



找不到 WMI 資料提供者。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**\_WMI \_ 無法解析的 \_ 實例 \_ 參考錯誤**
</dt> <dd> <dl> <dt>

4205 (0x106D) 
</dt> <dt>



WMI 資料提供者參考尚未註冊的實例集。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**\_WMI \_ 已 \_ 啟用的錯誤**
</dt> <dd> <dl> <dt>

4206 (0x106E) 
</dt> <dt>



WMI 資料區塊或事件通知已經啟用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**\_WMI \_ GUID 已 \_ 中斷連線時發生錯誤**
</dt> <dd> <dl> <dt>

4207 (0x106F) 
</dt> <dt>



WMI 資料區塊無法再使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**\_WMI \_ 伺服器 \_ 無法使用的錯誤**
</dt> <dd> <dl> <dt>

4208 (0x1070) 
</dt> <dt>



WMI 資料服務無法使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**\_WMI \_ DP \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

4209 (0x1071) 
</dt> <dt>



WMI 資料提供者無法執行要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**錯誤 \_ WMI \_ 不正確 \_ MOF**
</dt> <dd> <dl> <dt>

4210 (0x1072) 
</dt> <dt>



WMI MOF 資訊無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**錯誤 \_ WMI \_ 不正確 \_ REGINFO**
</dt> <dd> <dl> <dt>

4211 (0x1073) 
</dt> <dt>



WMI 註冊資訊無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**\_WMI \_ 已 \_ 停用的錯誤**
</dt> <dd> <dl> <dt>

4212 (0x1074) 
</dt> <dt>



WMI 資料區塊或事件通知已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**\_WMI \_ 唯讀錯誤 \_**
</dt> <dd> <dl> <dt>

4213 (0x1075) 
</dt> <dt>



WMI 資料項目目或資料區塊是唯讀的。


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**\_WMI \_ 設定 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

4214 (0x1076) 
</dt> <dt>



無法變更 WMI 資料項目或資料區塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**錯誤 \_ 不是 \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4250 (0x109A) 
</dt> <dt>



這項作業只會在應用程式容器的內容中有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**\_需要錯誤 APPCONTAINER \_**
</dt> <dd> <dl> <dt>

4251 (0x109B) 
</dt> <dt>



此應用程式只能在應用程式容器的內容中執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**\_ \_ \_ APPCONTAINER 中不支援的 \_ 錯誤**
</dt> <dd> <dl> <dt>

4252 (0x109C) 
</dt> <dt>



應用程式容器的內容中不支援這項功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**錯誤 \_ 不正確 \_ 封裝 \_ SID \_ 長度**
</dt> <dd> <dl> <dt>

4253 (0x109D) 
</dt> <dt>



提供的 SID 長度不是應用程式容器 Sid 的有效長度。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**錯誤 \_ 不正確 \_ 媒體**
</dt> <dd> <dl> <dt>

4300 (0x10CC) 
</dt> <dt>



媒體識別碼不代表有效的媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**錯誤 \_ 不正確連結 \_ 庫**
</dt> <dd> <dl> <dt>

4301 (0x10CD) 
</dt> <dt>



程式庫識別碼不代表有效的程式庫。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**錯誤 \_ 不正確 \_ 媒體 \_ 集區**
</dt> <dd> <dl> <dt>

4302 (0x10CE) 
</dt> <dt>



媒體集區識別碼不代表有效的媒體集區。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**錯誤 \_ 磁片磁碟機 \_ 媒體 \_ 不符**
</dt> <dd> <dl> <dt>

4303 (0x10CF) 
</dt> <dt>



磁片磁碟機和媒體不相容或存在於不同的程式庫中。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**錯誤 \_ 媒體 \_ 離線**
</dt> <dd> <dl> <dt>

4304 (0x10D0) 
</dt> <dt>



媒體目前存在於離線文件庫中，且必須在線上，才能執行這項操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**錯誤連結 \_ 庫 \_ 離線**
</dt> <dd> <dl> <dt>

4305 (0x10D1) 
</dt> <dt>



無法在離線程式庫上執行操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**錯誤 \_ 空白**
</dt> <dd> <dl> <dt>

4306 (0x10D2) 
</dt> <dt>



媒體櫃、磁片磁碟機或媒體集區是空的。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**錯誤 \_ 不是 \_ 空的**
</dt> <dd> <dl> <dt>

4307 (0x10D3) 
</dt> <dt>



媒體櫃、磁片磁碟機或媒體集區必須是空的，才能執行這種操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**錯誤 \_ 媒體 \_ 無法使用**
</dt> <dd> <dl> <dt>

4308 (0x10D4) 
</dt> <dt>



此媒體集區或媒體櫃中目前沒有可用的媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**錯誤 \_ 資源 \_ 已停用**
</dt> <dd> <dl> <dt>

4309 (0x10D5) 
</dt> <dt>



此操作所需的資源已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**\_不正確 \_ 清除程式錯誤**
</dt> <dd> <dl> <dt>

4310 (0x10D6) 
</dt> <dt>



媒體識別碼不代表有效的清除程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**\_無法 \_ \_ 清除錯誤**
</dt> <dd> <dl> <dt>

4311 (0x10D7) 
</dt> <dt>



磁片磁碟機無法清理或不支援清除。


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_ \_ 找不到錯誤物件 \_**
</dt> <dd> <dl> <dt>

4312 (0x10D8) 
</dt> <dt>



物件識別碼不代表有效的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**錯誤 \_ 資料庫 \_ 失敗**
</dt> <dd> <dl> <dt>

4313 (0x10D9) 
</dt> <dt>



無法讀取或寫入資料庫。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_資料庫已 \_ 滿的錯誤**
</dt> <dd> <dl> <dt>

4314 (0x10DA) 
</dt> <dt>



資料庫已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**錯誤 \_ 媒體 \_ 不相容**
</dt> <dd> <dl> <dt>

4315 (0x10DB) 
</dt> <dt>



媒體與裝置或媒體集區不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**錯誤 \_ 資源 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

4316 (0x10DC) 
</dt> <dt>



此操作所需的資源不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**錯誤 \_ 不正確作業 \_**
</dt> <dd> <dl> <dt>

4317 (0x10DD) 
</dt> <dt>



作業識別碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**錯誤 \_ 媒體 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

4318 (0x10DE) 
</dt> <dt>



媒體未裝載或可供使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**錯誤 \_ 裝置 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

4319 (0x10DF) 
</dt> <dt>



裝置尚未準備好可供使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**拒絕的錯誤 \_ 要求 \_**
</dt> <dd> <dl> <dt>

4320 (0x10E0) 
</dt> <dt>



操作員或系統管理員已拒絕要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**錯誤 \_ 不正確 \_ 磁片磁碟機 \_ 物件**
</dt> <dd> <dl> <dt>

4321 (0x10E1) 
</dt> <dt>



磁片磁碟機識別碼不代表有效的磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**錯誤 \_ 庫已 \_ 滿**
</dt> <dd> <dl> <dt>

4322 (0x10E2) 
</dt> <dt>



程式庫已滿。 沒有可供使用的位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**錯誤 \_ 媒體 \_ 無法 \_ 存取**
</dt> <dd> <dl> <dt>

4323 (0x10E3) 
</dt> <dt>



傳輸無法存取媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**\_無法 \_ \_ 載入媒體的 \_ 錯誤**
</dt> <dd> <dl> <dt>

4324 (0x10E4) 
</dt> <dt>



無法將媒體載入磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 磁片磁碟機**
</dt> <dd> <dl> <dt>

4325 (0x10E5) 
</dt> <dt>



無法取出磁片磁碟機狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 插槽**
</dt> <dd> <dl> <dt>

4326 (0x10E6) 
</dt> <dt>



無法取出位置狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**錯誤 \_ 無法 \_ \_ 清查 \_ 傳輸**
</dt> <dd> <dl> <dt>

4327 (0x10E7) 
</dt> <dt>



無法取得傳輸的狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**錯誤 \_ 傳輸已 \_ 滿**
</dt> <dd> <dl> <dt>

4328 (0x10E8) 
</dt> <dt>



無法使用傳輸，因為它已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**\_控制 \_ IEPORT 時發生錯誤**
</dt> <dd> <dl> <dt>

4329 (0x10E9) 
</dt> <dt>



無法開啟或關閉插入/退出埠。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**錯誤 \_ 無法 \_ \_ 退出 \_ 裝載的 \_ 媒體**
</dt> <dd> <dl> <dt>

4330 (0x10EA) 
</dt> <dt>



無法退出媒體，因為它位於磁片磁碟機中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**錯誤 \_ 清除 \_ 插槽位置 \_ 集合**
</dt> <dd> <dl> <dt>

4331 (0x10EB) 
</dt> <dt>



清除的位置已被保留。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**錯誤 \_ 清除 \_ 插槽 \_ 未 \_ 設定**
</dt> <dd> <dl> <dt>

4332 (0x10EC) 
</dt> <dt>



不會保留簡潔的位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**花費的錯誤 \_ 清除 \_ 磁帶 \_**
</dt> <dd> <dl> <dt>

4333 (0x10ED) 
</dt> <dt>



清除卷匣已執行磁片磁碟機清洗次數的上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**非 \_ 預期的錯誤 \_ OMID**
</dt> <dd> <dl> <dt>

4334 (0x10EE) 
</dt> <dt>



非預期的中型識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**無法 \_ \_ 刪除 \_ 最後一個 \_ 專案的錯誤**
</dt> <dd> <dl> <dt>

4335 (0x10EF) 
</dt> <dt>



無法刪除此群組或資源中最後一個剩餘的專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**錯誤 \_ 訊息 \_ 超過 \_ \_ 大小上限**
</dt> <dd> <dl> <dt>

4336 (0x10F0) 
</dt> <dt>



提供的訊息超過此參數允許的最大大小。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**錯誤 \_ 磁片區 \_ 包含 \_ SYS \_ 檔案**
</dt> <dd> <dl> <dt>

4337 (0x10F1) 
</dt> <dt>



磁片區包含系統或分頁檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**錯誤 \_ INDIGENOUS \_ 類型**
</dt> <dd> <dl> <dt>

4338 (0x10F2) 
</dt> <dt>



媒體類型無法從此媒體櫃中移除，因為媒體櫃中至少有一個磁片磁碟機報告它可以支援此媒體類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**錯誤， \_ 不 \_ 支援 \_ 磁片磁碟機**
</dt> <dd> <dl> <dt>

4339 (0x10F3) 
</dt> <dt>



此離線媒體無法在此系統上掛接，因為沒有任何已啟用的磁片磁碟機存在，可供使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**\_已安裝錯誤清除程式 \_ 墨水匣 \_**
</dt> <dd> <dl> <dt>

4340 (0x10F4) 
</dt> <dt>



磁帶媒體櫃中有一個整潔的墨水匣。


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**\_IEPORT \_ FULL 時發生錯誤**
</dt> <dd> <dl> <dt>

4341 (0x10F5) 
</dt> <dt>



無法使用插入/退出埠，因為它不是空的。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**離線的錯誤 \_ 檔 \_**
</dt> <dd> <dl> <dt>

4350 (0x10FE) 
</dt> <dt>



此檔案目前無法在這部電腦上使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**\_遠端 \_ 儲存體 \_ 未 \_ 啟用時發生錯誤**
</dt> <dd> <dl> <dt>

4351 (0x10FF) 
</dt> <dt>



遠端儲存體服務目前無法運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**\_遠端 \_ 存放裝置 \_ 媒體 \_ 錯誤**
</dt> <dd> <dl> <dt>

4352 (0x1100) 
</dt> <dt>



遠端儲存體服務發生媒體錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**錯誤 \_ 不 \_ 是重新 \_ 分析 \_ 點**
</dt> <dd> <dl> <dt>

4390 (0x1126) 
</dt> <dt>



檔案或目錄不是重新分析點。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**錯誤重新 \_ 分析 \_ 屬性 \_ 衝突**
</dt> <dd> <dl> <dt>

4391 (0x1127) 
</dt> <dt>



無法設定重新分析點屬性，因為它與現有的屬性衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**不正確重新 \_ \_ 分析 \_ 資料錯誤**
</dt> <dd> <dl> <dt>

4392 (0x1128) 
</dt> <dt>



重新分析點緩衝區中的資料無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**錯誤重新 \_ 分析 \_ 標記 \_ 無效**
</dt> <dd> <dl> <dt>

4393 (0x1129) 
</dt> <dt>



重新分析點緩衝區中出現的標記無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**錯誤重新 \_ 分析 \_ 標記 \_ 不符**
</dt> <dd> <dl> <dt>

4394 (0x112A) 
</dt> <dt>



要求中指定的標記和重新分析點中的標記不符。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**\_ \_ \_ \_ 找不到應用程式資料錯誤**
</dt> <dd> <dl> <dt>

4400 (0x1130) 
</dt> <dt>



找不到快取資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**\_應用程式 \_ 資料 \_ 過期時發生錯誤**
</dt> <dd> <dl> <dt>

4401 (0x1131) 
</dt> <dt>



快取資料已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**\_應用程式 \_ 資料損毀錯誤 \_**
</dt> <dd> <dl> <dt>

4402 (0x1132) 
</dt> <dt>



快取資料已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**超過錯誤的 \_ 應用程式 \_ 資料 \_ 限制 \_**
</dt> <dd> <dl> <dt>

4403 (0x1133) 
</dt> <dt>



快取資料已超過其大小上限，因此無法更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**\_ \_ \_ 需要重新開機應用程式資料錯誤 \_**
</dt> <dd> <dl> <dt>

4404 (0x1134) 
</dt> <dt>



快速快取已 ReArmed，需要重新開機，直到可以更新為止。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**偵測 \_ 到錯誤的 SECUREBOOT \_ 復原 \_**
</dt> <dd> <dl> <dt>

4420 (0x1144) 
</dt> <dt>



安全開機偵測到已嘗試回復受保護的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**錯誤的 \_ SECUREBOOT \_ 原則 \_ 違規**
</dt> <dd> <dl> <dt>

4421 (0x1145) 
</dt> <dt>



此值會受到安全開機原則的保護，且無法修改或刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**錯誤的 \_ SECUREBOOT \_ 無效 \_ 原則**
</dt> <dd> <dl> <dt>

4422 (0x1146) 
</dt> <dt>



安全開機原則無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤的 SECUREBOOT 原則發行者**
</dt> <dd> <dl> <dt>

4423 (0x1147) 
</dt> <dt>



新的安全開機原則未在其更新清單中包含目前的發行者。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**\_ \_ \_ 未簽署錯誤的 SECUREBOOT 原則 \_**
</dt> <dd> <dl> <dt>

4424 (0x1148) 
</dt> <dt>



安全開機原則可能未簽署，或由不信任的簽署者簽署。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**\_ \_ 未啟用錯誤 \_ SECUREBOOT**
</dt> <dd> <dl> <dt>

4425 (0x1149) 
</dt> <dt>



未在這部電腦上啟用安全開機。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**\_ \_ \_ 已取代錯誤的 SECUREBOOT 檔案**
</dt> <dd> <dl> <dt>

4426 (0x114A) 
</dt> <dt>



安全開機需要某些檔案和驅動程式不會被其他檔案或驅動程式取代。


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**錯誤 \_ 卸載 \_ 讀取 \_ FLT \_ 不 \_ 受支援**
</dt> <dd> <dl> <dt>

4440 (0x1158) 
</dt> <dt>



篩選不支援「複製卸載讀取」作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**\_ \_ \_ \_ 不支援錯誤卸載寫入 \_ FLT**
</dt> <dd> <dl> <dt>

4441 (0x1159) 
</dt> <dt>



篩選不支援「複製卸載寫入」作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤卸載讀取檔**
</dt> <dd> <dl> <dt>

4442 (0x115A) 
</dt> <dt>



檔案不支援複製卸載讀取操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤卸載寫入檔案**
</dt> <dd> <dl> <dt>

4443 (0x115B) 
</dt> <dt>



檔案不支援複製卸載寫入操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**錯誤 \_ 磁片 \_ 區 \_ 未 \_ 啟用 SIS**
</dt> <dd> <dl> <dt>

4500 (0x1194) 
</dt> <dt>



此磁片區上無法使用單一實例儲存體。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_相依 \_ 資源 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

5001 (0x1389) 
</dt> <dt>



無法完成操作，因為其他資源相依于此資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_ \_ \_ 找不到錯誤相依性**
</dt> <dd> <dl> <dt>

5002 (0x138A) 
</dt> <dt>



找不到叢集資源相依性。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**錯誤相依性 \_ \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

5003 (0x138B) 
</dt> <dt>



無法使叢集資源相依于指定的資源，因為它已經相依。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**錯誤 \_ 資源 \_ 未 \_ 上線**
</dt> <dd> <dl> <dt>

5004 (0x138C) 
</dt> <dt>



叢集資源不在線上。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**錯誤 \_ 主機 \_ 節點 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

5005 (0x138D) 
</dt> <dt>



此作業無法使用叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**錯誤 \_ 資源 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

5006 (0x138E) 
</dt> <dt>



叢集資源無法使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_ \_ 找不到錯誤資源 \_**
</dt> <dd> <dl> <dt>

5007 (0x138F) 
</dt> <dt>



找不到叢集資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**錯誤 \_ 關閉 \_ 叢集**
</dt> <dd> <dl> <dt>

5008 (0x1390) 
</dt> <dt>



正在關閉叢集。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**錯誤 \_ 無法 \_ 收回 \_ 主動 \_ 節點**
</dt> <dd> <dl> <dt>

5009 (0x1391) 
</dt> <dt>



除非節點已關閉或為最後一個節點，否則無法從叢集收回叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**錯誤 \_ 物件 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

5010 (0x1392) 
</dt> <dt>



物件已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_ \_ 清單中的 ERROR 物件 \_**
</dt> <dd> <dl> <dt>

5011 (0x1393) 
</dt> <dt>



此物件已經在清單中。


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**錯誤 \_ 群組 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

5012 (0x1394) 
</dt> <dt>



叢集群組無法供任何新的要求使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_ \_ 找不到錯誤群組 \_**
</dt> <dd> <dl> <dt>

5013 (0x1395) 
</dt> <dt>



找不到叢集群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**錯誤 \_ 群組 \_ 未 \_ 上線**
</dt> <dd> <dl> <dt>

5014 (0x1396) 
</dt> <dt>



無法完成操作，因為叢集群組不在線上。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**錯誤 \_ 主機 \_ 節點 \_ 不是 \_ 資源 \_ 擁有者**
</dt> <dd> <dl> <dt>

5015 (0x1397) 
</dt> <dt>



作業失敗，因為指定的叢集節點不是資源的擁有者，或節點不是資源的可能擁有者。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**錯誤 \_ 主機 \_ 節點 \_ 不是 \_ 群組 \_ 擁有者**
</dt> <dd> <dl> <dt>

5016 (0x1398) 
</dt> <dt>



作業失敗，因為指定的叢集節點不是群組擁有者，或者節點不是可能的群組擁有者。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**錯誤 \_ RESMON \_ 建立 \_ 失敗**
</dt> <dd> <dl> <dt>

5017 (0x1399) 
</dt> <dt>



無法在指定的資源監視器中建立叢集資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**\_線上錯誤 \_ RESMON \_ 失敗**
</dt> <dd> <dl> <dt>

5018 (0x139A) 
</dt> <dt>



資源監視器無法使叢集資源上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**\_線上錯誤資源 \_**
</dt> <dd> <dl> <dt>

5019 (0x139B) 
</dt> <dt>



因為叢集資源已上線，所以無法完成操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**錯誤 \_ 仲裁 \_ 資源**
</dt> <dd> <dl> <dt>

5020 (0x139C) 
</dt> <dt>



叢集資源無法刪除或離線，因為它是仲裁資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**錯誤 \_ 無法 \_ \_ 支援仲裁**
</dt> <dd> <dl> <dt>

5021 (0x139D) 
</dt> <dt>



叢集無法使指定的資源成為仲裁資源，因為它不能成為仲裁資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**錯誤 \_ 叢集 \_ 關機 \_**
</dt> <dd> <dl> <dt>

5022 (0x139E) 
</dt> <dt>



叢集軟體正在關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**錯誤 \_ 不正確 \_ 狀態**
</dt> <dd> <dl> <dt>

5023 (0x139F) 
</dt> <dt>



群組或資源不是正確的狀態，無法執行所要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**儲存的錯誤 \_ 資源 \_ 屬性 \_**
</dt> <dd> <dl> <dt>

5024 (0x13A0) 
</dt> <dt>



這些屬性已儲存，但在下一次資源上線之前，所有變更都不會生效。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**錯誤 \_ 不是 \_ 仲裁 \_ 類別**
</dt> <dd> <dl> <dt>

5025 (0x13A1) 
</dt> <dt>



叢集無法使指定的資源成為仲裁資源，因為它不屬於共用儲存類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**錯誤 \_ 核心 \_ 資源**
</dt> <dd> <dl> <dt>

5026 (0x13A2) 
</dt> <dt>



無法刪除叢集資源，因為它是核心資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**錯誤 \_ 仲裁 \_ 資源 \_ 線上 \_ 失敗**
</dt> <dd> <dl> <dt>

5027 (0x13A3) 
</dt> <dt>



仲裁資源無法上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**錯誤 \_ QUORUMLOG \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

5028 (0x13A4) 
</dt> <dt>



無法成功建立或裝載仲裁記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**錯誤 \_ CLUSTERLOG 損毀 \_**
</dt> <dd> <dl> <dt>

5029 (0x13A5) 
</dt> <dt>



叢集記錄檔已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**\_CLUSTERLOG \_ 記錄 \_ 超過 \_ MAXSIZE 時發生錯誤**
</dt> <dd> <dl> <dt>

5030 (0x13A6) 
</dt> <dt>



無法將記錄寫入叢集記錄檔，因為它超過大小上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**錯誤 \_ CLUSTERLOG \_ 超過 \_ MAXSIZE**
</dt> <dd> <dl> <dt>

5031 (0x13A7) 
</dt> <dt>



叢集記錄檔超過其大小上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**錯誤 \_ CLUSTERLOG \_ \_ 找不 \_ 到 CHKPOINT**
</dt> <dd> <dl> <dt>

5032 (0x13A8) 
</dt> <dt>



在叢集記錄檔中找不到檢查點記錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**錯誤 \_ CLUSTERLOG \_ \_ \_ 空間不足**
</dt> <dd> <dl> <dt>

5033 (0x13A9) 
</dt> <dt>



無法使用記錄所需的磁碟空間下限。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**錯誤 \_ 仲裁 \_ 擁有者運作中 \_**
</dt> <dd> <dl> <dt>

5034 (0x13AA) 
</dt> <dt>



叢集節點無法取得仲裁資源的控制權，因為資源是由另一個作用中節點所擁有。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**錯誤 \_ 網路 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

5035 (0x13AB) 
</dt> <dt>



此作業無法使用叢集網路。


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**錯誤 \_ 節點 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

5036 (0x13AC) 
</dt> <dt>



此作業無法使用叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**\_ \_ \_ 無法使用所有節點 \_ 的錯誤**
</dt> <dd> <dl> <dt>

5037 (0x13AD) 
</dt> <dt>



所有叢集節點都必須在執行中，才能執行此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**錯誤 \_ 資源 \_ 失敗**
</dt> <dd> <dl> <dt>

5038 (0x13AE) 
</dt> <dt>



叢集資源失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**錯誤 \_ 叢集 \_ 無效 \_ 節點**
</dt> <dd> <dl> <dt>

5039 (0x13AF) 
</dt> <dt>



叢集節點無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**錯誤 \_ 叢集 \_ 節點 \_ 存在**
</dt> <dd> <dl> <dt>

5040 (0x13B0) 
</dt> <dt>



叢集節點已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**錯誤 \_ 叢集 \_ 加入 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5041 (0x13B1) 
</dt> <dt>



節點正在加入叢集的進程中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**\_ \_ \_ \_ 找不到錯誤叢集節點**
</dt> <dd> <dl> <dt>

5042 (0x13B2) 
</dt> <dt>



找不到叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤叢集本機節點**
</dt> <dd> <dl> <dt>

5043 (0x13B3) 
</dt> <dt>



找不到叢集本機節點資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**錯誤 \_ 叢集 \_ 網路 \_ 存在**
</dt> <dd> <dl> <dt>

5044 (0x13B4) 
</dt> <dt>



叢集網路已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集網路**
</dt> <dd> <dl> <dt>

5045 (0x13B5) 
</dt> <dt>



找不到叢集網路。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**錯誤 \_ 叢集 \_ NETINTERFACE \_ 存在**
</dt> <dd> <dl> <dt>

5046 (0x13B6) 
</dt> <dt>



叢集網路介面已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 NETINTERFACE**
</dt> <dd> <dl> <dt>

5047 (0x13B7) 
</dt> <dt>



找不到叢集網路介面。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**錯誤叢集的 \_ \_ \_ 要求無效**
</dt> <dd> <dl> <dt>

5048 (0x13B8) 
</dt> <dt>



此物件的叢集要求無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**錯誤 \_ 群集 \_ 不正確 \_ 網路 \_ 提供者**
</dt> <dd> <dl> <dt>

5049 (0x13B9) 
</dt> <dt>



叢集網路提供者無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**錯誤 \_ 叢集 \_ 節點 \_ 關閉**
</dt> <dd> <dl> <dt>

5050 (0x13BA) 
</dt> <dt>



叢集節點已關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**無法連線到錯誤叢集 \_ \_ 節點 \_**
</dt> <dd> <dl> <dt>

5051 (0x13BB) 
</dt> <dt>



無法連線到叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**錯誤 \_ 叢集 \_ 節點 \_ 不是 \_ 成員**
</dt> <dd> <dl> <dt>

5052 (0x13BC) 
</dt> <dt>



叢集節點不是叢集的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**錯誤 \_ 叢集 \_ 加入 \_ 未 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5053 (0x13BD) 
</dt> <dt>



叢集聯結作業不在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ 網路**
</dt> <dd> <dl> <dt>

5054 (0x13BE) 
</dt> <dt>



叢集網路無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**錯誤 \_ 叢集 \_ 節點 \_ 啟動**
</dt> <dd> <dl> <dt>

5056 (0x13C0) 
</dt> <dt>



叢集節點已啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_ \_ \_ 使用中的錯誤叢集 IPADDR \_**
</dt> <dd> <dl> <dt>

5057 (0x13C1) 
</dt> <dt>



叢集 IP 位址已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**錯誤 \_ 叢集 \_ 節點 \_ 未 \_ 暫停**
</dt> <dd> <dl> <dt>

5058 (0x13C2) 
</dt> <dt>



叢集節點未暫停。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**錯誤 \_ 群集 \_ 沒有 \_ 安全性 \_ 內容**
</dt> <dd> <dl> <dt>

5059 (0x13C3) 
</dt> <dt>



沒有任何可用的叢集安全性內容。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**錯誤 \_ 叢集 \_ 網路 \_ 不是 \_ 內部**
</dt> <dd> <dl> <dt>

5060 (0x13C4) 
</dt> <dt>



叢集網路未設定為進行內部叢集通訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 啟動**
</dt> <dd> <dl> <dt>

5061 (0x13C5) 
</dt> <dt>



叢集節點已啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 關閉**
</dt> <dd> <dl> <dt>

5062 (0x13C6) 
</dt> <dt>



叢集節點已關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**錯誤 \_ 叢集 \_ 網路 \_ 已 \_ 上線**
</dt> <dd> <dl> <dt>

5063 (0x13C7) 
</dt> <dt>



叢集網路已上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**錯誤 \_ 叢集 \_ 網路 \_ 已 \_ 離線**
</dt> <dd> <dl> <dt>

5064 (0x13C8) 
</dt> <dt>



叢集網路已離線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已 \_ 成員**
</dt> <dd> <dl> <dt>

5065 (0x13C9) 
</dt> <dt>



叢集節點已經是叢集的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**錯誤 \_ 叢集 \_ 最後一個 \_ 內部 \_ 網路**
</dt> <dd> <dl> <dt>

5066 (0x13CA) 
</dt> <dt>



叢集網路是唯一針對兩個或多個作用中叢集節點之間的內部叢集通訊設定的網路。 無法從網路中移除內部通訊功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**錯誤 \_ 叢集 \_ 網路 \_ 有相依 \_ 項**
</dt> <dd> <dl> <dt>

5067 (0x13CB) 
</dt> <dt>



一或多個叢集資源相依于網路，以提供服務給用戶端。 用戶端存取功能無法從網路中移除。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**\_ \_ \_ 在 \_ 仲裁上發生錯誤的作業無效**
</dt> <dd> <dl> <dt>

5068 (0x13CC) 
</dt> <dt>



這是仲裁資源，因此無法在叢集資源上執行此作業。 您可能不會讓仲裁資源離線，或修改其可能的擁有者清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_ \_ 不 \_ 允許錯誤相依性**
</dt> <dd> <dl> <dt>

5069 (0x13CD) 
</dt> <dt>



叢集仲裁資源不允許有任何相依性。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**錯誤 \_ 叢集 \_ 節點已 \_ 暫停**
</dt> <dd> <dl> <dt>

5070 (0x13CE) 
</dt> <dt>



叢集節點已暫停。


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**錯誤 \_ 節點 \_ 無法 \_ 裝載 \_ 資源**
</dt> <dd> <dl> <dt>

5071 (0x13CF) 
</dt> <dt>



叢集資源無法上線。 擁有者節點無法執行此資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**錯誤 \_ 叢集 \_ 節點 \_ 未 \_ 就緒**
</dt> <dd> <dl> <dt>

5072 (0x13D0) 
</dt> <dt>



叢集節點尚未準備好執行要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**關閉錯誤叢集 \_ \_ 節點 \_ \_**
</dt> <dd> <dl> <dt>

5073 (0x13D1) 
</dt> <dt>



叢集節點正在關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**錯誤 \_ 叢集 \_ 加入已 \_ 中止**
</dt> <dd> <dl> <dt>

5074 (0x13D2) 
</dt> <dt>



叢集聯結作業已中止。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**錯誤叢集的 \_ \_ 版本不相容 \_**
</dt> <dd> <dl> <dt>

5075 (0x13D3) 
</dt> <dt>



叢集聯結作業失敗，因為加入的節點和其贊助者之間的軟體版本不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**已 \_ \_ \_ \_ 超過資源的 \_ 錯誤叢集 MAXNUM**
</dt> <dd> <dl> <dt>

5076 (0x13D4) 
</dt> <dt>



因為叢集已達可監視的資源數量限制，所以無法建立此資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**錯誤 \_ 叢集 \_ 系統 \_ 配置 \_ 已變更**
</dt> <dd> <dl> <dt>

5077 (0x13D5) 
</dt> <dt>



在叢集聯結或表單作業期間，系統組態已變更。 聯結或表單作業已中止。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤叢集資源類型**
</dt> <dd> <dl> <dt>

5078 (0x13D6) 
</dt> <dt>



找不到指定的資源類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**\_ \_ \_ 不 \_ 支援的錯誤叢集 AZUREMMBLOBCONTAINER.RESTYPE**
</dt> <dd> <dl> <dt>

5079 (0x13D7) 
</dt> <dt>



指定的節點不支援此類型的資源。 這可能是因為版本不一致或此節點上沒有資源 DLL。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 RESNAME**
</dt> <dd> <dl> <dt>

5080 (0x13D8) 
</dt> <dt>



此資源 DLL 不支援指定的資源名稱。 這可能是因為提供給資源 DLL 的錯誤 (或變更) 名稱所致。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**錯誤 \_ 叢集 \_ 未 \_ 註冊任何 RPC \_ 套件 \_**
</dt> <dd> <dl> <dt>

5081 (0x13D9) 
</dt> <dt>



無法向 RPC 伺服器註冊任何驗證套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**錯誤 \_ 叢集 \_ 擁有者 \_ 不 \_ 在 \_ PREFLIST 中**
</dt> <dd> <dl> <dt>

5082 (0x13DA) 
</dt> <dt>



因為群組的擁有者不在群組的慣用清單中，所以無法讓群組上線。 若要變更群組的擁有者節點，請移動群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ SEQMISMATCH**
</dt> <dd> <dl> <dt>

5083 (0x13DB) 
</dt> <dt>



聯結作業失敗，因為叢集資料庫序號已變更或與保險箱節點不相容。 如果叢集資料庫在聯結期間有所變更，則可能會在聯結作業期間發生此問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**\_RESMON \_ 無效 \_ 狀態時發生錯誤**
</dt> <dd> <dl> <dt>

5084 (0x13DC) 
</dt> <dt>



當資源處於目前狀態時，資源監視器將不允許執行失敗作業。 如果資源處於暫止狀態，就可能發生這種情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**錯誤 \_ 叢集 \_ 黏 \_ 非 \_ 保險箱**
</dt> <dd> <dl> <dt>

5085 (0x13DD) 
</dt> <dt>



非保險箱程式碼會要求保留鎖定以進行全域更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_ \_ \_ \_ 找不到錯誤仲裁磁碟**
</dt> <dd> <dl> <dt>

5086 (0x13DE) 
</dt> <dt>



叢集服務找不到仲裁磁碟。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**錯誤 \_ 資料庫 \_ 備份 \_ 已損毀**
</dt> <dd> <dl> <dt>

5087 (0x13DF) 
</dt> <dt>



備份的叢集資料庫可能已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**錯誤 \_ 叢集 \_ 節點 \_ 已經 \_ 有 \_ DFS \_ 根目錄**
</dt> <dd> <dl> <dt>

5088 (0x13E0) 
</dt> <dt>



DFS 根目錄已經存在於此叢集節點中。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**錯誤 \_ 資源 \_ 屬性無法變更 \_**
</dt> <dd> <dl> <dt>

5089 (0x13E1) 
</dt> <dt>



嘗試修改資源屬性失敗，因為它與另一個現有的屬性衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**錯誤 \_ 叢集 \_ 成員資格的 \_ \_ 狀態無效**
</dt> <dd> <dl> <dt>

5890 (0x1702) 
</dt> <dt>



嘗試的操作與節點目前的成員資格狀態不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**\_ \_ \_ \_ 找不到錯誤群集 QUORUMLOG**
</dt> <dd> <dl> <dt>

5891 (0x1703) 
</dt> <dt>



仲裁資源不包含仲裁記錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**錯誤 \_ 叢集 \_ 成員資格 \_ 終止**
</dt> <dd> <dl> <dt>

5892 (0x1704) 
</dt> <dt>



成員資格引擎要求關閉此節點上的叢集服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**錯誤 \_ 叢集 \_ 實例 \_ 識別碼 \_ 不符**
</dt> <dd> <dl> <dt>

5893 (0x1705) 
</dt> <dt>



聯結作業失敗，因為聯結節點的叢集實例識別碼與贊助商節點的叢集實例識別碼不相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**\_ \_ \_ \_ 找不到 \_ \_ IP 的錯誤叢集網路**
</dt> <dd> <dl> <dt>

5894 (0x1706) 
</dt> <dt>



找不到指定 IP 位址的相符叢集網路。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**錯誤 \_ 群集 \_ 屬性 \_ 資料 \_ 類型 \_ 不相符**
</dt> <dd> <dl> <dt>

5895 (0x1707) 
</dt> <dt>



屬性的實際資料類型不符合屬性的預期資料類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**錯誤叢集在 \_ \_ \_ 沒有清除的情況下收回 \_**
</dt> <dd> <dl> <dt>

5896 (0x1708) 
</dt> <dt>



已成功從叢集收回叢集節點，但節點未清除。 若要判斷哪些清除步驟失敗以及如何復原，請參閱使用事件檢視器的容錯移轉叢集應用程式事件記錄檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**錯誤 \_ 叢集 \_ 參數 \_ 不相符**
</dt> <dd> <dl> <dt>

5897 (0x1709) 
</dt> <dt>



針對資源的屬性所指定的兩個或多個參數值發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**無法叢集化錯誤 \_ 節點 \_ \_ \_**
</dt> <dd> <dl> <dt>

5898 (0x170A) 
</dt> <dt>



這部電腦不能成為叢集的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**錯誤叢集錯誤的 \_ \_ \_ 作業系統 \_ 版本**
</dt> <dd> <dl> <dt>

5899 (0x170B) 
</dt> <dt>



因為這部電腦未安裝正確的 Windows 版本，所以無法成為叢集的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**錯誤叢集無法 \_ \_ \_ 建立 \_ DUP \_ 叢集 \_ 名稱**
</dt> <dd> <dl> <dt>

5900 (0x170C) 
</dt> <dt>



因為叢集名稱已在使用中，所以無法使用指定的叢集名稱來建立叢集。 為叢集指定不同的名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**\_CLUSCFG \_ 已 \_ 認可的錯誤**
</dt> <dd> <dl> <dt>

5901 (0x170D) 
</dt> <dt>



已認可叢集設定動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**錯誤 \_ CLUSCFG \_ 復原 \_ 失敗**
</dt> <dd> <dl> <dt>

5902 (0x170E) 
</dt> <dt>



叢集設定動作無法復原。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**\_CLUSCFG \_ 系統 \_ 磁片 \_ 磁碟機 \_ 號 \_ 衝突時發生錯誤**
</dt> <dd> <dl> <dt>

5903 (0x170F) 
</dt> <dt>



指派給一個節點上之系統磁片的磁碟機號，與指派給另一個節點上的磁片的磁碟機號衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**錯誤 \_ 叢集 \_ 舊 \_ 版本**
</dt> <dd> <dl> <dt>

5904 (0x1710) 
</dt> <dt>



叢集中有一或多個節點正在執行的 Windows 版本不支援此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**錯誤叢集不相符的 \_ \_ \_ 電腦 \_ 帳戶 \_ 名稱**
</dt> <dd> <dl> <dt>

5905 (0x1711) 
</dt> <dt>



對應的電腦帳戶名稱與此資源的網路名稱不相符。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**錯誤 \_ 叢集 \_ 沒有 \_ 網路 \_ 配接器**
</dt> <dd> <dl> <dt>

5906 (0x1712) 
</dt> <dt>



沒有任何可用的網路介面卡。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**錯誤 \_ 叢集 \_ 有害**
</dt> <dd> <dl> <dt>

5907 (0x1713) 
</dt> <dt>



已有害叢集節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**錯誤 \_ 群集 \_ 群組 \_ 移動**
</dt> <dd> <dl> <dt>

5908 (0x1714) 
</dt> <dt>



群組無法接受要求，因為它正在移至另一個節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**錯誤 \_ 叢集 \_ 資源 \_ 類型 \_ 忙碌中**
</dt> <dd> <dl> <dt>

5909 (0x1715) 
</dt> <dt>



資源類型無法接受要求，因為太忙碌，無法執行另一個作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**錯誤 \_ 資源 \_ 呼叫 \_ 超時 \_**
</dt> <dd> <dl> <dt>

5910 (0x1716) 
</dt> <dt>



叢集資源 DLL 的呼叫已超時。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**\_不正確 \_ 叢集 \_ IPV6 \_ 位址錯誤**
</dt> <dd> <dl> <dt>

5911 (0x1717) 
</dt> <dt>



位址對 IPv6 位址資源而言是不正確。 需要全域 IPv6 位址，且必須符合叢集網路。 不允許相容性位址。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**錯誤 \_ 叢集 \_ 內部 \_ 無效 \_ 函數**
</dt> <dd> <dl> <dt>

5912 (0x1718) 
</dt> <dt>



發生內部叢集錯誤。 嘗試呼叫不正確函式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**錯誤 \_ 叢集 \_ 參數 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

5913 (0x1719) 
</dt> <dt>



參數值超出可接受的範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**錯誤 \_ 群集 \_ 部分 \_ 傳送**
</dt> <dd> <dl> <dt>

5914 (0x171A) 
</dt> <dt>



將資料傳送至叢集中的另一個節點時發生網路錯誤。 傳送的位元組數目小於所需的數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**錯誤叢集登錄 \_ \_ \_ 無效 \_ 函數**
</dt> <dd> <dl> <dt>

5915 (0x171B) 
</dt> <dt>



嘗試的叢集登錄操作無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**錯誤 \_ 群集 \_ 不正確 \_ 字串 \_ 終止**
</dt> <dd> <dl> <dt>

5916 (0x171C) 
</dt> <dt>



未正確地結束字元的輸入字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**錯誤 \_ 群集 \_ 不正確 \_ 字串 \_ 格式**
</dt> <dd> <dl> <dt>

5917 (0x171D) 
</dt> <dt>



字元的輸入字串不是其所代表之資料的有效格式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ 交易 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5918 (0x171E) 
</dt> <dt>



發生內部叢集錯誤。 交易正在進行時，嘗試了叢集資料庫交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**錯誤 \_ 叢集 \_ 資料庫 \_ 交易 \_ 未 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5919 (0x171F) 
</dt> <dt>



發生內部叢集錯誤。 未進行交易時，嘗試認可叢集資料庫交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**錯誤 \_ 叢集 \_ Null \_ 資料**
</dt> <dd> <dl> <dt>

5920 (0x1720) 
</dt> <dt>



發生內部叢集錯誤。 資料未正確初始化。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**錯誤 \_ 群集 \_ 部分 \_ 讀取**
</dt> <dd> <dl> <dt>

5921 (0x1721) 
</dt> <dt>



從資料流程讀取時發生錯誤。 傳回非預期的位元組數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**錯誤 \_ 群集 \_ 部分 \_ 寫入**
</dt> <dd> <dl> <dt>

5922 (0x1722) 
</dt> <dt>



寫入資料流程時發生錯誤。 無法寫入所需的位元組數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**錯誤叢集無法還原序列化 \_ \_ \_ \_ 資料**
</dt> <dd> <dl> <dt>

5923 (0x1723) 
</dt> <dt>



還原序列化叢集資料的資料流程時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**錯誤 \_ 相依的 \_ 資源 \_ 屬性 \_ 衝突**
</dt> <dd> <dl> <dt>

5924 (0x1724) 
</dt> <dt>



此資源的一或多個屬性值與其相依資源 (s) 相關聯的一或多個屬性值發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**錯誤 \_ 叢集 \_ 無 \_ 仲裁**
</dt> <dd> <dl> <dt>

5925 (0x1725) 
</dt> <dt>



叢集節點的仲裁不存在以形成叢集。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ IPV6 \_ 網路**
</dt> <dd> <dl> <dt>

5926 (0x1726) 
</dt> <dt>



叢集網路對 IPv6 位址資源無效，或不符合設定的位址。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**錯誤 \_ 群集 \_ 不正確 \_ IPV6 通道 \_ \_ 網路**
</dt> <dd> <dl> <dt>

5927 (0x1727) 
</dt> <dt>



叢集網路對 IPv6 通道資源而言是不正確。 檢查 IPv6 通道資源相依的 IP 位址資源設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_ \_ \_ \_ \_ 此 \_ 群組中不允許有錯誤仲裁**
</dt> <dd> <dl> <dt>

5928 (0x1728) 
</dt> <dt>



仲裁資源不能位於可用的儲存群組中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**錯誤相依性 \_ \_ 樹狀結構 \_ 太 \_ 複雜**
</dt> <dd> <dl> <dt>

5929 (0x1729) 
</dt> <dt>



這項資源的相依性太深。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_ \_ \_ 資源 \_ 呼叫中發生錯誤例外狀況**
</dt> <dd> <dl> <dt>

5930 (0x172A) 
</dt> <dt>



呼叫資源 DLL 產生未處理的例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**錯誤 \_ 叢集 \_ RHS \_ 無法 \_ 初始化**
</dt> <dd> <dl> <dt>

5931 (0x172B) 
</dt> <dt>



RHS 進程無法初始化。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**\_ \_ 未 \_ 安裝錯誤叢集**
</dt> <dd> <dl> <dt>

5932 (0x172C) 
</dt> <dt>



此節點上未安裝容錯移轉叢集功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ \_ \_ \_ \_ \_ \_ 相同節點上的 \_ 錯誤叢集資源必須在線上**
</dt> <dd> <dl> <dt>

5933 (0x172D) 
</dt> <dt>



此作業的資源必須在相同的節點上上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**叢集中的錯誤叢集 \_ \_ 節點數上限 \_ \_ \_**
</dt> <dd> <dl> <dt>

5934 (0x172E) 
</dt> <dt>



無法加入新節點，因為此叢集已經是節點的最大數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**錯誤 \_ 群集 \_ 太 \_ 多 \_ 節點**
</dt> <dd> <dl> <dt>

5935 (0x172F) 
</dt> <dt>



因為指定的節點數目超過允許的上限，所以無法建立此叢集。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**錯誤 \_ 叢集 \_ 物件 \_ 已 \_ 在使用中**
</dt> <dd> <dl> <dt>

5936 (0x1730) 
</dt> <dt>



嘗試使用指定的叢集名稱失敗，因為網域中已有啟用的電腦物件具有指定的名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**\_找到 NONCORE 的 \_ 群組 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

5937 (0x1731) 
</dt> <dt>



此叢集無法終結。 它具有非核心的應用程式群組，必須先刪除才能終結叢集。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**錯誤 \_ 檔案 \_ 共用 \_ 資源 \_ 衝突**
</dt> <dd> <dl> <dt>

5938 (0x1732) 
</dt> <dt>



與檔案共用見證資源相關聯的檔案共用無法由此叢集或其任何節點裝載。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**錯誤 \_ 叢集 \_ 收回 \_ 不正確 \_ 要求**
</dt> <dd> <dl> <dt>

5939 (0x1733) 
</dt> <dt>



此節點的收回目前無效。 由於仲裁需求節點收回會導致叢集關閉。 如果是叢集中的最後一個節點，則應該使用終結叢集命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**錯誤 \_ 叢集 \_ 單一 \_ 資源**
</dt> <dd> <dl> <dt>

5940 (0x1734) 
</dt> <dt>



叢集中只允許此資源類型的一個實例。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**錯誤 \_ 叢集 \_ 群組 \_ 單一 \_ 資源**
</dt> <dd> <dl> <dt>

5941 (0x1735) 
</dt> <dt>



每個資源群組只允許此資源類型的一個實例。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**錯誤 \_ 叢集 \_ 資源 \_ 提供者 \_ 失敗**
</dt> <dd> <dl> <dt>

5942 (0x1736) 
</dt> <dt>



因為一或多個提供者資源失敗，所以資源無法上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**錯誤 \_ 叢集 \_ 資源 \_ 設定 \_ 錯誤**
</dt> <dd> <dl> <dt>

5943 (0x1737) 
</dt> <dt>



資源表示它無法在任何節點上上線。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**錯誤 \_ 叢集 \_ 群組 \_ 忙碌中**
</dt> <dd> <dl> <dt>

5944 (0x1738) 
</dt> <dt>



目前無法在此群組上執行目前的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**錯誤 \_ 叢集 \_ 非 \_ 共用 \_ 磁片區**
</dt> <dd> <dl> <dt>

5945 (0x1739) 
</dt> <dt>



目錄或檔案不在叢集共用磁片區上。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**錯誤 \_ 群集 \_ 不正確 \_ 安全 \_ 描述項**
</dt> <dd> <dl> <dt>

5946 (0x173A) 
</dt> <dt>



安全描述項不符合叢集的需求。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ \_ \_ 使用中的錯誤叢集共用磁片區 \_**
</dt> <dd> <dl> <dt>

5947 (0x173B) 
</dt> <dt>



叢集中已設定一或多個共用磁片區資源。 這些資源必須移至可用的儲存體，作業才會成功。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**錯誤 \_ 叢集 \_ 使用 \_ 共用 \_ 磁片區 \_ API**
</dt> <dd> <dl> <dt>

5948 (0x173C) 
</dt> <dt>



無法直接操作此群組或資源。 使用共用磁片區 Api 來執行所需的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**錯誤 \_ 叢集 \_ 備份 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5949 (0x173D) 
</dt> <dt>



備份正在進行中。 請等候備份完成，然後再次嘗試此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**錯誤 \_ 非 \_ CSV \_ 路徑**
</dt> <dd> <dl> <dt>

5950 (0x173E) 
</dt> <dt>



路徑不屬於叢集共用磁片區。


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**錯誤 \_ CSV \_ 磁片區 \_ 不在 \_ 本機**
</dt> <dd> <dl> <dt>

5951 (0x173F) 
</dt> <dt>



叢集共用磁片區未在本機掛接在此節點上。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**錯誤 \_ 叢集 \_ 監視程式 \_ 終止**
</dt> <dd> <dl> <dt>

5952 (0x1740) 
</dt> <dt>



叢集監視程式即將終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**錯誤 \_ 叢集 \_ 資源被 \_ 否決 \_ 移動 \_ 不相容的 \_ 節點**
</dt> <dd> <dl> <dt>

5953 (0x1741) 
</dt> <dt>



因為資源不相容，所以已拒絕在兩個節點之間移動。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**錯誤 \_ 叢集 \_ \_ 節點 \_ 權數無效**
</dt> <dd> <dl> <dt>

5954 (0x1742) 
</dt> <dt>



要求無效，因為當叢集處於僅限磁碟仲裁模式時，無法變更節點權數，或因為變更節點權數會違反最低叢集仲裁需求。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**錯誤 \_ 叢集 \_ 資源被 \_ 否決 \_ 呼叫**
</dt> <dd> <dl> <dt>

5955 (0x1743) 
</dt> <dt>



資源拒絕呼叫。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**\_RESMON \_ 缺少系統 \_ 資源 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

5956 (0x1744) 
</dt> <dt>



資源無法啟動或執行，因為無法保留足夠的系統資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**錯誤 \_ 叢集 \_ 資源 \_ 被 \_ 否決 \_ 移動 \_ \_ \_ 到目的地的資源不足 \_**
</dt> <dd> <dl> <dt>

5957 (0x1745) 
</dt> <dt>



資源拒絕在兩個節點之間移動，因為目的地目前沒有足夠的資源可完成此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**錯誤 \_ 叢集 \_ 資源 \_ 被 \_ 否決 \_ 的資源無法移至 \_ \_ \_ 來源上的資源不足 \_**
</dt> <dd> <dl> <dt>

5958 (0x1746) 
</dt> <dt>



資源拒絕在兩個節點之間移動，因為來源目前沒有足夠的資源可完成此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**錯誤 \_ 叢集 \_ 群組已 \_ 排入佇列**
</dt> <dd> <dl> <dt>

5959 (0x1747) 
</dt> <dt>



無法完成要求的作業，因為群組已排入作業佇列中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**錯誤 \_ 叢集 \_ 資源 \_ 鎖定 \_ 狀態**
</dt> <dd> <dl> <dt>

5960 (0x1748) 
</dt> <dt>



因為資源已鎖定狀態，所以無法完成要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**\_ \_ 不允許錯誤叢集共用磁片區的 \_ \_ 容錯移轉 \_ \_**
</dt> <dd> <dl> <dt>

5961 (0x1749) 
</dt> <dt>



資源無法移至另一個節點，因為叢集共用磁片區已拒絕此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**錯誤 \_ 叢集 \_ 節點 \_ 清空 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

5962 (0x174A) 
</dt> <dt>



節點清空已在進行中。

此值也稱為 **錯誤叢集 \_ \_ 節點撤離 \_ 正在 \_ \_ 進行中**


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**錯誤 \_ 叢集 \_ 磁片 \_ 未 \_ 連線**
</dt> <dd> <dl> <dt>

5963 (0x174B) 
</dt> <dt>



叢集儲存體未連接到節點。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**錯誤 \_ 磁片 \_ 無法 \_ \_ 支援 CSV**
</dt> <dd> <dl> <dt>

5964 (0x174C) 
</dt> <dt>



磁片未設定成搭配 CSV 使用。 CSV 磁片至少必須有一個以 NTFS 格式化的磁碟分割。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**錯誤 \_ 資源 \_ 不 \_ 在 \_ 可用的 \_ 儲存體中**
</dt> <dd> <dl> <dt>

5965 (0x174D) 
</dt> <dt>



資源必須是可用儲存群組的一部分，才能完成此動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**錯誤 \_ 叢集 \_ 共用 \_ 磁片區重新 \_ 導向**
</dt> <dd> <dl> <dt>

5966 (0x174E) 
</dt> <dt>



因為磁片區處於重新導向模式，所以 CSVFS 失敗的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**錯誤 \_ 叢集 \_ 共用 \_ 磁片區 \_ 未重新 \_ 導向**
</dt> <dd> <dl> <dt>

5967 (0x174F) 
</dt> <dt>



CSVFS 失敗的作業，因為磁片區不在重新導向模式中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**錯誤 \_ 叢集 \_ 無法 \_ 傳回 \_ 屬性**
</dt> <dd> <dl> <dt>

5968 (0x1750) 
</dt> <dt>



目前無法傳回叢集屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**錯誤 \_ 叢集 \_ 資源 \_ 包含 \_ \_ \_ \_ \_ 共用 \_ 磁片區不支援的 DIFF 區域**
</dt> <dd> <dl> <dt>

5969 (0x1751) 
</dt> <dt>



叢集磁片資源包含不支援叢集共用磁片區的軟體快照差異區域。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**錯誤 \_ 叢集 \_ 資源 \_ 處於 \_ \_ 維護 \_ 模式**
</dt> <dd> <dl> <dt>

5970 (0x1752) 
</dt> <dt>



無法完成操作，因為資源處於維護模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**錯誤 \_ 叢集 \_ 親和性 \_ 衝突**
</dt> <dd> <dl> <dt>

5971 (0x1753) 
</dt> <dt>



因為叢集親和性衝突，所以無法完成操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**錯誤 \_ 叢集 \_ 資源 \_ 是 \_ 複本 \_ 虛擬 \_ 機**
</dt> <dd> <dl> <dt>

5972 (0x1754) 
</dt> <dt>



因為資源是複本虛擬機器，所以無法完成操作。


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

 

 




