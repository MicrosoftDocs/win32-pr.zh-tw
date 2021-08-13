---
description: 包含以字母 C 為開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: 'C (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3196913ae4e6b7cba256a5bc7978666dda0e0ca2b78760c40dd8793f4d2b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895716"
---
# <a name="c-security-glossary"></a>C (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**約**
</dt> <dd>

請參閱 *憑證授權單位* 單位。

</dd> <dt>

<span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA 憑證**
</dt> <dd>

識別 (CA) 的憑證授權單位單位，可對要求這些憑證的伺服器和用戶端發出伺服器和用戶端驗證憑證。 由於此憑證包含數位簽章中所用的公開金鑰，因此也稱為「簽章憑證」(Signature Certificate)。 如果 CA 是根授權單位，CA 憑證可能稱為根憑證。 有時亦稱為「網站憑證」(Site Certificate)。

</dd> <dt>

<span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA 階層**
</dt> <dd>

憑證授權單位單位 (CA) 階層包含多個 Ca。 其組織方式是讓每個 CA 都經過較高層級階層中的另一個 CA 認證，直到達到階層的最上層（也稱為「根授權單位」）為止。

</dd> <dt>

<span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG \_ DH \_ EPHEM**
</dt> <dd>

用於產生暫時金鑰時，Diffie-Hellman 金鑰交換演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*diffie-hellman (暫時) 金鑰交換演算法*](d-gly.md)。

</dd> <dt>

<span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG \_ DH \_ SF**
</dt> <dd>

用於產生儲存和轉寄索引鍵的 Diffie-Hellman 金鑰交換演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*diffie-hellman (儲存和轉寄) 的金鑰交換演算法*](d-gly.md)。

</dd> <dt>

<span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG \_ HMAC**
</dt> <dd>

以雜湊為基礎的訊息驗證碼演算法的 CryptoAPI 演算法識別碼。

另請參閱以 [*雜湊為基礎的訊息驗證碼*](h-gly.md)。

</dd> <dt>

<span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG \_ MAC**
</dt> <dd>

訊息驗證碼演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*訊息驗證碼*](m-gly.md)。

</dd> <dt>

<span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG \_ MD2**
</dt> <dd>

MD2 雜湊演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*MD2 演算法*](m-gly.md)。

</dd> <dt>

<span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG \_ MD5**
</dt> <dd>

MD5 雜湊演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*MD5 演算法*](m-gly.md)。

</dd> <dt>

<span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG \_ RC2**
</dt> <dd>

RC2 區塊加密演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*RC2 區塊演算法*](r-gly.md)。

</dd> <dt>

<span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG \_ RC4**
</dt> <dd>

RC4 資料流程加密演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*RC4 串流演算法*](r-gly.md)。

</dd> <dt>

<span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG \_ RSA \_ KEYX**
</dt> <dd>

使用於金鑰交換時的 RSA 公開金鑰演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*RSA 公開金鑰演算法*](r-gly.md)。

</dd> <dt>

<span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG \_ RSA \_ SIGN**
</dt> <dd>

用來產生數位簽章時，RSA 公開金鑰演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*RSA 公開金鑰演算法*](r-gly.md)。

</dd> <dt>

<span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG \_ SHA**
</dt> <dd>

 (SHA-1) 的安全雜湊演算法的 CryptoAPI 演算法識別碼。

另請參閱 [*安全雜湊演算法*](s-gly.md)。

</dd> <dt>

<span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**投**
</dt> <dd>

由 c. 所開發的一組 DES 對稱封鎖密碼。 Adams 和 S. E。 塔瓦雷斯。 >PROV \_ MS \_ EXCHANGE 提供者類型會指定使用64位區塊大小的特定轉換演算法。

</dd> <dt>

<span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**Cbc**
</dt> <dd>

請參閱 *加密區塊鏈*。

</dd> <dt>

<span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**證書**
</dt> <dd>

包含實體與實體公開金鑰相關資訊的數位簽署陳述式，因此會將這兩個資訊片段繫結在一起。 憑證是由信任的組織 (或稱為 *憑證授權單位單位) 證書 (頒發機構* 單位的實體在 ca 驗證該實體是否為其所指的實體之後) 。

憑證可包含不同的資料類型。 例如，X.509 憑證包含憑證格式、憑證序號、用來簽署憑證的演算法、發行憑證的 CA 名稱、要求憑證的實體名稱與其公開金鑰，以及 CA 的簽章。

</dd> <dt>

<span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**憑證 BLOB**
</dt> <dd>

包含憑證資料的 BLOB。

憑證 BLOB 是由呼叫 **CryptEncodeObject** 所建立。 當呼叫的輸出包含所有憑證資料時，此程式就會完成。

</dd> <dt>

<span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**憑證內容**
</dt> <dd>

\_憑證內容結構，其中包含憑證存放區的控制碼、原始編碼憑證 BLOB 的指標、憑證 \_ 資訊結構的指標，以及編碼類型成員。 它是包含大部分憑證資訊的 **CERT \_ 資訊** 結構。

</dd> <dt>

<span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**憑證編碼/解碼函數**
</dt> <dd>

管理將憑證和相關材質轉譯成可在不同環境中使用之標準二進位格式的函式。

</dd> <dt>

<span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**憑證編碼類型**
</dt> <dd>

定義憑證的編碼方式。 憑證編碼類型會儲存在編碼類型 (**DWORD**) 結構的低序位字組中。

</dd> <dt>

<span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**透過 CMS 的憑證管理**
</dt> <dd>

Cmc。 透過 CMS 的憑證管理。 CMC 是一種憑證管理通訊協定，它會使用 (CMS) 的密碼編譯訊息語法。 在將要求傳送至註冊伺服器之前，Microsoft 會包裝 [*PKCS \# 7*](p-gly.md) (CMS) 要求物件中的 CMC 憑證要求。

</dd> <dt>

<span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**憑證名稱 BLOB**
</dt> <dd>

憑證中包含的名稱資訊編碼標記法。 每個名稱 BLOB 都會對應到 **憑證 \_ 名稱 \_ blob** 結構。

例如， **cert \_ 資訊** 結構所參考的簽發者和主體資訊會儲存在兩個 **憑證 \_ 名稱 \_ BLOB** 結構中。

</dd> <dt>

<span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**憑證原則**
</dt> <dd>

一組命名規則，指出具有一般安全性需求之特定應用程式類別的憑證適用性。 例如，這類原則可能會將特定憑證限制在指定價格限制內的電子資料交換交易。

</dd> <dt>

<span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**憑證要求**
</dt> <dd>

特殊格式的電子郵件 (傳送給 CA) 用來要求憑證。 要求必須包含 CA 驗證要求所需的資訊，以及要求憑證之實體的公開金鑰。

建立要求所需的所有資訊都會對應到 **CERT \_ 要求 \_ 資訊** 結構。

</dd> <dt>

<span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**憑證撤銷清單**
</dt> <dd>

 (CRL) 由憑證授權單位單位維護及發佈的檔 (CA) ，其中列出不再有效的 CA 所發行的憑證。

</dd> <dt>

<span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**憑證伺服器**
</dt> <dd>

針對特定 CA 發行憑證的伺服器。 憑證伺服器軟體提供可自訂的服務，可用來發行和管理在採用公開金鑰加密的安全性系統中所使用的憑證。

</dd> <dt>

<span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**憑證服務**
</dt> <dd>

針對特定 *憑證授權單位* 單位發行憑證 (CA) 的軟體服務。 它提供可自訂的服務來發行和管理企業的憑證。 憑證可以用來提供驗證支援，包括安全電子郵件、web 驗證，以及智慧卡驗證。

</dd> <dt>

<span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**憑證存放區**
</dt> <dd>

一般來說，指的是用來存放憑證、憑證撤銷清單 (CRL)，以及憑證信任清單 (CTL) 的永久存放區。 然而，當您使用不需要存放在永久存放區的憑證時，可以單純在記憶體中建立並開啟憑證存放區。

憑證存放區是 CryptoAPI 中許多憑證功能的核心。

</dd> <dt>

<span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**憑證存放區功能**
</dt> <dd>

管理儲存體和抓取資料的函式，例如憑證、憑證撤銷清單 (Crl) ，以及 (Ctl) 的憑證信任清單。 這些函式可分成一般憑證函式、憑證撤銷清單函式，以及憑證信任清單功能。

</dd> <dt>

<span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**憑證範本**
</dt> <dd>

設定檔的 Windows 結構 (亦即，它會根據其預期的使用方式來 prespecifies 格式和內容) 。 向 Windows 的企業 *憑證授權單位* 單位 (CA) 要求 [*憑證*](/windows)時，憑證要求者是根據其存取權限，可以從以憑證範本為基礎的各種憑證類型（例如使用者和程式碼簽署）進行選取。

</dd> <dt>

<span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**憑證信任清單**
</dt> <dd>

 (CTL) 由受信任實體簽署的預先定義專案清單。 CTL 可以任何形式出現，例如憑證的雜湊清單，或是檔案名稱清單。 清單裡的所有項目都會經由簽署實體加以驗證 (核准)。

</dd> <dt>

<span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**憑證授權單位單位**
</dt> <dd>

 (CA) 信賴于發出憑證的實體，其會判斷提示要求憑證的收件者個人、電腦或組織是否滿足已建立原則的條件。

</dd> <dt>

<span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**Cfb**
</dt> <dd>

請參閱 *加密意見* 反應。

</dd> <dt>

<span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**連結模式**
</dt> <dd>

一種區塊加密模式，藉由結合加密文字和純文字來引入意見反應。

另請參閱 *加密區塊鏈*。

</dd> <dt>

<span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**密碼**
</dt> <dd>

用來加密資料的密碼編譯演算法;亦即，使用預先定義的金鑰將純文字轉換成加密文字。

</dd> <dt>

<span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**加密區塊鏈**
</dt> <dd>

 (CBC) 運作對稱式區塊加密的方法，此加密方法會使用意見將先前產生的加密文字與新的純文字結合在一起。

在加密之前，每個純文字區塊都會與前一個區塊的加密文字合併，再加上位 **XOR** 運算。 結合加密文字和純文字可確保即使純文字包含許多相同的區塊，它們都會加密為不同的加密文字區塊。

使用 Microsoft 基底密碼編譯提供者時，CBC 是預設的加密模式。

</dd> <dt>

<span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**加密區塊連結 MAC**
</dt> <dd>

區塊加密方法，它會使用區塊密碼將基底資料加密，然後使用最後一個加密區塊做為雜湊值。 用來建立 [*訊息驗證碼*](m-gly.md) (MAC) 的加密演算法是建立工作階段金鑰時所指定的金鑰。

</dd> <dt>

<span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**加密意見反應**
</dt> <dd>

 (CFB) 一個區塊加密模式，它會以純文字格式處理少量的純文字，而不是一次處理整個區塊。

這個模式會使用一個區塊大小的 shift 暫存器，並將其分成數個區段。 例如，如果區塊大小是每次處理八個位的64位，則移位暫存器會分成八個區段。

</dd> <dt>

<span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**密碼模式**
</dt> <dd>

區塊加密模式 (每個區塊都會個別加密，) 可使用 **CryptSetKeyParam** 函式來指定。 如果應用程式未明確指定其中一種模式，則會使用 (CBC) cipher 模式的加密區塊鏈。

ECB：不使用任何意見反應的區塊加密模式。

CBC：藉由結合加密文字和純文字來引進意見反應的區塊加密模式。

CFB：一種區塊加密模式，可將純文字的小型遞增處理為加密文字，而不是一次處理整個區塊。

OFB：使用類似于 CFB 之意見反應的區塊加密模式。

</dd> <dt>

<span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**密文**
</dt> <dd>

已加密的訊息。

</dd> <dt>

<span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**明文**
</dt> <dd>

請參閱 [*純文字*](p-gly.md)。

</dd> <dt>

<span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**客戶**
</dt> <dd>

起始與伺服器之連接的應用程式，而不是伺服器應用程式。

與 [*伺服器*](s-gly.md)比較。

</dd> <dt>

<span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**用戶端憑證**
</dt> <dd>

是指用於用戶端驗證的憑證，例如在 web 伺服器上驗證網頁瀏覽器。 當網頁瀏覽器用戶端嘗試存取安全的 web 伺服器時，用戶端會將其憑證傳送至伺服器，以允許它驗證用戶端的身分識別。

</dd> <dt>

<span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**Cmc**
</dt> <dd>

請參閱透過 *CMS 的憑證管理*。

</dd> <dt>

<span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**天然氣**
</dt> <dd>

請參閱 *密碼編譯 API：新一代*。

</dd> <dt>

<span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**通訊協定**
</dt> <dd>

序列化資料的方法 (轉換成字串，) 和還原序列化。 此通訊協定是由軟體和資料傳輸硬體所控制。

一般來說，以圖層為根據，簡化通訊協定可能包含應用層、編碼/解碼層和硬體層。

</dd> <dt>

<span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**限制委派**
</dt> <dd>

允許伺服器將要求僅代表用戶端轉寄給指定服務清單的行為。

**Windows XP：** 不支援限制委派。

</dd> <dt>

<span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**上下文**
</dt> <dd>

與連接相關的安全性資料。 內容包含工作階段金鑰和會話持續時間等資訊。

</dd> <dt>

<span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**coNtext 函數**
</dt> <dd>

用來連線至密碼編譯服務提供者 (CSP) 的函式。 這些函式可讓應用程式依名稱選擇特定的 CSP，或使用所需的功能類別取得一個。

</dd> <dt>

<span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**副署**
</dt> <dd>

現有簽章和訊息的簽章，或現有簽章的簽章。 副署可用來簽署現有簽章的加密雜湊，或用來為訊息建立時間戳記。

</dd> <dt>

<span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**憑據**
</dt> <dd>

[*安全性主體*](s-gly.md)先前經過驗證的登入資料，可用來建立自己的身分識別，例如密碼或 Kerberos 通訊協定票證。

</dd> <dt>

<span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**Crl**
</dt> <dd>

請參閱 *憑證撤銷清單*。

</dd> <dt>

<span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT \_ ASN \_ 編碼**
</dt> <dd>

指定憑證編碼方式的編碼類型。 憑證編碼類型會以 **DWORD** 的低序位字組儲存 (值為： 0x00000001) 。 此編碼類型的功能與 X509 \_ ASN \_ 編碼編碼類型相同。

</dd> <dt>

<span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**加密分析**
</dt> <dd>

加密分析是中斷加密文字的藝術與科學。 相反地，保護訊息安全的藝術與科學是密碼編譯。

</dd> <dt>

<span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**
</dt> <dd>

應用程式開發介面，可讓應用程式開發人員將驗證、編碼和加密新增至以 Windows 為基礎的應用程式。

</dd> <dt>

<span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**密碼編譯演算法**
</dt> <dd>

用於加密和解密的數學函數。 大部分的密碼編譯演算法是以替代密碼、調換密碼或兩者的組合為基礎。

</dd> <dt>

<span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**密碼編譯摘要**
</dt> <dd>

單向雜湊函式，採用可變長度的輸入字串，並將它轉換成固定長度的輸出字串， (稱為密碼編譯摘要。 ) 此固定長度的輸出字串對於每個不同的輸入字串是機率唯一的，因此可作為檔案的指紋。 下載具有密碼編譯摘要的檔案時，接收者會旁邊摘要。 如果輸出字串符合檔案中包含的摘要，則接收者會證明接收的檔案未遭篡改，而且與原先傳送的檔案相同。

</dd> <dt>

<span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**密碼編譯金鑰**
</dt> <dd>

密碼編譯金鑰是初始化密碼編譯演算法所需的一段資料。 密碼編譯系統的設計通常是為了確保其安全性只取決於其密碼編譯金鑰的安全性，而不是在保持演算法秘密的情況下。

有許多不同類型的密碼編譯金鑰，對應至各種不同的密碼編譯演算法。 您可以根據用於 (的演算法類型來分類金鑰，例如對稱或非對稱金鑰) 。 它們也可以根據系統內的存留期進行分類 (例如，長期或工作階段金鑰) 。

</dd> <dt>

<span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**密碼編譯服務提供者**
</dt> <dd>

 (CSP) 獨立的軟體模組，此模組實際上會執行驗證、編碼和加密的密碼編譯演算法。

</dd> <dt>

<span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**密碼**
</dt> <dd>

資訊安全的藝術與科學。 它包含資訊機密性、資料完整性、實體驗證及資料來源驗證。

</dd> <dt>

<span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**密碼編譯 API**
</dt> <dd>

請參閱 *CryptoAPI*。

</dd> <dt>

<span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**密碼編譯 API：新一代**
</dt> <dd>

 (CNG) 第二次產生 *CryptoAPI*。 CNG 可讓您將現有的演算法提供者取代為您自己的提供者，並在可用時加入新的演算法。 CNG 也允許從使用者和核心模式應用程式使用相同的 Api。

</dd> <dt>

<span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**密碼**
</dt> <dd>

包含密碼編譯和加密分析的數學分支。

</dd> <dt>

<span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**
</dt> <dd>

搭配 *密碼編譯服務提供者* 使用的系統程式介面 (CSP) 。

</dd> <dt>

<span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**Csp**
</dt> <dd>

請參閱 *密碼編譯服務提供者*。

</dd> <dt>

<span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP 系列**
</dt> <dd>

唯一的 Csp 群組，使用相同的一組資料格式並以相同的方式執行其功能。 即使兩個 CSP 系列使用相同的演算法 (例如，RC2 區塊加密) 、其不同的填補配置、金鑰長度或預設模式都會使每個群組相異。 CryptoAPI 的設計目的是讓每個 CSP 類型都代表一個特定的系列。

</dd> <dt>

<span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP 名稱**
</dt> <dd>

CSP 的文字名稱。 如果 CSP 已經由 Microsoft 簽署，此名稱必須完全符合匯出合規性憑證 (ECC) 中所指定的 CSP 名稱。

</dd> <dt>

<span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP 類型**
</dt> <dd>

指出與提供者相關聯的 CSP 系列。 當應用程式連接到特定類型的 CSP 時，每個 CryptoAPI 函式預設會以對應至該 CSP 類型的系列所規定的方式運作。

</dd> <dt>

<span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**Ctl**
</dt> <dd>

請參閱 *憑證信任清單*。

</dd> <dt>

<span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK \_ MEK**
</dt> <dd>

一種加密演算法，使用40位的 DES 金鑰變異，其中16位的56位 DES 金鑰會設定為零。 此演算法會依照40位 DES 的 IETF 草稿規格中的指定來執行。 在撰寫本文時，可以在 ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt 找到草稿規格。 此演算法與 **ALG \_ 識別碼** 值 CALG \_ CYLINK MEK 搭配使用 \_ 。

</dd> </dl>

 

 
