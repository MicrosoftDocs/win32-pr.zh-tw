---
title: '函數 (觸控點擊測試) '
description: 本節中的主題提供觸控點擊測試功能的參考規格。
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- 使用者互動
- input
- 指標
- 觸控
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106996333"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="39a82-107">觸控點擊測試功能</span><span class="sxs-lookup"><span data-stu-id="39a82-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="39a82-108">本節中的主題提供 [觸控點擊測試功能](functions.md)的參考規格。</span><span class="sxs-lookup"><span data-stu-id="39a82-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="39a82-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="39a82-109">In this section</span></span>

| <span data-ttu-id="39a82-110">主題</span><span class="sxs-lookup"><span data-stu-id="39a82-110">Topic</span></span> | <span data-ttu-id="39a82-111">描述</span><span class="sxs-lookup"><span data-stu-id="39a82-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="39a82-112">**EvaluateProximityToPolygon**</span><span class="sxs-lookup"><span data-stu-id="39a82-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="39a82-113">將多邊形的分數傳回為可能的觸控目標 (相較于與 touch contact 區域) 相交的其他所有多邊形，以及多邊形內的調整觸控點。</span><span class="sxs-lookup"><span data-stu-id="39a82-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="39a82-114">**EvaluateProximityToRect**</span><span class="sxs-lookup"><span data-stu-id="39a82-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="39a82-115">將矩形的分數傳回為可能的觸控目標，相較于所有其他與觸控連絡人區域相交的矩形，以及矩形內調整的觸控點。</span><span class="sxs-lookup"><span data-stu-id="39a82-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="39a82-116">**PackTouchHitTestingProximityEvaluation**</span><span class="sxs-lookup"><span data-stu-id="39a82-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="39a82-117">傳回接近的評估分數，以及調整的觸控點座標作為 [WM_TOUCHHITTESTING 訊息](../inputmsg/wm-touchhittesting.md) 回呼的封裝值。</span><span class="sxs-lookup"><span data-stu-id="39a82-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="39a82-118">**RegisterTouchHitTestingWindow**</span><span class="sxs-lookup"><span data-stu-id="39a82-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="39a82-119">註冊視窗以處理 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 通知</span><span class="sxs-lookup"><span data-stu-id="39a82-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="39a82-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="39a82-120">Related topics</span></span>

[<span data-ttu-id="39a82-121">觸控點擊測試參考</span><span class="sxs-lookup"><span data-stu-id="39a82-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
