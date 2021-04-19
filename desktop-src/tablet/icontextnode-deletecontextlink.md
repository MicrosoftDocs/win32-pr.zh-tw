---
description: 從 ICoNtextNode 物件的連結集合中刪除 ICoNtextLink 物件。
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: 'ICoNtextNode：:D eleteCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973858"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="9d80b-103">ICoNtextNode：:D eleteCoNtextLink 方法</span><span class="sxs-lookup"><span data-stu-id="9d80b-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="9d80b-104">從 [**ICoNtextNode**](icontextnode.md)物件的連結集合中刪除 [**ICoNtextLink**](icontextlink.md)物件。</span><span class="sxs-lookup"><span data-stu-id="9d80b-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d80b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d80b-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="9d80b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d80b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d80b-107">*pCoNtextLinkToDelete* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d80b-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d80b-108">要刪除的 [**ICoNtextLink**](icontextlink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9d80b-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d80b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d80b-109">Return value</span></span>

<span data-ttu-id="9d80b-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="9d80b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d80b-111">備註</span><span class="sxs-lookup"><span data-stu-id="9d80b-111">Remarks</span></span>

<span data-ttu-id="9d80b-112">內容連結具有來源節點和目的地節點 (請參閱 [**ICoNtextLink：： GetSourceNode**](icontextlink-getsourcenode.md) 和 [**ICoNtextLink：： GetDestinationNode**](icontextlink-getdestinationnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9d80b-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="9d80b-113">這個方法會從來源和目的地節點的內容連結集合中移除 [**ICoNtextLink**](icontextlink.md) ， (參閱 [**ICoNtextNode：： GetCoNtextLinks**](icontextnode-getcontextlinks.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9d80b-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d80b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d80b-114">Requirements</span></span>



| <span data-ttu-id="9d80b-115">需求</span><span class="sxs-lookup"><span data-stu-id="9d80b-115">Requirement</span></span> | <span data-ttu-id="9d80b-116">值</span><span class="sxs-lookup"><span data-stu-id="9d80b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d80b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d80b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d80b-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d80b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9d80b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d80b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d80b-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="9d80b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9d80b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9d80b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d80b-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="9d80b-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9d80b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9d80b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d80b-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d80b-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9d80b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d80b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d80b-126">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="9d80b-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9d80b-127">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="9d80b-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="9d80b-128">**ICoNtextNode::AddCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="9d80b-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="9d80b-129">**ICoNtextNode::GetCoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="9d80b-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="9d80b-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="9d80b-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




