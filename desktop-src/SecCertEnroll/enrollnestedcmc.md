---
description: 從檔案讀取現有的 CMC 憑證要求、將其包裝在另一個 CMC 要求中、簽署此外部要求、將它提交給憑證授權單位單位 (CA) ，然後將憑證回應儲存至檔案。
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191148"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="0cfed-103">enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="0cfed-103">enrollNestedCMC</span></span>

<span data-ttu-id="0cfed-104">EnrollNestedCMC 範例會從檔案讀取現有的 CMC 憑證要求、將其包裝在另一個 CMC 要求中、簽署此外部要求、將它提交給憑證授權單位單位 (CA) ，然後將憑證回應儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="0cfed-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="0cfed-105">Location</span><span class="sxs-lookup"><span data-stu-id="0cfed-105">Location</span></span>

<span data-ttu-id="0cfed-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ X509 憑證註冊 \\ VC \\ enrollNestedCMC 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="0cfed-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0cfed-107">討論</span><span class="sxs-lookup"><span data-stu-id="0cfed-107">Discussion</span></span>

<span data-ttu-id="0cfed-108">EnrollNestedCMC 範例：</span><span class="sxs-lookup"><span data-stu-id="0cfed-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="0cfed-109">處理下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="0cfed-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0cfed-110">輸入檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cfed-110">The name of the input file.</span></span>
    -   <span data-ttu-id="0cfed-111">輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cfed-111">The name of the output file.</span></span>
    -   <span data-ttu-id="0cfed-112">選用的要求範本。</span><span class="sxs-lookup"><span data-stu-id="0cfed-112">An optional request template.</span></span>
2.  <span data-ttu-id="0cfed-113">從檔案讀取現有的 CMC 要求作為 base63 編碼的位元組陣列、將位元組陣列轉換成 **BSTR**、建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 **BSTR** 來初始化 request 物件。</span><span class="sxs-lookup"><span data-stu-id="0cfed-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="0cfed-114">初始化的物件會成為內部要求。</span><span class="sxs-lookup"><span data-stu-id="0cfed-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="0cfed-115">使用在上一個步驟中建立並初始化的內部要求物件來初始化另一個 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="0cfed-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="0cfed-116">抓取現有的簽署憑證，如果找不到，則會從命令列上指定的範本建立憑證要求，並嘗試進行註冊。</span><span class="sxs-lookup"><span data-stu-id="0cfed-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="0cfed-117">FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。</span><span class="sxs-lookup"><span data-stu-id="0cfed-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="0cfed-118">從外部 CMC 要求抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合、建立新的 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件、使用抓取的簽署憑證將它初始化，然後將它新增至集合。</span><span class="sxs-lookup"><span data-stu-id="0cfed-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="0cfed-119">使用可辨別編碼規則 (DER) 來編碼 CMC 要求，並以 **BSTR** 形式抓取要求。</span><span class="sxs-lookup"><span data-stu-id="0cfed-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="0cfed-120">建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。</span><span class="sxs-lookup"><span data-stu-id="0cfed-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="0cfed-121">建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="0cfed-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="0cfed-122">檢查註冊程式的狀態，並將憑證回應從 CA 儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="0cfed-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="0cfed-123">EncodeToFileW 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="0cfed-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cfed-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cfed-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfed-125">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="0cfed-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="0cfed-126">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="0cfed-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
