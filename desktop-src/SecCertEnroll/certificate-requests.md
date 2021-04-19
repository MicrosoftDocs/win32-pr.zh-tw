---
description: 憑證註冊 SDK 可以用來建立 PKCS \# 10、pkcs \# 7、CMC 和自我簽署的憑證要求。
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: 憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974080"
---
# <a name="certificate-requests"></a><span data-ttu-id="218e1-103">憑證要求</span><span class="sxs-lookup"><span data-stu-id="218e1-103">Certificate Requests</span></span>

<span data-ttu-id="218e1-104">憑證註冊 SDK 可以用來建立 PKCS \# 10、pkcs \# 7、CMC 和自我簽署的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="218e1-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="218e1-105">每種類型的要求都會以下表所列的其中一個介面表示。</span><span class="sxs-lookup"><span data-stu-id="218e1-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="218e1-106">所有的要求介面都會直接或間接繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 介面。</span><span class="sxs-lookup"><span data-stu-id="218e1-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="218e1-107">介面</span><span class="sxs-lookup"><span data-stu-id="218e1-107">Interface</span></span>                                                                        | <span data-ttu-id="218e1-108">描述</span><span class="sxs-lookup"><span data-stu-id="218e1-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="218e1-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="218e1-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="218e1-110">表示 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="218e1-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="218e1-111">此介面繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)。</span><span class="sxs-lookup"><span data-stu-id="218e1-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="218e1-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="218e1-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="218e1-113">表示 PKCS \# 7 要求。</span><span class="sxs-lookup"><span data-stu-id="218e1-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="218e1-114">此介面繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)。</span><span class="sxs-lookup"><span data-stu-id="218e1-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="218e1-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="218e1-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="218e1-116">代表自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="218e1-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="218e1-117">此介面繼承自 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)。</span><span class="sxs-lookup"><span data-stu-id="218e1-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="218e1-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="218e1-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="218e1-119">表示 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="218e1-119">Represents a CMC request.</span></span> <span data-ttu-id="218e1-120">此介面繼承自 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)。</span><span class="sxs-lookup"><span data-stu-id="218e1-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="218e1-121">下圖顯示憑證註冊 API 所支援之要求物件的繼承結構。</span><span class="sxs-lookup"><span data-stu-id="218e1-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="218e1-122">[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件可直接或間接作為所有可用要求物件的基類。</span><span class="sxs-lookup"><span data-stu-id="218e1-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![要求介面的繼承結構](images/certificate-request-inheritance.png)

<span data-ttu-id="218e1-124">無論何種類型，憑證要求都會包含提出要求之主體的相關資訊、主體的公開金鑰、一組屬性、一組 x.509 第3版延伸 (可提交為屬性) 的一部分，以及簽章。</span><span class="sxs-lookup"><span data-stu-id="218e1-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="218e1-125">這些問題是由下列主題所解決：</span><span class="sxs-lookup"><span data-stu-id="218e1-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="218e1-126">主體名稱</span><span class="sxs-lookup"><span data-stu-id="218e1-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="218e1-127">屬性</span><span class="sxs-lookup"><span data-stu-id="218e1-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="218e1-128">擴充功能</span><span class="sxs-lookup"><span data-stu-id="218e1-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="218e1-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="218e1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="218e1-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="218e1-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="218e1-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="218e1-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="218e1-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="218e1-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="218e1-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="218e1-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



