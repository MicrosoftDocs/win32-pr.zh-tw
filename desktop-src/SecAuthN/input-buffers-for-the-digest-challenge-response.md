---
description: 使用 Microsoft Digest 的 HTTP 驗證需要三個輸入緩衝區才能產生挑戰回應。 下表摘要說明這些緩衝區。
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: 摘要挑戰回應的輸入緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112189"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="b1d53-104">摘要挑戰回應的輸入緩衝區</span><span class="sxs-lookup"><span data-stu-id="b1d53-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="b1d53-105">使用 Microsoft Digest 的 HTTP 驗證需要三個輸入緩衝區才能產生挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="b1d53-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="b1d53-106">下表摘要說明這些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b1d53-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="b1d53-107">緩衝區編號</span><span class="sxs-lookup"><span data-stu-id="b1d53-107">Buffer number</span></span> | <span data-ttu-id="b1d53-108">包含</span><span class="sxs-lookup"><span data-stu-id="b1d53-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="b1d53-109">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="b1d53-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b1d53-110">0</span><span class="sxs-lookup"><span data-stu-id="b1d53-110">0</span></span>             | <span data-ttu-id="b1d53-111">從伺服器收到的挑戰</span><span class="sxs-lookup"><span data-stu-id="b1d53-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="b1d53-112">之 SECBUFFER \_ TOKEN</span><span class="sxs-lookup"><span data-stu-id="b1d53-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="b1d53-113">1</span><span class="sxs-lookup"><span data-stu-id="b1d53-113">1</span></span>             | <span data-ttu-id="b1d53-114">HTTP 方法</span><span class="sxs-lookup"><span data-stu-id="b1d53-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="b1d53-115">之 SECBUFFER \_ 參數</span><span class="sxs-lookup"><span data-stu-id="b1d53-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="b1d53-116">2</span><span class="sxs-lookup"><span data-stu-id="b1d53-116">2</span></span>             | <span data-ttu-id="b1d53-117">H (實體) </span><span class="sxs-lookup"><span data-stu-id="b1d53-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="b1d53-118">之 SECBUFFER \_ 參數</span><span class="sxs-lookup"><span data-stu-id="b1d53-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="b1d53-119">3</span><span class="sxs-lookup"><span data-stu-id="b1d53-119">3</span></span>             | <span data-ttu-id="b1d53-120">目標伺服器 (SPN) 的 [*服務主體名稱*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b1d53-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="b1d53-121">**之 secbuffer \_目標 \_ 主機** \| **之 SECBUFFER \_ READONLY**</span><span class="sxs-lookup"><span data-stu-id="b1d53-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="b1d53-122">4</span><span class="sxs-lookup"><span data-stu-id="b1d53-122">4</span></span>             | <span data-ttu-id="b1d53-123">通道系結 token 值</span><span class="sxs-lookup"><span data-stu-id="b1d53-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="b1d53-124">**之 secbuffer \_通道 \_** 系結 \| **之 SECBUFFER \_ READONLY**</span><span class="sxs-lookup"><span data-stu-id="b1d53-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="b1d53-125">緩衝區零包含從伺服器收到的摘要挑戰，以回應存取保護之資源的初始要求。</span><span class="sxs-lookup"><span data-stu-id="b1d53-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="b1d53-126">緩衝區1包含方法的字串標記法，例如 "GET" 或 "POST"。</span><span class="sxs-lookup"><span data-stu-id="b1d53-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="b1d53-127">方法會在 A2 的計算中使用，如 [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)中所述。</span><span class="sxs-lookup"><span data-stu-id="b1d53-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="b1d53-128">緩衝區2是訊息的實體主體的 [*MD5*](../secgloss/m-gly.md) 雜湊，如 RFC 2617 中所述。</span><span class="sxs-lookup"><span data-stu-id="b1d53-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="b1d53-129">當搭配通道系結使用 Digest 時，緩衝區3會在 UTF-8 格式中包含目標伺服器的 SPN。</span><span class="sxs-lookup"><span data-stu-id="b1d53-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="b1d53-130">當搭配通道系結使用 Digest 時，緩衝區4包含通道系結 token 值。</span><span class="sxs-lookup"><span data-stu-id="b1d53-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="b1d53-131">SASL 的輸入緩衝區</span><span class="sxs-lookup"><span data-stu-id="b1d53-131">Input Buffers for SASL</span></span>

<span data-ttu-id="b1d53-132">僅提供緩衝區零。</span><span class="sxs-lookup"><span data-stu-id="b1d53-132">Supply buffer zero only.</span></span> <span data-ttu-id="b1d53-133">為了與其他 Ssp 相容，您可以呼叫 [**InitializeSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) ，而不會有有效的伺服器挑戰。</span><span class="sxs-lookup"><span data-stu-id="b1d53-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="b1d53-134">在此情況下， *pInput* 參數應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b1d53-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
