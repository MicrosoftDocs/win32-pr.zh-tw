---
description: 表示辨識器用來繪製筆墨的區域。 此區域稱為辨識指南。
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: 'InkRecognizerGuide 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195322"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="31a8a-104">InkRecognizerGuide 類別</span><span class="sxs-lookup"><span data-stu-id="31a8a-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="31a8a-105">表示辨識器用來繪製筆墨的區域。</span><span class="sxs-lookup"><span data-stu-id="31a8a-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="31a8a-106">此區域稱為辨識指南。</span><span class="sxs-lookup"><span data-stu-id="31a8a-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="31a8a-107">**InkRecognizerGuide** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="31a8a-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="31a8a-108">介面</span><span class="sxs-lookup"><span data-stu-id="31a8a-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="31a8a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="31a8a-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="31a8a-110">介面</span><span class="sxs-lookup"><span data-stu-id="31a8a-110">Interfaces</span></span>

<span data-ttu-id="31a8a-111">**InkRecognizerGuide** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="31a8a-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="31a8a-112">介面</span><span class="sxs-lookup"><span data-stu-id="31a8a-112">Interface</span></span>               | <span data-ttu-id="31a8a-113">描述</span><span class="sxs-lookup"><span data-stu-id="31a8a-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="31a8a-114">**IInkRecognizerGuide**</span><span class="sxs-lookup"><span data-stu-id="31a8a-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="31a8a-115">這個物件會實 **IInkRecognizerGuide** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="31a8a-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31a8a-116">屬性</span><span class="sxs-lookup"><span data-stu-id="31a8a-116">Properties</span></span>

<span data-ttu-id="31a8a-117">**InkRecognizerGuide** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="31a8a-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="31a8a-118">屬性</span><span class="sxs-lookup"><span data-stu-id="31a8a-118">Property</span></span>                                                       | <span data-ttu-id="31a8a-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="31a8a-119">Access type</span></span>           | <span data-ttu-id="31a8a-120">Description</span><span class="sxs-lookup"><span data-stu-id="31a8a-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31a8a-121">**資料行**</span><span class="sxs-lookup"><span data-stu-id="31a8a-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="31a8a-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-122">Read/write</span></span><br/> | <span data-ttu-id="31a8a-123">取得或設定節目表方塊中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="31a8a-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="31a8a-124">**DrawnBox**</span><span class="sxs-lookup"><span data-stu-id="31a8a-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="31a8a-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-125">Read/write</span></span><br/> | <span data-ttu-id="31a8a-126">取得或設定在平板電腦螢幕上實際繪製的方塊，以及寫入的位置。</span><span class="sxs-lookup"><span data-stu-id="31a8a-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="31a8a-127">**GuideData**</span><span class="sxs-lookup"><span data-stu-id="31a8a-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="31a8a-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-128">Read/write</span></span><br/> | <span data-ttu-id="31a8a-129">取得或設定 c + + 開發人員的參考資料。</span><span class="sxs-lookup"><span data-stu-id="31a8a-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="31a8a-130">**中線**</span><span class="sxs-lookup"><span data-stu-id="31a8a-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="31a8a-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-131">Read/write</span></span><br/> | <span data-ttu-id="31a8a-132">取得或設定中線高度。</span><span class="sxs-lookup"><span data-stu-id="31a8a-132">Gets or sets the midline height.</span></span> <span data-ttu-id="31a8a-133">中線高度是繪製方塊的距離，與基線之間的距離。</span><span class="sxs-lookup"><span data-stu-id="31a8a-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="31a8a-134">**行**</span><span class="sxs-lookup"><span data-stu-id="31a8a-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="31a8a-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-135">Read/write</span></span><br/> | <span data-ttu-id="31a8a-136">取得或設定節目表方塊中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="31a8a-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="31a8a-137">**WritingBox**</span><span class="sxs-lookup"><span data-stu-id="31a8a-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="31a8a-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a8a-138">Read/write</span></span><br/> | <span data-ttu-id="31a8a-139">取得或設定節目表方塊中的隱藏寫入區域，在此區域中可以實際進行寫入。</span><span class="sxs-lookup"><span data-stu-id="31a8a-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="31a8a-140">備註</span><span class="sxs-lookup"><span data-stu-id="31a8a-140">Remarks</span></span>

<span data-ttu-id="31a8a-141">您可以藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化此物件。</span><span class="sxs-lookup"><span data-stu-id="31a8a-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="31a8a-142">依預設，沒有任何辨識器指南。</span><span class="sxs-lookup"><span data-stu-id="31a8a-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="31a8a-143">預設的指南會將所有屬性值設定為0。</span><span class="sxs-lookup"><span data-stu-id="31a8a-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="31a8a-144">您必須使用這個物件的屬性來設定節目表。</span><span class="sxs-lookup"><span data-stu-id="31a8a-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="31a8a-145">如果應用程式已在使用者應寫入的畫面上繪製指導方針，則應用程式應該設定辨識器指南的屬性值，以通知辨識器。</span><span class="sxs-lookup"><span data-stu-id="31a8a-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="31a8a-146">這些屬性僅適用于辨識器的使用。</span><span class="sxs-lookup"><span data-stu-id="31a8a-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="31a8a-147">設定它們本身並不會在顯示時繪製視覺線索。</span><span class="sxs-lookup"><span data-stu-id="31a8a-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="31a8a-148">應用程式或控制項會繪製視覺線索。</span><span class="sxs-lookup"><span data-stu-id="31a8a-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="31a8a-149">辨識器指南可以包含資料列和資料行，而這些資料行會讓辨識器成為執行辨識的較佳內容。</span><span class="sxs-lookup"><span data-stu-id="31a8a-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="31a8a-150">使用輔助線將內容提供給筆墨時，可以更容易辨識像是 "t" 和 "I" 的字母。</span><span class="sxs-lookup"><span data-stu-id="31a8a-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="31a8a-151">例如，您可以在螢幕上繪製水平線，以顯示應該發生書寫的位置 (這種類型的指南只會包含資料列，而且不會) 任何資料行。</span><span class="sxs-lookup"><span data-stu-id="31a8a-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="31a8a-152">藉由撰寫程式程式碼，而不是某些任意空間，辨識精確度也會有所改善。</span><span class="sxs-lookup"><span data-stu-id="31a8a-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="31a8a-153">本指南會以筆墨空間座標來指定筆墨的界限。</span><span class="sxs-lookup"><span data-stu-id="31a8a-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="31a8a-154">[**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)屬性可以定義一個方塊，其大小等於或小於 [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)屬性所定義的方塊。</span><span class="sxs-lookup"><span data-stu-id="31a8a-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="31a8a-155">下圖顯示辨識器指南的元素，其中包含兩個數據列和沒有任何資料行。</span><span class="sxs-lookup"><span data-stu-id="31a8a-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![顯示辨識器指南元素的圖例](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="31a8a-157">除了在螢幕上繪製可顯示要寫入之使用者的線條之外，您還可以在用來撰寫字元或單字的畫面上繪製儲存格。</span><span class="sxs-lookup"><span data-stu-id="31a8a-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="31a8a-158">這稱為已裝箱的輸入，適用于某些亞洲語言。</span><span class="sxs-lookup"><span data-stu-id="31a8a-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="31a8a-159">若要判斷辨識器是否能夠進行已裝箱的輸入，請呼叫 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件的 [[**功能**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities)] 屬性。</span><span class="sxs-lookup"><span data-stu-id="31a8a-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="31a8a-160">下圖顯示具有四個數據行的辨識器指南。</span><span class="sxs-lookup"><span data-stu-id="31a8a-160">The following figure shows a recognizer guide with four columns.</span></span>

![圖例顯示具有四個數據行的辨識器指南](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="31a8a-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="31a8a-162">Requirements</span></span>



| <span data-ttu-id="31a8a-163">需求</span><span class="sxs-lookup"><span data-stu-id="31a8a-163">Requirement</span></span> | <span data-ttu-id="31a8a-164">值</span><span class="sxs-lookup"><span data-stu-id="31a8a-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a8a-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31a8a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="31a8a-166">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="31a8a-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31a8a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="31a8a-168">都不支援</span><span class="sxs-lookup"><span data-stu-id="31a8a-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="31a8a-169">標頭</span><span class="sxs-lookup"><span data-stu-id="31a8a-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a8a-170"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31a8a-171">程式庫</span><span class="sxs-lookup"><span data-stu-id="31a8a-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="31a8a-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="31a8a-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31a8a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a8a-174">**IInkRecognizer 介面**</span><span class="sxs-lookup"><span data-stu-id="31a8a-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="31a8a-175">**InkRecognizerCoNtext 類別**</span><span class="sxs-lookup"><span data-stu-id="31a8a-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

