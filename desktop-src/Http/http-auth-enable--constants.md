---
title: 'HTTP_AUTH_ENABLE_ 常數 (Http.sys) '
description: 定義可以在 URL 群組上啟用的驗證配置。
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466789"
---
# <a name="http_auth_enable_-constants"></a>HTTP \_ 驗證 \_ 啟用 \_ 常數

**HTTP \_ AUTH \_ ENABLE** 常數定義可以在 URL 群組上啟用的驗證配置。

這些常數會用於 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) 結構中。

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP \_ AUTH \_ ENABLE \_ BASIC**
</dt> <dd> <dl> <dt>



已啟用基本驗證配置。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP \_ 驗證 \_ 啟用 \_ 摘要**
</dt> <dd> <dl> <dt>



摘要式驗證配置已啟用。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP \_ 驗證 \_ 啟用 \_ KERBEROS**
</dt> <dd> <dl> <dt>



Kerberos 驗證配置已啟用。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ 驗證（ \_ 例如旗標） \_ \_ 啟用 \_ KERBEROS \_ 認證 \_ 快取**
</dt> <dd> <dl> <dt>



Kerberos 認證快取已啟用。

**Windows Server 2003 與之前：** 無法使用。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP \_ 驗證（ \_ 例如 \_ 旗標 \_ 捕捉 \_ 認證）**
</dt> <dd> <dl> <dt>



HTTP 伺服器 API 會捕捉呼叫端身分識別，並只將其用於協商和 Kerberos 配置的驗證。

**Windows Server 2003 與之前：** 無法使用。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP \_ AUTH \_ 啟用 \_ NTLM**
</dt> <dd> <dl> <dt>



已啟用 NTLM 驗證配置。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP \_ AUTH \_ ENABLE \_ NEGOTIATE**
</dt> <dd> <dl> <dt>



已啟用 Negotiate 驗證配置。


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP \_ AUTH \_ \_ 全部啟用**
</dt> <dd> <dl> <dt>



所有驗證配置都會啟用。


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

[**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





