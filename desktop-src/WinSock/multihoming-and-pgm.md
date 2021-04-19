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
# <a name="multihoming-and-pgm"></a>多宿主和 PGM

必須將特殊考慮提供給多宿主的 PGM 傳送者或接收者。 此頁面描述考慮，並提供最佳程式設計作法的指導方針。

## <a name="multihomed-pgm-sender"></a>多重主目錄的 PGM 傳送者

當應用程式無法在呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式時指定介面時，就會使用第一個可用的介面。 如果沒有可用的介面， **連接將** 會失敗。

當應用程式使用 [RM \_ SET \_ SEND \_ IF](socket-options.md) socket 選項來指定介面時，會使用 [**tcp/ip 以隱含**](/windows/desktop/api/winsock/nf-winsock-bind) 方式對該介面進行系結嘗試，如果 tcp/ip 對系結要求失敗，則會失敗。 如果介面是使用 RM \_ set SEND 設定 \_ \_ ，如果有多次，則只適用最後一個介面設定。

Windows 通訊端會維護已設定的介面，如果該介面消失，會話就會中斷連線。

## <a name="multihomed-pgm-receiver"></a>多重主目錄的 PGM 接收器

當應用程式無法在呼叫 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函式時指定介面時，就會使用預設介面。 如果沒有可用的介面，系結 [**會失敗。**](/windows/desktop/api/winsock/nf-winsock-bind)

當應用程式指定一或多個要接聽的介面時，如果 Windows 通訊端嘗試使用 TCP/IP 系結至要求的介面或介面， [則使用 RM \_ ADD \_ RECEIVE \_ ](socket-options.md)。 任何來自 TCP/IP 的錯誤都會導致此要求失敗。 不同于 PGM 傳送者的情況，多次新增接收介面會導致接聽程式張貼在所有成功新增的介面上。 \_ \_ \_ 如果通訊端選項停止接聽介面，請使用 RM DEL RECEIVE。

Windows 通訊端不會維護多個指定接聽介面的狀態，而是會依賴 TCP/IP 來執行這項操作。 但是，當會話正在進行時，Windows 通訊端會追蹤該會話的連入介面，如果該介面消失，Windows 通訊端就會中斷會話的連線。

 

 



