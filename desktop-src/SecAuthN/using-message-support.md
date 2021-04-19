---
description: 說明如何使用 SSPI 訊息支援。
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: 使用訊息支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996881"
---
# <a name="using-message-support"></a><span data-ttu-id="e6cb7-103">使用訊息支援</span><span class="sxs-lookup"><span data-stu-id="e6cb7-103">Using Message Support</span></span>

<span data-ttu-id="e6cb7-104">在完成交握並建立安全連線之後，應用程式可以使用 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)、 [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage)、 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) 函式，以與遠端電腦交換已簽署或加密的應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="e6cb7-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="e6cb7-105">下列各節將示範在建立 [*安全性內容*](../secgloss/s-gly.md) 之後使用這些功能的範例：</span><span class="sxs-lookup"><span data-stu-id="e6cb7-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="e6cb7-106">簽署訊息</span><span class="sxs-lookup"><span data-stu-id="e6cb7-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="e6cb7-107">驗證訊息</span><span class="sxs-lookup"><span data-stu-id="e6cb7-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="e6cb7-108">加密訊息</span><span class="sxs-lookup"><span data-stu-id="e6cb7-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="e6cb7-109">解密訊息</span><span class="sxs-lookup"><span data-stu-id="e6cb7-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
