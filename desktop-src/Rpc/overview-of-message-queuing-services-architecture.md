---
title: 訊息佇列服務架構總覽
description: 訊息佇列服務 (MSMQ) 使用網站/企業模型。 一般而言，網站是實體位置，例如建築物。 企業包含一或多個網站，並代表一個組織。
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301563"
---
# <a name="overview-of-message-queuing-services-architecture"></a>訊息佇列服務架構總覽

訊息佇列服務 (MSMQ) 使用網站/企業模型。 一般而言，網站是實體位置，例如建築物。 企業包含一或多個網站，並代表一個組織。

下圖說明 MSMQ 服務的架構。

![msmq 架構](images/msmq.png)

MSMQ 的核心是訊息佇列資訊服務 (MQIS) 資料庫，這會在 SQL Server 上執行。 企業有單一的主要 MQIS，稱為「主要企業控制器」。 每個網站都有自己的 MQIS，稱為 *主要網站控制器* 以及零或多個 *備份網站控制器*。 最後，有個別的用戶端電腦，每個電腦都有自己的佇列管理員，並以服務的形式執行。 主要企業控制器也可以是主要網站控制器，而且任何控制器也可以是用戶端。

訊息佇列可以是公用或私用。 公用佇列會在 Active Directory 中註冊，並可在網路上存取。 公用佇列中的訊息會路由傳送到整個企業，在 MSMQ 的控制之下。 用戶端應用程式訊息會在網站控制器的佇列管理員之間移動，以從用戶端的佇列管理員移至目的地佇列。

私用佇列是由本機佇列管理員維護，而且不會在 Active Directory 中註冊。 私用佇列訊息的範圍僅限於它們所在的電腦。

 

 




