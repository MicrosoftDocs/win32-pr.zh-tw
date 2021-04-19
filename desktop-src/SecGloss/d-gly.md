---
description: 包含以字母 D 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d007cbb9-b547-4dc7-bc22-b526f650f7c2
title: 'D (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f81a17b2ba2c34b6d5367c1f920ad4b2a4048b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979237"
---
# <a name="d-security-glossary"></a>D (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_dac_gly"></span><span id="_SECURITY_DAC_GLY"></span>**Dac**
</dt> <dd>

請參閱 *動態存取控制*。

</dd> <dt>

<span id="_security_dacl_gly"></span><span id="_SECURITY_DACL_GLY"></span>**Dacl**
</dt> <dd>

查看 *任意存取控制清單*。

</dd> <dt>

<span id="_security_data_content_type_gly"></span><span id="_SECURITY_DATA_CONTENT_TYPE_GLY"></span>**資料內容類型**
</dt> <dd>

PKCS 7 定義的基底內容類型 \# 。 資料內容只是一個八位 (位元組) 字串。

</dd> <dt>

<span id="_security_data_encryption_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_GLY"></span>**資料加密**
</dt> <dd>

請參閱 [*加密*](e-gly.md)。

</dd> <dt>

<span id="_security_data_encryption_function_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_FUNCTION_GLY"></span>**資料加密函式**
</dt> <dd>

請參閱 [*加密和解密功能*](e-gly.md)。

</dd> <dt>

<span id="_security_data_encryption_standard_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_STANDARD_GLY"></span>**資料加密標準**
</dt> <dd>

 (DES) 將64位區塊中的資料加密的區塊加密。 DES 是對稱演算法，使用相同的演算法和金鑰來進行加密和解密。

DES 在1970年初開發，也稱為 DEA (資料加密演算法，由 ANSI) ，而 DEA-1 （依 ISO）。

</dd> <dt>

<span id="_security_datagram_gly"></span><span id="_SECURITY_DATAGRAM_GLY"></span>**傳送**
</dt> <dd>

使用透過封包切換網路路由傳送資訊的通道。 這項資訊包括個別的資訊封包，以及與這些封包相關聯的傳遞資訊，例如目的地位址。 在封包切換網路中，資料封包會彼此獨立地路由傳送，而且可能會遵循不同的路由。 他們可能也會以與其傳送的順序不同的順序抵達。

</dd> <dt>

<span id="_security_decoding_gly"></span><span id="_SECURITY_DECODING_GLY"></span>**解碼**
</dt> <dd>

將編碼的物件 (例如憑證) 或資料轉換回其原始格式的處理常式。

一般來說，資料是由通訊協定的編碼/解碼層解碼。 **CryptDecodeObject** 函式的呼叫會將憑證解碼。

</dd> <dt>

<span id="_security_decryption_gly"></span><span id="_SECURITY_DECRYPTION_GLY"></span>**解密**
</dt> <dd>

將加密文字轉換成純文字的程式。 解密與加密相反。

</dd> <dt>

<span id="_security_default_mode_gly"></span><span id="_SECURITY_DEFAULT_MODE_GLY"></span>**預設模式**
</dt> <dd>

預設設定，例如封鎖加密加密模式或封鎖加密填補方法。

</dd> <dt>

<span id="_security_der_gly"></span><span id="_SECURITY_DER_GLY"></span>**DER**
</dt> <dd>

請參閱 *可辨別編碼規則*。

</dd> <dt>

<span id="_security_derived_key_gly"></span><span id="_SECURITY_DERIVED_KEY_GLY"></span>**衍生金鑰**
</dt> <dd>

**CryptDeriveKey** 函式的呼叫所建立的密碼編譯金鑰。 您可以從密碼或任何其他使用者資料建立衍生金鑰。 衍生金鑰可讓應用程式視需要建立工作階段金鑰，而不必儲存特定的金鑰。

</dd> <dt>

<span id="_security_des_gly"></span><span id="_SECURITY_DES_GLY"></span>**Des**
</dt> <dd>

請參閱 *資料加密標準*。

</dd> <dt>

<span id="_security_dh_gly"></span><span id="_SECURITY_DH_GLY"></span>**Dh**
</dt> <dd>

請參閱 *diffie-hellman 演算法*。

</dd> <dt>

<span id="_security_dh_keyx_gly"></span><span id="_SECURITY_DH_KEYX_GLY"></span>**DH \_ KEYX**
</dt> <dd>

Diffie-Hellman 金鑰交換演算法的 CryptoAPI 演算法名稱。

另請參閱 *diffie-hellman 演算法*。

</dd> <dt>

<span id="_security_diffie_hellman_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_ALGORITHM_GLY"></span>**Diffie-hellman 演算法**
</dt> <dd>

 (DH) 用於安全金鑰交換的公開金鑰演算法。 Diffie-Hellman 不能用於資料加密。 此演算法會指定為 >PROV \_ DSS \_ DH 提供者類型的金鑰交換演算法。

另請參閱 *diffie-hellman (儲存和轉寄) 的金鑰交換演算法* 和 *diffie-hellman (暫時) 金鑰交換演算法*。

</dd> <dt>

<span id="_security_diffie_hellman_store_and_forward_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_STORE_AND_FORWARD_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Diffie-hellman (儲存和轉寄) 的金鑰交換演算法**
</dt> <dd>

Diffie-Hellman 演算法，也就是在終結金鑰控制碼之後，將 exchange 金鑰值保留 (在 CSP) 中。

另請參閱 *diffie-hellman (暫時) 金鑰交換演算法*。

</dd> <dt>

<span id="_security_diffie_hellman_ephemeral_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_EPHEMERAL_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Diffie-hellman (暫時) 金鑰交換演算法**
</dt> <dd>

一種 Diffie-Hellman 演算法，此演算法會在金鑰控制碼損毀時，從 CSP 中刪除交換金鑰值。

另請參閱 *diffie-hellman (儲存和轉寄) 的金鑰交換演算法*。

</dd> <dt>

<span id="_security_digested_data_gly"></span><span id="_SECURITY_DIGESTED_DATA_GLY"></span>**子集資料**
</dt> <dd>

由 PKCS 7 定義的資料內容類型 \# ，由任何類型的資料加上訊息雜湊 (摘要) 內容所組成。

</dd> <dt>

<span id="_security_digital_certificate_gly"></span><span id="_SECURITY_DIGITAL_CERTIFICATE_GLY"></span>**數位憑證**
</dt> <dd>

請參閱 [*憑證*](c-gly.md)。

</dd> <dt>

<span id="_security_digital_envelope_gly"></span><span id="_SECURITY_DIGITAL_ENVELOPE_GLY"></span>**數位信封**
</dt> <dd>

使用收件者公開金鑰加密的私用訊息。 您只能使用收件者的私密金鑰來解密封裝的訊息，只允許收件者瞭解訊息。

</dd> <dt>

<span id="_security_digital_signature_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_GLY"></span>**數位簽章**
</dt> <dd>

將傳送者的身分識別繫結至所傳送資訊的資料。 數位簽章可與任何訊息、檔案，或其他數位編碼資訊一併送出，也可以個別傳輸。 數位簽章可以用在公開金鑰環境中，並提供驗證與完整性服務。

</dd> <dt>

<span id="_security_digital_signature_algorithm_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_ALGORITHM_GLY"></span>**數位簽章演算法**
</dt> <dd>

 (DSA) 數位簽章標準 (DSS) 所指定的公開金鑰演算法。 DSA 僅用來產生數位簽章。 它無法用於資料加密。

</dd> <dt>

<span id="_security_digital_signature_key_pair_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_KEY_PAIR_GLY"></span>**數位簽章金鑰組**
</dt> <dd>

請參閱簽章 [*金鑰*](s-gly.md)組。

</dd> <dt>

<span id="_security_digital_signature_standard_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_STANDARD_GLY"></span>**數位簽章標準**
</dt> <dd>

 (DSS) 指定數位簽章演算法 (DSA) 做為其簽章演算法以及 SHA-1 做為其訊息雜湊演算法的標準。 DSA 是一個公開金鑰加密，只用來產生數位簽章，不能用於資料加密。 DSS 是由 >PROV \_ dss、>prov \_ dss \_ DH 和 >prov \_ FORTEZZA 提供者類型所指定。

</dd> <dt>

<span id="_security_discretionary_access_control_list_gly"></span><span id="_SECURITY_DISCRETIONARY_ACCESS_CONTROL_LIST_GLY"></span>**任意存取控制清單**
</dt> <dd>

 (DACL) 存取控制清單，此清單是由物件擁有者所控制，並指定特定使用者或群組可以擁有的物件存取權。

另請參閱 [*存取控制清單*](a-gly.md) 和 [*系統存取控制清單*](s-gly.md)。

</dd> <dt>

<span id="_security_distinguished_encoding_rules_gly"></span><span id="_SECURITY_DISTINGUISHED_ENCODING_RULES_GLY"></span>**可辨別編碼規則**
</dt> <dd>

 (DER) 一組規則，可將 ASN. 1 定義的資料編碼為外部儲存體或傳輸的位串流。 每個 ASN. 1 物件都只有一個對應的 DER 編碼。 DER 定義于 CCITT 建議的 x.509，第8.7 節。 這是 CryptoAPI 目前所使用的兩種編碼方法之一。

</dd> <dt>

<span id="_security_dll_gly"></span><span id="_SECURITY_DLL_GLY"></span>**Dll**
</dt> <dd>

請參閱 *動態連結程式庫*。

</dd> <dt>

<span id="_security_dsa_gly"></span><span id="_SECURITY_DSA_GLY"></span>**Dsa**
</dt> <dd>

請參閱 *數位簽章演算法*。

</dd> <dt>

<span id="_security_dss_gly"></span><span id="_SECURITY_DSS_GLY"></span>**Dss**
</dt> <dd>

請參閱 *數位簽章標準*。

</dd> <dt>

<span id="_security_dynamic_access_control_gly"></span><span id="_SECURITY_DYNAMIC_ACCESS_CONTROL_GLY"></span>**動態存取控制**
</dt> <dd>

 (DAC) 能夠根據使用者、裝置和資源宣告來指定存取控制原則。 這可讓應用程式更有彈性地進行驗證，同時維持安全性和合規性需求。

</dd> <dt>

<span id="_security_dynamic_link_library_gly"></span><span id="_SECURITY_DYNAMIC_LINK_LIBRARY_GLY"></span>**動態連結程式庫**
</dt> <dd>

 (DLL) 檔案，其中包含可從其他應用程式呼叫的可執行常式。

</dd> </dl>

 

 



