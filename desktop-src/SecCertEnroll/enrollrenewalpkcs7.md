---
description: 建立 PKCS \# 7 要求物件以更新現有的憑證。 要求物件會使用新的金鑰組，但會保留與要更新之憑證相關聯的密碼編譯提供者。
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513588"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="40a87-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="40a87-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="40a87-105">EnrollRenewalPKCS7 範例會建立 PKCS \# 7 要求物件來更新現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="40a87-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="40a87-106">要求物件會使用新的金鑰組，但會保留與要更新之憑證相關聯的密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="40a87-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="40a87-107">Location</span><span class="sxs-lookup"><span data-stu-id="40a87-107">Location</span></span>

<span data-ttu-id="40a87-108">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollRenewalPKCS7 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="40a87-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="40a87-109">討論</span><span class="sxs-lookup"><span data-stu-id="40a87-109">Discussion</span></span>

<span data-ttu-id="40a87-110">EnrollRenewalPKCS7 範例：</span><span class="sxs-lookup"><span data-stu-id="40a87-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="40a87-111">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="40a87-111">Processes the command line arguments.</span></span> <span data-ttu-id="40a87-112">命令列應該包含用來建立憑證要求的範本名稱。</span><span class="sxs-lookup"><span data-stu-id="40a87-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="40a87-113">使用命令列上指定的範本名稱來抓取現有的憑證，或者，如果找不到憑證，則會嘗試使用該範本註冊一個憑證。</span><span class="sxs-lookup"><span data-stu-id="40a87-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="40a87-114">FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。</span><span class="sxs-lookup"><span data-stu-id="40a87-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="40a87-115">驗證憑證鏈，並將憑證轉換成 **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="40a87-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="40a87-116">建立 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件，並使用現有的憑證將它初始化。</span><span class="sxs-lookup"><span data-stu-id="40a87-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="40a87-117">由於 *inheritOptions* 參數設定為 InheritDefault，因此會為要求建立新的金鑰組，但會使用現有憑證中的密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="40a87-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="40a87-118">如需詳細資訊，請參閱 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) 方法。</span><span class="sxs-lookup"><span data-stu-id="40a87-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="40a87-119">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 PKCS \# 7 要求物件初始化它、嘗試向 CA 註冊，並監視註冊程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="40a87-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="40a87-120">CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="40a87-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40a87-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="40a87-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a87-122">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="40a87-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="40a87-123">PKCS \# 7 更新要求</span><span class="sxs-lookup"><span data-stu-id="40a87-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="40a87-124">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="40a87-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



