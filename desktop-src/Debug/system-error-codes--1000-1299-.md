---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1000-1299，適用于開發人員。
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: '系統錯誤碼 (1000-1299)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: dfda2e29a6b75acd683842509229f3bc52d7e8d3599855b01d8376f5a7daf2ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076332"
---
# <a name="system-error-codes-1000-1299"></a>系統錯誤碼 (1000-1299) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[[錯誤碼](system-error-codes.md)] 頁面上有資源清單。

下列清單描述錯誤1000到1299的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**錯誤 \_ 堆疊 \_ 溢位**
</dt> <dd> <dl> <dt>

1001 (0x3E9) 
</dt> <dt>



遞迴太深;堆疊溢位。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**錯誤 \_ 不正確 \_ 訊息**
</dt> <dd> <dl> <dt>

1002 (0x3EA) 
</dt> <dt>



視窗無法對傳送的訊息採取動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**錯誤 \_ \_ 無法 \_ 完成**
</dt> <dd> <dl> <dt>

1003 (0x3EB) 
</dt> <dt>



無法完成此函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**錯誤 \_ 不正確 \_ 旗標**
</dt> <dd> <dl> <dt>

1004 (0x3EC) 
</dt> <dt>



不正確旗標。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**\_無法辨識的磁片區錯誤 \_**
</dt> <dd> <dl> <dt>

1005 (0x3ED) 
</dt> <dt>



磁片區未包含已辨識的檔案系統。 請確定已載入所有必要的檔案系統驅動程式，且磁片區未損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**錯誤 \_ 檔案 \_ 無效**
</dt> <dd> <dl> <dt>

1006 (0x3EE) 
</dt> <dt>



檔案的磁片區已從外部改變，因此開啟的檔案已不再有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**錯誤 \_ 全螢幕 \_ 模式**
</dt> <dd> <dl> <dt>

1007 (0x3EF) 
</dt> <dt>



要求的作業無法以全螢幕模式執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**錯誤 \_ 無 \_ 標記**
</dt> <dd> <dl> <dt>

1008 (0x3F0) 
</dt> <dt>



嘗試參考不存在的權杖。


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**錯誤 \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1) 
</dt> <dt>



Configuration registry 資料庫已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**錯誤 \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2) 
</dt> <dt>



設定登錄機碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**錯誤 \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3) 
</dt> <dt>



無法開啟設定登錄機碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**錯誤 \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4) 
</dt> <dt>



無法讀取設定登錄機碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**錯誤 \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5) 
</dt> <dt>



無法寫入設定登錄機碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**復原錯誤登錄 \_ \_**
</dt> <dd> <dl> <dt>

1014 (0x3F6) 
</dt> <dt>



您必須使用記錄檔或替代複本來復原登錄資料庫中的其中一個檔案。 復原成功。


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**錯誤登錄已損毀 \_ \_**
</dt> <dd> <dl> <dt>

1015 (0x3F7) 
</dt> <dt>



登錄已損毀。 其中一個包含登錄資料的檔案的結構已損毀，或檔案的系統記憶體映射已損毀，或因為替代複製或記錄檔不存在或損毀，所以無法復原檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**登錄 \_ \_ IO \_ 失敗錯誤**
</dt> <dd> <dl> <dt>

1016 (0x3F8) 
</dt> <dt>



登錄 unrecoverably 所起始的 i/o 作業失敗。 登錄無法讀取或寫出或清除其中一個檔案，其中包含系統的登錄映射。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**錯誤，不是登錄檔 \_ \_ \_**
</dt> <dd> <dl> <dt>

1017 (0x3F9) 
</dt> <dt>



系統已嘗試將檔案載入或還原到登錄中，但指定的檔案不是登錄檔案格式。


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**\_ \_ 已刪除錯誤索引鍵**
</dt> <dd> <dl> <dt>

1018 (0x3FA) 
</dt> <dt>



在已標示為要刪除的登錄機碼上嘗試了不合法的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**錯誤 \_ 無 \_ 記錄檔 \_ 空間**
</dt> <dd> <dl> <dt>

1019 (0x3FB) 
</dt> <dt>



系統無法在登錄記錄檔中配置所需的空間。


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**錯誤索引 \_ 鍵 \_ 具有 \_ 子系**
</dt> <dd> <dl> <dt>

1020 (0x3FC) 
</dt> <dt>



無法在已有子機碼或值的登錄機碼中建立符號連結。


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**錯誤 \_ 子 \_ 必須 \_ 為 \_ VOLATILE**
</dt> <dd> <dl> <dt>

1021 (0x3FD) 
</dt> <dt>



無法在 volatile 父機碼下建立穩定的子機碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**\_通知 \_ 列舉 \_ 目錄時發生錯誤**
</dt> <dd> <dl> <dt>

1022 (0x3FE) 
</dt> <dt>



正在完成通知變更要求，且未在呼叫端的緩衝區中傳回信息。 呼叫端現在必須列舉檔案以找出變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**錯誤 \_ 相依的 \_ 服務執行 \_ 中**
</dt> <dd> <dl> <dt>

1051 (0x41B) 
</dt> <dt>



停止控制項已傳送至其他正在執行之服務所相依的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**錯誤 \_ 不正確 \_ 服務 \_ 控制**
</dt> <dd> <dl> <dt>

1052 (0x41C) 
</dt> <dt>



要求的控制項對此服務無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**錯誤 \_ 服務 \_ 要求 \_ 超時**
</dt> <dd> <dl> <dt>

1053 (0x41D) 
</dt> <dt>



服務未即時回應啟動或控制要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**錯誤 \_ 服務 \_ 無 \_ 執行緒**
</dt> <dd> <dl> <dt>

1054 (0x41E) 
</dt> <dt>



無法為服務建立執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**錯誤 \_ 服務 \_ 資料庫已 \_ 鎖定**
</dt> <dd> <dl> <dt>

1055 (0x41F) 
</dt> <dt>



服務資料庫已鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**錯誤 \_ 服務 \_ 已在執行 \_**
</dt> <dd> <dl> <dt>

1056 (0x420) 
</dt> <dt>



服務的實例已在執行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**錯誤 \_ 不正確 \_ 服務 \_ 帳戶**
</dt> <dd> <dl> <dt>

1057 (0x421) 
</dt> <dt>



帳戶名稱無效或不存在，或密碼對指定的帳號名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**錯誤 \_ 服務 \_ 已停用**
</dt> <dd> <dl> <dt>

1058 (0x422) 
</dt> <dt>



無法啟動服務，原因可能是服務已停用，或服務沒有已啟用的裝置與其相關聯。


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**錯誤 \_ 迴圈相依性 \_**
</dt> <dd> <dl> <dt>

1059 (0x423) 
</dt> <dt>



已指定迴圈服務相依性。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**錯誤 \_ 服務 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

1060 (0x424) 
</dt> <dt>



指定的服務不是以已安裝的服務形式存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**錯誤 \_ 服務 \_ 無法 \_ 接受 \_ CTRL**
</dt> <dd> <dl> <dt>

1061 (0x425) 
</dt> <dt>



這次服務無法接受控制訊息。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**錯誤 \_ 服務 \_ 未 \_ 啟用**
</dt> <dd> <dl> <dt>

1062 (0x426) 
</dt> <dt>



尚未啟動服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**錯誤 \_ 失敗的 \_ SERVICE \_ CONTROLLER \_ CONNECT**
</dt> <dd> <dl> <dt>

1063 (0x427) 
</dt> <dt>



服務處理常式無法連接到服務控制器。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**服務發生錯誤 \_ 例外狀況 \_ \_**
</dt> <dd> <dl> <dt>

1064 (0x428) 
</dt> <dt>



處理控制項要求時，在服務中發生例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**錯誤 \_ 資料庫 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

1065 (0x429) 
</dt> <dt>



指定的資料庫不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**錯誤 \_ 服務 \_ 特定 \_ 錯誤**
</dt> <dd> <dl> <dt>

1066 (0x42A) 
</dt> <dt>



服務傳回服務特定的錯誤碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**錯誤 \_ 進程已 \_ 中止**
</dt> <dd> <dl> <dt>

1067 (0x42B) 
</dt> <dt>



進程意外結束。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**錯誤 \_ 服務相依性 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

1068 (0x42C) 
</dt> <dt>



相依性服務或群組無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**錯誤 \_ 服務 \_ 登入 \_ 失敗**
</dt> <dd> <dl> <dt>

1069 (0x42D) 
</dt> <dt>



登入失敗，因此服務無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**錯誤 \_ 服務 \_ 啟動停止 \_ 回應**
</dt> <dd> <dl> <dt>

1070 (0x42E) 
</dt> <dt>



啟動之後，服務會在啟動暫止狀態下無反應。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**錯誤 \_ 不正確 \_ 服務 \_ 鎖定**
</dt> <dd> <dl> <dt>

1071 (0x42F) 
</dt> <dt>



指定的服務資料庫鎖定無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_ \_ 標記 \_ 為刪除的錯誤服務 \_**
</dt> <dd> <dl> <dt>

1072 (0x430) 
</dt> <dt>



指定的服務已標示為要刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**錯誤 \_ 服務 \_ 存在**
</dt> <dd> <dl> <dt>

1073 (0x431) 
</dt> <dt>



指定的服務已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**錯誤 \_ 已在執行 \_ \_ LKG**
</dt> <dd> <dl> <dt>

1074 (0x432) 
</dt> <dt>



系統目前是以最後一個已知良好的設定來執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**錯誤 \_ 服務相依性 \_ \_ 已刪除**
</dt> <dd> <dl> <dt>

1075 (0x433) 
</dt> <dt>



相依性服務不存在或已標示為要刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**\_ \_ 已接受錯誤 \_ 開機**
</dt> <dd> <dl> <dt>

1076 (0x434) 
</dt> <dt>



目前的開機已被接受，可做為最後一個已知良好的控制集。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**錯誤 \_ 服務 \_ 從未 \_ 啟動**
</dt> <dd> <dl> <dt>

1077 (0x435) 
</dt> <dt>



自上次開機之後，不會嘗試啟動服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**\_ \_ 服務名稱重複 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

1078 (0x436) 
</dt> <dt>



名稱已用來作為服務名稱或服務顯示名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**錯誤 \_ 不同的 \_ 服務 \_ 帳戶**
</dt> <dd> <dl> <dt>

1079 (0x437) 
</dt> <dt>



針對此服務指定的帳號不同于在相同進程中執行的其他服務所指定的帳號。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**錯誤 \_ 無法 \_ 偵測 \_ 驅動程式 \_ 失敗**
</dt> <dd> <dl> <dt>

1080 (0x438) 
</dt> <dt>



失敗動作只能針對 Win32 服務設定，而不能針對驅動程式進行設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**錯誤 \_ 無法 \_ 偵測 \_ 進程 \_ 中止**
</dt> <dd> <dl> <dt>

1081 (0x439) 
</dt> <dt>



這項服務會在與服務控制管理員相同的進程中執行。 因此，如果此服務的進程非預期地終止，服務控制管理員就無法採取動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**錯誤 \_ 的 \_ 修復 \_ 程式**
</dt> <dd> <dl> <dt>

1082 (0x43A) 
</dt> <dt>



尚未針對此服務設定任何修復程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**錯誤 \_ 服務 \_ 不 \_ 在 \_ EXE 中**
</dt> <dd> <dl> <dt>

1083 (0x43B) 
</dt> <dt>



這項服務設定為在其中執行的可執行程式，不會執行服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**錯誤 \_ 未 \_ 安全開機 \_ 服務**
</dt> <dd> <dl> <dt>

1084 (0x43C) 
</dt> <dt>



這項服務無法在保管庫模式下啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_ \_ 媒體的錯誤 \_ 結束**
</dt> <dd> <dl> <dt>

1100 (0x44C) 
</dt> <dt>



已達到磁帶的實體結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**偵測到錯誤的標記 \_ \_**
</dt> <dd> <dl> <dt>

1101 (0x44D) 
</dt> <dt>



磁帶存取已達到標記。


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**\_媒體開始 \_ 時發生 \_ 錯誤**
</dt> <dd> <dl> <dt>

1102 (0x44E) 
</dt> <dt>



遇到磁帶或磁碟分割的開頭。


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**偵測 \_ 到錯誤 SETMARK \_**
</dt> <dd> <dl> <dt>

1103 (0x44F) 
</dt> <dt>



磁帶存取已達一組檔案的結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**\_未偵測 \_ 到任何資料時發生錯誤 \_**
</dt> <dd> <dl> <dt>

1104 (0x450) 
</dt> <dt>



磁帶上沒有其他資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**錯誤 \_ 分割區 \_ 失敗**
</dt> <dd> <dl> <dt>

1105 (0x451) 
</dt> <dt>



無法分割磁帶。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**錯誤 \_ 不正確 \_ 區塊 \_ 長度**
</dt> <dd> <dl> <dt>

1106 (0x452) 
</dt> <dt>



存取 multivolume 磁碟分割的新磁帶時，目前的區塊大小不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**錯誤 \_ 裝置 \_ 未 \_ 分割**
</dt> <dd> <dl> <dt>

1107 (0x453) 
</dt> <dt>



載入磁帶時，找不到磁帶磁碟分割資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**\_無法 \_ \_ 鎖定媒體的 \_ 錯誤**
</dt> <dd> <dl> <dt>

1108 (0x454) 
</dt> <dt>



無法鎖定媒體退出機制。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**\_無法卸載 \_ \_ 媒體的 \_ 錯誤**
</dt> <dd> <dl> <dt>

1109 (0x455) 
</dt> <dt>



無法卸載媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**錯誤 \_ 媒體 \_ 已變更**
</dt> <dd> <dl> <dt>

1110 (0x456) 
</dt> <dt>



磁片磁碟機中的媒體可能已變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**錯誤 \_ 匯流排 \_ 重設**
</dt> <dd> <dl> <dt>

1111 (0x457) 
</dt> <dt>



I/o 匯流排已重設。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**\_ \_ \_ 磁片磁碟機中沒有媒體的錯誤 \_**
</dt> <dd> <dl> <dt>

1112 (0x458) 
</dt> <dt>



磁片磁碟機中沒有任何媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**\_沒有 \_ UNICODE \_ 轉譯的錯誤**
</dt> <dd> <dl> <dt>

1113 (0x459) 
</dt> <dt>



目標多位元組字碼頁中不存在 Unicode 字元的對應。


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**錯誤 \_ DLL \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

1114 (0x45A) 
</dt> <dt>



動態連結程式庫 (DLL) 初始化常式失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**錯誤 \_ 關閉 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

1115 (0x45B) 
</dt> <dt>



系統關機正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**錯誤 \_ \_ ，無法 \_ \_ 進行關閉**
</dt> <dd> <dl> <dt>

1116 (0x45C) 
</dt> <dt>



無法中止系統關機，因為沒有正在進行的關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**錯誤 \_ IO \_ 裝置**
</dt> <dd> <dl> <dt>

1117 (0x45D) 
</dt> <dt>



因為 I/O 裝置錯誤，所以無法執行要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**錯誤 \_ 序列 \_ 無 \_ 裝置**
</dt> <dd> <dl> <dt>

1118 (0x45E) 
</dt> <dt>



未成功初始化任何序列裝置。 序列驅動程式將會卸載。


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**錯誤 \_ IRQ \_ 忙碌**
</dt> <dd> <dl> <dt>

1119 (0x45F) 
</dt> <dt>



無法開啟與其他裝置 (IRQ) 共用中斷要求的裝置。 至少有一個使用該 IRQ 的其他裝置已開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**\_寫入錯誤 \_**
</dt> <dd> <dl> <dt>

1120 (0x460) 
</dt> <dt>



序列 i/o 作業已由另一個寫入至序列埠來完成。 IOCTL \_ 序列 \_ XOFF 計數器已 \_ 達到零。 ) 


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**錯誤 \_ 計數器 \_ TIMEOUT**
</dt> <dd> <dl> <dt>

1121 (0x461) 
</dt> <dt>



序列 i/o 作業已完成，因為超時時間已過期。 IOCTL \_ 序列 \_ XOFF 計數器未 \_ 達到零。 ) 


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤的軟碟識別碼標記**
</dt> <dd> <dl> <dt>

1122 (0x462) 
</dt> <dt>



在磁片磁碟機上找不到任何識別碼位址標記。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**錯誤的磁片 \_ 磁碟機 \_ \_ 圖錯誤**
</dt> <dd> <dl> <dt>

1123 (0x463) 
</dt> <dt>



磁片磁區識別碼欄位與磁碟控制卡播放軌位址不符。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**錯誤 \_ 磁片 \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

1124 (0x464) 
</dt> <dt>



磁碟控制卡回報磁片磁碟機無法辨識的錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**錯誤的 \_ 軟碟登錄 \_ \_**
</dt> <dd> <dl> <dt>

1125 (0x465) 
</dt> <dt>



磁碟控制卡在其暫存器中傳回不一致的結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**錯誤 \_ 磁片重新 \_ 校準 \_ 失敗**
</dt> <dd> <dl> <dt>

1126 (0x466) 
</dt> <dt>



存取硬碟時，即使在重試之後，重新校準作業也會失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**錯誤 \_ 磁片 \_ 操作 \_ 失敗**
</dt> <dd> <dl> <dt>

1127 (0x467) 
</dt> <dt>



存取硬碟時，即使在重試之後，磁片作業也會失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**錯誤 \_ 磁片 \_ 重設 \_ 失敗**
</dt> <dd> <dl> <dt>

1128 (0x468) 
</dt> <dt>



存取硬碟時，需要重設磁碟控制卡，但即使失敗也是如此。


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**錯誤 \_ EOM \_ 溢位**
</dt> <dd> <dl> <dt>

1129 (0x469) 
</dt> <dt>



遇到磁帶的實體結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**錯誤 \_ 的 \_ \_ 伺服器 \_ 記憶體不足**
</dt> <dd> <dl> <dt>

1130 (0x46A) 
</dt> <dt>



沒有足夠的可用伺服器儲存空間來處理此命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**錯誤 \_ 可能的 \_ 鎖死**
</dt> <dd> <dl> <dt>

1131 (0x46B) 
</dt> <dt>



偵測到潛在的鎖死狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**錯誤 \_ 對應 \_ 對齊**
</dt> <dd> <dl> <dt>

1132 (0x46C) 
</dt> <dt>



基底位址或指定的檔案位移沒有適當的對齊方式。


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**\_設定 \_ 拒絕電源 \_ 狀態 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1140 (0x474) 
</dt> <dt>



嘗試變更系統電源狀態是由另一個應用程式或驅動程式所拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**錯誤 \_ 設定 \_ 電源 \_ 狀態 \_ 失敗**
</dt> <dd> <dl> <dt>

1141 (0x475) 
</dt> <dt>



系統 BIOS 無法嘗試變更系統電源狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**錯誤 \_ 太 \_ 多 \_ 連結**
</dt> <dd> <dl> <dt>

1142 (0x476) 
</dt> <dt>



嘗試在檔案系統所支援的檔案上建立更多連結。


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**\_舊的 \_ WIN \_ 版本錯誤**
</dt> <dd> <dl> <dt>

1150 (0x47E) 
</dt> <dt>



指定的程式需要較新版本的 Windows。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**錯誤 \_ 應用程式錯誤的 \_ \_ 作業系統**
</dt> <dd> <dl> <dt>

1151 (0x47F) 
</dt> <dt>



所指定的程式不是 Windows 或 MS-DOS 程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**\_單一 \_ 實例 \_ 應用程式錯誤**
</dt> <dd> <dl> <dt>

1152 (0x480) 
</dt> <dt>



無法啟動一個以上指定之程式的實例。


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**\_RMODE \_ 應用程式時發生錯誤**
</dt> <dd> <dl> <dt>

1153 (0x481) 
</dt> <dt>



指定的程式是針對舊版 Windows 所撰寫。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**錯誤 \_ 不正確 \_ DLL**
</dt> <dd> <dl> <dt>

1154 (0x482) 
</dt> <dt>



執行此應用程式所需的其中一個程式庫檔案已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**錯誤 \_ 沒有 \_ 關聯**
</dt> <dd> <dl> <dt>

1155 (0x483) 
</dt> <dt>



沒有任何應用程式與指定的檔案相關聯，無法進行這項操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**錯誤 \_ DDE \_ 失敗**
</dt> <dd> <dl> <dt>

1156 (0x484) 
</dt> <dt>



將命令傳送至應用程式時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_ \_ 找不到錯誤 DLL \_**
</dt> <dd> <dl> <dt>

1157 (0x485) 
</dt> <dt>



找不到執行此應用程式所需的程式庫檔案之一。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**\_沒有 \_ 其他 \_ 使用者 \_ 控制碼的錯誤**
</dt> <dd> <dl> <dt>

1158 (0x486) 
</dt> <dt>



目前的進程已使用其系統管理員物件的所有系統額度。


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ 僅限錯誤訊息同步 \_**
</dt> <dd> <dl> <dt>

1159 (0x487) 
</dt> <dt>



訊息只能與同步作業搭配使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**錯誤 \_ 來源 \_ 元素 \_ 空白**
</dt> <dd> <dl> <dt>

1160 (0x488) 
</dt> <dt>



指出的來源元素沒有任何媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**錯誤 \_ 目的地 \_ 元素已 \_ 滿**
</dt> <dd> <dl> <dt>

1161 (0x489) 
</dt> <dt>



指出的目的地元素已包含媒體。


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**錯誤 \_ 的 \_ 元素 \_ 位址無效**
</dt> <dd> <dl> <dt>

1162 (0x48A) 
</dt> <dt>



指出的元素不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**錯誤 \_ 雜誌 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

1163 (0x48B) 
</dt> <dt>



指出的專案是不存在之雜誌的一部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**\_需要重新 \_ 初始化錯誤裝置 \_**
</dt> <dd> <dl> <dt>

1164 (0x48C) 
</dt> <dt>



指出的裝置需要重新初始化，因為硬體發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**錯誤 \_ 裝置 \_ 需要 \_ 清除**
</dt> <dd> <dl> <dt>

1165 (0x48D) 
</dt> <dt>



裝置已指出需要先清除，再嘗試進行進一步的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**\_裝置 \_ 門 \_ 開啟時發生錯誤**
</dt> <dd> <dl> <dt>

1166 (0x48E) 
</dt> <dt>



裝置已指出其門已開啟。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**錯誤 \_ 裝置 \_ 未 \_ 連線**
</dt> <dd> <dl> <dt>

1167 (0x48F) 
</dt> <dt>



裝置未連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**\_找不 \_ 到錯誤**
</dt> <dd> <dl> <dt>

1168 (0x490) 
</dt> <dt>



Element not found.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**錯誤 \_ 無 \_ 相符**
</dt> <dd> <dl> <dt>

1169 (0x491) 
</dt> <dt>



索引中的指定索引鍵沒有相符的結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ 找不到錯誤集 \_**
</dt> <dd> <dl> <dt>

1170 (0x492) 
</dt> <dt>



指定的屬性集不存在物件上。


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_ \_ 找不到錯誤點 \_**
</dt> <dd> <dl> <dt>

1171 (0x493) 
</dt> <dt>



傳遞至 GetMouseMovePoints 的點不在緩衝區中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**錯誤 \_ 無 \_ 追蹤 \_ 服務**
</dt> <dd> <dl> <dt>

1172 (0x494) 
</dt> <dt>



追蹤 (工作站) 服務未執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**錯誤 \_ 的 \_ 磁片區 \_ 識別碼**
</dt> <dd> <dl> <dt>

1173 (0x495) 
</dt> <dt>



找不到磁片區識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**\_無法 \_ \_ 移除 \_ 已取代的錯誤**
</dt> <dd> <dl> <dt>

1175 (0x497) 
</dt> <dt>



無法移除要取代的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**錯誤 \_ 無法 \_ \_ 移動 \_ 取代**
</dt> <dd> <dl> <dt>

1176 (0x498) 
</dt> <dt>



無法將取代檔案移至要取代的檔案。 要取代的檔案已保留其原始名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**錯誤 \_ 無法 \_ \_ 移動 \_ 更換 \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499) 
</dt> <dt>



無法將取代檔案移至要取代的檔案。 要取代的檔案已使用備份名稱重新命名。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**錯誤 \_ 日誌 \_ 刪除 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

1178 (0x49A) 
</dt> <dt>



正在刪除磁片區變更日誌。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**錯誤 \_ 日誌 \_ 未 \_ 啟用**
</dt> <dd> <dl> <dt>

1179 (0x49B) 
</dt> <dt>



磁片區變更日誌未啟用。


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_發現可能 \_ 的檔案錯誤 \_**
</dt> <dd> <dl> <dt>

1180 (0x49C) 
</dt> <dt>



找到檔案，但它可能不是正確的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_ \_ 已刪除錯誤記錄項目 \_**
</dt> <dd> <dl> <dt>

1181 (0x49D) 
</dt> <dt>



記錄項目已從日誌中刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**\_ \_ 已排程錯誤 \_ 關閉**
</dt> <dd> <dl> <dt>

1190 (0x4A6) 
</dt> <dt>



已排程系統關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**\_關機 \_ 使用者 \_ 登入 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1191 (0x4A7) 
</dt> <dt>



因為有其他使用者登入電腦，所以無法起始系統關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**錯誤 \_ 錯誤 \_ 裝置**
</dt> <dd> <dl> <dt>

1200 (0x4B0) 
</dt> <dt>



指定的裝置名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**錯誤 \_ 連接 \_ UNAVAIL**
</dt> <dd> <dl> <dt>

1201 (0x4B1) 
</dt> <dt>



裝置目前未連線，但它是記住的連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**\_ \_ 已記住錯誤 \_ 裝置**
</dt> <dd> <dl> <dt>

1202 (0x4B2) 
</dt> <dt>



本機裝置名稱已記住與另一個網路資源的連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**錯誤 \_ 沒有 \_ 淨 \_ 或不 \_ 正確的 \_ 路徑**
</dt> <dd> <dl> <dt>

1203 (0x4B3) 
</dt> <dt>



網路路徑的輸入不正確、不存在，或網路提供者目前無法使用。 請嘗試重新鍵入路徑，或洽詢您的網路系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**錯誤 \_ 的 \_ 提供者錯誤**
</dt> <dd> <dl> <dt>

1204 (0x4B4) 
</dt> <dt>



指定的網路提供者名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**錯誤 \_ 無法 \_ 開啟 \_ 設定檔**
</dt> <dd> <dl> <dt>

1205 (0x4B5) 
</dt> <dt>



無法開啟網路連線設定檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**錯誤 \_ 的 \_ 設定檔錯誤**
</dt> <dd> <dl> <dt>

1206 (0x4B6) 
</dt> <dt>



網路連接設定檔已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**錯誤 \_ 不是 \_ 容器**
</dt> <dd> <dl> <dt>

1207 (0x4B7) 
</dt> <dt>



無法列舉非容器。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**錯誤 \_ 擴充 \_ 錯誤**
</dt> <dd> <dl> <dt>

1208 (0x4B8) 
</dt> <dt>



發生擴充錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**錯誤 \_ 不正確擁有 \_**
</dt> <dd> <dl> <dt>

1209 (0x4B9) 
</dt> <dt>



指定組名的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**錯誤 \_ 不正確 \_ COMPUTERNAME**
</dt> <dd> <dl> <dt>

1210 (0x4BA) 
</dt> <dt>



指定電腦名稱稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**錯誤 \_ 不正確 \_ 事件名稱**
</dt> <dd> <dl> <dt>

1211 (0x4BB) 
</dt> <dt>



指定之事件名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**錯誤 \_ 不正確 \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

1212 (0x4BC) 
</dt> <dt>



指定功能變數名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**錯誤 \_ 不正確 \_ SERVICENAME**
</dt> <dd> <dl> <dt>

1213 (0x4BD) 
</dt> <dt>



指定服務名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**錯誤 \_ 的 \_ 網路名稱無效**
</dt> <dd> <dl> <dt>

1214 (0x4BE) 
</dt> <dt>



指定之網路名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**錯誤 \_ 不正確 \_ 共用名稱**
</dt> <dd> <dl> <dt>

1215 (0x4BF) 
</dt> <dt>



指定之共用名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**錯誤 \_ 無效 \_ PASSWORDNAME**
</dt> <dd> <dl> <dt>

1216 (0x4C0) 
</dt> <dt>



指定之密碼的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**錯誤 \_ 無效 \_ MESSAGENAME**
</dt> <dd> <dl> <dt>

1217 (0x4C1) 
</dt> <dt>



指定之訊息名稱的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**錯誤 \_ 無效 \_ MESSAGEDEST**
</dt> <dd> <dl> <dt>

1218 (0x4C2) 
</dt> <dt>



指定之訊息目的地的格式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**錯誤 \_ 會話 \_ 認證 \_ 衝突**
</dt> <dd> <dl> <dt>

1219 (0x4C3) 
</dt> <dt>



不允許使用多個使用者名稱對伺服器或共用資源進行多個連接。 中斷伺服器或共用資源的所有先前連接，然後再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_超過遠端 \_ 會話 \_ 限制 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

1220 (0x4C4) 
</dt> <dt>



嘗試建立網路伺服器的會話，但已為該伺服器建立了太多會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**錯誤 \_ DUP \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

1221 (0x4C5) 
</dt> <dt>



網路上的另一部電腦已在使用工作組或功能變數名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**錯誤 \_ 的 \_ 網路**
</dt> <dd> <dl> <dt>

1222 (0x4C6) 
</dt> <dt>



網路不存在或未啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**錯誤已 \_ 取消**
</dt> <dd> <dl> <dt>

1223 (0x4C7) 
</dt> <dt>



使用者已取消作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_使用者 \_ 對應檔 \_ 錯誤**
</dt> <dd> <dl> <dt>

1224 (0x4C8) 
</dt> <dt>



在開啟使用者對應區段的檔案上，無法執行所要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**\_拒絕連接 \_ 錯誤**
</dt> <dd> <dl> <dt>

1225 (0x4C9) 
</dt> <dt>



遠端電腦拒絕網路連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**錯誤 \_ 正常 \_ 中斷連線**
</dt> <dd> <dl> <dt>

1226 (0x4CA) 
</dt> <dt>



網路連接已正常關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_ \_ 已 \_ 關聯的錯誤位址**
</dt> <dd> <dl> <dt>

1227 (0x4CB) 
</dt> <dt>



網路傳輸端點已經有與其相關聯的位址。


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**錯誤 \_ 位址 \_ 未 \_ 關聯**
</dt> <dd> <dl> <dt>

1228 (0x4CC) 
</dt> <dt>



尚未與網路端點相關聯的位址。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**\_連接 \_ 不正確錯誤**
</dt> <dd> <dl> <dt>

1229 (0x4CD) 
</dt> <dt>



嘗試在不存在的網路連接上進行作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**使用中的 \_ 連接錯誤 \_**
</dt> <dd> <dl> <dt>

1230 (0x4CE) 
</dt> <dt>



在使用中的網路連接上嘗試了不正確作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**無法連線到 \_ 網路錯誤 \_**
</dt> <dd> <dl> <dt>

1231 (0x4CF) 
</dt> <dt>



無法到達網路位置。 如需網路疑難排解的詳細資訊，請參閱 Windows 說明。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**錯誤 \_ 主機 \_ 無法連線**
</dt> <dd> <dl> <dt>

1232 (0x4D0) 
</dt> <dt>



無法到達網路位置。 如需網路疑難排解的詳細資訊，請參閱 Windows 說明。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**錯誤 \_ 通訊協定 \_ 無法連線**
</dt> <dd> <dl> <dt>

1233 (0x4D1) 
</dt> <dt>



無法到達網路位置。 如需網路疑難排解的詳細資訊，請參閱 Windows 說明。


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**錯誤 \_ 埠 \_ 無法連線**
</dt> <dd> <dl> <dt>

1234 (0x4D2) 
</dt> <dt>



遠端系統上的目的地網路端點沒有任何服務正在運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**錯誤 \_ 要求已 \_ 中止**
</dt> <dd> <dl> <dt>

1235 (0x4D3) 
</dt> <dt>



要求已中止。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**錯誤 \_ 連接已 \_ 中止**
</dt> <dd> <dl> <dt>

1236 (0x4D4) 
</dt> <dt>



本機系統已中止網路連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**錯誤 \_ 重試**
</dt> <dd> <dl> <dt>

1237 (0x4D5) 
</dt> <dt>



無法完成作業。 應執行重試。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_連接 \_ 計數 \_ 限制錯誤**
</dt> <dd> <dl> <dt>

1238 (0x4D6) 
</dt> <dt>



無法連接到伺服器，因為已達到此帳戶的並行連接數目限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**錯誤 \_ 登入 \_ 時間 \_ 限制**
</dt> <dd> <dl> <dt>

1239 (0x4D7) 
</dt> <dt>



在此帳戶的一天未授權時間內嘗試登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**錯誤 \_ 登入 \_ WKSTA \_ 限制**
</dt> <dd> <dl> <dt>

1240 (0x4D8) 
</dt> <dt>



帳戶未經授權，無法從此工作站登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**錯誤 \_ 的 \_ 位址不正確**
</dt> <dd> <dl> <dt>

1241 (0x4D9) 
</dt> <dt>



網路位址無法用於要求的操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**\_已 \_ 註冊錯誤**
</dt> <dd> <dl> <dt>

1242 (0x4DA) 
</dt> <dt>



服務已註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ 找不到錯誤服務 \_**
</dt> <dd> <dl> <dt>

1243 (0x4DB) 
</dt> <dt>



指定的服務不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**錯誤 \_ 未 \_ 通過驗證**
</dt> <dd> <dl> <dt>

1244 (0x4DC) 
</dt> <dt>



未執行所要求的作業，因為使用者尚未經過驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**錯誤 \_ 未 \_ 登入 \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD) 
</dt> <dt>



未執行所要求的作業，因為使用者尚未登入網路。 指定的服務不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**錯誤 \_ 繼續**
</dt> <dd> <dl> <dt>

1246 (0x4DE) 
</dt> <dt>



繼續進行中的工作。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**錯誤 \_ 已 \_ 初始化**
</dt> <dd> <dl> <dt>

1247 (0x4DF) 
</dt> <dt>



已嘗試在初始化完成時執行初始化作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**\_沒有 \_ 其他 \_ 裝置的錯誤**
</dt> <dd> <dl> <dt>

1248 (0x4E0) 
</dt> <dt>



沒有其他本機裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**錯誤 \_ 的 \_ \_ 網站錯誤**
</dt> <dd> <dl> <dt>

1249 (0x4E1) 
</dt> <dt>



指定的網站不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**\_域 \_ 控制器 \_ 存在錯誤**
</dt> <dd> <dl> <dt>

1250 (0x4E2) 
</dt> <dt>



具有指定名稱的網域控制站已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**\_只有 \_ 在 \_ 連接時才會發生錯誤**
</dt> <dd> <dl> <dt>

1251 (0x4E3) 
</dt> <dt>



只有當您連接到伺服器時，才支援這項作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**錯誤覆 \_ 寫 \_ NOCHANGES**
</dt> <dd> <dl> <dt>

1252 (0x4E4) 
</dt> <dt>



即使沒有任何變更，群組原則架構也應該呼叫延伸模組。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**錯誤 \_ 的 \_ 使用者 \_ 設定檔錯誤**
</dt> <dd> <dl> <dt>

1253 (0x4E5) 
</dt> <dt>



指定的使用者沒有有效的設定檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**\_SBS 不 \_ 支援 \_ 的 \_ 錯誤**
</dt> <dd> <dl> <dt>

1254 (0x4E6) 
</dt> <dt>



執行 Windows Server 2003 for Small Business Server 的電腦不支援這項操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**錯誤 \_ 伺服器 \_ 關閉 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

1255 (0x4E7) 
</dt> <dt>



伺服器電腦正在關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**錯誤 \_ 主機 \_ 關閉**
</dt> <dd> <dl> <dt>

1256 (0x4E8) 
</dt> <dt>



遠端系統無法使用。 如需網路疑難排解的詳細資訊，請參閱 Windows 說明。


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**錯誤 \_ 非 \_ 帳戶 \_ SID**
</dt> <dd> <dl> <dt>

1257 (0x4E9) 
</dt> <dt>



提供的安全識別碼並非來自帳戶網域。


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**錯誤 \_ 非 \_ 網域 \_ SID**
</dt> <dd> <dl> <dt>

1258 (0x4EA) 
</dt> <dt>



提供的安全識別碼沒有網域元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**\_APPHELP \_ 區塊時發生錯誤**
</dt> <dd> <dl> <dt>

1259 (0x4EB) 
</dt> <dt>



AppHelp 對話方塊已取消，因此無法啟動應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_ \_ 原則停用存取錯誤 \_ \_**
</dt> <dd> <dl> <dt>

1260 (0x4EC) 
</dt> <dt>



群組原則封鎖了此程式。 如需相關資訊，請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**錯誤的 \_ REG \_ NAT \_ 耗用量**
</dt> <dd> <dl> <dt>

1261 (0x4ED) 
</dt> <dt>



程式嘗試使用不正確註冊值。 通常是因為未初始化的登錄所造成。 此錯誤是 Itanium 特定的錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**\_離線 CSCSHARE 時發生錯誤 \_**
</dt> <dd> <dl> <dt>

1262 (0x4EE) 
</dt> <dt>



共用目前為離線或不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**錯誤 \_ PKINIT \_ 失敗**
</dt> <dd> <dl> <dt>

1263 (0x4EF) 
</dt> <dt>



Kerberos 通訊協定在智慧卡登入期間驗證 KDC 憑證時發生錯誤。 系統事件記錄檔中有更多的資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**錯誤的 \_ 智慧卡 \_ 子系統 \_ 失敗**
</dt> <dd> <dl> <dt>

1264 (0x4F0) 
</dt> <dt>



Kerberos 通訊協定嘗試利用智慧卡子系統時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**偵測 \_ 到錯誤降級 \_**
</dt> <dd> <dl> <dt>

1265 (0x4F1) 
</dt> <dt>



系統無法連絡網域控制站來服務驗證要求。 請稍後再試一次。


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**錯誤 \_ 電腦已 \_ 鎖定**
</dt> <dd> <dl> <dt>

1271 (0x4F7) 
</dt> <dt>



電腦已鎖定，無法在沒有強制選項的情況下關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**錯誤 \_ 回呼 \_ 提供 \_ 不正確 \_ 資料**
</dt> <dd> <dl> <dt>

1273 (0x4F9) 
</dt> <dt>



應用程式定義的回呼在呼叫時，會給予不正確資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_需要錯誤同步處理 \_ 前景重新 \_ 整理 \_**
</dt> <dd> <dl> <dt>

1274 (0x4FA) 
</dt> <dt>



群組原則架構應該在同步的前景原則重新整理中呼叫延伸模組。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**錯誤 \_ 驅動程式已 \_ 封鎖**
</dt> <dd> <dl> <dt>

1275 (0x4FB) 
</dt> <dt>



此驅動程式已被封鎖而無法載入。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**錯誤 \_ 無效 \_ 的匯入 \_ \_ 非 \_ DLL**
</dt> <dd> <dl> <dt>

1276 (0x4FC) 
</dt> <dt>



動態連結程式庫 (DLL) 參考的模組不是 DLL 也不是進程的可執行檔映射。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_存取 \_ 停用 \_ WEBBLADE 時發生錯誤**
</dt> <dd> <dl> <dt>

1277 (0x4FD) 
</dt> <dt>



Windows 無法開啟此程式，因為它已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**\_存取 \_ 停用的錯誤 \_ WEBBLADE \_ 篡改**
</dt> <dd> <dl> <dt>

1278 (0x4FE) 
</dt> <dt>



Windows 因為授權強制系統已遭篡改或損毀，所以無法開啟此程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**錯誤 \_ 復原 \_ 失敗**
</dt> <dd> <dl> <dt>

1279 (0x4FF) 
</dt> <dt>



交易復原失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**錯誤 \_ 已經是 \_ 光纖**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



目前的執行緒已轉換為光纖。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**錯誤 \_ 已經是 \_ 執行緒**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



目前的執行緒已經從光纖轉換。


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**錯誤 \_ 堆疊 \_ 緩衝區 \_ 溢出**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



系統在此應用程式中偵測到堆疊型緩衝區溢位。 此溢出可能會讓惡意使用者能夠掌控此應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**\_超過錯誤參數 \_ 配額 \_**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



其中一個參數中的資料比函式可操作的更多。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**錯誤 \_ 偵錯工具非使用中 \_**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



嘗試對 debug 物件進行作業失敗，因為物件正在刪除中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**錯誤 \_ 延遲 \_ 載入 \_ 失敗**
</dt> <dd> <dl> <dt>

1285 (0x505) 
</dt> <dt>



嘗試延遲載入 .dll，或在延遲載入的 .dll 中取得函數位址失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**不 \_ 允許錯誤的 VDM \_**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 是16位應用程式。 您沒有執行16位應用程式的許可權。 請向您的系統管理員確認您的許可權。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**錯誤 \_ 不明 \_ 錯誤**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



沒有足夠的資訊可找出失敗的原因。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**錯誤 \_ 不正確 \_ CRUNTIME \_ 參數**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



傳遞至 C 執行時間函數的參數不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**\_VDL 以外的錯誤 \_**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



作業發生超過檔案的有效資料長度。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**錯誤 \_ 的 \_ 服務 \_ SID \_ 類型不相容**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



服務啟動失敗，因為相同進程中的一或多個服務具有不相容的服務 SID 類型設定。 具有受限制服務 SID 類型的服務，只能與具有受限 SID 類型的其他服務並存于相同的進程中。 如果這項服務的服務 SID 類型是剛設定的，則必須重新開機裝載進程，才能啟動此服務。

在 Windows Server 2003 和 Windows XP 上，不受限制的服務無法與其他服務並存于相同的進程中。 具有不受限制服務 SID 類型的服務必須移至擁有的進程，才能啟動此服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**錯誤 \_ 驅動程式 \_ 進程已 \_ 終止**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



裝載此裝置之驅動程式的進程已終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**錯誤的 \_ 執行 \_ 限制**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



作業嘗試超過執行定義的限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**錯誤 \_ 進程 \_ 受到 \_ 保護**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



目標進程或目標執行緒的包含進程是受保護的進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**錯誤 \_ 服務 \_ 通知 \_ 用戶端 \_ 延遲**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



服務通知用戶端延遲到電腦目前的服務狀態之後太遠。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_超過錯誤磁片 \_ 配額 \_**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



要求的檔案作業失敗，因為已超過儲存配額。 若要釋出磁碟空間，請將檔案移到不同的位置，或刪除不必要的檔案。 如需相關資訊，請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**封鎖的錯誤 \_ 內容 \_**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



要求的檔案作業失敗，因為儲存原則封鎖了該類型的檔。 如需相關資訊，請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**錯誤 \_ 的 \_ 服務 \_ 許可權不相容**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



服務帳戶設定中沒有正常運作所需的許可權。 您可以使用服務 Microsoft Management Console (MMC) 嵌入式管理單元 (services.msc) 和本機安全性設定 MMC 嵌入式管理單元 (secpol.msc，以查看服務設定和帳戶設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**錯誤 \_ 應用程式停止 \_ 回應**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



這項作業所涉及的執行緒似乎沒有回應。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**錯誤 \_ 不正確 \_ 標籤**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



指出特定的安全識別碼可能無法指派為物件的標籤。


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




