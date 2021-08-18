---
title: 接收變更的通知
description: 許多用戶端可以同時更新路由表，而且用戶端必須在路由資訊發生變更時收到通知。
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788708"
---
# <a name="receiving-notification-of-changes"></a>接收變更的通知

許多用戶端可以同時更新路由表，而且用戶端必須在路由資訊發生變更時收到通知。 例如，未收到其他用戶端對路由表之變更通知的用戶端，可能會公告過期的路由資訊。 藉由程式設計用戶端註冊路由表管理員來註冊路由表中的變更，就可以防止這種情況。 路由表管理員會將變更的通知傳送給所有註冊用來接收這些用戶端的用戶端。

變更通知只適用于目的地。 沒有任何方法可以查詢路由表管理員是否有特定路由的變更。

對目的地的其中一個路由進行變更時，路由表管理員會送出已發生變更的通知。 這項通知只會傳送到已向路由表管理員註冊的用戶端，以瞭解所發生的變更類型。 路由表管理員中路由資訊的所有變更都會出現在一或多個視圖中，而且可以在任何支援的視圖子集中要求變更通知訊息。

目前有三種類型的變更通知可供用戶端註冊：

-   對目的地的路由進行任何變更的通知。 此要求是使用 RTM 「 \_ 變更 \_ 類型全部」旗標進行 \_ 。
-   如果目的地的最佳路由變更，或目前最佳路由變更的下列任何資訊，則會發出通知：

    -   喜好設定
    -   下一個躍點
    -   路由旗標

    此要求是使用 RTM \_ 變更類型的 \_ \_ 最佳旗標進行。

-   類型 RTM 變更類型的所有變更的 \_ 通知 \_ \_ ，最適合最大路由中非轉送旗標的變更。 例如，路由器管理員會在單點傳送視圖中等待此類型的變更，並更新單播轉寄站中的資訊。 此要求是使用 RTM \_ 變更 \_ 類型 \_ 轉送旗標進行。

變更通知的要求也可以藉由將變更通知註冊為「標示」的目的地，限制為目的地的子集。 用戶端可以藉由呼叫 [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)來標示變更通知的目的地。

發生變更時，路由表管理員會檢查是否有任何用戶端必須收到這項變更的通知。 如果符合下列所有條件，用戶端必須收到變更通知：

-   發生的變更類型是用戶端已註冊通知的類型
-   如果用戶端已要求所有目的地的變更，則會變更用戶端已標示的目的地，或任何目的地
-   用戶端已要求發生此變更之視圖的變更通知

如果變更符合上述所有條件，則會快取此變更，並通知用戶端。

通知不會指定實際變更的內容，只會指出已發生的變更。 用戶端必須使用從先前呼叫 [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)取得的通知控制碼來呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) ，以取出變更。

 

 




