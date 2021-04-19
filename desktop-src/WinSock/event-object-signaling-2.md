---
description: WSPEventSelect 的行為與 WSPAsyncSelect 完全相同，不同之處在于，它不會在發生任何指定的 FD \_ XXX 網路事件時（例如，fd 讀取、fd 寫入等），而不會造成 Windows 訊息傳送 (例如， \_ \_ ) ，則會設定指定的事件物件。
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: 事件物件信號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970808"
---
# <a name="event-object-signaling"></a><span data-ttu-id="d0715-103">事件物件信號</span><span class="sxs-lookup"><span data-stu-id="d0715-103">Event Object Signaling</span></span>

<span data-ttu-id="d0715-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) 的行為與 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 完全相同，不同之處在于，它不會在發生任何指定的 FD \_ XXX 網路事件時（例如，fd 讀取、fd 寫入等），而不會造成 Windows 訊息傳送 (例如， \_ \_ ) ，則會設定指定的事件物件。</span><span class="sxs-lookup"><span data-stu-id="d0715-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="d0715-105">此外， \_ 服務提供者還會記住特定的 FD XXX 網路事件。</span><span class="sxs-lookup"><span data-stu-id="d0715-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="d0715-106">這是必要的，因為出現任何和所有提名的網路事件，將導致單一事件物件變成信號。</span><span class="sxs-lookup"><span data-stu-id="d0715-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="d0715-107">呼叫 [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) 會導致網路事件記憶體的目前內容複寫到用戶端提供的緩衝區，以及要清除的網路事件記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0715-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="d0715-108">用戶端也可以指定要以不可部分完成的方式，連同網路事件記憶體一起清除的特定事件物件。</span><span class="sxs-lookup"><span data-stu-id="d0715-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
