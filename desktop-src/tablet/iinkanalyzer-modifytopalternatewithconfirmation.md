---
description: 將目前的上方替代變更為指定的 IAnalysisAlternate。
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318452"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="1bc3d-103">IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法</span><span class="sxs-lookup"><span data-stu-id="1bc3d-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="1bc3d-104">將目前的上方替代變更為指定的 [**IAnalysisAlternate**](ianalysisalternate.md)。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc3d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1bc3d-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="1bc3d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1bc3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc3d-107">*替代* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bc3d-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc3d-108">要設定為新的 top 替代的分析替代。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="1bc3d-109">*fconfirmAutomatically* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bc3d-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc3d-110">**變異 \_TRUE** 表示將對應至分析替代的所有筆墨分葉內容節點設定為 **ConfirmationType \_ NodeTypeAndProperties** 的確認類型 (請參閱 [**ICoNtextNode：： IsConfirmed**](icontextnode-isconfirmed.md) 和 [**ConfirmationType**](confirmationtype.md)) ; **變異 \_FALSE** 表示將對應至分析替代的所有筆墨分葉內容節點設定為 **ConfirmationType \_ None** 的確認類型。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc3d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bc3d-111">Return value</span></span>

<span data-ttu-id="1bc3d-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc3d-113">備註</span><span class="sxs-lookup"><span data-stu-id="1bc3d-113">Remarks</span></span>

<span data-ttu-id="1bc3d-114">若要取得分析替代項，請使用 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)、 [**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)或 [**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="1bc3d-115">若要取得與分析替代相關聯的內容節點物件，請使用 [**IAnalysisAlternate：： GetAlternateNodes 方法**](ianalysisalternate-getalternatenodes.md)。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="1bc3d-116">若要變更內容節點的確認類型，請使用 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)。</span><span class="sxs-lookup"><span data-stu-id="1bc3d-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bc3d-117">Requirements</span></span>



| <span data-ttu-id="1bc3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1bc3d-118">Requirement</span></span> | <span data-ttu-id="1bc3d-119">值</span><span class="sxs-lookup"><span data-stu-id="1bc3d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc3d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bc3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc3d-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bc3d-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1bc3d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bc3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc3d-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="1bc3d-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1bc3d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1bc3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bc3d-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1bc3d-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1bc3d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc3d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc3d-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc3d-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1bc3d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bc3d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc3d-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1bc3d-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1bc3d-130">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="1bc3d-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="1bc3d-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="1bc3d-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1bc3d-132">**筆墨分析 ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="1bc3d-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="1bc3d-133">參考</span><span class="sxs-lookup"><span data-stu-id="1bc3d-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




