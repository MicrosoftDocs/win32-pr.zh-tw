---
description: 從內部的嵌套 PKCS 10 要求建立 CMC 要求物件 \# 。
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318068"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="22485-103">createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="22485-103">createCNGCustomCMC</span></span>

<span data-ttu-id="22485-104">CreateCNGCustomCMC 範例會從內部的嵌套 PKCS 10 要求建立 CMC request 物件 \# 。</span><span class="sxs-lookup"><span data-stu-id="22485-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="22485-105">內部要求是使用非對稱 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)所建立。</span><span class="sxs-lookup"><span data-stu-id="22485-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="22485-106">私密金鑰是使用「密碼編譯 API：新一代」 (CNG) 密碼編譯提供者，以及在命令列上指定的演算法來建立。</span><span class="sxs-lookup"><span data-stu-id="22485-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="22485-107">您也可以在私密金鑰上設定自訂選項（例如，匯出原則和金鑰保護層級）。</span><span class="sxs-lookup"><span data-stu-id="22485-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="22485-108">Location</span><span class="sxs-lookup"><span data-stu-id="22485-108">Location</span></span>

<span data-ttu-id="22485-109">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ createCNGCustomCMC 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="22485-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="22485-110">討論</span><span class="sxs-lookup"><span data-stu-id="22485-110">Discussion</span></span>

<span data-ttu-id="22485-111">CreateCNGCustomCMC 範例：</span><span class="sxs-lookup"><span data-stu-id="22485-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="22485-112">處理下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="22485-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="22485-113">CNG [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) (CSP) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="22485-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="22485-114">用來產生非對稱私密金鑰的演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="22485-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="22485-115">用來 [*雜湊*](/windows/desktop/SecGloss/h-gly)[*憑證要求*](/windows/desktop/SecGloss/c-gly)的演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="22485-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="22485-116">要在其中儲存憑證要求的輸出檔。</span><span class="sxs-lookup"><span data-stu-id="22485-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="22485-117">選擇性的字串 (AlternateSignature) 如果存在，則會指定使用離散而不是合併的簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="22485-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="22485-118">如需詳細資訊，請參閱 [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) 屬性。</span><span class="sxs-lookup"><span data-stu-id="22485-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="22485-119">建立 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件，並設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="22485-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="22485-120">**LegacyCsp**</span><span class="sxs-lookup"><span data-stu-id="22485-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="22485-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="22485-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="22485-122">**演算法**</span><span class="sxs-lookup"><span data-stu-id="22485-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="22485-123">**KeyProtection**</span><span class="sxs-lookup"><span data-stu-id="22485-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="22485-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="22485-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="22485-125">建立非對稱私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="22485-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="22485-126">建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並使用私密金鑰將它初始化。</span><span class="sxs-lookup"><span data-stu-id="22485-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="22485-127">建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 \# 在步驟4中建立的 PKCS 10 要求物件來初始化它。</span><span class="sxs-lookup"><span data-stu-id="22485-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="22485-128">根據命令列上是否指定替代簽章字串，將替代簽章演算法旗標設定為 **variant \_ TRUE** 或 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="22485-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="22485-129">如需詳細資訊，請參閱 [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)。</span><span class="sxs-lookup"><span data-stu-id="22485-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="22485-130">從命令列上指定的演算法名稱，建立 (OID) 的 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly)[*物件識別碼*](/windows/desktop/SecGloss/o-gly)，並在 CMC 要求物件上設定 oid。</span><span class="sxs-lookup"><span data-stu-id="22485-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="22485-131">簽署憑證要求，並使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 進行編碼。</span><span class="sxs-lookup"><span data-stu-id="22485-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="22485-132">抓取包含已編碼之 CMC 憑證要求的字串，並將其儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="22485-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="22485-133">EncodeToFileW 函式定義于 EnrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="22485-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22485-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="22485-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22485-135">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="22485-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="22485-136">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="22485-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="22485-137">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="22485-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="22485-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="22485-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
