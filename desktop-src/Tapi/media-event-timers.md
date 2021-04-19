---
description: 許多應用程式都取決於媒體事件之間的時間關聯性 (例如，所收到的 DTMF 數位) 用來判斷要求之作業的本質。
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: 媒體事件計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976404"
---
# <a name="media-event-timers"></a><span data-ttu-id="060b9-103">媒體事件計時器</span><span class="sxs-lookup"><span data-stu-id="060b9-103">Media Event Timers</span></span>

<span data-ttu-id="060b9-104">許多應用程式都取決於媒體事件之間的時間關聯性 (例如，所收到的 DTMF 數位) 用來判斷要求之作業的本質。</span><span class="sxs-lookup"><span data-stu-id="060b9-104">Many applications depend on the timing relationship between media events (for example, DTMF digits received) to determine the nature of a requested operation.</span></span> <span data-ttu-id="060b9-105">例如，在語音信箱應用程式中，兩個連續的 DTMF "1" 數位可能表示「備份兩個區段」或「從訊息開頭重新執行」，取決於兩個數字之間經過多少時間。</span><span class="sxs-lookup"><span data-stu-id="060b9-105">For example, in a voice mail application, two consecutive DTMF "1" digits may mean "back up two segments" or "replay from beginning of message", depending on how much time elapsed between the two digits.</span></span> <span data-ttu-id="060b9-106">在用戶端/伺服器環境中，如果在應用程式執行所在的不同處理器上執行 DTMF 偵測，則在區域網路中的延遲會讓媒體事件之間的時間關聯性變得很有可能扭曲，進而導致這些以時間為基礎的差異可能遺失或變成不可靠。</span><span class="sxs-lookup"><span data-stu-id="060b9-106">In a client/server environment, if the DTMF detection is being performed on a separate processor from the one on which the application is running, latency in the local area network makes it very likely that the timing relationship between media events will be skewed, with the result that these timing-based differences could be lost or become unreliable.</span></span>

<span data-ttu-id="060b9-107">若要解決此問題，您可以將數個 TAPI 訊息加上時間戳記。</span><span class="sxs-lookup"><span data-stu-id="060b9-107">To resolve this issue, several TAPI messages can be timestamped.</span></span> <span data-ttu-id="060b9-108">因為這是這些事件之間的相對時間，所以事件的「時鐘時間」並不重要，而且牽涉到倒數第二次的時間，這些時間戳記會使用 [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函式所傳回的毫秒解析「從 Windows 啟動以來的時間」。</span><span class="sxs-lookup"><span data-stu-id="060b9-108">Because it is the relative timing between these events that is important, the "clock time" of the event is not important, and sub-second timing is involved, these timestamps use the millisecond-resolution "time since Windows started" returned by the [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) function.</span></span> <span data-ttu-id="060b9-109">應用程式必須注意這是伺服器 (或電腦上的滴答計數，此服務提供者直接管理硬體正在執行) ，而且不一定是應用程式執行所在的同一部電腦;因此，這些 TAPI 訊息中的時間戳記只能與彼此進行比較，而不能與應用程式執行所在處理器上的 **GetTickCount** 所傳回的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="060b9-109">Applications must be aware that this is the tick count on the server (or machine where the service provider directly managing the hardware is running), and is not necessarily the same machine on which the application is executing; thus, the timestamps in these TAPI messages can only be compared to each other, and not to the value returned by **GetTickCount** on the processor on which the application is running.</span></span>

<span data-ttu-id="060b9-110">可能有時間戳記的 TAPI 訊息如下： [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)和 [**行 \_ MONITORTONE**](line-monitortone.md)。</span><span class="sxs-lookup"><span data-stu-id="060b9-110">The TAPI messages that can be timestamped are: [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), and [**LINE\_MONITORTONE**](line-monitortone.md).</span></span> <span data-ttu-id="060b9-111">滴答計數會插入這些訊息的 *dwParam3* 中。</span><span class="sxs-lookup"><span data-stu-id="060b9-111">The tick count is inserted into *dwParam3* of these messages.</span></span> <span data-ttu-id="060b9-112">如果服務提供者不支援時間戳記 (這會由這些訊息中的服務提供者設定 *dwParam3* 指定為 0) ，則 TAPI 本身會將滴答計數插入所有這些訊息的 *dwParam3* 中 (它會稍微扭曲，但在訊息已到達處理序間通訊配置) 的情況下，則小於應用程式的執行方式。</span><span class="sxs-lookup"><span data-stu-id="060b9-112">If timestamping is not supported by the service provider (which is indicated by the service provider setting *dwParam3* in these messages to 0), then TAPI itself will insert the tick count into *dwParam3* of all of these messages (it can be skewed somewhat, but less than if the application did the same after the messages had traversed an interprocess communication scheme).</span></span>

 

 
