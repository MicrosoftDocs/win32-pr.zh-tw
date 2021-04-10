---
description: Qop 指示詞所識別的保護品質是由伺服器在摘要式挑戰中指定，然後由用戶端在挑戰回應中確認。
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: 保護品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027286"
---
# <a name="quality-of-protection"></a><span data-ttu-id="c30f6-103">保護品質</span><span class="sxs-lookup"><span data-stu-id="c30f6-103">Quality of Protection</span></span>

<span data-ttu-id="c30f6-104">Qop 指示詞所識別的保護品質是由伺服器在摘要式挑戰中指定，然後由用戶端在挑戰回應中確認。</span><span class="sxs-lookup"><span data-stu-id="c30f6-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="c30f6-105">如果用戶端需要伺服器不支援的保護品質，用戶端必須終止驗證。</span><span class="sxs-lookup"><span data-stu-id="c30f6-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="c30f6-106">下表說明 qop 指示詞的可能值。</span><span class="sxs-lookup"><span data-stu-id="c30f6-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="c30f6-107">值</span><span class="sxs-lookup"><span data-stu-id="c30f6-107">Value</span></span>                   | <span data-ttu-id="c30f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="c30f6-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30f6-109">作者</span><span class="sxs-lookup"><span data-stu-id="c30f6-109">"auth"</span></span>                  | <span data-ttu-id="c30f6-110">僅限於驗證 (Authentication)。</span><span class="sxs-lookup"><span data-stu-id="c30f6-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="c30f6-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c30f6-111">"auth-int"</span></span>              | <span data-ttu-id="c30f6-112">使用簽章進行驗證和 [*完整性*](../secgloss/i-gly.md) 檢查。</span><span class="sxs-lookup"><span data-stu-id="c30f6-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="c30f6-113"> (SASL 僅) 「驗證」</span><span class="sxs-lookup"><span data-stu-id="c30f6-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="c30f6-114">使用簽章和加密進行驗證、完整性和機密性檢查。</span><span class="sxs-lookup"><span data-stu-id="c30f6-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="c30f6-115">如需詳細資訊，請參閱 [密碼](ciphers.md)。</span><span class="sxs-lookup"><span data-stu-id="c30f6-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="c30f6-116">保護品質取決於傳遞給 Microsoft Digest SSP 的內容需求旗標。</span><span class="sxs-lookup"><span data-stu-id="c30f6-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="c30f6-117">下表列出與保護品質相關的旗標，以及 qop 指示詞的結果值。</span><span class="sxs-lookup"><span data-stu-id="c30f6-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="c30f6-118">旗標</span><span class="sxs-lookup"><span data-stu-id="c30f6-118">Flag</span></span>                         | <span data-ttu-id="c30f6-119">qop 值</span><span class="sxs-lookup"><span data-stu-id="c30f6-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="c30f6-120">*XXX* \_要求 \_ 機密性</span><span class="sxs-lookup"><span data-stu-id="c30f6-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="c30f6-121">「驗證」 (SASL 僅) </span><span class="sxs-lookup"><span data-stu-id="c30f6-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="c30f6-122">*XXX* \_要求重新執行偵測 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c30f6-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="c30f6-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c30f6-123">"auth-int"</span></span>              |
| <span data-ttu-id="c30f6-124">*XXX* \_要求 \_ 順序 \_ 偵測</span><span class="sxs-lookup"><span data-stu-id="c30f6-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="c30f6-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c30f6-125">"auth-int"</span></span>              |
| <span data-ttu-id="c30f6-126">*XXX* \_需求 \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="c30f6-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="c30f6-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="c30f6-127">"auth-int"</span></span>              |
| <span data-ttu-id="c30f6-128">(無)</span><span class="sxs-lookup"><span data-stu-id="c30f6-128">(none)</span></span>                       | <span data-ttu-id="c30f6-129">作者</span><span class="sxs-lookup"><span data-stu-id="c30f6-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="c30f6-130">伺服器應用程式所指定的內容需求旗標具有 ASC 的前置詞，而用戶端指定的旗標則以 ISC 作為前置詞。</span><span class="sxs-lookup"><span data-stu-id="c30f6-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="c30f6-131">若要判斷您的應用程式所使用的旗標值，請將這些首碼中的其中一個設為 *XXX*。</span><span class="sxs-lookup"><span data-stu-id="c30f6-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="c30f6-132">如需其他伺服器相關資訊，請參閱 [產生摘要挑戰](generating-the-digest-challenge.md)。</span><span class="sxs-lookup"><span data-stu-id="c30f6-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="c30f6-133">如需其他用戶端的相關資訊，請參閱 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。</span><span class="sxs-lookup"><span data-stu-id="c30f6-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
