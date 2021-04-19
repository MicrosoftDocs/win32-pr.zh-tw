---
description: 在通訊端可以用來設定連接或接收連線要求之前，它必須系結至本機位址。
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: 系結至本機位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971400"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="8036d-103">系結至本機位址</span><span class="sxs-lookup"><span data-stu-id="8036d-103">Binding to a Local Address</span></span>

<span data-ttu-id="8036d-104">在通訊端可以用來設定連接或接收連線要求之前，它必須系結至本機位址。</span><span class="sxs-lookup"><span data-stu-id="8036d-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="8036d-105">這可以藉由呼叫 [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))來明確完成，如果在呼叫此函式時，將通訊端解除系結，則會隱含地 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="8036d-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 
