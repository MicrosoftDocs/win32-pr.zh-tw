---
description: 矩形是一側四邊的多邊形，其相反的邊是平行且相等的長度。
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: 繪製矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848557"
---
# <a name="drawing-rectangles"></a>繪製矩形

矩形是一側四邊的多邊形，其相反的邊是平行且相等的長度。 雖然應用程式可以藉由呼叫 [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) 函式來繪製矩形，以提供每個角落的座標，但 [**矩形**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) 函式提供較簡單的方法。 此函式只需要左上角和右下角的座標。 當應用程式呼叫 [**矩形**](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式時，如果未針對指定的裝置內容設定任何世界轉換，系統就會繪製矩形，但不包含右邊和右下角。

如果使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 或 [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) 函式來設定世界轉換，系統就會包含右邊和下邊緣。

除了繪製傳統矩形之外，您還可以繪製具有圓角的矩形。 [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)函式要求應用程式提供左上角和右上角的座標，以及用來圓角的橢圓形寬度和高度。

應用程式可以使用下列函數來操作矩形。



| 函式                         | 描述                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | 重新繪製矩形的內部。                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | 重新繪製矩形的側邊。                                  |
| [**InvertRect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | 反轉出現在矩形內部的色彩。 |



 

 

 
