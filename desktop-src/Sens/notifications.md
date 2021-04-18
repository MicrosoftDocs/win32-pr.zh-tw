---
description: 系統事件通知服務可讓行動感知的應用程式接收來自 SENS 監視之系統事件的通知。 當要求的事件發生時，SENS 會通知應用程式。
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: '通知 (系統事件通知服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971548"
---
# <a name="notifications-system-event-notification-service"></a>通知 (系統事件通知服務) 

系統事件通知服務可讓行動感知的應用程式接收來自 SENS 監視之系統事件的通知。 當要求的事件發生時，SENS 會通知應用程式。

SENS 可以通知應用程式有三個系統事件類別：

-   TCP/IP 網路事件，例如 TCP/IP 網路連接的狀態或連接的品質。
-   使用者登入事件。
-   電池和 AC 電源事件。

例如，應用程式可以訂閱下列任何系統事件：

-   建立網路連線能力
-   當指定的連線 (QOC) 參數時，可在指定的連線品質內達到指定的目的地時發出通知
-   電腦已切換到電池電源
-   剩餘電池計量的百分比在指定的參數內
-   發生使用同步處理管理員的已排程事件

**Windows Server 2008 R2 和 windows 7：** 訂閱者最多需要3分鐘的時間，才能回應 [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) 和 [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) 介面上的通知。 3分鐘之後，SENS 會取消對訂閱者的呼叫，並解除封鎖通知執行緒。 如果需要較長的作業來回應通知，請儘快傳回 **ISensLogon** 或 **ISensLogon2** ，然後開啟另一個執行緒進行處理。

 

 



