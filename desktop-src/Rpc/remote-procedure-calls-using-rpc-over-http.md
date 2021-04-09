---
title: 使用 RPC over HTTP 的遠端程序呼叫
description: 網際網路瀏覽器程式通常會使用超文字傳輸通訊協定 (HTTP) 作為流覽全球 Web 的主要方式。
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- 使用 RPC/HTTP 的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931809"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="04d3b-104">使用 RPC over HTTP 的遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="04d3b-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="04d3b-105">網際網路瀏覽器程式通常會使用超文字傳輸通訊協定 (HTTP) 作為流覽全球 Web 的主要方式。</span><span class="sxs-lookup"><span data-stu-id="04d3b-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="04d3b-106">因此，HTTP 現在會在大部分的電腦上看到廣泛的使用量。</span><span class="sxs-lookup"><span data-stu-id="04d3b-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="04d3b-107">Microsoft 已將其 Internet Information Server 的功能延伸 (IIS) ，以提供使用 HTTP 的遠端程序呼叫服務。</span><span class="sxs-lookup"><span data-stu-id="04d3b-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="04d3b-108">Microsoft RPC over HTTP 的 (RPC over HTTP) 可讓 RPC 用戶端安全且有效率地透過網際網路連接到 RPC 伺服器程式，並執行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="04d3b-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="04d3b-109">這是透過稱為 RPC over HTTP Proxy 的媒介，或單純的 RPC Proxy 來完成。</span><span class="sxs-lookup"><span data-stu-id="04d3b-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="04d3b-110">RPC Proxy 會在 IIS 電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="04d3b-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="04d3b-111">它會接受來自網際網路的 RPC 要求、對這些要求執行驗證、驗證和存取檢查，如果要求通過所有測試，RPC Proxy 就會將要求轉送到執行實際處理的 RPC 伺服器。</span><span class="sxs-lookup"><span data-stu-id="04d3b-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="04d3b-112">使用 RPC over HTTP 時，RPC 用戶端和伺服器不會直接通訊;相反地，它們會使用 RPC Proxy 作為媒介。</span><span class="sxs-lookup"><span data-stu-id="04d3b-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="04d3b-113">因為許多原因而選擇這個模型。</span><span class="sxs-lookup"><span data-stu-id="04d3b-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="04d3b-114">如需詳細資訊，請參閱 [RPC OVER HTTP 安全性](rpc-over-http-security.md)。</span><span class="sxs-lookup"><span data-stu-id="04d3b-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="04d3b-115">本節提供下列主題中 RPC over HTTP 的總覽：</span><span class="sxs-lookup"><span data-stu-id="04d3b-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="04d3b-116">使用 HTTP 做為 RPC 傳輸</span><span class="sxs-lookup"><span data-stu-id="04d3b-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="04d3b-117">RPC over HTTP 安全性</span><span class="sxs-lookup"><span data-stu-id="04d3b-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="04d3b-118">RPC over HTTP 的系統需求和互通性</span><span class="sxs-lookup"><span data-stu-id="04d3b-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="04d3b-119">設定 RPC over HTTP 的電腦</span><span class="sxs-lookup"><span data-stu-id="04d3b-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="04d3b-120">RPC over HTTP 部署建議</span><span class="sxs-lookup"><span data-stu-id="04d3b-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="04d3b-121">如需有關高容量 RPC over HTTP 案例的詳細資訊，請參閱 [MICROSOFT RPC 負載平衡](rpc-load-balancing.md)。</span><span class="sxs-lookup"><span data-stu-id="04d3b-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




