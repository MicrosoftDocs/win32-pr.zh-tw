---
description: 讓傳輸應用程式查詢認證安全性支援提供者 (CredSSP) 安全性封裝的特定屬性。
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: QueryContextAttributes (CredSSP) 函式 (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b8ff421a2173f2ce2c5521e0706b53c3f6c326038179345d139acd0a157c7d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920227"
---
# <a name="querycontextattributes-credssp-function"></a>QueryCoNtextAttributes (CredSSP) 函數

**QueryCoNtextAttributes (CredSSP)** 函數可讓傳輸應用程式查詢認證安全性支援提供者 (CredSSP) 安全性封裝，以取得安全性內容的特定 [*屬性*](../secgloss/a-gly.md#_security_attribute_gly)。

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

要查詢的安全性內容控制碼。

</dd> <dt>

*ulAttribute* \[在\]
</dt> <dd>

要傳回之內容的屬性。 此參數可以是下列其中一個值。 除非另有指定，否則屬性會同時適用于用戶端和伺服器。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ATTR \_ C \_ 存取 \_ 權杖**</dt> <dt>0x80000012</dt> </dl>                                 | *PBuffer* 參數包含 [**SecPkgCoNtext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)結構的指標，該結構會指定目前安全性內容的存取權杖。<br/> 只有在伺服器上才支援此屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ATTR \_ C \_ 完整 \_ 存取 \_ 權杖**</dt> <dt>0x80000082</dt> </dl>                 | *PBuffer* 參數包含 [**SecPkgCoNtext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)結構的指標，該結構會指定目前安全性內容的存取權杖。<br/> 只有在伺服器上才支援此屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ATTR \_ 憑證 \_ 信任 \_ 狀態**</dt> <dt>0x80000084</dt> </dl>                        | *PBuffer* 參數包含憑證 [**\_ 信任 \_ 狀態**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status)結構的指標，此結構會指定憑證的信任資訊。<br/> 只有用戶端才支援此屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ATTR \_**</dt>認證 <dt>0x80000080</dt> </dl>                                                              | *PBuffer* 參數包含 [**SecPkgCoNtext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)結構的指標，該結構會指定用戶端認證。<br/> 用戶端認證可以是使用者名稱和密碼，或是使用者名稱和智慧卡 PIN。<br/> 只有在伺服器上才支援此屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ATTR \_ 認證 \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | *PBuffer* 參數包含 [**SecPkgCoNtext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)結構的指標，該結構會指定用戶端認證。 <br/> 如果用戶端認證是使用者名稱和密碼，則緩衝區是壓縮的 [**KERB \_ 互動式 \_ 登錄**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) 結構。<br/> 如果用戶端認證是使用者名稱和智慧卡 PIN，則緩衝區是封裝的 [**KERB \_ 憑證 \_ 登**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) 入結構。<br/> 如果用戶端認證是線上身分識別認證，則緩衝區會是已封送處理的 [**SEC \_ \_ AUTH \_ identity \_ EX2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) 結構。<br/> 只有 CredSSP 伺服器才支援此屬性。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 不支援這個值。<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ATTR \_ 協商 \_ 套件**</dt> <dt>0x80000081</dt> </dl>                   | *PBuffer* 參數包含 [**SecPkgCoNtext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的指標，此結構會指定 [Microsoft Negotiate](microsoft-negotiate.md)提供者所協商之驗證套件的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ATTR \_ 封裝 \_ 資訊**</dt> <dt>10</dt> </dl>                                                | *PBuffer* 參數包含 [**SecPkgCoNtext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)結構的指標。<br/> 傳回使用中 SSP 的資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ATTR \_ 伺服器 \_ 驗證 \_ 旗標**</dt> <dt>0x80000083</dt> </dl>                        | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 旗標**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags)結構的指標，此結構會指定目前安全性內容中之旗標的相關資訊。<br/> 只有用戶端才支援此屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ATTR \_ 大小**</dt> <dt>0x0</dt> </dl>                                                                     | *PBuffer* 參數包含 [**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)結構的指標。<br/> 查詢每個訊息函數和驗證交換中使用的結構大小。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ATTR \_ 主體 \_ 安全性 \_ 屬性**</dt> <dt>124</dt> </dl> | *PBuffer* 參數包含 [**SecPkgCoNtext \_ SubjectAttributes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes)結構的指標。<br/> 此值會傳回連接之安全性屬性的相關資訊。<br/> 只有 CredSSP 伺服器才支援這個值。<br/> **Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[擴展\]
</dt> <dd>

接收屬性之結構的指標。 結構類型取決於 *ulAttribute* 參數的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 SEC \_ E \_ OK。

如果函式失敗，可能會傳回下列錯誤碼。



| 傳回碼/值                                                                                                                                                            | Description                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**秒 \_E \_ 不正確 \_ 控制碼**</dt> <dt>0x80100003</dt> </dl>       | 函數失敗。 *PhCoNtext* 參數會指定未完成內容的控制碼。<br/> |
| <dl> <dt>**秒 \_E \_ 不支援的 \_ 函數**</dt> <dt>0x80090302</dt> </dl> | 函數失敗。 *UlAttribute* 參數的值無效。<br/>                 |



 

## <a name="remarks"></a>備註

*PBuffer* 參數所指向的結構會根據所查詢的屬性而有所不同。

雖然呼叫端必須配置 *pBuffer* 結構本身，但 SSP 會配置所需的記憶體，以保存 *pBuffer* 結構的變動大小成員。 您必須呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式來釋放 SSP 所配置的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                   |
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

[**SecPkgCoNtext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**SecPkgCoNtext \_ 大小**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
