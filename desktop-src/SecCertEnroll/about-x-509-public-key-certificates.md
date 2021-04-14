---
description: 公開金鑰密碼編譯依賴公開和私密金鑰組來加密和解密內容。
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: X.509 公開金鑰憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555759"
---
# <a name="x509-public-key-certificates"></a>X.509 公開金鑰憑證

公開金鑰密碼編譯依賴公開和私密金鑰組來加密和解密內容。 金鑰與數學相關，且使用其中一個金鑰加密的內容只能使用其他金鑰進行解密。 私密金鑰會保持秘密。 公開金鑰通常會內嵌于二進位憑證中，而且憑證會發行至所有授權使用者都能連接的資料庫。

X.509 公開金鑰基礎結構 (PKI) 標準識別健全公開金鑰憑證的需求。 憑證是將公開金鑰系結至個人、電腦或組織的帶正負號資料結構。 憑證是由 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位)  (ca 所發行。 所有負責保護使用公開金鑰之通訊的人員，都會依賴 CA 來充分驗證其簽發憑證之個人、系統或實體的身分識別。 驗證層級通常取決於交易所需的安全性層級。 如果 CA 可適當地驗證要求者的身分識別，它會簽署 (加密) 、編碼和頒發證書。

憑證是將公開金鑰系結至實體的帶正負號資料結構。 [*X.509*](/windows/desktop/SecGloss/x-gly)憑證的 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 語法如下列範例所示。

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

自1998開始，x.509 公開金鑰憑證標準的三個版本已演進。 如下圖所示，每個後續版本的資料結構都會保留存在於舊版中的欄位，並加入更多的欄位。

![x.509 憑證第1、2和3版](images/x509certificateversions.png)

下列主題會更詳細地討論可用欄位：

-   [基本欄位](about-basic-fields.md)
-   [第2版欄位](about-version-2-fields.md)
-   [第3版擴充功能](about-version-3-extensions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[公開金鑰基礎結構](public-key-infrastructure.md)
</dt> </dl>

 

 
