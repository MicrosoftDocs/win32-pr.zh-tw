---
title: 取消
description: WWSAPI 中的大部分作業都可以在執行期間取消。
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- 取消 Windows 的 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316849"
---
# <a name="cancellation"></a><span data-ttu-id="e7b1e-106">取消</span><span class="sxs-lookup"><span data-stu-id="e7b1e-106">Cancellation</span></span>

<span data-ttu-id="e7b1e-107">WWSAPI 中的大部分作業都可以在執行期間取消。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="e7b1e-108">您用來取消作業的函式取決於受影響的物件。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="e7b1e-109">函式</span><span class="sxs-lookup"><span data-stu-id="e7b1e-109">Function</span></span>                                           | <span data-ttu-id="e7b1e-110">描述</span><span class="sxs-lookup"><span data-stu-id="e7b1e-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7b1e-111">**WsAbortChannel**</span><span class="sxs-lookup"><span data-stu-id="e7b1e-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="e7b1e-112">取消指定通道上所有暫止的輸入和輸出，並將通道狀態設定為 WS \_ 通道狀態發生錯誤 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="e7b1e-113">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="e7b1e-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="e7b1e-114">取消指定接聽程式上所有暫止的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="e7b1e-115">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="e7b1e-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="e7b1e-116">取消指定的服務 proxy 上所有暫止的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="e7b1e-117">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e7b1e-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="e7b1e-118">中斷並中止服務主機上的目前作業。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="e7b1e-119">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="e7b1e-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="e7b1e-120">放棄呼叫，在指定的服務 proxy 上呼叫指定的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="e7b1e-121">如需影響 [伺服器端服務作業](server-side-service-operations.md) 和服務模型回呼之取消的詳細資訊，請參閱 [呼叫取消](call-cancellation.md)。</span><span class="sxs-lookup"><span data-stu-id="e7b1e-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




