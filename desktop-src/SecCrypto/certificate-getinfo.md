---
description: 從憑證抓取資訊。
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: ICertificate2：： GetInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985749"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2：： GetInfo 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**GetInfo** 方法會從 [*憑證*](../secgloss/c-gly.md)中抓取資訊。

## <a name="syntax"></a>語法


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*InfoType* \[在\]
</dt> <dd>

[**CAPICOM 憑證 \_ \_ 資訊 \_ 類型**](capicom-cert-info-type.md)列舉值，指定要從憑證中取出的資料類型。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                     | 意義                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ 簡單 \_ 名稱**</dt> </dl> | 傳回憑證主體的顯示名稱。<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ 簡單 \_ 名稱**</dt> </dl>    | 傳回憑證簽發者的顯示名稱。<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 主體 \_ 電子郵件 \_ 名稱**</dt> </dl>    | 傳回憑證主體的電子郵件地址。<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ 電子郵件 \_ 名稱**</dt> </dl>       | 傳回憑證簽發者的電子郵件地址。<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ UPN**</dt> </dl>                          | 傳回憑證主體的 UPN。 在 CAPICOM 2.0 中引進。<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ UPN**</dt> </dl>                             | 傳回憑證簽發者的 UPN。 在 CAPICOM 2.0 中引進。<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ DNS \_ 名稱**</dt> </dl>          | 傳回憑證主體的 DNS 名稱。 在 CAPICOM 2.0 中引進。<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ DNS \_ 名稱**</dt> </dl>             | 傳回憑證簽發者的 DNS 名稱。 在 CAPICOM 2.0 中引進。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

包含要求之資訊的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[加密物件](cryptography-objects.md)
</dt> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 
