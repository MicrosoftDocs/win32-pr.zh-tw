---
description: TSPI 包含許多作業，可啟動呼叫控制碼的存留期。
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: 非同步回復與新呼叫控制碼上的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850487"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="b9935-103">非同步回復與新呼叫控制碼上的事件</span><span class="sxs-lookup"><span data-stu-id="b9935-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="b9935-104">TSPI 包含許多作業，可啟動呼叫控制碼的存留期。</span><span class="sxs-lookup"><span data-stu-id="b9935-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="b9935-105">如果服務提供者針對這類作業傳回成功，它必須填入 **HDRVCALL** 類型的不透明控制碼，它會在傳回之前將它用於新的呼叫。</span><span class="sxs-lookup"><span data-stu-id="b9935-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="b9935-106">在收到相符的 [*完成 \_*](/windows/win32/api/tspi/nc-tspi-async_completion) 程式之前，TAPI 永遠不會在呼叫上執行作業。</span><span class="sxs-lookup"><span data-stu-id="b9935-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="b9935-107">如果服務提供者傳回失敗，控制碼就會自動變成不正確 (也就是沒有 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)) 。</span><span class="sxs-lookup"><span data-stu-id="b9935-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="b9935-108">實際上，在非同步完成之前，TAPI 會將控制碼視為「尚未生效」。</span><span class="sxs-lookup"><span data-stu-id="b9935-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="b9935-109">在收到相符的 [*完成 \_*](/windows/win32/api/tspi/nc-tspi-async_completion) 程式之後，服務提供者也必須將控制碼視為「無效」。</span><span class="sxs-lookup"><span data-stu-id="b9935-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="b9935-110">換句話說，它不得針對新的呼叫發出任何 [*line \_ 事件*](/windows/win32/api/tspi/nc-tspi-lineevent) 函式，或將它包含在訊息的呼叫計數或該行的狀態資料結構中。</span><span class="sxs-lookup"><span data-stu-id="b9935-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="b9935-111">TAPI 等級也符合這些生命週期的限制;在相符的 [**行 \_ 回復**](./line-reply.md) 訊息之前，不會傳回或有效的新呼叫控制碼，而且新呼叫的任何事件都不會傳遞至應用程式，直到行 \_ 回復訊息為止。</span><span class="sxs-lookup"><span data-stu-id="b9935-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="b9935-112">此「啟動存留期」原則適用的 TSPI 作業如下：</span><span class="sxs-lookup"><span data-stu-id="b9935-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="b9935-113">**TSPI \_ lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="b9935-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="b9935-114">**TSPI \_ lineForward**</span><span class="sxs-lookup"><span data-stu-id="b9935-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="b9935-115">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="b9935-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="b9935-116">**TSPI \_ linePickup**</span><span class="sxs-lookup"><span data-stu-id="b9935-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="b9935-117">**TSPI \_ linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="b9935-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="b9935-118">**TSPI \_ lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="b9935-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="b9935-119">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="b9935-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="b9935-120">**TSPI \_ lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="b9935-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
