---
title: 執行託管裝置
description: 具有 UPnP 技術的裝置主機會實行核心的 UPnP 通訊協定探索、描述、控制和事件。
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675251"
---
# <a name="implementing-a-hosted-device"></a>執行託管裝置

具有 UPnP 技術的裝置主機會實行核心的 UPnP 通訊協定：探索、描述、控制和事件。 執行託管裝置的開發人員只需要提供：

-   裝置及其服務的描述。
-   裝置功能的實作為。

例如，時鐘裝置的開發人員必須為其提供以 UPnP 為基礎的裝置和服務描述，並可執行時鐘函式 (例如維持時間、設定時間，以及回應目前時間) 的查詢。 裝置主機：

-   根據 UPnP 探索通訊協定宣佈裝置。
-   回應裝置描述的查詢。
-   將控制權要求路由至裝置程式碼中執行時鐘函數的部分。
-   維護服務的事件訂閱。
-   當服務的狀態變更時，將事件通知傳送給訂閱者。

 

 




