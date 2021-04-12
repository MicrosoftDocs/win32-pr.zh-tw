---
title: 'TBS 傳回碼 (Tbs) '
description: TBS 會使用下列程式碼來指出函式呼叫的結果。
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384701"
---
# <a name="tbs-return-codes"></a>TBS 傳回碼

TBS 會使用下列程式碼來指出函式呼叫的結果。



| 常數/值                                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**Tb \_SUCCESS**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | 此函數已成功。<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**Tb \_E \_ INTERNAL \_ ERROR**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | 發生內部軟體錯誤。<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**Tb \_E \_ 錯誤的 \_ 參數**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | 一或多個參數值無效。<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**Tb \_E \_ 不正確 \_ 輸出 \_ 指標**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | 指定的輸出指標不正確。<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**Tb \_E \_ 不正確 \_ 內容**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | 指定的內容控制碼未參考有效的內容。<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**Tb \_E \_ \_ 緩衝區**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | 指定的輸出緩衝區太小。<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**Tb \_E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | 與 TPM 通訊時發生錯誤。<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**Tb \_電子 \_ 不正確 \_ 內容 \_ 參數**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | 嘗試建立 TB 內容時，傳遞了不正確內容參數。<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt> </dl>                | TBS 服務未執行，因此無法啟動。<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**Tb \_電子 (0x80284009) 的 \_ \_ 多 \_ tb \_**</dt>內容 <dt>2150121481</dt> </dl>         | 因為有太多開啟的內容，所以無法建立新的內容。<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**Tb \_電子 \_ 郵件 \_ 太 \_ 多**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | 因為有太多開啟的虛擬資源，所以無法建立新的虛擬資源。<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**Tb \_E \_ 服務 \_ 開始 \_ 擱置**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | TBS 服務已啟動，但尚未執行。<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**Tb \_E \_ PPI \_ 不 \_ 支援**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | 不支援實體存在性介面。<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**Tb \_E \_ 命令 \_ 已取消**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | 命令已取消。<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**Tb \_E \_ 緩衝區 \_ 太 \_ 大**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | 輸入或輸出緩衝區太大。<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**Tb \_E \_ \_ 找不 \_ 到 TPM**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | 在這部電腦上找不到相容的可信賴平臺模組 (TPM) 安全性裝置。<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**Tb \_E \_ 服務 \_ 已停用**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | 已停用 [TB] 服務。<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**Tb \_E \_ 無 \_ 事件 \_ 記錄**</dt>檔 <dt>2150121489 (0x80284011)</dt> </dl>                                     | 無法使用 TB 事件記錄檔。<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**Tb \_E \_ \_ 拒絕存取**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | 呼叫端沒有適當的許可權，無法執行所要求的作業。<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**Tb \_E 布建 \_ \_ 不 \_ 允許**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | 指定的旗標不允許 TPM 布建動作。<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**Tb \_E \_ PPI \_ 函數 \_ 不支援**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | 此固件的實體目前狀態介面不支援要求的方法。<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**Tb \_E \_ OWNERAUTH \_ \_ 找不到**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | 找不到要求的 TPM OwnerAuth 值。<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**Tb \_E 布建 \_ \_ 未完成**</dt>的 <dt>2150121493 (0x80284015)</dt> </dl>     | TPM 布建未完成。 如需完成布建的詳細資訊，請呼叫 [**Win32 \_ tpm**](/windows/desktop/SecProv/win32-tpm) WMI 方法來布建 Tpm ( 「布建」 ) 並檢查傳回的資訊。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Tb. h</dt> </dl> |



 

