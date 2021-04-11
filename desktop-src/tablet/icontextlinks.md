---
description: 包含物件的集合，這些物件會執行 ICoNtextLink 介面。
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: 'ICoNtextLinks 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943472"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="a8176-103">ICoNtextLinks 介面</span><span class="sxs-lookup"><span data-stu-id="a8176-103">IContextLinks interface</span></span>

<span data-ttu-id="a8176-104">包含物件的集合，這些物件會執行 [**ICoNtextLink**](icontextlink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="a8176-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a8176-105">成員</span><span class="sxs-lookup"><span data-stu-id="a8176-105">Members</span></span>

<span data-ttu-id="a8176-106">**ICoNtextLinks** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a8176-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8176-107">**ICoNtextLinks** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8176-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="a8176-108">方法</span><span class="sxs-lookup"><span data-stu-id="a8176-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8176-109">方法</span><span class="sxs-lookup"><span data-stu-id="a8176-109">Methods</span></span>

<span data-ttu-id="a8176-110">**ICoNtextLinks** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a8176-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="a8176-111">方法</span><span class="sxs-lookup"><span data-stu-id="a8176-111">Method</span></span>                                                 | <span data-ttu-id="a8176-112">描述</span><span class="sxs-lookup"><span data-stu-id="a8176-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8176-113">**GetCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="a8176-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="a8176-114">抓取位於指定之索引處的 [**ICoNtextLink**](icontextlink.md) 。</span><span class="sxs-lookup"><span data-stu-id="a8176-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="a8176-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="a8176-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="a8176-116">抓取這個集合中的 [**ICoNtextLink**](icontextlink.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="a8176-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8176-117">備註</span><span class="sxs-lookup"><span data-stu-id="a8176-117">Remarks</span></span>

<span data-ttu-id="a8176-118">這通常是透過 [**ICoNtextNode：： GetCoNtextLinks**](icontextnode-getcontextlinks.md) 方法來存取。</span><span class="sxs-lookup"><span data-stu-id="a8176-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8176-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8176-119">Requirements</span></span>



| <span data-ttu-id="a8176-120">需求</span><span class="sxs-lookup"><span data-stu-id="a8176-120">Requirement</span></span> | <span data-ttu-id="a8176-121">值</span><span class="sxs-lookup"><span data-stu-id="a8176-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8176-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8176-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8176-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8176-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8176-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8176-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8176-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="a8176-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a8176-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a8176-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8176-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a8176-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8176-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a8176-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8176-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8176-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a8176-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8176-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8176-131">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="a8176-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="a8176-132">**ICoNtextNode::AddCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="a8176-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="a8176-133">**ICoNtextNode：:D eleteCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="a8176-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="a8176-134">**ICoNtextNode::GetCoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="a8176-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="a8176-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="a8176-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

