---
description: 將 VMR 同步處理至監視器的更新速率
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: 將 VMR 同步處理至監視器的更新速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194954"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>將 VMR 同步處理至監視器的更新速率

在罕見的情況下，您可能會想要以監視器的重新整理頻率來精確同步處理影片轉譯，如此一來，每次監視器重新整理時，就只會顯示一個新的畫面格。 執行這項作業的最可靠方式是建立自訂配置器提供者，以使用翻轉作業（而非 array.blit 作業）將影片位寫入主要介面。 每次監視器重新整理時，都會呼叫 "Flip"，因此，如果您的影片資料流程未包含時間戳記，則 VMR 會盡可能快速轉譯為主要介面，但介面會封鎖串流，直到翻轉作業完成為止。 這表示，只要 CPU 沒有超載，下一個畫面會在每次監視器重新整理時，一律在主要介面上等候。 但是，如果有其他需要大量 CPU 的進程正在執行，它可能會使您的 DirectShow 串流執行緒，讓它無法將影片畫面的速度夠快到主要表面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VMR Renderless 播放模式 (自訂配置器-展示者) ](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



