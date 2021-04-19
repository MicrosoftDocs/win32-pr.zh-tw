---
description: 抓取 \_ \_ 可指定提供者類型之 CAPICOM >prov 類型列舉的值。
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: PrivateKey. ProviderType 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998705"
---
# <a name="privatekeyprovidertype-property"></a>PrivateKey. ProviderType 屬性

\[**ProviderType** 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**ProviderType** 屬性會抓取可指定提供者類型的 [**CAPICOM \_ >prov \_ 類型**](capicom-prov-type.md)列舉值。

## <a name="syntax"></a>Syntax


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>屬性值

表示提供者類型之 [**CAPICOM \_ >prov \_ 類型**](capicom-prov-type.md) 列舉的值。 下表顯示可能的值。



| 值                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ FULL**</dt> </dl>                 | 完整的 [*RSA*](../secgloss/r-gly.md) [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。 此提供者類型支援 [*數位簽章*](../secgloss/d-gly.md) 和資料 [*加密*](../secgloss/e-gly.md)。<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ SIG**</dt> </dl>                    | RSA CSP 的子集，支援雜湊和數位簽章所需的函式和演算法。<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ >PROV \_ DSS**</dt> </dl>                                 | [*數位簽章標準*](../secgloss/d-gly.md) (DSS) CSP。 此提供者類型僅支援雜湊和數位簽章。 DSS 會使用 [*數位簽章演算法*](../secgloss/d-gly.md) (DSA) 。<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ >PROV \_ FORTEZZA**</dt> </dl>                  | 包含密碼編譯通訊協定和演算法的 CSP， (NIST) 的規範 [*標準和技術*](../secgloss/n-gly.md) 。<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ EXCHANGE**</dt> </dl>        | 專為 Microsoft Exchange 郵件應用程式和其他與 Microsoft Mail 相容的應用程式的密碼編譯需求而設計的 CSP。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ >PROV \_ SSL**</dt> </dl>                                 | 支援 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ SCHANNEL**</dt> </dl>     | 支援 RSA 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ >PROV \_ DSS \_ DH**</dt> </dl>                       | 支援 [*數位簽章標準*](../secgloss/d-gly.md) (DSS) 和 [*diffie-hellman*](../secgloss/d-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | 支援橢圓曲線數位簽章演算法的 CSP (ECDSA) 函數和數位簽章所需的演算法。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | 支援橢圓曲線 Nyberg-Rueppel 類比 (ECNRA) 函數和數位簽章所需演算法的 CSP。<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECDSA \_ FULL**</dt> </dl> | 支援完整 ECDSA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECNRA \_ FULL**</dt> </dl> | 支援完整 ECNRA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ >PROV \_ DH \_ SCHANNEL**</dt> </dl>        | 支援 [*diffie-hellman*](../secgloss/d-gly.md) 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ >PROV \_ SPYRUS \_ LYNKS**</dt> </dl>     | 支援 SPYRUS LYNKS 插卡裝置的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ >PROV \_ RNG**</dt> </dl>                                 | 處理亂數產生的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**\_>PROV \_ INTEL \_ SEC 的 CAPICOM**</dt> </dl>              | 提供 Intel 安全性的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ >PROV \_ 取代 \_ OWF**</dt> </dl>        | 支援取代 (OWFs) 的單向格式從密碼產生之方法的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ AES**</dt> </dl>                    | 使用 [*進階加密標準*](../secgloss/a-gly.md) (AES) 演算法支援數位簽章和資料加密的 CSP。<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
