---
description: 在衍生類別中覆寫時，評估指定的 ICoNtextNode 物件是否符合準則。
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack：： EvaluateCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971203"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="bd097-103">IMatchesCriteriaCallBack：： EvaluateCoNtextNode 方法</span><span class="sxs-lookup"><span data-stu-id="bd097-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="bd097-104">在衍生類別中覆寫時，評估指定的 [**ICoNtextNode**](icontextnode.md) 物件是否符合準則。</span><span class="sxs-lookup"><span data-stu-id="bd097-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd097-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd097-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="bd097-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd097-107">*pCoNtextNodeToEvaluate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd097-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd097-108">要評估的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="bd097-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="bd097-109">*pbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bd097-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd097-110">**變異 \_** 如果 *pCoNtextNodeToEvaluate* 符合條件，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bd097-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd097-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd097-111">Return value</span></span>

<span data-ttu-id="bd097-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="bd097-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd097-113">備註</span><span class="sxs-lookup"><span data-stu-id="bd097-113">Remarks</span></span>

<span data-ttu-id="bd097-114">若要使用 [**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md) 或 [**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)，請建立可執行 [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)的類別。</span><span class="sxs-lookup"><span data-stu-id="bd097-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="bd097-115">如果 [**ICoNtextNode**](icontextnode.md)物件符合您的準則，請執行 **IMatchesCriteriaCallBack：： EvaluateCoNtextNode** 傳回 **Variant \_ TRUE** ，否則傳回 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bd097-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="bd097-116">針對某些準則，您可能需要提供方法來初始化或維護 **IMatchesCriteriaCallBack** 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd097-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd097-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd097-117">Requirements</span></span>



| <span data-ttu-id="bd097-118">需求</span><span class="sxs-lookup"><span data-stu-id="bd097-118">Requirement</span></span> | <span data-ttu-id="bd097-119">值</span><span class="sxs-lookup"><span data-stu-id="bd097-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd097-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd097-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd097-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd097-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd097-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd097-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd097-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="bd097-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bd097-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bd097-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd097-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="bd097-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bd097-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bd097-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd097-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd097-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bd097-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd097-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd097-129">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="bd097-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="bd097-130">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="bd097-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="bd097-131">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="bd097-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="bd097-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="bd097-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




