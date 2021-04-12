---
description: 只有在使用 Digest 作為 SASL 機制時，下列材質才有效。 使用 Microsoft Digest 的 HTTP 驗證無法使用加密和加密。
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: 加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192103"
---
# <a name="ciphers"></a><span data-ttu-id="bf42a-104">加密</span><span class="sxs-lookup"><span data-stu-id="bf42a-104">Ciphers</span></span>

<span data-ttu-id="bf42a-105">只有在使用 Digest 作為 SASL 機制時，下列材質才有效。</span><span class="sxs-lookup"><span data-stu-id="bf42a-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="bf42a-106">使用 Microsoft Digest 的 HTTP 驗證無法使用加密和加密。</span><span class="sxs-lookup"><span data-stu-id="bf42a-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="bf42a-107">摘要 SASL 挑戰的 cipher 指示詞包含伺服器所支援的密碼的清單，而伺服器需要機密通訊。</span><span class="sxs-lookup"><span data-stu-id="bf42a-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="bf42a-108">只有在 qop 指示詞設定為 "auth-會議" 時，才可以包含 cipher 指示詞。</span><span class="sxs-lookup"><span data-stu-id="bf42a-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="bf42a-109">下表列出由 Microsoft Digest 辨識的密碼，從最強到最弱的順序。</span><span class="sxs-lookup"><span data-stu-id="bf42a-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="bf42a-110">加密值</span><span class="sxs-lookup"><span data-stu-id="bf42a-110">Cipher value</span></span> | <span data-ttu-id="bf42a-111">Description</span><span class="sxs-lookup"><span data-stu-id="bf42a-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf42a-112">rc4</span><span class="sxs-lookup"><span data-stu-id="bf42a-112">"rc4"</span></span>        | <span data-ttu-id="bf42a-113">具有128位金鑰的 RC4 密碼。</span><span class="sxs-lookup"><span data-stu-id="bf42a-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bf42a-114">3des</span><span class="sxs-lookup"><span data-stu-id="bf42a-114">"3des"</span></span>       | <span data-ttu-id="bf42a-115">在 [*CBC*](/windows/desktop/SecGloss/c-gly)模式中使用 EDE 的 [*三重 DES*](/windows/desktop/SecGloss/t-gly)加密，每個 E 階段都有相同的索引鍵 (兩個索引鍵模式) 。</span><span class="sxs-lookup"><span data-stu-id="bf42a-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="bf42a-116">金鑰總長度為112位。</span><span class="sxs-lookup"><span data-stu-id="bf42a-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="bf42a-117">"rc4-56"</span><span class="sxs-lookup"><span data-stu-id="bf42a-117">"rc4-56"</span></span>     | <span data-ttu-id="bf42a-118">具有56位金鑰的 RC4 密碼。</span><span class="sxs-lookup"><span data-stu-id="bf42a-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bf42a-119">"rc4-40"</span><span class="sxs-lookup"><span data-stu-id="bf42a-119">"rc4-40"</span></span>     | <span data-ttu-id="bf42a-120">具有40位金鑰的 RC4 密碼。</span><span class="sxs-lookup"><span data-stu-id="bf42a-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bf42a-121">演算法</span><span class="sxs-lookup"><span data-stu-id="bf42a-121">"des"</span></span>        | <span data-ttu-id="bf42a-122">[*加密標準中的資料加密標準*](/windows/desktop/SecGloss/d-gly) (DES [*) 加密，*](/windows/desktop/SecGloss/c-gly) (CBC) 模式的56位金鑰。</span><span class="sxs-lookup"><span data-stu-id="bf42a-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="bf42a-123">當伺服器應用程式要求機密性時 (qop = "驗證人員" ) Microsoft Digest 將會產生一項挑戰，以提供用戶端安裝在伺服器上的所有加密，並支援摘要。</span><span class="sxs-lookup"><span data-stu-id="bf42a-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="bf42a-124">摘要用戶端會選取最強的可用加密。</span><span class="sxs-lookup"><span data-stu-id="bf42a-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="bf42a-125">如需指定機密性的詳細資訊，請參閱 [產生摘要挑戰](generating-the-digest-challenge.md)。</span><span class="sxs-lookup"><span data-stu-id="bf42a-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
