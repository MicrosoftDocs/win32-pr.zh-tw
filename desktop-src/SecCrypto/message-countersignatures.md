---
description: 有時簽署的訊息需要副署。
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: 訊息副署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690740"
---
# <a name="message-countersignatures"></a><span data-ttu-id="9cb79-103">訊息副署</span><span class="sxs-lookup"><span data-stu-id="9cb79-103">Message Countersignatures</span></span>

<span data-ttu-id="9cb79-104">有時簽署的訊息需要 [*副署*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb79-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="9cb79-105">例如，使用者 A 可能會將已簽署的資料訊息傳送給使用者 B，要求 B 以檔中包含的條款來確認協定。</span><span class="sxs-lookup"><span data-stu-id="9cb79-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="9cb79-106">使用者 B 會解碼訊息、讀取條款，並在協定中來副署訊息。</span><span class="sxs-lookup"><span data-stu-id="9cb79-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="9cb79-107">然後，副署訊息會傳送回使用者 A。使用者 A 現在知道，而且可以證明該使用者 B 是否同意這些條款。</span><span class="sxs-lookup"><span data-stu-id="9cb79-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="9cb79-108">下表列出的區段包含 message countersigning 的程式描述或 C 程式範例。</span><span class="sxs-lookup"><span data-stu-id="9cb79-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="9cb79-109">區段</span><span class="sxs-lookup"><span data-stu-id="9cb79-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="9cb79-110">目錄</span><span class="sxs-lookup"><span data-stu-id="9cb79-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="9cb79-111">訊息函數</span><span class="sxs-lookup"><span data-stu-id="9cb79-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="9cb79-112">列出計數器特徵標記功能。</span><span class="sxs-lookup"><span data-stu-id="9cb79-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="9cb79-113">Countersigning 訊息</span><span class="sxs-lookup"><span data-stu-id="9cb79-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="9cb79-114">詳細說明計數器簽署訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="9cb79-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="9cb79-115">驗證副署</span><span class="sxs-lookup"><span data-stu-id="9cb79-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="9cb79-116">詳細說明驗證計數器簽章的程式。</span><span class="sxs-lookup"><span data-stu-id="9cb79-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="9cb79-117">驗證已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="9cb79-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="9cb79-118">詳細說明在已簽署的訊息上驗證簽章的流程。</span><span class="sxs-lookup"><span data-stu-id="9cb79-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="9cb79-119">範例 C 程式：編碼和解碼副署訊息</span><span class="sxs-lookup"><span data-stu-id="9cb79-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="9cb79-120">編碼和解碼副署訊息的 C 程式範例。</span><span class="sxs-lookup"><span data-stu-id="9cb79-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
