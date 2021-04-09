---
description: 憑證授權單位 (CA) 負責證明使用者、電腦及組織的身分識別。
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: 憑證授權單位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850871"
---
# <a name="certification-authorities"></a><span data-ttu-id="0a6f7-103">憑證授權單位</span><span class="sxs-lookup"><span data-stu-id="0a6f7-103">Certification Authorities</span></span>

<span data-ttu-id="0a6f7-104"> (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位負責證明至使用者、電腦和組織的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-104">A [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) is responsible for attesting to the identity of users, computers, and organizations.</span></span> <span data-ttu-id="0a6f7-105">CA 會驗證實體，並簽發數位簽署憑證為該身分識別提供擔保。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-105">The CA authenticates an entity and vouches for that identity by issuing a digitally signed certificate.</span></span> <span data-ttu-id="0a6f7-106">CA 也可以管理、撤銷，以及更新憑證。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-106">The CA can also manage, revoke, and renew certificates.</span></span>

<span data-ttu-id="0a6f7-107">CA 可以是公用或私用。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-107">A CA can be public or private.</span></span> <span data-ttu-id="0a6f7-108">公用 CA 提供憑證服務，通常是透過網際網路公開的。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-108">A public CA provides certification services, typically for a fee, to the public over the Internet.</span></span> <span data-ttu-id="0a6f7-109">私用 CA 提供此服務給分隔擴展的成員，例如商務員工或其他私人群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-109">A private CA provides this service to the members of a delimited population such as the employees of a business or members of some other private group.</span></span>

<span data-ttu-id="0a6f7-110">CA 用來驗證使用者的方式不同，但不在本檔的討論範圍內。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-110">The means by which a CA authenticates an end user are varied and beyond the scope of this documentation.</span></span> <span data-ttu-id="0a6f7-111">不過，驗證的方法會因提供者類型而異。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-111">Clearly, however, methods of authentication vary by type of provider.</span></span> <span data-ttu-id="0a6f7-112">例如，私人 CA 可以參考群組名單（例如員工資料庫或 Active Directory）來建立使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-112">For example, a private CA can establish the identity of end users by referring to a group roster such as an employee database or Active Directory.</span></span> <span data-ttu-id="0a6f7-113">公開 CA 所執行的驗證方法通常比較複雜，而且部分取決於憑證所承諾的保證等級。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-113">The authentication methods performed by a public CA are generally more complex and depend partly on the level of assurance being promised by the certificate.</span></span>

<span data-ttu-id="0a6f7-114">隨著公開金鑰基礎結構的擴展 (PKI) 成長，單一 CA 可能會變得很難有效管理它所發出的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-114">As the population of a public key infrastructure (PKI) grows, it can become difficult for a single CA to effectively manage all of the certificates it has issued.</span></span> <span data-ttu-id="0a6f7-115">CA 可以藉由授權 PKI 中的其他 Ca 來簽發憑證，以彌補這些問題。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-115">The CA can compensate by authorizing other CAs in the PKI to issue certificates.</span></span> <span data-ttu-id="0a6f7-116">初始 CA 稱為根，而它授權的 Ca 稱為附屬節點。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-116">The initial CA is called the root, and the CAs it authorizes are called subordinates.</span></span> <span data-ttu-id="0a6f7-117">次級 Ca 也可以在根設定的限制內指定自己的子公司。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-117">Subordinate CAs can also designate their own subsidiaries within the limits set by the root.</span></span> <span data-ttu-id="0a6f7-118">產生的結構稱為「憑證階層」。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-118">The resulting structure is called a certificate hierarchy.</span></span> <span data-ttu-id="0a6f7-119">對階層中較低的 Ca 發出的憑證，包含足夠的憑證來追蹤指向根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-119">The certificates issued to CAs lower in the hierarchy contain enough certificates to trace a path back to the root.</span></span> <span data-ttu-id="0a6f7-120">這稱為憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-120">This is called a certificate chain.</span></span>

<span data-ttu-id="0a6f7-121">「憑證授權單位單位」一詞指的是可保證使用者身分識別的組織，以及組織用來發行和管理憑證的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-121">The term certification authority can refer to both the organization that vouches for the identity of an end user and the server used by the organization to issue and manage certificates.</span></span> <span data-ttu-id="0a6f7-122">您可以設定 Windows server 做為 CA 伺服器，而且此檔通常會在使用「CA」一詞時參考該伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-122">A Windows server can be configured to act as a CA server, and this documentation usually refers to the server when using the term CA.</span></span>

<span data-ttu-id="0a6f7-123">憑證註冊 API 主要是使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件來與 CA 互動。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-123">The Certificate Enrollment API interacts with a CA mainly by using the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="0a6f7-124">此物件上的 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 方法可以自動編碼憑證要求、將憑證要求提交給 CA，以及安裝已發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-124">The [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) method on this object can automatically encode a certificate request, submit it to the CA, and install the issued certificate.</span></span> <span data-ttu-id="0a6f7-125">您也可以使用已初始化的 **IX509Enrollment** 物件進行頻外註冊或延遲註冊。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-125">You can also use an initialized **IX509Enrollment** object for out-of-band enrollment or for delayed enrollment.</span></span> <span data-ttu-id="0a6f7-126">此外，您可以使用 [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) 物件來監視註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="0a6f7-126">In addition, you can use the [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) object to monitor enrollment status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a6f7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a6f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a6f7-128">PKI 元素</span><span class="sxs-lookup"><span data-stu-id="0a6f7-128">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 
