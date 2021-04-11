---
title: 服務授權
description: 應用程式可以針對服務主機上的內送訊息，執行自訂授權。
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- 適用于 Windows 的服務授權 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093515"
---
# <a name="service-authorization"></a><span data-ttu-id="3ebf6-106">服務授權</span><span class="sxs-lookup"><span data-stu-id="3ebf6-106">Service Authorization</span></span>

<span data-ttu-id="3ebf6-107">應用程式可以針對服務主機上的內送訊息，執行自訂授權。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="3ebf6-108">服務主機會收到安全性回呼 [**ws \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)，作為傳送至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)函式之 [**ws \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="3ebf6-109">收到 [WS \_ 訊息](ws-message.md) 時，就會叫用此回呼。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="3ebf6-110">應用程式可以依賴此回呼，針對服務主機上的內送訊息執行自訂授權。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="3ebf6-111">如果授權失敗，安全性回呼函式會傳回失敗的 HR，而服務主機會中止通道。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="3ebf6-112">如需範例的範例，請參閱 [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md)的使用者名稱（透過 SSL）範例。</span><span class="sxs-lookup"><span data-stu-id="3ebf6-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




