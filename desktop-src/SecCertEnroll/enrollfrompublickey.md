---
description: 初始化 PKCS \# 10 憑證要求物件、將它包裝在 CMC 要求物件中、將 CMC 要求提交給企業憑證授權單位單位 (CA) ，然後將 CA 傳回的憑證儲存在檔案中。
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691040"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="0b197-103">enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="0b197-103">enrollFromPublicKey</span></span>

<span data-ttu-id="0b197-104">EnrollFromPublicKey 範例會初始化 PKCS \# 10 憑證要求物件、將它包裝在 CMC 要求物件中、將 CMC 要求提交給企業憑證授權單位單位 (CA) ，然後將 CA 傳回的憑證儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="0b197-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="0b197-105">Location</span><span class="sxs-lookup"><span data-stu-id="0b197-105">Location</span></span>

<span data-ttu-id="0b197-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollFromPublicKey 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="0b197-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0b197-107">討論</span><span class="sxs-lookup"><span data-stu-id="0b197-107">Discussion</span></span>

<span data-ttu-id="0b197-108">EnrollFromPublicKey 範例：</span><span class="sxs-lookup"><span data-stu-id="0b197-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="0b197-109">處理下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="0b197-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0b197-110">憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b197-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="0b197-111">用來將已安裝的憑證儲存為 base64 編碼位元組陣列的檔案名。</span><span class="sxs-lookup"><span data-stu-id="0b197-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="0b197-112">選用的簽署憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="0b197-112">An optional signing certificate template name.</span></span> <span data-ttu-id="0b197-113">如果憑證存放區中沒有憑證，則會使用範本來建立簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="0b197-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="0b197-114">建立 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)私密金鑰物件，並使用目前電腦的預設密碼編譯提供者、金鑰大小和 [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec)值，呼叫 [**create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create)方法來建立非對稱私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0b197-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="0b197-115">抓取 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件的公開金鑰部分。</span><span class="sxs-lookup"><span data-stu-id="0b197-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="0b197-116">建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並使用命令列上指定的範本和公開金鑰將它初始化。</span><span class="sxs-lookup"><span data-stu-id="0b197-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="0b197-117">建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 PKCS \# 10 要求物件初始化它。</span><span class="sxs-lookup"><span data-stu-id="0b197-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="0b197-118">抓取現有的簽署憑證，如果找不到，則會從命令列上指定的範本建立憑證要求，並嘗試進行註冊。</span><span class="sxs-lookup"><span data-stu-id="0b197-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="0b197-119">FindCertByKeyUsage 定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="0b197-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="0b197-120">驗證憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="0b197-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="0b197-121">建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，使用簽署憑證將它初始化、從 CMC request 物件抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合，然後將簽署憑證物件新增至集合。</span><span class="sxs-lookup"><span data-stu-id="0b197-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="0b197-122">使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 來編碼 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="0b197-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="0b197-123">建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。</span><span class="sxs-lookup"><span data-stu-id="0b197-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="0b197-124">建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="0b197-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="0b197-125">檢查註冊程式的狀態，並將已安裝的憑證儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="0b197-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="0b197-126">EncodeToFileW 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="0b197-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b197-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b197-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b197-128">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="0b197-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="0b197-129">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="0b197-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0b197-130">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="0b197-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
