---
title: 部署負載平衡
description: 部署負載平衡
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36d1ba29aedd5e94c29095d18fb84790ec4b76956ea20bc2ffd584b5a6a179f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021840"
---
# <a name="deploying-load-balancing"></a>部署負載平衡

典型的部署環境和使用案例是使用 RPC 負載平衡器，如下所示：![rpc 負載平衡](images/rpc-load-balancing.png)

1.  RPC 用戶端會對伺服器陣列進行 RPC/HTTP 連接。
2.  連線會透過網路轉送至前端負載平衡器
3.  前端負載平衡器會選擇要為要求提供服務的伺服器。 在此範例中，前端負載平衡器會將連接轉送到伺服器1。
4.  RPC 負載平衡器服務會仲裁連接。 它會判斷這是用戶端的第一個連接，並將連接與本機伺服器伺服器1產生關聯。
5.  用戶端會進行第二個 RPC/HTTP 要求。
6.  要求會透過網路轉送至前端負載平衡器。
7.  前端負載平衡器會選擇要為要求提供服務的伺服器。 在此情況下，前端負載平衡器會選擇 Server 2 來服務要求。
8.  RPC Load Balancer 服務會仲裁連接。 它會辨識出來自此用戶端的連線正在由伺服器1提供服務。
9.  連接會轉送至伺服器1。

 

 




