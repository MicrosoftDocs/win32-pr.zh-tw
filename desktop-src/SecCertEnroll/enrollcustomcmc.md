---
description: 建立 CMC 憑證要求，並在憑證階層中註冊電腦。
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691044"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="e194e-103">enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="e194e-103">enrollCustomCMC</span></span>

<span data-ttu-id="e194e-104">EnrollCustomCMC 範例會建立 CMC 憑證要求，並在憑證階層中註冊電腦。</span><span class="sxs-lookup"><span data-stu-id="e194e-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="e194e-105">Location</span><span class="sxs-lookup"><span data-stu-id="e194e-105">Location</span></span>

<span data-ttu-id="e194e-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomCMC 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e194e-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e194e-107">討論</span><span class="sxs-lookup"><span data-stu-id="e194e-107">Discussion</span></span>

<span data-ttu-id="e194e-108">EnrollCustomCMC 範例：</span><span class="sxs-lookup"><span data-stu-id="e194e-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="e194e-109">處理下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="e194e-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="e194e-110">要加入至憑證要求的自訂名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="e194e-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="e194e-111">替代主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e194e-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="e194e-112">針對增強金鑰使用方法 (OID) 的物件識別碼 (EKU) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="e194e-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="e194e-113">建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 要求物件，並使用電腦內容將它初始化。</span><span class="sxs-lookup"><span data-stu-id="e194e-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="e194e-114">使用 PKCS \# 10 要求初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。</span><span class="sxs-lookup"><span data-stu-id="e194e-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="e194e-115">使用命令列上指定的 OID 來建立 [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) 物件，並將它新增至 CMC 要求的擴充集合。</span><span class="sxs-lookup"><span data-stu-id="e194e-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="e194e-116">使用命令列上指定的名稱建立 [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) 物件，並將它加入至 [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) 集合，使用集合初始化 [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) 延伸模組，並將其新增至 CMC 要求的擴充集合。</span><span class="sxs-lookup"><span data-stu-id="e194e-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="e194e-117">使用命令列上指定的名稱和值建立 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件，並將它新增至 CMC 要求的 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) 集合中。</span><span class="sxs-lookup"><span data-stu-id="e194e-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="e194e-118">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 CMC 要求物件將它初始化，並抓取包含 base64 編碼要求的字串。</span><span class="sxs-lookup"><span data-stu-id="e194e-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="e194e-119">建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。</span><span class="sxs-lookup"><span data-stu-id="e194e-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="e194e-120">建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="e194e-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="e194e-121">檢查提交狀態，並在成功時將憑證安裝至憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e194e-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e194e-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e194e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e194e-123">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="e194e-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="e194e-124">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="e194e-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="e194e-125">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="e194e-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
