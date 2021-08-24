---
description: 指定演算法識別碼。
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: 'ALG_ID (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482394"
---
# <a name="alg_id"></a>ALG_ID

**ALG_ID** 資料類型會指定演算法識別碼。 此資料類型的參數會傳遞至 CryptoAPI 中的大部分函數。


```C++
typedef unsigned int ALG_ID;
```



下表列出目前定義的演算法識別碼。 自訂 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (csp) 的作者可以定義新值。 此外，自定義 csp 針對金鑰規格所使用的 ALG_ID **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 與提供者相依。 目前的對應會在資料表之後。




| 識別碼 | 值 | 描述 | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | <a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密演算法。 | 
| CALG_3DES_112 | 0x00006609 | 具有等於112位之有效金鑰長度的雙金鑰 <a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密。 | 
| CALG_AES | 0x00006611 | 進階加密標準 (AES) 。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。 | 
| CALG_AES_128 | 0x0000660e | 128位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。 | 
| CALG_AES_192 | 0x0000660f | 192位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。 | 
| CALG_AES_256 | 0x00006610 | 256位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。 | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Diffie-hellman 的控制碼的暫存演算法識別碼-已同意的金鑰。 | 
| CALG_CYLINK_MEK | 0x0000660c | 用來建立40位 DES 金鑰的演算法，該金鑰具有同位位和零的金鑰位，以使其金鑰長度64位。 <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_DES | 0x00006601 | DES 加密演算法。 | 
| CALG_DESX | 0x00006604 | DESX 加密演算法。 | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman 暫時金鑰交換演算法。 | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman 儲存和轉寄金鑰交換演算法。 | 
| CALG_DSS_SIGN | 0x00002200 | DSA <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰</em></a> 簽章演算法。 | 
| CALG_ECDH | 0x0000aa05 | 橢圓曲線 Diffie-Hellman 金鑰交換演算法。<blockquote>[!Note]<br />只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</blockquote><br /><strong>Windows Server 2003 和 Windows XP：</strong>不支援此演算法。<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | 暫時的橢圓曲線 Diffie-Hellman 金鑰交換演算法。<blockquote>[!Note]<br />只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</blockquote><br /><strong>Windows Server 2003 和 Windows XP：</strong>不支援此演算法。<br /> | 
| CALG_ECDSA | 0x00002203 | 橢圓曲線數位簽章演算法。<blockquote>[!Note]<br />只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。</blockquote><br /><strong>Windows Server 2003 和 Windows XP：</strong>不支援此演算法。<br /> | 
| CALG_ECMQV | 0x0000a001 | 橢圓曲線 Menezes、Qu 和 Vanstone (MQV) 的金鑰交換演算法。 不支援此演算法。 | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | 單向函數雜湊演算法。 | 
| CALG_HUGHES_MD5 | 0x0000a003 | Hughes MD5 雜湊演算法。 | 
| CALG_HMAC | 0x00008009 | HMAC 金鑰雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_KEA_KEYX | 0x0000aa04 |  (FORTEZZA) 的 KEA 金鑰交換演算法。 不支援此演算法。 | 
| CALG_MAC | 0x00008005 | <a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> 金鑰雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_MD2 | 0x00008001 | MD2 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_MD4 | 0x00008002 | MD4 雜湊演算法。 | 
| CALG_MD5 | 0x00008003 | MD5 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_NO_SIGN | 0x00002000 | 沒有簽章演算法。 | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | 演算法只會在 CNG 中執行。 宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。 | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | 演算法是在編碼的參數中定義。 只有使用 CNG 才支援此演算法。 宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。 | 
| CALG_PCT1_MASTER | 0x00004c04 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_RC2 | 0x00006602 | RC2 區塊加密演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_RC4 | 0x00006801 | RC4 資料流程加密演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_RC5 | 0x0000660d | RC5 區塊加密演算法。 | 
| CALG_RSA_KEYX | 0x0000a400 | RSA 公開金鑰交換演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_RSA_SIGN | 0x00002400 | RSA 公開金鑰簽章演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_SEAL | 0x00006802 | 密封加密演算法。 不支援此演算法。 | 
| CALG_SHA | 0x00008004 | SHA 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_SHA1 | 0x00008004 | 與 <strong>CALG_SHA</strong>相同。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。 | 
| CALG_SHA_256 | 0x0000800c | 256位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>Windows XP SP3：</strong>Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br /><strong>Windows xp SP2、Windows XP SP1 和 Windows xp：</strong>不支援此演算法。<br /> | 
| CALG_SHA_384 | 0x0000800d | 384位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>Windows XP SP3：</strong>Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br /><strong>Windows xp SP2、Windows XP SP1 和 Windows xp：</strong>不支援此演算法。<br /> | 
| CALG_SHA_512 | 0x0000800e | 512位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>Windows XP SP3：</strong>Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br /><strong>Windows xp SP2、Windows XP SP1 和 Windows xp：</strong>不支援此演算法。<br /> | 
| CALG_SKIPJACK | 0x0000660a | Skipjack 區塊加密演算法 (FORTEZZA) 。 不支援此演算法。 | 
| CALG_SSL2_MASTER | 0x00004c05 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_SSL3_MASTER | 0x00004c01 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_SSL3_SHAMD5 | 0x00008008 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_TEK | 0x0000660b | TEK-TIPS FORUMS (FORTEZZA) 。 不支援此演算法。 | 
| CALG_TLS1_MASTER | 0x00004c06 | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 
| CALG_TLS1PRF | 0x0000800a | 由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。 | 




 

針對 [Microsoft 基礎密碼編譯提供者](microsoft-base-cryptographic-provider.md)、 [microsoft 強式密碼](microsoft-strong-cryptographic-provider.md)編譯提供者，[以及 Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)，用於 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的主要規格 **ALG_IDs** 如下所示：

-   **CALG_RSA_KEYX** 用於 **AT_KEYEXCHANGE**。
-   **CALG_RSA_SIGN** 用於 **AT_SIGNATURE**。

針對 [Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)，用於金鑰規格 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的 **ALG_IDs** 如下所示：

-   **CALG_DH_SF** 用於 **AT_KEYEXCHANGE**。
-   **CALG_DSS_SIGN** 用於 **AT_SIGNATURE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[密碼編譯函式](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
