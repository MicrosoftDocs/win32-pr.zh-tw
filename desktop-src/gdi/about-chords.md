---
description: 弦是一個區域，系結于橢圓形和稱為正向的線段的交集。 下圖顯示使用弦函數繪製的弦。
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: 關於 Chords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512464"
---
# <a name="about-chords"></a><span data-ttu-id="60cfc-104">關於 Chords</span><span class="sxs-lookup"><span data-stu-id="60cfc-104">About Chords</span></span>

<span data-ttu-id="60cfc-105">*弦* 是一個區域，系結于橢圓形和稱為 *正* 向的線段的交集。</span><span class="sxs-lookup"><span data-stu-id="60cfc-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="60cfc-106">下圖顯示使用 [**弦**](/windows/desktop/api/Wingdi/nf-wingdi-chord) 函數繪製的弦。</span><span class="sxs-lookup"><span data-stu-id="60cfc-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![elipse 的圖例，顯示兩個 radials、正向和絃](images/csfsh-02.png)

<span data-ttu-id="60cfc-108">呼叫 [**弦**](/windows/win32/api/wingdi/nf-wingdi-chord)時，應用程式會提供橢圓形周框的左上角和右下角的座標，以及兩個點的座標來定義兩個 radials。</span><span class="sxs-lookup"><span data-stu-id="60cfc-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="60cfc-109">放射狀線是從橢圓形周框的中心繪製到橢圓形上某個點的直線。</span><span class="sxs-lookup"><span data-stu-id="60cfc-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="60cfc-110">當系統繪製弦的弧形部分時，它會使用目前的弧形方向來指定裝置內容。</span><span class="sxs-lookup"><span data-stu-id="60cfc-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="60cfc-111">預設弧線方向是逆時針的。</span><span class="sxs-lookup"><span data-stu-id="60cfc-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="60cfc-112">您可以藉由呼叫 [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) 函式，讓您的應用程式重設弧線方向。</span><span class="sxs-lookup"><span data-stu-id="60cfc-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
