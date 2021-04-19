---
description: 當新的通訊會話抵達時，在位址和媒體類型中註冊感興趣的 TAPI 應用程式將會收到事件通知。
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: 回應在別處起始的會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992518"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="dddd7-103">回應在別處起始的會話</span><span class="sxs-lookup"><span data-stu-id="dddd7-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="dddd7-104">當新的通訊會話抵達時，在 [位址](address-ovr.md) 和 [媒體類型](media-type-ovr.md) 中註冊感興趣的 TAPI 應用程式將會收到 [事件通知](event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="dddd7-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="dddd7-105">只有一個應用程式會透過會話提供擁有權 [許可權](privilege-ovr.md) 。</span><span class="sxs-lookup"><span data-stu-id="dddd7-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="dddd7-106">此應用程式無法拒絕會話。</span><span class="sxs-lookup"><span data-stu-id="dddd7-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="dddd7-107">傳入會話的初始撥號狀態為 [提供]。</span><span class="sxs-lookup"><span data-stu-id="dddd7-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="dddd7-108">當通話處於供應狀態時，如果服務提供者提供了此資訊且可供使用，則應用程式可以取得持有人模式和呼叫原因等資訊。</span><span class="sxs-lookup"><span data-stu-id="dddd7-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="dddd7-109">某些呼叫資訊可能無法立即使用，例如呼叫者識別碼。</span><span class="sxs-lookup"><span data-stu-id="dddd7-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="dddd7-110">提供的會話有六個基本的回應： [回答](answer-ovr.md)、 [接受](accept-ovr.md)、 [遞交](handoffs-ovr.md)、 [捨棄](drop-ovr.md)、 [轉寄](forward-ovr.md)和重新 [導向](redirect-ovr.md)。</span><span class="sxs-lookup"><span data-stu-id="dddd7-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="dddd7-111">根據服務提供者，這些作業的完整集合可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="dddd7-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



