---
description: 更新區域會識別已過期或無效且需要重繪的視窗部分。
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: 更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717968"
---
# <a name="the-update-region"></a>更新區域

*更新區域* 會識別已過期或無效且需要重繪的視窗部分。 系統會使用更新區域來產生適用于應用程式的 [**WM \_ 油漆**](wm-paint.md) 訊息，並將應用程式的最新內容帶入最新的時間降到最低。 系統只會將不正確視窗部分新增至更新區域，因此只需要繪製該部分。

當系統判斷某個視窗需要更新時，會將更新區域的維度設定為視窗的無效部分。 設定更新區域不會立即讓應用程式進行繪製。 相反地，應用程式會繼續從應用程式訊息佇列中取出訊息，直到沒有訊息保留為止。 系統接著會檢查更新區域，如果區域不是空的 (非 Null) ，它就會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至視窗程式。

應用程式可以使用更新區域來產生其 [**WM \_ 繪製**](wm-paint.md) 訊息。 例如，從開啟的檔案載入資料的應用程式通常會在載入時設定更新區域，以便在處理下一個 **WM \_ 油漆** 訊息時繪製新的資料。 一般來說，應用程式不應該在其資料變更時繪製，而是透過 **WM \_ 油漆** 訊息來路由所有繪圖作業。

 

 



