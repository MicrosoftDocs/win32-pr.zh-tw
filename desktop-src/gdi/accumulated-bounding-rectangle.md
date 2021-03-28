---
description: 累積的周框是最小的矩形，可封閉受最近繪圖作業影響的視窗或工作區部分。
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: 累積的周框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512928"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="b0e02-103">累積的周框</span><span class="sxs-lookup"><span data-stu-id="b0e02-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="b0e02-104">累積的周 *框* 是最小的矩形，可封閉受最近繪圖作業影響的視窗或工作區部分。</span><span class="sxs-lookup"><span data-stu-id="b0e02-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="b0e02-105">應用程式可以使用這個矩形，輕鬆地判斷繪圖作業所造成的變更範圍。</span><span class="sxs-lookup"><span data-stu-id="b0e02-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="b0e02-106">它有時會與 [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) 搭配使用，以判斷在清除更新鎖定之後必須重新繪製的工作區部分。</span><span class="sxs-lookup"><span data-stu-id="b0e02-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="b0e02-107">應用程式會使用 [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) 函數 (指定 DCB \_ 讓) 開始累積周框。</span><span class="sxs-lookup"><span data-stu-id="b0e02-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="b0e02-108">系統隨後會累積周框的點，因為應用程式會使用指定的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="b0e02-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="b0e02-109">應用程式可以使用 [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) 函數，隨時取得目前的周框矩形。</span><span class="sxs-lookup"><span data-stu-id="b0e02-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="b0e02-110">應用程式會再次呼叫 **SetBoundsRect** 來停止累積，並指定 DCB \_ DISABLE 值。</span><span class="sxs-lookup"><span data-stu-id="b0e02-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



