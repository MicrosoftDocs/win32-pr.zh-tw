---
description: 表示能夠分析筆劃集合的版面配置，並將其分成文字和圖形。
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: 'InkDivider 類別 (Msinkaut15) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996914"
---
# <a name="inkdivider-class"></a><span data-ttu-id="2fdef-103">InkDivider 類別</span><span class="sxs-lookup"><span data-stu-id="2fdef-103">InkDivider class</span></span>

<span data-ttu-id="2fdef-104">表示能夠分析筆劃集合的版面配置，並將其分成文字和圖形。</span><span class="sxs-lookup"><span data-stu-id="2fdef-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="2fdef-105">**InkDivider** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2fdef-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="2fdef-106">介面</span><span class="sxs-lookup"><span data-stu-id="2fdef-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="2fdef-107">方法</span><span class="sxs-lookup"><span data-stu-id="2fdef-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="2fdef-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2fdef-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="2fdef-109">介面</span><span class="sxs-lookup"><span data-stu-id="2fdef-109">Interfaces</span></span>

<span data-ttu-id="2fdef-110">**InkDivider** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="2fdef-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="2fdef-111">介面</span><span class="sxs-lookup"><span data-stu-id="2fdef-111">Interface</span></span>       | <span data-ttu-id="2fdef-112">描述</span><span class="sxs-lookup"><span data-stu-id="2fdef-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="2fdef-113">**IInkDivider**</span><span class="sxs-lookup"><span data-stu-id="2fdef-113">**IInkDivider**</span></span> | <span data-ttu-id="2fdef-114">這個物件會實 **IInkDivider** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="2fdef-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="2fdef-115">方法</span><span class="sxs-lookup"><span data-stu-id="2fdef-115">Methods</span></span>

<span data-ttu-id="2fdef-116">**InkDivider** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2fdef-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="2fdef-117">方法</span><span class="sxs-lookup"><span data-stu-id="2fdef-117">Method</span></span>                              | <span data-ttu-id="2fdef-118">描述</span><span class="sxs-lookup"><span data-stu-id="2fdef-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fdef-119">**劃分**</span><span class="sxs-lookup"><span data-stu-id="2fdef-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="2fdef-120">傳回 [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件，其中包含 **InkDivider** 物件中筆劃的結構化資訊。</span><span class="sxs-lookup"><span data-stu-id="2fdef-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2fdef-121">屬性</span><span class="sxs-lookup"><span data-stu-id="2fdef-121">Properties</span></span>

<span data-ttu-id="2fdef-122">**InkDivider** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2fdef-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="2fdef-123">屬性</span><span class="sxs-lookup"><span data-stu-id="2fdef-123">Property</span></span>                                                             | <span data-ttu-id="2fdef-124">存取類型</span><span class="sxs-lookup"><span data-stu-id="2fdef-124">Access type</span></span>           | <span data-ttu-id="2fdef-125">Description</span><span class="sxs-lookup"><span data-stu-id="2fdef-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fdef-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="2fdef-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="2fdef-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2fdef-127">Read/write</span></span><br/> | <span data-ttu-id="2fdef-128">取得或設定 HIMETRIC 單位中預期的手寫高度。</span><span class="sxs-lookup"><span data-stu-id="2fdef-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="2fdef-129">**RecognizerCoNtext**</span><span class="sxs-lookup"><span data-stu-id="2fdef-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="2fdef-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2fdef-130">Read/write</span></span><br/> | <span data-ttu-id="2fdef-131">取得或設定用於手寫辨識的 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2fdef-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="2fdef-132">**中風**</span><span class="sxs-lookup"><span data-stu-id="2fdef-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="2fdef-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2fdef-133">Read/write</span></span><br/> | <span data-ttu-id="2fdef-134">取得或設定 **InkDivider** 物件所包含的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="2fdef-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="2fdef-135">備註</span><span class="sxs-lookup"><span data-stu-id="2fdef-135">Remarks</span></span>

<span data-ttu-id="2fdef-136">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="2fdef-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="2fdef-137">**InkDivider** 物件使用筆觸的版面配置、筆劃的新增順序、筆劃的繪製方向，以及執行筆墨分析的其他因素。」。</span><span class="sxs-lookup"><span data-stu-id="2fdef-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="2fdef-138">**InkDivider** 物件所分析的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合會包含在 **InkDivider** 物件的 [[**筆觸**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="2fdef-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="2fdef-139">當您在集合中加入或刪除時， **InkDivider** 物件會動態分析 InkStrokes 集合，但不會執行任何筆觸修改。</span><span class="sxs-lookup"><span data-stu-id="2fdef-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="2fdef-140">分析結果會在 [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="2fdef-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="2fdef-141">**InkDivider** 物件會使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件，以更精確地分割筆劃並將辨識字串指派給結果。</span><span class="sxs-lookup"><span data-stu-id="2fdef-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="2fdef-142">**InkDivider** 物件使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件的預設屬性設定。</span><span class="sxs-lookup"><span data-stu-id="2fdef-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="2fdef-143">如果您沒有將辨識器內容指派給 **InkDivider** 物件， **InkDivider** 物件仍會分析筆墨，但是會比較不精確地分割筆劃，且不會將文字與部門結果產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2fdef-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="2fdef-144">在將筆劃新增至 [**筆觸**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)屬性之前，應該先設定 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性。</span><span class="sxs-lookup"><span data-stu-id="2fdef-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="2fdef-145">將筆劃加入至 **InkDivider** 物件之後，就無法變更 **RecognizerCoNtext** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2fdef-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="2fdef-146">**InkDivider** 目前不支援垂直語言。</span><span class="sxs-lookup"><span data-stu-id="2fdef-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="2fdef-147">為了讓 **InkDivider** 物件正確辨識這些語言，該語言的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件必須支援可用的輸入功能，而且必須由左至右寫入字元。</span><span class="sxs-lookup"><span data-stu-id="2fdef-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fdef-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fdef-148">Requirements</span></span>



| <span data-ttu-id="2fdef-149">需求</span><span class="sxs-lookup"><span data-stu-id="2fdef-149">Requirement</span></span> | <span data-ttu-id="2fdef-150">值</span><span class="sxs-lookup"><span data-stu-id="2fdef-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdef-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fdef-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2fdef-152">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fdef-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2fdef-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fdef-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2fdef-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="2fdef-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="2fdef-155">標頭</span><span class="sxs-lookup"><span data-stu-id="2fdef-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fdef-156"><dt>Msinkaut15 (也需要 Msinkaut15 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2fdef-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2fdef-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fdef-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fdef-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fdef-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="2fdef-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fdef-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdef-160">**IInkDivisionResult 介面**</span><span class="sxs-lookup"><span data-stu-id="2fdef-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="2fdef-161">**InkRecognizerCoNtext 類別**</span><span class="sxs-lookup"><span data-stu-id="2fdef-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="2fdef-162">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2fdef-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

