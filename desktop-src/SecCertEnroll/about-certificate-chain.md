---
description: 憑證鏈是憑證的階層集合，會導致使用者或電腦回到信任的根目錄，通常是組織 (CA) 的根憑證授權單位。
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: 憑證鏈結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982094"
---
# <a name="certificate-chain"></a><span data-ttu-id="53d2a-103">憑證鏈結</span><span class="sxs-lookup"><span data-stu-id="53d2a-103">Certificate Chain</span></span>

<span data-ttu-id="53d2a-104">憑證鏈是憑證的階層集合，會導致使用者或電腦回到信任的根目錄，通常是組織 (CA) 的根憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="53d2a-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="53d2a-105">因為所有的合作物件都有信任根憑證，所以合作物件可以藉由驗證憑證鏈來得到終端實體憑證的信任。</span><span class="sxs-lookup"><span data-stu-id="53d2a-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="53d2a-106">驗證通常需要建立鏈中的每個憑證：</span><span class="sxs-lookup"><span data-stu-id="53d2a-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="53d2a-107">是由先前憑證中的公開金鑰簽署。</span><span class="sxs-lookup"><span data-stu-id="53d2a-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="53d2a-108">尚未過期。</span><span class="sxs-lookup"><span data-stu-id="53d2a-108">Has not expired.</span></span>
-   <span data-ttu-id="53d2a-109">尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="53d2a-109">Has not been revoked.</span></span>
-   <span data-ttu-id="53d2a-110">符合先前憑證所指定的原則。</span><span class="sxs-lookup"><span data-stu-id="53d2a-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53d2a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="53d2a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53d2a-112">憑證階層</span><span class="sxs-lookup"><span data-stu-id="53d2a-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="53d2a-113">交叉認證</span><span class="sxs-lookup"><span data-stu-id="53d2a-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="53d2a-114">信任模型</span><span class="sxs-lookup"><span data-stu-id="53d2a-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



