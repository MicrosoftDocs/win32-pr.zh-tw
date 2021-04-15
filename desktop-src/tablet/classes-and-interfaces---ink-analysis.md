---
description: 本節包含筆墨分析中所使用之介面和類別的相關資訊。 筆墨分析類別和介面不符合自動化規範。
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: 筆墨分析類別和介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510907"
---
# <a name="ink-analysis-classes-and-interfaces"></a><span data-ttu-id="36ed0-104">筆墨分析類別和介面</span><span class="sxs-lookup"><span data-stu-id="36ed0-104">Ink Analysis Classes and Interfaces</span></span>

<span data-ttu-id="36ed0-105">本節包含筆墨分析中所使用之介面和類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="36ed0-105">This section contains information about the interfaces and classes used in ink analysis.</span></span> <span data-ttu-id="36ed0-106">筆墨分析類別和介面不符合自動化規範。</span><span class="sxs-lookup"><span data-stu-id="36ed0-106">The ink analysis classes and interfaces are not Automation-compliant.</span></span>

## <a name="classes"></a><span data-ttu-id="36ed0-107">類別</span><span class="sxs-lookup"><span data-stu-id="36ed0-107">Classes</span></span>



| <span data-ttu-id="36ed0-108">類別</span><span class="sxs-lookup"><span data-stu-id="36ed0-108">Class</span></span>                                    | <span data-ttu-id="36ed0-109">描述</span><span class="sxs-lookup"><span data-stu-id="36ed0-109">Description</span></span>                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="36ed0-110">**AnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="36ed0-110">**AnalysisRegion**</span></span>](analysisregion.md) | <span data-ttu-id="36ed0-111">實行 [**IAnalysisRegion**](ianalysisregion.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="36ed0-111">Implements the [**IAnalysisRegion**](ianalysisregion.md) interface.</span></span><br/> |
| [<span data-ttu-id="36ed0-112">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="36ed0-112">**InkAnalyzer**</span></span>](inkanalyzer.md)       | <span data-ttu-id="36ed0-113">實行 [**IInkAnalyzer**](iinkanalyzer.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="36ed0-113">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span><br/>       |



 

## <a name="interfaces"></a><span data-ttu-id="36ed0-114">介面</span><span class="sxs-lookup"><span data-stu-id="36ed0-114">Interfaces</span></span>



| <span data-ttu-id="36ed0-115">介面</span><span class="sxs-lookup"><span data-stu-id="36ed0-115">Interface</span></span>                                                    | <span data-ttu-id="36ed0-116">描述</span><span class="sxs-lookup"><span data-stu-id="36ed0-116">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36ed0-117">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="36ed0-117">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)             | <span data-ttu-id="36ed0-118">表示 [**ICoNtextNode**](icontextnode.md) 物件的可能手寫辨識字組相符專案。</span><span class="sxs-lookup"><span data-stu-id="36ed0-118">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                        |
| [<span data-ttu-id="36ed0-119">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="36ed0-119">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)           | <span data-ttu-id="36ed0-120">包含物件的集合，這些物件會執行 [**IAnalysisAlternate**](ianalysisalternate.md) 介面，且為筆跡分析的結果。</span><span class="sxs-lookup"><span data-stu-id="36ed0-120">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span><br/>                                               |
| [<span data-ttu-id="36ed0-121">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="36ed0-121">**IAnalysisRegion**</span></span>](ianalysisregion.md)                   | <span data-ttu-id="36ed0-122">公開代表檔區域之區域的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="36ed0-122">Exposes methods and properties for a region that represents an area of a document.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="36ed0-123">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="36ed0-123">**IAnalysisStatus**</span></span>](ianalysisstatus.md)                   | <span data-ttu-id="36ed0-124">藉由描述分析是否成功完成，以及是否發生任何警告，來表示筆墨分析作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="36ed0-124">Represents the status of the ink analysis operation by describing whether the analysis was completed successfully and whether any warnings occurred.</span></span><br/>                                                  |
| [<span data-ttu-id="36ed0-125">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="36ed0-125">**IAnalysisWarning**</span></span>](ianalysiswarning.md)                 | <span data-ttu-id="36ed0-126">表示筆墨分析作業期間發生的警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="36ed0-126">Represents a warning or error that occurs during an ink analysis operation.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="36ed0-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="36ed0-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)               | <span data-ttu-id="36ed0-128">包含物件的集合，這些物件會執行 [**IAnalysisWarning**](ianalysiswarning.md) 介面，且為筆跡分析作業的結果。</span><span class="sxs-lookup"><span data-stu-id="36ed0-128">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                      |
| [<span data-ttu-id="36ed0-129">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="36ed0-129">**IContextLink**</span></span>](icontextlink.md)                         | <span data-ttu-id="36ed0-130">表示兩個 [**ICoNtextNode**](icontextnode.md) 物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36ed0-130">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="36ed0-131">**ICoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="36ed0-131">**IContextLinks**</span></span>](icontextlinks.md)                       | <span data-ttu-id="36ed0-132">包含物件的集合，這些物件會執行 [**ICoNtextLink**](icontextlink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="36ed0-132">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="36ed0-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="36ed0-133">**IContextNode**</span></span>](icontextnode.md)                         | <span data-ttu-id="36ed0-134">代表物件樹狀結構中建立為筆跡分析一部分的節點。</span><span class="sxs-lookup"><span data-stu-id="36ed0-134">Represents a node in a tree of objects that are created as part of ink analysis.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="36ed0-135">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="36ed0-135">**IContextNodes**</span></span>](icontextnodes.md)                       | <span data-ttu-id="36ed0-136">包含物件的集合，這些物件會執行 [**ICoNtextNode**](icontextnode.md) 介面，且為筆跡分析作業的結果。</span><span class="sxs-lookup"><span data-stu-id="36ed0-136">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                              |
| [<span data-ttu-id="36ed0-137">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="36ed0-137">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)     | <span data-ttu-id="36ed0-138">提供手寫辨識器的存取權，以搭配筆墨分析使用。</span><span class="sxs-lookup"><span data-stu-id="36ed0-138">Provides access to handwriting recognizers for use with ink analysis.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="36ed0-139">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="36ed0-139">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)   | <span data-ttu-id="36ed0-140">包含物件的集合，這些物件會執行 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 介面，以及表示辨識手寫、物件或手勢的能力。</span><span class="sxs-lookup"><span data-stu-id="36ed0-140">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span><br/> |
| [<span data-ttu-id="36ed0-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="36ed0-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)                         | <span data-ttu-id="36ed0-142">提供對版面配置分析、書寫和繪製分類，以及手寫辨識的存取。</span><span class="sxs-lookup"><span data-stu-id="36ed0-142">Provides access to layout analysis, writing and drawing classification, and handwriting recognition.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="36ed0-143">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="36ed0-143">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md) | <span data-ttu-id="36ed0-144">公開方法，以評估 [**ICoNtextNode**](icontextnode.md) 物件是否符合或失敗指定的條件。</span><span class="sxs-lookup"><span data-stu-id="36ed0-144">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span><br/>                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="36ed0-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="36ed0-145">Return Values</span></span>

<span data-ttu-id="36ed0-146">Tablet PC COM 程式庫中的方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="36ed0-146">Methods in the Tablet PC COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="36ed0-147">除非另有說明，否則此表描述 **HRESULT** 值的意義。</span><span class="sxs-lookup"><span data-stu-id="36ed0-147">Unless otherwise noted, the meanings of the **HRESULT** values are described in this table.</span></span>



| <span data-ttu-id="36ed0-148">HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="36ed0-148">HRESULT value</span></span>                                   | <span data-ttu-id="36ed0-149">Description</span><span class="sxs-lookup"><span data-stu-id="36ed0-149">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ed0-150">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="36ed0-150">S\_OK</span></span><br/>                                | <span data-ttu-id="36ed0-151">成功。</span><span class="sxs-lookup"><span data-stu-id="36ed0-151">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="36ed0-152">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="36ed0-152">E\_POINTER</span></span><br/>                           | <span data-ttu-id="36ed0-153">輸入或輸出參數的至少一個指標 () 無效。</span><span class="sxs-lookup"><span data-stu-id="36ed0-153">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="36ed0-154">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="36ed0-154">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="36ed0-155">成員嘗試傳入不正確引數。</span><span class="sxs-lookup"><span data-stu-id="36ed0-155">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="36ed0-156">E \_ 筆墨 \_ 例外狀況</span><span class="sxs-lookup"><span data-stu-id="36ed0-156">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="36ed0-157">發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="36ed0-157">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="36ed0-158">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="36ed0-158">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="36ed0-159">系統無法配置記憶體來完成操作。</span><span class="sxs-lookup"><span data-stu-id="36ed0-159">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="36ed0-160">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="36ed0-160">E\_FAIL</span></span><br/>                              | <span data-ttu-id="36ed0-161">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="36ed0-161">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="36ed0-162">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="36ed0-162">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="36ed0-163">成員嘗試使用不正確作業。</span><span class="sxs-lookup"><span data-stu-id="36ed0-163">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="36ed0-164">TPC \_ E \_ 無效 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="36ed0-164">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="36ed0-165">成員嘗試使用不正確模式。</span><span class="sxs-lookup"><span data-stu-id="36ed0-165">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="36ed0-166">TPC \_ E \_ 不正確設定 \_</span><span class="sxs-lookup"><span data-stu-id="36ed0-166">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="36ed0-167">成員嘗試使用不正確設定。</span><span class="sxs-lookup"><span data-stu-id="36ed0-167">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="36ed0-168">TPC \_ E \_ 不正確封 \_ 包 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="36ed0-168">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="36ed0-169">成員嘗試使用不正確封包描述。</span><span class="sxs-lookup"><span data-stu-id="36ed0-169">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="36ed0-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="36ed0-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ed0-171">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="36ed0-171">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




