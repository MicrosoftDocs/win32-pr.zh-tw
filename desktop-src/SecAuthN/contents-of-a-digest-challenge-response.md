---
description: 當用戶端收到摘要挑戰以回應資源的要求時，用戶端必須傳送摘要挑戰回應給伺服器。
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: 摘要挑戰回應的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193283"
---
# <a name="contents-of-a-digest-challenge-response"></a><span data-ttu-id="4b3c4-103">摘要挑戰回應的內容</span><span class="sxs-lookup"><span data-stu-id="4b3c4-103">Contents of a Digest Challenge Response</span></span>

<span data-ttu-id="4b3c4-104">當用戶端收到摘要挑戰以回應資源的要求時，用戶端必須傳送摘要挑戰回應給伺服器。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-104">The client must send the server a Digest challenge response when it receives a Digest challenge in response to a request for a resource.</span></span> <span data-ttu-id="4b3c4-105">用戶端必須再次傳送要求，並提供包含挑戰回應的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-105">The client must send the request again, supplying an Authorization header with the challenge response.</span></span> <span data-ttu-id="4b3c4-106">下表說明構成摘要挑戰回應的指示詞。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-106">The following table describes the directives that make up a Digest challenge response.</span></span>



| <span data-ttu-id="4b3c4-107">指示詞</span><span class="sxs-lookup"><span data-stu-id="4b3c4-107">Directive</span></span>          | <span data-ttu-id="4b3c4-108">Description</span><span class="sxs-lookup"><span data-stu-id="4b3c4-108">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3c4-109">username</span><span class="sxs-lookup"><span data-stu-id="4b3c4-109">username</span></span>           | <span data-ttu-id="4b3c4-110">要求資源之 [*安全性主體*](/windows/desktop/SecGloss/s-gly) 的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-110">The account name of the [*security principal*](/windows/desktop/SecGloss/s-gly) requesting the resource.</span></span>                                                                  |
| <span data-ttu-id="4b3c4-111">Realm</span><span class="sxs-lookup"><span data-stu-id="4b3c4-111">Realm</span></span>              | <span data-ttu-id="4b3c4-112">包含使用者名稱所指出之帳戶的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-112">The name of the domain that contains the account indicated by username.</span></span>                                                                                                                                                    |
| <span data-ttu-id="4b3c4-113">nonce</span><span class="sxs-lookup"><span data-stu-id="4b3c4-113">nonce</span></span>              | <span data-ttu-id="4b3c4-114">摘要挑戰中所收到的 nonce。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-114">The nonce received in the Digest challenge.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="4b3c4-115">uri</span><span class="sxs-lookup"><span data-stu-id="4b3c4-115">uri</span></span>                | <span data-ttu-id="4b3c4-116">要求的資源 (URI) 的通用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-116">The Universal Resource Identifier (URI) of the requested resource.</span></span>                                                                                                                                                         |
| <span data-ttu-id="4b3c4-117">qop</span><span class="sxs-lookup"><span data-stu-id="4b3c4-117">qop</span></span>                | <span data-ttu-id="4b3c4-118">[保護的品質](quality-of-protection.md)。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-118">The [quality of protection](quality-of-protection.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="4b3c4-119">數控</span><span class="sxs-lookup"><span data-stu-id="4b3c4-119">nc</span></span>                 | <span data-ttu-id="4b3c4-120">Nonce 計數。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-120">The nonce count.</span></span> <span data-ttu-id="4b3c4-121">用戶端使用 nonce 傳送挑戰回應的次數。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-121">The number of times the client has sent a challenge response using the nonce.</span></span> <span data-ttu-id="4b3c4-122">如需詳細資訊，請參閱 nonce 指示詞。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-122">For more information, see the nonce directive.</span></span>                                                                              |
| <span data-ttu-id="4b3c4-123">cnonce</span><span class="sxs-lookup"><span data-stu-id="4b3c4-123">cnonce</span></span>             | <span data-ttu-id="4b3c4-124">用戶端為每個挑戰回應所產生的唯一編碼值。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-124">A unique encoded value generated by the client for each challenge response.</span></span>                                                                                                                                                |
| <span data-ttu-id="4b3c4-125">回應</span><span class="sxs-lookup"><span data-stu-id="4b3c4-125">response</span></span>           | <span data-ttu-id="4b3c4-126">根據摘要存取規格 ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)) 所計算的值。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-126">A value computed according to the Digest Access specification ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)).</span></span> <span data-ttu-id="4b3c4-127">精確的回應決定性證明使用者的密碼在用戶端上是已知的。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-127">An accurate response is conclusive proof that the user's password is known on the client side.</span></span> |
| <span data-ttu-id="4b3c4-128">演算法</span><span class="sxs-lookup"><span data-stu-id="4b3c4-128">algorithm</span></span>          | <span data-ttu-id="4b3c4-129">摘要挑戰中所收到的演算法。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-129">The algorithm received in the Digest challenge.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4b3c4-130">不透明</span><span class="sxs-lookup"><span data-stu-id="4b3c4-130">opaque</span></span>             | <span data-ttu-id="4b3c4-131">摘要挑戰中收到的不透明值。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-131">The opaque value received in the Digest challenge.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="4b3c4-132">僅 (SASL) cipher</span><span class="sxs-lookup"><span data-stu-id="4b3c4-132">(SASL only) cipher</span></span> | <span data-ttu-id="4b3c4-133">摘要挑戰中所收到的其中一個加密值。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-133">One of the cipher values received in the Digest challenge.</span></span> <span data-ttu-id="4b3c4-134">如需加密的詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-134">For cipher details, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                             |



 

<span data-ttu-id="4b3c4-135">Microsoft Digest 支援下列使用者名稱/領域格式：</span><span class="sxs-lookup"><span data-stu-id="4b3c4-135">Microsoft Digest supports the following username/Realm forms:</span></span>

-   <span data-ttu-id="4b3c4-136">使用者名稱領域</span><span class="sxs-lookup"><span data-stu-id="4b3c4-136">Username Realm</span></span>
-   <span data-ttu-id="4b3c4-137">AccountName 網域 (一般) </span><span class="sxs-lookup"><span data-stu-id="4b3c4-137">AccountName Domain (flat)</span></span>
-   <span data-ttu-id="4b3c4-138">UPN "" (空白) </span><span class="sxs-lookup"><span data-stu-id="4b3c4-138">UPN "" (blank)</span></span>
-   <span data-ttu-id="4b3c4-139">NetBIOS "" (空白) </span><span class="sxs-lookup"><span data-stu-id="4b3c4-139">NetBIOS "" (blank)</span></span>

<span data-ttu-id="4b3c4-140">雖然支援大寫字元，但為了達到符合伺服器預先計算之摘要雜湊值的最佳效能，建議使用小寫字元。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-140">While uppercase characters are supported, for best performance matching the server's precalculated Digest hash values, the use of lowercase characters is recommended.</span></span>

<span data-ttu-id="4b3c4-141">使用預先計算的雜湊是一項新功能，可讓系統操作員略過在網域控制站上使用可還原的加密密碼。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-141">The use of precalculated hashes is a new feature that allows system operators to skip the use of reversible encrypted passwords on the domain controller.</span></span> <span data-ttu-id="4b3c4-142">當使用者的密碼變更時，會為使用者形成預先計算的雜湊。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-142">A precalculated hash is formed for a user when the user's password is changed.</span></span>

<span data-ttu-id="4b3c4-143">Microsoft Digest 會產生用戶端應用程式的摘要挑戰回應字串。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-143">Microsoft Digest generates the Digest challenge response string for client applications.</span></span> <span data-ttu-id="4b3c4-144">如需詳細資訊，請參閱 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。</span><span class="sxs-lookup"><span data-stu-id="4b3c4-144">For details, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
