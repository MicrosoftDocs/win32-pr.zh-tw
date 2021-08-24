---
title: Edge UI 會在「內建」和「慣性」案例中隱藏
description: Edge UI 會在「內建」和「慣性」案例中隱藏
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec032fa97f54fc1b1325055c9b02bdebe9e817b0f85971c2e2a7062e93c284c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593958"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>Edge UI 會在「內建」和「慣性」案例中隱藏

## <a name="platform"></a>平台

<dl> 用戶端-Windows 8。1  
</dl>

## <a name="description"></a>描述

在某些情況下，使用者可能會意外地叫用 Edge UI， (常用鍵、應用程式行、應用程式切換) 。 我們推出了一項功能，可讓開發人員為整個螢幕設計 UI，而不需要進行 affordances (例如，框線) 來防止使用者意外碰到邊緣。

有兩種情況可能會導致最常導致意外的邊緣撥動：

-   在快速移動中，互動的速度和不精確有時可能會讓它們從畫面邊緣進入
-   如果使用者在手寫時快速離開並重新進入螢幕區域（例如，在繪圖應用程式中），則這項傳入行為可能會錯誤地觸發 Edge UI 並中斷使用者體驗

為了改進使用者和開發人員體驗，現在會在兩個特定的實例中隱藏 Edge UI：

-   當使用者在應用程式中移動時，在支援 DManip 慣性和撥動的情況下，當慣性發生時，將不會在 timeout 視窗內叫用 Edge UI
-   在經過認證的裝置上，當使用者從螢幕中快速撥動到畫面之外，並在特定參數內 (的內部) 移動時，將不會叫用 Edge UI

## <a name="manifestations"></a>表現

當使用應用程式時，使用者快速地對邊緣進行輕量，將會看到意外的邊緣調用。

## <a name="solution"></a>解決方案

開發人員應牢記這些緩和措施，而且應該能夠使用全螢幕，而不需要擔心使用者在邊緣與應用程式互動時，不會不慎觸發 Edge UI。

 

 




