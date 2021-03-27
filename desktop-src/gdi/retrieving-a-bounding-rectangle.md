---
description: 應用程式會藉由呼叫 GetRgnBox 函數來抓取區域周框的維度。
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: 正在抓取周框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691831"
---
# <a name="retrieving-a-bounding-rectangle"></a>正在抓取周框

應用程式會藉由呼叫 [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) 函數來抓取區域周框的維度。 如果區域是矩形， **GetRgnBox** 會傳回區域的維度。 如果區域是橢圓形，則函式會傳回可在橢圓形周圍繪製之最小矩形的維度。 矩形的長邊與橢圓形的主要軸具有相同的長度，而矩形的最短邊與橢圓形的次要軸具有相同的長度。 如果區域是多邊形， **GetRgnBox** 會傳回可在整個多邊形周圍繪製之最小矩形的維度。

 

 



