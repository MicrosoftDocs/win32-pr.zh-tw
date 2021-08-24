---
description: 包含可針對目前 Microsoft Windows HTTP 服務 (WinHTTP) 會話設定或抓取的選項。
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: WinHttpRequestOption 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051876"
---
# <a name="winhttprequestoption-enumeration"></a>WinHttpRequestOption 列舉

**WinHttpRequestOption** 列舉包含可為目前 Microsoft Windows HTTP 服務 (WinHTTP) 會話設定或抓取的選項。

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**
</dt> <dd>

設定或抓取包含 [*使用者代理程式*](glossary.md)字串的 **VARIANT** 。

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption \_ URL**
</dt> <dd>

捕獲包含資源 URL 的 **VARIANT** 。 此值為唯讀;您無法使用這個屬性來設定 URL。 在呼叫 [**Open**](iwinhttprequest-open.md) 方法之前，無法讀取 URL。 此選項適用于在 [**傳送**](iwinhttprequest-send.md) 方法完成後檢查 URL，以確認是否發生任何重新導向。

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

設定或抓取識別 URL 字串 [*字碼頁*](glossary.md)的 **VARIANT** 。 預設值為 UTF-8 字碼頁。 字碼頁是用來將以 [**Open**](iwinhttprequest-open.md) 方法傳遞的 Unicode URL 字串轉換成單一位元組的字串表示。

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

設定或抓取 **VARIANT** ，指出是否將 URL 字串中的百分比字元轉換成 escape 序列。 此選項的預設值為 **VARIANT \_ TRUE** ，指定所有不安全的美國國家標準局 (ANSI) 字元，但百分比符號會轉換成 escape 序列。

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

設定或抓取 **VARIANT** ，指出應忽略的伺服器憑證錯誤。 這可以是下列其中一個或多個旗標的組合。



| 錯誤                                                  | 值  |
|--------------------------------------------------------|--------|
| 未知的憑證授權單位單位 (CA) 或未受信任的根 | 0x0100 |
| 錯誤的使用方式                                            | 0x0200 |
| 不正確一般名稱 (CN)                                | 0x1000 |
| 不正確日期或憑證已過期                    | 0x2000 |



 

在5.1 版的 WinHTTP 中，此選項的預設值為零，因此不會忽略任何錯誤。 在舊版的 WinHTTP 中，預設設定為0x3300，這會導致預設忽略所有伺服器憑證錯誤。

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

設定 **VARIANT** ，指定傳送至伺服器進行驗證的用戶端憑證。 此選項表示以反斜線分隔之用戶端憑證的位置、 [*憑證存放區*](glossary.md)和主體。 如需有關選取用戶端憑證的詳細資訊，請參閱 [WinHTTP 中的 SSL](ssl-in-winhttp.md)。

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

設定或抓取 **VARIANT** ，指出當伺服器指定資源的新位置時，是否會自動重新導向要求。 此選項的預設值為 **VARIANT \_ TRUE** ，表示要求會自動重新導向。

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

設定或抓取 **VARIANT** ，指出 URL 的路徑和查詢元件中不安全的字元是否會轉換成 escape 序列。 此選項的預設值為 **VARIANT \_ TRUE**，指定要轉換路徑和查詢中的字元。

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

設定或抓取 **VARIANT** ，指出 URL 的查詢元件中不安全的字元是否會轉換成 escape 序列。 此選項的預設值為 **VARIANT \_ TRUE**，指定要轉換查詢中的字元。

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

設定或抓取表示可以使用哪些安全通訊協定的 **變異** 。 此選項會選取用戶端可接受的通訊協定。 此通訊協定會在安全通訊端層 (SSL) 信號交換期間進行協商。 這可以是下列其中一個或多個旗標的組合。



| 通訊協定                           | 值  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| 傳輸層安全性 (TLS) 1。0 | 0x0080 |



 

此選項的預設值為0x0028，表示可以使用 SSL 2.0 或 SSL 3.0。 如果此選項設定為零，用戶端和伺服器就無法判斷可接受的安全性通訊協定，而下一個 [**傳送**](iwinhttprequest-send.md) 會導致錯誤。

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**
</dt> <dd>

設定或抓取表示追蹤目前是否已啟用的 **變異** 。 如需 Microsoft Windows HTTP 服務 (winHTTP) 中追蹤功能的詳細資訊，請參閱[winHTTP 追蹤設備](winhttptracecfg-exe--a-trace-configuration-tool.md)。

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

控制 [**WinHttpRequest**](winhttprequest.md) 物件是否會在 SSL 憑證驗證作業期間，暫時還原用戶端模擬。 **WinHttpRequest** 物件的預設設定為 **TRUE**。 將此選項設定為 **FALSE** ，以在執行憑證驗證作業時保持模擬。

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

控制 WinHTTP 是否允許重新導向。 根據預設，除了從安全的 (HTTPs) URL 傳送至不安全的 (HTTP) URL 以外，所有重新導向都會自動遵循。 將此選項設定為 **TRUE** ，以啟用 HTTPS 對 HTTP 重新導向。

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

啟用或停用 Passport 驗證的支援。 預設會停用 Passport 驗證的自動支援;將此選項設定為 **TRUE** ，以啟用 Passport 驗證支援。

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

設定或抓取 WinHTTP 遵循的重新導向數目上限;預設值為10。 這項限制可防止未經授權的網站在大量重新導向之後讓 WinHTTP 用戶端停止。

**Windows XP SP1 和 Windows 2000 SP3：** 不支援這個列舉值。

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

設定或抓取伺服器回應之標頭部分大小上限的系結集合。 這項系結會透過傳送無限標頭資料的回應，來保護用戶端免于嘗試停止用戶端的惡意伺服器。 預設值為 64 KB。

**Windows XP SP1 和 Windows 2000 SP3：** 不支援這個列舉值。

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

設定或抓取將從回應清空的資料量的系結，以便重複使用連接。 預設值是 1 MB。

**Windows XP SP1 和 Windows 2000 SP3：** 不支援這個列舉值。

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

設定或抓取布林值，指出是否應該使用 HTTP/1.1 或 HTTP/1.0。 預設值為 **TRUE**，因此預設會使用 HTTP/1.1。

**Windows XP SP1 和 Windows 2000 SP3：** 不支援這個列舉值。

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

啟用 SSL 協商期間的伺服器憑證撤銷檢查。 當伺服器呈現憑證時，會執行檢查，以判斷憑證是否已被其簽發者撤銷。 如果憑證確實撤銷，或撤銷檢查失敗，因為無法下載憑證撤銷清單 (CRL) ，要求會失敗;這類撤銷錯誤無法隱藏。

**Windows XP SP1 和 Windows 2000 SP3：** 不支援這個列舉值。

</dd> </dl>

## <a name="remarks"></a>備註

藉由指定上述其中一個常數作為 [**option**](iwinhttprequest-option.md) 屬性的參數，來設定選項。

> [!Note]  
> 如 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的[執行時間需求](winhttp-start-page.md)一節。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




