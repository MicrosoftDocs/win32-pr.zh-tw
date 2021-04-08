---
title: 路由器初始化
description: 路由器、路由器管理員和路由通訊協定/用戶端的設定資訊會劃分為全域資訊和每個介面資訊，並且儲存在登錄和路由器的電話簿檔案（node.js）中。
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- 路由器 RRAS，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670899"
---
# <a name="router-initialization"></a>路由器初始化

路由器、路由器管理員和路由通訊協定/用戶端的設定資訊會劃分為全域資訊和每個介面資訊，並且儲存在登錄和路由器的電話簿檔案（node.js）中。

當路由器進程啟動時，DIM (動態介面管理員) 從登錄讀取路由器設定。 DIM 會建立介面資訊所指定的介面。

DIM 也會捕獲全域路由器管理員資訊。 DIM 會啟動對應至此資訊的路由器管理員，並將資訊傳遞給它們。 例如，如果 DIM 在登錄中找到 IP 路由器管理員的全域資訊，則 DIM 會啟動 IP 路由器管理員，並將全域資訊傳遞給它。 如果特定路由器管理員的登錄中沒有任何全域資訊，則 DIM 不會啟動該路由器管理員。

路由器管理員會檢查從 DIM 接收的全域資訊。 如果路由器管理員在全域資訊中找到特定用戶端的特定資訊，則路由器管理員會載入用戶端的 DLL (例如 IpNAT.dll) ，並藉由呼叫用戶端的 [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) 和 [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) 函式來初始化用戶端。 路由器管理員會在呼叫 [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)時，將用戶端特定的全域資訊傳遞給用戶端。

在每個階段，傳遞給下一個實體的資訊對其前面的實體而言是不透明的。 也就是說，DIM 不會解讀 IP 路由器管理員的全域資訊，而是要讓 IP 路由器管理員知道這項資訊。 同樣地，「IP 路由器管理員」並不會解讀 OSPF 的特定資訊，因為它是 OSPF 資訊。

 

 




