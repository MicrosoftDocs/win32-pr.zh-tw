---
description: 說明如何使用 Microsoft Digest 來保護訊息。
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: 使用 Microsoft Digest 保護訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969417"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="68799-103">使用 Microsoft Digest 保護訊息</span><span class="sxs-lookup"><span data-stu-id="68799-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="68799-104">HTTP 和 SASL</span><span class="sxs-lookup"><span data-stu-id="68799-104">HTTP and SASL</span></span>

<span data-ttu-id="68799-105">用戶端和伺服器會使用 [安全性支援提供者介面](sspi.md) (SSPI) 訊息 [*完整性*](../secgloss/i-gly.md) 函式 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 來保護訊息，以偵測特定類型的安全性違規。</span><span class="sxs-lookup"><span data-stu-id="68799-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="68799-106">用戶端會呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函數，以使用其 [*安全性內容*](../secgloss/s-gly.md)來簽署訊息。</span><span class="sxs-lookup"><span data-stu-id="68799-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="68799-107">伺服器會使用 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函數來驗證訊息的來源。</span><span class="sxs-lookup"><span data-stu-id="68799-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="68799-108">除了驗證隨附于訊息 [*的簽*](../secgloss/d-gly.md) 章之外， **VerifySignature** 函式也會檢查 nc 指示詞所指定的 [*nonce*](../secgloss/n-gly.md) 計數 (，) 是否大於針對 nonce 傳送的最後一個計數。</span><span class="sxs-lookup"><span data-stu-id="68799-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="68799-109">如果不是這種情況， **VerifySignature** 函式會傳回序列錯誤碼中的秒 \_ \_ 數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="68799-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="68799-110">僅限 SASL</span><span class="sxs-lookup"><span data-stu-id="68799-110">SASL Only</span></span>

<span data-ttu-id="68799-111">[**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage)和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)函式提供在用戶端與伺服器之間交換之後續驗證訊息的機密性。</span><span class="sxs-lookup"><span data-stu-id="68799-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="68799-112">為了使用訊息機密性函數，伺服器和用戶端必須已使用下列屬性建立 [*安全性內容*](../secgloss/s-gly.md) ：</span><span class="sxs-lookup"><span data-stu-id="68799-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="68799-113">Qop 指示詞所指定的保護品質必須是 "auth"。</span><span class="sxs-lookup"><span data-stu-id="68799-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="68799-114">加密機制必須透過 cipher 指示詞來指定。</span><span class="sxs-lookup"><span data-stu-id="68799-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 
