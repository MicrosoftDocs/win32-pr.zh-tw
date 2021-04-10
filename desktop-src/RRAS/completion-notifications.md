---
title: 完成通知
description: 在完成連接作業之前，遠端存取連線管理員會繼續進度通知。
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021489"
---
# <a name="completion-notifications"></a>完成通知

在完成連接作業之前，遠端存取連線管理員會繼續進度通知。 這會發生在下列情況：

-   處理常式會收到 RASCS \_ 連接，或 RASCS \_ 中斷連線的通知。 RAS 用戶端應用程式可以結束，而不會中斷任何已建立的連接。
-   發生錯誤。 處理常式會收到通知，指出發生錯誤時的錯誤和連接狀態。 RAS 用戶端應用程式可能會結束。

在呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)之後，RAS 用戶端應用程式不應假設連接作業已完成。 在結束之前，它應該等待上述其中一個條件。

 

 




