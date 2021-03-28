---
description: 這兩個應用程式定義的對應模式 (MM \_ ISOTROPIC 和 mm \_ 各向異性) 是針對應用程式特定的對應模式所提供。
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Application-Defined 對應模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991291"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="41c7d-103">Application-Defined 對應模式</span><span class="sxs-lookup"><span data-stu-id="41c7d-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="41c7d-104">這兩個應用程式定義的對應模式 (MM \_ ISOTROPIC 和 mm \_ 各向異性) 是針對應用程式特定的對應模式所提供。</span><span class="sxs-lookup"><span data-stu-id="41c7d-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="41c7d-105">MM \_ ISOTROPIC 模式可保證 x 方向和 y 方向中的邏輯單元相等，而 mm 非等 \_ 向模式則可讓單位不同。</span><span class="sxs-lookup"><span data-stu-id="41c7d-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="41c7d-106">CAD 或繪圖應用程式可受益于 MM \_ ISOTROPIC 對應模式，但可能需要指定邏輯單元，以對應至工程師的規模遞增 (1/64 英寸) 。</span><span class="sxs-lookup"><span data-stu-id="41c7d-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="41c7d-107">使用預先定義的對應模式 (MM \_ HIENGLISH 或 mm HIMETRIC) ，就很難取得這些單位 \_ ; 不過，您可以藉由選取 mm \_ ISOTROPIC (或 mm 非 \_) 模式來輕鬆取得這些單位。</span><span class="sxs-lookup"><span data-stu-id="41c7d-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="41c7d-108">下列範例顯示如何將邏輯單元設定為1/64 英寸：</span><span class="sxs-lookup"><span data-stu-id="41c7d-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



