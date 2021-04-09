---
description: 藉 \# 由繼承公開金鑰和私密金鑰和憑證範本，從現有的憑證建立 PKCS 7 要求。
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689687"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="e509f-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="e509f-103">enrollPKCS7</span></span>

<span data-ttu-id="e509f-104">EnrollPKCS7 範例會透過 \# 繼承公開金鑰和私密金鑰和憑證範本，從現有的憑證建立 PKCS 7 要求。</span><span class="sxs-lookup"><span data-stu-id="e509f-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="e509f-105">現有的憑證會用來簽署要求。</span><span class="sxs-lookup"><span data-stu-id="e509f-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="e509f-106">此範例會在憑證階層中註冊使用者，並安裝憑證回應。</span><span class="sxs-lookup"><span data-stu-id="e509f-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="e509f-107">此範例會使用現有的憑證來註冊並安裝新的憑證。</span><span class="sxs-lookup"><span data-stu-id="e509f-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="e509f-108">如需更新現有憑證的詳細資訊，請參閱 [enrollRenewalPKCS7](enrollrenewalpkcs7.md)。</span><span class="sxs-lookup"><span data-stu-id="e509f-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="e509f-109">Location</span><span class="sxs-lookup"><span data-stu-id="e509f-109">Location</span></span>

<span data-ttu-id="e509f-110">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollPKCS7 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e509f-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e509f-111">討論</span><span class="sxs-lookup"><span data-stu-id="e509f-111">Discussion</span></span>

<span data-ttu-id="e509f-112">EnrollPKCS7 範例：</span><span class="sxs-lookup"><span data-stu-id="e509f-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="e509f-113">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="e509f-113">Processes the command line arguments.</span></span> <span data-ttu-id="e509f-114">命令列應該包含用來尋找現有憑證的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="e509f-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="e509f-115">使用命令列上指定的範本名稱來抓取現有的憑證，或者，如果找不到憑證，則嘗試註冊使用該範本建立的新憑證。</span><span class="sxs-lookup"><span data-stu-id="e509f-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="e509f-116">FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。</span><span class="sxs-lookup"><span data-stu-id="e509f-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="e509f-117">驗證憑證鏈，並將憑證轉換成 **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="e509f-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="e509f-118">建立 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件，並使用現有的憑證將它初始化。</span><span class="sxs-lookup"><span data-stu-id="e509f-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="e509f-119">新的 PKCS \# 7 要求物件會從現有的憑證繼承私用和公開金鑰和範本。</span><span class="sxs-lookup"><span data-stu-id="e509f-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="e509f-120">建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，並使用現有的憑證將它初始化，然後將它新增至 PKCS \# 7 request 物件。</span><span class="sxs-lookup"><span data-stu-id="e509f-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="e509f-121">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 PKCS \# 7 要求物件初始化它、嘗試向 CA 註冊，並監視註冊程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="e509f-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="e509f-122">CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="e509f-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e509f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e509f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e509f-124">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="e509f-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="e509f-125">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="e509f-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



