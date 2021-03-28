---
description: 橢圓形是由兩個固定點（ (f1 和 f2）所定義的封閉曲線，) 讓距離 (d1 + d2 ) 從曲線上任何點到兩個固定點的總和是常數。
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: 關於橢圓形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565674"
---
# <a name="about-ellipses"></a><span data-ttu-id="803d7-103">關於橢圓形</span><span class="sxs-lookup"><span data-stu-id="803d7-103">About Ellipses</span></span>

<span data-ttu-id="803d7-104">橢圓形是由兩個固定點（ (f1 和 f2）所定義的封閉曲線，) 讓距離 (d1 + d2 ) 從曲線上任何點到兩個固定點的總和是常數。</span><span class="sxs-lookup"><span data-stu-id="803d7-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="803d7-105">下圖顯示使用 [**橢圓形**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) 函數繪製的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="803d7-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![顯示橢圓形、兩個固定點、兩個距離和周框矩形的圖例](images/csfsh-01.png)

<span data-ttu-id="803d7-107">呼叫 [**橢圓形**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)時，應用程式會提供橢圓周框矩形左上角和右下角的座標。</span><span class="sxs-lookup"><span data-stu-id="803d7-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="803d7-108">周 *框* 是完全圍繞橢圓形的最小矩形。</span><span class="sxs-lookup"><span data-stu-id="803d7-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="803d7-109">當系統繪製橢圓形時，如果未設定任何世界轉換，則會排除右邊和右下方。</span><span class="sxs-lookup"><span data-stu-id="803d7-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="803d7-110">因此，針對任何測量 x 單位寬度 x y 單位偏高的矩形，相關聯的橢圓形會依 y1 單位來測量 x1 單位寬。</span><span class="sxs-lookup"><span data-stu-id="803d7-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="803d7-111">如果應用程式藉由呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 或 [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) 函式來設定世界轉換，系統就會包含右邊和右下方。</span><span class="sxs-lookup"><span data-stu-id="803d7-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



