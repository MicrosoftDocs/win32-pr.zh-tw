---
description: 取得與這個替代相關聯的 ICoNtextNode 物件。
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate：： GetAlternateNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979736"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="0bfe7-103">IAnalysisAlternate：： GetAlternateNodes 方法</span><span class="sxs-lookup"><span data-stu-id="0bfe7-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="0bfe7-104">取得與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bfe7-105">語法</span><span class="sxs-lookup"><span data-stu-id="0bfe7-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="0bfe7-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bfe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bfe7-107">*ppAlternateNodes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0bfe7-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bfe7-108">[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bfe7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bfe7-109">Return value</span></span>

<span data-ttu-id="0bfe7-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0bfe7-111">備註</span><span class="sxs-lookup"><span data-stu-id="0bfe7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0bfe7-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點集合時，請在 *ppAlternateNodes* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="0bfe7-113">這個方法會傳回與這個替代相關聯的分葉內容節點。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="0bfe7-114">分葉節點的範例包括 InkWord、TextWord、Image、InkDrawing 和 InkBullet 內容節點。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="0bfe7-115">如需詳細資訊，請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [CoNtext 節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="0bfe7-116">因為它們對應至替代專案，所以這些 [**ICoNtextNode**](icontextnode.md) 物件不是 [**IInkAnalyzer**](iinkanalyzer.md) 物件根 **ICoNtextNode** 的下階 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) ，除非它們是最上層的替代專案，也就是 [**IAnalysisAlternates**](ianalysisalternates.md) 集合中的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="0bfe7-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bfe7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bfe7-117">Requirements</span></span>



| <span data-ttu-id="0bfe7-118">需求</span><span class="sxs-lookup"><span data-stu-id="0bfe7-118">Requirement</span></span> | <span data-ttu-id="0bfe7-119">值</span><span class="sxs-lookup"><span data-stu-id="0bfe7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfe7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bfe7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0bfe7-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bfe7-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0bfe7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bfe7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0bfe7-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="0bfe7-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0bfe7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0bfe7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bfe7-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0bfe7-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0bfe7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0bfe7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bfe7-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bfe7-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0bfe7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bfe7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bfe7-129">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="0bfe7-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="0bfe7-130">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="0bfe7-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0bfe7-131">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="0bfe7-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="0bfe7-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="0bfe7-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="0bfe7-133">AnalysisCore. AnalysisAlternateBase. AlternateNodes</span><span class="sxs-lookup"><span data-stu-id="0bfe7-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

