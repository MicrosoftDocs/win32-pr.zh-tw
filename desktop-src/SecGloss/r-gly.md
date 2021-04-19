---
description: 包含以字母 R 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: 'R (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978233"
---
# <a name="r-security-glossary"></a>R (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [](u-gly.md) [](v-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

RC2 演算法的 [*CryptoAPI*](c-gly.md) 演算法名稱。

另請參閱 *RC2 區塊演算法*。

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**RC2 區塊演算法**
</dt> <dd>

以 RC2 64 位對稱封鎖密碼為基礎的資料 [*加密*](e-gly.md) 演算法。 RC2 是由 >PROV \_ RSA \_ 完整提供者類型所指定。 [*CryptoAPI*](c-gly.md) 會依識別碼參考此演算法 (CALG \_ rc2) 、名稱 (RC2) 以及類別 (ALG \_ 類別 \_ 資料 \_ 加密) 。

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

RC4 演算法的 [*CryptoAPI*](c-gly.md) 演算法名稱。

另請參閱 *RC4 串流演算法*。

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**RC4 串流演算法**
</dt> <dd>

以 RC4 對稱資料流程加密為基礎的資料 [*加密*](e-gly.md) 演算法。 RC4 是透過 >PROV \_ RSA \_ 完整提供者類型來指定。 [*CryptoAPI*](c-gly.md) 會依識別碼參考此演算法 (CALG \_ rc4) 、名稱 (rc4) ，以及類別 (ALG \_ 類別 \_ 資料 \_ 加密) 。

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

請參閱 *相對辨別名稱*。

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**讀者**
</dt> <dd>

[*智慧卡*](s-gly.md)子系統內的標準裝置。  (IFD) 的介面裝置，可支援對智慧卡進行雙向的輸入/輸出。 它可能與整個系統、一或多個讀者群組或特定終端機相關聯。 智慧卡子系統允許讀取器專用於指派給它的終端機。 不過，目前只有一個終端機存在於電腦上。

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**讀取器驅動程式**
</dt> <dd>

將驅動程式服務對應至特定硬體讀取器裝置的特定驅動程式。 它必須將卡片插入和移除事件傳達給 [*智慧卡*](s-gly.md) 類別驅動程式，以轉寄至智慧卡資源管理員，而且必須透過任何原始、T = 0、T = 1 或 pt 通訊協定，將資料交換功能提供給卡片。

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**讀者群組**
</dt> <dd>

讀取器的邏輯群組。 讀者群組可以由系統定義，或是由使用者或系統管理員所建立。 讀者群組是由可在讀者群組上採取行動的智慧卡功能所使用。 為了避免與使用者定義的群組發生名稱衝突，Microsoft 保留使用包含貨幣符號 ($) 的任何名稱。

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**讀取器協助程式驅動程式**
</dt> <dd>

提供常見的智慧卡驅動程式支援常式，以及對特定驅動程式所需的額外 T = 0 和 T = 1 通訊協定支援。

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**參考計數**
</dt> <dd>

用來追蹤 COM 物件的整數值。 建立物件時，它的參考計數會設定為一個。 每次介面系結至物件時，它的參考計數就會遞增;當介面連接終結時，參考計數就會遞減。 當參考計數到達零時，會終結物件。 該物件的所有介面都是不正確。

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**相對辨別名稱**
</dt> <dd>

 (RDN) 在憑證要求中包含主體的實體。 RDN 中的元素是由其屬性定義，不需要包含名稱。 就 [*CryptoAPI*](c-gly.md)而言，rdn 是由 cert rdn 結構所定義 \_ ，然後再指向 cert \_ rdn \_ ATTR 屬性結構的陣列。 每個屬性結構都會指定單一屬性。

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**相對識別碼**
</dt> <dd>

 (RID) [*安全識別碼*](s-gly.md) (SID) 的部分，識別與發行 SID 的授權單位相關的使用者或群組。

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**重新置放的存放區**
</dt> <dd>

已從其預設登錄位置移至登錄中不同位置的 [*憑證存放區*](c-gly.md) 。

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**遠端存放**
</dt> <dd>

位於另一部電腦上的 [*憑證存放區*](c-gly.md) ，例如檔案伺服器或其他共用的遠端電腦。

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**回復 APDU**
</dt> <dd>

[*應用程式協定資料單位*](a-gly.md) (APDU) 在回復中傳送給已接收的 APDU。

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**否認**
</dt> <dd>

此功能可讓使用者拒絕承認執行了某些動作，而其他人亦無法證明是否為事實。 例如，刪除檔案，以及誰可以成功拒絕的使用者。

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**資源管理員**
</dt> <dd>

管理多個讀取器和智慧卡存取權的 [*智慧卡*](s-gly.md) 子系統模組。 資源管理員會識別和追蹤資源、跨多個應用程式佈建讀取器和資源，以及支援用來存取指定卡片上可用之服務的交易基本專案。

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**資源管理員 API**
</dt> <dd>

提供資源管理員服務直接存取的一組 Windows 函數。

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**資源管理員內容**
</dt> <dd>

資源管理員在存取智慧卡資料庫時所使用的內容。 存取資料庫時，查詢和管理功能主要會使用 resource manager 內容。 資源管理員內容的範圍可以是目前的使用者或系統。

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**撤銷清單**
</dt> <dd>

請參閱 [*憑證撤銷清單*](c-gly.md)。

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**擺脫**
</dt> <dd>

請參閱 *相對識別碼*。

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**根授權單位**
</dt> <dd>

CA 階層的最上層 (CA) 的 [*憑證授權單位*](c-gly.md) 單位。 根授權可於下一層階層架構中驗證 CA。

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**根憑證**
</dt> <dd>

識別 CA 的自我簽署 [*憑證授權單位*](c-gly.md) 單位 (CA) 憑證。 它稱為根憑證，因為它是根 CA 的憑證。 根 CA 必須簽署自己的 CA 憑證，因為根據定義，沒有較高的憑證授權單位單位可簽署其 CA 憑證。

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**Rsa**
</dt> <dd>

RSA Data Security，Inc. 是 [*公開金鑰加密標準*](p-gly.md) 的主要開發人員和發行者， (PKCS) 。 名稱中的 "RSA" 代表公司的三名開發人員和擁有者的名稱： Rivest、Shamir 和 Adleman。

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

RSA 金鑰交換演算法的 [*CryptoAPI*](c-gly.md) 演算法名稱。 CryptoAPI 也會根據演算法識別碼來參考此演算法 (CALG \_ RSA \_ KEYX) 和類別 (ALG \_ 類別 \_ 金鑰 \_ 交換) 。

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA \_ 簽署**
</dt> <dd>

RSA 簽名演算法的 CryptoAPI 演算法名稱。 CryptoAPI 也會根據演算法識別碼來參考此演算法 (CALG \_ RSA \_ SIGN) 和 CLASS (ALG 類別簽章 \_ \_) 。

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**RSA 公開金鑰演算法**
</dt> <dd>

以常用的 RSA 公開金鑰加密為基礎的金鑰交換和簽章演算法。 >PROV \_ rsa \_ FULL、>prov \_ RSA \_ SIG、>PROV \_ MS \_ EXCHANGE 和 >prov \_ SSL 提供者類型會使用此演算法。 CryptoAPI 會依識別碼參考此演算法 (CALG \_ rsa \_ KEYX 和 CALG \_ rsa \_ sign) 、名稱 (rsa \_ KEYX 和 rsa \_ sign) 以及類別 (ALG \_ 類別機 \_ 碼 \_ 交換) 。

</dd> </dl>

 

 



