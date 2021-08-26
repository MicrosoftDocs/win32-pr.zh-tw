---
title: 正在捕獲變更狀態並忽略變更
description: 用戶端可以藉由呼叫 RtmGetChangeStatus 來查詢路由表管理員，以找出目的地變更的通知是否暫止。 此函式會傳回 TRUE，直到呼叫端透過呼叫 RtmGetChangedDests 來抓取此變更為止。
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028058"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>正在捕獲變更狀態並忽略變更

用戶端可以藉由呼叫 [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)來查詢路由表管理員，以找出目的地變更的通知是否暫止。 此函式會傳回 **TRUE** ，直到呼叫端透過呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)來抓取此變更為止。

用戶端可以使用此查詢來避免執行在接收和處理變更通知之後必須復原的動作。 使用這項功能可讓用戶端將某些作業延後到較晚的時間，以有效率地工作。

用戶端也可以呼叫 [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)，以忽略目的地的暫止變更通知。 除非在呼叫 [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)之後發生其他變更，否則 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)的後續呼叫不會傳回此目的地。

 

 




