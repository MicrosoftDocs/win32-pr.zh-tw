---
description: 將指定的筆觸與這個 ICoNtextNode 相關聯。
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'ICoNtextNode：： SetStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000072"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="f27e2-103">ICoNtextNode：： SetStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="f27e2-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="f27e2-104">將指定的筆觸與這個 [**ICoNtextNode**](icontextnode.md)相關聯。</span><span class="sxs-lookup"><span data-stu-id="f27e2-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f27e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="f27e2-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="f27e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="f27e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f27e2-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f27e2-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f27e2-108">*PlStrokeIds* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="f27e2-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="f27e2-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f27e2-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f27e2-110">要與此 [**ICoNtextNode**](icontextnode.md)建立關聯之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f27e2-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f27e2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f27e2-111">Return value</span></span>

<span data-ttu-id="f27e2-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f27e2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f27e2-113">備註</span><span class="sxs-lookup"><span data-stu-id="f27e2-113">Remarks</span></span>

<span data-ttu-id="f27e2-114">這個方法不會更新筆墨分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f27e2-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="f27e2-115">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="f27e2-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f27e2-116">使用這個方法可將筆劃資料指派給特定的內容節點。</span><span class="sxs-lookup"><span data-stu-id="f27e2-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="f27e2-117">如需有關同步處理應用程式資料與 **IInkAnalyzer** 的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f27e2-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="f27e2-118">如果任何指定的筆劃已經與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回 **E \_ INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="f27e2-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f27e2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f27e2-119">Requirements</span></span>



| <span data-ttu-id="f27e2-120">需求</span><span class="sxs-lookup"><span data-stu-id="f27e2-120">Requirement</span></span> | <span data-ttu-id="f27e2-121">值</span><span class="sxs-lookup"><span data-stu-id="f27e2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f27e2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f27e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f27e2-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f27e2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f27e2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f27e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f27e2-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="f27e2-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f27e2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f27e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f27e2-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f27e2-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f27e2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f27e2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f27e2-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f27e2-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f27e2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f27e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f27e2-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="f27e2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f27e2-132">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="f27e2-133">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f27e2-134">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="f27e2-135">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f27e2-136">**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="f27e2-137">**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="f27e2-138">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="f27e2-139">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="f27e2-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="f27e2-140">**ICoNtextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="f27e2-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="f27e2-141">**ICoNtextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="f27e2-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="f27e2-142">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="f27e2-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




