---
description: 建立子 ICoNtextNode 物件，其中只包含型別、識別碼和位置的相關資訊。
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'ICoNtextNode：： CreatePartiallyPopulatedSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848093"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="b730c-103">ICoNtextNode：： CreatePartiallyPopulatedSubNode 方法</span><span class="sxs-lookup"><span data-stu-id="b730c-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="b730c-104">建立子 [**ICoNtextNode**](icontextnode.md) 物件，其中只包含型別、識別碼和位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b730c-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="b730c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b730c-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="b730c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b730c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b730c-107">*pNodeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b730c-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b730c-108">要建立之內容節點的型別。</span><span class="sxs-lookup"><span data-stu-id="b730c-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="b730c-109">*pNodeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b730c-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b730c-110">新節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b730c-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="b730c-111">*pNodeLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b730c-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b730c-112">新節點的位置。</span><span class="sxs-lookup"><span data-stu-id="b730c-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="b730c-113">*pPartiallyPopulatedCoNtextNodeCreated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b730c-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b730c-114">新的部分填入 [**ICoNtextNode**](icontextnode.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="b730c-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b730c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b730c-115">Return value</span></span>

<span data-ttu-id="b730c-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b730c-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b730c-117">備註</span><span class="sxs-lookup"><span data-stu-id="b730c-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b730c-118">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *pPartiallyPopulatedCoNtextNodeCreated* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="b730c-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="b730c-119">新的 [**ICoNtextNode**](icontextnode.md) 會加入至此內容節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b730c-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="b730c-120">當有現有的子節點時，新建立的 **ICoNtextNode** 會加入做為最後一個子節點。</span><span class="sxs-lookup"><span data-stu-id="b730c-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="b730c-121">如需類型、識別碼和位置的詳細資訊，請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)、 [**ICoNtextNode：： GetId**](icontextnode-getid.md)和 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)。</span><span class="sxs-lookup"><span data-stu-id="b730c-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="b730c-122">此方法是用來在內容節點樹狀結構中，用來建立 [**ICoNtextNode**](icontextnode.md) 物件的方法，然後才能使用它的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b730c-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="b730c-123">如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b730c-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b730c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b730c-124">Requirements</span></span>



| <span data-ttu-id="b730c-125">需求</span><span class="sxs-lookup"><span data-stu-id="b730c-125">Requirement</span></span> | <span data-ttu-id="b730c-126">值</span><span class="sxs-lookup"><span data-stu-id="b730c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b730c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b730c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b730c-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b730c-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b730c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b730c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b730c-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="b730c-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b730c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b730c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b730c-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b730c-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b730c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b730c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b730c-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b730c-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b730c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b730c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b730c-136">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b730c-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b730c-137">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="b730c-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b730c-138">**ICoNtextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="b730c-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="b730c-139">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="b730c-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="b730c-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b730c-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

