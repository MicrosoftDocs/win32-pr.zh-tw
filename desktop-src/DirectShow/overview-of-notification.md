---
description: 事件通知總覽
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: 事件通知總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148531"
---
# <a name="overview-of-event-notification"></a>事件通知總覽

篩選準則會透過張貼事件通知，將事件通知 Graph 管理員。 事件可能是預期的內容，例如資料流程的結尾，或可能代表錯誤，例如轉譯資料流程失敗。 篩選 Graph 管理員本身會處理一些篩選事件，並讓應用程式的其他事件得以處理。 如果篩選 Graph 管理員沒有處理篩選事件，它就會將事件通知放入佇列中。 篩選圖形也可以將應用程式的事件通知排在佇列中。

應用程式會從佇列抓取事件，並根據事件種類來回應事件。 因此 DirectShow 中的事件通知，類似于 Microsoft Windows 訊息佇列配置。 應用程式也可以取消篩選 Graph 管理員的預設行為指定的事件種類。 篩選 Graph 管理員接著會將這些事件直接放入佇列中，以便讓應用程式處理。

這種機制可讓

-   篩選 Graph 管理員，以與應用程式進行通訊。
-   篩選準則，可與應用程式和篩選 Graph 管理員進行通訊。
-   判斷其對處理事件之介入程度的應用程式。

 

 



