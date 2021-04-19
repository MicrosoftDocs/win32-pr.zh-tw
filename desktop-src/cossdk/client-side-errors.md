---
description: Client-Side 錯誤
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970717"
---
# <a name="client-side-errors"></a>Client-Side 錯誤

用戶端的失敗會以類似伺服器端失敗的方式處理。 例如，如果訊息無法從用戶端移至伺服器，[訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))就可以將訊息移至其目的地佇列。 在此情況下，訊息會移至用戶端無效信件佇列。

COM + 佇列元件服務會監視無效信件佇列。 如果訊息已移動，佇列的元件服務會建立例外狀況類別的實例，並呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來要求 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)。 如果成功，無效信件佇列監視器會叫用 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)。

物件可以採取一些動作來反轉先前交易的效果。 如果播放認可，則會從交易無效信件佇列中移除訊息。 如果播放失敗或必要的 CLSID 和介面無法使用，則訊息會保留在交易無效信件佇列中。

如果您需要介入以上所述的程式，或如果您需要將有害訊息移出其最終的靜止佇列，請使用訊息移動器公用程式。 如需訊息移動器公用程式的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[持續性 Client-Side 失敗](persistent-client-side-failures.md)
</dt> <dt>

[伺服器端錯誤](server-side-errors.md)
</dt> </dl>

 

 
