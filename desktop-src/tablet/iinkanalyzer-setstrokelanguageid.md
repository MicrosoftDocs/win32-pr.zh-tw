---
description: 變更指定之筆劃的地區設定識別碼。
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'IInkAnalyzer：： SetStrokeLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511644"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="38d52-103">IInkAnalyzer：： SetStrokeLanguageId 方法</span><span class="sxs-lookup"><span data-stu-id="38d52-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="38d52-104">變更指定之筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d52-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d52-105">語法</span><span class="sxs-lookup"><span data-stu-id="38d52-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="38d52-106">參數</span><span class="sxs-lookup"><span data-stu-id="38d52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d52-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38d52-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38d52-108">要指派地區設定識別碼之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d52-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="38d52-109">*lStrokeLCID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38d52-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38d52-110">要指派給筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d52-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d52-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="38d52-111">Return value</span></span>

<span data-ttu-id="38d52-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="38d52-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38d52-113">備註</span><span class="sxs-lookup"><span data-stu-id="38d52-113">Remarks</span></span>

<span data-ttu-id="38d52-114">當您藉由呼叫 [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)、 [**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)、 [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)或 [**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)來加入筆劃時，會設定筆觸的地區設定。</span><span class="sxs-lookup"><span data-stu-id="38d52-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="38d52-115">若要取得目前指派給筆劃的地區設定，請呼叫 [**IInkAnalyzer：： GetStrokeLanguageId 方法**](iinkanalyzer-getstrokelanguageid.md)。</span><span class="sxs-lookup"><span data-stu-id="38d52-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="38d52-116">指定的筆觸會移至未分類的筆墨節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，其中包含相同語言的筆觸。</span><span class="sxs-lookup"><span data-stu-id="38d52-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="38d52-117">如果沒有這類 [**ICoNtextNode**](icontextnode.md) ，此方法會建立新的非分類筆墨節點，並將筆劃移至該節點。</span><span class="sxs-lookup"><span data-stu-id="38d52-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="38d52-118">未分類的筆墨節點是具有 UnclassifiedInk 類型的 **ICoNtextNode** 。</span><span class="sxs-lookup"><span data-stu-id="38d52-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="38d52-119">如果這個方法從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，此方法也會將筆劃的周框方塊新增至 ink 分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="38d52-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="38d52-120">如果 *lStrokeLCID* 參數符合筆劃目前的語言識別項，則這個方法不會移動筆劃。</span><span class="sxs-lookup"><span data-stu-id="38d52-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="38d52-121">如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回而不更新 **IInkAnalyzer**。</span><span class="sxs-lookup"><span data-stu-id="38d52-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="38d52-122">如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="38d52-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="38d52-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d52-123">Requirements</span></span>



| <span data-ttu-id="38d52-124">需求</span><span class="sxs-lookup"><span data-stu-id="38d52-124">Requirement</span></span> | <span data-ttu-id="38d52-125">值</span><span class="sxs-lookup"><span data-stu-id="38d52-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d52-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38d52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="38d52-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38d52-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38d52-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38d52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="38d52-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="38d52-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="38d52-130">標頭</span><span class="sxs-lookup"><span data-stu-id="38d52-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d52-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="38d52-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="38d52-132">DLL</span><span class="sxs-lookup"><span data-stu-id="38d52-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38d52-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38d52-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="38d52-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38d52-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d52-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="38d52-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="38d52-136">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="38d52-137">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="38d52-138">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="38d52-139">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="38d52-140">**IInkAnalyzer：： GetStrokeLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="38d52-141">**IInkAnalyzer：： SetStrokesLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="38d52-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="38d52-142">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="38d52-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

