---
description: 抓取指定之 ICoNtextNode 物件的子系之指定型別的所有 ICoNtextNode 物件。
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'IInkAnalyzer：： FindNodesOfTypeInSubTree 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998069"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="7b9b3-103">IInkAnalyzer：： FindNodesOfTypeInSubTree 方法</span><span class="sxs-lookup"><span data-stu-id="7b9b3-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="7b9b3-104">抓取指定之 **ICoNtextNode** 物件的子系之指定型別的所有 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b9b3-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="7b9b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="7b9b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b9b3-107">*pNodeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b9b3-108">指定節點類型的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b3-109">*pCoNtextNodeToSearchFrom* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b9b3-110">要搜尋其子系的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b3-111">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b9b3-112">[**ICoNtextNodes**](icontextnodes.md)集合，其中包含型別為 *pNodeType* 的所有節點，這些節點是 *pCoNtextNodeToSearchFrom* 的子系。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b9b3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b9b3-113">Return value</span></span>

<span data-ttu-id="7b9b3-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b9b3-115">備註</span><span class="sxs-lookup"><span data-stu-id="7b9b3-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7b9b3-116">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="7b9b3-117">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含 *pCoNtextNodeToSearchFrom* 節點，這個方法會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="7b9b3-118">*PNodeType* 屬性必須包含全域唯一識別碼， (GUID) 來自 [內容節點類型](context-node-types.md)常數。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="7b9b3-119">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="7b9b3-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9b3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b9b3-120">Requirements</span></span>



| <span data-ttu-id="7b9b3-121">需求</span><span class="sxs-lookup"><span data-stu-id="7b9b3-121">Requirement</span></span> | <span data-ttu-id="7b9b3-122">值</span><span class="sxs-lookup"><span data-stu-id="7b9b3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9b3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b9b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9b3-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b9b3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b9b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9b3-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b9b3-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b9b3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="7b9b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9b3-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7b9b3-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b9b3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7b9b3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b9b3-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b9b3-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b9b3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b9b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9b3-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-133">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-134">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-135">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-136">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-137">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-138">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-139">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-140">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7b9b3-141">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7b9b3-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

