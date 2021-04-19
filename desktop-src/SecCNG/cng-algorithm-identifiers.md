---
description: 用來識別各種 CNG 函數和結構中的標準加密演算法，例如 CRYPT \_ 介面 \_ REG 結構。
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: 'CNG 演算法識別碼 (Bcrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba244f2a815933322793fdd572ed7a4e69256a0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000239"
---
# <a name="cng-algorithm-identifiers"></a>CNG 演算法識別碼

下列識別碼用來識別各種 CNG 函式和結構中的標準加密演算法，例如 [**CRYPT \_ 介面 \_ REG**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) 結構。 協力廠商提供者可能會有其他支援的演算法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數/值</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3des &quot; </dt> </dl></td>
<td style="text-align: left;">三重資料加密標準對稱式加密演算法。<br/> 標準： SP800-67，SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">112位的三重資料加密標準對稱式加密演算法。<br/> 標準： SP800-67，SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Advanced encryption standard 對稱式加密演算法。<br/> 標準： FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Advanced encryption standard (AES) 以密碼為基礎的訊息驗證碼 (CMAC) 對稱式加密演算法。<br/> 標準： SP 800-38B<br/> <strong>Windows 8：</strong> 此演算法的支援開始。<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Advanced encryption standard (AES) Galois 訊息驗證碼 (GMAC) 對稱式加密演算法。<br/> 標準： SP800-38D<br/> <strong>Windows Vista：</strong> 從 Windows Vista SP1 開始支援此演算法。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </dl></td>
<td style="text-align: left;"> (CAPI) 金鑰衍生函式演算法的加密 API。 由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; DES &quot; </dt> </dl></td>
<td style="text-align: left;">資料加密標準對稱式加密演算法。<br/> 標準： FIPS 46-3、FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">擴充的資料加密標準對稱式加密演算法。<br/> 標準：無<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </dl></td>
<td style="text-align: left;">Diffie-Hellman 的金鑰交換演算法。<br/> 標準： PKCS #3<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">數位簽章演算法。<br/> 標準： FIPS 186-2<br/> <strong>Windows 8：</strong> 從 Windows 8 開始，此演算法支援 FIPS 186-3。 小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">256位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。<br/> 標準： SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">384位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。<br/> 標準： SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">521位的質數橢圓曲線 Diffie-Hellman 金鑰交換演算法。<br/> 標準： SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">256位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。<br/> 標準： FIPS 186-2、X x9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">384位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。<br/> 標準： FIPS 186-2、X x9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">521位質數橢圓曲線數位簽章演算法 (FIPS 186-2) 。<br/> 標準： FIPS 186-2、X x9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">MD2 雜湊演算法。<br/> 標準： RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">MD4 雜湊演算法。<br/> 標準： RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">MD5 雜湊演算法。<br/> 標準： RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">RC2 區塊對稱式加密演算法。<br/> 標準： RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">RC4 對稱式加密演算法。<br/> 標準：各種<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">亂數字產生器演算法。<br/> 標準： FIPS 186-2、FIPS 140-2、NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
從 Windows Vista SP1 和 Windows Server 2008 開始，亂數產生器是以 NIST SP 800-90 標準中指定的 AES 計數器模式為基礎。
</blockquote>
<br/> <strong>Windows Vista：</strong> 亂數產生器是根據 FIPS 186-2 標準中指定的雜湊型亂數產生器。<br/> <strong>Windows 8：</strong> 從 Windows 8 開始，RNG 演算法支援 FIPS 186-3。 小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">雙重橢圓曲線亂數字產生器演算法。 <br/> 標準： SP800-90。<br/> <strong>Windows 8：</strong> 從 Windows 8 開始，EC RNG 演算法支援 FIPS 186-3。 小於或等於1024位的金鑰會遵循 FIPS 186-2，以及大於1024的金鑰，以達 FIPS 186-3。<br/> <strong>Windows 10：</strong> 從 Windows 10 開始，已移除雙重橢圓曲線亂數字產生器演算法。 此演算法的現有用法將繼續運作;不過，亂數產生器是以 NIST SP 800-90 標準中指定的 AES 計數器模式為基礎。 新的程式碼應該使用 <strong>BCRYPT_RNG_ALGORITHM</strong>，建議您將現有的程式碼變更為使用 <strong>BCRYPT_RNG_ALGORITHM</strong>。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">適用于 DSA (數位簽章演算法) 的亂數字產生器演算法。 <br/> 標準： FIPS 186-2。<br/> <strong>Windows 8：</strong> FIPS 186-3 的支援開始。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">RSA 公開金鑰演算法。 <br/> 標準： PKCS #1 1.5 和2.0 版。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">RSA 簽章演算法。 目前不支援此演算法。 您可以使用 <strong>BCRYPT_RSA_ALGORITHM</strong> 演算法來執行 RSA 簽署作業。 <br/> 標準： PKCS #1 1.5 和2.0 版。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">160位的安全雜湊演算法。 <br/> 標準： FIPS 180-2、FIPS 198。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">256位的安全雜湊演算法。<br/> 標準： FIPS 180-2、FIPS 198。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </dl></td>
<td style="text-align: left;">384位的安全雜湊演算法。 <br/> 標準： FIPS 180-2、FIPS 198。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">512位的安全雜湊演算法。 <br/> 標準： FIPS 180-2、FIPS 198。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">計數器模式、雜湊式訊息驗證碼 (HMAC) 金鑰衍生函式演算法。 由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">SP800-56A 主要衍生函式演算法。 由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">以密碼為基礎的金鑰衍生函數 2 (PBKDF2) 演算法。 由 <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> 和 <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> 函數使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">一般質數橢圓曲線數位簽章演算法 (如需詳細資訊) ，請參閱 <strong>備註</strong> 。 <br/> 標準： ANSI X x9.62。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">一般質數橢圓曲線 Diffie-Hellman 金鑰交換演算法 (如需詳細資訊，請參閱 <strong>備註</strong>) 。 <br/> 標準： SP800-56A。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">XTS 模式中的先進加密標準對稱式加密演算法。 <br/> 標準： SP-800-38E、IEEE Std 1619-2007。<br/> <strong>Windows 10：</strong> 此演算法的支援開始。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

若要 **使用 BCRYPT \_ ecdsa \_ ALGORITM** 或 **BCRYPT \_ ecdh \_ 演算法**，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)做為 *pszAlgId*。 然後使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為 [CNG 命名曲線] 中所列的名為演算法。

若要直接提供使用者定義的橢圓曲線參數，請使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 來設定 **BCRYPT \_ ECC \_ 參數** 屬性。 下載 [Windows 10 密碼編譯提供者開發人員套件 (CPDK) ](https://www.microsoft.com/download/details.aspx?id=30688) 以取得詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Bcrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




