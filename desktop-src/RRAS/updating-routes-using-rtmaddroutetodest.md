---
title: 使用 RtmAddRouteToDest 更新路由
description: 如果用戶端在新增路由時不需要效率，則應該使用下列方法來更新路由。
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025328"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>使用 RtmAddRouteToDest 更新路由

如果用戶端在新增路由時不需要效率，則應該使用下列方法來更新路由。 這種方法的效率較低，因為它需要取得路由的控制碼，並將 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構傳遞到路由表管理員。 此方法也需要更多時間。 由於 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 並不會直接操作路由表，因此使用此方法會以簡單的方式來交易效率。

如需示範如何使用這些函數的範例程式碼，請參閱 [使用 RtmAddRouteToDest 新增和更新路由](add-and-update-routes-using-rtmaddroutetodest.md)。

 

 




