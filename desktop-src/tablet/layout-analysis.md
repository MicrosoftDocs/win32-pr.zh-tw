---
description: 版面配置分析是在筆劃集合上操作，並且將筆劃分類為手寫和繪圖元素。 分隔物件提供對 Tablet PC 版面配置分析功能的存取。
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: 版面配置分析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969405"
---
# <a name="layout-analysis"></a><span data-ttu-id="7497f-104">版面配置分析</span><span class="sxs-lookup"><span data-stu-id="7497f-104">Layout Analysis</span></span>

<span data-ttu-id="7497f-105">版面配置分析是在 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合上操作，並且將筆劃分類為手寫和繪圖元素。</span><span class="sxs-lookup"><span data-stu-id="7497f-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="7497f-106">[**分隔**](inkdivider-class.md)物件提供對 Tablet PC 版面配置分析功能的存取。</span><span class="sxs-lookup"><span data-stu-id="7497f-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="7497f-107">下表描述 [**分隔**](inkdivider-class.md)物件將筆劃分類至 [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉的結構化元素類型。</span><span class="sxs-lookup"><span data-stu-id="7497f-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="7497f-108">類型</span><span class="sxs-lookup"><span data-stu-id="7497f-108">Type</span></span>          | <span data-ttu-id="7497f-109">Description</span><span class="sxs-lookup"><span data-stu-id="7497f-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7497f-110">**區段**</span><span class="sxs-lookup"><span data-stu-id="7497f-110">**Segment**</span></span>   | <span data-ttu-id="7497f-111">辨識區段。</span><span class="sxs-lookup"><span data-stu-id="7497f-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="7497f-112">**線條**</span><span class="sxs-lookup"><span data-stu-id="7497f-112">**Line**</span></span>      | <span data-ttu-id="7497f-113">包含一或多個辨識區段的手寫行。</span><span class="sxs-lookup"><span data-stu-id="7497f-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="7497f-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="7497f-114">**Paragraph**</span></span> | <span data-ttu-id="7497f-115">包含一或多行手寫的筆劃區塊。</span><span class="sxs-lookup"><span data-stu-id="7497f-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="7497f-116">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="7497f-116">**Drawing**</span></span>   | <span data-ttu-id="7497f-117">非手寫的筆墨。</span><span class="sxs-lookup"><span data-stu-id="7497f-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="7497f-118">[**分割**](inkdivider-class.md)物件具有 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，其 **會在您** 每次在集合中加入或刪除時動態分析。</span><span class="sxs-lookup"><span data-stu-id="7497f-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="7497f-119">**分割** 物件不可序列化，而且您無法儲存其分析狀態。</span><span class="sxs-lookup"><span data-stu-id="7497f-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="7497f-120">因此， **分隔** 物件是針對必須區分混合手寫和繪圖輸入的應用程式所設計，但不需要重新分析會話之間的大量筆跡。</span><span class="sxs-lookup"><span data-stu-id="7497f-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="7497f-121">您可以取得目前分析結果的靜態快照集，這會在 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="7497f-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="7497f-122">您可以取得 [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) 物件，每個物件都代表 **DivisionResult** 物件的單一結構元素。</span><span class="sxs-lookup"><span data-stu-id="7497f-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="7497f-123">**DivisionResult** 和 **DivisionUnit** 物件不是可序列化的。</span><span class="sxs-lookup"><span data-stu-id="7497f-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="7497f-124">不過，這些物件的狀態資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="7497f-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="7497f-125">[**分隔**](inkdivider-class.md)物件僅適用于由左至右書寫。</span><span class="sxs-lookup"><span data-stu-id="7497f-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="7497f-126">若要讓 **分隔** 物件能夠正確地分析垂直語言（例如中文），必須從左至右（而不是從上到下）繪製字元。</span><span class="sxs-lookup"><span data-stu-id="7497f-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

