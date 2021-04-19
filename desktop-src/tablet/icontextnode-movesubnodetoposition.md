---
description: 將指定的子 ICoNtextNode 物件重新排序為指定的索引。
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'ICoNtextNode：： MoveSubNodeToPosition 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972869"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="d6d41-103">ICoNtextNode：： MoveSubNodeToPosition 方法</span><span class="sxs-lookup"><span data-stu-id="d6d41-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="d6d41-104">將指定的子 [**ICoNtextNode**](icontextnode.md) 物件重新排序為指定的索引。</span><span class="sxs-lookup"><span data-stu-id="d6d41-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d41-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6d41-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d6d41-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6d41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d41-107">*pSubnodeToMove* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6d41-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d41-108">要移動的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d6d41-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="d6d41-109">*ulNewIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6d41-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d41-110">子節點新位置的索引。</span><span class="sxs-lookup"><span data-stu-id="d6d41-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d41-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6d41-111">Return value</span></span>

<span data-ttu-id="d6d41-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d6d41-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d41-113">備註</span><span class="sxs-lookup"><span data-stu-id="d6d41-113">Remarks</span></span>

<span data-ttu-id="d6d41-114">如果 *pSubnodeToMove* 不是此 [**ICoNtextNode**](icontextnode.md)的子節點，則傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="d6d41-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d41-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6d41-115">Requirements</span></span>



| <span data-ttu-id="d6d41-116">需求</span><span class="sxs-lookup"><span data-stu-id="d6d41-116">Requirement</span></span> | <span data-ttu-id="d6d41-117">值</span><span class="sxs-lookup"><span data-stu-id="d6d41-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d41-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6d41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d41-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6d41-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d6d41-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6d41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d41-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="d6d41-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d6d41-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d6d41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6d41-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d6d41-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d6d41-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d41-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d41-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d41-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d6d41-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6d41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d41-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="d6d41-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d6d41-128">**ICoNtextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="d6d41-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="d6d41-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d6d41-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




