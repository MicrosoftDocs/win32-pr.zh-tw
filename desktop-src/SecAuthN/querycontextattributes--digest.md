---
description: 可讓傳輸應用程式查詢 [*安全性內容*](../secgloss/s-gly.md)特定屬性的摘要 [*安全性封裝*](../secgloss/s-gly.md)。
ms.assetid: d4cd2cc4-77a2-42ba-9029-f4d92706c5c2
title: QueryContextAttributes (Digest) 函式 (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1e26e81d190f031479633fe96fbc49496b661302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511228"
---
# <a name="querycontextattributes-digest-function"></a>QueryCoNtextAttributes (Digest) 函數

**QueryCoNtextAttributes (Digest)** 函數可讓傳輸應用程式查詢 [*安全性內容*](../secgloss/s-gly.md)特定 [*屬性*](../secgloss/a-gly.md#_security_attribute_gly)的摘要 [*安全性封裝*](../secgloss/s-gly.md)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCoNtext* \[在\]
</dt> <dd>

要查詢的 [*安全性內容*](../secgloss/s-gly.md) 控制碼。

</dd> <dt>

*ulAttribute* \[在\]
</dt> <dd>

指定要傳回之內容的屬性。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ATTR \_ 存取 \_ 權杖**</dt> <dt>18</dt> </dl>                                   | *PBuffer* 參數包含 [**SecPkgCoNtext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)結構的指標。<br/> 傳回存取權杖的控制碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ATTR \_ 授權**</dt>單位 <dt>6</dt> </dl>                                              | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 授權**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)單位結構的指標。<br/> 查詢驗證授權單位的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ATTR \_ 用戶端 \_ 指定了 \_ 目標**</dt> <dt>27</dt> </dl> | *PBuffer* 參數包含 [**SecPkgCoNtext \_ ClientSpecifiedTarget**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget)結構的指標，該結構代表用戶端所提供之初始目標 (SPN) 的服務主體名稱。 <br/> 只有在使用通道系結時，才支援這個值。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ATTR \_ 認證 \_ 2**</dt> <dt>0x80000086</dt> </dl>                                          | *PBuffer* 參數包含 [**SecPkgCoNtext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)結構的指標，該結構會指定用戶端認證。 <br/> 如果用戶端認證是使用者名稱和密碼，則緩衝區是壓縮的 [**KERB \_ 互動式 \_ 登錄**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) 結構。<br/> 如果用戶端認證是使用者名稱和智慧卡 PIN，則緩衝區是封裝的 [**KERB \_ 憑證 \_ 登**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) 入結構。<br/> 如果用戶端認證是線上身分識別認證，則緩衝區會是已封送處理的 [**SEC \_ \_ AUTH \_ identity \_ EX2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) 結構。<br/> 只有 CredSSP 伺服器才支援此屬性。<br/> **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ATTR \_ DCE \_ INFO**</dt> <dt>3</dt> </dl>                                                | *PBuffer* 參數包含 [**SecPkgCoNtext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)結構的指標。<br/> 查詢 DCE 服務所使用的授權資料。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ATTR \_ 旗標**</dt> <dt>14</dt> </dl>                                                         | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 旗標**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags)結構的指標。<br/> 傳回已協商內容旗標的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ATTR 索引 \_ 鍵 \_ 資訊**</dt> <dt>5</dt> </dl>                                                | *PBuffer* 參數包含 [**SecPkgCoNtext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)結構的指標。<br/> 查詢 [*安全性內容*](../secgloss/s-gly.md)中所使用之索引鍵的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ATTR \_**</dt>存留期 <dt>2</dt> </dl>                                                 | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 生命週期**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)結構的指標。<br/> 查詢內容的存留期範圍。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ ATTR \_ 本機 \_ 認證**</dt> </dl>                                                                                                 | *PBuffer* 參數包含 **SecPkgCoNtext \_ LocalCredentialInfo** 結構的指標。 (已過時)<br/> 由 SECPKG \_ ATTR \_ LOCAL \_ CERT CONTEXT 取代 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ATTR \_ 名稱**</dt> <dt>1</dt> </dl>                                                          | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 名稱**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)結構的指標。<br/> 查詢與內容相關聯的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ATTR \_ 原生 \_ 名稱**</dt> <dt>13</dt> </dl>                                   | *PBuffer* 參數包含 [**SecPkgCoNtext \_ NativeNames**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa)結構的指標。<br/> 從輸出票證傳回主體名稱 (CNAME) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ATTR \_ 協商 \_ 資訊**</dt> <dt>12</dt> </dl>                       | *PBuffer* 參數包含 [**SecPkgCoNtext \_ NegotiationInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa)結構的指標。<br/> 傳回 [*安全性封裝*](../secgloss/s-gly.md) 的相關資訊，這些資訊與協調程式搭配使用，以及使用該封裝之協商的目前狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ATTR \_ 封裝 \_ 資訊**</dt> <dt>10</dt> </dl>                                   | *PBuffer* 參數包含 [**SecPkgCoNtext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的指標。<br/> 傳回使用中 SSP 的資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ATTR \_ 密碼 \_ 到期**</dt> <dt>8</dt> </dl>                           | *PBuffer* 參數包含 [**SecPkgCoNtext \_ PasswordExpiry**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry)結構的指標。<br/> 傳回密碼到期資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ATTR \_ 根 \_ 存放區**</dt> <dt>0x55</dt> </dl>                                       | *PBuffer* 參數包含 **HCERTCONTEXT** 的指標。 尋找包含根存放區所提供之憑證的憑證內容。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ATTR \_ 會話 \_ 金鑰**</dt> <dt>9</dt> </dl>                                       | *PBuffer* 參數包含 [**SecPkgCoNtext \_ setsessionkey**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey)結構的指標。<br/> 傳回 [*工作階段金鑰*](../secgloss/s-gly.md)s 的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ATTR \_ 大小**</dt> <dt>0</dt> </dl>                                                          | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)結構的指標。<br/> 查詢每個訊息函數中使用的結構大小。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_STREAM_SIZES"></span><span id="secpkg_attr_stream_sizes"></span><dl> <dt>**SECPKG \_ATTR \_ 資料流程 \_ 大小**</dt> <dt>4</dt> </dl>                                    | *PBuffer* 參數包含 [**SecPkgCoNtext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)結構的指標。<br/> 查詢每個訊息函數中所使用之資料流程各部分的大小。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ATTR \_ 目標 \_ 資訊**</dt> <dt>17</dt> </dl>                 | *PBuffer* 參數包含 [**SecPkgCoNtext \_ TargetInformation**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation)結構的指標。<br/> 傳回遠端伺服器名稱的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[擴展\]
</dt> <dd>

接收屬性之結構的指標。 所指向結構的類型取決於 *ulAttribute* 參數中指定的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 SEC \_ E \_ OK。

如果函式失敗，則傳回值為非零的錯誤碼。

## <a name="remarks"></a>備註

*PBuffer* 參數所指向的結構會根據所查詢的屬性而有所不同。 呼叫端必須配置 *pBuffer* 結構本身，但 SSP 會配置所需的記憶體，以保存 *pBuffer* 結構的變數大小成員。 藉由呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式，可以釋出 SSP 配置的記憶體。

\_讀取 SECPKG ATTR \_ REMOTE \_ CERT \_ coNtext 或 SECPKG \_ ATTR \_ LOCAL \_ cert \_ coNtext 值之後， **hCertStore** 成員將會設定為包含中繼憑證（如果有的話）的憑證存放區控制碼。 此外，應用程式會負責呼叫 [**CertFreeCertificateCoNtext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) ，以釋放憑證內容所使用的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode 與 ANSI 名稱<br/>   | **QueryCoNtextAttributesW** (Unicode) 和 **QueryCoNtextAttributesA** (ANSI) <br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**憑證 \_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgCoNtext \_ 授權單位**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgCoNtext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgCoNtext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**SecPkgCoNtext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**SecPkgCoNtext \_ 生命週期**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**SecPkgCoNtext \_ 名稱**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgCoNtext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
