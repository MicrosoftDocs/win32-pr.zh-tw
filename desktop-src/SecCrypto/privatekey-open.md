---
description: 存取現有的金鑰容器。 此方法會 \_ 使用指定的資訊新增 CERT key \_ >prov \_ INFO \_ \_ 屬性 ID 屬性，將金鑰容器關聯至對應至私密金鑰的憑證。
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: PrivateKey，Open 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987068"
---
# <a name="privatekeyopen-method"></a>PrivateKey，Open 方法

\[**Open** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**Open** 方法會存取現有的 [*金鑰容器*](../secgloss/k-gly.md)。 此方法會使用指定的資訊新增[](../secgloss/c-gly.md) CERT [](../secgloss/p-gly.md) \_ key \_ >prov \_ INFO \_ \_ 屬性 ID 屬性，將金鑰容器關聯至對應至私密金鑰的憑證。

## <a name="syntax"></a>語法


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*容器* \[在\]
</dt> <dd>

包含金鑰容器名稱的字串。

</dd> <dt>

*ProviderName* \[在中，選擇性\]
</dt> <dd>

字串，其中包含提供者的名稱。 預設值為 CAPICOM \_ >prov \_ MS 增強 \_ 的 \_ >prov。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                      | 意義                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ >PROV**</dt> </dl>                                          | Microsoft 基礎密碼編譯提供者。<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ 增強的 \_ >PROV**</dt> </dl>                           | Microsoft 增強型密碼編譯提供者。<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ 強式 \_ >PROV**</dt> </dl>                                 | Microsoft 強式密碼編譯提供者。<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ RSA \_ SIG \_ >PROV**</dt> </dl>                | Microsoft RSA signature 密碼編譯提供者。<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ RSA \_ SCHANNEL \_ >PROV**</dt> </dl> | Microsoft RSA Schannel 密碼編譯提供者。<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ DSS \_ >PROV**</dt> </dl>                             | Microsoft 基底 DSS 密碼編譯提供者。<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ DSS \_ DH \_ >PROV**</dt> </dl>                   | Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者。<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ ENH \_ DSS \_ DH \_ >PROV**</dt> </dl>                   | Microsoft 增強的 DSS 和 Diffie-Hellman 密碼編譯提供者。<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ DEF \_ DH \_ SCHANNEL \_ >PROV**</dt> </dl>    | Microsoft DH Schannel 密碼編譯提供者。<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ 捨棄 \_ >PROV**</dt> </dl>                                    | Microsoft 基礎智慧卡密碼編譯提供者。<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ ENH \_ RSA \_ AES \_ >PROV**</dt> </dl>                | Microsoft 增強的 RSA 和 AES 密碼編譯提供者。<br/>            |



 

</dd> <dt>

*ProviderType* \[在中，選擇性\]
</dt> <dd>

指定提供者類型之 [**CAPICOM \_ >prov \_ 類型**](capicom-prov-type.md) 列舉的值。 預設值為 CAPICOM \_ >prov \_ RSA \_ FULL。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ FULL**</dt> </dl>                 | 完整的 [*RSA*](../secgloss/r-gly.md) [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。 此提供者類型支援 [*數位簽章*](../secgloss/d-gly.md) 和資料 [*加密*](../secgloss/e-gly.md)。<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ SIG**</dt> </dl>                    | RSA CSP 的子集，僅支援 [*雜湊*](../secgloss/h-gly.md) 和 [*數位簽章*](../secgloss/d-gly.md)所需的函數和演算法。<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ >PROV \_ DSS**</dt> </dl>                                 | [*數位簽章標準*](../secgloss/d-gly.md) (DSS) CSP。 此提供者類型僅支援雜湊和數位簽章。 DSS 會使用 [*數位簽章演算法*](../secgloss/d-gly.md) (DSA) 。<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ >PROV \_ FORTEZZA**</dt> </dl>                  | 包含密碼編譯通訊協定和演算法的 CSP， (NIST) 的規範 [*標準和技術*](../secgloss/n-gly.md) 。<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ >PROV \_ MS \_ EXCHANGE**</dt> </dl>        | 支援 Microsoft Exchange 郵件應用程式的 CSP，以及與 Microsoft Mail 相容的其他應用程式。<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ >PROV \_ SSL**</dt> </dl>                                 | 支援 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ SCHANNEL**</dt> </dl>     | 支援 RSA 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ >PROV \_ DSS \_ DH**</dt> </dl>                       | 支援 DSS 和 [*diffie-hellman*](../secgloss/d-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | 支援橢圓曲線數位簽章演算法的 CSP (ECDSA) 函數和數位簽章所需的演算法。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | 支援橢圓曲線 Nyberg-Rueppel 類比 (ECNRA) 函數和數位簽章所需演算法的 CSP。<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECDSA \_ FULL**</dt> </dl> | 支援完整 ECDSA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ >PROV \_ EC \_ ECNRA \_ FULL**</dt> </dl> | 支援完整 ECNRA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ >PROV \_ DH \_ SCHANNEL**</dt> </dl>        | 支援 [*diffie-hellman*](../secgloss/d-gly.md) 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ >PROV \_ SPYRUS \_ LYNKS**</dt> </dl>     | 支援 SPYRUS LYNKS 插卡裝置的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ >PROV \_ RNG**</dt> </dl>                                 | 處理亂數產生的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**\_>PROV \_ INTEL \_ SEC 的 CAPICOM**</dt> </dl>              | 提供 Intel 安全性的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ >PROV \_ 取代 \_ OWF**</dt> </dl>        | 支援取代從密碼產生單向格式之方法的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ >PROV \_ RSA \_ AES**</dt> </dl>                    | 使用進階加密標準 ([*AES*](../secgloss/a-gly.md)) 演算法支援數位簽章和資料加密的 CSP。<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[在中，選擇性\]
</dt> <dd>

指定私密金鑰類型之 [**CAPICOM \_ 金鑰 \_ 規格**](capicom-key-spec.md) 列舉的值。 預設值是 [CAPICOM \_ 金鑰規格簽章] \_ \_ 。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                        | 意義                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM \_ 金鑰 \_ 規格 \_ KEYEXCHANGE**</dt> </dl> | 金鑰可用於加密和簽署。<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**CAPICOM \_ 金鑰 \_ 規格簽章 \_**</dt> </dl>       | 金鑰只能用於簽署。<br/>           |



 

</dd> <dt>

*StoreLocation* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md)列舉值，指定索引鍵所在之存放區的位置。 預設值是 [CAPICOM \_ 目前 \_ 使用者 \_ 存放區]。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**CAPICOM \_ 記憶體 \_ 存放區**</dt> </dl>                                                | 存放區是記憶體存放區。 存放區內容中的任何變更都不會保存。<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM \_ 本機 \_ 電腦 \_ 存放區**</dt> </dl>                          | 存放區是本機電腦存放區。 只有當使用者擁有讀取/寫入權限時，本機電腦存放區才可以是讀取/寫入存放區。 如果使用者具有讀取/寫入權限，且存放區已開啟讀取/寫入，則會保存存放區內容中的變更。<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**CAPICOM \_ 目前的 \_ 使用者 \_ 存放區**</dt> </dl>                             | 存放區是目前的使用者存放區。 目前的使用者存放區可能是「讀取/寫入」存放區。 如果是，就會保存存放區內容中的變更。<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 使用者 \_ 存放區**</dt> </dl> | 存放區是 Active Directory 存放區。 Active Directory 存放區只能在唯讀模式中開啟。 憑證無法在 Active Directory 存放區中新增或移除。<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**</dt> </dl>                   | 存放區是一組目前的智慧卡。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[在中，選擇性\]
</dt> <dd>

指出 CAPICOM 是否會嘗試存取金鑰的布林值。 若 **為 True，則** 會嘗試存取金鑰。 如果金鑰是使用者保護的，或是在智慧卡或其他裝置上，則可能會產生對話方塊。 預設值為 **[False]** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

\_ \_ \_ 從 web 應用程式編寫腳本時，這個方法會傳回不允許的 CAPICOM E。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
