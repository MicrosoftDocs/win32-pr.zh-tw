---
description: 憑證註冊 API 支援下列屬性。 您可以使用下列各節中所識別的對應介面，建立個別的屬性。
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: 支援的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774411"
---
# <a name="supported-attributes"></a>支援的屬性

憑證註冊 API 支援下列屬性。 您可以使用下列各節中所識別的對應介面，建立個別的屬性。

## <a name="clientid"></a>ClientId

[**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)介面可用來定義屬性，其中包含傳送憑證要求之用戶端電腦的相關資訊。 您可以使用此資訊進行診斷。

**適用于：** PKCS \# 10 或 CMC 要求。

**OID：** XCN \_ OID \_ 要求 \_ 用戶端 \_ 資訊 (1.3.6.1.4.1.311.21.20) 

## <a name="extensions"></a>延伸模組

[**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)介面可以用來定義一組 x.509 第3版憑證延伸。 支援下列擴充功能。 如需詳細資訊，請參閱擴充介面主題。



| 延伸模組              | 描述                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | 包含與憑證相關聯之簽發者的一或多個替代名稱形式。                                                                                                                                       |
| AuthorityKeyIdentifier | 包含唯一的索引鍵識別碼，用來區分 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 的多個憑證簽署金鑰。 |
| BasicConstraints       | 指出主體是否可作為 CA。                                                                                                                                                                                   |
| CertificatePolicies    | 識別與憑證相關聯的原則和選用的辨識符號資訊。                                                                                                                                      |
| MSApplicationPolicies  | 識別憑證的一或多個用途。 此延伸模組類似于 EnhancedKeyUsage 延伸模組，但卻是由 Microsoft 定義。                                                                                           |
| EnhancedKeyUsage       | 識別憑證中包含之公開金鑰的一或多個用法。 除了金鑰使用延伸模組之外，還可以使用增強金鑰使用方法擴充功能。                                                  |
| KeyUsage               | 識別憑證中包含的公開金鑰可執行之作業的限制。                                                                                                                  |
| SmimeCapabilities      | 將電子郵件收件者的解密功能報告給電子郵件寄件者，讓寄件者選擇雙方所支援之最安全的對稱演算法。                                                      |
| SubjectKeyIdentifier   | 包含唯一金鑰識別碼，可用來區分與憑證擁有者相關聯的多個簽署金鑰。                                                                                          |
| 範本               | 識別發行或更新憑證時要使用的範本。 延伸模組包含範本 (OID) 的物件識別碼。                                                                                       |
| TemplateName           | 識別發行或更新憑證時要使用的範本。 延伸模組包含範本的名稱。                                                                                                          |



 

**適用于：** PKCS \# 10 要求。

**OID：** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14) 

## <a name="archivekey"></a>ArchiveKey

[**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)介面可用來定義屬性，其中包含提交給 CA 以進行封存的加密私密金鑰。

**適用于：** CMC 要求。

**OID：** XCN \_ OID \_ 封存 \_ 金鑰 \_ ATTR (1.3.6.1.4.1.311.21.13) 

## <a name="archivekeyhash"></a>ArchiveKeyHash

[**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)介面可以用來定義 **ArchiveKey** 屬性中所包含之私密金鑰的雜湊。

**適用于：** CMC 要求。

**OID：** XCN \_ OID \_ ENCRYPTED \_ KEY \_ HASH (1.3.6.1.4.1.311.21.21) 

## <a name="cspprovider"></a>CspProvider

[**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)介面可用來定義屬性，其中包含要求者用來進行密碼編譯作業之 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) (CSP) 的相關資訊。

**適用于：** PKCS \# 10 要求。 當您建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件時，會自動建立這個屬性。

**OID：** XCN \_ OID \_ 註冊 \_ CSP \_ 提供者 (1.3.6.1.4.1.311.13.2.2) 

## <a name="osversion"></a>OSVersion

[**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)介面可以用來建立包含用戶端作業系統版本資訊的屬性。 CA 可以使用此資訊來決定建立憑證時要套用的處理類型。

**適用于：** PKCS \# 10 或 CMC 要求。

**OID：** XCN \_ OID \_ OS \_ VERSION (1.3.6.1.4.1.311.13.2.3) 

## <a name="renewalcertificate"></a>RenewalCertificate

[**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)介面可以用來建立包含要更新之憑證的屬性。

**適用于：** PKCS \# 10 要求。 如果您藉 \# 由使用正在更新的憑證來初始化 PKCS 10 要求來建立 PKCS 10 要求，就會自動建立這個屬性。

**OID：** XCN \_ OID \_ 更新 \_ 憑證 (1.3.6.1.4.1.311.13.1) 

 

 
