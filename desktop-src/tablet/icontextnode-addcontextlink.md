---
description: 將新的 ICoNtextLink 加入至 ICoNtextNode 物件的內容連結集合。
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'ICoNtextNode：： AddCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972870"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="5d0c3-103">ICoNtextNode：： AddCoNtextLink 方法</span><span class="sxs-lookup"><span data-stu-id="5d0c3-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="5d0c3-104">將新的 [**ICoNtextLink**](icontextlink.md) 加入至 [**ICoNtextNode**](icontextnode.md) 物件的內容連結集合。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d0c3-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="5d0c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="5d0c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d0c3-107">*pDestinationNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d0c3-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d0c3-108">新 [**ICoNtextLink**](icontextlink.md)的目的地 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d0c3-109">*linkDirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d0c3-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d0c3-110">要建立之 [**ICoNtextLink**](icontextlink.md) 物件的方向。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="5d0c3-111">*ppCoNtextLinkToAdd* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5d0c3-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d0c3-112">新 [**ICoNtextLink**](icontextlink.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d0c3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d0c3-113">Return value</span></span>

<span data-ttu-id="5d0c3-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0c3-115">備註</span><span class="sxs-lookup"><span data-stu-id="5d0c3-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5d0c3-116">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *ppCoNtextLinkToAdd* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="5d0c3-117">這個 [**ICoNtextNode**](icontextnode.md) 物件是來源節點 (請參閱 [**ICoNtextLink：： GetSourceNode**](icontextlink-getsourcenode.md)) 以取得新的 [**ICoNtextLink**](icontextlink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5d0c3-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0c3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d0c3-118">Requirements</span></span>



| <span data-ttu-id="5d0c3-119">需求</span><span class="sxs-lookup"><span data-stu-id="5d0c3-119">Requirement</span></span> | <span data-ttu-id="5d0c3-120">值</span><span class="sxs-lookup"><span data-stu-id="5d0c3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0c3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d0c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0c3-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d0c3-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5d0c3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d0c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0c3-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d0c3-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5d0c3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5d0c3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d0c3-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="5d0c3-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5d0c3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5d0c3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d0c3-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d0c3-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5d0c3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d0c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0c3-130">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-131">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-132">**ICoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-133">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-134">**ICoNtextNode：:D eleteCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-135">**ICoNtextNode::GetCoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="5d0c3-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="5d0c3-136">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="5d0c3-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

