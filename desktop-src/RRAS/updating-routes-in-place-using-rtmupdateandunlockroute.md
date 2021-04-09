---
title: 使用 RtmUpdateAndUnlockRoute 就地更新路由
description: 就地更新通常比以間接方法（例如，RtmAddRouteToDest 函式所使用的）更新路由表更有效率。
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021607"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>使用 RtmUpdateAndUnlockRoute 就地更新路由

就地更新通常比以間接方法（例如， [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 函式所使用的）更新路由表更有效率。 這個方法更有效率，因為用戶端不需要取得控制碼，也不需要在路由表管理員之間傳遞 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構。 這個方法也會花費較少的時間。 不過，直接更新路由表可能會有風險，因為路由表管理員並不是以媒介的形式運作。

如需示範如何使用這些函數的範例程式碼，請參閱 [使用 RtmUpdateAndUnlockRoute 就地更新路由](update-a-route-in-place-using-rtmupdateandunlockroute.md)。

 

 




