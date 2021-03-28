---
description: 除了繪製線條或曲線，應用程式可以藉由呼叫單一函式來繪製線條和曲線輸出的組合。 例如，應用程式可以藉由呼叫 AngleArc 函數來繪製圓形圖的外框。
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: 結合線條和曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972740"
---
# <a name="combined-lines-and-curves"></a>結合線條和曲線

除了繪製線條或曲線，應用程式可以藉由呼叫單一函式來繪製線條和曲線輸出的組合。 例如，應用程式可以藉由呼叫 [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) 函數來繪製圓形圖的外框。

[**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)函式會沿著圓形的周邊繪製弧線，並繪製將弧線起點連接至圓形中心的線條。 除了使用 **AngleArc** 函式之外，應用程式也可以使用 [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) 函數，結合線條和不規則曲線輸出。

 

 



