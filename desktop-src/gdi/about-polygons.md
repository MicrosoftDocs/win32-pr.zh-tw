---
description: 多邊形是具有直邊的填滿形狀。
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: 關於多邊形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0d28bd915237991294f6579448ca08785481f374814f0ed5840f77ee9f813c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966438"
---
# <a name="about-polygons"></a>關於多邊形

*多邊形* 是具有直邊的填滿形狀。 多邊形的側邊使用目前的畫筆繪製。 當系統填滿多邊形時，它會使用目前的筆刷和目前的多邊形填滿模式。 這兩種填滿模式（替代 (預設) 和繞組）會決定是否要填滿或省略複雜多邊形內的區域。 應用程式可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函式來選取其中一個模式。 如需多邊形填滿模式的詳細資訊，請參閱 [區域](regions.md)。

下圖顯示使用 [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)繪製的多邊形。

![以五向星形為圖形的多邊形圖例](images/csfsh-04.png)

除了使用 [**多邊形**](/windows/win32/api/wingdi/nf-wingdi-polygon)繪製單一多邊形，應用程式可以使用 [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) 函數來繪製多個多邊形。

 

 
