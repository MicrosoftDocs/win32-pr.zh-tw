---
description: 有幾個函式會將憑證內容或內容的連結新增至 store \[ Platform 軟體發展工具組 (SDK) \] 。
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: 使用憑證存放區中的憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320040"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="8cbcb-103">使用憑證存放區中的憑證</span><span class="sxs-lookup"><span data-stu-id="8cbcb-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="8cbcb-104">有幾個函式會將憑證內容或內容的連結新增至存放區。</span><span class="sxs-lookup"><span data-stu-id="8cbcb-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="8cbcb-105">針對已在憑證內容表單中的憑證：</span><span class="sxs-lookup"><span data-stu-id="8cbcb-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="8cbcb-106">**CertAddCertificateCoNtextToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="8cbcb-107">**CertAddCRLCoNtextToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="8cbcb-108">**CertAddCTLCoNtextToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="8cbcb-109">**CertAddCertificateLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="8cbcb-110">**CertAddCRLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="8cbcb-111">**CertAddCTLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="8cbcb-112">針對編碼形式但不是完整憑證內容的憑證：</span><span class="sxs-lookup"><span data-stu-id="8cbcb-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="8cbcb-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="8cbcb-114">**CertAddEncodedCRLToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="8cbcb-115">**CertAddEncodedCTLToStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="8cbcb-116">下列函式會將憑證、CRL 或 CTL 的參考計數遞減一，以將其從存放區中刪除。</span><span class="sxs-lookup"><span data-stu-id="8cbcb-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="8cbcb-117">如果這會導致參考計數變成零，則會釋放用來儲存憑證、CRL 或 CTL 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8cbcb-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="8cbcb-118">**CertDeleteCertificateFromStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="8cbcb-119">**CertDeleteCRLFromStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="8cbcb-120">**CertDeleteCTLFromStore**</span><span class="sxs-lookup"><span data-stu-id="8cbcb-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



