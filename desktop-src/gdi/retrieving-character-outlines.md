---
description: 您可以使用 GetGlyphOutline 函數，從 TrueType 字型取出圖像的外框。
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: 正在抓取字元外框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638193632d4992dfb53f29a3dfe66a858b3e1fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972529"
---
# <a name="retrieving-character-outlines"></a><span data-ttu-id="d68f0-103">正在抓取字元外框</span><span class="sxs-lookup"><span data-stu-id="d68f0-103">Retrieving Character Outlines</span></span>

<span data-ttu-id="d68f0-104">您可以使用 [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) 函數，從 TrueType 字型取出圖像的外框。</span><span class="sxs-lookup"><span data-stu-id="d68f0-104">You can use the [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) function to retrieve the outline of a glyph from a TrueType font.</span></span> <span data-ttu-id="d68f0-105">[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea)函式所傳回的圖像大綱適用于格線擬合的圖像。</span><span class="sxs-lookup"><span data-stu-id="d68f0-105">The glyph outline returned by the [**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) function is for a grid-fitted glyph.</span></span> <span data-ttu-id="d68f0-106"> (格線擬合的字元已經過修改，因此其點陣圖影像會盡可能符合圖像的原始設計 ) 。若您的應用程式需要未修改的圖像大綱，請在大小等於字型單位的字型中，要求字元的字元外框。</span><span class="sxs-lookup"><span data-stu-id="d68f0-106">(A grid-fitted glyph has been modified so that its bitmap image conforms as closely as possible to the original design of the glyph.) If your application requires an unmodified glyph outline, request the glyph outline for a character in a font whose size is equal to the font's em units.</span></span> <span data-ttu-id="d68f0-107"> (若要建立具有這個大小的字型，請將 [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfHeight** 成員設定為 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **ntmSizeEM** 成員值的負值 ) 。</span><span class="sxs-lookup"><span data-stu-id="d68f0-107">(To create a font with this size, set the **lfHeight** member of the [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to the negative of the value of the **ntmSizeEM** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.)</span></span>

<span data-ttu-id="d68f0-108">[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) 會以點陣圖或一系列的線條和曲線來傳回大綱。</span><span class="sxs-lookup"><span data-stu-id="d68f0-108">[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) returns the outline as a bitmap or as a series of polylines and splines.</span></span> <span data-ttu-id="d68f0-109">當應用程式將圖像大綱視為一連串的多線條和曲線時，會傳回 [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) 結構中的資訊，並在描述圖像時所需的 [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) 結構數目。</span><span class="sxs-lookup"><span data-stu-id="d68f0-109">When an application retrieves a glyph outline as a series of polylines and splines, the information is returned in a [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) structure followed by as many [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) structures as required to describe the glyph.</span></span> <span data-ttu-id="d68f0-110">所有點都會以 [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) 結構的形式傳回，並代表絕對位置，而不是相對移動。</span><span class="sxs-lookup"><span data-stu-id="d68f0-110">All points are returned as [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) structures and represent absolute positions, not relative moves.</span></span> <span data-ttu-id="d68f0-111">[**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader)結構的 **pfxStart** 成員所指定的起點是開始分佈的輪廓點。</span><span class="sxs-lookup"><span data-stu-id="d68f0-111">The starting point specified by the **pfxStart** member of the [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) structure is the point where the outline for a contour begins.</span></span> <span data-ttu-id="d68f0-112">接下來的 [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) 結構可以是聚合線條記錄或曲線記錄。</span><span class="sxs-lookup"><span data-stu-id="d68f0-112">The [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) structures that follow can be either polyline records or spline records.</span></span>

<span data-ttu-id="d68f0-113">若要轉譯 TrueType 字元外框，您必須同時使用折線和曲線記錄。</span><span class="sxs-lookup"><span data-stu-id="d68f0-113">To render a TrueType character outline, you must use both the polyline and the spline records.</span></span> <span data-ttu-id="d68f0-114">系統可以輕鬆地轉譯折線和曲線。</span><span class="sxs-lookup"><span data-stu-id="d68f0-114">The system can render both polylines and splines easily.</span></span> <span data-ttu-id="d68f0-115">每一個聚合線條和曲線記錄盡可能包含最多的連續點，以將傳回的記錄數目降至最低。</span><span class="sxs-lookup"><span data-stu-id="d68f0-115">Each polyline and spline record contains as many sequential points as possible, to minimize the number of records returned.</span></span>

<span data-ttu-id="d68f0-116">在 [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) 結構中指定的起始點一律位於圖像的外框上。</span><span class="sxs-lookup"><span data-stu-id="d68f0-116">The starting point specified in the [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) structure is always on the outline of the glyph.</span></span> <span data-ttu-id="d68f0-117">指定的點可作為輪廓的開始和結束點。</span><span class="sxs-lookup"><span data-stu-id="d68f0-117">The specified point serves as both the starting and ending points for the contour.</span></span>

<span data-ttu-id="d68f0-118">本節提供下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d68f0-118">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="d68f0-119">聚合線條記錄</span><span class="sxs-lookup"><span data-stu-id="d68f0-119">Polyline Records</span></span>](polyline-records.md)
-   [<span data-ttu-id="d68f0-120">曲線記錄</span><span class="sxs-lookup"><span data-stu-id="d68f0-120">Spline Records</span></span>](spline-records.md)

 

 
