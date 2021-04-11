---
description: 下列介面可以用來建立憑證要求。
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: 憑證要求介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113776"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="79165-103">憑證要求介面</span><span class="sxs-lookup"><span data-stu-id="79165-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="79165-104">下列介面可以用來建立憑證要求。</span><span class="sxs-lookup"><span data-stu-id="79165-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="79165-105">介面</span><span class="sxs-lookup"><span data-stu-id="79165-105">Interface</span></span>                                                                          | <span data-ttu-id="79165-106">描述</span><span class="sxs-lookup"><span data-stu-id="79165-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79165-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="79165-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="79165-108">表示憑證要求的抽象最上層介面。</span><span class="sxs-lookup"><span data-stu-id="79165-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="79165-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="79165-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="79165-110">可讓您直接建立憑證，而不需經過註冊或憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="79165-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="79165-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="79165-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="79165-112">擴充 [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) 介面，以從範本啟用初始化。</span><span class="sxs-lookup"><span data-stu-id="79165-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="79165-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="79165-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="79165-114">表示 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="79165-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="79165-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="79165-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="79165-116">擴充 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 介面，以從範本啟用初始化。</span><span class="sxs-lookup"><span data-stu-id="79165-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="79165-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="79165-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="79165-118">表示 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="79165-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="79165-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="79165-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="79165-120">擴充 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 介面，以從範本啟用初始化。</span><span class="sxs-lookup"><span data-stu-id="79165-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="79165-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="79165-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="79165-122">擴充 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 介面，並新增可啟用 TPM 憑證證明的屬性。</span><span class="sxs-lookup"><span data-stu-id="79165-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="79165-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="79165-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="79165-124">表示 PKCS \# 7 要求。</span><span class="sxs-lookup"><span data-stu-id="79165-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="79165-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="79165-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="79165-126">擴充 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 介面，以從範本啟用初始化。</span><span class="sxs-lookup"><span data-stu-id="79165-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="79165-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="79165-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79165-128">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="79165-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



