---
description: 建立自訂的 PKCS \# 10 要求、將它提交給獨立的憑證授權單位單位（ (CA) ），並在憑證存放區中安裝已發行的憑證。
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972261"
---
# <a name="enrollcustompkcs10"></a><span data-ttu-id="cea8d-103">enrollCustomPKCS10</span><span class="sxs-lookup"><span data-stu-id="cea8d-103">enrollCustomPKCS10</span></span>

<span data-ttu-id="cea8d-104">EnrollCustomPKCS10 範例會建立自訂 PKCS \# 10 要求、將它提交給 (CA) 的獨立憑證授權單位單位，並在憑證存放區中安裝已發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="cea8d-104">The enrollCustomPKCS10 sample creates a custom PKCS \#10 request, submits it to a stand-alone certification authority (CA), and installs the issued certificate in the certificate store.</span></span> <span data-ttu-id="cea8d-105">獨立 CA 不需要 Active Directory，也不會使用範本。</span><span class="sxs-lookup"><span data-stu-id="cea8d-105">A stand-alone CA does not require Active Directory and does not use templates.</span></span>

## <a name="location"></a><span data-ttu-id="cea8d-106">Location</span><span class="sxs-lookup"><span data-stu-id="cea8d-106">Location</span></span>

<span data-ttu-id="cea8d-107">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomPKCS10 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="cea8d-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="cea8d-108">討論</span><span class="sxs-lookup"><span data-stu-id="cea8d-108">Discussion</span></span>

<span data-ttu-id="cea8d-109">EnrollCustomPKCS10 範例：</span><span class="sxs-lookup"><span data-stu-id="cea8d-109">The enrollCustomPKCS10 sample:</span></span>

1.  <span data-ttu-id="cea8d-110">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="cea8d-110">Processes the command line arguments.</span></span> <span data-ttu-id="cea8d-111">命令列應該包含 X. 500 憑證主體名稱、電子郵件 (RFC822) 名稱和增強金鑰使用方法 (EKU) 物件識別碼 (OID) 。</span><span class="sxs-lookup"><span data-stu-id="cea8d-111">The command line should contain the X.500 certificate subject name, the email (RFC822) name, and an Enhanced Key Usage (EKU) object identifier (OID).</span></span> <span data-ttu-id="cea8d-112">例如，您可以指定下列引數以進行註冊 *user1@example.com* ：</span><span class="sxs-lookup"><span data-stu-id="cea8d-112">For example, you can specify the following arguments to enroll *user1@example.com*:</span></span>
    -   <span data-ttu-id="cea8d-113">主體名稱： "*CN = user1，dc = example，dc = com*"</span><span class="sxs-lookup"><span data-stu-id="cea8d-113">Subject name: "*CN=user1,DC=example,DC=com*"</span></span>
    -   <span data-ttu-id="cea8d-114">RFC822 名稱： *user1@example.com*</span><span class="sxs-lookup"><span data-stu-id="cea8d-114">RFC822 name: *user1@example.com*</span></span>
    -   <span data-ttu-id="cea8d-115">用戶端驗證 EKU OID：1.3.6.1.5.5.7.3。2</span><span class="sxs-lookup"><span data-stu-id="cea8d-115">Client authentication EKU OID: 1.3.6.1.5.5.7.3.2</span></span>
2.  <span data-ttu-id="cea8d-116">建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件，並指定 [**X509CertificateEnrollmentCoNtext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext)列舉的 **CoNtextUser** 值，為終端使用者初始化它。</span><span class="sxs-lookup"><span data-stu-id="cea8d-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it for the end user by specifying the **ContextUser** value of the [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) enumeration.</span></span>
3.  <span data-ttu-id="cea8d-117">建立 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件，使用物件將主體名稱編碼為位元組陣列，並將陣列加入至 PKCS \# 10 要求物件。</span><span class="sxs-lookup"><span data-stu-id="cea8d-117">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses the object to encode the subject name to a byte array, and adds the array to the PKCS \#10 request object.</span></span>
4.  <span data-ttu-id="cea8d-118">建立 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) 物件，使用命令列上指定的 EKU 物件識別碼 (OID) 來初始化它、建立 [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) 集合、將新的 **IObjectId** (EKU) 物件加入至集合、使用集合來初始化 [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) 物件，並將此物件加入至要求。</span><span class="sxs-lookup"><span data-stu-id="cea8d-118">Creates an [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) object, initializes it by using the EKU object identifier (OID) specified on the command line, creates an [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) collection, adds the new **IObjectId** (EKU) object to the collection, uses the collection to initialize an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object and adds this object to the request.</span></span>
5.  <span data-ttu-id="cea8d-119">建立 [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) 物件，使用命令列上指定的 RFC822 名稱將它初始化、建立 [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) 集合、將新 **IAlternativeName** (RFC822 名稱 ) 物件加入至集合、建立 [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) 物件，並將此物件加入至要求。</span><span class="sxs-lookup"><span data-stu-id="cea8d-119">Creates an [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object, initializes it by using the RFC822 name specified on the command line, Creates an [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, adds the new **IAlternativeName** (RFC822 name ) object to the collection, creates an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) object and adds this object to the request.</span></span>
6.  <span data-ttu-id="cea8d-120">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件將它初始化，並抓取包含 base64 編碼要求的字串。</span><span class="sxs-lookup"><span data-stu-id="cea8d-120">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object, and retrieves a string that contains a base64-encoded request.</span></span>
7.  <span data-ttu-id="cea8d-121">建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。</span><span class="sxs-lookup"><span data-stu-id="cea8d-121">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="cea8d-122">建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="cea8d-122">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="cea8d-123">檢查提交狀態，如果註冊成功，則將憑證安裝至憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="cea8d-123">Checks the submission status and, if enrollment is successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cea8d-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cea8d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cea8d-125">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="cea8d-125">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="cea8d-126">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="cea8d-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
