---
description: Windows 通訊端中的一般點對點通訊端與 c \_ 根 multipoint 通訊端之間的差異 (Winsock) SPI。
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: SPI 中 Multipoint 通訊端和一般通訊端之間的語義差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974600"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>SPI 中 Multipoint 通訊端和一般通訊端之間的語義差異

在控制平面中，c \_ 根通訊端和一般點對點通訊端之間有一些重要的語義差異：

-   C \_ 根通訊端可以在 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 中用來聯結新的分葉。
-   藉 \_ 由呼叫 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) 將 c 根通訊端放入接聽模式 (，並不會 \_ 防止 c 根通訊端在 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 的呼叫中用來加入新的分葉，或是用於傳送和接收 multipoint 資料。
-   關閉 c \_ 根通訊端會導致所有相關聯的 c 分 \_ 葉通訊端取得 FD \_ 關閉通知。

在 \_ 控制平面中，c 分葉通訊端和一般通訊端之間沒有任何語義上的差異，不同之處在于 c 分 \_ 葉通訊端可以在 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)中使用，而 \_ 在 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) 中使用 c 分葉通訊端表示只應接受 multipoint 連接要求。

在資料平面中，d \_ 根通訊端和一般點對點通訊端之間的語義差異如下：

-   在 d 根通訊端上傳送的資料 \_ 將會傳遞至相同 multipoint 會話中的所有葉。
-   D 根通訊端上接收的資料 \_ 可能來自任何離開。

\_根資料平面中的 d 分葉通訊端與一般通訊端沒有任何語義差異，不過，在 nonrooted 資料平面中，d 分葉通訊端上傳送的資料 \_ 將會移至所有其他分葉節點，而接收的資料可能來自其他任何分葉節點。 如先前所述，d 分 \_ 葉通訊端是否位於根目錄或 nonrooted 資料平面中的相關資訊，是否包含在通訊端的對應 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中。

 

 
