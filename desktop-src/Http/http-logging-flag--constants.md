---
title: 'HTTP_LOGGING_FLAG_ 常數 (Http.sys) '
description: 定義要在 HTTP 伺服器 API 上設定記錄的選項。
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686158"
---
# <a name="http_logging_flag_-constants"></a>HTTP \_ 記錄 \_ 旗標 \_ 常數

**Http \_ 記錄 \_ 旗 \_** 標常數定義了在 HTTP 伺服器 API 上設定記錄的選項。

這些常數會在 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info) 結構中使用。

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP \_ 記錄 \_ 旗標 \_ 本地 \_ 時間 \_ 變換**
</dt> <dd> <dl> <dt>



記錄檔變換是以當地時間為基礎。 根據預設，記錄檔變換是以國際標準時間 (UTC) 為基礎。


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_記錄 \_ 旗標 \_ 使用 \_ UTF8 \_ 轉換**
</dt> <dd> <dl> <dt>



寫入記錄檔時，會將 unicode 欄位轉換成 UTF8 multibytes。 根據預設，記錄檔會以本機字碼頁轉換來撰寫。


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP \_ 記錄 \_ 旗標 \_ 記錄檔 \_ 錯誤 \_**
</dt> <dd> <dl> <dt>



記錄檔只包含錯誤資訊。 預設會記錄錯誤和成功回應。 如果 **HTTP \_ 記錄旗標 \_ \_ 記錄 \_ \_** 檔或 **HTTP \_ 記錄旗標 \_ 記錄 \_ \_ \_** 檔都沒有成功，則會記錄錯誤和成功資訊。

如果同時設定了 **HTTP \_ 記錄 \_ 旗標記錄檔 \_ \_ 成功 \_** 旗標，則無法設定這個旗標。 這兩個旗標彼此互斥。


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_記錄 \_ 旗 \_ \_ \_** 標記錄檔成功
</dt> <dd> <dl> <dt>



記錄檔只包含成功資訊。 預設會記錄錯誤和成功交易。 如果 **HTTP \_ 記錄旗標 \_ \_ 記錄 \_ \_** 檔或 **HTTP \_ 記錄旗標 \_ 記錄 \_ \_ \_** 檔都沒有成功，則會記錄錯誤和成功資訊。

如果同時設定了 **HTTP \_ 記錄 \_ 旗標記錄檔 \_ \_ 錯誤 \_** 旗標，則無法設定這個旗標。 這兩個旗標彼此互斥。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Http.sys</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HTTP 伺服器 API 版本2.0 常數](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





