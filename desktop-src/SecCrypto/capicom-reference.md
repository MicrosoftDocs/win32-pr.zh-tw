---
description: 提供的服務可讓應用程式開發人員根據密碼編譯將安全性新增至應用程式。
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: CAPICOM 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94bd7f8c2052f53b4dc1e244251ba76c1b10e349e0f43434a926db6dbeb9190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772109"
---
# <a name="capicom-reference"></a>CAPICOM 參考

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

CAPICOM COM 用戶端提供的服務可讓應用程式開發人員根據 [*密碼*](../secgloss/c-gly.md) 編譯將安全性新增至應用程式。 CryptoAPI 包含使用 [*數位簽章*](../secgloss/d-gly.md)進行驗證、封套訊息以及加密和解密資料的功能。



| 類別                    | 描述                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 憑證存放區物件   | 可用來在這些存放區中使用憑證存放區和憑證的物件。                                       |
| 數位簽章物件   | 用來數位簽署資料和驗證數位簽章的物件。                                                      |
| 封裝的資料物件      | 物件，可用來建立用於隱私權的封包資料訊息，以及解密封包訊息中的資料。                      |
| 資料加密物件     | 用來加密資料和解密加密資料的物件。                                                                |
| 輔助物件           | 用來變更預設行為，以及管理憑證、憑證存放區和使用者介面 (UI) 訊息的物件。 |
| 互通性介面 | 允許衍生 CryptoAPI 以與 CAPICOM 2.0 一起運作的介面。                                          |
| 列舉類型           | 用於 CAPICOM 的列舉類型。                                                                                       |



 

## <a name="certificate-store-objects"></a>憑證存放區物件

下列物件適用于 [*憑證存放區*](../secgloss/c-gly.md) 和這些存放區中的憑證。 CAPICOM 支援使用目前的使用者、本機電腦、記憶體和 Active Directory 憑證存放區。



| Object                                             | 描述                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](certificate.md)                 | 單一數位憑證。                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | [**PolicyInformation**](policyinformation.md)物件的集合。                                                 |
| [**憑證**](certificates.md)               | [**憑證**](certificate.md)物件的集合。                                                               |
| [**CertificateStatus**](certificatestatus.md)     | 提供憑證的狀態資訊。                                                                           |
| [**鏈**](chain.md)                             | 根據數位憑證建立和檢查憑證驗證鏈。                                       |
| [**ExtendedProperties**](extendedproperties.md)   | 代表 [**ExtendedProperty**](extendedproperty.md) 物件的集合。                                        |
| [**ExtendedProperty**](extendedproperty.md)       | 表示 Microsoft 擴充的屬性。                                                                               |
| [**延伸模組**](extension.md)                     | 代表單一憑證延伸。                                                                              |
| [**延伸模組**](extensions.md)                   | 表示 [**擴充**](extension.md) 物件的集合。                                                      |
| [**PrivateKey**](privatekey.md)                   | 代表私密金鑰。                                                                                               |
| [**PublicKey**](publickey.md)                     | 代表 [**憑證**](certificate.md) 物件中的公開金鑰。                                                 |
| [**儲存**](store.md)                             | 提供屬性和方法，以選擇、管理及使用憑證存放區和這些存放區中的憑證。 |
| [**範本**](template.md)                       | 代表憑證的憑證延伸範本。                                                       |



 

## <a name="digital-signature-objects"></a>數位簽章物件

系統會匯出下列物件以數位方式簽署資料，並驗證數位簽章。



| Object                           | 描述                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | 提供使用 Authenticode 數位簽章來簽署內容的功能。 |
| [**SignedData**](signeddata.md) | 用來簽署資料和驗證簽署資料簽章的物件。               |
| [**簽署者**](signer.md)         | 單一資料簽署者的資訊，包括簽署者的憑證。           |
| [**簽名**](signers.md)       | [**簽署者**](signer.md)物件的集合。                                    |



 

## <a name="enveloped-data-objects"></a>封裝的資料物件

系統會匯出下列物件，以建立用於隱私權的封包資料訊息，以及解密封包訊息中的資料。



| Object                                 | 描述                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | 用來建立、傳送和接收封包資料的物件。 封包資料會經過加密，因此只有預期的收件者可以將它解密。 |
| [**收件者**](recipients.md)       | 封裝訊息的預定收件者之 [**憑證**](certificate.md) 物件的集合。                           |



 

## <a name="data-encryption-objects"></a>資料加密物件

下列物件會被匯出，以加密隱私權的任意資料，並將加密的資料解密。



| Object                                 | 描述                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**A**](encrypteddata.md) | 用來加密資料的物件。 [**A**](encrypteddata.md)物件中的加密資料可以進行解密。 |



 

## <a name="auxiliary-objects"></a>輔助物件

系統會匯出下列物件，以變更其他物件的預設行為，以及管理憑證、憑證存放區和訊息。



| Object                                         | 描述                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**演算法**](algorithm.md)                 | 設定密碼編譯作業中所使用的演算法和 [*金鑰長度*](../secgloss/k-gly.md) 。 |
| [**屬性**](attribute.md)                 | 提供與簽章相關的一段新增資訊，例如簽署的時間。                                                    |
| [**屬性**](attributes.md)               | [**屬性**](attribute.md)物件的集合。                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | 提供對憑證使用基本條件約束的唯讀存取。                                                                    |
| [**EKU**](eku.md)                             | 提供憑證之 EKU 屬性的存取權。                                                                                              |
| [**Eku**](ekus.md)                           | [**EKU**](eku.md)物件的集合。                                                                                                       |
| [**EncodedData**](encodeddata.md)             | 代表編碼資料的區塊。                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | 提供對憑證擴充金鑰使用方式屬性的唯讀存取。                                                                 |
| [**HashedData**](hasheddata.md)               | 提供將雜湊演算法套用至字串的功能。                                                                               |
| [**KeyUsage**](keyusage.md)                   | 提供憑證的金鑰使用方式屬性的唯讀存取權。                                                                              |
| [**老**](oid.md)                             | 代表數個 CAPICOM 屬性所使用的物件識別碼。                                                                     |
| [**Oid**](oids.md)                           | 表示 [**OID**](oid.md) 物件的集合。                                                                                          |
| [**PolicyInformation**](policyinformation.md) | 提供對延伸模組之原則 Oid 的存取。                                                                                             |
| [**Qualifier**](qualifier.md)                 | 代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。                                                           |
| [**限定詞**](qualifiers.md)               | 表示限定詞的集合。                                                                                                          |
| [**設定**](settings.md)                   | 啟用或停用對話方塊，以在未指定身分識別的情況下提示輸入簽署者或寄件者身分識別。                                     |
| [**公用程式**](utilities.md)                 | 提供一般工作的功能。                                                                                                        |



 

## <a name="interoperability-interfaces"></a>互通性介面

下列介面可讓 CryptoAPI 的衍生與 CAPICOM 2.0 一起運作。



| 介面                              | 描述                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertCoNtext**](icertcontext.md)   | 提供 CAPICOM x.509v3 [**憑證**](certificate.md) 物件內容的存取權。 此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。 |
| [**ICertStore**](icertstore.md)       | 提供 CAPICOM [**存放區**](store.md) 物件內容的存取權。 此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。               |
| [**IChainCoNtext**](ichaincontext.md) | 提供 CAPICOM [**鏈**](chain.md) 物件內容的存取權。 此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。         |



 

## <a name="enumeration-types"></a>列舉類型

CAPICOM 定義下列列舉類型：

-   [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置**](capicom-active-directory-search-location.md)
-   [**CAPICOM \_ 屬性**](capicom-attribute.md)
-   [**CAPICOM \_ CERT \_ 資訊 \_ 類型**](capicom-cert-info-type.md)
-   [**CAPICOM \_ 憑證 \_ 尋找 \_ 類型**](capicom-certificate-find-type.md)
-   [**CAPICOM \_ 憑證 \_ 包含 \_ 選項**](capicom-certificate-include-option.md)
-   [**CAPICOM \_ 憑證 \_ 另存新檔 \_ \_ 類型**](capicom-certificate-save-as-type.md)
-   [**CAPICOM \_ 憑證 \_ 另存新檔 \_ \_ 類型**](capicom-certificates-save-as-type.md)
-   [**CAPICOM \_ 檢查 \_ 旗標**](capicom-check-flag.md)
-   [**CAPICOM \_ EKU**](capicom-eku.md)
-   [**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)
-   [**CAPICOM \_ 加密 \_ 演算法**](capicom-encryption-algorithm.md)
-   [**CAPICOM \_ 加密 \_ 金鑰 \_ 長度**](capicom-encryption-key-length.md)
-   [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)
-   [**CAPICOM \_ 匯出 \_ 旗標**](capicom-export-flag.md)
-   [**CAPICOM \_ 雜湊 \_ 演算法**](capicom-hash-algorithm.md)
-   [**CAPICOM \_ 金鑰 \_ 位置**](capicom-key-location.md)
-   [**CAPICOM \_ 金鑰 \_ 規格**](capicom-key-spec.md)
-   [**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗標**](capicom-key-storage-flag.md)
-   [**CAPICOM \_ OID**](capicom-oid.md)
-   [**CAPICOM \_ PROPID**](capicom-propid.md)
-   [**CAPICOM \_ >PROV \_ 類型**](capicom-prov-type.md)
-   [**CAPICOM \_ 秘密 \_ 類型**](capicom-secret-type.md)
-   [**CAPICOM \_ 簽署的 \_ 資料 \_ 驗證 \_ 旗標**](capicom-signed-data-verify-flag.md)
-   [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md)
-   [**CAPICOM \_ 存放區 \_ 開啟 \_ 模式**](capicom-store-open-mode.md)
-   [**CAPICOM \_ 存放 \_ 區 \_ 的儲存 \_ 類型**](capicom-store-save-as-type.md)

 

 
