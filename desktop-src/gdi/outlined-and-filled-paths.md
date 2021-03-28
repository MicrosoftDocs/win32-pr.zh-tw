---
description: 應用程式可以藉由呼叫 StrokePath 函式來繪製路徑的外框，它可以藉由呼叫 FillPath 函式來填滿路徑的內部，而且可以藉由呼叫 StrokeAndFillPath 函式來大綱和填滿路徑。
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: 輪廓和填滿路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943802"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="0a1e1-103">輪廓和填滿路徑</span><span class="sxs-lookup"><span data-stu-id="0a1e1-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="0a1e1-104">應用程式可以藉由呼叫 [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) 函式來繪製路徑的外框，它可以藉由呼叫 [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) 函式來填滿路徑的內部，而且可以藉由呼叫 [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) 函式來大綱和填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="0a1e1-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="0a1e1-105">每當應用程式填滿路徑時，系統就會使用 DC 目前的填滿模式。</span><span class="sxs-lookup"><span data-stu-id="0a1e1-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="0a1e1-106">應用程式可以藉由呼叫 [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) 函式來取得此模式，而且可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函數來設定新的填滿模式。</span><span class="sxs-lookup"><span data-stu-id="0a1e1-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="0a1e1-107">如需這兩種填滿模式的說明，請參閱 [區域](regions.md)。</span><span class="sxs-lookup"><span data-stu-id="0a1e1-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="0a1e1-108">下圖顯示電腦輔助設計 (CAD) 應用程式所建立之物件的交叉區段，其使用已加上輪廓和填滿的路徑。</span><span class="sxs-lookup"><span data-stu-id="0a1e1-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![圖例顯示物件的交叉截面視圖，並以不同的填滿模式指出不同的部分](images/cspth-01.png)

 

 



