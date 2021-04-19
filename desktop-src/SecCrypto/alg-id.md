---
description: 指定演算法識別碼。
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: 'ALG_ID (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982759"
---
# <a name="alg_id"></a>ALG_ID

**ALG_ID** 資料類型會指定演算法識別碼。 此資料類型的參數會傳遞至 CryptoAPI 中的大部分函數。


```C++
typedef unsigned int ALG_ID;
```



下表列出目前定義的演算法識別碼。 自訂 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (csp) 的作者可以定義新值。 此外，自定義 csp 針對金鑰規格所使用的 ALG_ID **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 與提供者相依。 目前的對應會在資料表之後。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>識別碼</th>
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td><a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密演算法。</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>具有等於112位之有效金鑰長度的雙金鑰 <a href="/windows/desktop/SecGloss/t-gly"><em>三重 DES</em></a> 加密。</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>進階加密標準 (AES) 。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>128位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>192位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>256位 AES。 <a href="microsoft-aes-cryptographic-provider.md">MICROSOFT AES 密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Diffie-hellman 的控制碼的暫存演算法識別碼-已同意的金鑰。</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>用來建立40位 DES 金鑰的演算法，該金鑰具有同位位和零的金鑰位，以使其金鑰長度64位。 <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>DES 加密演算法。</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>DESX 加密演算法。</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Diffie-Hellman 暫時金鑰交換演算法。</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman 儲存和轉寄金鑰交換演算法。</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>DSA <a href="/windows/desktop/SecGloss/p-gly"><em>公開金鑰</em></a> 簽章演算法。</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>橢圓曲線 Diffie-Hellman 金鑰交換演算法。
<blockquote>
[!Note]<br />
只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。
</blockquote>
<br/> <strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>暫時的橢圓曲線 Diffie-Hellman 金鑰交換演算法。
<blockquote>
[!Note]<br />
只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。
</blockquote>
<br/> <strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>橢圓曲線數位簽章演算法。
<blockquote>
[!Note]<br />
只有透過 <a href="/windows/desktop/SecCNG/cng-portal">密碼編譯 API：新一代</a>才支援此演算法。
</blockquote>
<br/> <strong>Windows Server 2003 和 WINDOWS XP：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>橢圓曲線 Menezes、Qu 和 Vanstone (MQV) 的金鑰交換演算法。 不支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>單向函數雜湊演算法。</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Hughes MD5 雜湊演算法。</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>HMAC 金鑰雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td> (FORTEZZA) 的 KEA 金鑰交換演算法。 不支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> 金鑰雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>MD2 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>MD4 雜湊演算法。</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>MD5 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>沒有簽章演算法。</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xffffffff</td>
<td>演算法只會在 CNG 中執行。 宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>演算法是在編碼的參數中定義。 只有使用 CNG 才支援此演算法。 宏（IS_SPECIAL_OID_INFO_ALGID）可以用來判斷密碼編譯演算法是否只支援使用 CNG 函數。</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>RC2 區塊加密演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>RC4 資料流程加密演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>RC5 區塊加密演算法。</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>RSA 公開金鑰交換演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>RSA 公開金鑰簽章演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>密封加密演算法。 不支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>SHA 雜湊演算法。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>與 <strong>CALG_SHA</strong>相同。 <a href="microsoft-base-cryptographic-provider.md">Microsoft 基礎密碼編譯提供者</a>支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>256位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br/> <strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>384位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br/> <strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>512位 SHA 雜湊演算法。 Microsoft 增強型 RSA 和 AES 密碼編譯提供者支援此演算法。<strong>WINDOWS XP SP3：</strong> Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 支援此演算法。<br/> <strong>WINDOWS xp 加裝 SP2、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 不支援此演算法。<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Skipjack 區塊加密演算法 (FORTEZZA) 。 不支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>TEK-TIPS FORUMS (FORTEZZA) 。 不支援此演算法。</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>由 Schannel.dll 作業系統使用。 應用程式不應使用此 <strong>ALG_ID</strong> 。</td>
</tr>
</tbody>
</table>



 

針對 [Microsoft 基礎密碼編譯提供者](microsoft-base-cryptographic-provider.md)、 [microsoft 強式密碼](microsoft-strong-cryptographic-provider.md)編譯提供者，[以及 Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)，用於 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的主要規格 **ALG_IDs** 如下所示：

-   **CALG_RSA_KEYX** 用於 **AT_KEYEXCHANGE**。
-   **CALG_RSA_SIGN** 用於 **AT_SIGNATURE**。

針對 [Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)，用於金鑰規格 **AT_KEYEXCHANGE** 和 **AT_SIGNATURE** 的 **ALG_IDs** 如下所示：

-   **CALG_DH_SF** 用於 **AT_KEYEXCHANGE**。
-   **CALG_DSS_SIGN** 用於 **AT_SIGNATURE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[密碼編譯函式](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
