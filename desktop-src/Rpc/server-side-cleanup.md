---
title: 伺服器端清除
description: " (RPC) 的伺服器端清除和遠端程序呼叫。"
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021707"
---
# <a name="server-side-cleanup"></a>伺服器端清除

想像下列案例：

用戶端會開啟內容控制碼，然後停止或中斷與伺服器的連線。 伺服器如何偵測到用戶端已失敗，而內容控制碼應該會向下執行？ 有兩個個子案例：一個是用戶端以有條理的方式關閉。 在這種情況下，它會通知伺服器它正在關機，而伺服器可以清除，包括執行內容執行。 如果用戶端未以順序關機或無法通知伺服器，則伺服器會使用保持連接狀態，以判斷用戶端是否仍然可用。 在伺服器端， [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) 函數沒有任何作用。 相反地，伺服器會使用每台電腦的全域-保持運作設定，預設為大約兩小時。 如果用戶端沒有回應伺服器的持續連線，連接就會關閉。 當指定之用戶端進程的所有連接都已關閉時，伺服器會清除並執行未完成的內容控制碼。

 

 




