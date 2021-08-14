---
description: 應用程式會藉由呼叫 GetRgnBox 函數來抓取區域周框的維度。
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: 正在抓取周框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886142"
---
# <a name="retrieving-a-bounding-rectangle"></a>正在抓取周框

應用程式會藉由呼叫 [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) 函數來抓取區域周框的維度。 如果區域是矩形， **GetRgnBox** 會傳回區域的維度。 如果區域是橢圓形，則函式會傳回可在橢圓形周圍繪製之最小矩形的維度。 矩形的長邊與橢圓形的主要軸具有相同的長度，而矩形的最短邊與橢圓形的次要軸具有相同的長度。 如果區域是多邊形， **GetRgnBox** 會傳回可在整個多邊形周圍繪製之最小矩形的維度。

 

 



