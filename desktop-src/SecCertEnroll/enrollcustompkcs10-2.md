---
description: 建立自訂的 PKCS \# 10 要求，並嘗試在企業憑證授權單位單位 (CA) 中註冊它。
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972455"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="91440-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="91440-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="91440-104">EnrollCustomPKCS10 \_ 2 範例會建立自訂的 PKCS \# 10 要求，並嘗試在企業 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 中註冊它。</span><span class="sxs-lookup"><span data-stu-id="91440-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="91440-105">Location</span><span class="sxs-lookup"><span data-stu-id="91440-105">Location</span></span>

<span data-ttu-id="91440-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomPKCS10 \_ 2 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="91440-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="91440-107">討論</span><span class="sxs-lookup"><span data-stu-id="91440-107">Discussion</span></span>

<span data-ttu-id="91440-108">EnrollCustomPKCS10 \_ 2 範例：</span><span class="sxs-lookup"><span data-stu-id="91440-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="91440-109">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="91440-109">Processes the command line arguments.</span></span> <span data-ttu-id="91440-110">命令列應該包含範本的名稱和密碼編譯提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="91440-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="91440-111">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用命令列上指定的範本名稱將它初始化。</span><span class="sxs-lookup"><span data-stu-id="91440-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="91440-112">從註冊物件捕獲 [*憑證要求*](/windows/desktop/SecGloss/c-gly) 。</span><span class="sxs-lookup"><span data-stu-id="91440-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="91440-113">\#從步驟3取得的憑證要求物件抓取最內層的 PKCS 10 要求。</span><span class="sxs-lookup"><span data-stu-id="91440-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="91440-114">從 PKCS 10 要求中取出 [*私用金鑰*](/windows/desktop/SecGloss/p-gly) \# 。</span><span class="sxs-lookup"><span data-stu-id="91440-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="91440-115">建立 [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) 集合，並將可用的密碼編譯提供者加入至集合，然後針對命令列上指定的提供者抓取 [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) 物件。</span><span class="sxs-lookup"><span data-stu-id="91440-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="91440-116">設定私密金鑰的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="91440-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="91440-117">嘗試註冊 [*憑證要求*](/windows/desktop/SecGloss/c-gly)。</span><span class="sxs-lookup"><span data-stu-id="91440-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91440-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="91440-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91440-119">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="91440-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="91440-120">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="91440-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
