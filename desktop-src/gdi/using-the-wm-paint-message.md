---
description: 您可以使用 WM \_ 油漆訊息來執行顯示資訊所需的繪圖。
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: 使用 WM_PAINT 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037446"
---
# <a name="using-the-wm_paint-message"></a>使用 WM \_ 油漆訊息

您可以使用 [**WM \_ 油漆**](wm-paint.md) 訊息來執行顯示資訊所需的繪圖。 因為 \_ 當您的視窗必須更新或您明確要求更新時，系統會將 WM 繪製訊息傳送至您的應用程式，因此您可以合併程式碼，以在應用程式的視窗程式中進行繪製。 只要您的應用程式必須繪製新的或現有的資訊，您就可以使用此程式碼。

下列各節顯示使用 WM \_ 油漆訊息在視窗中繪製的各種方式：

-   [在工作區中繪圖](drawing-in-the-client-area.md)
-   [重繪整個工作區](redrawing-the-entire-client-area.md)
-   [更新區域中的重繪](redrawing-in-the-update-region.md)
-   [使工作區失效](invalidating-the-client-area.md)
-   [繪製最小化視窗](drawing-a-minimized-window.md)
-   [繪製自訂視窗背景](drawing-a-custom-window-background.md)

 

 



