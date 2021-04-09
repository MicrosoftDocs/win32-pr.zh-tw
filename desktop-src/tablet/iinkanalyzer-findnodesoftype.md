---
description: 抓取指定類型的所有 ICoNtextNode 物件。
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'IInkAnalyzer：： FindNodesOfType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848077"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="52454-103">IInkAnalyzer：： FindNodesOfType 方法</span><span class="sxs-lookup"><span data-stu-id="52454-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="52454-104">抓取指定類型的所有 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="52454-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="52454-105">語法</span><span class="sxs-lookup"><span data-stu-id="52454-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="52454-106">參數</span><span class="sxs-lookup"><span data-stu-id="52454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52454-107">*pNodeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52454-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52454-108">指定節點類型的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="52454-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="52454-109">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="52454-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52454-110">[**ICoNtextNodes**](icontextnodes.md)的指標，其中包含 *pNodeType* 類型的所有節點。</span><span class="sxs-lookup"><span data-stu-id="52454-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52454-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="52454-111">Return value</span></span>

<span data-ttu-id="52454-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="52454-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52454-113">備註</span><span class="sxs-lookup"><span data-stu-id="52454-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="52454-114">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="52454-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="52454-115">*PNodeType* 屬性必須包含來自 [內容節點類型](context-node-types.md)常數的 GUID。</span><span class="sxs-lookup"><span data-stu-id="52454-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="52454-116">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="52454-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="52454-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="52454-117">Requirements</span></span>



| <span data-ttu-id="52454-118">需求</span><span class="sxs-lookup"><span data-stu-id="52454-118">Requirement</span></span> | <span data-ttu-id="52454-119">值</span><span class="sxs-lookup"><span data-stu-id="52454-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52454-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52454-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52454-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52454-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="52454-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52454-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52454-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="52454-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="52454-124">標頭</span><span class="sxs-lookup"><span data-stu-id="52454-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="52454-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="52454-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="52454-126">DLL</span><span class="sxs-lookup"><span data-stu-id="52454-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52454-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52454-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="52454-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52454-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52454-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="52454-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="52454-130">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="52454-131">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="52454-132">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="52454-133">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="52454-134">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="52454-135">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="52454-136">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="52454-137">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="52454-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="52454-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="52454-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

