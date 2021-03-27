---
description: 曲線記錄代表二次曲線 (也就是 TrueType 所使用的二次 b 曲線) 。
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: 曲線記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692596"
---
# <a name="spline-records"></a><span data-ttu-id="a6f50-103">曲線記錄</span><span class="sxs-lookup"><span data-stu-id="a6f50-103">Spline Records</span></span>

<span data-ttu-id="a6f50-104">曲線記錄代表二次曲線 (也就是 TrueType 所使用的二次 b 曲線) 。</span><span class="sxs-lookup"><span data-stu-id="a6f50-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="a6f50-105">樣條記錄是從上一筆記錄的最後一個點開始 (或針對輪廓中的第一筆記錄，並將起始點) 。</span><span class="sxs-lookup"><span data-stu-id="a6f50-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="a6f50-106">針對第一個曲線記錄，記錄中的起始點和最後一個點是在圖像大綱上。</span><span class="sxs-lookup"><span data-stu-id="a6f50-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="a6f50-107">對於所有其他的曲線記錄而言，只有最後一個點是在圖像大綱上。</span><span class="sxs-lookup"><span data-stu-id="a6f50-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="a6f50-108">樣條記錄中的所有其他點都是在字元外框外，而且必須轉譯為 b 曲線的控制點。</span><span class="sxs-lookup"><span data-stu-id="a6f50-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="a6f50-109">輪廓中的最後一個曲線或聚合線條記錄一律會以輪廓的起點作為結尾。</span><span class="sxs-lookup"><span data-stu-id="a6f50-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="a6f50-110">這種安排可確保每個分佈都已關閉。</span><span class="sxs-lookup"><span data-stu-id="a6f50-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="a6f50-111">因為 b 曲線需要三個點， (在外框的兩個點之間的字元外框輪廓) ，所以當曲線記錄包含一個以上的離曲線點時，您必須執行一些計算。</span><span class="sxs-lookup"><span data-stu-id="a6f50-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="a6f50-112">例如，如果曲線記錄包含三個點 (A、B 和 C) 而不是第一筆記錄，則點 A 和 B 會關閉字元外框。</span><span class="sxs-lookup"><span data-stu-id="a6f50-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="a6f50-113">若要解讀點 A，請使用目前的位置 (永遠在圖像大綱) ，以及在點 A 和 B 之間的圖像大綱上的點。若要尋找介於 A 和 B 之間的中點 (M) ，您可以執行下列計算。</span><span class="sxs-lookup"><span data-stu-id="a6f50-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="a6f50-114">M = A + (B A) /2</span><span class="sxs-lookup"><span data-stu-id="a6f50-114">M = A + (B A)/2</span></span>

<span data-ttu-id="a6f50-115">根據 TrueType 字型中所使用之曲線格式的定義，曲線記錄中連續外框之間的中間點是在圖像大綱上的點。</span><span class="sxs-lookup"><span data-stu-id="a6f50-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="a6f50-116">如果目前的位置是由 P 指定，則此曲線記錄所定義的兩個二次曲線會是 (P、A、M) 和 (M、B、C) 。</span><span class="sxs-lookup"><span data-stu-id="a6f50-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



