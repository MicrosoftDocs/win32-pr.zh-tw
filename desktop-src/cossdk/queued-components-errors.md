---
description: 佇列元件錯誤
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: 佇列元件錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973393"
---
# <a name="queued-components-errors"></a><span data-ttu-id="7121a-103">佇列元件錯誤</span><span class="sxs-lookup"><span data-stu-id="7121a-103">Queued Components Errors</span></span>

<span data-ttu-id="7121a-104">當已排入佇列的元件呼叫失敗時，可能是因為無法將它傳送到伺服器 (用戶端失敗) 或因為它在 (到達伺服器端失敗) 時無法執行，所以對應的 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 訊息稱為「有害訊息」（ *有害 Message*）。</span><span class="sxs-lookup"><span data-stu-id="7121a-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="7121a-105">COM + 佇列的元件服務會使用一連串的重試佇列來處理有害訊息。</span><span class="sxs-lookup"><span data-stu-id="7121a-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="7121a-106">經過數次重試之後，訊息會移至最後的靜止佇列。</span><span class="sxs-lookup"><span data-stu-id="7121a-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="7121a-107">訊息會留在靜止佇列中，直到使用佇列的元件訊息移動器公用程式手動移動為止。</span><span class="sxs-lookup"><span data-stu-id="7121a-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="7121a-108">如需使用訊息移動器的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="7121a-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="7121a-109">在下表所述的主題中，可以找到各種錯誤發生之事件順序的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="7121a-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="7121a-110">主題</span><span class="sxs-lookup"><span data-stu-id="7121a-110">Topic</span></span>                                                                             | <span data-ttu-id="7121a-111">描述</span><span class="sxs-lookup"><span data-stu-id="7121a-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7121a-112">伺服器端錯誤</span><span class="sxs-lookup"><span data-stu-id="7121a-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="7121a-113">詳細說明 COM + 佇列元件服務對伺服器端失敗的回應。</span><span class="sxs-lookup"><span data-stu-id="7121a-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="7121a-114">用戶端錯誤</span><span class="sxs-lookup"><span data-stu-id="7121a-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="7121a-115">詳細說明 COM + 佇列元件服務對用戶端失敗的回應。</span><span class="sxs-lookup"><span data-stu-id="7121a-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="7121a-116">持續性 Client-Side 失敗</span><span class="sxs-lookup"><span data-stu-id="7121a-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="7121a-117">詳細說明 COM + 佇列元件服務對重複用戶端失敗的回應。</span><span class="sxs-lookup"><span data-stu-id="7121a-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




