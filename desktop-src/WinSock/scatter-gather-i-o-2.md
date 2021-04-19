---
description: WSARecv、WSARecvFrom、WSARecvMsg、WSASend、WSASendMsg 和 WSASendTo 函數全都採用應用程式緩衝區的陣列作為輸入參數，並可用於散佈/收集 (或向量) i/o。
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: 散佈/收集 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983434"
---
# <a name="scattergather-io"></a><span data-ttu-id="ae337-103">散佈/收集 i/o</span><span class="sxs-lookup"><span data-stu-id="ae337-103">Scatter/Gather I/O</span></span>

<span data-ttu-id="ae337-104">[**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)、 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)和 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)函數全都採用應用程式緩衝區的陣列作為輸入參數，並可用於散佈/收集 (或向量) i/o。</span><span class="sxs-lookup"><span data-stu-id="ae337-104">The [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) functions all take an array of application buffers as input parameters and can be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="ae337-105">這在傳送的每個訊息的部分包含一或多個固定長度的標頭元件（除了訊息內文以外）時，這可能非常有用。</span><span class="sxs-lookup"><span data-stu-id="ae337-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed-length header components in addition to the message body.</span></span> <span data-ttu-id="ae337-106">在傳送之前，應用程式不需要將這類標頭元件串連成單一連續緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae337-106">Such header components need not be concatenated by the application into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="ae337-107">同樣地，在接收時，標頭元件可以自動分割成不同的緩衝區，並將訊息主體視為本身。</span><span class="sxs-lookup"><span data-stu-id="ae337-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body by itself.</span></span>

<span data-ttu-id="ae337-108">當接收到多個緩衝區時，不論是否使用所有提供的緩衝區，都會在從網路抵達資料時完成。</span><span class="sxs-lookup"><span data-stu-id="ae337-108">When receiving into multiple buffers, completion occurs as data arrives from the network, regardless of whether all the supplied buffers are utilized.</span></span>

 

 
