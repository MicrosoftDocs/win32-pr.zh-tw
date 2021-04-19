---
description: 建立 CMC 憑證要求，以在憑證授權單位單位 (CA) 封存私密金鑰。
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974078"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="71100-103">enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="71100-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="71100-104">EnrollKeyArchivalCMC 範例會建立 CMC 憑證要求，以在憑證授權單位單位 (CA) 封存私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="71100-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="71100-105">如需詳細資訊，請參閱 [CMC 金鑰保存要求](cmc-key-archival-request.md)。</span><span class="sxs-lookup"><span data-stu-id="71100-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="71100-106">Location</span><span class="sxs-lookup"><span data-stu-id="71100-106">Location</span></span>

<span data-ttu-id="71100-107">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollKeyArchivalCMC 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="71100-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="71100-108">討論</span><span class="sxs-lookup"><span data-stu-id="71100-108">Discussion</span></span>

<span data-ttu-id="71100-109">EnrollKeyArchivalCMC 範例：</span><span class="sxs-lookup"><span data-stu-id="71100-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="71100-110">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="71100-110">Processes the command line arguments.</span></span> <span data-ttu-id="71100-111">命令列應包含用於註冊的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="71100-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="71100-112">使用範本名稱，建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 憑證要求物件，並將其初始化為終端使用者內容。</span><span class="sxs-lookup"><span data-stu-id="71100-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="71100-113">設定 CMC 要求的 [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) 屬性。</span><span class="sxs-lookup"><span data-stu-id="71100-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="71100-114">建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。</span><span class="sxs-lookup"><span data-stu-id="71100-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="71100-115">建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它來取得 CA 的 exchange 憑證。</span><span class="sxs-lookup"><span data-stu-id="71100-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="71100-116">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件、使用 CMC 要求進行初始化、建立包含金鑰封存要求的 base64 編碼字串，並將它提交給 CA。</span><span class="sxs-lookup"><span data-stu-id="71100-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71100-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="71100-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71100-118">CMC 金鑰封存要求</span><span class="sxs-lookup"><span data-stu-id="71100-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="71100-119">CMC 要求</span><span class="sxs-lookup"><span data-stu-id="71100-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="71100-120">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="71100-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
