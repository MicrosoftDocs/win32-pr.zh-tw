---
title: 視窗工作站
description: 視窗工作站包含剪貼簿、atom 資料表，以及一或多個桌面物件。 每個視窗工作站物件都是安全物件。 建立視窗站時，它會與呼叫進程建立關聯，並指派給目前的會話。
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- 視窗站物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d55e43a0db21b23a6704949f0d72a184c9034f625689b800814ac8a93891b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199689"
---
# <a name="window-stations"></a>視窗工作站

*視窗工作站* 包含剪貼簿、atom 資料表，以及一或多個 [桌面](desktops.md)物件。 每個視窗工作站物件都是安全物件。 建立視窗站時，它會與呼叫進程建立關聯，並指派給目前的會話。

*互動式視窗工作站* 是唯一可以顯示使用者介面或接收使用者輸入的視窗站。 它會指派給互動式使用者的登入會話，並包含鍵盤、滑鼠和顯示裝置。 它一律命名為 "WinSta0"。 所有其他視窗工作站都是非互動式的，這表示它們無法顯示使用者介面或接收使用者輸入。

當使用者使用遠端桌面服務登入電腦時，就會啟動使用者的會話。 每個會話都與其本身的互動式視窗工作站（名為 "WinSta0"）相關聯。 如需詳細資訊，請參閱 [遠端桌面會話](/windows/desktop/TermServ/terminal-services-sessions)。

如需視窗工作站的詳細資訊，請參閱下列主題：

-   [視窗工作站和桌面建立](window-station-and-desktop-creation.md)
-   [處理與視窗工作站的連接](process-connection-to-a-window-station.md)
-   [Windows 工作站安全性與存取權限](window-station-security-and-access-rights.md)

 

 