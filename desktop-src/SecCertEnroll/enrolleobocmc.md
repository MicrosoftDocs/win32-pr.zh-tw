---
description: 代表另一位使用者建立 CMC 憑證要求，並在證書階層中註冊使用者。
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511989"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="0a0cf-103">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="0a0cf-103">enrollEOBOCMC</span></span>

<span data-ttu-id="0a0cf-104">EnrollEOBOCMC 範例會代表另一個使用者建立 CMC 憑證要求，並在憑證階層中註冊使用者。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="0a0cf-105">代表其他使用者註冊需要使用註冊代理程式憑證來簽署憑證要求。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="0a0cf-106">Location</span><span class="sxs-lookup"><span data-stu-id="0a0cf-106">Location</span></span>

<span data-ttu-id="0a0cf-107">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollEOBOCMC 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0a0cf-108">討論</span><span class="sxs-lookup"><span data-stu-id="0a0cf-108">Discussion</span></span>

<span data-ttu-id="0a0cf-109">EnrollEOBOCMC 範例：</span><span class="sxs-lookup"><span data-stu-id="0a0cf-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="0a0cf-110">處理下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="0a0cf-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0a0cf-111">憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="0a0cf-112">要求憑證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="0a0cf-113">要儲存要求的個人資訊交換名稱 (PFX) 檔。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="0a0cf-114">用於 PFX 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="0a0cf-115">選用的註冊代理程式範本名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="0a0cf-116">如果憑證存放區中沒有註冊代理程式憑證，則會使用此範本來建立註冊代理程式憑證。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="0a0cf-117">建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用命令列上指定的憑證範本將它初始化。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="0a0cf-118">將要求者的名稱加入 CMC request 物件。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="0a0cf-119">抓取現有的註冊代理程式憑證，如果找不到，則會從命令列上指定的註冊代理程式範本建立憑證要求，並嘗試進行註冊。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="0a0cf-120">確認包含註冊代理程式憑證的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="0a0cf-121">建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，使用註冊代理程式憑證將它初始化、從 CMC request 物件抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合，並將註冊代理程式簽署憑證物件新增至集合。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="0a0cf-122">下一個步驟中所討論的 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件會使用憑證來簽署 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="0a0cf-123">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件、使用 CMC 要求進行初始化、嘗試註冊，以及檢查註冊程式的進度。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="0a0cf-124">將已安裝的憑證匯出至 PFX 檔案。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="0a0cf-125">使用命令列上指定的密碼來保護檔案。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="0a0cf-126">EncodeToFileW 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="0a0cf-127">從憑證存放區刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="0a0cf-128">下列程式碼範例中使用的函式可以在 CryptoAPI 檔中找到。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="0a0cf-129">從電腦刪除私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0a0cf-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0cf-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a0cf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0cf-131">CMC EOBO 要求</span><span class="sxs-lookup"><span data-stu-id="0a0cf-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="0a0cf-132">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="0a0cf-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0a0cf-133">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="0a0cf-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



