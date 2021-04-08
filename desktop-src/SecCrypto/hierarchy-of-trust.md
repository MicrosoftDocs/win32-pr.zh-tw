---
description: 數位憑證的可信度是利用信任階層來建立。
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: 信任階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485c721493a93c7ea55b1993345e8168ccab319b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851291"
---
# <a name="hierarchy-of-trust"></a><span data-ttu-id="b8dc7-103">信任階層</span><span class="sxs-lookup"><span data-stu-id="b8dc7-103">Hierarchy of Trust</span></span>

<span data-ttu-id="b8dc7-104">[*數位憑證*](../secgloss/c-gly.md)的使用者必須有高層級的信任，憑證才會生效。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-104">For [*digital certificates*](../secgloss/c-gly.md) to be effective, users of certificates must have a high level of trust in them.</span></span> <span data-ttu-id="b8dc7-105">在某些情況下，使用者不會信任憑證的簽發者。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-105">There are cases where a user does not trust the issuer of a certificate.</span></span> <span data-ttu-id="b8dc7-106">如果憑證使用者從未聽說過證書 [*頒發機構*](../secgloss/c-gly.md) 單位，因而無法在臉部值接受來自該簽發者的憑證，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-106">This could happen if the certificate user has never heard of the [*certification authority*](../secgloss/c-gly.md) and therefore is uncomfortable with accepting a certificate from that issuer at face value.</span></span> <span data-ttu-id="b8dc7-107">此問題是由信任階層的認證程式所解決。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-107">This problem is addressed in the certifying process by a hierarchy of trust.</span></span>

<span data-ttu-id="b8dc7-108">信任階層的開頭至少有一個憑證授權單位單位信任的憑證授權單位單位中的所有實體。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-108">A hierarchy of trust begins with at least one certification authority that is trusted by all entities in the certificate chain.</span></span> <span data-ttu-id="b8dc7-109">這可以是內部憑證授權單位單位系統管理員，或是專門用來驗證身分識別和發行憑證的外部公司或組織。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-109">This can be an internal certification authority administrator or an external company or organization that specializes in verifying identities and issuing certificates.</span></span> <span data-ttu-id="b8dc7-110">此授權單位稱為「 [*根授權*](../secgloss/r-gly.md)單位」。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-110">This authority is called the [*root authority*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="b8dc7-111">然後，根授權單位會驗證其他憑證授權單位單位（稱為「第一層」憑證授權單位單位），然後再發行憑證，並認證其他或第二層的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-111">The root authority then certifies other certification authorities, called first-tier certification authorities, who can then issue certificates and also certify additional or second-tier certification authorities.</span></span> <span data-ttu-id="b8dc7-112">下圖顯示這種情況。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-112">This situation is shown in the following illustration.</span></span>

![信任階層](images/trust.png)

<span data-ttu-id="b8dc7-114">簽發憑證之憑證授權單位單位的身分識別是憑證的一部分。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-114">The identity of the certification authority issuing a certificate is part of a certificate.</span></span> <span data-ttu-id="b8dc7-115">該憑證授權單位單位稱為憑證的簽發者。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-115">That certification authority is called the certificate's issuer.</span></span> <span data-ttu-id="b8dc7-116">當憑證的簽發者是第1層或第2層憑證授權單位單位時，該憑證的接收者可以判斷憑證的簽發者是否以憑證授權單位單位在其上方的憑證授權單位單位做為有效的憑證授權單位單位，而且較高層級的憑證授權單位單位會以較高層級的憑證授權單位單位認證，直到確定最低層級的憑證授權單位單位和根目錄之間存在信任鏈憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-116">When a certificate's issuer is a tier 1 or tier 2 certification authority, the receiver of that certificate can determine whether the certificate's issuer is certified as a valid certification authority by a certification authority at a level above it, and that the higher level certification authority is certified as a valid certification authority by still a higher level certification authority until it is determined that a chain of trust exists between the lowest level certification authority and the root certification authority.</span></span>

<span data-ttu-id="b8dc7-117">例如，在上圖中，您可以驗證 CA \# 4 是否已通過 ca 1 的憑證授權單位單位認證 \# ，而且 ca \# 1 已通過根 CA 的憑證授權單位單位認證。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-117">For example, in the preceding illustration, it can be verified that CA \#4 was certified as a certification authority by CA \#1, and that CA \#1 was certified as a certification authority by the root CA.</span></span> <span data-ttu-id="b8dc7-118">因此，當來自較低層級憑證授權單位單位的憑證與加密訊息一起傳遞時，其信任鏈中所有憑證的相關資訊會連同它一起傳遞。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-118">Thus when a certificate from a lower-level certification authority is passed along with the encrypted message, information about all of the certificates in its chain of trust up to the root is passed along with it.</span></span>

<span data-ttu-id="b8dc7-119">剛剛呈現的圖例和描述是概念。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-119">The illustration and description just presented is conceptual.</span></span> <span data-ttu-id="b8dc7-120">在真實世界中，憑證授權單位單位的狀況不斷演進，而且沒有建立或接受單一根授權單位。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-120">In the real world, the certification authority situation is evolving and no single root authority has been established or accepted.</span></span> <span data-ttu-id="b8dc7-121">簡而言之，授權的孤島將會依照下圖所示進行開發。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-121">In the short term, islands of authority will develop as shown in the following illustration.</span></span>

![信任階層中的授權孤島](images/trust2.png)

<span data-ttu-id="b8dc7-123">在這段時間內，下圖中的根島（根目錄1和根2）可能會變成單一根 CA 的第1層 Ca。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-123">In time, the root islands, Root 1 and Root 2 in the illustration, could become Tier 1 CAs to a single root CA.</span></span> <span data-ttu-id="b8dc7-124">屆時，此情況會再次具有單一根授權單位。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-124">At that point, the situation would again have a single root authority.</span></span> <span data-ttu-id="b8dc7-125">您仍然可以看到實際的圖片將如何演進。</span><span class="sxs-lookup"><span data-stu-id="b8dc7-125">It remains to be seen just how the actual picture will evolve.</span></span>

 

 
