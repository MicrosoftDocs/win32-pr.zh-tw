---
description: 郵筒是單向處理序間通訊的一種機制， (IPC) 。 應用程式可以將訊息儲存在信箱中。 郵筒的擁有者可以取出儲存在該處的訊息。
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975264"
---
# <a name="mailslots"></a>Mailslots

*郵筒* 是單向處理序間通訊的一種機制， (IPC) 。 應用程式可以將訊息儲存在信箱中。 郵筒的擁有者可以取出儲存在該處的訊息。 這些訊息通常會透過網路傳送到指定的電腦或指定網域中的所有電腦。 *網域* 是共用組名的一組工作站和伺服器。

-   [關於 Mailslots](about-mailslots.md)
-   [使用 Mailslots](using-mailslots.md)
-   [郵筒參考](mailslot-reference.md)

您可以選擇使用 [具名管道](named-pipes.md) 或 [Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2) ，而非 mailslots 進行處理序間通訊。 具名管道是一種簡單的方法，可讓兩個進程交換訊息。 相反地，Mailslots 是一種簡單的方式，可讓程式將訊息廣播至多個進程。 其中一個重要的考慮是 mailslots 使用資料包廣播訊息。 *資料包* 是網路在網路上傳送的小型資訊封包。 和無線電或電視廣播一樣，資料包不會提供回條的確認;沒有任何方法可保證已收到資料包。 就像山脈、大型建築或干擾信號可能會導致無線電或電視信號遺失，有一些東西可以防止資料包到達特定目的地。 具名管道就像電話一樣：您只會與一個合作物件通訊，但您知道訊息正在接收。

 

 
