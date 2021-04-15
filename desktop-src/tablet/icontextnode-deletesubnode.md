---
description: 移除子 ICoNtextNode。
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: 'ICoNtextNode：:D eleteSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511681"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="e670c-103">ICoNtextNode：:D eleteSubNode 方法</span><span class="sxs-lookup"><span data-stu-id="e670c-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="e670c-104">移除子 [**ICoNtextNode**](icontextnode.md)。</span><span class="sxs-lookup"><span data-stu-id="e670c-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e670c-105">語法</span><span class="sxs-lookup"><span data-stu-id="e670c-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="e670c-106">參數</span><span class="sxs-lookup"><span data-stu-id="e670c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e670c-107">*pCoNtextNodeToDelete* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e670c-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e670c-108">要移除的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="e670c-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e670c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e670c-109">Return value</span></span>

<span data-ttu-id="e670c-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e670c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e670c-111">備註</span><span class="sxs-lookup"><span data-stu-id="e670c-111">Remarks</span></span>

<span data-ttu-id="e670c-112">\_如果 *pCoNtextNodeToDelete* 參數不是這個 [**ICoNtextNode**](icontextnode.md)物件的子系，則會傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="e670c-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e670c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e670c-113">Requirements</span></span>



| <span data-ttu-id="e670c-114">需求</span><span class="sxs-lookup"><span data-stu-id="e670c-114">Requirement</span></span> | <span data-ttu-id="e670c-115">值</span><span class="sxs-lookup"><span data-stu-id="e670c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e670c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e670c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e670c-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e670c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e670c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e670c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e670c-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="e670c-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e670c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e670c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e670c-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e670c-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e670c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e670c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e670c-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e670c-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e670c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e670c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e670c-125">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="e670c-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e670c-126">**ICoNtextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="e670c-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="e670c-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e670c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




