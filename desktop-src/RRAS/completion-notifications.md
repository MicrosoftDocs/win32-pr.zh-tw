---
title: 完成通知
description: 在完成連接作業之前，遠端存取連線管理員會繼續進度通知。
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6dcfad1ae0dfd4eefb3df00dceefce0df77d93239a6e7c2c4fa6517cac25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791602"
---
# <a name="completion-notifications"></a>完成通知

在完成連接作業之前，遠端存取連線管理員會繼續進度通知。 這會發生在下列情況：

-   處理常式會收到 RASCS \_ 連接，或 RASCS \_ 中斷連線的通知。 RAS 用戶端應用程式可以結束，而不會中斷任何已建立的連接。
-   發生錯誤。 處理常式會收到通知，指出發生錯誤時的錯誤和連接狀態。 RAS 用戶端應用程式可能會結束。

在呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)之後，RAS 用戶端應用程式不應假設連接作業已完成。 在結束之前，它應該等待上述其中一個條件。

 

 




