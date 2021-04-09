---
description: 包含以字母 P 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: 'P (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850515"
---
# <a name="p-security-glossary"></a>P (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [](u-gly.md) [](v-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**填充**
</dt> <dd>

通常會在最後一個純文字區塊很短時加入的字串。 例如，如果區塊長度是64位，而最後一個區塊只包含40個位，則必須將24位的填補加入至最後一個區塊。 填補字串可能包含零、替代零和一或其他模式。 使用 [*CryptoAPI*](c-gly.md) 的應用程式不需要在其加密之前將填補新增至其純文字，也不需要在解密後將其移除。 這會自動處理。

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**密碼篩選**
</dt> <dd>

提供密碼原則強制執行和變更通知的 DLL。 由密碼篩選器所執行的函式是由 [*本地安全機構*](l-gly.md)呼叫。

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**持續性儲存體**
</dt> <dd>

當它的電源中斷連線時，任何保持不變的儲存媒體。 許多 [*憑證存放區*](c-gly.md) 資料庫都是持續性儲存的形式。

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**Pkcs**
</dt> <dd>

請參閱 *公開金鑰加密標準*。

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

根據 [RFC 3447](https://tools.ietf.org/html/rfc3447)中定義的 RSA 演算法來實行公開金鑰加密的建議標準。

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

RSA Data Security，Inc. 開發和維護的個人資訊交換語法標準此語法標準會指定可移植格式，以儲存或傳輸使用者的私密金鑰、憑證和其他秘密。

另請參閱 [*憑證*](c-gly.md) 和 *公開金鑰加密標準*。

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \# 7 簽署的資料**
</dt> <dd>

使用公開金鑰加密標準 \# 7 (PKCS 7) 簽署的資料物件， \# 並封裝用來簽署檔案的資訊。 通常，它會包含簽署者的憑證和 [*根憑證*](r-gly.md)。

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

密碼編譯訊息語法標準。 一種通用的資料語法，可套用在數位簽章與加密之類的密碼編譯上。 它也提供將憑證或憑證撤銷清單和其他訊息屬性（例如時間戳記）傳播至訊息的語法。

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS \_ 7 \_ ASN \_ 編碼**
</dt> <dd>

[*訊息編碼類型*](m-gly.md)。 訊息編碼類型會儲存在 **DWORD** (值的高序位字組中： 0x00010000) 。

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**明文**
</dt> <dd>

尚未加密的訊息。 純文字 (Plaintext) 訊息有時亦稱為「純文字」(Cleartext) 訊息。

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**可攜式可執行檔 (PE) 映射**
</dt> <dd>

標準 Windows 可執行檔案格式。

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**Prf**
</dt> <dd>

請參閱 *虛擬隨機函數*。

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**主要認證**
</dt> <dd>

MsV1 \_ 0 authentication 套件會定義主要認證金鑰字串值：主要認證字串會保留初始登入時提供的認證。 它包含使用者名稱，以及區分大小寫且區分大小寫的使用者密碼格式。

另請參閱 [*補充認證*](s-gly.md)。

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**主要服務提供者**
</dt> <dd>

提供卡片控制項介面的服務提供者。 每個智慧卡都可以在智慧卡資料庫中註冊其主要服務提供者。

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**主要權杖**
</dt> <dd>

通常只由 Windows 核心建立的存取權杖。 它可能會指派給處理常式，以代表該進程的預設安全性資訊。

另請參閱 [*存取權杖*](a-gly.md) 和模擬 [*權杖*](i-gly.md)。

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**主要**
</dt> <dd>

請參閱 [*安全性主體*](s-gly.md)。

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**隱私**
</dt> <dd>

從 view 或 secret 隔離的條件。 就訊息而言，私用訊息是加密的訊息，其文字會隱藏在視野之外。 就金鑰而言，私密金鑰是與其他金鑰隱藏的秘密金鑰。

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**私密金鑰**
</dt> <dd>

公開金鑰演算法中所使用之金鑰組的密碼一半。 一般來說，私密金鑰可用來加密對稱工作階段金鑰、對訊息進行數位簽署，或是針對使用對應公開金鑰加密的訊息進行解密。

另請參閱 *公開金鑰*。

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**私密金鑰 BLOB**
</dt> <dd>

包含完整公開/私密金鑰組的金鑰 BLOB。 系統管理程式會使用私密金鑰 Blob 來傳輸金鑰組。 因為金鑰組的私密金鑰部分非常機密，所以這些 Blob 通常會以對稱加密來加密。 這些金鑰 Blob 也可供高階應用程式使用，其中金鑰組會儲存在應用程式中，而不是依賴 CSP 的儲存機制。 藉由呼叫 **CryptExportKey** 函數來建立金鑰 BLOB。

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**特權**
</dt> <dd>

使用者用來執行各種系統相關作業的權限，例如關閉系統、載入裝置驅動程式，或是變更系統時間等等。 使用者的存取權杖包含使用者或使用者群組所持有的許可權清單。

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**過程**
</dt> <dd>

應用程式賴以執行的安全性內容。 一般來說，安全性內容會與使用者相關聯，因此所有在特定處理序下執行的應用程式都會具備擁有之使用者的權限。

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**>PROV \_ DSS**
</dt> <dd>

請參閱 *>prov \_ DSS 提供者類型*。

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**>PROV \_ DSS 提供者類型**
</dt> <dd>

預先定義的提供者類型，僅支援數位簽章和雜湊。 它會指定 DSA 簽名演算法，以及 MD5 和 SHA-1 雜湊演算法。

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**>PROV \_ DSS \_ DH**
</dt> <dd>

請參閱 *>prov \_ DSS \_ DH 提供者類型*。

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**>PROV \_ DSS \_ DH 提供者類型**
</dt> <dd>

預先定義的提供者類型，可提供金鑰交換、數位簽章和雜湊演算法。 它類似于 >PROV \_ DSS 提供者類型。

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**>PROV \_ FORTEZZA**
</dt> <dd>

請參閱 *>prov \_ FORTEZZA 提供者類型*。

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**>PROV \_ FORTEZZA 提供者類型**
</dt> <dd>

預先定義的提供者類型，可提供金鑰交換、數位簽章、加密和雜湊演算法。 此提供者類型所指定的密碼編譯通訊協定和演算法，是由美國國家標準和技術協會所擁有 (NIST) 。

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**>PROV \_ MS \_ EXCHANGE**
</dt> <dd>

請參閱 *>prov \_ MS \_ EXCHANGE 提供者類型*。

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**>PROV \_ MS \_ EXCHANGE 提供者類型**
</dt> <dd>

預先定義的提供者類型，專為 Microsoft Exchange 的需求以及與 Microsoft Mail 相容的其他應用程式所設計。 它提供了金鑰交換、數位簽章、加密和雜湊演算法。

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**>PROV \_ RSA \_ FULL**
</dt> <dd>

請參閱 *>prov \_ RSA \_ 完整提供者類型*。

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**>PROV \_ RSA \_ 完整提供者類型**
</dt> <dd>

由 Microsoft 和 RSA Data Security，Inc. 定義的預先定義提供者類型。此一般目的提供者類型提供了金鑰交換、數位簽章、加密和雜湊演算法。 金鑰交換、數位簽章和加密演算法是以 RSA 公開金鑰加密為基礎。

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**>PROV \_ RSA \_ SIG**
</dt> <dd>

請參閱 *>prov \_ RSA \_ SIG 提供者類型*。

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**>PROV \_ RSA \_ SIG 提供者類型**
</dt> <dd>

由 Microsoft 和 RSA 資料安全性定義的預先定義提供者類型。 此提供者類型是 >PROV \_ RSA FULL 的子集 \_ ，僅提供數位簽章和雜湊演算法。 數位簽章演算法是 RSA 公開金鑰演算法。

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**>PROV \_ SSL**
</dt> <dd>

請參閱 *>prov \_ SSL 提供者類型*。

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**>PROV \_ SSL 提供者類型**
</dt> <dd>

支援安全通訊端層 (SSL) 通訊協定的預先定義提供者類型。 此類型提供金鑰加密、數位簽章、加密和雜湊演算法。 可從 Netscape communication Corp 取得說明 SSL 的規格。

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**供應商**
</dt> <dd>

請參閱 [*密碼編譯服務提供者*](c-gly.md)。

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**提供者名稱**
</dt> <dd>

用來識別 CSP 的名稱。 例如，Microsoft 基底密碼編譯提供者版本1.0。 通常會在呼叫 **CryptAcquireCoNtext** 函式以連接至 CSP 時使用提供者名稱。

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**提供者類型**
</dt> <dd>

用來識別密碼編譯服務提供者類型 (CSP) 的詞彙。 Csp 會分組為不同的提供者類型，以代表標準資料格式和通訊協定的特定系列。 相較于 CSP 的唯一提供者名稱，提供者類型對指定的 CSP 而言並不是唯一的。 通常會在呼叫 **CryptAcquireCoNtext** 函式以連接至 CSP 時使用提供者類型。

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**虛擬隨機函式**
</dt> <dd>

 (PRF) 一個函式，該函式會採用索引鍵、標籤和種子做為輸入，然後產生任意長度的輸出。

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**公開/私密金鑰組**
</dt> <dd>

一組用在公開金鑰密碼編譯上的密碼編譯金鑰。 針對每個使用者，CSP 通常會維護兩組公開/私密金鑰組：交換金鑰組和數位簽章金鑰組。 兩組金鑰不管任何工作階段都會受到維護。

請參閱 [*exchange 金鑰*](e-gly.md) 組和簽章 [*金鑰*](s-gly.md)組。

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**公開金鑰**
</dt> <dd>

解密工作階段金鑰或數位簽章時，慣常使用的密碼編譯金鑰。 公開金鑰也可以用來加密訊息，以保證只有擁有對應之私密金鑰的使用者才能解密訊息。

另請參閱 *私密金鑰*。

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**公開金鑰演算法**
</dt> <dd>

使用兩個金鑰的非對稱式加密，一個用於加密、公開金鑰和另一個用於解密，也就是私用金鑰。 如同金鑰名稱所暗示，用來將純文字編碼的公開金鑰可供任何人使用。 不過，私密金鑰必須保持秘密。 只有私密金鑰可以解密加密文字。 在此程式中使用的公開金鑰演算法很慢 (的順序比) 1000 的對稱演算法慢，而且通常用來加密工作階段金鑰或數位簽署訊息。

另請參閱 *公開金鑰* 和 *私密金鑰*。

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**公開金鑰 BLOB**
</dt> <dd>

用來儲存公開/私密金鑰組之公開金鑰部分的 BLOB。 公開金鑰 Blob 未加密，因為包含在中的公開金鑰不是秘密。 公開金鑰 BLOB 是藉由呼叫 **CryptExportKey** 函式所建立。

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**公開金鑰密碼編譯標準**
</dt> <dd>

 (PKCS) 一組涵蓋安全性功能的公開金鑰加密語法標準，包括簽署資料的方法、交換金鑰、要求憑證、公開金鑰加密和解密，以及其他安全性功能。

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**公開金鑰加密**
</dt> <dd>

使用一組金鑰來加密，其中一支金鑰用來加密資料，而另一支用來解密資料。 反之，對稱的加密演算法會使用相同的金鑰來進行加密與解密。 在實務上，公開金鑰加密通常用來保護對稱式加密演算法所使用的工作階段金鑰。 在此情況下，會使用公開金鑰來加密工作階段金鑰，而過去則是用它來加密一些資料，而私密金鑰則是用來解密。 除了保護工作階段金鑰之外，公開金鑰密碼編譯同時也可用來數位簽署訊息 (使用私密金鑰) 並驗證簽章 (使用公開金鑰)。

另請參閱 *公開金鑰演算法*。

</dd> </dl>

 

 



