---
description: 您可以使用 IX509Extension 介面來定義任意的延伸模組。
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: 支援的延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690759"
---
# <a name="supported-extensions"></a>支援的延伸模組

您可以使用 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面來定義任意的延伸模組。 憑證註冊 API 也提供衍生自 **IX509Extension** 的介面，可讓您輕鬆地建立任何最常見的擴充功能。 下列清單會識別 Microsoft 憑證授權單位單位所支援的通用擴充功能，以及您可以用來建立它們的物件識別碼和介面。

## <a name="alternativenames"></a>AlternativeNames

替代名稱延伸可以用來針對憑證要求的主體定義一或多個替代名稱表單。 別名形式範例包含電子郵件地址、DNS 名稱、IP 位址及 URI。

**介面：** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID：** XCN \_ OID \_ SUBJECT \_ ALT \_ NAME2 (2.5.29.17) 

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

授權資訊存取延伸模組會識別如何存取 CA 資訊和服務。 擴充值包含一連串的 Uri。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ 授權單位 \_ 資訊 \_ 存取 (1.3.6.1.5.5.7.1.1) 

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

授權單位金鑰識別碼延伸可以識別對應至簽署已發行憑證之 CA 私密金鑰的 CA 公開金鑰。 它是由 Windows server 上的憑證路徑建立軟體用來尋找 CA 憑證。 當 CA 發出憑證時，會將擴充值設定為等於 CA 簽署憑證中的 **SubjectKeyIdentifier** 延伸模組。 此值通常是公開金鑰的 SHA-1 雜湊。

**介面：** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID：** XCN \_ OID \_ 授權單位 \_ 金鑰 \_ IDENTIFIER2 (2.5.29.35) 

## <a name="basicconstraints"></a>BasicConstraints

基本限制延伸可以用來識別實體是否可做為憑證授權單位單位 (CA) ，如果是的話，則可以存在於憑證鏈中的次級 Ca 數目。

**介面：** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID：** XCN \_ OID \_ BASIC \_ CONSTRAINTS2 (2.5.29.19) 

## <a name="certificatepolicies"></a>CertificatePolicies

憑證原則擴充可以用來識別用來發出憑證的原則，而且可以使用它的用途。 這些是由 (Oid) 的物件識別碼集合所識別。 針對組織的需求自訂原則。

**介面：** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID：** XCN \_ OID \_ CERT \_ 原則 (2.5.29.32) 

## <a name="crldistributionpoints"></a>CrlDistributionPoints

憑證撤銷清單 (CRL) 發佈點延伸模組包含基底憑證撤銷清單 (CRL) 的 URI。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ CRL \_ DIST \_ (2.5.29.31) 

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

[增強金鑰使用方法] 延伸模組可以用來定義憑證中包含之公開金鑰的一或多個用法。

**介面：** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID：** XCN \_ OID \_ 增強 \_ 金鑰 \_ 使用方法 (2.5.29.37) 

## <a name="freshestcrl"></a>FreshestCRL

最新版的 CRL 延伸模組包含 delta CRL 的 URI。 此擴充功能和 **CrlDistributionPoints** 延伸模組使用相同的 asn.1 語法。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ 最 \_ (2.5.29.46) 的 CRL

## <a name="keyusage"></a>KeyUsage

金鑰使用方法延伸可以用來定義憑證中包含的公開金鑰所能執行的作業限制。 例如，您可以指定只使用公開金鑰來建立數位簽章、簽署憑證撤銷清單 (CRL) ，或將另一個金鑰加密。

**介面：** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID：** XCN \_ OID \_ 金鑰 \_ 使用方法 (2.5.29.15) 

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

應用程式可以使用 Microsoft 應用程式原則擴充功能來根據允許的使用方式來篩選憑證。 允許的用法是由 Oid 識別。 此延伸模組類似于 **EnhancedKeyUsage** 延伸模組，但會將更嚴格的語義套用至父 CA。 此延伸模組是 Microsoft 專有的。

**介面：** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID：** XCN \_ OID \_ 應用程式憑證 \_ \_ 原則 (1.3.6.1.4.1.311.21.10) 

## <a name="nameconstraints"></a>NameConstraints

名稱限制延伸是用來識別憑證階層中憑證的所有主體名稱必須位於其中的命名空間。 這個延伸只能用於一個 CA 憑證中。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ 名稱 \_ 條件約束 (2.5.29.30) 

## <a name="policyconstraints"></a>PolicyConstraints

原則限制延伸會新增至 CA 憑證，藉由禁止原則對應或要求階層中的每個憑證都包含可接受的原則識別碼來限制路徑驗證。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ 原則 \_ 條件約束 (2.5.29.36) 

## <a name="policymappings"></a>PolicyMappings

原則對應延伸模組是用來識別對應至發行 CA 中原則的次級 CA 中的原則。 擴充值包含一連串的發行 CA，以及由物件識別碼表示的次級 CA 原則對應。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ 原則對應 \_ (2.5.29.33) 

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

私密金鑰使用期限延伸是用來指定私密金鑰的不同有效期間，而非與金鑰相關聯的憑證。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ PRI加值稅EKEY \_ 使用 \_ 期間 (2.5.29.16) 

## <a name="smimecapabilities"></a>SmimeCapabilities

安全/多用途網際網路郵件延伸 (S/MIME) 功能延伸模組可用來將電子郵件收件者的解密功能回報給電子郵件訊息的寄件者，讓傳送者可以選擇雙方所支援的最安全加密演算法。 擴充功能值包含對稱式加密演算法 Oid 的集合，以及每個 Oid 的選擇性加密強度。

**介面：** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID：** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15) 

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

主體目錄屬性延伸可以用來傳達識別碼屬性，例如憑證主體的國籍。 延伸值是 OID 值配對的序列。

**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID：** XCN \_ OID \_ SUBJECT \_ DIR \_ ATTRS (2.5.29.9) 

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

主體金鑰識別碼延伸可以用來區別憑證主體所持有的多個公開金鑰。 延伸值通常是金鑰的 SHA-1 雜湊。

**介面：** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID：** XCN \_ OID \_ 主體 \_ 金鑰 \_ 識別碼 (2.5.29.14) 

## <a name="template"></a>範本

範本延伸模組可以用來識別發行或更新憑證時要使用的第2版範本。 擴充值包含範本 OID 和選用的版本資訊。 此延伸模組是 Microsoft 專有的。

**介面：** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID：** XCN \_ OID \_ 證書 \_ 範本 (1.3.6.1.4.1.311.21.7) 

## <a name="templatename"></a>TemplateName

範本名稱延伸可以用來識別發行或更新憑證時要使用的第1版範本。 擴充值包含範本的名稱。 此延伸模組是 Microsoft 專有的。

**介面：** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID：** XCN \_ OID \_ 註冊 \_ CERTTYPE \_ 延伸模組 (元1.3.6.1.4.1.311.20.2 參考) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[擴充功能](extensions.md)
</dt> </dl>

 

 



