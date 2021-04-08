---
description: 事件通知總覽
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: 事件通知總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687960"
---
# <a name="overview-of-event-notification"></a>事件通知總覽

篩選會透過張貼事件通知，通知篩選圖形管理員有關事件的資訊。 事件可能是預期的內容，例如資料流程的結尾，或可能代表錯誤，例如轉譯資料流程失敗。 篩選圖形管理員本身會處理一些篩選事件，並讓應用程式的其他事件保持處理。 如果篩選圖形管理員沒有處理篩選事件，它會將事件通知放入佇列中。 篩選圖形也可以將應用程式的事件通知排在佇列中。

應用程式會從佇列抓取事件，並根據事件種類來回應事件。 因此，DirectShow 中的事件通知與 Microsoft Windows 訊息佇列配置類似。 應用程式也可以針對指定的事件種類，取消篩選圖形管理員的預設行為。 篩選圖形管理員接著會將這些事件直接放入佇列中，以便讓應用程式處理。

這種機制可讓

-   用來與應用程式通訊的篩選圖形管理員。
-   篩選器可與應用程式和篩選器圖形管理員進行通訊。
-   判斷其對處理事件之介入程度的應用程式。

 

 



