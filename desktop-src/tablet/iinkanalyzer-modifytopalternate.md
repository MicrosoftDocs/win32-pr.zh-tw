---
description: 將目前的上方替代變更為指定的替代，並清除所有與替代物件相關聯之 ICoNtextNode 物件的確認類型。
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer：： ModifyTopAlternate 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997088"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="28411-103">IInkAnalyzer：： ModifyTopAlternate 方法</span><span class="sxs-lookup"><span data-stu-id="28411-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="28411-104">將目前的上方替代變更為指定的替代，並清除所有與替代物件相關聯之 [**ICoNtextNode**](icontextnode.md) 物件的確認類型。</span><span class="sxs-lookup"><span data-stu-id="28411-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="28411-105">語法</span><span class="sxs-lookup"><span data-stu-id="28411-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="28411-106">參數</span><span class="sxs-lookup"><span data-stu-id="28411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28411-107">*pAlternate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28411-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28411-108">[**IAnalysisAlternate**](ianalysisalternate.md)物件，其中包含新的 top 替代。</span><span class="sxs-lookup"><span data-stu-id="28411-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28411-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="28411-109">Return value</span></span>

<span data-ttu-id="28411-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="28411-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28411-111">備註</span><span class="sxs-lookup"><span data-stu-id="28411-111">Remarks</span></span>

<span data-ttu-id="28411-112">若要取得分析替代項，請使用 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)、 [**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)或 [**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)。</span><span class="sxs-lookup"><span data-stu-id="28411-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="28411-113">若要取得與分析替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件，請使用 [**IAnalysisAlternate：： GetAlternateNodes 方法**](ianalysisalternate-getalternatenodes.md)。</span><span class="sxs-lookup"><span data-stu-id="28411-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="28411-114">若要變更內容節點的確認類型，請使用 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)。</span><span class="sxs-lookup"><span data-stu-id="28411-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28411-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="28411-115">Requirements</span></span>



| <span data-ttu-id="28411-116">需求</span><span class="sxs-lookup"><span data-stu-id="28411-116">Requirement</span></span> | <span data-ttu-id="28411-117">值</span><span class="sxs-lookup"><span data-stu-id="28411-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28411-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28411-118">Minimum supported client</span></span><br/> | <span data-ttu-id="28411-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28411-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="28411-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28411-120">Minimum supported server</span></span><br/> | <span data-ttu-id="28411-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="28411-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="28411-122">標頭</span><span class="sxs-lookup"><span data-stu-id="28411-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="28411-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="28411-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="28411-124">DLL</span><span class="sxs-lookup"><span data-stu-id="28411-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28411-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28411-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="28411-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28411-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28411-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="28411-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="28411-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="28411-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="28411-129">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="28411-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="28411-130">**ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="28411-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="28411-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="28411-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




