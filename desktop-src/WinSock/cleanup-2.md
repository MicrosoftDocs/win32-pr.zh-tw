---
description: Ws2 \_32.dll (和分層式通訊協定) 會針對 WSPStartup 的每個調用呼叫 WSPCleanup 一次。
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: 清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997488"
---
# <a name="cleanup"></a><span data-ttu-id="d2a8b-103">清除</span><span class="sxs-lookup"><span data-stu-id="d2a8b-103">Cleanup</span></span>

<span data-ttu-id="d2a8b-104">Ws2 \_32.dll (和分層式通訊協定) 會針對 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)的每個調用呼叫 [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))一次。</span><span class="sxs-lookup"><span data-stu-id="d2a8b-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="d2a8b-105">在每次叫用時， **WSPCleanup** 應該遞減每個進程的參考計數器，而當計數器到達零時，服務提供者必須準備要從記憶體卸載。</span><span class="sxs-lookup"><span data-stu-id="d2a8b-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="d2a8b-106">第一個商務順序是在設定為正常關閉的通訊端上完成傳送任何未傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="d2a8b-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="d2a8b-107">之後，提供者所持有的任何和所有資源都將被釋放。</span><span class="sxs-lookup"><span data-stu-id="d2a8b-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="d2a8b-108">服務提供者必須停留在可透過呼叫 **WSPStartup** 立即重新初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="d2a8b-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
