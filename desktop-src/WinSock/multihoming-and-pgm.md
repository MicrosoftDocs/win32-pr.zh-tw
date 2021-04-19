---
description: 必須將特殊考慮提供給多宿主的 PGM 傳送者或接收者。 此頁面描述考慮，並提供最佳程式設計作法的指導方針。
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: 多宿主和 PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972630"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="5d227-104">多宿主和 PGM</span><span class="sxs-lookup"><span data-stu-id="5d227-104">Multihoming and PGM</span></span>

<span data-ttu-id="5d227-105">必須將特殊考慮提供給多宿主的 PGM 傳送者或接收者。</span><span class="sxs-lookup"><span data-stu-id="5d227-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="5d227-106">此頁面描述考慮，並提供最佳程式設計作法的指導方針。</span><span class="sxs-lookup"><span data-stu-id="5d227-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="5d227-107">多重主目錄的 PGM 傳送者</span><span class="sxs-lookup"><span data-stu-id="5d227-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="5d227-108">當應用程式無法在呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式時指定介面時，就會使用第一個可用的介面。</span><span class="sxs-lookup"><span data-stu-id="5d227-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="5d227-109">如果沒有可用的介面， **連接將** 會失敗。</span><span class="sxs-lookup"><span data-stu-id="5d227-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="5d227-110">當應用程式使用 [RM \_ SET \_ SEND \_ IF](socket-options.md) socket 選項來指定介面時，會使用 [**tcp/ip 以隱含**](/windows/desktop/api/winsock/nf-winsock-bind) 方式對該介面進行系結嘗試，如果 tcp/ip 對系結要求失敗，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="5d227-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="5d227-111">如果介面是使用 RM \_ set SEND 設定 \_ \_ ，如果有多次，則只適用最後一個介面設定。</span><span class="sxs-lookup"><span data-stu-id="5d227-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="5d227-112">Windows 通訊端會維護已設定的介面，如果該介面消失，會話就會中斷連線。</span><span class="sxs-lookup"><span data-stu-id="5d227-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="5d227-113">多重主目錄的 PGM 接收器</span><span class="sxs-lookup"><span data-stu-id="5d227-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="5d227-114">當應用程式無法在呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函式時指定介面時，就會使用預設介面。</span><span class="sxs-lookup"><span data-stu-id="5d227-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="5d227-115">如果沒有可用的介面，系結 [**會失敗。**](/windows/desktop/api/winsock/nf-winsock-bind)</span><span class="sxs-lookup"><span data-stu-id="5d227-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="5d227-116">當應用程式指定一或多個要接聽的介面時，如果 Windows 通訊端嘗試使用 TCP/IP 系結至要求的介面或介面， [則使用 RM \_ ADD \_ RECEIVE \_ ](socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="5d227-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="5d227-117">任何來自 TCP/IP 的錯誤都會導致此要求失敗。</span><span class="sxs-lookup"><span data-stu-id="5d227-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="5d227-118">不同于 PGM 傳送者的情況，多次新增接收介面會導致接聽程式張貼在所有成功新增的介面上。</span><span class="sxs-lookup"><span data-stu-id="5d227-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="5d227-119">\_ \_ \_ 如果通訊端選項停止接聽介面，請使用 RM DEL RECEIVE。</span><span class="sxs-lookup"><span data-stu-id="5d227-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="5d227-120">Windows 通訊端不會維護多個指定接聽介面的狀態，而是會依賴 TCP/IP 來執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="5d227-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="5d227-121">但是，當會話正在進行時，Windows 通訊端會追蹤該會話的連入介面，如果該介面消失，Windows 通訊端就會中斷會話的連線。</span><span class="sxs-lookup"><span data-stu-id="5d227-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



