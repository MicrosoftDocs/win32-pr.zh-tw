---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼0-499，適用于開發人員。
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: '系統錯誤碼 (0-499)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: a9eddec2baf098f62bb1c0ad88e632360807e7f3fd0ea045f2565587f13e93a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405647"
---
# <a name="system-error-codes-0-499"></a>系統錯誤碼 (0-499) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[[錯誤碼](system-error-codes.md)] 頁面上有資源清單。

下列清單說明 [系統錯誤碼](system-error-codes.md) (錯誤0到 499) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**錯誤 \_ 成功**
</dt> <dd> <dl> <dt>

0 (0x0) 
</dt> <dt>



作業已成功完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**錯誤不正確函式 \_ \_**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



不正確的函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_ \_ \_ 找不到錯誤檔案**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



系統找不到指定的檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_ \_ 找不到錯誤路徑 \_**
</dt> <dd> <dl> <dt>

3 (0x3) 
</dt> <dt>



系統找不到所指定的路徑。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**錯誤 \_ 太 \_ 多 \_ 開啟 \_ 的檔案**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



系統無法開啟檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**\_拒絕存取 \_ 錯誤**
</dt> <dd> <dl> <dt>

5 (0x5) 
</dt> <dt>



存取遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**
</dt> <dd> <dl> <dt>

6 (0x6) 
</dt> <dt>



控制代碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**錯誤 \_ 領域 \_ 垃圾桶**
</dt> <dd> <dl> <dt>

7 (0x7) 
</dt> <dt>



儲存體控制區塊已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



沒有足夠的記憶體資源可用來處理此命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**錯誤 \_ 不正確 \_ 區塊**
</dt> <dd> <dl> <dt>

9 (0x9) 
</dt> <dt>



儲存體控制區塊位址無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**錯誤 \_ 的 \_ 環境錯誤**
</dt> <dd> <dl> <dt>

10 (0xA) 
</dt> <dt>



環境不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**錯誤 \_ \_ 格式錯誤**
</dt> <dd> <dl> <dt>

11 (0xB) 
</dt> <dt>



嘗試載入了格式不正確的程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**\_存取不正確錯誤 \_**
</dt> <dd> <dl> <dt>

12 (0xC) 
</dt> <dt>



存取程式碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**錯誤 \_ 不正確 \_ 資料**
</dt> <dd> <dl> <dt>

13 (0xD) 
</dt> <dt>



資料無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**錯誤 \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE) 
</dt> <dt>



沒有足夠的儲存空間可用來完成此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**錯誤 \_ 不正確 \_ 磁片磁碟機**
</dt> <dd> <dl> <dt>

15 (0xF) 
</dt> <dt>



系統找不到指定的磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**錯誤的 \_ 當前 \_ 目錄**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



無法移除目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**錯誤 \_ 不是 \_ 相同的 \_ 裝置**
</dt> <dd> <dl> <dt>

17 (0x11) 
</dt> <dt>



系統無法將檔案移至不同的磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**錯誤 \_ 的 \_ 檔案 \_**
</dt> <dd> <dl> <dt>

18 (0x12) 
</dt> <dt>



沒有其他檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**錯誤 \_ 寫入 \_ 保護**
</dt> <dd> <dl> <dt>

19 (0x13) 
</dt> <dt>



媒體受到寫入保護。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**錯誤 \_ 錯誤 \_ 單位**
</dt> <dd> <dl> <dt>

20 (0x14) 
</dt> <dt>



系統找不到指定的裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**錯誤 \_ 未 \_ 就緒**
</dt> <dd> <dl> <dt>

21 (0x15) 
</dt> <dt>



裝置未就緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**錯誤錯誤的 \_ \_ 命令**
</dt> <dd> <dl> <dt>

22 (0x16) 
</dt> <dt>



裝置無法辨識命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**錯誤 \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17) 
</dt> <dt>



資料錯誤 (迴圈冗余檢查) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**錯誤 \_ \_ 長度錯誤**
</dt> <dd> <dl> <dt>

24 (0x18) 
</dt> <dt>



程式發出命令，但命令長度不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**錯誤 \_ 搜尋**
</dt> <dd> <dl> <dt>

25 (0x19) 
</dt> <dt>



磁片磁碟機在磁片上找不到特定的區域或曲目。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**錯誤 \_ 非 \_ DOS \_ 磁片**
</dt> <dd> <dl> <dt>

26 (0x1A) 
</dt> <dt>



無法存取指定的磁片或磁片。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ 找不到錯誤磁區 \_**
</dt> <dd> <dl> <dt>

27 (0x1B) 
</dt> <dt>



磁片磁碟機找不到要求的磁區。


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**錯誤 \_ 出 \_ \_ 紙**
</dt> <dd> <dl> <dt>

28 (0x1C) 
</dt> <dt>



印表機紙張用完。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**錯誤 \_ 寫入 \_ 錯誤**
</dt> <dd> <dl> <dt>

29 (Bugcheck 0x1d) 
</dt> <dt>



系統無法寫入指定的裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**錯誤 \_ 讀取 \_ 錯誤**
</dt> <dd> <dl> <dt>

30 (0x1E) 
</dt> <dt>



系統無法從指定的裝置讀取。


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**錯誤 \_ GEN \_ 失敗**
</dt> <dd> <dl> <dt>

31 (0x1F) 
</dt> <dt>



連接至系統的裝置無法運作。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**錯誤 \_ 共用 \_ 違規**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



由於已有另一個處理序正在使用該檔案，所以此處理序無法存取該檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**錯誤 \_ 鎖定 \_ 違規**
</dt> <dd> <dl> <dt>

33 (0x21) 
</dt> <dt>



處理序無法存取檔案，因為其他處理序鎖定了該檔案的一部分。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**錯誤 \_ 的 \_ 磁片**
</dt> <dd> <dl> <dt>

34 (0x22) 
</dt> <dt>



磁片磁碟機中有錯誤的磁片。 插入 %2 (磁片區序號： %3) 到磁片磁碟機 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**\_超出共用 \_ 緩衝區時發生錯誤 \_**
</dt> <dd> <dl> <dt>

36 (0x24) 
</dt> <dt>



開啟太多檔案進行共用。


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**錯誤 \_ 處理 \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26) 
</dt> <dt>



已到達檔案結尾。


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**錯誤 \_ 處理 \_ 磁片已 \_ 滿**
</dt> <dd> <dl> <dt>

39 (0x27) 
</dt> <dt>



磁碟已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**\_不 \_ 支援的錯誤**
</dt> <dd> <dl> <dt>

50 (0x32) 
</dt> <dt>



不支援此要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**錯誤 \_ REM \_ 非 \_ 清單**
</dt> <dd> <dl> <dt>

51 (0x33) 
</dt> <dt>



Windows 找不到網路路徑。 請確認網路路徑是否正確，且目的地電腦未忙碌或已關閉。 如果 Windows 仍找不到網路路徑，請洽詢您的網路系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**錯誤 \_ DUP \_ 名稱**
</dt> <dd> <dl> <dt>

52 (0x34) 
</dt> <dt>



您未連線，因為網路上有重複的名稱。 如果要加入網域，請移至主控台中的 [系統] 變更電腦名稱稱，然後再試一次。 如果加入工作組，請選擇另一個工作組名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**錯誤 \_ 錯誤 \_ NETPATH**
</dt> <dd> <dl> <dt>

53 (0x35) 
</dt> <dt>



找不到網路路徑。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**\_網路 \_ 忙碌時發生錯誤**
</dt> <dd> <dl> <dt>

54 (0x36) 
</dt> <dt>



網路忙碌中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**錯誤 \_ 開發人員 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

55 (0x37) 
</dt> <dt>



無法再使用指定的網路資源或裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**錯誤 \_ 太 \_ 多 \_**
</dt> <dd> <dl> <dt>

56 (0x38) 
</dt> <dt>



已達到網路 BIOS 命令的限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**錯誤 \_ ADAP \_ HDW \_ 錯誤**
</dt> <dd> <dl> <dt>

57 (0x39) 
</dt> <dt>



發生網路介面卡硬體錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**錯誤 \_ 的 \_ NET \_ RESP**
</dt> <dd> <dl> <dt>

58 (0x3A) 
</dt> <dt>



指定的伺服器無法執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**\_UNEXP \_ NET \_ ERR 時發生錯誤**
</dt> <dd> <dl> <dt>

59 (0x3B) 
</dt> <dt>



發生未預期的網路錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**錯誤錯誤的 \_ \_ REM \_ ADAP**
</dt> <dd> <dl> <dt>

60 (0x3C) 
</dt> <dt>



遠端介面卡不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**\_PRINTQ \_ FULL 時發生錯誤**
</dt> <dd> <dl> <dt>

61 (0x3D) 
</dt> <dt>



印表機佇列已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**錯誤的多工 \_ \_ 緩衝處理 \_ 空間**
</dt> <dd> <dl> <dt>

62 (0x3E) 
</dt> <dt>



伺服器上無法使用儲存等候列印之檔案的空間。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**錯誤 \_ 列印已 \_ 取消**
</dt> <dd> <dl> <dt>

63 (0x3F) 
</dt> <dt>



您等候列印的檔案已刪除。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**\_ \_ 已刪除錯誤的錯誤**
</dt> <dd> <dl> <dt>

64 (0x40) 
</dt> <dt>



指定的網路名稱不再可用。


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**\_拒絕網路 \_ 存取時發生錯誤 \_**
</dt> <dd> <dl> <dt>

65 (0x41 向) 
</dt> <dt>



網路存取遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**錯誤 \_ 的 \_ 開發 \_ 類型錯誤**
</dt> <dd> <dl> <dt>

66 (0x42) 
</dt> <dt>



網路資源類型不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**錯誤 \_ 的 \_ 網路 \_ 名稱錯誤**
</dt> <dd> <dl> <dt>

67 (0x43) 
</dt> <dt>



找不到網路名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**錯誤 \_ 太 \_ 多 \_ 名稱**
</dt> <dd> <dl> <dt>

68 (0x44) 
</dt> <dt>



已超過本機電腦網路介面卡的名稱限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**錯誤 \_ 太 \_ 多 \_ SES 之始**
</dt> <dd> <dl> <dt>

69 (0x45) 
</dt> <dt>



已超過網路 BIOS 會話限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**\_共用錯誤 \_ 暫停**
</dt> <dd> <dl> <dt>

70 (0x46) 
</dt> <dt>



遠端伺服器已暫停或正在啟動中。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**錯誤 \_ 需求 \_ 未 \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47) 
</dt> <dt>



目前無法再對此遠端電腦進行連線，因為電腦可以接受的連線數目已經過多。


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**錯誤 \_ REDIR \_ 暫停**
</dt> <dd> <dl> <dt>

72 (0x48) 
</dt> <dt>



指定的印表機或磁片裝置已暫停。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**錯誤檔案已 \_ \_ 存在**
</dt> <dd> <dl> <dt>

80 (0x50) 
</dt> <dt>



檔案存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**錯誤 \_ 無法 \_ 進行**
</dt> <dd> <dl> <dt>

82 (0x52) 
</dt> <dt>



無法建立目錄或檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**錯誤 \_ 失敗 \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53) 
</dt> <dt>



在 INT 24 上失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**\_結構錯誤 \_ \_**
</dt> <dd> <dl> <dt>

84 (0x54) 
</dt> <dt>



無法使用儲存體處理此要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**\_已 \_ 指派錯誤**
</dt> <dd> <dl> <dt>

85 (0x55) 
</dt> <dt>



本機裝置名稱已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**錯誤 \_ 不正確 \_ 密碼**
</dt> <dd> <dl> <dt>

86 (0x56) 
</dt> <dt>



指定的網路密碼不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**錯誤 \_ 不正確 \_ 參數**
</dt> <dd> <dl> <dt>

87 (0x57) 
</dt> <dt>



參數錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**錯誤 \_ 網路 \_ 寫入 \_ 錯誤**
</dt> <dd> <dl> <dt>

88 (0x58) 
</dt> <dt>



網路上發生寫入錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**錯誤 \_ 無 \_ 處理器 \_ 位置**
</dt> <dd> <dl> <dt>

89 (0x59) 
</dt> <dt>



系統目前無法啟動另一個進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**錯誤 \_ 太 \_ 多 \_ 信號**
</dt> <dd> <dl> <dt>

100 (0x64) 
</dt> <dt>



無法建立另一個系統信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**\_排除 \_ SEM \_ 已 \_ 擁有的錯誤**
</dt> <dd> <dl> <dt>

101 (0x65) 
</dt> <dt>



獨佔信號是由另一個進程所擁有。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**\_ \_ 設定的錯誤 \_ SEM**
</dt> <dd> <dl> <dt>

102 (0x66) 
</dt> <dt>



信號已設定且無法關閉。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**錯誤 \_ 太 \_ 多 \_ SEM \_ 要求**
</dt> <dd> <dl> <dt>

103 (0x67) 
</dt> <dt>



無法再次設定信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**插 \_ 斷 \_ \_ 時間無效 \_ 錯誤**
</dt> <dd> <dl> <dt>

104 (0x68) 
</dt> <dt>



無法在插斷時間要求獨佔的信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**\_SEM \_ 擁有者 \_ 壞掉時發生錯誤**
</dt> <dd> <dl> <dt>

105 (0x69) 
</dt> <dt>



此信號的先前擁有權已結束。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_SEM \_ 使用者 \_ 限制時發生錯誤**
</dt> <dd> <dl> <dt>

106 (0x6A) 
</dt> <dt>



插入磁片磁碟機 %1 的磁片。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**錯誤 \_ 磁片 \_ 變更**
</dt> <dd> <dl> <dt>

107 (0x6B) 
</dt> <dt>



程式已停止，因為未插入替代的磁片。


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**錯誤 \_ 磁片磁碟機已 \_ 鎖定**
</dt> <dd> <dl> <dt>

108 (0x6C) 
</dt> <dt>



磁片正在使用中，或已被其他進程鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**錯誤 \_ 中斷的 \_ 管道**
</dt> <dd> <dl> <dt>

109 (0x6D) 
</dt> <dt>



已結束管道。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**錯誤 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

110 (0x6E) 
</dt> <dt>



系統無法開啟指定的裝置或檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**錯誤 \_ 緩衝區 \_ 溢位**
</dt> <dd> <dl> <dt>

111 (0x6F) 
</dt> <dt>



檔案名稱太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**錯誤 \_ 磁片已 \_ 滿**
</dt> <dd> <dl> <dt>

112 (0x70) 
</dt> <dt>



磁碟的空間不足。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**\_沒有 \_ 其他 \_ 搜尋 \_ 控制碼的錯誤**
</dt> <dd> <dl> <dt>

113 (0x71) 
</dt> <dt>



沒有其他可用的內部檔案識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**錯誤 \_ 不正確 \_ 目標 \_ 控制碼**
</dt> <dd> <dl> <dt>

114 (0x72) 
</dt> <dt>



目標內部檔案識別碼不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**錯誤 \_ 不正確 \_ 類別**
</dt> <dd> <dl> <dt>

117 (0x75) 
</dt> <dt>



應用程式所進行的 IOCTL 呼叫不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**錯誤 \_ 不正確 \_ 驗證 \_ 參數**
</dt> <dd> <dl> <dt>

118 (0x76) 
</dt> <dt>



驗證寫切換參數值不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**錯誤 \_ 的 \_ 驅動程式 \_ 等級錯誤**
</dt> <dd> <dl> <dt>

119 (0x77) 
</dt> <dt>



系統不支援要求的命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**\_ \_ 未執行錯誤 \_ 呼叫**
</dt> <dd> <dl> <dt>

120 (0x78) 
</dt> <dt>



此系統不支援此功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**錯誤 \_ SEM \_ 超時**
</dt> <dd> <dl> <dt>

121 (0x79) 
</dt> <dt>



信號超時時間已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**\_緩衝區不足的錯誤 \_**
</dt> <dd> <dl> <dt>

122 (0x7A) 
</dt> <dt>



傳遞給系統呼叫的資料區域太小。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**錯誤 \_ 不正確 \_ 名稱**
</dt> <dd> <dl> <dt>

123 (0x7B) 
</dt> <dt>



檔案名、目錄名稱或磁片區標籤語法不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**錯誤 \_ 不正確 \_ 層級**
</dt> <dd> <dl> <dt>

124 (0x7C) 
</dt> <dt>



系統呼叫層級不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**錯誤 \_ 的 \_ 磁片區卷 \_ 標**
</dt> <dd> <dl> <dt>

125 (0x7D) 
</dt> <dt>



磁片沒有磁片區標籤。


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**\_ \_ 找不到錯誤 MOD \_**
</dt> <dd> <dl> <dt>

126 (0x7E) 
</dt> <dt>



找不到指定的模組。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**\_ \_ 找不到錯誤處理器 \_**
</dt> <dd> <dl> <dt>

127 (0x7F) 
</dt> <dt>



找不到指定的程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**錯誤 \_ 等候 \_ 沒有 \_ 子系**
</dt> <dd> <dl> <dt>

128 (0x80) 
</dt> <dt>



沒有任何子進程需要等候。


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**錯誤 \_ 子系 \_ 未 \_ 完成**
</dt> <dd> <dl> <dt>

129 (0x81) 
</dt> <dt>



%1 應用程式無法在 Win32 模式中執行。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**錯誤 \_ 直接 \_ 存取 \_ 控制碼**
</dt> <dd> <dl> <dt>

130 (0x82) 
</dt> <dt>



嘗試針對原始磁片 i/o 以外的作業，使用開啟磁碟分割的檔案控制代碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**錯誤 \_ 負 \_ 搜尋**
</dt> <dd> <dl> <dt>

131 (0x83) 
</dt> <dt>



嘗試在檔開頭之前移動檔案指標。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_ \_ 裝置上的錯誤搜尋 \_**
</dt> <dd> <dl> <dt>

132 (0x84) 
</dt> <dt>



無法在指定的裝置或檔案上設定檔案指標。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**錯誤 \_ 為 \_ 聯結 \_ 目標**
</dt> <dd> <dl> <dt>

133 (0x85) 
</dt> <dt>



JOIN 或 SUBST 命令無法用於包含先前已加入之磁片磁碟機的磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**\_已 \_ 加入錯誤**
</dt> <dd> <dl> <dt>

134 (0x86) 
</dt> <dt>



嘗試在已加入的磁片磁碟機上使用 JOIN 或 SUBST 命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**錯誤 \_ 為 \_ SUBSTED**
</dt> <dd> <dl> <dt>

135 (0x87) 
</dt> <dt>



嘗試在已替代的磁片磁碟機上使用 JOIN 或 SUBST 命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**錯誤 \_ 未 \_ 加入**
</dt> <dd> <dl> <dt>

136 (0x88) 
</dt> <dt>



系統嘗試刪除未聯結之磁片磁碟機的聯結。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**錯誤 \_ 未 \_ SUBSTED**
</dt> <dd> <dl> <dt>

137 (0x89) 
</dt> <dt>



系統嘗試刪除未替代之磁片磁碟機的替換。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**聯結 \_ 時發生 \_ 錯誤 \_**
</dt> <dd> <dl> <dt>

138 (0x8A) 
</dt> <dt>



系統嘗試將磁片磁碟機加入聯結磁片磁碟機上的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**\_將 SUBST 錯誤替代 \_ 為 \_ SUBST**
</dt> <dd> <dl> <dt>

139 (0x8B) 
</dt> <dt>



系統嘗試將磁片磁碟機替換成替代磁片磁碟機上的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**\_將錯誤加入 \_ 至 \_ SUBST**
</dt> <dd> <dl> <dt>

140 (0x8C) 
</dt> <dt>



系統嘗試將磁片磁碟機加入替代磁片磁碟機上的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**\_ \_ 要聯結的錯誤 SUBST \_**
</dt> <dd> <dl> <dt>

141 (0x8D) 
</dt> <dt>



系統嘗試將磁片磁碟機替代為已加入磁片磁碟機上的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**錯誤 \_ 忙碌 \_ 磁片磁碟機**
</dt> <dd> <dl> <dt>

142 (0x8E) 
</dt> <dt>



系統目前無法執行聯結或 SUBST。


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**錯誤 \_ 的 \_ 磁片磁碟機**
</dt> <dd> <dl> <dt>

143 (0x8F) 
</dt> <dt>



系統無法將磁片磁碟機加入或替代相同磁片磁碟機上的目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**錯誤 \_ 目錄 \_ 不是 \_ 根目錄**
</dt> <dd> <dl> <dt>

144 (0x90) 
</dt> <dt>



目錄不是根目錄的子目錄。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**錯誤 \_ 目錄 \_ 不是 \_ 空的**
</dt> <dd> <dl> <dt>

145 (0x91) 
</dt> <dt>



目錄不是空的。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**錯誤 \_ 是 \_ SUBST \_ 路徑**
</dt> <dd> <dl> <dt>

146 (0x92) 
</dt> <dt>



指定的路徑正在替代中使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**錯誤 \_ 為 \_ 聯結 \_ 路徑**
</dt> <dd> <dl> <dt>

147 (0x93) 
</dt> <dt>



沒有足夠的資源可用來處理此命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**錯誤 \_ 路徑 \_ 忙碌中**
</dt> <dd> <dl> <dt>

148 (0x94) 
</dt> <dt>



目前無法使用指定的路徑。


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**錯誤 \_ 為 \_ SUBST \_ 目標**
</dt> <dd> <dl> <dt>

149 (0x95) 
</dt> <dt>



嘗試加入或取代磁片磁碟機上的目錄是先前替代目標的磁片磁碟機。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**錯誤 \_ 系統 \_ 追蹤**
</dt> <dd> <dl> <dt>

150 (0x96) 
</dt> <dt>



未在 CONFIG.SYS 檔案中指定系統追蹤資訊，或不允許追蹤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**錯誤 \_ 不正確 \_ 事件 \_ 計數**
</dt> <dd> <dl> <dt>

151 (0x97) 
</dt> <dt>



DosMuxSemWait 的指定訊號事件數目不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**錯誤 \_ 太 \_ 多 \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98) 
</dt> <dt>



DosMuxSemWait 未執行;已設定過多的信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**錯誤 \_ \_ 清單 \_ 格式無效**
</dt> <dd> <dl> <dt>

153 (0x99) 
</dt> <dt>



DosMuxSemWait 清單不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**錯誤 \_ 標籤 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

154 (0x9A) 
</dt> <dt>



您輸入的磁片區標籤超過目的檔案系統的標籤字元限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**錯誤 \_ 太 \_ 多 \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B) 
</dt> <dt>



無法建立另一個執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**拒絕的錯誤 \_ 信號 \_**
</dt> <dd> <dl> <dt>

156 (0x9C) 
</dt> <dt>



收件者進程拒絕了信號。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**捨棄的錯誤 \_**
</dt> <dd> <dl> <dt>

157 (0x9D) 
</dt> <dt>



區段已經捨棄，無法鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**錯誤 \_ 未 \_ 鎖定**
</dt> <dd> <dl> <dt>

158 (0x9E) 
</dt> <dt>



區段已經解除鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**錯誤 \_ \_ THREADID \_ 位址錯誤**
</dt> <dd> <dl> <dt>

159 (0x9F) 
</dt> <dt>



執行緒識別碼的位址不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**錯誤 \_ 的 \_ 引數錯誤**
</dt> <dd> <dl> <dt>

160 (0xA0) 
</dt> <dt>



一或多個引數不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**錯誤 \_ \_ 路徑名稱錯誤**
</dt> <dd> <dl> <dt>

161 (0xA1) 
</dt> <dt>



指定的路徑無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**錯誤 \_ 信號 \_ 暫止**
</dt> <dd> <dl> <dt>

162 (0xA2) 
</dt> <dt>



信號已暫止。


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**已 \_ \_ 達到 THRDS 的錯誤最大值 \_**
</dt> <dd> <dl> <dt>

164 (0xA4) 
</dt> <dt>



無法在系統中建立其他執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**錯誤 \_ 鎖定 \_ 失敗**
</dt> <dd> <dl> <dt>

167 (0xA7) 
</dt> <dt>



無法鎖定檔案的區域。


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**錯誤 \_ 忙碌**
</dt> <dd> <dl> <dt>

170 (0xAA) 
</dt> <dt>



要求的資源正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**錯誤 \_ 裝置 \_ 支援 \_ \_ 進行中**
</dt> <dd> <dl> <dt>

171 (0xAB) 
</dt> <dt>



裝置的命令支援偵測正在進行中。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**錯誤 \_ 取消 \_ 違規**
</dt> <dd> <dl> <dt>

173 (0xAD) 
</dt> <dt>



提供的取消區域沒有未處理的鎖定要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**\_ \_ \_ 不 \_ 支援錯誤的不可部分完成鎖定**
</dt> <dd> <dl> <dt>

174 (0xAE) 
</dt> <dt>



檔案系統不支援對鎖定類型進行不可部分完成的變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**錯誤 \_ 不正確 \_ 區段 \_ 編號**
</dt> <dd> <dl> <dt>

180 (0xB4) 
</dt> <dt>



系統偵測到不正確的區段編號。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**錯誤 \_ 不正確 \_ 序數**
</dt> <dd> <dl> <dt>

182 (0xB6) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**錯誤 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

183 (0xB7) 
</dt> <dt>



無法建立檔案，該檔案已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**錯誤 \_ 不正確 \_ 旗標 \_ 編號**
</dt> <dd> <dl> <dt>

186 (0xBA) 
</dt> <dt>



傳遞的旗標不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**\_ \_ 找不到錯誤 SEM \_**
</dt> <dd> <dl> <dt>

187 (0xBB) 
</dt> <dt>



找不到指定的系統信號名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**\_ \_ 啟動 \_ CODESEG 時發生錯誤**
</dt> <dd> <dl> <dt>

188 (0xBC) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**錯誤 \_ 無效 \_ STACKSEG**
</dt> <dd> <dl> <dt>

189 (0xBD) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**錯誤 \_ 不正確 \_ MODULETYPE**
</dt> <dd> <dl> <dt>

190 (0xBE) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**錯誤 \_ 不正確 \_ EXE 簽 \_ 章**
</dt> <dd> <dl> <dt>

191 (0xBF) 
</dt> <dt>



無法在 Win32 模式中執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**錯誤 \_ EXE \_ 標示為 \_ 無效**
</dt> <dd> <dl> <dt>

192 (0xC0) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**錯誤 \_ 的 \_ EXE \_ 格式錯誤**
</dt> <dd> <dl> <dt>

193 (0xC1) 
</dt> <dt>



%1 不是有效的 Win32 應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**反復 \_ 資料的錯誤 \_ \_ 超過 \_ 64k**
</dt> <dd> <dl> <dt>

194 (0xC2) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**錯誤 \_ 無效 \_ MINALLOCSIZE**
</dt> <dd> <dl> <dt>

195 (0xC3) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**\_ \_ 從不正確 \_ \_ 環形 DYNLINK 錯誤**
</dt> <dd> <dl> <dt>

196 (0xC4) 
</dt> <dt>



作業系統無法執行此應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**\_ \_ 未啟用錯誤 \_ IOPL**
</dt> <dd> <dl> <dt>

197 (0xC5) 
</dt> <dt>



作業系統目前尚未設定為執行此應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**錯誤 \_ 無效 \_ SEGDPL**
</dt> <dd> <dl> <dt>

198 (0xC6) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**錯誤 \_ AUTODATASEG \_ 超過 \_ 64k**
</dt> <dd> <dl> <dt>

199 (0xC7) 
</dt> <dt>



作業系統無法執行此應用程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**錯誤 \_ RING2SEG \_ 必須 \_ \_ 可移動**
</dt> <dd> <dl> <dt>

200 (0xC8) 
</dt> <dt>



程式碼片段不能大於或等於64K。


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**\_RELOC \_ 鏈 \_ XEEDS \_ SEGLIM 時發生錯誤**
</dt> <dd> <dl> <dt>

201 (0xC9) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**\_ \_ \_ RELOC 鏈中的錯誤 INFLOOP \_**
</dt> <dd> <dl> <dt>

202 (元素 0xca) 
</dt> <dt>



作業系統無法執行 %1。


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**\_ \_ 找不到錯誤 ENVVAR \_**
</dt> <dd> <dl> <dt>

203 (0xCB) 
</dt> <dt>



系統找不到所輸入的環境選項。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**錯誤 \_ 未 \_ \_ 傳送信號**
</dt> <dd> <dl> <dt>

205 (0xCD) 
</dt> <dt>



命令子樹中沒有進程有信號處理常式。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**錯誤 \_ 檔案名 \_ EXCED \_ 範圍**
</dt> <dd> <dl> <dt>

206 (0xCE) 
</dt> <dt>



檔案名或副檔名太長。


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**\_RING2 \_ \_ 使用中堆疊 \_ 時發生錯誤**
</dt> <dd> <dl> <dt>

207 (0xCF) 
</dt> <dt>



環形2堆疊正在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**錯誤 \_ 中繼 \_ 擴充 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

208 (0xD0) 
</dt> <dt>



通用檔案名字元 \* 或？的輸入不正確，或指定了太多的通用檔案名字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**錯誤 \_ 不正確 \_ 信號 \_ 號碼**
</dt> <dd> <dl> <dt>

209 (0xD1) 
</dt> <dt>



張貼的信號不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**錯誤 \_ 執行緒 \_ 1 \_ 非使用中**
</dt> <dd> <dl> <dt>

210 (0xD2) 
</dt> <dt>



無法設定信號處理常式。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**\_鎖定錯誤**
</dt> <dd> <dl> <dt>

212 (0xD4) 
</dt> <dt>



區段已鎖定，無法重新配置。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**錯誤 \_ 太 \_ 多 \_ 模組**
</dt> <dd> <dl> <dt>

214 (0xD6) 
</dt> <dt>



有太多動態連結模組附加到這個程式或動態連結模組。


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_ \_ 不 \_ 允許錯誤的嵌套**
</dt> <dd> <dl> <dt>

215 (0xD7) 
</dt> <dt>



無法將呼叫嵌套至 LoadModule。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**錯誤 \_ EXE \_ 電腦 \_ 類型 \_ 不相符**
</dt> <dd> <dl> <dt>

216 (0xD8) 
</dt> <dt>



此版本的 %1 與您正在執行的 Windows 版本不相容。 檢查電腦的系統資訊，然後洽詢軟體發行者。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**錯誤 \_ EXE \_ 無法 \_ 修改 \_ 帶正負號的 \_ 二進位檔**
</dt> <dd> <dl> <dt>

217 (0xD9) 
</dt> <dt>



影像檔案 %1 已簽署，無法修改。


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**錯誤 \_ EXE \_ 無法 \_ 修改 \_ 強式 \_ 帶正負 \_ 號的二進位檔**
</dt> <dd> <dl> <dt>

218 (0xDA) 
</dt> <dt>



影像檔案 %1 經過強式簽署，無法修改。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**錯誤 \_ 檔案 \_ 簽 \_ 出**
</dt> <dd> <dl> <dt>

220 (0xDC) 
</dt> <dt>



此檔案已簽出或鎖定，可供其他使用者編輯。


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_需要錯誤簽出 \_**
</dt> <dd> <dl> <dt>

221 (0xDD) 
</dt> <dt>



您必須先簽出檔案，然後再儲存變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**錯誤 \_ 錯誤 \_ 檔 \_ 類型**
</dt> <dd> <dl> <dt>

222 (0xDE) 
</dt> <dt>



已封鎖要儲存或抓取的檔案類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**錯誤 \_ 檔案 \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

223 (0xDF) 
</dt> <dt>



檔案大小超過允許的限制，因此無法儲存。


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_需要驗證錯誤表單 \_ \_**
</dt> <dd> <dl> <dt>

224 (0xE0) 
</dt> <dt>



拒絕存取。 在此位置開啟檔案之前，您必須先將網站新增至 [信任的網站] 清單、流覽至網站，然後選取要自動登入的選項。


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**\_受病毒 \_ 感染的錯誤**
</dt> <dd> <dl> <dt>

225 (0xE1) 
</dt> <dt>



因為檔案包含病毒或潛在的垃圾軟體，所以操作未順利完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**\_已刪除病毒的錯誤 \_**
</dt> <dd> <dl> <dt>

226 (0xE2) 
</dt> <dt>



此檔案包含病毒或潛在的垃圾軟體，無法開啟。 由於這種病毒或潛在的垃圾軟體的本質，檔案已從這個位置移除。


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**錯誤 \_ 輸送 \_ 區域**
</dt> <dd> <dl> <dt>

229 (0xE5) 
</dt> <dt>



管道為本機。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**錯誤的 \_ 無效 \_ 管道**
</dt> <dd> <dl> <dt>

230 (0xE6) 
</dt> <dt>



管道狀態無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**錯誤 \_ 管道 \_ 忙碌中**
</dt> <dd> <dl> <dt>

231 (0xE7) 
</dt> <dt>



所有管道實例都忙碌中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**錯誤 \_ 的 \_ 資料**
</dt> <dd> <dl> <dt>

232 (0xE8) 
</dt> <dt>



正在關閉管道。


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**錯誤 \_ 管道 \_ 未 \_ 連接**
</dt> <dd> <dl> <dt>

233 (0xE9) 
</dt> <dt>



管道的另一端沒有進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**錯誤 \_ 的 \_ 資料**
</dt> <dd> <dl> <dt>

234 (0xEA) 
</dt> <dt>



有更多可用的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**\_VC \_ 中斷連線時發生錯誤**
</dt> <dd> <dl> <dt>

240 (0xF0) 
</dt> <dt>



會話已取消。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**錯誤 \_ 不正確 \_ EA \_ 名稱**
</dt> <dd> <dl> <dt>

254 (0xFE) 
</dt> <dt>



指定的擴充屬性名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**錯誤 \_ EA \_ 清單 \_ 不一致**
</dt> <dd> <dl> <dt>

255 (0xFF) 
</dt> <dt>



擴充屬性不一致。


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**等候 \_ 超時**
</dt> <dd> <dl> <dt>

258 (0x102) 
</dt> <dt>



等候作業逾時。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_沒有 \_ 其他 \_ 專案的錯誤**
</dt> <dd> <dl> <dt>

259 (0x103) 
</dt> <dt>



沒有其他可用的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_無法 \_ 複製錯誤**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



無法使用複製函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**錯誤 \_ 目錄**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



目錄名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**錯誤 \_ EAS \_ 無法 \_ 適用**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



擴充屬性不符合緩衝區。


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**錯誤 \_ EA \_ 檔案 \_ 已損毀**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



裝載的檔案系統上的擴充屬性檔已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**錯誤 \_ EA \_ 資料表已 \_ 滿**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



擴充屬性資料表檔案已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**\_不正確 \_ EA \_ 控制碼錯誤**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



指定的擴充屬性控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**\_ \_ 不 \_ 支援的錯誤 EAS**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



裝載的檔案系統不支援擴充屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**錯誤 \_ 非 \_ 擁有者**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



嘗試釋放不是由呼叫端所擁有的 mutex。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**錯誤 \_ 太 \_ 多 \_ 貼文**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



對信號發出太多貼文。


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**錯誤 \_ 部分 \_ 複製**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



只有部分的 ReadProcessMemory 或 WriteProcessMemory 要求已完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**\_ \_ 未 \_ 授與錯誤 OPLOCK**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Oplock 要求遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**\_不正確 \_ OPLOCK \_ 通訊協定錯誤**
</dt> <dd> <dl> <dt>

301 (0x12D) 
</dt> <dt>



系統收到不正確 oplock 通知。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**錯誤 \_ 磁片 \_ 太過 \_ 分散**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



磁片區太過分散，無法完成此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**\_刪除 \_ 暫止錯誤**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



無法開啟檔案，因為正在刪除該檔案。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**\_ \_ 與 \_ 全域 \_ 簡短名稱登錄 \_ \_ \_ 設定不相容的錯誤**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



因為全域登錄設定的緣故，所以可能不會變更這個磁片區的簡短名稱設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_ \_ \_ 未 \_ \_ 在磁片區上啟用錯誤簡短名稱 \_**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



此磁片區未啟用簡短名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**錯誤 \_ 安全性 \_ 資料流程 \_ 不 \_ 一致**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



指定磁片區的安全性資料流程處於不一致的狀態。 請在磁片區上執行 CHKDSK。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**\_不正確 \_ 鎖定 \_ 範圍錯誤**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



因為不正確位元組範圍，所以無法處理要求的檔案鎖定作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**錯誤 \_ 映射 \_ 子系統 \_ 不 \_ 存在**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



支援映射類型所需的子系統不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**\_ \_ \_ 已定義錯誤通知 \_ GUID**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



指定的檔案已經有與其相關聯的通知 GUID。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**錯誤 \_ 不正確 \_ 例外狀況 \_ 處理常式**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



偵測到不正確例外狀況處理常式常式。


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**錯誤的 \_ 重複 \_ 許可權**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



為權杖指定了重複的許可權。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**錯誤 \_ 未 \_ 處理任何範圍 \_**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



無法處理指定操作的範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**\_系統檔案不 \_ 允許錯誤 \_ \_ \_**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



不允許在檔案系統內部檔案上執行操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**錯誤 \_ 磁片 \_ 資源已 \_ 用盡**
</dt> <dd> <dl> <dt>

314 (0x13A) 
</dt> <dt>



此磁片的實體資源已用盡。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**錯誤 \_ 不正確 \_ 權杖**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



代表資料的權杖無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**\_ \_ \_ 不支援的錯誤裝置功能 \_**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



裝置不支援命令功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**錯誤 \_ MR \_ 中間找 \_ 不 \_ 到**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



系統在 %2 的訊息檔中找不到訊息編號 0x %1 的郵件內文。


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ \_ 找不到錯誤範圍 \_**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



找不到指定的範圍。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**錯誤 \_ 未定義 \_ 範圍**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



目的電腦上未定義指定的集中存取原則。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**錯誤 \_ 不正確 \_ 端點**
</dt> <dd> <dl> <dt>

320 (0x140) 
</dt> <dt>



從 Active Directory 取得的集中存取原則無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**錯誤 \_ 裝置 \_ 無法連線**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



無法連線到裝置。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**錯誤 \_ 裝置 \_ 沒有 \_ 資源**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



目標裝置的資源不足，無法完成操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**錯誤 \_ 資料總和 \_ 檢查碼 \_ 錯誤**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



發生資料完整性總和檢查碼錯誤。 檔案資料流程中的資料已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**錯誤 \_ 混合的 \_ 核心 \_ EA \_ 操作**
</dt> <dd> <dl> <dt>

324 (0x144) 
</dt> <dt>



在相同的作業中，嘗試修改核心和一般擴充屬性 (EA) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_ \_ \_ \_ 不 \_ 支援錯誤檔層級修剪**
</dt> <dd> <dl> <dt>

326 (0x146) 
</dt> <dt>



裝置不支援檔案層級修剪。


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**錯誤 \_ 位移 \_ 對齊 \_ 違規**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



命令指定的資料位移與裝置的資料細微性/對齊方式不一致。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_ \_ \_ \_ 參數清單中的無效 \_ 欄位**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



命令在其參數清單中指定了不正確欄位。


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_ \_ \_ 正在進行錯誤作業**
</dt> <dd> <dl> <dt>

329 (0x149) 
</dt> <dt>



目前正在與裝置進行操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**錯誤錯誤的 \_ \_ 裝置 \_ 路徑**
</dt> <dd> <dl> <dt>

330 (0x14A) 
</dt> <dt>



嘗試透過目標裝置的無效路徑來傳送命令。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**錯誤 \_ 太 \_ 多 \_ 描述項**
</dt> <dd> <dl> <dt>

331 (0x14B) 
</dt> <dt>



命令指定了超過裝置所支援之最大值的一些描述項。


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**\_ \_ 停用清除資料的錯誤 \_**
</dt> <dd> <dl> <dt>

332 (0x14C) 
</dt> <dt>



指定的檔案上已停用清除。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**錯誤 \_ 不是 \_ 重複的 \_ 儲存體**
</dt> <dd> <dl> <dt>

333 (0x14D) 
</dt> <dt>



存放裝置不提供冗余。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_ \_ \_ 不支援錯誤的常駐檔 \_**
</dt> <dd> <dl> <dt>

334 (0x14E) 
</dt> <dt>



常駐檔案不支援操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**\_ \_ \_ 不支援錯誤壓縮檔案 \_**
</dt> <dd> <dl> <dt>

335 (0x14F) 
</dt> <dt>



壓縮檔案不支援操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_ \_ 不支援錯誤 \_ 目錄**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



目錄不支援操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**\_無法 \_ \_ 從複製讀取 \_ 錯誤**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



無法讀取指定的要求資料複本。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**錯誤 \_ 失敗 \_ NOACTION \_ 重新開機**
</dt> <dd> <dl> <dt>

350 (0x15E) 
</dt> <dt>



需要系統重新開機時，不會採取任何動作。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**錯誤 \_ 失敗 \_ 關閉**
</dt> <dd> <dl> <dt>

351 (0x15F) 
</dt> <dt>



關機操作失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**錯誤 \_ \_ 重新開機失敗**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



重新開機作業失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**\_達到的 \_ 會話數上限 \_**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



已達到會話的數目上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**錯誤 \_ 執行緒 \_ 模式 \_ 已經是 \_ 背景**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



執行緒已處於背景處理模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**錯誤 \_ 執行緒 \_ 模式 \_ 不是 \_ 背景**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



執行緒不是處於背景處理模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**錯誤 \_ 進程 \_ 模式 \_ 已經是 \_ 背景**
</dt> <dd> <dl> <dt>

402 (0x192) 
</dt> <dt>



進程已經處於背景處理模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**錯誤 \_ 進程 \_ 模式 \_ 不是 \_ 背景**
</dt> <dd> <dl> <dt>

403 (0x193) 
</dt> <dt>



進程並非處於背景處理模式。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**錯誤 \_ 不正確 \_ 位址**
</dt> <dd> <dl> <dt>

487 (0x1E7) 
</dt> <dt>



嘗試存取不正確位址。


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winerror.h (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




