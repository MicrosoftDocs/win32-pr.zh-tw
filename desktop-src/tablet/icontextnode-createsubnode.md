---
description: 建立新的子 ICoNtextNode 物件。
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'ICoNtextNode：： CreateSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848092"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="c500e-103">ICoNtextNode：： CreateSubNode 方法</span><span class="sxs-lookup"><span data-stu-id="c500e-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="c500e-104">建立新的子 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c500e-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c500e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c500e-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="c500e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c500e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c500e-107">*pNodeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c500e-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c500e-108">**GUID** ，代表要建立的 [**ICoNtextNode**](icontextnode.md)類型。</span><span class="sxs-lookup"><span data-stu-id="c500e-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="c500e-109">*ppCoNtextNodeCreated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c500e-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c500e-110">新 [**ICoNtextNode**](icontextnode.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="c500e-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c500e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c500e-111">Return value</span></span>

<span data-ttu-id="c500e-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c500e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c500e-113">備註</span><span class="sxs-lookup"><span data-stu-id="c500e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c500e-114">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *ppCoNtextNodeCreated* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="c500e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="c500e-115">新的 [**ICoNtextNode**](icontextnode.md) 會加入至此內容節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c500e-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="c500e-116">當有現有的子節點時，新建立的 **ICoNtextNode** 會加入做為最後一個子節點。</span><span class="sxs-lookup"><span data-stu-id="c500e-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="c500e-117">如需內容節點類型的清單，請參閱 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c500e-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c500e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c500e-118">Requirements</span></span>



| <span data-ttu-id="c500e-119">需求</span><span class="sxs-lookup"><span data-stu-id="c500e-119">Requirement</span></span> | <span data-ttu-id="c500e-120">值</span><span class="sxs-lookup"><span data-stu-id="c500e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c500e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c500e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c500e-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c500e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c500e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c500e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c500e-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="c500e-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c500e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c500e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c500e-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c500e-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c500e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c500e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c500e-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c500e-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c500e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c500e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c500e-130">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="c500e-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c500e-131">**ICoNtextNode：:D eleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="c500e-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="c500e-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c500e-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

