---
description: 包含以字母 B 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: 'B (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001739"
---
# <a name="b-security-glossary"></a>B (安全性詞彙) 

[B](a-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**備份授權單位**
</dt> <dd>

在安全電腦上執行的受信任應用程式，可為其用戶端的工作階段金鑰提供次要儲存體。 備份授權單位會將工作階段金鑰儲存為金鑰 Blob，並以備份授權單位的公開金鑰加密。

</dd> <dt>

<span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**基底內容類型**
</dt> <dd>

PKCS 7 訊息中包含的資料類型 \# 。 基底內容類型只包含資料，不包含任何密碼編譯增強功能，例如雜湊或簽章。 目前，唯一的基底內容類型是資料內容類型。

</dd> <dt>

<span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**基底加密函式**
</dt> <dd>

CryptoAPI 架構中最低層級的函數。 應用程式和其他高階 CryptoAPI 函式會使用這些功能來存取 CSP 提供的密碼編譯演算法、安全的金鑰產生，以及安全地儲存秘密。

另請參閱 [*加密服務提供者*](c-gly.md)。

</dd> <dt>

<span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**基本編碼規則**
</dt> <dd>

 (BER) 用來將 ASN. 1 定義的資料編碼成位資料流程的規則集 (零或) 用於外部儲存體或傳輸。 單一 asn.1 物件可以有數個對等的 BER 編碼。 BER 定義于 CCITT 建議的209中。 這是 CryptoAPI 目前所使用的兩種編碼方法之一。

</dd> <dt>

<span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**誤碼率**
</dt> <dd>

請參閱 *基本編碼規則*。

</dd> <dt>

<span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**位元組由大到小**
</dt> <dd>

記憶體或資料格式，其中最重要的位元組會儲存在較低的位址，或先到達。

另請參閱 [*位元組由小到小*](l-gly.md)。

</dd> <dt>

<span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**Blob**
</dt> <dd>

包含一或多個固定長度標頭結構和內容特定資料的一般位序列。

另請參閱 [*主要 blob*](k-gly.md)、 [*憑證 blob*](c-gly.md)、 [*憑證名稱 blob*](c-gly.md)和 [*屬性 blob*](a-gly.md)。

</dd> <dt>

<span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**區塊加密**
</dt> <dd>

一種加密演算法，可將離散單位中的資料加密 (稱為區塊) ，而不是連續的位元組資料流程。 最常見的區塊大小為64位。 例如，DES 是封鎖密碼。

另請參閱 [*資料流程加密*](s-gly.md)。

</dd> <dt>

<span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**大量加密金鑰**
</dt> <dd>

從主要金鑰衍生的工作階段金鑰。 大量加密金鑰用於 [*Schannel*](s-gly.md) 加密中。

</dd> </dl>

 

 



