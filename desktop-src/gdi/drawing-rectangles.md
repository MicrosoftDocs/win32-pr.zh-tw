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
# <a name="drawing-rectangles"></a><span data-ttu-id="0051f-103">繪製矩形</span><span class="sxs-lookup"><span data-stu-id="0051f-103">Drawing Rectangles</span></span>

<span data-ttu-id="0051f-104">矩形是一側四邊的多邊形，其相反的邊是平行且相等的長度。</span><span class="sxs-lookup"><span data-stu-id="0051f-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="0051f-105">雖然應用程式可以藉由呼叫 [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) 函式來繪製矩形，以提供每個角落的座標，但 [**矩形**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) 函式提供較簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="0051f-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="0051f-106">此函式只需要左上角和右下角的座標。</span><span class="sxs-lookup"><span data-stu-id="0051f-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="0051f-107">當應用程式呼叫 [**矩形**](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式時，如果未針對指定的裝置內容設定任何世界轉換，系統就會繪製矩形，但不包含右邊和右下角。</span><span class="sxs-lookup"><span data-stu-id="0051f-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="0051f-108">如果使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 或 [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) 函式來設定世界轉換，系統就會包含右邊和下邊緣。</span><span class="sxs-lookup"><span data-stu-id="0051f-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="0051f-109">除了繪製傳統矩形之外，您還可以繪製具有圓角的矩形。</span><span class="sxs-lookup"><span data-stu-id="0051f-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="0051f-110">[**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)函式要求應用程式提供左上角和右上角的座標，以及用來圓角的橢圓形寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="0051f-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="0051f-111">應用程式可以使用下列函數來操作矩形。</span><span class="sxs-lookup"><span data-stu-id="0051f-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="0051f-112">函式</span><span class="sxs-lookup"><span data-stu-id="0051f-112">Function</span></span>                         | <span data-ttu-id="0051f-113">描述</span><span class="sxs-lookup"><span data-stu-id="0051f-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0051f-114">**FillRect**</span><span class="sxs-lookup"><span data-stu-id="0051f-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="0051f-115">重新繪製矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="0051f-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="0051f-116">**FrameRect**</span><span class="sxs-lookup"><span data-stu-id="0051f-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="0051f-117">重新繪製矩形的側邊。</span><span class="sxs-lookup"><span data-stu-id="0051f-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="0051f-118">**InvertRect**</span><span class="sxs-lookup"><span data-stu-id="0051f-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="0051f-119">反轉出現在矩形內部的色彩。</span><span class="sxs-lookup"><span data-stu-id="0051f-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 
