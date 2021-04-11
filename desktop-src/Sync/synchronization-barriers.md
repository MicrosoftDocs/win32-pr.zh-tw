---
description: 同步處理屏障可讓多個執行緒等候，直到所有線程都已到達特定的執行點，然後再繼續任何執行緒。
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: 同步處理阻礙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194728"
---
# <a name="synchronization-barriers"></a>同步處理阻礙

同步處理屏障可讓多個執行緒等候，直到所有線程都已到達特定的執行點，然後再繼續任何執行緒。 無法跨進程共用同步處理阻礙。

同步處理屏障適用于階段式計算，其中平行執行相同程式碼的執行緒必須全都完成一個階段，然後才繼續進行下一個階段。

若要建立同步處理屏障，請呼叫 [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) 函式，並指定執行緒的最大數目，以及執行緒在封鎖之前應該旋轉多少次。 然後啟動將使用屏障的執行緒。 在每個執行緒完成其工作之後，它會呼叫 [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) 來等候關卡。 **EnterSynchronizationBarrier** 函式會封鎖每個執行緒，直到關卡中封鎖的執行緒數目達到屏障的執行緒計數上限為止，此時 **EnterSynchronizationBarrier** 會解除封鎖所有線程。 **EnterSynchronizationBarrier** 函式只會針對其中一個進入屏障的執行緒傳回 **TRUE** ，並針對所有其他執行緒傳回 **FALSE** 。

若要釋放不再需要的同步處理屏障，請呼叫 [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)。 呼叫 [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) 後立即呼叫此函式是安全的，因為該函式可確保所有線程在釋放之前都已完成使用屏障。

如果不會刪除同步處理屏障，執行緒可以在進入屏障時，指定 **同步處理 \_ 屏障 \_ 旗標 \_ 無 \_ 刪除旗標** 。 使用屏障的所有線程都必須指定此旗標;如果有任何執行緒沒有，則會忽略旗標。 此旗標會導致函式略過刪除安全所需的額外工作，這可改善效能。 請注意，在此旗標生效時刪除關卡可能會導致不正確控制碼存取，以及一或多個永久封鎖的執行緒。

 

 



