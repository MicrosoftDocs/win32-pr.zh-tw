---
description: 如果通訊端處於非封鎖模式中，則任何 i/o 作業都必須立即完成，或傳回錯誤碼 WSAEWOULDBLOCK，表示作業無法立即完成。
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: 非封鎖的輸入/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5885e8a9b4c8badb2cd2c8e77b85d6fe097ed9a56be7b6146b586de81bbe6a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384478"
---
# <a name="nonblocking-inputoutput"></a>非封鎖的輸入/輸出

如果通訊端處於非封鎖模式中，則任何 i/o 作業都必須立即完成，或傳回錯誤碼 WSAEWOULDBLOCK，表示作業無法立即完成。 在後者的情況下，需要一種機制來探索何時適合在預期作業成功的情況下，再次嘗試操作。 已針對此用途定義了一組網路事件。 您可以使用 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))來輪詢或等候這些事件，或是藉由呼叫 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 或 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))來註冊非同步傳遞。 如需詳細資訊，請參閱 [網路事件通知](notification-of-network-events-2.md) 。

 

 
