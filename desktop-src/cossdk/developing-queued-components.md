---
description: 開發已排入佇列的元件
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: 開發已排入佇列的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688699"
---
# <a name="developing-queued-components"></a><span data-ttu-id="b4f5c-103">開發已排入佇列的元件</span><span class="sxs-lookup"><span data-stu-id="b4f5c-103">Developing Queued Components</span></span>

<span data-ttu-id="b4f5c-104">COM + 佇列元件服務要求所有應用程式方法只包含 \[ in \] 參數，沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="b4f5c-105">由於用戶端進行呼叫時，不一定可以使用伺服器物件，因此傳送可建立另一個物件的訊息，即可傳回伺服器結果。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="b4f5c-106">如此一來，雙向通訊就不會出現在每個案例中，而只會在需要時，透過一系列物件之間的單向訊息來進行。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="b4f5c-107">若要使用 COM + 佇列的元件服務，您必須已安裝「 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 」服務。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="b4f5c-108">訊息佇列不會自動安裝。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="b4f5c-109">在作業系統安裝期間或使用 [ **新增/移除程式**] 時，必須選取 [訊息佇列]。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="b4f5c-110">內部訊息佇列憑證會在登入時自動建立。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="b4f5c-111">下表中描述的主題提供更多特製化情況的其他考慮。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="b4f5c-112">主題</span><span class="sxs-lookup"><span data-stu-id="b4f5c-112">Topic</span></span>                                                                                           | <span data-ttu-id="b4f5c-113">描述</span><span class="sxs-lookup"><span data-stu-id="b4f5c-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f5c-114">[以參數 s 的形式傳遞物件](passing-objects-as-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="b4f5c-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="b4f5c-115">描述如何將物件以 \[ in \] 參數傳遞至已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="b4f5c-116">工作組模式中的安全性限制</span><span class="sxs-lookup"><span data-stu-id="b4f5c-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="b4f5c-117">描述在工作組模式中使用訊息佇列驗證的限制。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="b4f5c-118">執行緒考量</span><span class="sxs-lookup"><span data-stu-id="b4f5c-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="b4f5c-119">描述與線上程之間傳遞記錄器介面指標相關的特定考慮。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="b4f5c-120">接收回應</span><span class="sxs-lookup"><span data-stu-id="b4f5c-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="b4f5c-121">說明如何針對已排入佇列的元件呼叫來建立回應。</span><span class="sxs-lookup"><span data-stu-id="b4f5c-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




