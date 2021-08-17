---
title: Multipoint 通訊端和一般通訊端之間的語義差異
description: C \_ 根 multipoint 通訊端和一般點對點通訊端之間的差異。
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b30ff05c72fc43bf3f4e731242d9f22a2236e9f6fd275c382b57fb05d094cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740808"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Multipoint 通訊端和一般通訊端之間的語義差異

在控制平面中，c \_ 根通訊端和一般點對點通訊端之間有一些重要的語義差異：

-   C \_ 根通訊端可以在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 中用來聯結新的分葉。
-   藉 \_ 由呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) 將 c 根通訊端放入接聽模式 (，並不會阻止 c \_ 根通訊端在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 的呼叫中使用，以加入新的分葉，或是用於傳送和接收 multipoint 資料。
-   關閉 c \_ 根通訊端會導致所有相關聯的 c 分 \_ 葉通訊端取得 FD \_ 關閉通知。

在 \_ 控制平面中，c 分葉通訊端和一般通訊端之間沒有任何語義上的差異，不同之處在于 c 分 \_ 葉通訊端可以在 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)中使用，而 \_ [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 中的 c 分葉通訊端表示只應接受 multipoint 連接要求。

在資料平面中，d \_ 根通訊端和一般點對點通訊端之間的語義差異如下：

-   在 d 根通訊端上傳送的資料 \_ 會傳遞至相同 multipoint 會話中的所有保留。
-   D 根通訊端上接收的資料 \_ 可能來自任何離開。

\_根資料平面中的 d 分葉通訊端與一般通訊端沒有任何語義差異，不過，在 nonrooted 資料平面中，d 分葉通訊端上傳送的資料會 \_ 移至所有其他分葉節點，而接收的資料可能來自任何其他分葉節點。 如先前所述，d 分 \_ 葉通訊端是否位於根目錄或 nonrooted 資料平面中的相關資訊，是否包含在通訊端的對應 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中。

 

 
