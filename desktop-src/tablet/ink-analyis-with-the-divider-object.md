---
description: 分隔物件提供版面配置分析功能，可將筆劃分類並群組為不同的結構化元素。
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: 使用分隔物件的筆墨分析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f1df175f8746e56cf6ebd1b222b3901fbef36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511034"
---
# <a name="ink-analysis-with-the-divider-object"></a><span data-ttu-id="b8060-103">使用分隔物件的筆墨分析</span><span class="sxs-lookup"><span data-stu-id="b8060-103">Ink Analysis with the Divider Object</span></span>

<span data-ttu-id="b8060-104">[分隔](/previous-versions/ms583616(v=vs.100))物件提供版面配置分析功能，可將筆劃分類並群組為不同的結構化元素。</span><span class="sxs-lookup"><span data-stu-id="b8060-104">The [Divider](/previous-versions/ms583616(v=vs.100)) object provides layout analysis features that classify and group strokes into different structural elements.</span></span>

## <a name="divider-object"></a><span data-ttu-id="b8060-105">分隔物件</span><span class="sxs-lookup"><span data-stu-id="b8060-105">Divider Object</span></span>

<span data-ttu-id="b8060-106">當您新增或移除筆劃時， [分割](/previous-versions/ms583616(v=vs.100)) 物件會分析筆劃。</span><span class="sxs-lookup"><span data-stu-id="b8060-106">The [Divider](/previous-versions/ms583616(v=vs.100)) object analyzes strokes as you add or remove them.</span></span> <span data-ttu-id="b8060-107">您可以藉由呼叫分隔物件的[除法](/previous-versions/ms568936(v=vs.100))方法，在[DivisionResult](/previous-versions/ms583620(v=vs.100))物件中取出分析筆劃的目前分類和群組。</span><span class="sxs-lookup"><span data-stu-id="b8060-107">You can retrieve the current classification and grouping of the analyzed strokes in a [DivisionResult](/previous-versions/ms583620(v=vs.100)) object by calling the [Divide](/previous-versions/ms568936(v=vs.100)) method of the Divider object.</span></span>

<span data-ttu-id="b8060-108">[分割](/previous-versions/ms583616(v=vs.100))物件所分析的筆觸會保留在分隔物件的 [[筆劃](/previous-versions/ms582090(v=vs.100))] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b8060-108">The strokes that the [Divider](/previous-versions/ms583616(v=vs.100)) object analyzes are kept in the [Strokes](/previous-versions/ms582090(v=vs.100)) property of the Divider object.</span></span> <span data-ttu-id="b8060-109">因為 [筆劃](/previous-versions/ms552701(v=vs.100)) 集合是筆墨資料的參考，而不是實際資料本身，所以筆劃集合的父 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件變更可能會使筆劃集合無效。</span><span class="sxs-lookup"><span data-stu-id="b8060-109">Because a [Strokes](/previous-versions/ms552701(v=vs.100)) collection is a reference to ink data and is not the actual data itself, changes in the parent [Ink](/previous-versions/ms583670(v=vs.100)) object of the Strokes collection can invalidate the Strokes collection.</span></span> <span data-ttu-id="b8060-110">如需筆墨資料的詳細資訊，請參閱 [筆墨資料](ink-data.md)。</span><span class="sxs-lookup"><span data-stu-id="b8060-110">For more information about ink data, see [Ink Data](ink-data.md).</span></span>

<span data-ttu-id="b8060-111">[分割](/previous-versions/ms583616(v=vs.100))物件會使用辨識器內容來改善其辨識區段的分析，並產生手寫元素的辨識文字。</span><span class="sxs-lookup"><span data-stu-id="b8060-111">The [Divider](/previous-versions/ms583616(v=vs.100)) object uses a recognizer context to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span> <span data-ttu-id="b8060-112">如果未將辨識器內容指派給分割區物件的 [RecognizerCoNtext](/previous-versions/ms582089(v=vs.100)) 屬性，或未安裝辨識器，則配置分析功能會執行辨識區段分割，而且沒有任何文字與 [DivisionResult](/previous-versions/ms583620(v=vs.100)) 物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="b8060-112">If a recognizer context is not assigned to the [RecognizerContext](/previous-versions/ms582089(v=vs.100)) property of the Divider object or recognizers are not installed, then the layout analysis feature performs the recognition segment division, and no text is associated with the [DivisionResult](/previous-versions/ms583620(v=vs.100)) object.</span></span> <span data-ttu-id="b8060-113">如需筆跡辨識的詳細資訊，請參閱 [筆跡](ink-recognition.md)辨識。</span><span class="sxs-lookup"><span data-stu-id="b8060-113">For more information about ink recognition, see [Ink Recognition](ink-recognition.md).</span></span>

## <a name="divisionresult-object"></a><span data-ttu-id="b8060-114">DivisionResult 物件</span><span class="sxs-lookup"><span data-stu-id="b8060-114">DivisionResult Object</span></span>

<span data-ttu-id="b8060-115">每個[DivisionResult](/previous-versions/ms583620(v=vs.100))物件都會在呼叫[除法](/previous-versions/ms568936(v=vs.100))方法時，記錄[分界線](/previous-versions/ms583616(v=vs.100))物件所包含之筆劃的版面配置分析。</span><span class="sxs-lookup"><span data-stu-id="b8060-115">Each [DivisionResult](/previous-versions/ms583620(v=vs.100)) object records the layout analysis of the strokes contained by the [Divider](/previous-versions/ms583616(v=vs.100)) object at the time the [Divide](/previous-versions/ms568936(v=vs.100)) method is called.</span></span> <span data-ttu-id="b8060-116">DivisionResult 物件也會儲存分析中所使用之筆劃的複本。</span><span class="sxs-lookup"><span data-stu-id="b8060-116">The DivisionResult object also stores a copy of the strokes that were used in the analysis.</span></span>

<span data-ttu-id="b8060-117">[DivisionResult](/previous-versions/ms583620(v=vs.100))物件會依結構化元素類型來分組分析結果。</span><span class="sxs-lookup"><span data-stu-id="b8060-117">The [DivisionResult](/previous-versions/ms583620(v=vs.100)) object groups the analysis results by structural element type.</span></span> <span data-ttu-id="b8060-118">DivisionResult 物件的 [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) 方法會在 [DivisionUnits](/previous-versions/ms583625(v=vs.100)) 集合中傳回指定類型的所有結構化元素集合。</span><span class="sxs-lookup"><span data-stu-id="b8060-118">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the DivisionResult object returns in a [DivisionUnits](/previous-versions/ms583625(v=vs.100)) collection the collection of all structural elements of a given type.</span></span> <span data-ttu-id="b8060-119">[InkDivisionType](/previous-versions/ms552251(v=vs.100))列舉會定義版面配置分析可辨識的元素類型。</span><span class="sxs-lookup"><span data-stu-id="b8060-119">The [InkDivisionType](/previous-versions/ms552251(v=vs.100)) enumeration defines the element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="b8060-120">下表描述 [InkDivisionType](/previous-versions/ms552251(v=vs.100)) 列舉中的元素類型。</span><span class="sxs-lookup"><span data-stu-id="b8060-120">The following table describes the element types in the [InkDivisionType](/previous-versions/ms552251(v=vs.100)) enumeration.</span></span>



| <span data-ttu-id="b8060-121">Name</span><span class="sxs-lookup"><span data-stu-id="b8060-121">Name</span></span>                 | <span data-ttu-id="b8060-122">描述</span><span class="sxs-lookup"><span data-stu-id="b8060-122">Description</span></span>                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8060-123">區段</span><span class="sxs-lookup"><span data-stu-id="b8060-123">Segment</span></span><br/>   | <span data-ttu-id="b8060-124">辨識區段。</span><span class="sxs-lookup"><span data-stu-id="b8060-124">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="b8060-125">線條</span><span class="sxs-lookup"><span data-stu-id="b8060-125">Line</span></span><br/>      | <span data-ttu-id="b8060-126">包含一或多個辨識區段的手寫行。</span><span class="sxs-lookup"><span data-stu-id="b8060-126">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="b8060-127">Paragraph</span><span class="sxs-lookup"><span data-stu-id="b8060-127">Paragraph</span></span><br/> | <span data-ttu-id="b8060-128">包含一或多行手寫的筆劃區塊。</span><span class="sxs-lookup"><span data-stu-id="b8060-128">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="b8060-129">繪圖</span><span class="sxs-lookup"><span data-stu-id="b8060-129">Drawing</span></span><br/>   | <span data-ttu-id="b8060-130">非文字的筆墨。</span><span class="sxs-lookup"><span data-stu-id="b8060-130">Ink that is not text.</span></span><br/>                                                 |



 

<span data-ttu-id="b8060-131">下圖顯示 [DivisionResult](/previous-versions/ms583620(v=vs.100)) 物件辨識的不同元素類型範例。</span><span class="sxs-lookup"><span data-stu-id="b8060-131">The following image shows an example of the different element types the [DivisionResult](/previous-versions/ms583620(v=vs.100)) object recognizes.</span></span>

![divisionresult 物件辨識的不同元素類型圖例](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a><span data-ttu-id="b8060-133">DivisionUnits 集合和 DivisionUnit 物件</span><span class="sxs-lookup"><span data-stu-id="b8060-133">DivisionUnits Collection and DivisionUnit Objects</span></span>

<span data-ttu-id="b8060-134">每個 [DivisionUnits](/previous-versions/ms583625(v=vs.100)) 集合都是單一結構專案類型的版面配置分析結果複本。</span><span class="sxs-lookup"><span data-stu-id="b8060-134">Each [DivisionUnits](/previous-versions/ms583625(v=vs.100)) collection is a copy of the layout analysis result for a single type of structural element.</span></span> <span data-ttu-id="b8060-135">[DivisionUnit](/previous-versions/ms583624(v=vs.100))物件代表 DivisionUnits 集合中的個別元素。</span><span class="sxs-lookup"><span data-stu-id="b8060-135">The [DivisionUnit](/previous-versions/ms583624(v=vs.100)) object represents an individual element in the DivisionUnits collection.</span></span> <span data-ttu-id="b8060-136">每個結構專案都有組成專案的筆劃參考。</span><span class="sxs-lookup"><span data-stu-id="b8060-136">Each structural element has a reference to the strokes that make up the element.</span></span> <span data-ttu-id="b8060-137">如果已安裝辨識器，手寫元素就會有可用的辨識文字。</span><span class="sxs-lookup"><span data-stu-id="b8060-137">If recognizers are installed, handwriting elements have recognition text available.</span></span> <span data-ttu-id="b8060-138">行和辨識區段專案也包含可將元素的筆觸從垂直旋轉為水準的旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="b8060-138">Line and recognition segment elements also include a rotation matrix that can rotate an element's strokes from vertical to horizontal.</span></span>

<span data-ttu-id="b8060-139">[筆墨分割範例](ink-divider-sample.md)主題示範如何使用具有[筆墨](/previous-versions/ms583670(v=vs.100))物件的[分界線](/previous-versions/ms583616(v=vs.100))物件來執行筆墨版面配置分析。</span><span class="sxs-lookup"><span data-stu-id="b8060-139">The [Ink Divider Sample](ink-divider-sample.md) topic demonstrates how to use a [Divider](/previous-versions/ms583616(v=vs.100)) object with [Ink](/previous-versions/ms583670(v=vs.100)) objects to perform ink layout analysis.</span></span>

<span data-ttu-id="b8060-140">如需使用筆墨分析的詳細資訊，請參閱 [分割物件](the-divider-object.md)。</span><span class="sxs-lookup"><span data-stu-id="b8060-140">For more information about using ink analysis, see [The Divider Object](the-divider-object.md).</span></span>

 

