---
description: 包含以字母 K 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: 'K (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7d1b474b774b5cdb7a0b8d05a512a8d291573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944624"
---
# <a name="k-security-glossary"></a>K (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](u-gly.md) [](v-gly.md) [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**KCA**
</dt> <dd>

請參閱 *主要憑證授權單位* 單位。

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**Kdc**
</dt> <dd>

請參閱 *金鑰發佈中心*。

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**KEA**
</dt> <dd>

請參閱 *金鑰交換演算法*。

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Kerberos 通訊協定**
</dt> <dd>

一種通訊協定，可定義用戶端與網路驗證服務的互動方式。 用戶端從 Kerberos 金鑰發佈中心 (KDC) 取得票證，並在建立連線時將這些票證呈交給伺服器。 Kerberos 票證代表用戶端的網路認證。

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**金鑰 BLOB**
</dt> <dd>

包含已加密之私密金鑰的 BLOB。 金鑰 Blob 提供將金鑰儲存在 CSP 外部的方法。 藉由呼叫 **CryptExportKey** 函式，從 CSP 匯出現有的金鑰，即可建立金鑰 blob。 稍後，您可以藉由呼叫 **CryptImportKey** 函式，將金鑰 BLOB 匯入至提供者， (通常不同電腦上的不同 CSP) 。 這會在 CSP 中建立金鑰，這個金鑰是匯出的複本。

另請參閱 [*簡單的金鑰 blob*](s-gly.md)、 [*公開金鑰 BLOB*](p-gly.md)和 [*私密金鑰 blob*](p-gly.md)。

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**金鑰 BLOB 格式**
</dt> <dd>

從 CSP 匯出公用或工作階段金鑰時，金鑰 BLOB 的格式。 格式是由匯出 CSP 的提供者類型所指定。 藉由呼叫 **CryptExportKey** 來建立金鑰 BLOB。

另請參閱 [*公開金鑰 blob*](p-gly.md) 和 [*簡單金鑰 blob*](s-gly.md)。

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**金鑰憑證授權單位單位**
</dt> <dd>

 (KCA) 受信任的實體，此實體通常會保留以 KCA 的私密金鑰簽署之複合訊息的安全資料庫。 在實際執行的情況下，複合訊息是由使用者的名稱、使用者的公開金鑰，以及使用者的任何其他重要資訊所組成。 當接收應用程式從使用者取得已簽署的訊息時，應用程式可以藉由將訊息與儲存在 KCA 資料庫中的公開金鑰進行比較，以驗證收到的公開金鑰。

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**金鑰容器**
</dt> <dd>

金鑰資料庫的一部分，其中包含 (exchange 和簽章金鑰組) 屬於特定使用者的所有金鑰組。 每個容器都有唯一的名稱，此名稱會在呼叫 **CryptAcquireCoNtext** 函式以取得容器的控制碼時使用。

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**金鑰資料庫**
</dt> <dd>

包含特定 CSP 之持續密碼編譯金鑰的資料庫。 資料庫包含一個或多個金鑰容器，可個別儲存特定使用者的所有密碼編譯金鑰組。

另請參閱 *金鑰容器*。

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**金鑰發佈中心**
</dt> <dd>

 (KDC) 一個網路服務，可提供用於 Kerberos V5 驗證通訊協定的會話票證和暫時工作階段金鑰。 KDC 會在所有網域控制站上以特殊許可權的進程的形式執行。

另請參閱 *Kerberos 通訊協定*。

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**金鑰交換演算法**
</dt> <dd>

用來加密和解密 exchange 金鑰的演算法)  (對稱工作階段金鑰。 某些常見的金鑰交換演算法包含 Diffie-Hellman 和 KEA，也就是 >PROV \_ FORTEZZA 提供者類型所指定的金鑰交換演算法。 KEA 演算法是 Diffie-Hellman 演算法的改良版。 每個提供者類型只能指定一個金鑰交換演算法。

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**金鑰交換演算法**
</dt> <dd>

 (KEA) 由 >PROV \_ FORTEZZA 提供者類型指定的金鑰交換演算法。 此演算法是 Diffie-Hellman 演算法的改良版。

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**金鑰交換憑證**
</dt> <dd>

用來加密傳送給另一方之資訊的憑證。 用戶端可以使用憑證授權單位單位 (CA) 金鑰 exchange 憑證來加密傳送至 CA 的資訊。

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**金鑰交換功能**
</dt> <dd>

一組用來交換或傳輸金鑰的函數。 金鑰交換函式也可以用來執行完整驗證的三階段金鑰交換。

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**金鑰-交換金鑰組**
</dt> <dd>

請參閱 [*exchange 金鑰*](e-gly.md)組。

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**金鑰交換私密金鑰**
</dt> <dd>

交換金鑰組的私密金鑰。

另請參閱 [*exchange 金鑰*](e-gly.md)組。

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**金鑰交換通訊協定**
</dt> <dd>

雙方用來交換資訊以建立共用機密的通訊協定。 共用密碼通常會用來作為對稱式加密金鑰。

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**金鑰交換公開金鑰**
</dt> <dd>

交換金鑰組的公開金鑰。

另請參閱 [*exchange 金鑰*](e-gly.md)組。

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**金鑰產生功能**
</dt> <dd>

應用程式用來產生和自訂密碼編譯金鑰的一組函數。 這些函式包含變更連結模式、初始化向量和其他加密功能的完整支援。

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**金鑰長度**
</dt> <dd>

由某些提供者指定的值，指出與該提供者一起使用之公開/私密金鑰組和工作階段金鑰的長度。

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**金鑰組**
</dt> <dd>

私密金鑰與其相關的公開金鑰。

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**金鑰儲存提供者**
</dt> <dd>

 (KSP) 獨立的軟體模組，其可執行建立、管理、儲存和取出 [*私密金鑰*](p-gly.md)的功能。

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

請參閱 *金鑰儲存提供者*。

</dd> </dl>

 

 



