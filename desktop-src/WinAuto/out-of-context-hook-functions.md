---
title: 內容外攔截函式
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 深入瞭解：內容外攔截函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e41e9a6bba1f705c3c5dc8781b2663be22086955f5dee45f07022504d0ccbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133741"
---
# <a name="out-of-context-hook-functions"></a>內容外攔截函式

下列清單概述跨內容攔截函式的主要層面：

-   跨內容攔截函式位於用戶端的位址空間中，不論它是在程式碼主體或 DLL 中。
-   非內容攔截函式不會對應到伺服器的位址空間。
-   觸發事件時，攔截函式的參數會跨進程界限封送處理。
-   由於封送處理的緣故，內容外攔截函式明顯比內容攔截函式慢。
-   系統會將事件通知排入佇列，以便 (因為執行封送處理) 所需的時間而以非同步方式抵達。

雖然事件通知是非同步，但 Microsoft Active Accessibility 可確保回呼函數會依照產生的順序來接收所有事件。

作業系統的使用者元件會為由內容外攔截函式所處理的事件配置記憶體。 當攔截函式傳回時，便會釋放記憶體。 如果攔截函式無法快速處理事件，則會降低使用者資源，最終會導致錯誤或回應時間太慢。 這些問題可能會發生在下列情況：

-   事件的引發速度非常快。
-   系統很慢。
-   攔截函式處理事件的速度很慢。
-   用戶端正在 Windows 9x 上執行。

 

 




