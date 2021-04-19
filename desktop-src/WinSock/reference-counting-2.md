---
description: 進程可能會在重複的通訊端上呼叫 WSPCloseSocket，而描述項將會解除配置。 不過，基礎通訊端會保持開啟，直到在最後一個描述項上呼叫 WSPCloseSocket 為止。
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: 參考計數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987456"
---
# <a name="reference-counting"></a><span data-ttu-id="66b93-104">參考計數</span><span class="sxs-lookup"><span data-stu-id="66b93-104">Reference Counting</span></span>

<span data-ttu-id="66b93-105">進程可能會在重複的通訊端上呼叫 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) ，而描述項將會解除配置。</span><span class="sxs-lookup"><span data-stu-id="66b93-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="66b93-106">不過，基礎通訊端會保持開啟，直到在最後一個描述項上呼叫 **WSPCloseSocket** 為止。</span><span class="sxs-lookup"><span data-stu-id="66b93-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
