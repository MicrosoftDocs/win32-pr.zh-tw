---
description: 封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。 產生的訊息是 PKCS \# 7/CMS 格式。
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: 在 CAPICOM 中建立及接收封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318236"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="64558-104">在 CAPICOM 中建立及接收封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="64558-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="64558-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="64558-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="64558-106">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="64558-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="64558-107">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="64558-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="64558-108">封包訊息是針對一組收件者加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="64558-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="64558-109">在 envelopment 程式中，會產生會話加密金鑰，並使用該金鑰來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="64558-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="64558-110">然後，會使用每個預定收件者憑證的公開金鑰，針對每個收件者個別加密加密金鑰本身。</span><span class="sxs-lookup"><span data-stu-id="64558-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="64558-111">封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。</span><span class="sxs-lookup"><span data-stu-id="64558-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="64558-112">產生的訊息是 PKCS \# 7/CMS 格式。</span><span class="sxs-lookup"><span data-stu-id="64558-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="64558-113">下列各節顯示封包訊息工作的程式和範例：</span><span class="sxs-lookup"><span data-stu-id="64558-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="64558-114">傳送封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="64558-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="64558-115">接收封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="64558-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



