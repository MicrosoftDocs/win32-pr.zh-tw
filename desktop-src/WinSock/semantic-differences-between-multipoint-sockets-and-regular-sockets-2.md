---
title: Multipoint 通訊端和一般通訊端之間的語義差異
description: C \_ 根 multipoint 通訊端和一般點對點通訊端之間的差異。
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983433"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="6aaab-103">Multipoint 通訊端和一般通訊端之間的語義差異</span><span class="sxs-lookup"><span data-stu-id="6aaab-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="6aaab-104">在控制平面中，c \_ 根通訊端和一般點對點通訊端之間有一些重要的語義差異：</span><span class="sxs-lookup"><span data-stu-id="6aaab-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="6aaab-105">C \_ 根通訊端可以在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 中用來聯結新的分葉。</span><span class="sxs-lookup"><span data-stu-id="6aaab-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="6aaab-106">藉 \_ 由呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) 將 c 根通訊端放入接聽模式 (，並不會阻止 c \_ 根通訊端在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 的呼叫中使用，以加入新的分葉，或是用於傳送和接收 multipoint 資料。</span><span class="sxs-lookup"><span data-stu-id="6aaab-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="6aaab-107">關閉 c \_ 根通訊端會導致所有相關聯的 c 分 \_ 葉通訊端取得 FD \_ 關閉通知。</span><span class="sxs-lookup"><span data-stu-id="6aaab-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="6aaab-108">在 \_ 控制平面中，c 分葉通訊端和一般通訊端之間沒有任何語義上的差異，不同之處在于 c 分 \_ 葉通訊端可以在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)中使用，而 \_ [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 中的 c 分葉通訊端表示只應接受 multipoint 連接要求。</span><span class="sxs-lookup"><span data-stu-id="6aaab-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="6aaab-109">在資料平面中，d \_ 根通訊端和一般點對點通訊端之間的語義差異如下：</span><span class="sxs-lookup"><span data-stu-id="6aaab-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="6aaab-110">在 d 根通訊端上傳送的資料 \_ 會傳遞至相同 multipoint 會話中的所有保留。</span><span class="sxs-lookup"><span data-stu-id="6aaab-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="6aaab-111">D 根通訊端上接收的資料 \_ 可能來自任何離開。</span><span class="sxs-lookup"><span data-stu-id="6aaab-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="6aaab-112">\_根資料平面中的 d 分葉通訊端與一般通訊端沒有任何語義差異，不過，在 nonrooted 資料平面中，d 分葉通訊端上傳送的資料會 \_ 移至所有其他分葉節點，而接收的資料可能來自任何其他分葉節點。</span><span class="sxs-lookup"><span data-stu-id="6aaab-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="6aaab-113">如先前所述，d 分 \_ 葉通訊端是否位於根目錄或 nonrooted 資料平面中的相關資訊，是否包含在通訊端的對應 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中。</span><span class="sxs-lookup"><span data-stu-id="6aaab-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
