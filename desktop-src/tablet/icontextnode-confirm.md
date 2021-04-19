---
description: 修改確認類型，以控制 IInkAnalyzer 物件可變更的 ICoNtextNode 內容。
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'ICoNtextNode：： Confirm 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973480"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="5881e-103">ICoNtextNode：： Confirm 方法</span><span class="sxs-lookup"><span data-stu-id="5881e-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="5881e-104">修改確認類型，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 物件可變更的 [**ICoNtextNode**](icontextnode.md)內容。</span><span class="sxs-lookup"><span data-stu-id="5881e-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5881e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5881e-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="5881e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5881e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5881e-107">*confirmedType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5881e-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5881e-108">套用至節點的 [**ConfirmationType**](confirmationtype.md) 。</span><span class="sxs-lookup"><span data-stu-id="5881e-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5881e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5881e-109">Return value</span></span>

<span data-ttu-id="5881e-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="5881e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5881e-111">備註</span><span class="sxs-lookup"><span data-stu-id="5881e-111">Remarks</span></span>

<span data-ttu-id="5881e-112">使用這個方法可讓使用者確認 [**IInkAnalyzer**](iinkanalyzer.md) 已正確分析筆劃。</span><span class="sxs-lookup"><span data-stu-id="5881e-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="5881e-113">在呼叫 **ICoNtextNode：： Confirm** 之後， **IInkAnalyzer** 將不會在後續分析期間變更這些筆觸的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5881e-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="5881e-114">當使用者已確認分析結果，而不希望 [**IInkAnalyzer**](iinkanalyzer.md)在稍後的分析期間變更 [**ICoNtextNode**](icontextnode.md)時，請使用 **ICoNtextNode：： Confirm** 。</span><span class="sxs-lookup"><span data-stu-id="5881e-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="5881e-115">例如，如果使用者將 "to" 單字寫入，然後應用程式呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)，則筆墨分析器會產生值為 "to" 的 InkWord 節點。</span><span class="sxs-lookup"><span data-stu-id="5881e-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="5881e-116">如果使用者接著將 "me" 之後新增為一個單字，而應用程式再次呼叫 **IInkAnalyzer：：分析方法** ，則筆墨分析器可以移除先前的 InkWord 節點，並建立值為 "書籍" 的新 InkWord 節點。</span><span class="sxs-lookup"><span data-stu-id="5881e-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="5881e-117">但是，如果在第一次呼叫 **IInkAnalyzer：： Confirm 方法** 之後，應用程式會在 InkWord 節點上呼叫 **ICoNtextNode：： Confirm** （ [**ConfirmationType**](confirmationtype.md) 值 **NodeTypeAndProperties**），然後使用者加入 "Me"，然後當應用程式呼叫 **IInkAnalyzer：：分析方法** 時，筆墨分析器不會移除或變更 "to" 節點。</span><span class="sxs-lookup"><span data-stu-id="5881e-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="5881e-118">相反地，「筆跡分析器」可能會辨識「到」和「我」兩個 InkWord 節點。</span><span class="sxs-lookup"><span data-stu-id="5881e-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="5881e-119">[**ICoNtextNode**](icontextnode.md) 只能確認 InkWord 和 InkDrawing 類型的物件 (請參閱) 的 [內容節點類型](context-node-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="5881e-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="5881e-120">當節點不是分葉節點時， **ICoNtextNode：： Confirm** 會傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="5881e-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="5881e-121">[**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md) 和 [**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md) 會 unconfirm 從中移除筆劃資料的任何節點。</span><span class="sxs-lookup"><span data-stu-id="5881e-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="5881e-122">[**ICoNtextNode：： SetStrokes**](icontextnode-setstrokes.md)、 [**IInkAnalyzer：： SetStrokesType**](iinkanalyzer-setstrokestype.md)和 [**IInkAnalyzer：： SetStrokeType**](iinkanalyzer-setstroketype.md)如果已確認 [**INVALIDOPERATION**](icontextnode.md)物件，則傳回 **CORE \_ E \_ ICoNtextNode** 。</span><span class="sxs-lookup"><span data-stu-id="5881e-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="5881e-123">如果已確認來源或目的節點， [**ICoNtextNode：： ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5881e-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5881e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5881e-124">Requirements</span></span>



| <span data-ttu-id="5881e-125">需求</span><span class="sxs-lookup"><span data-stu-id="5881e-125">Requirement</span></span> | <span data-ttu-id="5881e-126">值</span><span class="sxs-lookup"><span data-stu-id="5881e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5881e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5881e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5881e-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5881e-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5881e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5881e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5881e-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="5881e-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5881e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5881e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5881e-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="5881e-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5881e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5881e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5881e-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5881e-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5881e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5881e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5881e-136">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="5881e-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5881e-137">**ICoNtextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="5881e-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="5881e-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="5881e-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




