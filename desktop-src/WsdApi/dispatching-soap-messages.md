---
description: 有許多方式可以處理將收到的 SOAP 訊息分派至適當的服務。 這兩個最簡單的機制是傳輸層級分派，以及位址和動作分派。
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: 分派 SOAP 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a60e896557a64b840ec890ddc5c5d2e2cf8295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513581"
---
# <a name="dispatching-soap-messages"></a><span data-ttu-id="5369e-104">分派 SOAP 訊息</span><span class="sxs-lookup"><span data-stu-id="5369e-104">Dispatching SOAP Messages</span></span>

<span data-ttu-id="5369e-105">有許多方式可以處理將收到的 SOAP 訊息分派至適當的服務。</span><span class="sxs-lookup"><span data-stu-id="5369e-105">There are many ways to handle dispatching received SOAP messages to the appropriate service.</span></span> <span data-ttu-id="5369e-106">這兩個最簡單的機制是傳輸層級分派，以及位址和動作分派。</span><span class="sxs-lookup"><span data-stu-id="5369e-106">The two simplest mechanisms are transport level dispatch, and address and action dispatch.</span></span>

## <a name="transport-level-dispatch"></a><span data-ttu-id="5369e-107">傳輸層級分派</span><span class="sxs-lookup"><span data-stu-id="5369e-107">Transport level dispatch</span></span>

<span data-ttu-id="5369e-108">使用傳輸層級分派時，會使用基礎 HTTP 伺服器 (例如 [HTTP API](/windows/desktop/Http/http-api-start-page)) 來管理將要求路由傳送至裝置及其服務。</span><span class="sxs-lookup"><span data-stu-id="5369e-108">With transport level dispatch, the underlying HTTP server (such as the [HTTP API](/windows/desktop/Http/http-api-start-page)) is used to manage routing of requests to the device and its services.</span></span> <span data-ttu-id="5369e-109">伺服器會為每個服務提供不同的 URL，並為每個 URL 註冊不同的接收。</span><span class="sxs-lookup"><span data-stu-id="5369e-109">The server provides a different URL for each service and for the device and different sinks are registered for each URL.</span></span> <span data-ttu-id="5369e-110">這可讓您設計程式碼，讓每個服務都與另一個服務隔離，不論是在相同進程內以個別元件的形式執行，或是以個別進程的形式執行。</span><span class="sxs-lookup"><span data-stu-id="5369e-110">This allows code to be designed such that each service is isolated from the other, either running as separate components within the same process or running as separate processes.</span></span>

<span data-ttu-id="5369e-111">傳輸層級分派有幾個優點。</span><span class="sxs-lookup"><span data-stu-id="5369e-111">Transport level dispatch has a few advantages.</span></span> <span data-ttu-id="5369e-112">您可以將訊息分派至適當的元件，而不需要先剖析 SOAP 封套或訊息內文。</span><span class="sxs-lookup"><span data-stu-id="5369e-112">Messages can be dispatched to the appropriate component without first parsing the SOAP envelope or message body.</span></span> <span data-ttu-id="5369e-113">此外，您可以重複使用大部分 HTTP 伺服器實施所提供之路由傳送訊息的現有機制，這表示不需要自訂分派程式碼。</span><span class="sxs-lookup"><span data-stu-id="5369e-113">Also, the existing mechanism for routing messages provided by most HTTP server implementations can be reused, which means custom dispatching code is unnecessary.</span></span> <span data-ttu-id="5369e-114">此外，它也會隔離服務之間的 SOAP 處理常式代碼，以提供某種程度的安全性，因為安全服務可避免訊息流經通用程式碼。</span><span class="sxs-lookup"><span data-stu-id="5369e-114">It also isolates the SOAP processing code between services, which provides a level of security, as secure services avoid having messages travel through common code.</span></span>

## <a name="address-and-action-dispatch"></a><span data-ttu-id="5369e-115">位址和動作分派</span><span class="sxs-lookup"><span data-stu-id="5369e-115">Address and action dispatch</span></span>

<span data-ttu-id="5369e-116">Address 和 action 分派相依于 SOAP 標頭，以決定要分派訊息的適當服務。</span><span class="sxs-lookup"><span data-stu-id="5369e-116">Address and action dispatch relies on the SOAP headers to determine the appropriate service to which the message is dispatched.</span></span> <span data-ttu-id="5369e-117">此模型也可能使用其他資訊（例如參考參數）來進一步協助分派。</span><span class="sxs-lookup"><span data-stu-id="5369e-117">This model may also use additional information, such as reference parameters, to further help dispatching.</span></span>

<span data-ttu-id="5369e-118">這種模型鼓勵程式碼在多層式訊息堆疊中重複使用，因為所有的程式碼都是由所有服務所共用。</span><span class="sxs-lookup"><span data-stu-id="5369e-118">This model encourages code reuse throughout a layered messaging stack, as all code up to the SOAP processor is shared by all services.</span></span> <span data-ttu-id="5369e-119">此外，服務的相異傳輸位址並不是必要的，這表示 UUID 位址可用於服務端點。</span><span class="sxs-lookup"><span data-stu-id="5369e-119">Also, distinct transport addresses for services are not required, which means that UUID addresses can be used for service endpoints.</span></span> <span data-ttu-id="5369e-120">位址和動作分派也會直接轉譯為程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="5369e-120">Address and action dispatch also translates more directly to a programming model.</span></span> <span data-ttu-id="5369e-121">開發人員可以將服務和裝置插入管理路由的單一元件，而不需要系結至 HTTP 層或為每個服務建立個別的元件。</span><span class="sxs-lookup"><span data-stu-id="5369e-121">Developers can plug services and devices into a single component which manages routing, rather than having to tie into a HTTP layer or creating separate components for each service.</span></span>

 

 
