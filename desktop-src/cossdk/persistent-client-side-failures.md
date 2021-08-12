---
description: 持續性 Client-Side 失敗
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: 持續性 Client-Side 失敗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305771"
---
# <a name="persistent-client-side-failures"></a>持續性 Client-Side 失敗

在某些情況下， [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 可以將訊息移至目的地佇列。 例如，如果佇列存取控制不允許將訊息從用戶端移至伺服器，則會將違規的訊息移至用戶端無效信件佇列。 發生這種情況時，COM + 佇列的元件服務可讓例外狀況類別與元件相關聯。 若要將例外狀況類別與元件產生關聯，請在 [元件服務管理工具] 的 [元件屬性] 頁面中，使用 [ **Advanced** ] 索引標籤。 您也可以使用 COM + 系統管理函數的 ExceptionClass catalog component 屬性，以程式設計的方式建立例外狀況類別的關聯。

例外狀況類別定義為執行 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)之元件的 PROGID 或 CLSID。 排入佇列的元件服務具有可掃描交易無效信件佇列的無效信件佇列監視器。 如果佇列中有訊息，寄不出的信件佇列監視器會具現化與目標群組件相關聯的例外狀況處理常式，並呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)，表示有用戶端、無法復原的錯誤。

除了 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)之外，例外狀況處理常式也應該執行與處理例外狀況之伺服器元件相同的介面集。 呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) 時，已排入佇列的元件執行時間會將失敗的訊息播放回例外狀況處理常式。 這可讓例外狀況處理常式針對無法移至伺服器的訊息（例如，藉由產生補償交易）來執行替代行為。

如果例外狀況處理常式完成所有已播放的方法呼叫，則會從交易寄不出的信件佇列中移除訊息，並加以關閉。 但是，如果例外狀況處理常式藉由傳回其中一個方法呼叫的失敗狀態來中止訊息，則會將訊息傳回給交易無效信件佇列。 下列事件順序顯示用戶端例外狀況的處理方式：

1.  訊息佇列無法將訊息傳遞至伺服器，並將訊息放到交易的無效信件佇列。
2.  寄不出的信件佇列接聽程式 (DLQL) 在交易無效信件佇列中尋找訊息。
3.  DLQL 會從訊息中抓取目標群組件 CLSID，並檢查是否有例外狀況類別。
4.  DLQL 會具現化例外狀況類別。
5.  DLQL 會查詢例外狀況類別的 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) 。
6.  DLQL 會在例外狀況類別中呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) 方法。
7.  DLQL 會將訊息中的所有屬性和方法呼叫播放到例外狀況類別。
8.  如果例外狀況處理常式成功完成交易，則 DLQL 會刪除訊息。 例外狀況處理常式可能會發出 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)，且訊息會保留在寄不出的信件佇列中。

如果上述任何一個步驟失敗，訊息就會保留在交易無效信件佇列中。

啟動時，DLQL 會讀取訊息佇列交易式寄不出的信件佇列上的每個訊息，並為每個已佇列的元件訊息具現化例外狀況類別。 一旦通過佇列，它就會等待新的訊息。 然後，它會在每個新的寄不出的信件佇列訊息抵達時進行處理。

如果您需要介入此處所述的程式，或如果您需要將有害訊息移出其最終的靜止佇列，請使用訊息移動器公用程式。 如需訊息移動器公用程式的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端錯誤](client-side-errors.md)
</dt> <dt>

[伺服器端錯誤](server-side-errors.md)
</dt> </dl>

 

 



