---
description: 表示 ICoNtextNode 物件的可能手寫辨識字組相符專案。
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: 'IAnalysisAlternate 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191427"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="e7c88-103">IAnalysisAlternate 介面</span><span class="sxs-lookup"><span data-stu-id="e7c88-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="e7c88-104">表示 [**ICoNtextNode**](icontextnode.md) 物件的可能手寫辨識字組相符專案。</span><span class="sxs-lookup"><span data-stu-id="e7c88-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="e7c88-105">成員</span><span class="sxs-lookup"><span data-stu-id="e7c88-105">Members</span></span>

<span data-ttu-id="e7c88-106">**IAnalysisAlternate** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e7c88-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7c88-107">**IAnalysisAlternate** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e7c88-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="e7c88-108">方法</span><span class="sxs-lookup"><span data-stu-id="e7c88-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7c88-109">方法</span><span class="sxs-lookup"><span data-stu-id="e7c88-109">Methods</span></span>

<span data-ttu-id="e7c88-110">**IAnalysisAlternate** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e7c88-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="e7c88-111">方法</span><span class="sxs-lookup"><span data-stu-id="e7c88-111">Method</span></span>                                                                          | <span data-ttu-id="e7c88-112">描述</span><span class="sxs-lookup"><span data-stu-id="e7c88-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7c88-113">**GetAlternateNodes**</span><span class="sxs-lookup"><span data-stu-id="e7c88-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="e7c88-114">抓取與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e7c88-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="e7c88-115">**GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="e7c88-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="e7c88-116">抓取值，指出 [**IInkAnalyzer**](iinkanalyzer.md) 對 **IAnalysisAlternate** 精確度的信賴等級。</span><span class="sxs-lookup"><span data-stu-id="e7c88-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="e7c88-117">**GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="e7c88-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="e7c88-118">抓取 **IAnalysisAlternate** 物件的已識別字串值。</span><span class="sxs-lookup"><span data-stu-id="e7c88-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="e7c88-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="e7c88-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="e7c88-120">抓取與這個 **IAnalysisAlternate** 相關聯的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7c88-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e7c88-121">備註</span><span class="sxs-lookup"><span data-stu-id="e7c88-121">Remarks</span></span>

<span data-ttu-id="e7c88-122">使用者的手寫形式有許多變化。</span><span class="sxs-lookup"><span data-stu-id="e7c88-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="e7c88-123">基於這個理由，手寫辨識器有時可以將手寫轉換成文字，與使用者所預期的不同。</span><span class="sxs-lookup"><span data-stu-id="e7c88-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="e7c88-124">當 [**IInkAnalyzer**](iinkanalyzer.md) 對筆劃集合執行分析時， **IInkAnalyzer** 會尋找手寫表示的最可能字組。</span><span class="sxs-lookup"><span data-stu-id="e7c88-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="e7c88-125">此外， **IInkAnalyzer** 也會尋找替代辨識相符專案的集合，這些專案會儲存在 [**IAnalysisAlternates**](ianalysisalternates.md) 集合中。</span><span class="sxs-lookup"><span data-stu-id="e7c88-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="e7c88-126">為了讓使用者能夠利用辨識替代，您必須建立使用者介面，讓使用者可以選取正確的 **IAnalysisAlternate**。</span><span class="sxs-lookup"><span data-stu-id="e7c88-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="e7c88-127">**IAnalysisAlternate** 物件通常是透過 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)來取得。</span><span class="sxs-lookup"><span data-stu-id="e7c88-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="e7c88-128">集合中的第一個 **IAnalysisAlternate** 物件是 [**IInkAnalyzer**](iinkanalyzer.md) 視為最可能替代的物件。</span><span class="sxs-lookup"><span data-stu-id="e7c88-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="e7c88-129">這個介面相當於 .NET Framework 中的 [AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) 。</span><span class="sxs-lookup"><span data-stu-id="e7c88-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c88-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7c88-130">Requirements</span></span>



| <span data-ttu-id="e7c88-131">需求</span><span class="sxs-lookup"><span data-stu-id="e7c88-131">Requirement</span></span> | <span data-ttu-id="e7c88-132">值</span><span class="sxs-lookup"><span data-stu-id="e7c88-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c88-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7c88-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c88-134">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7c88-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7c88-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7c88-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c88-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7c88-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e7c88-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e7c88-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c88-138"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e7c88-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7c88-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c88-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7c88-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c88-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e7c88-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7c88-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c88-142">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="e7c88-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="e7c88-143">**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="e7c88-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e7c88-144">**IInkAnalyzer：： GetAlternatesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="e7c88-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="e7c88-145">**IInkAnalyzer：： GetAlternates 方法**</span><span class="sxs-lookup"><span data-stu-id="e7c88-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="e7c88-146">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e7c88-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

