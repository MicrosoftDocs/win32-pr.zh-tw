---
description: 下列介面可以用來管理憑證簽章和公開金鑰和私密金鑰。
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: 憑證簽章和金鑰介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850555"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="90ee6-103">憑證簽章和金鑰介面</span><span class="sxs-lookup"><span data-stu-id="90ee6-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="90ee6-104">下列介面可以用來管理憑證簽章和公開金鑰和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="90ee6-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="90ee6-105">介面</span><span class="sxs-lookup"><span data-stu-id="90ee6-105">Interface</span></span>                                                      | <span data-ttu-id="90ee6-106">描述</span><span class="sxs-lookup"><span data-stu-id="90ee6-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ee6-107">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="90ee6-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="90ee6-108">代表可讓您簽署憑證要求的簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="90ee6-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="90ee6-109">**ISignerCertificates**</span><span class="sxs-lookup"><span data-stu-id="90ee6-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="90ee6-110">管理 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="90ee6-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="90ee6-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="90ee6-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="90ee6-112">代表可用於加密、簽署和金鑰協定的非對稱私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="90ee6-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="90ee6-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="90ee6-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="90ee6-114">表示公開/私密金鑰組中的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="90ee6-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="90ee6-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="90ee6-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="90ee6-116">表示用來簽署憑證要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="90ee6-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="90ee6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="90ee6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ee6-118">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="90ee6-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



