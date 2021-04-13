---
description: 包含以字母 E 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f1caccd2-3453-448e-b194-bf899eff8091
title: '電子 (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed30465ef5764d4553ceb03e1094b73d940f85f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513705"
---
# <a name="e-security-glossary"></a>電子 (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**歐洲 央行**
</dt> <dd>

請參閱 *電子 codebook*。

</dd> <dt>

<span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**Ecc**
</dt> <dd>

請參閱 *橢圓曲線密碼* 編譯。

</dd> <dt>

<span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**Efs**
</dt> <dd>

請參閱 *加密檔案系統*。

</dd> <dt>

<span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**
</dt> <dd>

請參閱 *增強金鑰使用* 方法。

</dd> <dt>

<span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**電子 codebook**
</dt> <dd>

 (ECB) 區塊加密模式 (每個區塊會個別加密) 不會使用任何意見反應。 這表示，相同訊息中的任何純文字區塊 (或相同金鑰所加密的不同訊息中，) 轉換成相同的加密文字區塊。 初始化向量無法與此加密模式搭配使用。 如果加密文字區塊的單一位有混淆，則整個對應的純文字區塊也會有混淆。

</dd> <dt>

<span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**橢圓曲線密碼編譯**
</dt> <dd>

 (ECC) 以橢圓曲線的屬性為基礎的公開金鑰加密方法。 ECC 的主要優點是提高效率，因為裝置變得較小，且安全性需求會更嚴苛。 例如，介於163位和512位之間的 ECC 金鑰是對等的安全性層級 RSA 金鑰大小的一到一 thirtieth。 金鑰大小會增加 ECC 增加的相對效率。

</dd> <dt>

<span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**編碼**
</dt> <dd>

將資料轉換為位元資料流的處理序。 編碼是將資料轉換為零 (0) 與壹 (1) 資料流之序列化處理序的一部分。

</dd> <dt>

<span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**編碼類型**
</dt> <dd>

是指用於憑證和訊息編碼的編碼類型。 編碼類型會指定為 **DWORD**，其中以低序位字組儲存的憑證編碼類型，以及儲存在高序位單字中的訊息編碼類型。 雖然某些函數或結構欄位只需要其中一種編碼類型，但一律可以接受兩者同時指定。

</dd> <dt>

<span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**加密**
</dt> <dd>

將純文字轉換成加密文字的程式，可協助防止未經授權的合作物件讀取和瞭解。 加密是解密的相反。

</dd> <dt>

<span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**加密的資料**
</dt> <dd>

已從純文字轉換成加密文字的資料。 加密的訊息會在傳送或儲存訊息時，用來偽裝訊息的內容。

</dd> <dt>

<span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**加密檔案系統**
</dt> <dd>

 (EFS) Windows 作業系統中的一項功能，可讓使用者對 NTFS 磁片區磁片上的檔案和資料夾進行加密，以防止入侵者存取這些檔案和資料夾。

</dd> <dt>

<span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**加密和解密功能**
</dt> <dd>

簡化的訊息函式，用來編碼和加密 (或解碼) 資料並將其解密。 這些函式是一組支援同時加密和解密資料的功能。

另請參閱 [*簡化的訊息函數*](s-gly.md)。

</dd> <dt>

<span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**增強型內容類型**
</dt> <dd>

PKCS 7 訊息中包含的資料類別 \# ，其中包含 (可能已加密) 的資料，以及雜湊或簽章等密碼編譯增強功能。 PKCS 7 所定義的增強型資料類型 \# 包括已簽署的資料、封包資料、簽署和封包資料，以及子集 (雜湊) 資料。

</dd> <dt>

<span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**增強金鑰使用方法**
</dt> <dd>

 (EKU) 憑證延伸和憑證擴充屬性值。 EKU 會指定憑證有效的用途。

</dd> <dt>

<span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**封包資料內容類型**
</dt> <dd>

PKCS \# 7 增強的內容，其中包含) 的加密內容 (，以及一或多個收件者)  (的內容加密金鑰。 收件者的加密內容和加密金鑰的組合稱為該收件者的 *數位信封* 。 當您想要保留訊息秘密的內容，並只允許指定的人員或實體抓取內容時，應該使用這種類型的訊息。

</dd> <dt>

<span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**交換金鑰**
</dt> <dd>

請參閱 *exchange 金鑰* 組。

</dd> <dt>

<span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**交換金鑰組**
</dt> <dd>

公開/私密金鑰組，可用來加密工作階段金鑰，使其能安全地儲存並與其他使用者交換。 交換金鑰組是藉由呼叫 **CryptGenKey** 函式來建立。

比較簽章 [*金鑰*](s-gly.md)組。

</dd> <dt>

<span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**外部存放區**
</dt> <dd>

在快取的記憶體（例如網路伺服器上的資料庫）中，維護其憑證、Crl 和 Ctl 的憑證存放區。 呼叫 **CertOpenStore** 函式時，外部存放區不會讀取和解碼其憑證、CRL 和 CTL。 讀取和解碼會延後，直到呼叫列舉或尋找方法為止。

</dd> </dl>

 

 



