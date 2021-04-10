---
title: 關於路由表管理員第1版
description: 路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- 路由及遠端存取服務 RRAS，路由表管理員第1版
- 路由及遠端存取服務 RRAS，路由表管理員第1版，描述
- 路由表管理員第1版 RRAS
- 路由表管理員第1版 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021571"
---
# <a name="about-routing-table-manager-version-1"></a>關於路由表管理員第1版

**Windows Server 2003：** 此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 新的應用程式應該使用路由表管理員第2版 API。

路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。 路由表管理員會提供路由資訊給所有感興趣的元件，例如路由通訊協定、管理代理程式和監視代理程式。 路由表管理員也會決定路由通訊協定已知的每個目的地網路的最佳路由。 它會根據路由通訊協定優先順序以及與路由相關聯的計量來決定此路由。 請注意，系統管理員可以設定路由通訊協定優先順序。 路由表管理員接著會將最佳路由資訊傳遞至轉寄站，並傳回路由通訊協定。

每個路由通訊協定都會呼叫 [**RtmRegisterClient**](rtmregisterclient.md) 來向路由表管理員註冊。 **RtmRegisterClient** 會傳回路由通訊協定用來新增或刪除路由專案的控制碼。 **RtmRegisterClient** 也可讓路由通訊協定向路由表管理員註冊事件物件。 路由表管理員會通知此事件物件，以通知路由通訊協定中的最佳路由資訊變更。 所有其他元件都可以透過路由列舉來取得路由表管理員中儲存的資訊。

 

 




