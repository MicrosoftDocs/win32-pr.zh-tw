---
title: Named-Pipe 通訊協定上的非同步 RPC
description: 如果您使用具名管道 (ncacn \_ np) 做為傳輸通訊協定，您應該避免在伺服器上允許大量閒置暫止的呼叫。
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1dade78846bc978abeb8bbbe5c324144db2645177722ca5afd1a62f99a3ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023668"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>Named-Pipe 通訊協定上的非同步 RPC

如果您使用具名管道 ([**ncacn \_ Np**](/windows/desktop/Midl/ncacn-np)) 做為傳輸通訊協定，您應該避免在伺服器上允許大量閒置暫止的呼叫。 使用具名管道時，每個等候回復的用戶端都將在伺服器上讀取暫止的具名管道，而每個用戶端都需要特定數量的核心記憶體。

例如，您不會想要對具有具名管道傳輸的新電子郵件使用通知呼叫，因為即使用戶端閒置，而且核心記憶體可能會耗盡，這類呼叫仍會維持擱置狀態。 請注意，這不是其他連接導向通訊協定的問題，例如 [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)。

由於具名管道是傳輸通訊協定，因此您的應用程式可以藉由指定 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 作為字串系結中的通訊協定來使用它們。 如需具名管道的詳細資訊，請參閱 [具名管道](/windows/desktop/ipc/named-pipes)。 如需建立字串系結的詳細資訊，請參閱 [使用字串](finding-server-host-systems.md)系結。

 

 