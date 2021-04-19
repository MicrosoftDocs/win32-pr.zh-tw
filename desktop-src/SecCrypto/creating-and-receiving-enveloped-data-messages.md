---
description: 封包訊息是針對某位或一組收件者加密的訊息。
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: 建立和接收封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973626"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="157cd-103">建立和接收封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="157cd-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="157cd-104">封包訊息是針對一組收件者加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="157cd-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="157cd-105">在 envelopment 程式中，會產生會話加密金鑰，並使用該金鑰來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="157cd-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="157cd-106">然後，會使用每個預定收件者憑證的公開金鑰，針對每個收件者個別加密加密金鑰本身。</span><span class="sxs-lookup"><span data-stu-id="157cd-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="157cd-107">封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。</span><span class="sxs-lookup"><span data-stu-id="157cd-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="157cd-108">產生的訊息是 [*PKCS \# 7*](../secgloss/p-gly.md)/CMS 格式。</span><span class="sxs-lookup"><span data-stu-id="157cd-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="157cd-109">下列各節顯示封包訊息工作的程式和範例：</span><span class="sxs-lookup"><span data-stu-id="157cd-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="157cd-110">編碼封包資料</span><span class="sxs-lookup"><span data-stu-id="157cd-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="157cd-111">解碼封包資料</span><span class="sxs-lookup"><span data-stu-id="157cd-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="157cd-112">編碼封包訊息的替代程式碼</span><span class="sxs-lookup"><span data-stu-id="157cd-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="157cd-113">範例 C 程式：編碼封包、簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="157cd-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
