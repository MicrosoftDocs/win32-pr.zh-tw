---
description: 列出 CryptoAPI 提供的物件。
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: 加密物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386147"
---
# <a name="cryptography-objects"></a>加密物件

加密物件會根據使用方式進行分類，如下所示：

-   [憑證存放區物件](#certificate-store-objects)
-   [數位簽章物件](#digital-signature-objects)
-   [封裝的資料物件](#enveloped-data-objects)
-   [資料加密物件](#data-encryption-objects)
-   [輔助物件](#auxiliary-objects)
-   [憑證註冊物件](#certificate-enrollment-objects)

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
| [**ExtendedProperty**](extendedproperties.md)     | 表示 Microsoft 擴充的屬性。                                                                               |
| [**延伸模組**](extension.md)                     | 代表單一憑證延伸。                                                                              |
| [**延伸模組**](extensions.md)                   | 表示 [**擴充**](extension.md) 物件的集合。                                                      |
| [**PrivateKey**](privatekey.md)                   | 代表私密金鑰。                                                                                               |
| [**PublicKey**](publickey.md)                     | 代表 [**憑證**](certificate.md) 物件中的公開金鑰。                                                 |
| [**市集**](store.md)                             | 提供屬性和方法，以選擇、管理及使用憑證存放區和這些存放區中的憑證。 |
| [**範本**](template.md)                       | 代表憑證的憑證延伸範本。                                                       |



 

## <a name="digital-signature-objects"></a>數位簽章物件

系統會匯出下列物件以數位方式簽署資料，並驗證數位簽章。



| Object                           | 描述                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | 物件，用來以 Authenticode 數位簽章簽署程式碼，以及驗證簽署程式碼的簽章。 |
| [**SignedData**](signeddata.md) | 用來簽署資料和驗證簽署資料簽章的物件。                                        |
| [**簽署者**](signer.md)         | 單一資料簽署者的資訊，包括簽署者的憑證。                                    |
| [**簽名**](signers.md)       | [**簽署者**](signer.md)物件的集合。                                                             |



 

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
| [**NoticeNumbers**](noticenumbers.md)         | 表示 [**擴充**](extension.md) 物件的集合。                                                                              |
| [**老**](oid.md)                             | 代表數個 CAPICOM 屬性所使用的物件識別碼。                                                                     |
| [**Oid**](oids.md)                           | 表示 [**OID**](oid.md) 物件的集合。                                                                                          |
| [**PolicyInformation**](policyinformation.md) | 提供對延伸模組之原則 Oid 的存取。                                                                                             |
| [**Qualifier**](qualifier.md)                 | 代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。                                                           |
| [**限定詞**](qualifiers.md)               | 表示限定詞的集合。                                                                                                          |
| [**設定**](settings.md)                   | 啟用或停用對話方塊，以在未指定身分識別的情況下提示輸入簽署者或寄件者身分識別。                                     |
| [**公用程式**](utilities.md)                 | 提供一般工作的功能。                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>憑證註冊物件

下列物件用於憑證註冊。



| Object                     | 描述                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | 代表憑證註冊控制項的物件。 這主要用於 Visual Basic 或其他自動化語言的程式設計時。 |



 

 

 
