---
description: 視窗的座標系統是以顯示裝置的座標系統為基礎。
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: 視窗座標系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692592"
---
# <a name="window-coordinate-system"></a><span data-ttu-id="c0607-103">視窗座標系統</span><span class="sxs-lookup"><span data-stu-id="c0607-103">Window Coordinate System</span></span>

<span data-ttu-id="c0607-104">視窗的座標系統是以顯示裝置的座標系統為基礎。</span><span class="sxs-lookup"><span data-stu-id="c0607-104">The coordinate system for a window is based on the coordinate system of the display device.</span></span> <span data-ttu-id="c0607-105">基本測量單位是裝置單位 (通常是圖元) 。</span><span class="sxs-lookup"><span data-stu-id="c0607-105">The basic unit of measure is the device unit (typically, the pixel).</span></span> <span data-ttu-id="c0607-106">畫面上的點會以 x 和 y 座標配對來描述。</span><span class="sxs-lookup"><span data-stu-id="c0607-106">Points on the screen are described by x- and y-coordinate pairs.</span></span> <span data-ttu-id="c0607-107">X 座標會增加到右邊;y 座標從上到下增加。</span><span class="sxs-lookup"><span data-stu-id="c0607-107">The x-coordinates increase to the right; y-coordinates increase from top to bottom.</span></span> <span data-ttu-id="c0607-108">系統的源 (0、0) 取決於所使用的座標類型。</span><span class="sxs-lookup"><span data-stu-id="c0607-108">The origin (0,0) for the system depends on the type of coordinates being used.</span></span>

<span data-ttu-id="c0607-109">系統和應用程式會在螢幕上以 *螢幕座標* 指定視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="c0607-109">The system and applications specify the position of a window on the screen in *screen coordinates*.</span></span> <span data-ttu-id="c0607-110">若為螢幕座標，則原點是畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="c0607-110">For screen coordinates, the origin is the upper-left corner of the screen.</span></span> <span data-ttu-id="c0607-111">視窗的完整位置通常是由 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構描述，其中包含定義視窗左上角和右下角的兩個點的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="c0607-111">The full position of a window is often described by a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the screen coordinates of two points that define the upper-left and lower-right corners of the window.</span></span>

<span data-ttu-id="c0607-112">系統和應用程式會使用 *用戶端座標* 來指定時間點在視窗中的位置。</span><span class="sxs-lookup"><span data-stu-id="c0607-112">The system and applications specify the position of points in a window by using *client coordinates*.</span></span> <span data-ttu-id="c0607-113">在此案例中，原點是視窗或工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="c0607-113">The origin in this case is the upper-left corner of the window or client area.</span></span> <span data-ttu-id="c0607-114">無論視窗在螢幕上的位置為何，用戶端座標都能確保應用程式在視窗中繪製時，可以使用一致的座標值。</span><span class="sxs-lookup"><span data-stu-id="c0607-114">Client coordinates ensure that an application can use consistent coordinate values while drawing in the window, regardless of the position of the window on the screen.</span></span>

<span data-ttu-id="c0607-115">工作區的維度也會由包含區域之用戶端座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構描述。</span><span class="sxs-lookup"><span data-stu-id="c0607-115">The dimensions of the client area are also described by a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains client coordinates for the area.</span></span> <span data-ttu-id="c0607-116">在所有情況下，矩形的左上座標都會包含在視窗或工作區中，而右下角座標則會被排除。</span><span class="sxs-lookup"><span data-stu-id="c0607-116">In all cases, the upper-left coordinate of the rectangle is included in the window or client area, while the lower-right coordinate is excluded.</span></span> <span data-ttu-id="c0607-117">視窗或工作區中的圖形作業會從封閉矩形的右和下邊緣中排除。</span><span class="sxs-lookup"><span data-stu-id="c0607-117">Graphics operations in a window or client area are excluded from the right and lower edges of the enclosing rectangle.</span></span>

<span data-ttu-id="c0607-118">有時候，應用程式可能需要將一個視窗中的座標組應到另一個視窗中的座標。</span><span class="sxs-lookup"><span data-stu-id="c0607-118">Occasionally, applications may be required to map coordinates in one window to those of another window.</span></span> <span data-ttu-id="c0607-119">應用程式可以使用 [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) 函數來對應座標。</span><span class="sxs-lookup"><span data-stu-id="c0607-119">An application can map coordinates by using the [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) function.</span></span> <span data-ttu-id="c0607-120">如果其中一個視窗是桌面視窗，此函式會有效地將螢幕座標轉換成用戶端座標，反之亦然。桌面視窗一律會以螢幕座標指定。</span><span class="sxs-lookup"><span data-stu-id="c0607-120">If one of the windows is the desktop window, the function effectively converts screen coordinates to client coordinates and vice versa; the desktop window is always specified in screen coordinates.</span></span>

 

 
