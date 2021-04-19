---
description: 抓取 ICoNtextLink 物件的集合，這些物件表示與其他 ICoNtextNode 物件的關聯性。
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'ICoNtextNode：： GetCoNtextLinks 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991745"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="c0e42-103">ICoNtextNode：： GetCoNtextLinks 方法</span><span class="sxs-lookup"><span data-stu-id="c0e42-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="c0e42-104">抓取 [**ICoNtextLink**](icontextlink.md) 物件的集合，這些物件表示與其他 [**ICoNtextNode**](icontextnode.md) 物件的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c0e42-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e42-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0e42-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="c0e42-106">參數</span><span class="sxs-lookup"><span data-stu-id="c0e42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e42-107">*ppCoNtextLinks* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0e42-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0e42-108">[**ICoNtextLink**](icontextlink.md)物件集合的指標，表示與其他 [**ICoNtextNode**](icontextnode.md)物件的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c0e42-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e42-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0e42-109">Return value</span></span>

<span data-ttu-id="c0e42-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e42-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e42-111">備註</span><span class="sxs-lookup"><span data-stu-id="c0e42-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c0e42-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容連結集合時，請在 *ppCoNtextLinks* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="c0e42-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="c0e42-113">若要取得父節點或子節點關聯性的相關資訊，請使用 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 或 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e42-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="c0e42-114">如需連結所描述之關聯性類型的詳細資訊，請參閱 [**ICoNtextLink**](icontextlink.md) 和 [**CoNtextLinkDirection**](contextlinkdirection.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e42-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e42-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0e42-115">Requirements</span></span>



| <span data-ttu-id="c0e42-116">需求</span><span class="sxs-lookup"><span data-stu-id="c0e42-116">Requirement</span></span> | <span data-ttu-id="c0e42-117">值</span><span class="sxs-lookup"><span data-stu-id="c0e42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e42-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0e42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e42-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0e42-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c0e42-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0e42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e42-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="c0e42-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c0e42-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c0e42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0e42-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c0e42-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c0e42-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e42-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0e42-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0e42-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c0e42-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0e42-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e42-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="c0e42-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c0e42-128">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="c0e42-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="c0e42-129">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="c0e42-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="c0e42-130">**ICoNtextNode::AddCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="c0e42-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="c0e42-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c0e42-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

