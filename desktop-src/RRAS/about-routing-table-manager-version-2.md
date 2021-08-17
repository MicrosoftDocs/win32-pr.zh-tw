---
title: 關於路由表管理員第2版
description: 下列檔說明路由表管理員第2版 (RTMv2) 技術。
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- 路由及遠端存取服務 RRAS，路由表管理員第2版
- 路由及遠端存取服務 RRAS，路由表管理員第2版，描述
- 路由表管理員第2版 RRAS
- 路由表管理員第2版 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87228222f31daf7f951064d05c92d950a3fff0d570fcac3536887b50193b16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792105"
---
# <a name="about-routing-table-manager-version-2"></a>關於路由表管理員第2版

下列檔說明路由表管理員第2版 (RTMv2) 技術。 RTMv2 API 是 Windows 2000 和更新版本作業系統的一項功能，可用來撰寫與路由表管理員互動的路由通訊協定。

路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。

Windows NT 4.0 版無法使用 RTMv2。 此外，RTMv2 不能用於 Windows NT 4.0 或 Windows 2000 上執行的 IPX 路由通訊協定。 如果您使用的是 IPX 或正在撰寫 Windows NT 4.0 的路由通訊協定，請參閱[關於路由表管理員第1版](about-routing-table-manager-version-1.md)。

本總覽將說明下列主題：

-   [路由表管理員架構的元件](components-of-the-routing-table-manager-architecture.md)
-   [向路由表管理員註冊](registering-with-the-routing-table-manager.md)
-   [列舉已註冊的實體](enumerating-registered-entities.md)
-   [使用方法](using-methods.md)
-   [使用不透明的指標](using-opaque-pointers.md)
-   [標示 Hold-Down 狀態的路由](marking-routes-for-the-hold-down-state.md)
-   [新增路由](adding-routes.md)
-   [正在抓取路由資訊](retrieving-route-information.md)
-   [更新路由](updating-routes.md)
-   [接收變更的通知](receiving-notification-of-changes.md)
-   [使用下一個躍點](working-with-next-hops.md)
-   [列舉路由表專案](enumerating-routing-table-entries.md)
-   [尋找路由表中的特定資訊](finding-specific-information-in-the-routing-table.md)
-   [維護 Client-Specific 清單](maintaining-client-specific-lists.md)
-   [管理控制碼](managing-handles.md)

 

 




