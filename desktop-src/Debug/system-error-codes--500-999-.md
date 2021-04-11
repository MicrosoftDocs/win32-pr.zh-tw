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
# <a name="system-error-codes-500-999"></a>系統錯誤碼 (500-999) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。

下列清單描述 (錯誤500到 999) 的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**\_使用者 \_ 設定檔 \_ 載入錯誤**
</dt> <dd> <dl> <dt>

500 (0x1F4) 
</dt> <dt>



無法載入使用者設定檔。


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**錯誤 \_ 算術 \_ 溢位**
</dt> <dd> <dl> <dt>

534 (0x216) 
</dt> <dt>



算術結果超過32個位。


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**連接的錯誤 \_ 管道 \_**
</dt> <dd> <dl> <dt>

535 (0x217) 
</dt> <dt>



管道的另一端有處理常式。


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**錯誤 \_ 管道 \_ 接聽**
</dt> <dd> <dl> <dt>

536 (0x218) 
</dt> <dt>



等候進程開啟管道的另一端。


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**錯誤 \_ 驗證器 \_ 停止**
</dt> <dd> <dl> <dt>

537 (0x219) 
</dt> <dt>



應用程式驗證器在目前的進程中發現錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**錯誤 \_ ABIOS \_ 錯誤**
</dt> <dd> <dl> <dt>

538 (0x21A) 
</dt> <dt>



ABIOS 子系統發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**錯誤 \_ WX86 \_ 警告**
</dt> <dd> <dl> <dt>

539 (0x21B) 
</dt> <dt>



WX86 子系統發生警告。


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**錯誤 \_ WX86 \_ 錯誤**
</dt> <dd> <dl> <dt>

540 (0x21C) 
</dt> <dt>



WX86 子系統發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**錯誤 \_ 計時器 \_ 未 \_ 取消**
</dt> <dd> <dl> <dt>

541 (0x21D) 
</dt> <dt>



嘗試取消或設定具有相關聯的 APC 的計時器，且主體執行緒不是最初以關聯的 APC 常式設定計時器的執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**錯誤 \_ 回溯**
</dt> <dd> <dl> <dt>

542 (0x21E) 
</dt> <dt>



回溯例外狀況程式碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**錯誤 \_ \_ 堆疊錯誤**
</dt> <dd> <dl> <dt>

543 (0x21F) 
</dt> <dt>



在回溯操作期間遇到無效或未對齊的堆疊。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**錯誤 \_ 不正確回溯 \_ \_ 目標**
</dt> <dd> <dl> <dt>

544 (0x220) 
</dt> <dt>



回溯作業期間發生不正確回溯目標。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**錯誤 \_ 不正確 \_ 埠 \_ 屬性**
</dt> <dd> <dl> <dt>

545 (0x221) 
</dt> <dt>



指定給 NtCreatePort 的物件屬性無效或指定給 NtConnectPort 的埠屬性無效


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**錯誤 \_ 埠 \_ 訊息 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

546 (0x222) 
</dt> <dt>



傳遞至 NtRequestPort 或 NtRequestWaitReplyPort 的訊息長度超過埠允許的最大訊息數。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**錯誤 \_ 不正確 \_ 配額 \_**
</dt> <dd> <dl> <dt>

547 (0x223) 
</dt> <dt>



嘗試降低低於目前使用量的配額限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**\_ \_ 已 \_ 附加的錯誤裝置**
</dt> <dd> <dl> <dt>

548 (0x224) 
</dt> <dt>



嘗試附加至已附加至另一個裝置的裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**錯誤 \_ 指令 \_ 對齊**
</dt> <dd> <dl> <dt>

549 (0x225) 
</dt> <dt>



嘗試在未對齊的位址執行指令，而主機系統不支援未對齊的指令參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**\_ \_ 未啟動錯誤 \_ 分析**
</dt> <dd> <dl> <dt>

550 (0x226) 
</dt> <dt>



未啟動程式碼剖析。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ 未 \_ 停止錯誤程式碼剖析**
</dt> <dd> <dl> <dt>

551 (0x227) 
</dt> <dt>



未停止程式碼剖析。


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**錯誤 \_ 無法 \_ \_ 解讀**
</dt> <dd> <dl> <dt>

552 (0x228) 
</dt> <dt>



傳遞的 ACL 未包含必要的最小資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**\_限制錯誤 \_ 分析 \_**
</dt> <dd> <dl> <dt>

553 (0x229) 
</dt> <dt>



使用中的分析物件數目已達上限，而且無法再啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**錯誤 \_ 無法 \_ 等候**
</dt> <dd> <dl> <dt>

554 (0x22A) 
</dt> <dt>



用來表示作業無法繼續，而不會封鎖 i/o。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**錯誤 \_ 無法 \_ 終止 \_ 本身**
</dt> <dd> <dl> <dt>

555 (0x22B) 
</dt> <dt>



表示執行緒依預設會嘗試終止本身 (稱為 NtTerminateThread 與 **Null**) ，而且它是目前進程中的最後一個執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**未 \_ 預期的錯誤 \_ MM \_ CREATE \_ ERR**
</dt> <dd> <dl> <dt>

556 (0x22C) 
</dt> <dt>



如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。 不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**錯誤未 \_ 預期的 \_ MM \_ 對應 \_ 錯誤**
</dt> <dd> <dl> <dt>

557 (0x22D) 
</dt> <dt>



如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。 不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**未預期的錯誤， \_ \_ \_ 擴充 \_ 錯誤**
</dt> <dd> <dl> <dt>

558 (0x22E) 
</dt> <dt>



如果傳回的 MM 錯誤未在標準 FsRtl 篩選中定義，則會將它轉換成下列其中一個保證在篩選中的錯誤。 不過，在此情況下，資訊會遺失，而篩選器會正確處理例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**錯誤 \_ 的 \_ 函數 \_ 資料表**
</dt> <dd> <dl> <dt>

559 (0x22F) 
</dt> <dt>



在回溯作業期間遇到格式不正確的函式資料表。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**錯誤， \_ 不會 \_ \_ 轉譯 GUID**
</dt> <dd> <dl> <dt>

560 (0x230) 
</dt> <dt>



指出嘗試將保護指派給檔案系統檔案或目錄，而安全描述項中的其中一個 Sid 無法轉譯為檔案系統可儲存的 GUID。 這會導致保護嘗試失敗，這可能會導致檔案建立嘗試失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**\_不正確 \_ LDT \_ 大小錯誤**
</dt> <dd> <dl> <dt>

561 (0x231) 
</dt> <dt>



指出嘗試藉由設定其大小來擴大 LDT，或大小不是偶數的選取器。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**錯誤 \_ 不正確 \_ LDT \_ 位移**
</dt> <dd> <dl> <dt>

563 (0x233) 
</dt> <dt>



指出 LDT 資訊的起始值不是選取器大小的整數倍數。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**錯誤 \_ 不正確 \_ LDT \_ 描述項**
</dt> <dd> <dl> <dt>

564 (0x234) 
</dt> <dt>



指出使用者在嘗試設定 Ldt 描述項時，提供了不正確描述項。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**錯誤 \_ 太 \_ 多 \_ 執行緒**
</dt> <dd> <dl> <dt>

565 (0x235) 
</dt> <dt>



表示進程的執行緒太多，無法執行要求的動作。 例如，只有當進程有零個或一個執行緒時，才會執行主要權杖的指派。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**錯誤 \_ 執行緒 \_ 不 \_ 在 \_ 進程中**
</dt> <dd> <dl> <dt>

566 (0x236) 
</dt> <dt>



嘗試在特定進程內的執行緒上操作，但指定的執行緒不在指定的處理常式中。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_超過錯誤分頁檔 \_ 配額 \_**
</dt> <dd> <dl> <dt>

567 (0x237) 
</dt> <dt>



超過分頁檔案配額。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**錯誤 \_ 登入 \_ 伺服器 \_ 衝突**
</dt> <dd> <dl> <dt>

568 (0x238) 
</dt> <dt>



Netlogon 服務無法啟動，因為網域中執行的另一個 Netlogon 服務與指定的角色發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**\_需要同步處理錯誤 \_**
</dt> <dd> <dl> <dt>

569 (0x239) 
</dt> <dt>



Windows 伺服器上的 SAM 資料庫與網域控制站上的複本之間的同步處理有明顯的差異。 需要完整的同步處理。


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**錯誤 \_ 網路 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

570 (0x23A) 
</dt> <dt>



NtCreateFile API 失敗。 此錯誤永遠不會傳回給應用程式，而是 Windows Lan Manager 重新導向程式在其內部錯誤對應常式中使用的預留位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**錯誤 \_ IO \_ 許可權 \_ 失敗**
</dt> <dd> <dl> <dt>

571 (0x23B) 
</dt> <dt>



{許可權失敗}無法變更進程的 i/o 許可權。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR \_ CONTROL \_ C \_ EXIT**
</dt> <dd> <dl> <dt>

572 (0x23C) 
</dt> <dt>



{Application Exit by CTRL + C}應用程式因 CTRL + C 而終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**錯誤 \_ 遺失 \_ SYSTEMFILE**
</dt> <dd> <dl> <dt>

573 (0x23D) 
</dt> <dt>



{遺失系統檔案}所需的系統檔案% hs 不正確或遺失。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**錯誤 \_ 未處理的 \_ 例外狀況**
</dt> <dd> <dl> <dt>

574 (0x23E) 
</dt> <dt>



{應用程式錯誤}在位置 0x% 08lx 的應用程式中發生例外狀況% s (0x% 08lx) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**錯誤 \_ 應用程式 \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

575 (0x23F) 
</dt> <dt>



{應用程式錯誤}應用程式無法正確啟動 (0x% lx) 。 按一下 [確定] 以關閉應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**錯誤 \_ 頁面 \_ 建立 \_ 失敗**
</dt> <dd> <dl> <dt>

576 (0x240) 
</dt> <dt>



{無法建立分頁檔案}建立分頁檔案% hs 失敗 (% lx) 。 要求的大小為% ld。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**錯誤 \_ 不正確 \_ 影像 \_ 雜湊**
</dt> <dd> <dl> <dt>

577 (0x241) 
</dt> <dt>



Windows 無法驗證此檔案的數位簽章。 最近的硬體或軟體變更可能已安裝簽署錯誤或損毀的檔案，或可能是來自不明來源的惡意軟體。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**錯誤 \_ 的 \_ 分頁檔**
</dt> <dd> <dl> <dt>

578 (0x242) 
</dt> <dt>



{未指定分頁檔案}系統組態中未指定任何分頁檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**錯誤不 \_ 合法的 \_ FLOAT \_ 內容**
</dt> <dd> <dl> <dt>

579 (0x243) 
</dt> <dt>



意外發出浮點指令和浮點硬體的實際模式應用程式不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**錯誤 \_ 無 \_ 事件 \_ 配對**
</dt> <dd> <dl> <dt>

580 (0x244) 
</dt> <dt>



使用執行緒特定用戶端/伺服器事件組物件執行事件配對同步處理作業，但沒有與執行緒相關聯的事件配對物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**錯誤 \_ 網域 \_ CTRLR \_ 設定 \_ 錯誤**
</dt> <dd> <dl> <dt>

581 (0x245) 
</dt> <dt>



Windows Server 的設定不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**錯誤不 \_ 合法的 \_ 字元**
</dt> <dd> <dl> <dt>

582 (0x246) 
</dt> <dt>



遇到不合法的字元。 若為多位元組字元集，則會包含前導位元組，而不含後續的後隨位元組。 對於 Unicode 字元集，這包括了0xFFFF 和0xFFFE 的字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**錯誤 \_ 未定義 \_ 字元**
</dt> <dd> <dl> <dt>

583 (0x247) 
</dt> <dt>



Unicode 字元不會在安裝于系統上的 Unicode 字元集中定義。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**磁片區錯誤 \_ \_**
</dt> <dd> <dl> <dt>

584 (0x248) 
</dt> <dt>



無法在磁片磁碟機上建立分頁檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**錯誤 \_ BIOS \_ 無法 \_ \_ 連接 \_ 中斷**
</dt> <dd> <dl> <dt>

585 (0x249) 
</dt> <dt>



系統 BIOS 無法將系統中斷連接到裝置所連線的裝置或匯流排。


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**\_備份 \_ 控制器時發生錯誤**
</dt> <dd> <dl> <dt>

586 (0x24A) 
</dt> <dt>



這項作業只允許用於網域的主域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_超過錯誤變異 \_ 數限制 \_**
</dt> <dd> <dl> <dt>

587 (0x24B) 
</dt> <dt>



嘗試取得變異數，使其最大計數已超過。


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**\_需要錯誤 FS \_ 驅動程式 \_**
</dt> <dd> <dl> <dt>

588 (0x24C) 
</dt> <dt>



已存取磁片區，但該磁片區的檔案系統驅動程式尚未載入。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**錯誤 \_ 無法 \_ 載入 \_ 登錄 \_ 檔**
</dt> <dd> <dl> <dt>

589 (0x24D) 
</dt> <dt>



{Registry File 失敗}登錄無法載入 hive (檔) ：% hs 或其記錄檔或其他檔案。 它已損毀、不存在或不可寫入。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**錯誤的 \_ DEBUG \_ 附加 \_ 失敗**
</dt> <dd> <dl> <dt>

590 (0x24E) 
</dt> <dt>



{ [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)中發生未預期的失敗}處理 **DebugActiveProcess** API 要求時發生未預期的失敗。 您可以選擇 [確定] 終止進程，或選擇 [取消] 忽略錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**\_系統 \_ 進程 \_ 終止時發生錯誤**
</dt> <dd> <dl> <dt>

591 (0x24F) 
</dt> <dt>



{嚴重系統錯誤}% Hs 系統進程意外結束，狀態為 0x% 08x (0x% 08x 0x% 08x) 。 系統已關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**錯誤 \_ 資料 \_ 不 \_ 接受**
</dt> <dd> <dl> <dt>

592 (0x250) 
</dt> <dt>



{不接受資料}TDI 用戶端無法處理在指示期間收到的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**錯誤的 \_ VDM \_ 硬性 \_ 錯誤**
</dt> <dd> <dl> <dt>

593 (0x251) 
</dt> <dt>



NTVDM 發生硬性錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**錯誤 \_ 驅動程式 \_ 取消 \_ 超時**
</dt> <dd> <dl> <dt>

594 (0x252) 
</dt> <dt>



{取消 Timeout}驅動程式% hs 無法在分配的時間內完成取消的 i/o 要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**錯誤 \_ 回復 \_ 訊息 \_ 不符**
</dt> <dd> <dl> <dt>

595 (0x253) 
</dt> <dt>



{回復訊息不符}已嘗試回復 LPC 訊息，但訊息中的用戶端識別碼所指定的執行緒未在該訊息上等候。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**\_ \_ WRITEBEHIND 資料遺失 \_ 錯誤**
</dt> <dd> <dl> <dt>

596 (0x254) 
</dt> <dt>



{延遲寫入失敗}Windows 無法儲存檔案% hs 的所有資料。 資料已遺失。 發生此錯誤的原因可能是您的電腦硬體或網路連線失敗。 請嘗試將此檔案儲存在其他位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**錯誤 \_ 用戶端 \_ 伺服器 \_ 參數 \_ 無效**
</dt> <dd> <dl> <dt>

597 (0x255) 
</dt> <dt>



在 [用戶端/伺服器共用記憶體] 視窗中傳遞給伺服器的參數 (s) 無效。 共用記憶體視窗中可能已放置太多資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**錯誤 \_ 不是 \_ 小型 \_ 串流**
</dt> <dd> <dl> <dt>

598 (0x256) 
</dt> <dt>



資料流程不是小型的資料流程。


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**錯誤 \_ 堆疊 \_ 溢位 \_ 讀取**
</dt> <dd> <dl> <dt>

599 (0x257) 
</dt> <dt>



要求必須由堆疊溢位程式碼處理。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**\_轉換 \_ 成 \_ 大型的錯誤**
</dt> <dd> <dl> <dt>

600 (0x258) 
</dt> <dt>



指出如何處理配置作業的內部 .OFS 狀態碼。 當包含的 onode 移動或範圍資料流程轉換成大型資料流程之後，就會重試。


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**\_發現 \_ 超出 \_ 範圍的 \_ 錯誤**
</dt> <dd> <dl> <dt>

601 (0x259) 
</dt> <dt>



嘗試尋找物件在磁片區上找到依識別碼比對的物件，但它不在用於作業的控制碼範圍內。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**\_配置 \_ BUCKET 時發生錯誤**
</dt> <dd> <dl> <dt>

602 (0x25A) 
</dt> <dt>



Bucket 陣列必須成長。 這麼做之後，請重試交易。


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**錯誤 \_ 馬紹爾 \_ 溢位**
</dt> <dd> <dl> <dt>

603 (0x25B) 
</dt> <dt>



使用者/核心封送處理緩衝區已溢位。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**錯誤 \_ 不正確 \_ 變異**
</dt> <dd> <dl> <dt>

604 (0x25C) 
</dt> <dt>



提供的 variant 結構包含不正確資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**錯誤 \_ 的 \_ 壓縮 \_ 緩衝區錯誤**
</dt> <dd> <dl> <dt>

605 (0x25D) 
</dt> <dt>



指定的緩衝區包含格式不正確的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**錯誤 \_ 審核 \_ 失敗**
</dt> <dd> <dl> <dt>

606 (0x25E) 
</dt> <dt>



{Audit Failed}嘗試產生安全性審核失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_ \_ \_ 未設定錯誤計時器 \_ 解析**
</dt> <dd> <dl> <dt>

607 (0x25F) 
</dt> <dt>



目前的進程先前未設定計時器解析度。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**錯誤 \_ 的 \_ 登入 \_ 資訊不足**
</dt> <dd> <dl> <dt>

608 (0x260) 
</dt> <dt>



沒有足夠的帳戶資訊可供您登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**錯誤 \_ 的 \_ DLL 進入 \_ 點**
</dt> <dd> <dl> <dt>

609 (0x261) 
</dt> <dt>



{不正確 DLL Entrypoint}未正確寫入動態連結程式庫% hs。 堆疊指標處於不一致的狀態。 Entrypoint 應宣告為 WINAPI 或 STDCALL。 選取 [是] 以使 DLL 載入失敗。 選取 [否] 以繼續執行。 選取 [否] 可能會導致應用程式無法正常運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**錯誤錯誤的 \_ \_ 服務進入 \_ 點**
</dt> <dd> <dl> <dt>

610 (0x262) 
</dt> <dt>



{不正確服務回呼 Entrypoint}% Hs 服務的寫入不正確。 堆疊指標處於不一致的狀態。 回呼進入點應宣告為 WINAPI 或 STDCALL。 選取 [確定] 將會導致服務繼續操作。 不過，服務進程的運作方式可能不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**\_IP \_ 位址 \_ CONFLICT1 錯誤**
</dt> <dd> <dl> <dt>

611 (0x263) 
</dt> <dt>



IP 位址與網路上的其他系統發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**\_IP \_ 位址 \_ CONFLICT2 錯誤**
</dt> <dd> <dl> <dt>

612 (0x264) 
</dt> <dt>



IP 位址與網路上的其他系統發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**錯誤 \_ 登錄 \_ 配額 \_ 限制**
</dt> <dd> <dl> <dt>

613 (0x265) 
</dt> <dt>



{註冊表空間不足}系統已到達登錄的系統部分所允許的大小上限。 將會忽略其他儲存體要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**錯誤 \_ 不使用 \_ 回呼 \_**
</dt> <dd> <dl> <dt>

614 (0x266) 
</dt> <dt>



當沒有任何回呼處於作用中狀態時，無法執行回呼傳回系統服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**錯誤 \_ PWD \_ 太 \_ 短**
</dt> <dd> <dl> <dt>

615 (0x267) 
</dt> <dt>



提供的密碼太短，無法符合您的使用者帳戶原則。 請選擇較長的密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**錯誤 \_ PWD \_ 太 \_ 晚**
</dt> <dd> <dl> <dt>

616 (0x268) 
</dt> <dt>



您的使用者帳戶原則不允許您太頻繁地變更密碼。 這麼做是為了防止使用者變更回熟悉但可能發現的密碼。 如果您認為您的密碼已遭盜用，請立即洽詢您的系統管理員，以指派新的密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**錯誤 \_ PWD \_ 記錄 \_ 衝突**
</dt> <dd> <dl> <dt>

617 (0x269) 
</dt> <dt>



您已嘗試將您的密碼變更為您過去使用過的密碼。 您的使用者帳戶原則不允許這種情況。 請選取您先前未使用過的密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**錯誤 \_ 不支援的 \_ 壓縮**
</dt> <dd> <dl> <dt>

618 (0x26A) 
</dt> <dt>



不支援指定的壓縮格式。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**錯誤 \_ 不正確 \_ HW \_ 設定檔**
</dt> <dd> <dl> <dt>

619 (0x26B) 
</dt> <dt>



指定的硬體設定檔設定無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**錯誤 \_ 不正確 \_ PLUGPLAY \_ 裝置 \_ 路徑**
</dt> <dd> <dl> <dt>

620 (0x26C) 
</dt> <dt>



指定的隨插即用登錄裝置路徑無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**錯誤 \_ 配額 \_ 清單 \_ 不一致**
</dt> <dd> <dl> <dt>

621 (0x26D) 
</dt> <dt>



指定的配額清單與其描述項在內部不一致。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**錯誤 \_ 評估 \_ 到期日**
</dt> <dd> <dl> <dt>

622 (0x26E) 
</dt> <dt>



{Windows 評估通知}此 Windows 安裝的評估期間已過期。 此系統會在1小時內關機。 若要還原此 Windows 安裝的存取權，請使用此產品的授權散發升級此安裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**錯誤不 \_ 合法的 \_ DLL 重新配置 \_**
</dt> <dd> <dl> <dt>

623 (0x26F) 
</dt> <dt>



{不合法的系統 DLL 重新配置}系統 DLL% hs 已在記憶體中重新置放。 應用程式將無法正常執行。 發生重新配置的原因是 DLL% hs 已佔用保留給 Windows 系統 Dll 的位址範圍。 提供 DLL 的廠商應該連接至新的 DLL。


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**錯誤 \_ DLL \_ 初始化 \_ 失敗 \_ 登出**
</dt> <dd> <dl> <dt>

624 (0x270) 
</dt> <dt>



{DLL 初始化失敗}應用程式無法初始化，因為視窗站正在關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**錯誤 \_ 驗證 \_ 繼續**
</dt> <dd> <dl> <dt>

625 (0x271) 
</dt> <dt>



驗證程式必須繼續進行下一個步驟。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**錯誤 \_ 不 \_ \_ 相符**
</dt> <dd> <dl> <dt>

626 (0x272) 
</dt> <dt>



目前的索引列舉沒有相符的專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**錯誤 \_ 範圍 \_ 清單 \_ 衝突**
</dt> <dd> <dl> <dt>

627 (0x273) 
</dt> <dt>



因為發生衝突，所以無法將範圍加入至範圍清單。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**錯誤 \_ 伺服器 \_ SID \_ 不符**
</dt> <dd> <dl> <dt>

628 (0x274) 
</dt> <dt>



伺服器進程在與用戶端所需的 SID 不同的情況下執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**錯誤 \_ 無法 \_ 啟用 \_ 拒絕 \_**
</dt> <dd> <dl> <dt>

629 (0x275) 
</dt> <dt>



無法啟用標示為僅供拒絕使用的群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**錯誤 \_ 浮點數 \_ 多個 \_ 錯誤**
</dt> <dd> <dl> <dt>

630 (0x276) 
</dt> <dt>



意外多個浮點錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR \_ FLOAT \_ 多重 \_ 陷阱**
</dt> <dd> <dl> <dt>

631 (0x277) 
</dt> <dt>



意外多個浮點數陷阱。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**錯誤 \_ NOINTERFACE**
</dt> <dd> <dl> <dt>

632 (0x278) 
</dt> <dt>



不支援要求的介面。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**錯誤 \_ 驅動程式 \_ 無法 \_ 進入睡眠狀態**
</dt> <dd> <dl> <dt>

633 (0x279) 
</dt> <dt>



{系統待命失敗}驅動程式% hs 不支援待命模式。 更新此驅動程式可能會允許系統進入待命模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**錯誤損毀的 \_ \_ 系統檔案 \_**
</dt> <dd> <dl> <dt>

634 (0x27A) 
</dt> <dt>



系統檔案 %1 已損毀，已被取代。


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**錯誤 \_ 承諾用量 \_ 下限**
</dt> <dd> <dl> <dt>

635 (0x27B) 
</dt> <dt>



{虛擬記憶體下限太低}您系統的虛擬記憶體不足。 Windows 正在增加虛擬記憶體分頁檔的大小。 在此過程中，某些應用程式的記憶體要求可能會被拒絕。 如需詳細資訊，請參閱說明。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**錯誤 \_ PNP \_ 重新開機 \_ 列舉**
</dt> <dd> <dl> <dt>

636 (0x27C) 
</dt> <dt>



已移除裝置，因此必須重新開機列舉。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**錯誤 \_ 的 \_ 系統 \_ 映射 \_ 簽名錯誤**
</dt> <dd> <dl> <dt>

637 (0x27D) 
</dt> <dt>



{嚴重系統錯誤}系統映射% s 未正確簽署。 檔案已取代為已簽署的檔案。 系統已關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**\_ \_ 需要重新開機錯誤 PNP \_**
</dt> <dd> <dl> <dt>

638 (0x27E) 
</dt> <dt>



裝置不會在重新開機的情況下啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**錯誤 \_ 的 \_ 電源不足**
</dt> <dd> <dl> <dt>

639 (0x27F) 
</dt> <dt>



沒有足夠的電源可以完成要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**錯誤 \_ 多個錯誤 \_ \_ 違規**
</dt> <dd> <dl> <dt>

640 (0x280) 
</dt> <dt>



錯誤 \_ 多個錯誤 \_ \_ 違規


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**錯誤 \_ 系統 \_ 關機**
</dt> <dd> <dl> <dt>

641 (0x281) 
</dt> <dt>



系統正在關機。


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_ \_ 未設定錯誤 \_ 埠**
</dt> <dd> <dl> <dt>

642 (0x282) 
</dt> <dt>



嘗試移除 DebugPort 的進程，但尚未與進程建立關聯的埠。


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**錯誤 \_ DS \_ 版本 \_ 檢查 \_ 失敗**
</dt> <dd> <dl> <dt>

643 (0x283) 
</dt> <dt>



此版本的 Windows 與目錄樹系、網域或網域控制站的行為版本不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_ \_ 找不到錯誤範圍 \_**
</dt> <dd> <dl> <dt>

644 (0x284) 
</dt> <dt>



在範圍清單中找不到指定的範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**錯誤 \_ 的 \_ 安全 \_ 模式 \_ 驅動程式**
</dt> <dd> <dl> <dt>

646 (0x286) 
</dt> <dt>



驅動程式未載入，因為系統開機進入安全模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**\_ \_ 驅動程式專案錯誤失敗 \_**
</dt> <dd> <dl> <dt>

647 (0x287) 
</dt> <dt>



驅動程式未載入，因為它的初始化呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**錯誤 \_ 裝置 \_ 列舉 \_ 錯誤**
</dt> <dd> <dl> <dt>

648 (0x288) 
</dt> <dt>



"% Hs" 在套用電源或讀取裝置設定時，發生錯誤。 這可能是因為您的硬體失敗或連線不佳所造成。


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**錯誤 \_ 裝入 \_ 點 \_ 未 \_ 解決**
</dt> <dd> <dl> <dt>

649 (0x289) 
</dt> <dt>



建立作業失敗，因為名稱至少包含一個掛接點，而該掛接點會解析成未附加指定之裝置物件的磁片區。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**錯誤 \_ 不正確 \_ 裝置 \_ 物件 \_ 參數**
</dt> <dd> <dl> <dt>

650 (0x28A) 
</dt> <dt>



裝置物件參數不是有效的裝置物件，或未附加至檔案名所指定的磁片區。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**\_發生錯誤 MCA \_**
</dt> <dd> <dl> <dt>

651 (0x28B) 
</dt> <dt>



發生電腦檢查錯誤。 請檢查系統事件記錄檔以取得其他資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**錯誤 \_ 驅動程式 \_ 資料庫 \_ 錯誤**
</dt> <dd> <dl> <dt>

652 (0x28C) 
</dt> <dt>



\[ \] 處理驅動程式資料庫時發生錯誤 %2。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**錯誤 \_ 系統 \_ HIVE \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

653 (0x28D) 
</dt> <dt>



系統 hive 大小超過其限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**錯誤 \_ 驅動程式在 \_ \_ 卸載前失敗 \_**
</dt> <dd> <dl> <dt>

654 (0x28E) 
</dt> <dt>



無法載入驅動程式，因為先前版本的驅動程式仍在記憶體中。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**錯誤 \_ VOLSNAP \_ 準備 \_ 休眠**
</dt> <dd> <dl> <dt>

655 (0x28F) 
</dt> <dt>



{磁碟區陰影複製服務}請稍候，磁碟區陰影複製服務準備磁片區% hs 以進行休眠。


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**錯誤 \_ 休眠 \_ 失敗**
</dt> <dd> <dl> <dt>

656 (0x290) 
</dt> <dt>



系統無法休眠 (錯誤碼為% hs) 。 休眠將會停用，直到系統重新開機為止。


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**錯誤 \_ PWD \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

657 (0x291) 
</dt> <dt>



提供的密碼太長，無法符合您的使用者帳戶原則。 請選擇較短的密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**錯誤 \_ 檔 \_ 系統 \_ 限制**
</dt> <dd> <dl> <dt>

665 (0x299) 
</dt> <dt>



無法完成要求的作業，因為檔案系統有限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**錯誤判斷提示 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

668 (0x29C) 
</dt> <dt>



發生判斷提示失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**錯誤 \_ ACPI \_ 錯誤**
</dt> <dd> <dl> <dt>

669 (0x29D) 
</dt> <dt>



ACPI 子系統發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**錯誤 \_ WOW 判斷提示 \_**
</dt> <dd> <dl> <dt>

670 (0x29E) 
</dt> <dt>



WOW 判斷提示錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**錯誤 \_ PNP 錯誤的 \_ \_ MP \_ 資料表**
</dt> <dd> <dl> <dt>

671 (0x29F) 
</dt> <dt>



系統 BIOS MP 資料表中遺漏裝置。 將不會使用此裝置。 請洽詢您的系統廠商以取得系統 BIOS 更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**錯誤 \_ PNP \_ 轉譯 \_ 失敗**
</dt> <dd> <dl> <dt>

672 (0x2A0) 
</dt> <dt>



翻譯工具無法轉譯資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**錯誤 \_ PNP \_ IRQ \_ 轉譯 \_ 失敗**
</dt> <dd> <dl> <dt>

673 (0x2A1) 
</dt> <dt>



IRQ 翻譯工具無法轉譯資源。


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**錯誤 \_ PNP \_ 無效 \_ 識別碼**
</dt> <dd> <dl> <dt>

674 (0x2A2) 
</dt> <dt>



驅動程式 %2 為子裝置 (% 3) 傳回了不正確識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**錯誤 \_ 喚醒 \_ 系統 \_ 偵錯工具**
</dt> <dd> <dl> <dt>

675 (0x2A3) 
</dt> <dt>



{內核偵錯工具喚醒} 系統偵錯工具是由插斷喚醒。


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**錯誤 \_ 控制碼 \_ 已關閉**
</dt> <dd> <dl> <dt>

676 (0x2A4) 
</dt> <dt>



{控制碼已關閉}物件的控制碼已自動關閉，因為要求的作業結果。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**錯誤 \_ 無關的 \_ 資訊**
</dt> <dd> <dl> <dt>

677 (0x2A5) 
</dt> <dt>



{太多資訊}指定的存取控制清單 (ACL) 包含的資訊比預期的還要多。


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**\_RXACT \_ 需要認可 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

678 (0x2A6) 
</dt> <dt>



這個警告層級狀態表示登錄子樹已經有交易狀態，但先前已中止交易認可。 認可尚未完成，但尚未回復 (因此，如果需要) ，仍可進行認可。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**錯誤 \_ 媒體 \_ 檢查**
</dt> <dd> <dl> <dt>

679 (0x2A7) 
</dt> <dt>



{媒體已變更}媒體可能已變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**已 \_ 進行錯誤 GUID \_ 替代 \_**
</dt> <dd> <dl> <dt>

680 (0x2A8) 
</dt> <dt>



{GUID 替代}在將全域識別碼 (GUID) 轉換為 Windows 安全識別碼 (SID) 時，找不到系統管理員定義的 GUID 前置詞。 使用替代首碼，這將不會危害系統安全性。 不過，這可能會提供比預期更嚴格的存取權。


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**\_ \_ 符號上的錯誤已停止 \_**
</dt> <dd> <dl> <dt>

681 (0x2A9) 
</dt> <dt>



建立作業會在到達符號連結後停止。


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**錯誤 \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA) 
</dt> <dt>



已執行長時間跳躍。


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**\_PLUGPLAY \_ 拒絕的查詢 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

683 (0x2AB) 
</dt> <dt>



隨插即用查詢作業不成功。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**錯誤 \_ 回溯 \_ 合併**
</dt> <dd> <dl> <dt>

684 (0x2AC) 
</dt> <dt>



已執行框架合併。


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_復原登錄 \_ HIVE \_ 錯誤**
</dt> <dd> <dl> <dt>

685 (0x2AD) 
</dt> <dt>



{登錄 Hive 已復原}登錄 hive (檔案) ：% hs 已損毀，且已復原。 某些資料可能已遺失。


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**錯誤 \_ DLL \_ 可能 \_ 不 \_ 安全**
</dt> <dd> <dl> <dt>

686 (0x2AE) 
</dt> <dt>



應用程式正在嘗試從模組% hs 執行可執行程式碼。 這可能不安全。 有替代方案% hs 可供使用。 應用程式是否應該使用安全模組% hs？


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**錯誤 \_ DLL \_ 可能 \_ \_ 不相容**
</dt> <dd> <dl> <dt>

687 (0x2AF) 
</dt> <dt>



應用程式正在從模組% hs 載入可執行檔程式碼。 這是安全的，但可能與舊版的作業系統不相容。 有替代方案% hs 可供使用。 應用程式是否應該使用安全模組% hs？


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**錯誤 \_ DBG \_ 例外狀況 \_ 未 \_ 處理**
</dt> <dd> <dl> <dt>

688 (0x2B0) 
</dt> <dt>



偵錯工具未處理例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**錯誤 \_ DBG \_ 于 \_ 稍後回復**
</dt> <dd> <dl> <dt>

689 (0x2B1) 
</dt> <dt>



偵錯工具稍後會回復。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**錯誤 \_ DBG \_ 無法 \_ \_ 提供 \_ 控制碼**
</dt> <dd> <dl> <dt>

690 (0x2B2) 
</dt> <dt>



偵錯工具無法提供控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**錯誤 \_ DBG \_ 終止 \_ 執行緒**
</dt> <dd> <dl> <dt>

691 (0x2B3) 
</dt> <dt>



偵錯工具終止的執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**錯誤 \_ DBG \_ 終止 \_ 進程**
</dt> <dd> <dl> <dt>

692 (0x2B4) 
</dt> <dt>



偵錯工具已終止進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**錯誤 \_ DBG \_ 控制項 \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5) 
</dt> <dt>



偵錯工具得到控制項 C。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**錯誤 \_ DBG \_ PRINTEXCEPTION \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6) 
</dt> <dt>



控制項 C 上的偵錯工具列印例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**錯誤 \_ DBG \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7) 
</dt> <dt>



偵錯工具收到 RIP 例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**錯誤 \_ DBG \_ 控制 \_ 中斷**
</dt> <dd> <dl> <dt>

696 (0x2B8) 
</dt> <dt>



偵錯工具收到控制中斷。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**錯誤 \_ DBG \_ 命令 \_ 例外狀況**
</dt> <dd> <dl> <dt>

697 (0x2B9) 
</dt> <dt>



偵錯工具命令通訊例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**錯誤 \_ 物件 \_ 名稱 \_ 存在**
</dt> <dd> <dl> <dt>

698 (0x2BA) 
</dt> <dt>



{Object Exists}嘗試建立物件，而物件名稱已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**錯誤 \_ 執行緒 \_ 已 \_ 暫止**
</dt> <dd> <dl> <dt>

699 (0x2BB) 
</dt> <dt>



{執行緒已暫止}執行緒暫止時發生執行緒終止。 已繼續執行緒，並繼續進行終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**錯誤 \_ 影像 \_ 不 \_ 在 \_ 基底**
</dt> <dd> <dl> <dt>

700 (0x2BC) 
</dt> <dt>



{重定位映射}影像檔案中所指定的位址無法對應影像檔案。 您必須對此映射執行本機修正。


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**\_RXACT \_ 建立的狀態 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

701 (0x2BD) 
</dt> <dt>



此資訊層級狀態表示指定的登錄子樹交易狀態尚未存在且必須建立。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**錯誤 \_ 區段 \_ 通知**
</dt> <dd> <dl> <dt>

702 (0x2BE) 
</dt> <dt>



{區段載入} (VDM 的虛擬 DOS 機器) 正在載入、卸載或移動 MS-DOS 或 Win16 程式區段映射。 引發例外狀況，讓偵錯工具可以載入、卸載或追蹤這些16位區段內的符號和中斷點。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**錯誤 \_ 的 \_ 當前 \_ 目錄錯誤**
</dt> <dd> <dl> <dt>

703 (0x2BF) 
</dt> <dt>



{不正確目前的目錄}進程無法切換至啟動的目前的目錄% hs。 選取 [確定] 將目前的目錄設為% hs，或選取 [取消] 以結束。


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**\_備份的錯誤 FT \_ 讀取 \_ 修復 \_ \_**
</dt> <dd> <dl> <dt>

704 (0x2C0) 
</dt> <dt>



{多餘讀取}為了滿足讀取要求，NT 容錯檔案系統成功從重複的複本讀取要求的資料。 因為檔案系統在容錯磁片區的成員上發生失敗，但無法重新指派裝置的失敗區域，所以已完成此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**錯誤 \_ FT \_ 寫入 \_ 復原**
</dt> <dd> <dl> <dt>

705 (0x2C1) 
</dt> <dt>



{多餘寫入}為了滿足寫入要求，NT 容錯檔案系統已成功寫入一份重複的資訊。 因為檔案系統在容錯磁片區的成員上發生失敗，但無法重新指派裝置的失敗區域，所以已完成這項作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**錯誤 \_ 映射 \_ 電腦 \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

706 (0x2C2) 
</dt> <dt>



{電腦類型不符}影像檔案% hs 有效，但適用于目前電腦以外的電腦類型。 選取 [確定] 以繼續，或選取 [取消] 以使 DLL 載入失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**錯誤 \_ 接收 \_ 部分**
</dt> <dd> <dl> <dt>

707 (0x2C3) 
</dt> <dt>



{已接收部分資料}網路傳輸會將部分資料傳回給其用戶端。 其餘的資料將會在稍後傳送。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**\_收到 \_ 快速錯誤**
</dt> <dd> <dl> <dt>

708 (0x2C4) 
</dt> <dt>



{已收到快速資料}網路傳輸會將資料傳回給用戶端，而該用戶端是由遠端系統標示為已加速。


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**錯誤 \_ 接收 \_ 部分 \_ 加急**
</dt> <dd> <dl> <dt>

709 (0x2C5) 
</dt> <dt>



{已接收部分快速資料}網路傳輸會將部分資料傳回給其用戶端，而且此資料會被遠端系統標示為已加速。 其餘的資料將會在稍後傳送。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**錯誤 \_ 事件已 \_ 完成**
</dt> <dd> <dl> <dt>

710 (0x2C6) 
</dt> <dt>



{TDI 事件已完成}TDI 表示已順利完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**錯誤 \_ 事件 \_ 暫止**
</dt> <dd> <dl> <dt>

711 (0x2C7) 
</dt> <dt>



{TDI 事件暫止}TDI 表示已進入擱置狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**\_檢查 \_ 檔 \_ 系統時發生錯誤**
</dt> <dd> <dl> <dt>

712 (0x2C8) 
</dt> <dt>



正在檢查% wZ 上的檔案系統。


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**錯誤 \_ 嚴重 \_ 應用程式結束 \_**
</dt> <dd> <dl> <dt>

713 (0x2C9) 
</dt> <dt>



{嚴重的應用程式結束}% hs。


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_預先定義的 \_ 控制碼錯誤**
</dt> <dd> <dl> <dt>

714 (0x2CA) 
</dt> <dt>



指定的登錄機碼由預先定義的控制碼參考。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**錯誤 \_ 已 \_ 解除鎖定**
</dt> <dd> <dl> <dt>

715 (0x2CB) 
</dt> <dt>



{已解除鎖定頁面}鎖定頁面的頁面保護已變更為 [無存取]，而且頁面已從記憶體和進程解除鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**錯誤 \_ 服務 \_ 通知**
</dt> <dd> <dl> <dt>

716 (0x2CC) 
</dt> <dt>



% hs


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**錯誤 \_ 已 \_ 鎖定**
</dt> <dd> <dl> <dt>

717 (0x2CD) 
</dt> <dt>



{頁面鎖定}其中一個要鎖定的頁面已經鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**錯誤 \_ 記錄檔 \_ 硬性 \_ 錯誤**
</dt> <dd> <dl> <dt>

718 (0x2CE) 
</dt> <dt>



應用程式快顯視窗： %1： %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**錯誤 \_ 已經是 \_ WIN32**
</dt> <dd> <dl> <dt>

719 (0x2CF) 
</dt> <dt>



錯誤 \_ 已經是 \_ WIN32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**錯誤 \_ 映射 \_ 電腦 \_ 類型 \_ 不相符 \_ EXE**
</dt> <dd> <dl> <dt>

720 (0x2D0) 
</dt> <dt>



{電腦類型不符}影像檔案% hs 有效，但適用于目前電腦以外的電腦類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**\_未 \_ 執行任何 YIELD \_ 的錯誤**
</dt> <dd> <dl> <dt>

721 (0x2D1) 
</dt> <dt>



執行了 yield 執行，而且沒有任何執行緒可以執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**已 \_ 忽略錯誤計時器 \_ 繼續 \_**
</dt> <dd> <dl> <dt>

722 (0x2D2) 
</dt> <dt>



已忽略計時器 API 的可繼續旗標。


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**錯誤 \_ 仲裁 \_ 未處理**
</dt> <dd> <dl> <dt>

723 (0x2D3) 
</dt> <dt>



仲裁者已將這些資源的仲裁延後到其父系。


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**\_ \_ 不支援錯誤 \_ CARDBUS**
</dt> <dd> <dl> <dt>

724 (0x2D4) 
</dt> <dt>



因為 "% hs" 發生設定錯誤，所以無法啟動插入的 CardBus 裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**錯誤 \_ MP \_ 處理器 \_ 不相符**
</dt> <dd> <dl> <dt>

725 (0x2D5) 
</dt> <dt>



此多處理器系統中的 Cpu 不是全部相同的修訂層級。 若要使用所有處理器，作業系統會將其本身限制為系統中最少可用處理器的功能。 如果此系統發生問題，請洽詢 CPU 製造商以查看是否支援這種處理器組合。


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**錯誤 \_ 休眠**
</dt> <dd> <dl> <dt>

726 (0x2D6) 
</dt> <dt>



系統已進入休眠狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**錯誤 \_ 繼續 \_ 休眠**
</dt> <dd> <dl> <dt>

727 (0x2D7) 
</dt> <dt>



系統已從休眠狀態恢復。


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**錯誤的 \_ 固件 \_ 已更新**
</dt> <dd> <dl> <dt>

728 (0x2D8) 
</dt> <dt>



Windows 偵測到系統固件 (BIOS) 更新了之前的 \[ 固件日期 = %2，目前的固件日期 %3 \] 。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**\_ \_ 洩漏 \_ 鎖定頁面的 \_ 錯誤驅動程式**
</dt> <dd> <dl> <dt>

729 (0x2D9) 
</dt> <dt>



設備磁碟機正在洩漏鎖定的 i/o 頁面，導致系統效能降低。 系統已自動啟用追蹤程式碼，以便嘗試並攔截問題。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**錯誤 \_ 喚醒 \_ 系統**
</dt> <dd> <dl> <dt>

730 (0x2DA) 
</dt> <dt>



系統有喚醒。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**錯誤 \_ 等候 \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB) 
</dt> <dt>



錯誤 \_ 等候 \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**錯誤 \_ 等候 \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC) 
</dt> <dt>



錯誤 \_ 等候 \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**錯誤 \_ 等候 \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD) 
</dt> <dt>



錯誤 \_ 等候 \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**錯誤 \_ 等候 \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE) 
</dt> <dt>



錯誤 \_ 等候 \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**錯誤 \_ 放棄 \_ 等候 \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF) 
</dt> <dt>



錯誤 \_ 放棄 \_ 等候 \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**錯誤 \_ 放棄 \_ 等候 \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0) 
</dt> <dt>



錯誤 \_ 放棄 \_ 等候 \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**\_使用者 \_ APC 錯誤**
</dt> <dd> <dl> <dt>

737 (0x2E1) 
</dt> <dt>



\_使用者 \_ APC 錯誤


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**錯誤 \_ 核心 \_**
</dt> <dd> <dl> <dt>

738 (0x2E2) 
</dt> <dt>



錯誤 \_ 核心 \_


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**\_警示錯誤**
</dt> <dd> <dl> <dt>

739 (0x2E3) 
</dt> <dt>



\_警示錯誤


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_需要提高許可權 \_**
</dt> <dd> <dl> <dt>

740 (0x2E4) 
</dt> <dt>



要求的作業需要提高許可權。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**錯誤重新 \_ 分析**
</dt> <dd> <dl> <dt>

741 (0x2E5) 
</dt> <dt>



因為檔案的名稱會產生符號連結，所以物件管理員應該執行重新剖析。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**錯誤 \_ OPLOCK \_ 中斷 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

742 (0x2E6) 
</dt> <dt>



當 oplock 中斷正在進行時，開啟/建立作業已完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**裝載的錯誤 \_ 磁片區 \_**
</dt> <dd> <dl> <dt>

743 (0x2E7) 
</dt> <dt>



檔案系統已載入新的磁片區。


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**\_RXACT \_ 認可的錯誤**
</dt> <dd> <dl> <dt>

744 (0x2E8) 
</dt> <dt>



此成功層級狀態表示登錄子樹已經有交易狀態，但先前已中止交易認可。 認可現在已完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_通知 \_ 清除時發生錯誤**
</dt> <dd> <dl> <dt>

745 (0x2E9) 
</dt> <dt>



這表示通知變更要求已完成，因為關閉發出通知變更要求的控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**\_主要 \_ 傳輸 \_ 連接 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

746 (0x2EA) 
</dt> <dt>



{主要傳輸上的連接失敗}嘗試連接到主要傳輸上的遠端伺服器% hs，但連線失敗。 電腦可以在次要傳輸上連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 轉換**
</dt> <dd> <dl> <dt>

747 (0x2EB) 
</dt> <dt>



分頁錯誤是轉換錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 要求 \_ 零**
</dt> <dd> <dl> <dt>

748 (0x2EC) 
</dt> <dt>



分頁錯誤是要求零錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**寫入時錯誤 \_ 分頁錯誤 \_ \_ 複製 \_ \_**
</dt> <dd> <dl> <dt>

749 (0x2ED) 
</dt> <dt>



分頁錯誤是要求零錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**錯誤 \_ 頁面 \_ 錯誤 \_ 防護 \_ 頁面**
</dt> <dd> <dl> <dt>

750 (0x2EE) 
</dt> <dt>



分頁錯誤是要求零錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**錯誤 \_ 分頁錯誤頁面 \_ \_ \_ 檔案**
</dt> <dd> <dl> <dt>

751 (0x2EF) 
</dt> <dt>



從次要儲存裝置讀取時，已滿足分頁錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**鎖定快取頁面時發生錯誤 \_ \_ \_**
</dt> <dd> <dl> <dt>

752 (0x2F0) 
</dt> <dt>



在作業期間鎖定快取頁面。


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**錯誤損毀傾印 \_ \_**
</dt> <dd> <dl> <dt>

753 (0x2F1) 
</dt> <dt>



分頁檔案中有損毀傾印。


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**錯誤 \_ 緩衝區 \_ 全部為 \_ 零**
</dt> <dd> <dl> <dt>

754 (0x2F2) 
</dt> <dt>



指定的緩衝區包含所有零。


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**錯誤重新 \_ 分析 \_ 物件**
</dt> <dd> <dl> <dt>

755 (0x2F3) 
</dt> <dt>



因為檔案的名稱會產生符號連結，所以物件管理員應該執行重新剖析。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**錯誤 \_ 資源 \_ 需求 \_ 已變更**
</dt> <dd> <dl> <dt>

756 (0x2F4) 
</dt> <dt>



裝置已成功查詢-停止，且其資源需求已變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**錯誤 \_ 轉譯 \_ 完成**
</dt> <dd> <dl> <dt>

757 (0x2F5) 
</dt> <dt>



翻譯工具已將這些資源轉譯為全域空間，因此不應執行任何進一步的翻譯。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_沒有 \_ 終止的 \_ 錯誤**
</dt> <dd> <dl> <dt>

758 (0x2F6) 
</dt> <dt>



終止的進程沒有可終止的執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**錯誤 \_ 處理常式 \_ 不 \_ 在 \_ 工作中**
</dt> <dd> <dl> <dt>

759 (0x2F7) 
</dt> <dt>



指定的進程不是作業的一部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_ \_ 作業中的錯誤處理常式 \_**
</dt> <dd> <dl> <dt>

760 (0x2F8) 
</dt> <dt>



指定的進程是作業的一部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**錯誤 \_ VOLSNAP \_ 休眠 \_ 就緒**
</dt> <dd> <dl> <dt>

761 (0x2F9) 
</dt> <dt>



{磁碟區陰影複製服務}系統現在已準備好休眠。


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**錯誤 \_ FSFILTER \_ OP \_ 已 \_ 順利完成**
</dt> <dd> <dl> <dt>

762 (0x2FA) 
</dt> <dt>



檔案系統或檔案系統篩選器驅動程式已順利完成 FsFilter 操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**\_ \_ \_ 已連線的錯誤中斷向量 \_**
</dt> <dd> <dl> <dt>

763 (0x2FB) 
</dt> <dt>



指定的中斷向量已連接。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**錯誤 \_ 中斷 \_ 仍 \_ 連接**
</dt> <dd> <dl> <dt>

764 (0x2FC) 
</dt> <dt>



指定的中斷向量仍在連線。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**\_等候 \_ \_ OPLOCK 時發生錯誤**
</dt> <dd> <dl> <dt>

765 (0x2FD) 
</dt> <dt>



作業已封鎖等候 oplock。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**\_處理錯誤 DBG \_ 例外 \_ 狀況**
</dt> <dd> <dl> <dt>

766 (0x2FE) 
</dt> <dt>



偵錯工具處理的例外狀況。


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**錯誤 \_ DBG \_ 繼續**
</dt> <dd> <dl> <dt>

767 (0x2FF) 
</dt> <dt>



偵錯工具繼續。


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**錯誤 \_ 回呼 \_ POP \_ 堆疊**
</dt> <dd> <dl> <dt>

768 (0x300) 
</dt> <dt>



使用者模式回呼中發生例外狀況，應移除核心回呼框架。


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_ \_ 停用錯誤壓縮**
</dt> <dd> <dl> <dt>

769 (0x301) 
</dt> <dt>



此磁片區的壓縮已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**錯誤 \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302) 
</dt> <dt>



資料提供者無法透過結果集向後提取。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**錯誤 \_ CANTSCROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303) 
</dt> <dt>



資料提供者無法在結果集中向後滾動。


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**錯誤 \_ ROWSNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304) 
</dt> <dt>



資料提供者需要先釋出先前提取的資料，然後再要求更多資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**錯誤 \_ \_ 存取子 \_ 旗標錯誤**
</dt> <dd> <dl> <dt>

773 (0x305) 
</dt> <dt>



資料提供者無法解讀存取子中的資料行系結所設定的旗標。


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_遇到錯誤錯誤 \_**
</dt> <dd> <dl> <dt>

774 (0x306) 
</dt> <dt>



處理要求時發生一或多個錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**錯誤 \_ 無法 \_ 支援**
</dt> <dd> <dl> <dt>

775 (0x307) 
</dt> <dt>



執行不能執行要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**錯誤 \_ 要求 \_ \_ \_ 順序錯誤**
</dt> <dd> <dl> <dt>

776 (0x308) 
</dt> <dt>



元件的用戶端要求的作業在元件實例的狀態中是不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**錯誤 \_ 版本 \_ 剖析 \_ 錯誤**
</dt> <dd> <dl> <dt>

777 (0x309) 
</dt> <dt>



無法剖析版本號碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**錯誤 \_ BADSTARTPOSITION**
</dt> <dd> <dl> <dt>

778 (0x30A) 
</dt> <dt>



反覆運算器的開始位置無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**錯誤 \_ 記憶體 \_ 硬體**
</dt> <dd> <dl> <dt>

779 (0x30B) 
</dt> <dt>



硬體回報了無法修正的記憶體錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**\_ \_ 停用磁片修復錯誤 \_**
</dt> <dd> <dl> <dt>

780 (0x30C) 
</dt> <dt>



嘗試的作業必須啟用自我修復。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**\_資源不足 \_ \_ ，無法用於 \_ 指定的 \_ 共用 \_ 區段 \_ 大小**
</dt> <dd> <dl> <dt>

781 (0x30D) 
</dt> <dt>



在配置會話記憶體時，桌面堆積發生錯誤。 系統事件記錄檔中有更多的資訊。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**錯誤 \_ 系統 \_ >POWERSTATE \_ 轉換**
</dt> <dd> <dl> <dt>

782 (0x30E) 
</dt> <dt>



系統電源狀態是從 %2 轉換到 %3。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR \_ SYSTEM \_ >POWERSTATE \_ 複雜 \_ 轉換**
</dt> <dd> <dl> <dt>

783 (0x30F) 
</dt> <dt>



系統電源狀態是從 %2 轉換到 %3，但可以輸入 %4。


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**錯誤 \_ MCA \_ 例外狀況**
</dt> <dd> <dl> <dt>

784 (0x310) 
</dt> <dt>



因為 MCA，所以執行緒會因為 mca 例外狀況而分派。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_ \_ \_ 依原則的存取審核錯誤 \_**
</dt> <dd> <dl> <dt>

785 (0x311) 
</dt> <dt>



原則規則 %2 會監視 %1 的存取權。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**錯誤 \_ 存取 \_ 已停用 \_ \_ \_ \_ 原則的 \_ 不安全 UI**
</dt> <dd> <dl> <dt>

786 (0x312) 
</dt> <dt>



原則規則 %2 的系統管理員已限制存取 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**錯誤 \_ 放棄 \_ HIBERFILE**
</dt> <dd> <dl> <dt>

787 (0x313) 
</dt> <dt>



有效的休眠檔已失效，應予以放棄。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 網路 \_ 連線中斷時發生錯誤**
</dt> <dd> <dl> <dt>

788 (0x314) 
</dt> <dt>



{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。 發生此錯誤的原因可能是網路連線問題。 請嘗試將此檔案儲存在其他位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 網路 \_ 伺服器 \_ 錯誤遺失錯誤**
</dt> <dd> <dl> <dt>

789 (0x315) 
</dt> <dt>



{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。 檔案所在的伺服器傳回此錯誤。 請嘗試將此檔案儲存在其他位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**\_ \_ WRITEBEHIND \_ 資料 \_ 本機 \_ 磁片 \_ 錯誤遺失**
</dt> <dd> <dl> <dt>

790 (0x316) 
</dt> <dt>



{延遲寫入失敗}Windows 無法儲存檔案% hs; 的所有資料資料已遺失。 如果裝置已移除或媒體受到寫入保護，可能會導致此錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**錯誤 \_ 的 \_ MCFG \_ 資料表**
</dt> <dd> <dl> <dt>

791 (0x317) 
</dt> <dt>



此裝置所需的資源與 MCFG 資料表發生衝突。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**重新 \_ \_ 導向磁片修復 \_ 錯誤**
</dt> <dd> <dl> <dt>

792 (0x318) 
</dt> <dt>



磁片區修復在上線時無法執行。 請排程讓磁片區離線，讓它可以修復。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**錯誤 \_ 磁片 \_ 修復 \_ 失敗**
</dt> <dd> <dl> <dt>

793 (0x319) 
</dt> <dt>



磁片區修復失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**錯誤損毀 \_ \_ 記錄檔 \_ OVERFULL**
</dt> <dd> <dl> <dt>

794 (0x31A) 
</dt> <dt>



其中一個磁片區損毀記錄已滿。 可能偵測到的進一步損毀不會記錄下來。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**錯誤 \_ \_ \_ 損毀記錄損毀**
</dt> <dd> <dl> <dt>

795 (0x31B) 
</dt> <dt>



其中一個磁片區損毀記錄在內部損毀，需要重新建立。 磁片區可能包含未偵測到的損毀，且必須進行掃描。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**錯誤損毀 \_ \_ 記錄檔 \_ 無法使用**
</dt> <dd> <dl> <dt>

796 (0x31C) 
</dt> <dt>



其中一個磁片區損毀記錄無法用於操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**\_ \_ \_ 已刪除完整記錄 \_ 檔時發生錯誤**
</dt> <dd> <dl> <dt>

797 (0x31D) 
</dt> <dt>



其中一個磁片區損毀記錄檔已刪除，但仍有損毀記錄。 磁片區包含偵測到的損毀，且必須進行掃描。


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**已清除錯誤損毀 \_ \_ 記錄檔 \_**
</dt> <dd> <dl> <dt>

798 (0x31E) 
</dt> <dt>



Chkdsk 已清除其中一個磁片區損毀記錄，不再包含真正損毀的記錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**錯誤的 \_ 孤立 \_ 名稱已 \_ 用盡**
</dt> <dd> <dl> <dt>

799 (0x31F) 
</dt> <dt>



磁片區上有孤立的檔案，但無法復原，因為無法在復原目錄中建立更新的名稱。 檔案必須從修復目錄移動。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**錯誤 \_ OPLOCK \_ 切換 \_ 至 \_ 新的 \_ 控制碼**
</dt> <dd> <dl> <dt>

800 (0x320) 
</dt> <dt>



與此控制碼相關聯的 oplock 現在與不同的控制碼相關聯。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**錯誤 \_ 無法 \_ 授與 \_ 要求的 \_ OPLOCK**
</dt> <dd> <dl> <dt>

801 (0x321) 
</dt> <dt>



無法授與所要求層級的 oplock。 較低層級的 oplock 可能可供使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**錯誤 \_ 無法 \_ 中斷 \_ OPLOCK**
</dt> <dd> <dl> <dt>

802 (0x322) 
</dt> <dt>



作業未順利完成，因為它會導致 oplock 中斷。 呼叫端要求現有的 oplock 不會中斷。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**錯誤 \_ OPLOCK \_ 控制碼 \_ 已關閉**
</dt> <dd> <dl> <dt>

803 (0x323) 
</dt> <dt>



與此 oplock 相關聯的控制碼已關閉。 Oplock 現在已中斷。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**錯誤 \_ 無 \_ ACE \_ 條件**
</dt> <dd> <dl> <dt>

804 (0x324) 
</dt> <dt>



指定的存取控制專案 (ACE) 不包含條件。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**錯誤 \_ 不正確 \_ ACE \_ 條件**
</dt> <dd> <dl> <dt>

805 (0x325) 
</dt> <dt>



指定的存取控制專案 (ACE) 包含不正確條件。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**已 \_ 撤銷錯誤檔 \_ 控制碼 \_**
</dt> <dd> <dl> <dt>

806 (0x326) 
</dt> <dt>



已撤銷對指定檔案控制代碼的存取權。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_ \_ \_ 不同 \_ 基底的錯誤影像**
</dt> <dd> <dl> <dt>

807 (0x327) 
</dt> <dt>



影像檔案的對應位置與影像檔案中指定的位址不同，但仍會在映射上自動執行修正。


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**\_ \_ 拒絕存取 EA 的錯誤 \_**
</dt> <dd> <dl> <dt>

994 (0x3E2) 
</dt> <dt>



拒絕存取擴充屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**錯誤作業已 \_ \_ 中止**
</dt> <dd> <dl> <dt>

995 (0x3E3) 
</dt> <dt>



I/o 作業因為執行緒結束或應用程式要求而中止。


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**錯誤 \_ IO \_ 不完整**
</dt> <dd> <dl> <dt>

996 (0x3E4) 
</dt> <dt>



重迭的 i/o 事件未處於已發出信號的狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**錯誤 \_ IO \_ 暫止**
</dt> <dd> <dl> <dt>

997 (0x3E5) 
</dt> <dt>



重迭的 i/o 作業正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**錯誤 \_ NOACCESS**
</dt> <dd> <dl> <dt>

998 (0x3E6) 
</dt> <dt>



存取記憶體位置無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**錯誤 \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7) 
</dt> <dt>



執行 inpage 操作時發生錯誤。


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

 

 
