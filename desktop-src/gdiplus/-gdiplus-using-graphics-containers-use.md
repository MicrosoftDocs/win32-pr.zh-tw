---
description: Graphics 物件提供 DrawLine、DrawImage 和 DrawString 之類的方法來顯示向量影像、點陣影像和文字。
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: 使用圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972825"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="8d078-103">使用圖形容器</span><span class="sxs-lookup"><span data-stu-id="8d078-103">Using Graphics Containers</span></span>

<span data-ttu-id="8d078-104">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))、 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))和 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))之類的方法來顯示向量影像、點陣影像和文字。</span><span class="sxs-lookup"><span data-stu-id="8d078-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="8d078-105">**圖形** 物件也有數個屬性，會影響所繪製專案的品質和方向。</span><span class="sxs-lookup"><span data-stu-id="8d078-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="8d078-106">例如，[平滑模式] 屬性會決定是否要將消除鋸齒套用至線條和曲線，而 [世界轉換] 屬性則會影響繪製之專案的位置和旋轉。</span><span class="sxs-lookup"><span data-stu-id="8d078-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="8d078-107">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件通常會與特定顯示裝置相關聯。</span><span class="sxs-lookup"><span data-stu-id="8d078-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="8d078-108">當您在視窗中使用 **圖形** 物件來繪圖時， **圖形** 物件也會與該特定視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="8d078-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="8d078-109">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件可視為容器，因為它包含一組會影響繪圖的屬性，而且會連結到裝置特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="8d078-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="8d078-110">您可以藉由呼叫該 **圖形** 物件的 [BeginContainer](/previous-versions//ms535731(v=vs.85))方法，在現有的 **圖形** 物件內建立次要容器。</span><span class="sxs-lookup"><span data-stu-id="8d078-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="8d078-111">下列主題會更詳細地討論 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和嵌套容器：</span><span class="sxs-lookup"><span data-stu-id="8d078-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="8d078-112">圖形物件的狀態</span><span class="sxs-lookup"><span data-stu-id="8d078-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="8d078-113">巢狀圖形容器</span><span class="sxs-lookup"><span data-stu-id="8d078-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
