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
# <a name="x509-public-key-certificates"></a><span data-ttu-id="a7ecc-103">X.509 公開金鑰憑證</span><span class="sxs-lookup"><span data-stu-id="a7ecc-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="a7ecc-104">公開金鑰密碼編譯依賴公開和私密金鑰組來加密和解密內容。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="a7ecc-105">金鑰與數學相關，且使用其中一個金鑰加密的內容只能使用其他金鑰進行解密。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="a7ecc-106">私密金鑰會保持秘密。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-106">The private key is kept secret.</span></span> <span data-ttu-id="a7ecc-107">公開金鑰通常會內嵌于二進位憑證中，而且憑證會發行至所有授權使用者都能連接的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="a7ecc-108">X.509 公開金鑰基礎結構 (PKI) 標準識別健全公開金鑰憑證的需求。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="a7ecc-109">憑證是將公開金鑰系結至個人、電腦或組織的帶正負號資料結構。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="a7ecc-110">憑證是由 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位)  (ca 所發行。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="a7ecc-111">所有負責保護使用公開金鑰之通訊的人員，都會依賴 CA 來充分驗證其簽發憑證之個人、系統或實體的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="a7ecc-112">驗證層級通常取決於交易所需的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="a7ecc-113">如果 CA 可適當地驗證要求者的身分識別，它會簽署 (加密) 、編碼和頒發證書。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="a7ecc-114">憑證是將公開金鑰系結至實體的帶正負號資料結構。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="a7ecc-115">[*X.509*](/windows/desktop/SecGloss/x-gly)憑證的 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 語法如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

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

<span data-ttu-id="a7ecc-116">自1998開始，x.509 公開金鑰憑證標準的三個版本已演進。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="a7ecc-117">如下圖所示，每個後續版本的資料結構都會保留存在於舊版中的欄位，並加入更多的欄位。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![x.509 憑證第1、2和3版](images/x509certificateversions.png)

<span data-ttu-id="a7ecc-119">下列主題會更詳細地討論可用欄位：</span><span class="sxs-lookup"><span data-stu-id="a7ecc-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="a7ecc-120">基本欄位</span><span class="sxs-lookup"><span data-stu-id="a7ecc-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="a7ecc-121">第2版欄位</span><span class="sxs-lookup"><span data-stu-id="a7ecc-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="a7ecc-122">第3版擴充功能</span><span class="sxs-lookup"><span data-stu-id="a7ecc-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="a7ecc-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7ecc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ecc-124">公開金鑰基礎結構</span><span class="sxs-lookup"><span data-stu-id="a7ecc-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 
