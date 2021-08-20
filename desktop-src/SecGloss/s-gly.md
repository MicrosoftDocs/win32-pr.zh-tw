---
description: 包含以字母 S 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: " (安全性詞彙) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99805289ca49b0505a1bbba292ec5fc7753e684aa08d4b5f0ac464f9160633ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969946"
---
# <a name="s-security-glossary"></a> (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [](u-gly.md) [](v-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) S [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

請參閱 *安全/多用途網際網路郵件延伸*。

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**SACL**
</dt> <dd>

請參閱 *系統存取控制清單*。

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**salt 值**
</dt> <dd>

有時包含為工作階段金鑰一部分的亂數據。 當新增至工作階段金鑰時，純文字 salt 資料會放在加密的金鑰資料前面。 系統會新增 Salt 值以增加掛接暴力密碼破解 (字典所需的工作，) 攻擊以對稱金鑰加密加密的資料。 Salt 值是藉由呼叫 **CryptGenRandom** 產生的。

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**山 姆**
</dt> <dd>

請參閱 *安全性帳戶管理員*。

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**淨化的名稱**
</dt> <dd>

憑證授權單位單位的形式 (CA) 名稱，用於檔案名 (例如 [*憑證撤銷清單*](c-gly.md)) 和登錄機碼中。 若要移除檔案名、登錄機碼名稱或辨別名稱值不合法的字元，或因技術特定的原因而不合法的字元，則必須進行清理 CA 名稱的程式。 在憑證服務中，清理程式會將 CA 一般名稱中的任何不合法字元轉換成格式的5字元標記法 **！**_xxxx_，其中 **！** 是當做 escape 字元使用， *xxxx* 代表可唯一識別要轉換之字元的四個十六進位整數。

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**SAS**
</dt> <dd>

請參閱 *安全的關注順序*。

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**捨棄 $ DefaultReaders**
</dt> <dd>

終端機讀取器群組，其中包含指派給該終端機的所有讀取器，但不會保留給此特定用途。

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**捨棄 $ AllReaders**
</dt> <dd>

智慧卡全系統讀取器群組，其中包含智慧卡資源管理員引進的所有讀者。 當讀取器引進系統時，系統會自動將讀者新增至群組。

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**捨棄 \_ AUTOALLOCATE**
</dt> <dd>

智慧卡系統常數，會告知智慧卡資源管理員配置足夠的記憶體，並傳回已配置緩衝區的指標，而不是填入使用者提供的緩衝區。 傳回的緩衝區最後必須藉由呼叫 **SCardFreeMemory** 來釋放。

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

請參閱 *簡單憑證註冊通訊協定*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**頻道**
</dt> <dd>

在用戶端和伺服器之間提供驗證的安全性封裝。

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**安全的關注順序**
</dt> <dd>

 (SAS) 開始或關閉登入程式的金鑰順序。 預設序列是 CTRL + ALT + DEL。

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**安全的電子交易**
</dt> <dd>

 (設定) 透過網際網路保護電子交易的通訊協定。

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**安全雜湊演算法**
</dt> <dd>

 (SHA) 產生訊息摘要的雜湊演算法。 SHA 專門用在數位簽章標準 (DSS) 的數位簽章演算法 (DSA) 中。 CryptoAPI 會依據演算法的識別碼來參考此演算法 (CALG \_ sha) 、name (SHA) 以及類別 (ALG \_ 類別 \_ 雜湊) 。 SHA 共衍生出四種強度不同的演算法：SHA-1、SHA-256、SHA-384，與 SHA-512。 SHA-1 可產生 160 位元的訊息摘要。 SHA-256、SHA-384，與 SHA-512 可分別產生 256 位元、384 位元，與 512 位元的訊息摘要。 SHA 是由美國國家標準與技術局 (NIST) 與美國國家安全局 (NSA) 所共同開發出來的標準。

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**安全雜湊標準**
</dt> <dd>

NIST 和 NSA 所設計的標準。 此標準會定義 (SHA-1) 的安全雜湊演算法，以搭配數位簽章標準 (DSS) 使用。

另請參閱 *安全雜湊演算法*。

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**安全通訊端層通訊協定**
</dt> <dd>

 (SSL) 使用公開和秘密金鑰技術的組合來進行安全網路通訊的通訊協定。

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**安全/多用途網際網路郵件延伸模組**
</dt> <dd>

 (S/MIME) 利用公開金鑰加密的電子郵件安全性標準。

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**安全性帳戶管理員**
</dt> <dd>

 (SAM) 登入過程中所使用的 Windows 服務。 SAM 會維護使用者帳戶資訊，包括使用者所屬的群組。

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**安全性內容**
</dt> <dd>

目前生效的安全性屬性或規則。 例如，目前登入電腦的使用者或由智慧卡使用者所輸入的個人識別碼。 對 SSPI 來說，安全性內容是一種不透明的資料結構，其中包含與連線相關的安全性資料，例如工作階段金鑰或是指出工作階段的持續時間。

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**安全描述項**
</dt> <dd>

結構和相關聯的資料，其中包含安全物件的安全性資訊。 安全描述項會識別物件的擁有者和主要群組。 它也可以包含控制物件存取權的 DACL，以及控制存取物件之嘗試記錄的 SACL。

另請參閱 [*絕對安全描述項*](a-gly.md)、 [*任意存取控制清單*](d-gly.md)、 *自我相關安全描述項*、 *系統存取控制清單*。

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**安全識別碼**
</dt> <dd>

 (SID) 可識別使用者、群組和電腦帳戶之可變長度的資料結構。 第一次建立帳戶時，會在網路上的每個帳戶發出唯一的 SID。 Windows 中的內部進程指的是帳戶的 SID，而不是帳戶的使用者或組名。

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**安全性套件**
</dt> <dd>

安全性通訊協定的軟體實行。 安全性封裝包含在安全性支援提供者 Dll 或安全性支援提供者/驗證套件 Dll 中。

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**安全性通訊協定**
</dt> <dd>

規格，定義安全性相關的資料物件，以及如何使用物件來維護電腦系統安全性的相關規則。

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**安全性主體**
</dt> <dd>

安全性系統所識別的實體。 這些原則包括人類使用者，以及自發處理序。

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**安全性支援提供者**
</dt> <dd>

 (SSP) 動態連結程式庫 (DLL) ，藉由將一或多個安全性套件提供給應用程式來執行 SSPI。 每個安全性套件都能在應用程式的 SSPI 函式呼叫以及實際安全性模型的函式之間提供對應。 安全性套件支援 Kerberos 驗證和 Microsoft LAN Manager 等安全性通訊協定。

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**安全性支援提供者介面**
</dt> <dd>

 (SSPI) 傳輸層級應用程式之間的通用介面，例如 Microsoft 遠端程序呼叫 (RPC) 和安全性提供者，例如 Windows 分散式安全性。 SSPI 可讓傳輸應用程式呼叫其中一個安全性提供者來取得驗證的連線。 您不需要了解太多有關安全性通訊協定細節，就可以執行這些呼叫。

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**自我相關的安全描述項**
</dt> <dd>

將所有安全性資訊儲存在連續記憶體區塊中的安全描述項。

另請參閱 *安全描述項*。

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**序列 化**
</dt> <dd>

將資料轉換成一個字串和零的程式，以便能夠以序列方式進行傳輸。 編碼是此程式的一部分。

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**序列化的憑證存放區格式**
</dt> <dd>

 (.SST) 序列化的憑證存放區格式是唯一保留所有憑證存放區屬性的格式。 這在某些情況下很有用，例如使用自訂 EKU 屬性設定根目錄時，而且您想要將它們移到另一部電腦上。

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**伺服器**
</dt> <dd>

從用戶端電腦回應命令的電腦。 用戶端和伺服器會一起運作，以執行分散式應用程式功能。

另請參閱 [*client*](c-gly.md)。

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**伺服器憑證**
</dt> <dd>

是指用於伺服器驗證的憑證，例如向網頁瀏覽器驗證 web 伺服器。 當網頁瀏覽器用戶端嘗試存取安全的 web 伺服器時，伺服器會將其憑證傳送至瀏覽器，以允許它確認伺服器的身分識別。

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**伺服器閘道密碼編譯**
</dt> <dd>

 (SGC) *安全通訊端層* (SSL) 的延伸模組，可讓具有 Internet Information Services (IIS) 匯出版本的公司（例如金融機構）使用強式加密 (例如128位加密) 。

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**服務主體名稱**
</dt> <dd>

 (SPN) 用戶端用來唯一識別服務實例的名稱。 若您透過樹系在電腦上安裝多個服務執行個體，則每個執行個體都須有自己的 SPN。 如果用戶端可能會使用多個名稱來進行驗證，則指定的服務實例可以有多個 Spn

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**服務提供者 (智慧卡)**
</dt> <dd>

智慧卡子系統元件，可透過 COM 介面，提供特定智慧卡服務的存取權。

另請參閱 [*主要服務提供者*](p-gly.md)。

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**會話**
</dt> <dd>

在保護單一金鑰設定資料的原則下，訊息的交換作業。 例如，SSL 工作階段使用單一金鑰，來回傳送多則訊息。

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**工作階段金鑰**
</dt> <dd>

相對較短的密碼編譯金鑰，通常是由用戶端和以共用密碼為基礎的伺服器進行協商。 工作階段金鑰的存留期是由與其相關聯的會話所限制。 工作階段金鑰應該夠強，以在會話的存留期內承受加密分析。 傳送工作階段金鑰時，通常會使用金鑰交換金鑰來保護它們， (通常是非對稱金鑰) ，因此只有預期的收件者可以存取它們。 您可以藉由呼叫 **CryptDeriveKey** 函數，從雜湊值衍生工作階段金鑰。

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**工作階段金鑰衍生配置**
</dt> <dd>

指定從雜湊衍生金鑰的時機。 使用的方法取決於 CSP 型別。

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**設置**
</dt> <dd>

請參閱 *安全的電子交易*。

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**沙**
</dt> <dd>

安全雜湊演算法的 CryptoAPI 名稱，SHA-1。 其他雜湊演算法包括 [*MD2*](m-gly.md)、 [*MD4*](m-gly.md)和 [*MD5*](m-gly.md)。

另請參閱 *安全雜湊演算法*。

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**SHS**
</dt> <dd>

請參閱 *安全雜湊標準*。

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**希**
</dt> <dd>

請參閱 *安全性識別* 元。

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**簽章和資料驗證函數**
</dt> <dd>

簡化的訊息函式用來簽署外寄訊息，並確認已接收的訊息和相關資料中套用之簽章的真實性。

請參閱 *簡化的訊息函數*。

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**簽章憑證**
</dt> <dd>

包含公開金鑰的憑證，可用來驗證數位簽章。

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**簽名檔**
</dt> <dd>

包含特定 [*密碼編譯服務提供者*](c-gly.md) 之簽章 (CSP) 的檔案。 需要簽章檔案，以確保 CryptoAPI 能夠辨識 CSP。 CryptoAPI 會定期驗證此簽章，以確保 CSP 未遭到篡改。

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**簽名函數**
</dt> <dd>

用來建立及驗證數位簽章的函式。

另請參閱 *簡化的訊息函數*。

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**簽章金鑰組**
</dt> <dd>

用於驗證 (數位簽署) 訊息的公開/私密金鑰組。 簽章金鑰組是藉由呼叫 **CryptGenKey** 來建立。

另請參閱 [*exchange 金鑰*](e-gly.md)組。

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**簽章私用金鑰**
</dt> <dd>

簽章金鑰組的私密金鑰。

請參閱簽章 *金鑰* 組。

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**簽署和封包資料**
</dt> <dd>

PKCS 7 所定義的資料內容類型 \# 。 此資料類型是由一或多個收件者的加密內容，以及一或多個簽署者的雙向加密訊息雜湊組成。 雙重加密包含使用簽署者的私密金鑰進行加密，後面接著具有內容加密金鑰的加密。

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**簽署的資料**
</dt> <dd>

PKCS 7 所定義的資料內容類型 \# 。 此資料類型是由任何類型的內容加上加密的訊息雜湊所組成 (摘要) 零或多個簽署者的內容。 產生的雜湊可以用來確認簽署訊息的人員。 這些雜湊也會確認原始訊息在簽署訊息之後尚未經過修改。

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**簡單憑證註冊通訊協定**
</dt> <dd>

 (SCEP) 代表簡單憑證註冊通訊協定的縮寫。 此通訊協定目前為 draft 網際網路標準，可定義網路裝置與登錄授權單位之間的通訊 (遠端登入憑證) 。 如需詳細資訊，請參閱 [MICROSOFT SCEP 執行技術白皮書](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper)。

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**簡單金鑰 BLOB**
</dt> <dd>

以目的地使用者的金鑰交換公開金鑰加密的工作階段金鑰。 儲存工作階段金鑰或將工作階段金鑰傳送給另一位使用者時，會使用此金鑰 BLOB 類型。 藉由呼叫 **CryptExportKey** 來建立金鑰 BLOB。

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**簡化的訊息函數**
</dt> <dd>

訊息管理功能，例如訊息加密、解密、簽章和簽章驗證功能。 簡化的訊息函式的運作層級高於基底加密函式或低層級訊息函數。 簡化的訊息函式會將數個基本密碼編譯、低層級訊息和憑證函式包裝成單一函式，以特定方式執行特定工作，例如加密 PKCS \# 7 訊息或簽署訊息。

另請參閱 [*低層級的訊息函數*](l-gly.md)。

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**單一登入**
</dt> <dd>

 (SSO) 將 Microsoft 帳戶 (（例如 Microsoft Outlook .com 帳戶）連結至本機帳戶的能力，讓一個登入可讓使用者使用其他支援以其) 登入的應用程式。

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**SIP**
</dt> <dd>

請參閱 *主體介面套件*。

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**網站憑證**
</dt> <dd>

伺服器憑證和 [*憑證授權單位*](c-gly.md) 單位 (CA) 憑證有時稱為網站憑證。 參考伺服器憑證時，憑證會識別出提供憑證的網頁伺服器。 參考 CA 憑證時，憑證會識別發出伺服器和/或用戶端驗證憑證給要求這些憑證之伺服器和用戶端的 CA。

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Skipjack**
</dt> <dd>

指定為 Fortezza 加密 suite 一部分的加密演算法。 Skipjack 是具有固定金鑰長度80位的對稱式加密。 Skipjack 是美國國家安全機構 (NSA) 所建立的分類演算法。 Skipjack 演算法的技術詳細資料是秘密。

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**智慧卡**
</dt> <dd>

整合式電路 (ICC) 由個人或群組所擁有，而該群組的資訊必須根據特定擁有權指派來保護。 它會提供自己的實體存取控制;沒有智慧卡子系統在智慧卡上放置額外的存取控制。 智慧卡是一張塑膠卡，包含與 ISO 7816 相容的整合電路。

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**智慧卡通用對話方塊**
</dt> <dd>

可協助使用者選取和尋找智慧卡的通用對話方塊。 它可與智慧卡資料庫管理服務和讀取器服務搭配使用，以協助應用程式，並視需要使用者識別要用於特定用途的智慧卡。

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**智慧卡資料庫**
</dt> <dd>

資源管理員用來管理資源的資料庫。 它包含已知的智慧卡清單、每張卡片的介面和主要服務提供者，以及已知的智慧卡讀取器和讀者群組。

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**智慧卡子系統**
</dt> <dd>

用來提供智慧卡讀卡機與智慧卡感知應用程式之間連結的子系統。

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**軟體 Publisher 憑證**
</dt> <dd>

 (SPC) \# 包含 x.509 憑證的 PKCS 7 帶正負號資料物件。

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**SPC**
</dt> <dd>

請參閱 *軟體 Publisher 憑證*。

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**SPN**
</dt> <dd>

請參閱 *服務主體名稱*。

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**SSL**
</dt> <dd>

請參閱 *安全通訊端層的通訊協定*。

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**SSL3 用戶端驗證演算法**
</dt> <dd>

安全通訊端層 (SSL) 第3版中的用戶端驗證所使用的演算法。 在 SSL3 通訊協定中，MD5 雜湊和 SHA-1 雜湊的串連會以 RSA 私密金鑰進行簽署。 CryptoAPI 和 Microsoft Base 和增強型密碼編譯提供者支援 SSL3，雜湊類型為 CALG \_ SSL3 \_ SHAMD5。

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**SSL3 通訊協定**
</dt> <dd>

安全通訊端層 (SSL) 通訊協定的第3版。

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**SSO**
</dt> <dd>

請參閱 *單一登入*。

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**過磷酸鈣**
</dt> <dd>

請參閱 *安全性支援提供者*。

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**SSPI**
</dt> <dd>

請參閱 *安全性支援提供者介面*。

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**SST**
</dt> <dd>

請參閱已 *序列化的憑證存放區格式*。

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**狀態**
</dt> <dd>

所有與密碼編譯實體相關聯之保存值的集合，例如金鑰或雜湊。 此集合可以包含 (IV) 使用的 [*初始化向量*](i-gly.md) 、正在使用的演算法，或已計算的實體值等專案。

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**資料流程加密**
</dt> <dd>

一次連續加密資料的密碼。

另請參閱 [*封鎖密碼*](b-gly.md)。

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**子驗證套件**
</dt> <dd>

選擇性 DLL，可提供額外的驗證功能，通常是藉由擴充驗證演算法來進行。 如果已安裝子驗證套件，驗證套件將會先呼叫子驗證封裝，然後再將其驗證結果傳回給 (LSA) 的「本地安全機構」。

另請參閱「 [*本地安全機構*](l-gly.md)」。

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**主體介面套件**
</dt> <dd>

 (SIP) 軟體層的 Microsoft 專屬規格，可讓應用程式建立、儲存、取出及驗證主體簽章。 主題包括（但不限於）可移植的可執行映射 (.exe) 、封包 (.cab) 影像、一般檔案和類別目錄檔案。 每個主體類型都會針對雜湊計算使用不同的資料子集，而且需要不同的儲存和抓取程式。 因此，每個主體類型都有唯一的主體介面套件規格。

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

一組由美國國家安全機關公開的密碼編譯演算法，作為其密碼編譯現代化計畫的一部分。

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**補充認證**
</dt> <dd>

用來向外部安全性網域驗證 *安全性主體* 的認證。

另請參閱 [*主要認證*](p-gly.md)。

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**對稱演算法**
</dt> <dd>

一種密碼編譯演算法，通常會使用單一金鑰（通常稱為工作階段金鑰）進行加密和解密。 對稱演算法可以分為兩個類別，也就是串流演算法和區塊演算法 (也稱為「 *資料流程* 」和「 [*封鎖」密碼*](b-gly.md)) 。

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**對稱式加密**
</dt> <dd>

在加密與解密過程中，使用單一金鑰的加密作業。 針對大量資料進行加密時，通常會使用對稱加密。 一些較常見的對稱式加密演算法為 [*RC2*](r-gly.md)、 [*RC4*](r-gly.md)和 [*資料加密標準*](d-gly.md) (DES) 。

另請參閱 [*公開金鑰加密*](p-gly.md)。

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**對稱金鑰**
</dt> <dd>

與對稱式密碼編譯演算法搭配使用的秘密金鑰 (也就是使用相同金鑰的演算法進行加密和解密) 。 所有通訊方都必須知道這類金鑰。

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**系統存取控制清單**
</dt> <dd>

 (SACL) ACL 來控制要嘗試存取安全物件的 audit 訊息產生。 取得或設定物件之 SACL 的能力，是由通常只有系統管理員所持有的許可權所控制。

另請參閱 [*存取控制清單*](a-gly.md)、 [*任意存取控制清單*](d-gly.md)、 [*許可權*](p-gly.md)。

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**系統程式介面**
</dt> <dd>

[*密碼編譯服務提供者*](c-gly.md)所提供的一組函式 (CSP) ，可執行應用程式的功能。

</dd> </dl>

 

 



