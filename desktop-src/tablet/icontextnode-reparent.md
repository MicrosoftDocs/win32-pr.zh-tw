---
description: 將這個 ICoNtextNode 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'ICoNtextNode：：重做方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026254"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="7b1d1-103">ICoNtextNode：：重做方法</span><span class="sxs-lookup"><span data-stu-id="7b1d1-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="7b1d1-104">將這個 [**ICoNtextNode**](icontextnode.md) 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。</span><span class="sxs-lookup"><span data-stu-id="7b1d1-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b1d1-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="7b1d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="7b1d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1d1-107">*pNewParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b1d1-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1d1-108">這個 [**ICoNtextNode**](icontextnode.md) 物件的新父節點。</span><span class="sxs-lookup"><span data-stu-id="7b1d1-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1d1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b1d1-109">Return value</span></span>

<span data-ttu-id="7b1d1-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="7b1d1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1d1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b1d1-111">Requirements</span></span>



| <span data-ttu-id="7b1d1-112">需求</span><span class="sxs-lookup"><span data-stu-id="7b1d1-112">Requirement</span></span> | <span data-ttu-id="7b1d1-113">值</span><span class="sxs-lookup"><span data-stu-id="7b1d1-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1d1-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b1d1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7b1d1-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b1d1-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b1d1-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b1d1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7b1d1-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b1d1-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b1d1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7b1d1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b1d1-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7b1d1-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b1d1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7b1d1-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b1d1-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b1d1-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b1d1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b1d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1d1-123">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="7b1d1-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7b1d1-124">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="7b1d1-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="7b1d1-125">**ICoNtextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="7b1d1-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="7b1d1-126">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7b1d1-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




