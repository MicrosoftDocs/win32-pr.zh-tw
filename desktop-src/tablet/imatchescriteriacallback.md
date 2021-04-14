---
description: 公開方法，以評估 ICoNtextNode 物件是否符合或失敗指定的條件。
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: 'IMatchesCriteriaCallBack 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511035"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="debe8-103">IMatchesCriteriaCallBack 介面</span><span class="sxs-lookup"><span data-stu-id="debe8-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="debe8-104">公開方法，以評估 [**ICoNtextNode**](icontextnode.md) 物件是否符合或失敗指定的條件。</span><span class="sxs-lookup"><span data-stu-id="debe8-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="debe8-105">成員</span><span class="sxs-lookup"><span data-stu-id="debe8-105">Members</span></span>

<span data-ttu-id="debe8-106">**IMatchesCriteriaCallBack** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="debe8-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="debe8-107">**IMatchesCriteriaCallBack** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="debe8-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="debe8-108">方法</span><span class="sxs-lookup"><span data-stu-id="debe8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="debe8-109">方法</span><span class="sxs-lookup"><span data-stu-id="debe8-109">Methods</span></span>

<span data-ttu-id="debe8-110">**IMatchesCriteriaCallBack** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="debe8-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="debe8-111">方法</span><span class="sxs-lookup"><span data-stu-id="debe8-111">Method</span></span>                                                                      | <span data-ttu-id="debe8-112">描述</span><span class="sxs-lookup"><span data-stu-id="debe8-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="debe8-113">**EvaluateCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="debe8-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="debe8-114">在衍生類別中覆寫時，評估指定的 [**ICoNtextNode**](icontextnode.md) 物件是否符合準則。</span><span class="sxs-lookup"><span data-stu-id="debe8-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="debe8-115">備註</span><span class="sxs-lookup"><span data-stu-id="debe8-115">Remarks</span></span>

<span data-ttu-id="debe8-116">若要使用 [**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md) 或 [**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)，請建立可執行 **IMatchesCriteriaCallBack** 的類別。</span><span class="sxs-lookup"><span data-stu-id="debe8-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="debe8-117">如果 [**ICoNtextNode**](icontextnode.md)物件符合您的準則，請執行 [**IMatchesCriteriaCallBack：： EvaluateCoNtextNode**](imatchescriteriacallback-evaluatecontextnode.md)傳回 **Variant \_ TRUE** ，否則傳回 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="debe8-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="debe8-118">針對某些準則，您可能需要提供方法來初始化或維護 **IMatchesCriteriaCallBack** 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="debe8-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="debe8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="debe8-119">Requirements</span></span>



| <span data-ttu-id="debe8-120">需求</span><span class="sxs-lookup"><span data-stu-id="debe8-120">Requirement</span></span> | <span data-ttu-id="debe8-121">值</span><span class="sxs-lookup"><span data-stu-id="debe8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="debe8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="debe8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="debe8-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="debe8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="debe8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="debe8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="debe8-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="debe8-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="debe8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="debe8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="debe8-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="debe8-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="debe8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="debe8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="debe8-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="debe8-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="debe8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="debe8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debe8-131">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="debe8-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="debe8-132">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="debe8-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="debe8-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="debe8-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

