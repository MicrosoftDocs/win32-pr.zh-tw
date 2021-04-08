---
title: 標示 Hold-Down 狀態的路由
description: 某些用戶端（例如 RIP 和 DVMRP 等距離向量通訊協定）要求在刪除目的地的最後一個路由之後，將目的地公告為無法連線。
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932307"
---
# <a name="marking-routes-for-the-hold-down-state"></a>標示 Hold-Down 狀態的路由

某些用戶端（例如 RIP 和 DVMRP 等距離向量通訊協定）要求在刪除目的地的最後一個路由之後，將目的地公告為無法連線。 最後一個刪除的路由必須公告為無法存取，即使較新的路由同時抵達也是一樣。 最後一個刪除的路由會標示為處於 *按住狀態*。 按住進程可防止路由迴圈的構成。 路由通訊協定通告過時的路由資訊時，會導致路由迴圈。 當保留期限到期時，這些通訊協定會以新的最佳路由繼續其廣告。

採用 [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) 函式的通訊協定，會指出目的地處于「按住」狀態。 當用戶端通告此目的地的最佳路由時，會呼叫此函式。 如果稍後刪除此目的地的所有路由，則會在先前呼叫 **RtmHoldDestination** 所指定的時間期間，將刪除的最後一個路由保留在按住狀態。

當通訊協定通告目的地時，所使用的路由資訊取決於通訊協定是否使用「保留」狀態，以及目的地是否存在「保留中斷」狀態的路由。

未使用「保留」狀態的通訊協定可以忽略與目的地保持狀態相關的路由資訊，並且一律通告最佳路由。

如需顯示如何使用這些函式的範例程式碼，請參閱 [使用路由 Hold-Down 狀態](use-the-route-hold-down-state.md)。

 

 




