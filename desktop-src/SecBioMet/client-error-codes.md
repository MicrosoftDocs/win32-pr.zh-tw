---
title: '用戶端錯誤碼 (Winbio \_ err. h) '
description: Winbio err 標頭檔中定義的錯誤碼 \_ 。
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993838"
---
# <a name="client-error-codes"></a>用戶端錯誤碼

下列錯誤碼定義于 Winbio \_ err. h 標頭檔中。



| 常數/值                                                                                                                                                                                                                                                                                         | 描述                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_E \_ 不支援的 \_ 因素**</dt> <dt>0x80098001</dt> </dl>                              | 不支援指定的生物特徵辨識因素。<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_電子 \_ 不正確 \_ 單位**</dt> <dt>0x80098002</dt> </dl>                                                | 單位識別碼號碼未對應到有效的生物識別單元。<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_E \_ 未知的 \_ 識別碼**</dt> <dt>0x80098003</dt> </dl>                                                      | 生物識別範例不符合任何已知的身分識別。<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_E \_ 取消**</dt>的 <dt>0x80098004</dt> </dl>                                                             | 生物識別作業在完成之前已取消。<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_E \_ NO \_ MATCH**</dt> <dt>0x80098005</dt> </dl>                                                            | 生物識別範例不符合指定的身分識別或次要因素。<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_E \_ CAPTURE 已 \_ 中止**</dt> <dt>0x80098006</dt> </dl>                                       | 因為已中止捕獲作業，所以無法捕獲生物識別範例。<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_E \_ 註冊 \_ \_ 進行中**</dt> <dt>0x80098007</dt> </dl>                 | 註冊交易無法啟動，因為另一個註冊已在進行中。<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_電子 \_ 錯誤的 \_ CAPTURE**</dt> <dt>0x80098008</dt> </dl>                                                   | 捕捉的範例無法用於進一步的生物特徵辨識作業。<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_E \_ 不正確 \_ 控制項程式 \_ 代碼**</dt> <dt>0x80098009</dt> </dl>                       | 生物識別單位不支援指定的單元控制項程式碼。<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_\_ \_ \_ \_ 正在進行電子資料收集**</dt> <dt>0x8009800B</dt> </dl> | 暫止的資料收集作業已在進行中。<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_E \_ 不支援的 \_ 資料 \_ 格式**</dt> <dt>0x8009800C</dt> </dl>              | 生物識別感應器驅動程式不支援所要求的資料格式。<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_E \_ 不支援的 \_ 資料 \_ 類型**</dt> <dt>0x8009800D</dt> </dl>                    | 生物識別感應器驅動程式不支援所要求的資料類型。<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_E \_ 不支援的 \_ 目的**</dt> <dt>0x8009800E</dt> </dl>                           | 生物識別感應器驅動程式不支援要求的資料用途。<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_電子 \_ 不正確 \_ 裝置 \_ 狀態**</dt> <dt>0x8009800F</dt> </dl>                       | 生物識別單位未處於適當的狀態，無法執行指定的操作。<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_E \_ 裝置 \_ 忙碌**</dt> <dt>0x80098010</dt> </dl>                                                   | 因為感應器裝置忙碌中，所以無法執行操作。<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 無法 \_ 建立**</dt> <dt>0x80098011</dt> </dl>                       | 儲存體介面卡無法建立新的資料庫。<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 無法 \_ 開啟**</dt> <dt>0x80098012</dt> </dl>                             | 儲存體介面卡無法開啟現有的資料庫。<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 無法 \_ 關閉**</dt> <dt>0x80098013</dt> </dl>                          | 儲存體介面卡無法關閉資料庫。<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 無法 \_ 清除**</dt> <dt>0x80098014</dt> </dl>                          | 儲存體介面卡無法清除資料庫。<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ \_ 找不到**</dt> <dt>0x80098015</dt> </dl>                             | 儲存體介面卡找不到資料庫。<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 已經 \_ 存在**</dt> <dt>0x80098016</dt> </dl>              | 儲存體介面卡無法建立資料庫，因為指定的資料庫已經存在。<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_E \_ DATABASE \_ FULL**</dt> <dt>0x80098018</dt> </dl>                                             | 因為資料庫已滿，所以存放裝置介面卡無法將記錄新增至資料庫。<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 鎖定**</dt> <dt>0x80098019</dt> </dl>                                       | 資料庫已鎖定，且其內容無法存取。<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 損毀**</dt> <dt>0x8009801A</dt> </dl>                              | 資料庫的內容已損毀且無法存取。<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 沒有 \_ 這類 \_ 記錄**</dt> <dt>0x8009801B</dt> </dl>             | 未刪除任何記錄，因為未在資料庫中提供指定的身分識別和子係數。<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_E \_ 重複 \_ 註冊**</dt> <dt>0x8009801C</dt> </dl>                        | 指定的身分識別和子要素已在資料庫中註冊。<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 讀取 \_ 錯誤**</dt> <dt>0x8009801D</dt> </dl>                          | 嘗試從資料庫讀取時發生錯誤。<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 寫入 \_ 錯誤**</dt> <dt>0x8009801E</dt> </dl>                       | 嘗試寫入資料庫時，發生錯誤。<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 沒有 \_ 結果**</dt> <dt>0x8009801F</dt> </dl>                          | 資料庫中沒有符合查詢的記錄。<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 沒有 \_ 其他 \_ 記錄**</dt> <dt>0x80098020</dt> </dl>          | 已抓取最近資料庫查詢中的所有記錄。<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | 資料庫作業意外發生檔案結尾。<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_E \_ 資料庫 \_ 錯誤的 \_ 索引 \_ 向量**</dt> <dt>0x80098022</dt> </dl>       | 因為索引向量的格式不正確，所以資料庫操作失敗。<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_E \_ 不正確的 \_ BSP**</dt> <dt>0x80098024</dt> </dl>                                             | 生物識別單位不屬於指定的服務提供者。<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_\_不正確的 \_ 感應器 \_ 集**</dt>區 <dt>0x80098025</dt> </dl>                    | 生物識別單位不屬於指定的感應器集區。<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_E \_ NO \_ CAPTURE \_ DATA**</dt> <dt>0x80098026</dt> </dl>                                      | 感應器介面卡捕捉緩衝區是空的。<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_E \_ 不正確 \_ 感應器 \_ 模式**</dt> <dt>0x80098027</dt> </dl>                          | 感應器介面卡不支援設定中指定的感應器模式。<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_E \_ 鎖定 \_ 違規**</dt> <dt>0x8009802A</dt> </dl>                                          | 因為鎖定衝突，所以無法執行要求的操作。<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_E \_ 複製 \_ 範本**</dt> <dt>0x8009802B</dt> </dl>                              | 生物特徵辨識範本中的資料，與已存在於資料庫中另一個範本的資料相符。<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_E \_ 不正確 \_ 操作**</dt> <dt>0x8009802C</dt> </dl>                                 | 要求的作業對會話的目前狀態或生物特徵辨識單位無效。<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_E \_ 會話 \_ 忙碌**</dt> <dt>0x8009802D</dt> </dl>                                                | 會話無法開始新的作業，因為另一個作業已在進行中。<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_E \_ 認證 \_ >prov \_ 已停用**</dt> <dt>0x80098030</dt> </dl>                             | 系統原則設定已停用生物識別認證提供者。<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_E \_ \_ 認證 >prov \_ 沒有 \_ 認證**</dt> <dt>0x80098031</dt> </dl>             | 找不到要求的認證。<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_E \_ 停用**</dt>的 <dt>0x80098032</dt> </dl>                                                             | 系統原則設定已停用生物識別服務。<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_E \_ 設定 \_ 失敗**</dt> <dt>0x80098033</dt> </dl>                     | 無法設定生物識別單位。<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_E \_ 感應器 \_ 無法使用**</dt> <dt>0x80098034</dt> </dl>                              | 因為有一或多個生物特徵辨識單位無法使用，所以無法建立私人集區。<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_E \_ \_ 啟用 SAS**</dt>的 <dt>0x80098035</dt> </dl>                                                   |  (CTRL-ALT-刪除) 是登入所需的安全注意順序。<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_E \_ 裝置 \_ 失敗**</dt> <dt>0x80098036</dt> </dl>                                          | 生物識別感應器失敗。<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_E \_ FAST \_ 使用者 \_ 交換器 \_ 已停用**</dt> <dt>0x80098037</dt> </dl>       | 已停用 [快速切換使用者] >。<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_E \_ NOT \_ ACTIVE \_ CONSOLE**</dt> <dt>0x80098038</dt> </dl>                             | 無法從終端機伺服器用戶端會話開啟系統感應器集區。<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_E \_ 事件 \_ 監視器 \_ 主動**</dt> <dt>0x80098039</dt> </dl>                      | 已經有與指定會話相關聯的作用中事件監視器。<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_E \_ 不正確 \_ 屬性 \_ 類型**</dt> <dt>0x8009803A</dt> </dl>                    | 指定的值不是有效的屬性類型。<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_電子 \_ 不正確 \_ 屬性 \_ 識別碼**</dt> <dt>0x8009803B</dt> </dl>                          | 指定的值不是有效的屬性識別碼。<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_E \_ 不支援的 \_ 屬性**</dt> <dt>0x8009803C</dt> </dl>                        | 生物識別單位不支援指定的屬性。<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_E \_ ADAPTER \_ 完整性 \_ 失敗**</dt> <dt>0x8009803D</dt> </dl>        | 介面卡未通過完整性檢查。<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_我 \_ 更多 \_ 資料**</dt> <dt>0x00090001</dt> </dl>                                                         | 目前的註冊範本需要另一個範例。<br/>                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winbio \_ err。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





