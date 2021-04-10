---
title: 接收取消
description: 伺服器應用程式可以使用有問題呼叫的系結控制碼來呼叫 RpcServerTestCancel，以找出用戶端是否已要求取消非同步呼叫。 \_如果用戶端取消呼叫，它會傳回 RPC S \_ OK。
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021817"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="81f60-104">接收取消</span><span class="sxs-lookup"><span data-stu-id="81f60-104">Receiving Cancellations</span></span>

<span data-ttu-id="81f60-105">伺服器應用程式可以使用有問題呼叫的系結控制碼來呼叫 [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) ，以找出用戶端是否已要求取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="81f60-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="81f60-106">\_如果用戶端取消呼叫，它會傳回 RPC S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="81f60-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




