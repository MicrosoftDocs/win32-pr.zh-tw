---
description: 應用程式可以藉由呼叫 StrokePath 函式來繪製路徑的外框，它可以藉由呼叫 FillPath 函式來填滿路徑的內部，而且可以藉由呼叫 StrokeAndFillPath 函式來大綱和填滿路徑。
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: 輪廓和填滿路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660221eb1ef9d7ecf80d1d48ae18c8b234e76e5af3b30dba3323ee6feac3bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831598"
---
# <a name="outlined-and-filled-paths"></a>輪廓和填滿路徑

應用程式可以藉由呼叫 [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) 函式來繪製路徑的外框，它可以藉由呼叫 [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) 函式來填滿路徑的內部，而且可以藉由呼叫 [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) 函式來大綱和填滿路徑。

每當應用程式填滿路徑時，系統就會使用 DC 目前的填滿模式。 應用程式可以藉由呼叫 [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) 函式來取得此模式，而且可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函數來設定新的填滿模式。 如需這兩種填滿模式的說明，請參閱 [區域](regions.md)。

下圖顯示電腦輔助設計 (CAD) 應用程式所建立之物件的交叉區段，其使用已加上輪廓和填滿的路徑。

![圖例顯示物件的交叉截面視圖，並以不同的填滿模式指出不同的部分](images/cspth-01.png)

 

 



