---
description: 幾乎所有的應用程式都會使用畫面來顯示他們所操作的資料。
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: 關於繪製和繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991154"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="b3b78-103">關於繪製和繪製</span><span class="sxs-lookup"><span data-stu-id="b3b78-103">About Painting and Drawing</span></span>

<span data-ttu-id="b3b78-104">幾乎所有的應用程式都會使用畫面來顯示他們所操作的資料。</span><span class="sxs-lookup"><span data-stu-id="b3b78-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="b3b78-105">應用程式會繪製影像、繪製圖形以及寫入文字，讓使用者可以在建立、編輯和列印資料時加以查看。</span><span class="sxs-lookup"><span data-stu-id="b3b78-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="b3b78-106">Microsoft Windows 提供繪圖和繪圖的豐富支援，但由於多工作業系統的本質，因此應用程式必須在存取畫面時互相合作。</span><span class="sxs-lookup"><span data-stu-id="b3b78-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="b3b78-107">為了讓所有應用程式都能順暢且合作地運作，系統會管理螢幕的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="b3b78-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="b3b78-108">應用程式會使用 windows 作為其主要輸出裝置，而不是螢幕本身。</span><span class="sxs-lookup"><span data-stu-id="b3b78-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="b3b78-109">系統會提供可唯一對應至 windows 的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="b3b78-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="b3b78-110">應用程式會使用顯示裝置內容，將其輸出導向至指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="b3b78-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="b3b78-111">在視窗中繪製 (將輸出導向至該應用程式，) 可防止應用程式干擾其他應用程式的輸出，並允許應用程式互相並存，同時仍能充分利用系統的圖形功能。</span><span class="sxs-lookup"><span data-stu-id="b3b78-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="b3b78-112">在視窗中繪製的時機</span><span class="sxs-lookup"><span data-stu-id="b3b78-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="b3b78-113">WM \_ 油漆訊息</span><span class="sxs-lookup"><span data-stu-id="b3b78-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="b3b78-114">不含 WM \_ 油漆訊息的繪圖</span><span class="sxs-lookup"><span data-stu-id="b3b78-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="b3b78-115">視窗座標系統</span><span class="sxs-lookup"><span data-stu-id="b3b78-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="b3b78-116">視窗區域</span><span class="sxs-lookup"><span data-stu-id="b3b78-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="b3b78-117">視窗背景</span><span class="sxs-lookup"><span data-stu-id="b3b78-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="b3b78-118">最小化視窗</span><span class="sxs-lookup"><span data-stu-id="b3b78-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="b3b78-119">調整視窗大小</span><span class="sxs-lookup"><span data-stu-id="b3b78-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="b3b78-120">非工作區</span><span class="sxs-lookup"><span data-stu-id="b3b78-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="b3b78-121">子視窗更新區域</span><span class="sxs-lookup"><span data-stu-id="b3b78-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="b3b78-122">顯示裝置</span><span class="sxs-lookup"><span data-stu-id="b3b78-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="b3b78-123">視窗更新鎖定</span><span class="sxs-lookup"><span data-stu-id="b3b78-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="b3b78-124">累積的周框</span><span class="sxs-lookup"><span data-stu-id="b3b78-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



