---
description: 變更指定之筆劃的地區設定識別碼。
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'IInkAnalyzer：： SetStrokesLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970437"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="aaaf1-103">IInkAnalyzer：： SetStrokesLanguageId 方法</span><span class="sxs-lookup"><span data-stu-id="aaaf1-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="aaaf1-104">變更指定之筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaaf1-105">語法</span><span class="sxs-lookup"><span data-stu-id="aaaf1-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="aaaf1-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaaf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaaf1-107">*ulStrokeIdCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaaf1-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaf1-108">*PlStrokes* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="aaaf1-109">*plStrokes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaaf1-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaf1-110">要指派地區設定識別碼之筆劃的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="aaaf1-111">*lStrokesLCID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaaf1-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaf1-112">要指派給筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaaf1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaaf1-113">Return value</span></span>

<span data-ttu-id="aaaf1-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aaaf1-115">備註</span><span class="sxs-lookup"><span data-stu-id="aaaf1-115">Remarks</span></span>

<span data-ttu-id="aaaf1-116">當您藉由呼叫 [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)、 [**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)、 [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)或 [**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)來加入筆劃時，會設定筆觸的地區設定。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="aaaf1-117">若要取得目前指派給筆劃的地區設定，請呼叫 [**IInkAnalyzer：： GetStrokeLanguageId 方法**](iinkanalyzer-getstrokelanguageid.md)。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="aaaf1-118">指定的筆觸會移至未分類的筆墨節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，其中包含相同語言的筆觸。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="aaaf1-119">如果沒有這類 [**ICoNtextNode**](icontextnode.md) ，此方法會建立新的非分類筆墨節點，並將筆劃移至該節點。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="aaaf1-120">未分類的筆墨節點是具有 UnclassifiedInk 類型的 **ICoNtextNode** 。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="aaaf1-121">如果這個方法會從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，這個方法也會將筆劃的周框方塊新增至筆跡分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="aaaf1-122">如果 *lStrokeLCID* 參數符合筆劃目前的語言識別項，則這個方法不會移動筆劃。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="aaaf1-123">如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="aaaf1-124">如果任何指定的筆觸都沒有識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新 **IInkAnalyzer**。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="aaaf1-125">當 strokeIds 為 **Null** 時，這個方法會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="aaaf1-126">如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="aaaf1-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="aaaf1-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaaf1-127">Requirements</span></span>



| <span data-ttu-id="aaaf1-128">需求</span><span class="sxs-lookup"><span data-stu-id="aaaf1-128">Requirement</span></span> | <span data-ttu-id="aaaf1-129">值</span><span class="sxs-lookup"><span data-stu-id="aaaf1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaf1-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaaf1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aaaf1-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaaf1-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aaaf1-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaaf1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aaaf1-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="aaaf1-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aaaf1-134">標頭</span><span class="sxs-lookup"><span data-stu-id="aaaf1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaaf1-135"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="aaaf1-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aaaf1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="aaaf1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaaf1-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaaf1-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aaaf1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaaf1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaaf1-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-140">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-141">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-142">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-143">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-144">**IInkAnalyzer：： GetStrokeLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-145">**IInkAnalyzer：： SetStrokeLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="aaaf1-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="aaaf1-146">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="aaaf1-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

