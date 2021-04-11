---
description: WSPListen、WSPAccept 和 WSPConnect 的通訊協定基本概念，用來建立與 Windows 通訊端的通訊端連線 (Winsock) 。
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 通訊協定基本概念：接聽、連接、接受
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62ef290d71e571154b4d022c24c7e21f8fffa1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113017"
---
# <a name="protocol-basics-listen-connect-accept"></a>通訊協定基本概念：接聽、連接、接受

在用戶端-伺服器範例中，建立通訊端連線所牽涉到的基本作業最方便說明。

伺服器端會先建立通訊端、將其系結至已知的本機位址 (以便讓用戶端找到) ，然後透過 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))將通訊端置於接聽模式，以準備任何連入連線要求，並指定連線待處理專案佇列的長度。 服務提供者會將暫止的連接要求保存在待處理專案佇列中，直到伺服器處理這些要求或因為用戶端的超時) 而撤銷 (為止。 服務提供者可能會以無訊息方式忽略要求，將待處理專案佇列的大小延伸到超出提供者定義的上限。

此時，如果正在使用封鎖通訊端，伺服器端可能會立即呼叫 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) ，這會封鎖直到連線要求擱置為止。 相反地，伺服器也可以使用先前討論的其中一個網路事件指示機制，來排列連入連線要求的通知。 視所選的通知機制而定，提供者會在連接要求抵達時發出 Windows 訊息或發出事件物件的信號。 請參閱 [網路事件通知](notification-of-network-events-2.md) ，以瞭解如何註冊 FD \_ 接受網路事件。

用戶端會建立適當的通訊端，並藉由呼叫 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))來起始連線，並指定已知的伺服器位址。 用戶端通常不會在起始連接之前 [**執行明確的**](/windows/desktop/api/winsock/nf-winsock-bind) 系結作業，以允許服務提供者代表他們執行隱含系結。 如果通訊端處於封鎖模式，則 **WSPConnect** 會封鎖，直到伺服器收到 (的連線要求，或直到超時) 。 否則，用戶端應該使用先前討論的其中一個網路事件指示機制，來排列建立新連線的通知。 視所選的通知機制而定，提供者會透過 Windows 訊息或透過通知事件物件來指出這一點。

當伺服器端叫用 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)時，服務提供者會呼叫應用程式提供的條件函式，並使用函式參數從連接要求待處理專案佇列中的最上層專案傳遞至伺服器資訊。 這項資訊包括連線主機的位址、任何可用的使用者資料，以及任何可用的 QoS 資訊。 使用這種資訊，伺服器的條件函式會決定是否要接受要求、拒絕要求，還是延遲在稍後進行決策。 這項決定是透過 condition 函式的傳回值來表示。 請參閱 [網路事件通知](notification-of-network-events-2.md) ，以瞭解如何註冊 FD \_ CONNECT 網路事件。

如果伺服器決定接受要求，則提供者必須使用所有與接聽通訊端相同的屬性和事件註冊來建立新的通訊端。 原始通訊端會保持在接聽狀態，以便接收後續的連接要求。 透過 condition 函數的 output 參數，伺服器也可以提供任何回應使用者資料並指派 QoS 參數， (假設服務提供者) 支援這些作業。

 

 
