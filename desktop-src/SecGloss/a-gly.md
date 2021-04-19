---
description: 包含以字母 A 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0baaa937-f635-4500-8dcd-9dbbd6f4cd02
title: " (安全性詞彙) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a3c9bd82d68a80d5a014c19e6c81dddf5e2b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990375"
---
# <a name="a-security-glossary"></a> (安全性詞彙) 

[B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_absolute_security_descriptor_gly"></span><span id="_SECURITY_ABSOLUTE_SECURITY_DESCRIPTOR_GLY"></span>**絕對安全描述項**
</dt> <dd>

安全描述項結構，包含與物件相關聯之安全性資訊的指標。

另請參閱 [*安全描述項*](s-gly.md) 和 [*自我相關安全描述項*](s-gly.md)。

</dd> <dt>

<span id="_security_abstract_syntax_notation_one_gly"></span><span id="_SECURITY_ABSTRACT_SYNTAX_NOTATION_ONE_GLY"></span>**抽象語法標記法 (一)**
</dt> <dd>

 (asn.1) 用來指定用於序列傳輸之抽象物件的方法。

</dd> <dt>

<span id="_security_access_block_gly"></span><span id="_SECURITY_ACCESS_BLOCK_GLY"></span>**存取區塊**
</dt> <dd>

金鑰 BLOB，其中包含用來加密檔案或訊息的對稱式加密金鑰。 存取區塊只能以私密金鑰開啟。

</dd> <dt>

<span id="_security_access_control_entry_gly"></span><span id="_SECURITY_ACCESS_CONTROL_ENTRY_GLY"></span>**存取控制專案**
</dt> <dd>

 (ACE) 存取控制清單中的專案 (ACL) 。 ACE 包含一組存取權限，以及 (SID) 的安全識別碼，可識別允許、拒絕或審核許可權的信任者。

另請參閱 *存取控制清單*、 [*安全識別碼*](s-gly.md)和 [*信任者*](t-gly.md)。

</dd> <dt>

<span id="_security_access_control_list_gly"></span><span id="_SECURITY_ACCESS_CONTROL_LIST_GLY"></span>**存取控制清單**
</dt> <dd>

 (ACL) 適用于物件的安全性保護清單。  (物件可以是檔案、進程、事件，或任何其他具有安全描述項的專案。 ) 存取控制清單中的專案 (ACL) 是 (ACE) 的存取控制專案。 有兩種類型的存取控制清單：任意和系統。

另請參閱 *存取控制專案*、 [*任意存取控制清單*](d-gly.md)、 [*安全描述項*](s-gly.md)和 [*系統存取控制清單*](s-gly.md)。

</dd> <dt>

<span id="_security_access_mask_gly"></span><span id="_SECURITY_ACCESS_MASK_GLY"></span>**存取遮罩**
</dt> <dd>

32位值，指定存取控制專案 (ACE) 中允許或拒絕的許可權。 存取遮罩也用來在物件開啟時要求存取權限。

另請參閱 *存取控制專案*。

</dd> <dt>

<span id="_security_access_token_gly"></span><span id="_SECURITY_ACCESS_TOKEN_GLY"></span>**存取權杖**
</dt> <dd>

存取權杖包含登入工作階段所需的安全性資訊。 系統會在使用者登入時建立存取權杖，而且每個代表使用者執行的處理序都會擁有該權杖的複本。 權杖可識別使用者、使用者群組，以及使用者權限。 系統會使用權杖來控制安全物件的存取權限，並控制使用者是否能夠在本機電腦上執行與系統相關的各種作業。 存取權杖有兩種：主要和模擬。

另請參閱模擬 [*權杖*](i-gly.md)、 [*主要權杖*](p-gly.md)、 [*許可權*](p-gly.md)、 [*進程*](p-gly.md)和 [*安全識別碼*](s-gly.md)。

</dd> <dt>

<span id="_security_ace_gly"></span><span id="_SECURITY_ACE_GLY"></span>**Ace**
</dt> <dd>

請參閱 *存取控制專案*。

</dd> <dt>

<span id="_security_acl_gly"></span><span id="_SECURITY_ACL_GLY"></span>**Acl**
</dt> <dd>

請參閱 *存取控制清單*。

</dd> <dt>

<span id="_security_aes_gly"></span><span id="_SECURITY_AES_GLY"></span>**進階加密標準**
</dt> <dd>

 (AES) 由美國國家標準和技術規範所指定的密碼編譯演算法 (NIST) 以保護機密資訊。

</dd> <dt>

<span id="_security_alg_class_data_encrypt_gly"></span><span id="_SECURITY_ALG_CLASS_DATA_ENCRYPT_GLY"></span>**ALG \_ 類別 \_ 資料 \_ 加密**
</dt> <dd>

資料加密演算法的 CryptoAPI 演算法類別。 典型的資料加密演算法包括 RC2 和 RC4。

</dd> <dt>

<span id="_security_alg_class_hash_gly"></span><span id="_SECURITY_ALG_CLASS_HASH_GLY"></span>**ALG \_ 類別 \_ 雜湊**
</dt> <dd>

雜湊演算法的 CryptoAPI 演算法類別。 典型的雜湊演算法包括 MD2、MD5、SHA-1 和 MAC。

</dd> <dt>

<span id="_security_alg_class_key_exchange_gly"></span><span id="_SECURITY_ALG_CLASS_KEY_EXCHANGE_GLY"></span>**ALG \_ 類別 \_ 金鑰 \_ 交換**
</dt> <dd>

金鑰交換演算法的 CryptoAPI 演算法類別。 典型的金鑰交換演算法是 RSA \_ KEYX。

</dd> <dt>

<span id="_security_alg_class_signature_gly"></span><span id="_SECURITY_ALG_CLASS_SIGNATURE_GLY"></span>**ALG \_ 類別簽章 \_**
</dt> <dd>

簽名演算法的 CryptoAPI 演算法類別。 典型的數位簽章演算法是 RSA \_ SIGN。

</dd> <dt>

<span id="_security_apdu_gly"></span><span id="_SECURITY_APDU_GLY"></span>**APDU**
</dt> <dd>

請參閱 *應用程式協定資料單位*。

</dd> <dt>

<span id="_security_application_protocol_data_unit_gly"></span><span id="_SECURITY_APPLICATION_PROTOCOL_DATA_UNIT_GLY"></span>**應用程式協定資料單位**
</dt> <dd>

 (APDU) 命令順序 (應用程式協定資料單位) （可由智慧卡傳送或由應用程式傳回）。

另請參閱 [*回復 APDU*](r-gly.md)。

</dd> <dt>

<span id="_security_application_protocol_gly"></span><span id="_SECURITY_APPLICATION_PROTOCOL_GLY"></span>**應用程式協定**
</dt> <dd>

通常位於傳輸層上方的通訊協定。 例如，HTTP、TELNET、FTP 和 SMTP 都是所有的應用程式協定。

</dd> <dt>

<span id="_security_asn.1_gly"></span><span id="_SECURITY_ASN.1_GLY"></span>**ASN. 1**
</dt> <dd>

請參閱 *抽象語法標記法 (一)*。

</dd> <dt>

<span id="_security_ascii_gly"></span><span id="_SECURITY_ASCII_GLY"></span>**Ascii**
</dt> <dd>

美國訊息交換標準代碼 (ASCII) 。 將數值指派給字母、數位、標點符號和某些其他字元的編碼配置。

</dd> <dt>

<span id="_security_asymmetric_algorithm_gly"></span><span id="_SECURITY_ASYMMETRIC_ALGORITHM_GLY"></span>**非對稱演算法**
</dt> <dd>

請參閱 [*公開金鑰演算法*](p-gly.md)。

</dd> <dt>

<span id="_security_asymmetric_key_gly"></span><span id="_SECURITY_ASYMMETRIC_KEY_GLY"></span>**非對稱金鑰**
</dt> <dd>

與非對稱式密碼編譯演算法搭配使用的其中一個金鑰。 這種演算法會使用兩個密碼編譯金鑰：加密的「公開金鑰」和「私密金鑰」以進行解密。 在簽章和驗證中，會反轉角色：公開金鑰是用來進行驗證，而私密金鑰則是用來產生簽章。 這類演算法最重要的功能是，它們的安全性並不依賴公開金鑰秘密的 (，不過，它可能會要求公開金鑰的真實性，例如，從信任的來源) 取得這些金鑰。 需要私密金鑰的密碼。 公開金鑰演算法的範例包括 [*數位簽章演算法 (DSA)*](d-gly.md)、橢圓曲線數位簽章演算法 (ECDSA) ，以及 Rivest-Shamir-ADLEMAN (RSA) 系列的演算法。

</dd> <dt>

<span id="_security_atr_string_gly"></span><span id="_SECURITY_ATR_STRING_GLY"></span>**ATR 字串**
</dt> <dd>

開啟時，從智慧卡傳回的位元組序列。 這些位元組會用來識別系統的卡片。

</dd> <dt>

<span id="_security_attribute_gly"></span><span id="_SECURITY_ATTRIBUTE_GLY"></span>**屬性**
</dt> <dd>

 (RDN) 的相對辨別名稱元素。 一些典型的屬性包括一般名稱、姓氏、電子郵件地址、郵件標籤和國家/地區名稱。

</dd> <dt>

<span id="_security_attribute_blob_gly"></span><span id="_SECURITY_ATTRIBUTE_BLOB_GLY"></span>**屬性 BLOB**
</dt> <dd>

憑證要求中所儲存之屬性資訊的編碼標記法。

</dd> <dt>

<span id="_security_audit_security_object_gly"></span><span id="_SECURITY_AUDIT_SECURITY_OBJECT_GLY"></span>**Audit security 物件**
</dt> <dd>

控制稽核原則子系統存取權的安全描述項。

</dd> <dt>

<span id="_security_authentication_gly"></span><span id="_SECURITY_AUTHENTICATION_GLY"></span>**認證**
</dt> <dd>

用於驗證使用者、電腦、服務或處理序為何者或是否符合自稱之身分的處理序。

</dd> <dt>

<span id="_security_authentication_package_gly"></span><span id="_SECURITY_AUTHENTICATION_PACKAGE_GLY"></span>**驗證套件**
</dt> <dd>

封裝用來判斷是否允許使用者登入之驗證邏輯的 DLL。 LSA 藉由將要求傳送至驗證套件來驗證使用者登入。 驗證封裝接著會檢查登入資訊，並驗證或拒絕使用者登入嘗試。

</dd> <dt>

<span id="_security_authenticode_gly"></span><span id="_SECURITY_AUTHENTICODE_GLY"></span>**驗證**
</dt> <dd>

Internet Explorer 的安全性功能。 Authenticode 可讓可下載的可執行程式碼 (外掛程式或 ActiveX 控制項，例如) 將數位憑證附加至其產品，以確保使用者的程式碼是來自原始開發人員，而且尚未改變。 Authenticode 可讓終端使用者自行決定是否要在下載前接受或拒絕在網際網路上張貼的軟體元件。

</dd> </dl>

 

 



