---
title: 傳送呼叫給伺服器程式
description: 一旦用戶端的 RPC 執行時間已連接到伺服器端點，它就會 marshalls 引數，並將其傳送至伺服器。
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- 遠端程序呼叫 RPC、工作、將呼叫傳送至伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301771"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="400ad-104">傳送呼叫給伺服器程式</span><span class="sxs-lookup"><span data-stu-id="400ad-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="400ad-105">一旦用戶端的 RPC 執行時間已連接到伺服器端點，它就會 marshalls 引數，並將其傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="400ad-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="400ad-106">伺服器 RPC 執行時間會將已封送處理的引數提供給 unmarshalls 它們的存根，然後將它們傳遞給伺服器常式。</span><span class="sxs-lookup"><span data-stu-id="400ad-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="400ad-107">當伺服器常式傳回時，存根會挑選 \[ out \] 和 \[ in、out \] 參數和傳回值，marshalls 它們，然後將封送處理的資料傳送到伺服器 RPC 執行時間。</span><span class="sxs-lookup"><span data-stu-id="400ad-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="400ad-108">RPC 執行時間會將資料傳送回用戶端，其中用戶端 RPC 執行時間會將這些資料交給 unmarshalls 它們的用戶端存根，並傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="400ad-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




