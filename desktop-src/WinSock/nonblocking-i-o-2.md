---
description: 如果通訊端處於非封鎖模式中，則任何 i/o 作業都必須立即完成，或傳回錯誤碼 WSAEWOULDBLOCK，表示作業無法立即完成。
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: 非封鎖的輸入/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511413"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="05a0b-103">非封鎖的輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="05a0b-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="05a0b-104">如果通訊端處於非封鎖模式中，則任何 i/o 作業都必須立即完成，或傳回錯誤碼 WSAEWOULDBLOCK，表示作業無法立即完成。</span><span class="sxs-lookup"><span data-stu-id="05a0b-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="05a0b-105">在後者的情況下，需要一種機制來探索何時適合在預期作業成功的情況下，再次嘗試操作。</span><span class="sxs-lookup"><span data-stu-id="05a0b-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="05a0b-106">已針對此用途定義了一組網路事件。</span><span class="sxs-lookup"><span data-stu-id="05a0b-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="05a0b-107">您可以使用 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))來輪詢或等候這些事件，或是藉由呼叫 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 或 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))來註冊非同步傳遞。</span><span class="sxs-lookup"><span data-stu-id="05a0b-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="05a0b-108">如需詳細資訊，請參閱 [網路事件通知](notification-of-network-events-2.md) 。</span><span class="sxs-lookup"><span data-stu-id="05a0b-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
