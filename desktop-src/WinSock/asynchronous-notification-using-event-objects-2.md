---
description: WSAEventSelect 和 WSAEnumNetworkEvents 函式的目的是為了容納應用程式，例如沒有使用者介面 (的守護程式和服務，因此不會使用 Windows 控制碼) 。
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: 使用事件物件的非同步通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848027"
---
# <a name="asynchronous-notification-using-event-objects"></a>使用事件物件的非同步通知

[**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)和 [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents)函式的目的是為了容納應用程式，例如沒有使用者介面 (的守護程式和服務，因此不會使用 Windows 控制碼) 。 **WSAEventSelect** 函式的行為與 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)函數完全相同。 但是，不會在發生 FD XXX 網路事件時傳送 Windows 訊息 \_ (例如，fd \_ READ 和 FD \_ WRITE) ，會設定應用程式指定的事件物件。

此外， \_ 服務提供者還會記住特定的 FD XXX 網路事件。 應用程式可以呼叫 [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ，將網路事件記憶體的目前內容複寫到應用程式提供的緩衝區，並自動清除網路事件記憶體。 如有需要，應用程式也可以指定已清除的特定事件物件，以及網路事件記憶體。

 

 



