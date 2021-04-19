---
description: 佇列元件錯誤
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: 佇列元件錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973393"
---
# <a name="queued-components-errors"></a>佇列元件錯誤

當已排入佇列的元件呼叫失敗時，可能是因為無法將它傳送到伺服器 (用戶端失敗) 或因為它在 (到達伺服器端失敗) 時無法執行，所以對應的 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 訊息稱為「有害訊息」（ *有害 Message*）。

COM + 佇列的元件服務會使用一連串的重試佇列來處理有害訊息。 經過數次重試之後，訊息會移至最後的靜止佇列。 訊息會留在靜止佇列中，直到使用佇列的元件訊息移動器公用程式手動移動為止。 如需使用訊息移動器的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。

在下表所述的主題中，可以找到各種錯誤發生之事件順序的詳細說明。



| 主題                                                                             | 描述                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [伺服器端錯誤](server-side-errors.md)<br/>                           | 詳細說明 COM + 佇列元件服務對伺服器端失敗的回應。<br/>             |
| [用戶端錯誤](client-side-errors.md)<br/>                           | 詳細說明 COM + 佇列元件服務對用戶端失敗的回應。<br/>             |
| [持續性 Client-Side 失敗](persistent-client-side-failures.md)<br/> | 詳細說明 COM + 佇列元件服務對重複用戶端失敗的回應。<br/> |



 

 

 




