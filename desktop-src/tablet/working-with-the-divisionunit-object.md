---
description: DivisionUnit 物件代表 DivisionResult 物件的單一結構化元素。 DivisionUnit 物件可能代表繪圖、手寫的單一辨識區段、手寫行或手寫區塊。
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: 使用 DivisionUnit 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade8b617ae8e64c2641ef53a628a44e72e4fc35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847973"
---
# <a name="working-with-the-divisionunit-object"></a><span data-ttu-id="dc523-104">使用 DivisionUnit 物件</span><span class="sxs-lookup"><span data-stu-id="dc523-104">Working with the DivisionUnit Object</span></span>

<span data-ttu-id="dc523-105">**DivisionUnit** 物件代表 **DivisionResult** 物件的單一結構化元素。</span><span class="sxs-lookup"><span data-stu-id="dc523-105">The **DivisionUnit** object represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="dc523-106">**DivisionUnit** 物件可能代表繪圖、手寫的單一辨識區段、手寫行或手寫區塊。</span><span class="sxs-lookup"><span data-stu-id="dc523-106">A **DivisionUnit** object may represent a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting.</span></span>

<span data-ttu-id="dc523-107">[**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉會定義版面配置分析可辨識的結構化元素類型。</span><span class="sxs-lookup"><span data-stu-id="dc523-107">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span> <span data-ttu-id="dc523-108">在自動化中， **DivisionUnit** 物件稱為 [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)。</span><span class="sxs-lookup"><span data-stu-id="dc523-108">In Automation, the **DivisionUnit** object is called [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit).</span></span>

<span data-ttu-id="dc523-109">**DivisionUnit** 物件的 [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype)屬性會傳回 **DivisionUnit** 物件為的結構化元素類型。</span><span class="sxs-lookup"><span data-stu-id="dc523-109">The [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) property of the **DivisionUnit** object returns the structural element type that the **DivisionUnit** object is.</span></span> <span data-ttu-id="dc523-110">**DivisionUnit** 物件的 [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85))屬性會傳回手寫專案的辨識文字，或針對繪圖元素傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dc523-110">The [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) property of the **DivisionUnit** object returns the recognition text for handwriting elements, or **NULL** for drawing elements.</span></span>

<span data-ttu-id="dc523-111">**DivisionUnit** 物件的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes)屬性包含 **DivisionResult** 物件中對應至這個專案之筆劃的子集。</span><span class="sxs-lookup"><span data-stu-id="dc523-111">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) property of the **DivisionUnit** object contains the subset of the strokes in the **DivisionResult** object that correspond to this element.</span></span> <span data-ttu-id="dc523-112">由於手寫元素存在於不同層級的詳細資料，因此不同元素的 **筆觸** 集合可能會重迭。</span><span class="sxs-lookup"><span data-stu-id="dc523-112">Because handwriting elements exist for different levels of detail, the **Strokes** collections for different elements may overlap.</span></span> <span data-ttu-id="dc523-113">具體而言，辨識區段會共用含有線條和區塊的筆劃，而線條則會與它所屬的區塊共用筆觸。</span><span class="sxs-lookup"><span data-stu-id="dc523-113">Specifically, a recognition segment shares strokes with the line and block it is part of, and a line shares strokes with the block it is part of.</span></span>

<span data-ttu-id="dc523-114">**DivisionUnit** 物件的 [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform)屬性會傳回將元素的筆觸旋轉為水準的矩陣。</span><span class="sxs-lookup"><span data-stu-id="dc523-114">The [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) property of the **DivisionUnit** object returns a matrix for rotating the strokes of the element to horizontal.</span></span> <span data-ttu-id="dc523-115">若為段落和繪圖元素， **RotationTransform** 屬性會傳回識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="dc523-115">For paragraph and drawing elements the **RotationTransform** property returns the identity matrix.</span></span> <span data-ttu-id="dc523-116">文字辨識器在手寫上的執行速度會比在手寫上進行水準對齊的方式更好。</span><span class="sxs-lookup"><span data-stu-id="dc523-116">A text recognizer performs much better on handwriting that is horizontally aligned than it does on handwriting that is not.</span></span> <span data-ttu-id="dc523-117">在自動化中，這稱為 **RotationTransform** 屬性，它會傳回包含轉換矩陣的 [**InkTransform**](inktransform-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="dc523-117">In Automation, this is called the **RotationTransform** property, and it returns an [**InkTransform**](inktransform-class.md) object which contains the transformation matrix.</span></span> <span data-ttu-id="dc523-118">**RotationTransform** 屬性會針對段落和繪圖元素傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dc523-118">The **RotationTransform** property returns **NULL** for paragraph and drawing elements.</span></span>

<span data-ttu-id="dc523-119">如需 **DivisionResult** 物件的詳細資訊，請參閱 [使用 DivisionResult 物件](working-with-the-divisionresult-object.md)。</span><span class="sxs-lookup"><span data-stu-id="dc523-119">For more information about the **DivisionResult** object, see [Working with the DivisionResult Object](working-with-the-divisionresult-object.md).</span></span>

 

 
